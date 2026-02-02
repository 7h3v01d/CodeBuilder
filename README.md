# 🛠️ CodeBuilder (Archived)

A multi-language **compile & run** tool for local source files and GitHub repositories.

This project is archived and represents an early exploration into **automated code execution, build orchestration, and tooling across multiple programming languages**.

---

### 🚀 What is CodeBuilder?

CodeBuilder was an experiment in answering a simple question:

> “Can I take *any* source file, figure out what language it’s written in, compile it if needed, run it, and capture the results?”

The answer turned out to be: *yes — but it opens a lot of interesting doors.*

---

### ✨ What it can do

- 🔍 **Automatically detect programming language**
- ⚙️ **Compile code where required**
- ▶️ **Run executables or scripts**
- 📜 **Capture output and exit status**
- 🧾 **Log build/run results to disk**
- 🌐 **Clone and work with GitHub repositories** (early support)

Supported languages include:
- Python
- C
- C++
- C#
- Java
- Rust
- Go

---

### 🧠 How it works

1. Detect language from file extension
2. Route execution to a language-specific handler
3. Compile (if applicable)
4. Run the result
5. Capture output and return codes
6. Persist logs for inspection

Each language lives in its own module to keep responsibilities clean.

---

### 🗂️ Project structure
```text
codebuilder/
├── main.py
├── pyproject.toml
├── languages/
│ ├── python.py
│ ├── c.py
│ ├── cpp.py
│ ├── csharp.py
│ ├── java.py
│ ├── rust.py
│ └── go.py
├── utils/
│ ├── detector.py
│ ├── github_fetcher.py
│ └── logger.py
└── build_logs/
```

---

### ▶️ Usage

Run CodeBuilder on a local file:

```bash
python main.py path/to/source_file
```
The tool will:

- detect the language
- compile if needed
- run the program
- save logs in build_logs/

### ⚠️ Project status

Archived / Early Prototype

- Toolchains must already be installed (gcc, javac, rustc, etc.)
- No sandboxing or containerization
- Minimal error recovery
- GitHub support is basic

This repo exists as a learning artifact and foundation, not a finished product.

### 💡 If revisited someday…
Natural next steps would include:

- Docker-based sandboxing
- project-level builds (not just single files)
- language config files
- CI-style test runners
- GUI or web interface
- security hardening

### 📜 License
MIT (as defined in pyproject.toml).

### 🏷️ Status
Archived — raw, ambitious, and foundational.

This project marks an early step toward tool-building and multi-language orchestration ideas.

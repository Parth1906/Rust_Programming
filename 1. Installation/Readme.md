# 🦀 Chapter 1: Installing and Setting Up Rust

Welcome to **Chapter 1** of my **Rust Programming Course Repository**!  
In this chapter, we’ll cover everything you need to **install Rust**, verify your setup, and get ready to start coding.

Rust is a modern systems programming language focused on **safety**, **speed**, and **concurrency** — without sacrificing developer productivity.  
Before writing your first line of Rust code, you need to set up your development environment.

---

## 📦 Step 1: Installing Rust via `rustup`

The easiest and most reliable way to install Rust is using **rustup**,  
a command-line tool that manages Rust versions and associated tools.

> 🛠️ **Note:** You’ll need an active internet connection to download Rust and its components.

### 🔹 On Linux or macOS

Open your terminal and run:

```bash
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

This command:
1. Downloads the official installation script securely.
2. Installs `rustup`, which in turn installs the latest **stable Rust compiler** and **Cargo**, Rust’s package manager.

You might be asked to enter your password during installation.  
Once completed, you’ll see a message like:

```
Rust is installed now. Great!
```

---

### 🔹 On Windows

1. Visit the official Rust installation page:  
   👉 [https://www.rust-lang.org/tools/install](https://www.rust-lang.org/tools/install)
2. Download and run the **Rust installer** (`rustup-init.exe`).
3. Follow the on-screen instructions and choose **default installation**.
4. When prompted, install **Visual Studio Build Tools** — this provides:
   - A **linker** (used to join compiled outputs)
   - Native Windows libraries required to compile Rust programs

If you need detailed instructions for this step, visit:  
🔗 [Rustup Windows Installation Guide](https://rust-lang.github.io/rustup/installation/windows-msvc.html)

---

## ⚙️ Step 2: Installing a C Compiler (Linker)

Rust requires a **linker** to create final executable files.

- **macOS:**  
  Run this command to install the Xcode command-line tools:
  ```bash
  xcode-select --install
  ```

- **Linux (Ubuntu example):**  
  Install GCC and essential build tools:
  ```bash
  sudo apt update
  sudo apt install build-essential
  ```

- **Windows:**  
  Installing Visual Studio Build Tools (as mentioned earlier) will automatically include a linker.

---

## 🧩 Step 3: Verify Installation

After installation, confirm Rust is working by checking the version.

Open a terminal (or PowerShell on Windows) and run:

```bash
rustc --version
```

You should see output similar to:

```
rustc 1.83.0 (abcabcabc 2025-09-10)
```

If you see this, 🎉 **Rust is successfully installed!**

---

## 🧠 Step 4: Understanding Command Line Notation

Throughout this course and official Rust documentation:

- `$` indicates a **terminal command** (Linux/macOS)
- `>` indicates a **PowerShell or CMD command** (Windows)

👉 You **do not** type the `$` or `>` characters — they just represent the command prompt.

Example:
```bash
$ rustc --version
```
is the same as typing just:
```bash
rustc --version
```

---

## 🧰 Step 5: Updating and Uninstalling Rust

To keep Rust up-to-date, use:

```bash
rustup update
```

To uninstall Rust completely:

```bash
rustup self uninstall
```

---

## 📚 Step 6: Accessing Local Documentation

Once installed, you can view Rust’s **official documentation offline** by running:

```bash
rustup doc
```

This opens a local copy of the Rust documentation in your default browser.  
You can refer to it anytime you want to learn about a function, type, or module.

---

## ✏️ Step 7: Choosing a Code Editor or IDE

Rust code can be written in any text editor, but for a smooth experience, use one of the following:

| Editor / IDE | Plugin / Extension | Notes |
|---------------|-------------------|--------|
| **VS Code** | [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer) | 🟢 Recommended |
| **IntelliJ IDEA / CLion** | Built-in Rust support | Great for debugging |
| **Neovim / Vim** | coc-rust-analyzer | Lightweight setup |
| **Sublime Text** | LSP-rust-analyzer | Simple and fast |

> 💡 Tip: Install **rust-analyzer** — it provides autocompletion, type hints, and inline error messages.

---

## 🌐 Step 8: Working Offline (Optional)

If you plan to work offline, cache dependencies by running:

```bash
cargo new get-dependencies
cd get-dependencies
cargo add rand@0.8.5 trpl@0.2.0
```

This will download and store required packages locally so that future builds can be run offline using:

```bash
cargo build --offline
```

---

## 🔍 Step 9: Troubleshooting

If `rustc --version` doesn’t work, ensure Rust is added to your system’s PATH.

- **Windows CMD:**
  ```bash
  echo %PATH%
  ```
- **PowerShell:**
  ```bash
  echo $env:Path
  ```
- **Linux / macOS:**
  ```bash
  echo $PATH
  ```

If everything looks correct but Rust still doesn’t run, visit the [Rust Community Page](https://www.rust-lang.org/community) for support and guidance.

---

## ✅ Summary

By the end of this chapter, you should have:

- Installed Rust using `rustup`
- Set up a linker and compiler tools
- Verified the Rust installation
- Accessed local documentation
- Chosen an editor or IDE for writing Rust code

You’re now ready to begin your **Rust programming journey** — next up:  
🚀 **Writing your first Rust program!**

---

**Author:** Parth Rewoo  
📘 *Part of my Rust Programming Course Repository*

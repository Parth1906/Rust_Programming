# 🦀 Chapter 2: Your First Rust Program — "Hello, World!"

Welcome to **Chapter 2** of my Rust Programming Course Repository!  
In this chapter, you’ll create and run your very first Rust program — the traditional **“Hello, World!”**. 🎉  

This exercise introduces you to:
- Creating Rust project directories  
- Writing Rust source code  
- Compiling and running Rust programs  
- Understanding the anatomy of a Rust function  
- How Rust’s compilation model differs from interpreted languages  

---

## 📁 Step 1: Create a Project Directory

It’s best practice to keep all your Rust code organized under a single `rust_projects` folder.  
Open your terminal and run the following commands to create the project structure.

### 🔹 For Linux, macOS, or PowerShell (Windows)

```bash
mkdir ~/rust_projects
cd ~/rust_projects
mkdir hello_world
cd hello_world
```

### 🔹 For Windows CMD

```cmd
mkdir "%USERPROFILE%\rust_projects"
cd /d "%USERPROFILE%\rust_projects"
mkdir hello_world
cd hello_world
```

---

## 🧾 Step 2: Create the Rust Source File

Inside the `hello_world` folder, create a new file named **`main.rs`**.

> 💡 Rust source files always end with `.rs`.  
> Use underscores (`_`) for multi-word file names — for example, `hello_world.rs`, not `helloworld.rs`.

Open the file in your preferred editor (VS Code, Vim, or any IDE) and add the following code:

### 🦀 **Filename:** `main.rs`
```rust
fn main() {
    println!("Hello, world!");
}
```

This simple program prints “Hello, world!” to the terminal.

---

## ⚙️ Step 3: Compile and Run the Program

Now let’s compile the program using the Rust compiler (`rustc`) and then execute the compiled binary.

### 🔹 On Linux / macOS
```bash
rustc main.rs
./main
```

### 🔹 On Windows (PowerShell or CMD)
```cmd
rustc main.rs
.\main
```

✅ **Expected Output:**
```
Hello, world!
```

If you see this message, congratulations — you’ve successfully written and executed your first Rust program! 🎉  
You’re now officially a **Rust programmer**.

---

## 🔍 Step 4: Understanding the Code

Let’s break down the “Hello, World!” program line by line.

```rust
fn main() {
```
- `fn` declares a **function**.
- `main` is the special entry point function in every Rust executable.
- The parentheses `()` mean the function takes **no parameters**.
- The curly braces `{}` define the start and end of the function body.

> 🧠 Rust requires braces `{}` around all function bodies.  
> Style tip: place the opening `{` on the same line as the function declaration.

```rust
    println!("Hello, world!");
```
- `println!` is a **Rust macro** that prints text to the screen.
- The exclamation mark (`!`) means it’s a **macro**, not a normal function.  
  Macros allow Rust to extend its syntax and generate code.
- `"Hello, world!"` is a **string literal** passed as an argument.
- The line ends with a **semicolon (;)**, marking the end of the statement.

```rust
}
```
- Closes the `main` function definition.

---

## 🧩 Step 5: Compiling and Output Files

When you compile the program with `rustc main.rs`, Rust generates a binary executable in the same directory.

### On Linux / macOS / PowerShell
```bash
ls
```
Output:
```
main  main.rs
```

### On Windows CMD
```cmd
dir /B
```
Output:
```
main.exe
main.pdb
main.rs
```

- `main.rs` → Your source code  
- `main` or `main.exe` → Compiled executable  
- `main.pdb` → (Windows only) Debug information  

You can now run the compiled file directly:

```bash
./main      # Linux/macOS
.\main      # Windows
```

---

## ⚡ Step 6: Compilation vs Interpretation

Rust is an **ahead-of-time compiled** language.  
That means once you compile a program, you get a standalone executable that can run **without needing Rust installed**.

### Comparison:

| Language | Compilation Model | Requires Interpreter? |
|-----------|------------------|------------------------|
| **Rust** | Ahead-of-time (binary executable) | ❌ No |
| **C/C++** | Ahead-of-time | ❌ No |
| **Python** | Interpreted | ✅ Yes |
| **JavaScript** | Interpreted | ✅ Yes |

> 🔧 As your projects grow, you’ll manage builds, dependencies, and configurations using **Cargo**, Rust’s package and build system — introduced in the next chapter.

---

## 🧹 Step 7: Optional — Format Your Code with `rustfmt`

Rust includes an automatic code formatter named **`rustfmt`** to keep your code style consistent.

Run:
```bash
rustfmt main.rs
```

This formats your file according to Rust’s official style guide.

---

## ✅ Summary

By completing this chapter, you’ve learned how to:

- Create a new Rust project directory  
- Write a basic Rust program (`main.rs`)  
- Compile and execute Rust code  
- Understand macros, functions, and syntax  
- Compare Rust’s compilation model with other languages  

You’re now ready to explore **Cargo** — Rust’s powerful build system and package manager.

---

**Author:** Parth  
📘 *Part of my Rust Programming Course Repository*  
🚀 *Next Chapter → Working with Cargo and Project Structure*

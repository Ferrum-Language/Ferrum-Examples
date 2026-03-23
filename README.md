# Ferrum Examples

Example programs written in the [Ferrum](https://github.com/Ferrum-Language/Ferrum) programming language.

Ferrum has C syntax with compile-time memory safety — no garbage collector, no runtime overhead.

## Programs

| File | What it shows |
|------|--------------|
| `hello.fe` | Hello World — the simplest Ferrum program |
| `counter.fe` | While loop and integer arithmetic |
| `factorial.fe` | Recursive function, for loop |
| `ownership.fe` | `new`, `move()`, automatic `free()` |
| `borrows.fe` | Immutable `&` and mutable `&mut` borrows |
| `unsafe_demo.fe` | Raw pointers inside `unsafe {}` blocks |

## How to run

### Build the compiler first

```bash
git clone https://github.com/Ferrum-Language/Ferrum.git
cd Ferrum
bash build.sh
```

### Compile and run any example

```bash
./build/ferrumc hello.fe -o hello
./hello
```

### See the generated LLVM IR

```bash
./build/ferrumc ownership.fe --emit-ir
```

## Requirements

- `g++` with C++20
- LLVM 18 (`llvm-config`, `llc`)
- `gcc` (for linking)

```bash
# Ubuntu / Debian
sudo apt install llvm-18 llvm-18-dev gcc g++ build-essential
```

---

*Ferrum Compiler v0.2 — [Ferrum-Language](https://github.com/Ferrum-Language)*

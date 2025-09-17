# Custom-Compiler
Custom Compiler for Python-like Language. It performs lexical & syntax analysis, builds quads (intermediate code) with backpatching, constructs a symbol table with nesting levels/offsets, and emits **RISC-V (RV32I)** assembly.

## Language (cpy) — The Basics: 
- Integers only (range −32767..32767), variables via `#int`.  
- Control: `if / elif / else`, `while`.  
- I/O: `print(expr)`, `id = int(input())`.  
- Functions with parameters (call-by-value), nested functions, `return expr`.  
- Blocks use `:{ #{ ... #} }`. Globals re-declared in functions with `global`.  
- Comments: `## ... ##`.
- 
## Project layout
- `final.py` — the compiler (scanner, parser, quads, symbol table, RISC-V)  
- `test.cpy` — example program
  
## Requirements
- Python 3.x

## How to Run
```bash
python3 final.py test.cpy


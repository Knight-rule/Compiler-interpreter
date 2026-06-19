<h1 align="center">⚙️ MiniLang Compiler</h1>

<p align="center">
  <em>Complete compiler pipeline — lexer, parser, AST, and interpreter for a custom programming language</em>
</p>

<p align="center">
  <a href="https://knight-rule.github.io/compiler-interpreter"><img src="https://img.shields.io/badge/demo-live-brightgreen" alt="Live Demo"></a>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black" alt="JavaScript">
</p>

---

## ✨ Features

- [x] **Lexer** — Tokenizes source code into meaningful tokens
- [x] **Recursive Descent Parser** — Builds AST from token stream
- [x] **AST Interpreter** — Direct tree-walking execution
- [x] **Variables** — Declaration, assignment, and scoping
- [x] **Loops** — For and while loop constructs
- [x] **Functions** — First-class functions with parameters and return values
- [x] **Closures** — Lexical scoping with closure support
- [x] **Arrays & Strings** — Built-in data structures
- [x] **6 Example Programs** — Ready-to-run sample code
- [x] **Zero Dependencies** — Pure vanilla JavaScript

## 📸 Screenshot

![screenshot](screenshot.png)

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| HTML5 | Interactive code editor interface |
| CSS3 | Syntax highlighting and responsive layout |
| JavaScript | Compiler pipeline implementation |

## 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/knight-rule/compiler-interpreter.git

# Navigate to the project
cd compiler-interpreter

# Open in browser
open index.html
```

No build step or dependencies required — just open the HTML file!

## 📖 Usage

1. **Write Code** — Type MiniLang code in the editor panel
2. **Select Example** — Or choose from 6 pre-built example programs
3. **Click Run** — Execute the code and see output in the console
4. **View AST** — Toggle the AST visualization panel
5. **Step Through** — Watch the interpreter execute each node

```minilang
// MiniLang syntax example
fn fibonacci(n) {
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}

print(fibonacci(10));  // Output: 55
```

## ⚙️ How It Works

```
Source Code
    │
    ▼
┌──────────┐
│  Lexer   │  Tokenizes: keywords, identifiers, literals, operators
└────┬─────┘
     ▼
┌──────────┐
│  Parser  │  Recursive descent: builds AST from token stream
└────┬─────┘
     ▼
┌──────────┐
│   AST    │  Abstract Syntax Tree representation
└────┬─────┘
     ▼
┌──────────────┐
│ Interpreter  │  Tree-walking execution with environment stack
└──────────────┘
```

The compiler follows the classic pipeline:
1. **Lexical Analysis** — Characters → Tokens (NUMBER, IDENT, FUNC, IF, etc.)
2. **Parsing** — Tokens → AST nodes (Program, FunctionDef, IfStatement, etc.)
3. **Interpretation** — Walk the AST and execute each node, maintaining scope chains

## 🎯 MiniLang Grammar

```
program     → statement*
statement   → varDecl | funcDef | ifStmt | whileStmt | returnStmt | exprStmt
funcDef     → "fn" IDENT "(" params? ")" block
varDecl     → "var" IDENT "=" expression
ifStmt      → "if" expression block ("else" block)?
whileStmt   → "while" expression block
expression  → literal | IDENT | binary | call | array
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Prashant** — [@knight-rule](https://github.com/knight-rule)

<p align="center">
  Made with ❤️ for compiler enthusiasts
</p>

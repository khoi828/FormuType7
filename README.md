# 🧮 MathWrite 7 (Offline Edition)

![Python Version](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyQt5](https://img.shields.io/badge/UI-PyQt5-green)
![SymPy](https://img.shields.io/badge/CAS_Solver-SymPy-orange)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

**MathWrite 7** is an open-source clone that perfectly replicates the WYSIWYG equation editing experience and classic UI of MathType 7, built with Python and PyQt5. 

Designed to operate **100% offline**, it features a native Abstract Syntax Tree (AST) geometric layout engine, an integrated Computer Algebra System (CAS), and seamlessly exports high-quality images (Hi-DPI), AMS-LaTeX, or MathML 3.0 directly to Microsoft Word.

> **Developed by: mkhoithcsnduthanhhoa**

---

## ✨ Key Features

* **Classic MathType 7 UI:** Accurately reproduces the 5-layer interface (Symbol Palettes, Template Palettes, Tabbed Preset Toolbar, Horizontal Ruler, and WYSIWYG Canvas).
* **AST & WYSIWYG Architecture:** Real-time visual rendering. Navigate intuitively through equation slots using arrow keys and the `Tab` key without writing raw code.
* **Chord Shortcuts System:** Fully supports legacy MathType 2-step shortcuts (`Ctrl+F` for fractions, `Ctrl+R` for radicals, `Ctrl+G` for Greek letters, `Ctrl+T` for structural templates).
* **Offline CAS Solver:** Powered by SymPy. Automatically solve equations, calculate derivatives and integrals, simplify expressions, and plot 2D graphs directly within the editor.
* **Multi-Format Export:**
  * Copy transparent background images (PNG) at 300 DPI print quality.
  * Export sharp SVG vectors.
  * Generate standard AMS-LaTeX code.
  * Generate W3C Presentation MathML 3.0 (Paste directly into MS Word Equations via `Ctrl+V`).
* **Favorites System:** Save frequently used formulas and systems of equations for 1-click insertion.

---

## 📸 Screenshots

![Main Interface](Screenshot%202026-10-28%20113858.png)
> *Intuitive WYSIWYG editor with classic Palettes, Tabbed Toolbar, and Ruler.*

![Word Integration](Screenshot%202026-10-28%20114053.png)
> *Seamless integration with Microsoft Word: Paste as Hi-DPI Image or native Equation (MathML).*

---

## 🚀 Installation & Usage

### For End-Users (No Installation Required)
You do not need to install Python or any dependencies to use this application.
1. Navigate to the **[Releases](../../releases)** page of this repository.
2. Download the latest **`MathWrite7.exe`** file.
3. Move the file to your Desktop or any preferred folder and **double-click to run**. The software is fully portable and works 100% offline.

### For Developers (Build from Source)

If you want to modify the source code or build the executable yourself, follow these steps:

**1. Clone the repository:**
```bash
git clone https://github.com/Your_Username/MathWrite7-Offline.git
cd MathWrite7-Offline
```

**2. Install required dependencies:**
Python 3.8+ is required.
```bash
pip install PyQt5 matplotlib sympy numpy Pillow PyQt5-sip PyQt5.QtSvg
```

**3. Run the application directly:**
```bash
python mathwrite7_english.py
```

**4. Build a standalone .exe (Using PyInstaller):**
First, generate the icon file:
```bash
python make_icon.py
```
Then, compile the source code into a single executable:
```bash
pyinstaller --noconsole --onefile --clean --icon="math_icon.ico" --add-data "math_icon.ico;." --collect-data matplotlib --hidden-import sympy --hidden-import numpy --hidden-import PyQt5.QtSvg --name "MathWrite7" mathwrite7_english.py
```
The final standalone `.exe` will be located in the `dist` folder.

---

## ⌨️ Basic Keyboard Shortcuts

| Action | Shortcut (Windows) | Description |
| :--- | :--- | :--- |
| **Fraction** | `Ctrl + F` | Inserts a full-size fraction |
| **Square Root** | `Ctrl + R` | Inserts a radical symbol |
| **Superscript** | `Ctrl + H` | Inserts a superscript (power) |
| **Subscript** | `Ctrl + L` | Inserts a subscript |
| **Sub & Superscript** | `Ctrl + J` | Inserts both simultaneously |
| **Integral** | `Ctrl + I` | Inserts a definite integral with limits |
| **System of 2 Equations**| `Ctrl + E` | Opens a 2-row matrix with a left brace |
| **Parentheses** | `Ctrl + 9` or `Ctrl + (` | Auto-scaling parentheses |
| **Greek Letters** | `Ctrl + G` then letter | E.g., `Ctrl+G` then `a` for α, `p` for π |
| **Templates**| `Ctrl + T` then letter | E.g., `Ctrl+T` then `s` for Summation ∑ |
| **Clear Canvas** | `Ctrl + N` | Clears all current equations |
| **Copy (Default)** | `Ctrl + C` | Copies according to Preferences format |
| **Copy as Image** | `Ctrl + Shift + C` | Copies as Hi-DPI PNG for Word/Zalo |
| **Delete / Backspace** | `Backspace` | Auto-removes empty template boxes |
| **Navigate Slots** | `Tab` or Arrows | Jumps to the next input slot |

---

## 🤝 Contributing
Contributions, issues, and feature requests are highly welcome to make this tool even better! Feel free to check the *Issues* page if you want to contribute.

## 📝 License
This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute it.

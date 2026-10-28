# Mathwrite7
offline mathematical typesetting toolkit
# 🧮 MathType 7 Ultimate (Offline Edition)

![Python Version](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyQt5](https://img.shields.io/badge/UI-PyQt5-green)
![SymPy](https://img.shields.io/badge/CAS_Solver-SymPy-orange)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

**MathWrite** is an open-source clone that perfectly replicates the WYSIWYG equation editing experience and classic UI of MathType 7, built with Python and PyQt5. 
Designed to operate **100% offline**, it features a native Abstract Syntax Tree (AST) geometric layout engine, an integrated Computer Algebra System (CAS), and seamlessly exports high-quality images (Hi-DPI), AMS-LaTeX, or MathML 3.0 directly to Microsoft Word.
![alt text](image-1.png)
---

## ✨ Key Features

* **Classic MathType 7 UI:** Accurately reproduces the 5-layer interface (Symbol Palettes, Template Palettes, Tabbed Preset Toolbar, Horizontal Ruler, and WYSIWYG Canvas).
* **AST & WYSIWYG Architecture:** Real-time visual rendering. Navigate intuitively through equation slots using arrow keys and the `Tab` key without writing raw code.
* **Chord Shortcuts System:** Fully supports legacy MathType 2-step shortcuts (`Ctrl+F` for fractions, `Ctrl+R` for radicals, `Ctrl+G` for Greek letters, `Ctrl+T` for structural templates).
* **Offline CAS Solver:** Powered by SymPy. Automatically solve equations, calculate derivatives and integrals, simplify expressions, and plot 2D graphs directly within the editor.
* **Multi-Format Export:**
  * Copy transparent background images (![alt text](image.png)) at 300 DPI print quality.
  * Export sharp SVG vectors.
  * Generate standard AMS-LaTeX code.
  * Generate W3C Presentation MathML 3.0 (Paste directly into MS Word Equations via `Ctrl+V`).
* **Favorites System:** Save frequently used formulas and systems of equations for 1-click insertion.

---

## Screenshots


![Main Interface](![alt text](image-2.png))
> *Intuitive WYSIWYG editor with classic Palettes and Tabbed Toolbar.*


---

## 🚀 Installation & Usage

### For End-Users (No Installation Required)
You do not need to install Python or any dependencies to use this application.
1. Navigate to the **[Releases]** page of this repository.
2. Download the latest **`MathWrite7.exe`** file.
3. Move the file to your Desktop or any preferred folder and **double-click to run**. The software is fully portable and works 100% offline.

### For Developers (Build from Source)

If you want to modify the source code or build the executable yourself, follow these steps:

**1. Clone the repository:**
```bash
git clone https://github.com/khoi828/MathWrite7-1.0.git
**2. Install required dependencies:**
Python 3.8+ is required.
```bash
pip install PyQt5 matplotlib sympy numpy Pillow PyQt5-sip PyQt5.QtSvg

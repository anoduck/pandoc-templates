# 📝 pandoc-templates

A versatile collection of Pandoc templates designed to streamline document generation for various needs.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-None-lightgrey)
![Stars](https://img.shields.io/github/stars/anoduck/pandoc-templates?style=social)
![Forks](https://img.shields.io/github/forks/anoduck/pandoc-templates?style=social)

![Template Preview](/preview_example.png)


## ✨ Features

*   **📚 Diverse Template Collection:** Access a growing library of Pandoc templates, including academic, easy-to-use, and custom styles, catering to a wide range of document types.
*   **🚀 Rapid Document Generation:** Quickly convert Markdown or other formats into professional-looking PDFs, HTML, or Word documents with minimal effort.
*   **🎨 Highly Customizable:** Many templates offer extensive customization options via Pandoc metadata, allowing you to tailor output to your specific branding and formatting requirements.
*   **🛠️ Modular & Extensible:** Designed to be easily integrated into your existing workflows and adaptable for further development or creation of new templates.
*   **🔄 Cross-Format Compatibility:** Leverage Pandoc's power to output consistent documents across various formats (LaTeX, HTML, DOCX) using a single source.

## References

* You can have a really cool README Generated for your repo at [GitHub README
  Generator](https://gitreadme-maker.vercel.app/)
* [Pandoc Manual](https://pandoc.org/MANUAL.html)
* [Panscribe Manuscript Template](https://github.com/dylan-k/panscribe)
* Sweet collection of Pandoc Templates here! -> [Pandoc Templates](https://pandoc-templates.org/)

## ⚙️ Installation Guide

This repository contains Pandoc templates. To use them, you typically need to clone the repository and either place the templates in Pandoc's data directory or reference them directly in your Pandoc commands.

### Prerequisites

*   **Pandoc:** Ensure you have Pandoc installed on your system. You can download it from [pandoc.org](https://pandoc.org/installing.html).
*   **LaTeX Distribution (for PDF output):** For generating PDF documents, you will need a LaTeX distribution like TeX Live or MiKTeX.

### Manual Installation

1.  **Clone the Repository:**
    Navigate to your desired directory and clone the `pandoc-templates` repository:

    ```bash
    git clone https://github.com/anoduck/pandoc-templates.git
    ```

2. **Initialize the git submodules:**
   Before you do anything else, you need to initialize the submodules.
   
   ```bash
   git submodule init
   ```

3.  **Locate Pandoc's Data Directory (Optional but Recommended):**
    To make templates globally accessible, you can place them in Pandoc's data directory. The location varies by OS:
    *   **Linux/macOS:** `~/.local/share/pandoc` or `~/.pandoc`
    *   **Windows:** `%APPDATA%\pandoc`

    You can find the exact path by running:

    ```bash
    pandoc --version
    ```

    Look for the "User data directory" entry.

4.  **Copy Templates:**
    Copy the desired template directories (e.g., `academic-pandoc-template`, `easy-pandoc-templates`) from the cloned repository into the `templates` subdirectory within Pandoc's data directory. If the `templates` subdirectory doesn't exist, create it.

    ```bash
    # Example for Linux/macOS
    cp -r pandoc-templates/academic-pandoc-template ~/.local/share/pandoc/templates/
    cp -r pandoc-templates/easy-pandoc-templates ~/.local/share/pandoc/templates/
    # And so on for other templates you wish to install globally
    ```

    Alternatively, you can just keep the templates in your project directory and reference them by their path.


## 🚀 Usage Examples

Once installed, you can use the templates with the `pandoc` command-line tool.

### Basic Usage with an Academic Template

To convert a Markdown file (`my-paper.md`) into a PDF using the `academic-pandoc-template`:

```bash
pandoc my-paper.md \
  --template=academic-pandoc-template/template.tex \
  -o my-paper.pdf
```

### Using an Easy Template for HTML Output

To convert a Markdown file (`my-notes.md`) into an HTML document using an `easy-pandoc-template`:

```bash
pandoc my-notes.md \
  --template=easy-pandoc-templates/default.html \
  -o my-notes.html
```

### Specifying Custom Variables

Many templates support custom variables for fine-grained control over the output. These are often specified in your Markdown's YAML front matter or via Pandoc's `-V` flag.

**Example `my-document.md` with YAML front matter:**

```markdown
---
title: "My Awesome Document"
author: "Anoduck"
date: "2023-10-27"
documentclass: article
fontsize: 12pt
---

# Introduction

This is the introduction to my document.
```

**Then, convert to PDF:**

```bash
pandoc my-document.md \
  --template=pandoc-latex-template/template.tex \
  -o my-document.pdf
```


## 🗺️ Project Roadmap

Our goal is to continually expand and refine this template collection. Here's what's planned:

*   **V1.1 (Upcoming):**
    *   **New Template Category:** Introduce a "Presentation" template category for generating slides (e.g., Beamer, reveal.js).
    *   **Improved Documentation:** Enhance individual template documentation with more examples and customization options.
    *   **Accessibility Features:** Explore adding accessibility-focused features to output documents where applicable.
*   **V1.2 (Future):**
    *   **Community Contributions Integration:** Streamline the process for users to submit their own templates or improvements.
    *   **Template Testing Suite:** Develop automated tests to ensure template robustness and consistent output.
    *   **Language-Specific Templates:** Investigate adding templates tailored for specific non-English languages.


## 🤝 Contribution Guidelines

We welcome contributions to expand and improve this template collection! Please follow these guidelines:

*   **Fork the Repository:** Start by forking the `pandoc-templates` repository to your GitHub account.
*   **Branch Naming:** Create a new branch for your feature or bug fix. Use descriptive names like `feat/new-academic-template` or `fix/latex-compilation-issue`.
*   **Code Style:**
    *   For LaTeX templates (`.tex`), adhere to a consistent indentation (e.g., 2 spaces) and comment your custom additions clearly.
    *   For Lua filters (`.lua`), follow standard Lua style guides.
    *   For Markdown template components, ensure clean and readable Markdown.
*   **Pull Request Process:**
    *   Submit a Pull Request (PR) to the `main` branch of this repository.
    *   Provide a clear and concise description of your changes in the PR.
    *   Reference any related issues.
    *   Ensure your changes are well-tested and do not introduce regressions. Include sample input/output if applicable.
*   **Testing:** If you're adding a new template or significantly modifying an existing one, please include a sample Markdown file that demonstrates its usage and expected output.


## ⚖️ License Information

This repository currently has **No Explicit License** specified. This means that, by default, all rights are reserved by the copyright holder (`anoduck`).

If you wish to use, distribute, or modify the contents of this repository, please contact the main contributor, anoduck, for explicit permission.

---

*Generated by a professional README.md generator.*

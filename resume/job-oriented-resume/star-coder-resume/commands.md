# **Installation Commands for LaTeX Tools and Poppler Utilities**

#### **Debian / Ubuntu and Derivatives**
```bash
sudo apt install texlive-latex-recommended texlive-fonts-recommended texlive-latex-extra poppler-utils
```

> **Note:** The `aptitude` package manager is not preinstalled on most systems. If you intend to use it, you must first install it with `sudo apt install aptitude`. Otherwise, the default `apt` command is more widely used.

---

#### **Fedora / Red Hat / CentOS / RHEL**
```bash
sudo dnf install texlive-scheme-full poppler-utils
```

> **Note:** `texlive-scheme-full` installs the complete TeX Live suite. If you want a lighter setup, use `texlive-scheme-basic` or specific packages like `texlive-latex`.

---

### **Operations**

1. **Compile the `.tex` file into a `.pdf`**:
   ```bash
   pdflatex jaman-uddin.tex
   ```
   This generates `jaman-uddin.pdf` in the current directory.

2. **Convert the `.pdf` into a `.png`**:
   ```bash
   pdftoppm jaman-uddin.pdf jaman-uddin -png -r 300
   ```
   This generates `jaman-uddin-1.png` at 300 DPI.

3. **Rename the PNG file**:
   ```bash
   mv jaman-uddin-1.png jaman-uddin.png
   ```

---

### Additional Notes
- **Error Handling:** If `pdflatex` fails, check the `.log` file (e.g., `jaman-uddin.log`) for debugging information.
- **Dependencies:** Ensure that the system's repositories are up-to-date:
  ```bash
  sudo apt update && sudo apt upgrade      # For Debian/Ubuntu
  sudo dnf upgrade --refresh               # For Fedora
  ```
---

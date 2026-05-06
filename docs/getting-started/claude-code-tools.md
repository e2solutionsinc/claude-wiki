# Claude Code Useful Tools

These tools extend what Claude Code can read and work with. Install any you need via Homebrew or pip.

---

### gh — GitHub CLI
**Requires Homebrew:** `brew install gh`

Lets Claude Code interact with GitHub — view repos, check pull requests, inspect Actions runs, and read file contents directly from branches without cloning.

```bash
brew install gh
gh auth login
```

---

### mdbtools
**Requires Homebrew:** `brew install mdbtools`

Lets Claude Code read Microsoft Access database files (`.mdb`, `.accdb`). Also required to read **web config files with a `.wdb` extension** used by the Infios/Advantage platform.

```bash
brew install mdbtools
```

---

### openpyxl — Excel (.xlsx) reader
**Install via pip:** `pip3 install openpyxl`

Lets Claude Code read and extract data from modern Excel files (`.xlsx`).

```bash
pip3 install openpyxl
```

---

### xlrd — Legacy Excel (.xls) reader
**Install via pip:** `pip3 install xlrd`

Lets Claude Code read older Excel files (`.xls`).

```bash
pip3 install xlrd
```

---

### Playwright — Browser automation
**Install via pip:** `pip3 install playwright && python3 -m playwright install`

Lets Claude Code control a real browser — open pages, click, fill forms, take screenshots, and read JavaScript-rendered content.

```bash
pip3 install playwright
python3 -m playwright install
```

!!! note "Limited use in our current workflows"
    Playwright controls a browser on the **local Mac only**. It cannot access web browsers running inside a VM or RDP session. If the app inside the VM is accessible via a URL or IP from your Mac, Playwright can reach it that way — but otherwise it is of limited use in our current workflows.

---

### pdfplumber — PDF reader
**Install via pip:** `pip3 install pdfplumber`

Lets Claude Code read and extract text and tables from PDF files — useful for documentation, reports, and specs.

```bash
pip3 install pdfplumber
```

---

### python-docx — Word document reader
**Install via pip:** `pip3 install python-docx`

Lets Claude Code read and extract content from Word `.docx` files.

```bash
pip3 install python-docx
```

---

### jq — JSON parser
**Requires Homebrew:** `brew install jq`

Parses and queries JSON from the command line. Useful when working with config files, API responses, or any structured JSON data.

```bash
brew install jq
```

---

### tree — Directory structure viewer
**Requires Homebrew:** `brew install tree`

Displays folder structures visually in the terminal. Useful when mapping out or documenting project directories.

```bash
brew install tree
```

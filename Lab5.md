# Samyaak Gharat - Lab Extra (Starter Kit & Automation, No Images)

## Script: starter_kit.sh

### Code
```bash
#!/bin/bash
# Starter kit script for setting up a project structure

# Create the main project directories
mkdir -p project/{scripts,docs,data}

# Add README files in each folder
echo "# Project Root" > project/README.md
echo "# Scripts Folder" > project/scripts/README.md
echo "# Documentation Folder" > project/docs/README.md
echo "# Data Folder" > project/data/README.md
```

---

### Explanation
1. `#!/bin/bash` → Shebang line, tells the system to run the script using bash.
2. Comments (`# ...`) → Not executed, only used for explaining the code.
3. `mkdir -p project/{scripts,docs,data}` →
   - `mkdir` means *make directory*.
   - `-p` ensures parent directories are created if they don’t exist (avoids errors).
   - `{scripts,docs,data}` uses *brace expansion* to create three subfolders under `project/`:
     - `project/scripts/`
     - `project/docs/`
     - `project/data/`
4. `echo "text" > file` → Prints text and redirects it into a file. If the file doesn’t exist, it is created; if it exists, the contents are replaced.
   - Example: `echo "# Project Root" > project/README.md` → Creates a `README.md` file in the `project/` folder with the heading *Project Root*.

---

## Output Example
After running the script:
```
project/
├── README.md
├── scripts/
│   └── README.md
├── docs/
│   └── README.md
└── data/
    └── README.md
```

---

## Why is automation useful in DevOps?
1. **Consistency and reliability** — Ensures the same structure every time.
2. **Speed and efficiency** — Saves time by avoiding manual setup.
3. **Scalability** — Easy to reproduce the environment for multiple projects.
4. **Reduced human error** — Removes the risk of mistakes during setup.

---

## Question — What does `mkdir -p` do?
- `mkdir` = *make directory*.
- `-p` = Creates parent directories if they don’t already exist, preventing errors.

---



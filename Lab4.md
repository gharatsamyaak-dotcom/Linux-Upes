# Samyaak Gharat - Lab 4 (No Images, Revised)

## 1.⁠ ⁠backup.sh Script

Create a new file named backup.sh inside your project folder:

![images](Lab4.png)


## 1. Make Script Executable
Run the command below one time to allow execution:
```bash
chmod +x backup.sh
```

## 2. Testing the Script
1. Create a few sample `.txt` files in your directory.
2. Execute the script:
   ```bash
   ./backup.sh
   ```
3. Verify the backup folder contents:
   ```bash
   ls backup/
   ```

---

# Lab 4 – File & Backup Automation

## Objective
Set up an automated backup system that copies all `.txt` files into a `backup/` folder, adding timestamps to the filenames.

---

## Script Explanation

1. `mkdir -p backup` → Ensures a `backup/` directory exists (creates if missing).
2. `timestamp=$(date +"%Y%m%d_%H%M%S")` → Produces a timestamp string like `20250910_143012`.
3. `for file in *.txt; do ... done` → Iterates through each `.txt` file in the current folder.
4. `basename "$file" .txt` → Retrieves the filename without the `.txt` extension.
5. `cp "$file" "backup/${filename}_$timestamp.txt"` → Copies each file to the backup directory, appending the timestamp.

---

## Example Run

### Input Files
```
file1.txt
file2.txt
```

### Command
```bash
./backup.sh
```

### Output Files (in backup/)
```
backup/file1_20250910_120501.txt
backup/file2_20250910_120501.txt
```

---

### Question 1 — What’s the difference between `cp`, `mv`, and `rsync`?

- **cp (Copy)**
  - Creates a duplicate of a file or directory.
  - Leaves the original unchanged.
  - Example: `cp notes.txt notes_copy.txt`
  - Options: `-r` (recursive), `-i` (prompt before overwrite), `-u` (only copy if newer).
  - ✅ Good for quick duplication, ❌ doesn’t retain all metadata unless `-p`.

- **mv (Move/Rename)**
  - Moves or renames a file/directory.
  - Original is removed from source and placed at target location.
  - Example: `mv old.txt new.txt`
  - ✅ Very efficient, ❌ when moving across filesystems, it behaves like copy + delete.

- **rsync (Remote Sync)**
  - Syncs files/directories locally or to remote systems.
  - Example: `rsync -avh project/ backup/`
  - Features: incremental copying, SSH support, metadata preservation.
  - ✅ Perfect for backups, ❌ more complex compared to cp or mv.

---

### Question 2 — How to schedule scripts automatically?

- **Using at (One-time)**
  Run once at a specific time:
  ```bash
  echo "/home/user/backup.sh" | at 11:30
  ```

- **Using cron (Recurring)**
  Schedule regular runs:
  ```bash
  crontab -e
  ```
  Example: Run daily at midnight:
  ```bash
  0 0 * * * /home/user/backup.sh
  ```

---



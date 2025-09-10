# Dual Booting Linux with Windows

Dual booting allows you to install **Linux** alongside **Windows** on the same computer, giving you the choice to boot into either operating system at startup.

---

## ⚠️ Disclaimer
- Back up all important files before proceeding.
- This process involves modifying disk partitions, which can result in data loss if done incorrectly.
- Ensure your computer is plugged into power during the installation.

---

## 🛠 Requirements
- A computer with **Windows already installed**.
- A USB drive (8 GB or larger).
- Linux distribution ISO (e.g., Ubuntu, Fedora, Linux Mint).
- Tool to create bootable USB (e.g., [Rufus](https://rufus.ie), [balenaEtcher](https://etcher.io)).
- Free space on your hard drive (20 GB+ recommended).

---

## 🔹 Step 1: Prepare Windows
1. **Update Windows** to avoid compatibility issues.
2. **Disable Fast Startup**:
   - Control Panel → Power Options → Choose what the power buttons do → Turn off *fast startup*.
3. **Shrink Windows Partition**:
   - Press `Win + X` → Disk Management.
   - Right-click on the Windows partition → *Shrink Volume*.
   - Leave unallocated space for Linux (20–100 GB).

---

## 🔹 Step 2: Create Linux Bootable USB
1. Download your chosen Linux distribution ISO.
2. Open **Rufus** (or another tool).
3. Select your USB drive and the ISO file.
4. Click *Start* to create the bootable USB.

---

## 🔹 Step 3: Boot from USB
1. Restart your computer and enter **BIOS/UEFI** (usually `F2`, `F12`, `Del`, or `Esc`).
2. Change the boot order to prioritize **USB drive**.
3. Save and exit → your computer will boot into the Linux installer.

---

## 🔹 Step 4: Install Linux
1. Choose **"Install Linux"**.
2. Select **"Install alongside Windows Boot Manager"** (recommended).
   - If not available, choose *Something Else* and manually partition the unallocated space:
     - Root (`/`) → ext4, at least 20 GB.
     - Swap (optional) → 2–4 GB.
     - Home (`/home`) → rest of free space.
3. Install the Linux bootloader (GRUB) on the default drive (usually `/dev/sda`).

---

## 🔹 Step 5: Post-Installation
1. Remove USB and reboot.
2. You will see the follwing image-


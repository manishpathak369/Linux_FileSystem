# Linux_FileSystem
# 🐧 Understanding the Linux Filesystem

Unlike Windows, where you have drives like `C:`, `D:`, and `E:`, Linux uses a single hierarchical directory structure that starts from `/`, known as the **root directory**.

Everything in Linux, including applications, configuration files, devices, and personal data, exists somewhere under this directory.

## 📁 1. Linux Directory Structure

Here's a quick overview of the important directories:

| Directory | Purpose |
|---|---|
| `/` | Root directory; starting point of the filesystem |
| `/home` | Personal files and directories of normal users |
| `/root` | Home directory of the root user |
| `/etc` | System-wide configuration files |
| `/bin` | Essential user commands |
| `/sbin` | System administration commands |
| `/usr` | Applications, libraries, and shared resources |
| `/var` | Logs, caches, and variable application data |
| `/tmp` | Temporary files |
| `/boot` | Kernel, initramfs, and bootloader-related files |
| `/dev` | Device files |
| `/proc` | Virtual filesystem containing process and kernel information |
| `/sys` | Kernel and hardware information |
| `/mnt` | Temporary mount point for filesystems |
| `/media` | Common mount location for removable devices |
| `/opt` | Optional or third-party software |
| `/run` | Runtime data since system startup |

## 🏠 2. Your Home Directory

Your personal files are generally stored inside `/home/username`.

For example:

```text
/home/manish/
├── Desktop/
├── Documents/
├── Downloads/
├── Pictures/
├── Videos/
├── .config/
├── .local/
└── .cache/
```

Some useful shortcuts:

| Symbol | Meaning |
|---|---|
| `~` | Current user's home directory |
| `.` | Current directory |
| `..` | Parent directory |
| `/` | Root directory |

Example:

```bash
cd ~       # Go to home directory
cd ..      # Go one directory back
pwd        # Show current location
```

## 👻 3. Hidden Files

In Linux, files and directories beginning with a dot (`.`) are hidden by default.

For example:

- `.bashrc`
- `.config`
- `.local`
- `.cache`

To display hidden files:

```bash
ls -a
```

To display detailed information:

```bash
ls -lah
```

## 💿 4. Filesystem and Partitions

A partition is a section of a storage device, while a filesystem is how data is organized within it.

Linux supports several filesystem types:

| Filesystem | Description |
|---|---|
| ext4 | Popular Linux filesystem |
| Btrfs | Supports snapshots and subvolumes |
| XFS | High-performance journaling filesystem |
| ZFS | Advanced filesystem and volume manager |
| FAT32 | Widely compatible filesystem |
| exFAT | Commonly used for removable storage |
| NTFS | Common Windows filesystem |

Useful commands:

```bash
lsblk -f     # Show disks, partitions and filesystems
df -h        # Show available disk space
findmnt      # Show mounted filesystems
```

## 📦 5. Where Are Applications Stored?

Applications aren't necessarily stored in one directory. Their executables, libraries, configuration files, and resources can be distributed across different locations.

For example:

```text
/usr/bin/       → Executables
/usr/lib/       → Libraries
/usr/share/     → Shared resources
/etc/           → System configurations
~/.config/      → User configurations
~/.cache/       → User cache
```

On Arch Linux, you can see which files belong to an installed package:

```bash
pacman -Ql firefox
```

## ⌨️ 6. Useful Filesystem Commands

| Command | Purpose |
|---|---|
| `pwd` | Show current directory |
| `ls -la` | List all files |
| `cd` | Change directory |
| `mkdir` | Create directory |
| `touch` | Create empty file |
| `cp` | Copy files |
| `mv` | Move or rename files |
| `rm` | Remove files |
| `find` | Search for files |
| `du -sh` | Show directory size |
| `df -h` | Show disk usage |
| `file` | Identify file type |

---

**A small reminder:** `/`, `/root`, and `/home` are three different things. Don't confuse them as same! Bcz,I thought so at first.😅

You don't need to memorize the entire filesystem. Just understand what the important directories contain, and navigating Linux will become much easier.

Happy exploring! 🐧

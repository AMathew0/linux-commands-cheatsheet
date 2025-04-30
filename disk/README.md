# 💽 Linux Disk & Partition Management

This section covers basic to intermediate disk management commands for checking disk usage, mounting drives, and managing partitions.

---

🧾 Check Disk Usage

```bash
df -h                        # View mounted disks & space (human-readable)
du -sh /home/user/           # Get folder size
du -sh *                     # Size of each item in the current directory

📌 Disk & Partition Listing

lsblk                        # List all block devices
fdisk -l                     # View partition layout
blkid                        # Show UUIDs of disks

🧰 Mount & Unmount Drives

mount /dev/sdb1 /mnt         # Mount device to folder
umount /mnt                  # Unmount device
mount -a                     # Mount all in /etc/fstab

📁 Automount with /etc/fstab
Edit file:
nano /etc/fstab

Example entry:
ini
UUID=xxxx-xxxx /mnt/data ext4 defaults 0 2
Get UUID using blkid

🧱 Create/Format Partition
⚠️ Use with caution — may erase data!

fdisk /dev/sdb               # Open partitioning tool (MBR)
gdisk /dev/sdb               # For GPT
mkfs.ext4 /dev/sdb1          # Format as ext4
mkfs.vfat /dev/sdb1          # Format as FAT32

🛠️ Resize & Repair

resize2fs /dev/sda1          # Resize ext4 filesystem
fsck /dev/sda1               # Check and repair file system

🔍 Disk I/O & Performance

iostat                       # Install: sysstat package
iotop                        # Real-time disk usage per process

💡 Always backup data before resizing, formatting, or partitioning disks.

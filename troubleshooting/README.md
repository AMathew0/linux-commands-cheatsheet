# 🛠️ Linux Troubleshooting Commands

Use these commands to diagnose and resolve system issues related to services, logs, hardware, permissions, and system behavior.

---

```bash

🔎 Check System Logs

journalctl                   # View system logs (systemd)
journalctl -xe              # Show recent critical events
dmesg                        # Kernel & hardware logs
tail -f /var/log/syslog      # Follow live logs
less /var/log/auth.log       # Review authentication logs

💻 Service Troubleshooting

systemctl status ssh         # Check status of SSH service
systemctl restart nginx      # Restart a service
systemctl enable apache2     # Enable on boot

🌐 Network Issues

ping 8.8.8.8                 # Check basic connectivity
curl -I https://google.com   # Check HTTP response
ss -tuln                     # Show listening ports
ip link                      # Verify network interfaces

🧱 Disk & Filesystem Issues

df -h                        # Show disk usage
du -sh folder/               # Check folder size
lsblk                        # List attached disks
mount                        # Show mounted drives
fsck /dev/sda1               # Check disk for errors (use with caution)

🔐 Permission & Ownership Issues

ls -l file.txt               # View file permissions
chmod 755 script.sh          # Change file permission
chown user:group file.txt    # Change file ownership

🚫 Process or System Hang

top                          # Monitor CPU/memory
htop                         # Enhanced view (install needed)
kill -9 <PID>                # Force kill unresponsive process
reboot                       # Reboot system (if necessary)

🧩 Application Debugging

strace -p <PID>              # Trace system calls of a process
lsof -i :8080                # Check which app is using port 8080

🧪 System Performance Check

uptime                       # Load averages
vmstat 1                     # Memory and CPU performance
iostat                       # Disk I/O stats (from sysstat package)
💡 Always test recovery steps in a lab before production. Use man <command> for help.

# 🛠️ Linux Services & Daemons Management

This section covers commands to start, stop, enable, and troubleshoot services and background processes in Linux — essential for daily system maintenance.

---

```bash

⚙️ Manage Services (systemd-based)

systemctl status nginx           # Check service status
systemctl start nginx            # Start service
systemctl stop nginx             # Stop service
systemctl restart nginx          # Restart service
systemctl reload nginx           # Reload config without restart
systemctl enable nginx           # Enable service on boot
systemctl disable nginx          # Disable autostart

📌 Check All Services

systemctl list-units --type=service     # List active services
systemctl --failed                      # Show failed services

🧪 Service Logs

journalctl -u nginx                    # Logs for a specific service
journalctl -u ssh -b                  # Show SSH logs since last boot

💡 Legacy Init Systems (SysVinit)
Some older systems use service and chkconfig:

service apache2 status                 # Check status
service apache2 start                  # Start service
chkconfig apache2 on                   # Enable on boot

🔄 Reload Daemon or Configs

systemctl daemon-reexec               # Re-exec systemd
systemctl daemon-reload               # Reload unit files after changes

⛑ Troubleshooting Tips

ps aux | grep nginx                   # Is the service running?
netstat -tulnp | grep 80             # Is the port open?
ss -ltnp                             # Show listening services
lsof -i :443                         # Check what's using a port

🧠 Best Practice: Always check logs with journalctl and validate service files in /etc/systemd/system/ for persistent changes.

# ⚙️ Linux Process Management Commands

This section covers basic to advanced process control — useful for monitoring system resource usage, killing unresponsive processes, and managing background tasks.

---

## 📊 View Running Processes

```bash
ps                          # Show current shell’s processes
ps aux                      # List all running processes with details
ps -ef                      # Another common format
top                         # Real-time system monitor (press `q` to quit)
htop                        # Enhanced top (install required)

🔍 Search for Specific Processes

ps aux | grep nginx         # Find processes related to nginx
pgrep sshd                  # Get process ID(s) of a service

❌ Kill or Manage Processes

kill <PID>                  # Terminate process by ID
kill -9 <PID>               # Force kill (SIGKILL)
pkill firefox               # Kill all instances by name
killall chrome              # Kill all processes with this name

🔁 Background & Foreground Tasks

command &                  # Run in background
jobs                       # Show background jobs
fg %1                      # Bring job #1 to foreground
bg %1                      # Resume job #1 in background

⏱️ Scheduling & Delay

sleep 10                   # Pause for 10 seconds
watch -n 5 uptime          # Run `uptime` every 5 seconds

🧪 Resource Usage

uptime                     # System uptime and load
free -h                    # Memory usage
df -h                      # Disk space usage
du -sh folder/             # Folder size

💡 Tip: Use htop for easier process management 

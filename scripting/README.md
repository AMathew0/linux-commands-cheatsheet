# 📜 Basic Shell Scripting in Linux

This section introduces essential concepts and examples to help you create and understand basic shell scripts for automation and administration.

---

```bash

✨ Script Structure

#!/bin/bash
# This is a sample script

echo "Hello, World!"
Save it as hello.sh, then run:

chmod +x hello.sh   # Make script executable
./hello.sh          # Execute script

📥 Variables

name="John"
echo "Hello, $name"

📦 Input & Output

read -p "Enter your name: " username
echo "Welcome, $username!"

🔁 Loops
For Loop

for i in 1 2 3; do
  echo "Loop $i"
done

While Loop
count=1
while [ $count -le 3 ]; do
  echo "Count: $count"
  ((count++))
done

⚖️ Conditionals

if [ $1 -gt 10 ]; then
  echo "Greater than 10"
else
  echo "10 or less"
fi

📂 File Checking

if [ -f file.txt ]; then
  echo "File exists"
else
  echo "File not found"
fi

⚙️ Functions

greet() {
  echo "Hello, $1!"
}
greet "Alice"

📌 Script Arguments

echo "Script name: $0"
echo "First argument: $1"
echo "Total arguments: $#"

🔄 Cron Job Example
Edit crontab:
crontab -e

Run script every day at 7 AM:
0 7 * * * /path/to/script.sh

💡 Use shell scripting for backups, cleanup, automation, and daily sysadmin tasks.

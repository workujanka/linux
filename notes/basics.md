# Linux Basics for Beginners

1. What Linux Is
Linux is an open‑source operating system used in servers, cloud platforms, cybersecurity, DevOps, and embedded systems.
It’s built around the command line, which gives you precise control over the system.

Popular distributions: Ubuntu, Debian, Fedora, CentOS, Kali, Arch.
If you’re practicing on your laptop, Ubuntu or Linux Mint is the easiest starting point.

2. The Linux Filesystem
Linux organizes everything into a single tree starting at / (root).

  Directory     Purpose
  ----------    ----------------------------------------
  /home         Personal files for each user
  /etc          System configuration files
  /var          Logs, caches, variable data
  /usr          Applications and libraries
  /bin          Essential user commands
  /sbin         System administration commands
  /root         Home directory for the root user

You’ll use /home/<username> most of the time.

3. Basic Navigation Commands

  Action               Command                Meaning
  -------------------  ---------------------  -----------------------------
  Show current dir     pwd                    Where am I
  List files           ls                     Show files and folders
  List with details    ls -l                  Permissions, size, owner
  List hidden files    ls -a                  Shows files starting with .
  Change directory     cd foldername          Move into a folder
  Go back one level    cd ..                  Up one directory
  Go to home           cd                     Shortcut

4. Working With Files and Folders

  Action               Command
  -------------------  -----------------------------
  Create a folder      mkdir myfolder
  Create a file        touch file.txt
  Copy a file          cp file.txt backup.txt
  Move/rename          mv old.txt new.txt
  Delete a file        rm file.txt
  Delete a folder      rm -r foldername

Warning: Be careful with rm -r — it deletes permanently.

5. Permissions

Every file has:
- Owner
- Group
- Permissions: read (r), write (w), execute (x)

Example from ls -l:
  -rwxr-xr-- 1 user group 4096 Jan 26 script.sh

Breakdown:
  rwx → owner can read/write/execute
  r-x → group can read/execute
  r-- → others can only read

Change permissions:
  chmod 755 script.sh

Change owner:
  sudo chown user:group file

6. Installing Software

On Ubuntu/Debian:
  sudo apt update
  sudo apt install package-name

On Fedora:
  sudo dnf install package-name

7. Viewing and Editing Files

View content:
  cat file.txt
  less file.txt
  head file.txt
  tail file.txt

Edit content:
  nano file.txt      # beginner-friendly
  vim file.txt       # powerful but steep learning curve

8. Processes and System Monitoring

  Action               Command
  -------------------  -----------------------------
  Show processes       ps aux
  Kill a process       kill <PID>
  Live monitor         top or htop

9. Using sudo

sudo = “run as administrator”

Example:
  sudo apt update

You’ll be asked for your password.
Use it only when necessary.

10. Networking Basics

  Action               Command
  -------------------  -----------------------------
  Show IP address      ip a
  Test connection      ping google.com
  Show open ports      ss -tulnp




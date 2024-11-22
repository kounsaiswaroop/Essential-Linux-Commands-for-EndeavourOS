# Essential-Linux-Commands-for-EndeavourOS
A comprehensive guide to mastering the Konsole terminal in EndeavourOS Linux. This repository includes categorized commands with explanations, examples, and tips for managing your system, files, packages, networks, and more. Perfect for beginners and advanced users looking to optimize their Linux experience.

1. System Information
uname -r

Description: Displays the currently running Linux kernel version.
Example:
bash
Copy code
uname -r
Output:
6.5.3-arch1-1
neofetch

Description: Displays system information like OS, kernel, shell, memory, and more in a stylized format. You need to install neofetch first:
bash
Copy code
sudo pacman -S neofetch
neofetch
lsb_release -a

Description: Prints details about the distribution version.
Example:
bash
Copy code
lsb_release -a
Output:
yaml
Copy code
Distributor ID: EndeavourOS
Description:    EndeavourOS Linux
Release:        Rolling
Codename:       n/a
hostnamectl

Description: Used to query or change the system hostname.
Example:
bash
Copy code
hostnamectl set-hostname my-new-hostname
hostnamectl
Output: Shows the new hostname.
2. File Management
ls

Description: List files and directories.
Examples:
ls → Lists files in the current directory.
ls -l → Provides a detailed list with permissions, owner, size, and date.
ls -a → Lists all files, including hidden ones (those starting with .).
cd

Description: Change directories.
Examples:
cd /home/user/Documents → Moves to the Documents directory.
cd .. → Moves one level up.
cd ~ → Moves to the home directory.
cp

Description: Copy files or directories.
Examples:
cp file1.txt /backup/ → Copies file1.txt to /backup/.
cp -r /source_folder /destination → Copies a directory recursively.
rm

Description: Remove files or directories.
Examples:
rm file.txt → Deletes file.txt.
rm -r directory → Deletes a directory and its contents.
3. Package Management (Pacman)
sudo pacman -Syu

Description: Updates the system by syncing package databases and upgrading all packages.
Tip: Run this regularly to ensure your system stays up-to-date.
Example:
bash
Copy code
sudo pacman -Syu
sudo pacman -S [package_name]

Description: Installs a package from the official repositories.
Example:
bash
Copy code
sudo pacman -S firefox
sudo pacman -R [package_name]

Description: Removes an installed package.
Example:
bash
Copy code
sudo pacman -R libreoffice
sudo pacman -Ss [keyword]

Description: Searches for a package in the repositories.
Example:
bash
Copy code
sudo pacman -Ss vlc
4. AUR Management (yay)
yay -S [package_name]

Description: Installs packages from the Arch User Repository (AUR).
Example:
bash
Copy code
yay -S google-chrome
yay -Ss [keyword]

Description: Searches the AUR for packages.
Example:
bash
Copy code
yay -Ss spotify
yay -R [package_name]

Description: Removes AUR packages.
Example:
bash
Copy code
yay -R spotify
5. User and Permissions
chmod

Description: Changes file or directory permissions.
Syntax:
bash
Copy code
chmod [permissions] [file]
Example:
chmod 755 script.sh → Makes the script executable.
chown

Description: Changes file ownership.
Syntax:
bash
Copy code
chown [user]:[group] [file]
Example:
chown user1:user1 file.txt
passwd

Description: Change the password for the current or specified user.
Example:
bash
Copy code
passwd
6. System Monitoring
top / htop

Description: Displays running processes and resource usage.
Tip: Install htop for a more user-friendly interface:
bash
Copy code
sudo pacman -S htop
htop
free -h

Description: Shows memory usage in human-readable format.
Example:
bash
Copy code
free -h
df -h

Description: Displays disk space usage in human-readable format.
Example:
bash
Copy code
df -h
7. Network Commands
ping

Description: Checks connectivity to a host.
Example:
bash
Copy code
ping google.com
ip addr

Description: Displays network interface details.
Example:
bash
Copy code
ip addr
curl

Description: Transfers data from or to a server.
Example:
bash
Copy code
curl https://example.com
8. Customization
nano ~/.bashrc

Description: Edit the Bash configuration file to add aliases or customize the environment.
Example:
bash
Copy code
nano ~/.bashrc
alias

Description: Create shortcuts for commands.
Example:
bash
Copy code
alias ll='ls -la'
source ~/.bashrc

Description: Reloads the Bash configuration file.
Example:
bash
Copy code
source ~/.bashrc

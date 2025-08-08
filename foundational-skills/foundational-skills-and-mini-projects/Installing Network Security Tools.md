# Installing Network Security Tools on Linux

As part of building my foundational skills, I practiced using the Linux command line to install and manage network security tools using the APT package manager.

### Tools Installed:
- **Suricata**: A network threat detection engine.
- **tcpdump**: A command-line packet analyzer.

### What I Did:
Using a Debian-based Linux environment, I worked in the Bash shell to:
- Confirm that the APT package manager was installed (`apt`)
  - This returned usage and version info, confirming it was available.
- Install Suricata using: `sudo apt install suricata`
  - Suricata installed successfully and output its version when I typed `suricata`.
- Uninstall Suricata with: `sudo apt remove suricata`
  - When trying to run `suricata` again, I received: `-bash: /usr/bin/suricata: No such file or directory`
- Install tcpdump with: `sudo apt install tcpdump`
- Use `apt list --installed` to confirm both tools were installed and visible in the package list.
- Reinstalled Suricata and verified that both tools were working.

### Summary:

This mini project gave me hands-on experience using the APT package manager to install, verify, and remove essential network security tools like `Suricata` and `tcpdump` in a Debian-based Linux environment. I practiced using commands like `apt install`, `apt remove`, and `apt list --installed` to manage applications from the terminal.  

Being comfortable with these kinds of tasks is part of working in Linux-based systems, and this gave me the chance to build that familiarity through direct use.

# Awesome Termux [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)


# Introduction
 - Termux is an Android terminal emulator and Linux environment app that works directly with no rooting or setup required. A minimal base system is installed automatically - additional packages are available using the APT package manager.

* [Termux wiki](https://wiki.termux.com/wiki/Main_Page) 
* [Github](https://github.com/termux/)
* [Gitter](https://gitter.im/termux/termux)
* [Facebook Page](https://facebook.com/termux/)
* [Facebook Group](https://facebook.com/groups/termux/)
* [Twitter](https://twitter.com/termux)
* IRC Channel #Termux on freenode

### [How termux is different from Linux](https://wiki.termux.com/wiki/Differences_from_Linux)

### Termux:Addons
Termux has some extra features. You can add them by installing addons:

[Termux:API](https://play.google.com/store/apps/details?id=com.termux.api)
    Access Android and Chrome hardware features.

[Termux:Boot](https://play.google.com/store/apps/details?id=com.termux.boot)
    Run scripts when your device boots.

[Termux:Float](https://play.google.com/store/apps/details?id=com.termux.window)
    Run Termux in a floating window.

[Termux:Styling](https://play.google.com/store/apps/details?id=com.termux.styling)
    Have color schemes and powerline-ready fonts customize the appearance of the Termux terminal.

[Termux:Task](https://play.google.com/store/apps/details?id=com.termux.tasker)
    An easy way to call Termux executables from Tasker and compatible apps.

[Termux:Widget](https://play.google.com/store/apps/details?id=com.termux.widget)
    Start small scriptlets from the home screen.

### Shells in Termux 
- Zsh
- Bash
- Xonsh
- IPython
- Fish 
- TCSH
- [Read Wiki to learn more](https://wiki.termux.com/wiki/Shells)

### Customizing Termux
- Enable Dark UI Mode in Termux
Add this line to your ~/.termux/termux.properties
```
use-black-ui=true
```
- Disable Vibration/haptic feedback
Add this line to your ~/.termux/termux.properties
```
bell-character=ignore
```
- [Oh-my-termux](https://github.com/4679/oh-my-termux)
### Text Editors in Termux
- Emacs : Extensible, customizable text editor-and more 
- joe : Wordstar like text editor 
- jupp : user friendly full screen text editor 
- Micro : Micro is a terminal-based text editor that aims to be easy to use and intuitive (notepad like keybindings crtl+c crtl+v etc.)
- nano : nano is a small and friendly editor.
- ne : Easy-to-use and powerful text editor 
- sed : GNU stream text editor (More useful in bash scripting)
- Vim : Vi IMproved - enhanced vi editor 
- Neovim : Neovim is an extension of Vim: feature-parity and backwards compatibility are high priorities.
- zile : Lightweight clone of the Emacs text editor 
* [Read wiki to learn more](https://wiki.termux.com/wiki/Text_Editors)

### IDEs
- Codiad 
- emacs
- vim
* [Read wiki to learn more](https://wiki.termux.com/wiki/IDEs)

### Package Management
Termux uses apt and dpkg for package management, similar to Ubuntu or Debian. Many quirks from Ubuntu are carried over here.

Install package(s):
```
pkg i <package name>
```
Update and upgrade packages:
```
pkg up <package name>
```
Remove/Uninstall Package(s):
```
pkg un <package name>
```
List files 'owned' by package:
```
pkg f <package name>
```
Reinstall a Package(s):
```
pkg re <package name>
```
Show some info about package(s):
```
pkg sh <package name>
```
Search package(s):
```
pkg se <package name> or <regex>
```
List all packages:
```
pkg list-a
```
List all installed packages:
```
pkg list-i
```
* A quick warning for root users: if you prefer to use apt over pkg - never run it as root as you will mess up file permissions and SELinux contexts so you won't be able to use it as normal user. If you did this and your environment was broken, do not ask for help - this is your own fault ! 

* [Read wiki to learn more](https://wiki.termux.com/wiki/Package_Management)

### Servers & Daemons
Termux is capable of accessing remote devices by using some common tools. It is also possible to turn a device running Termux into remote controlled server. 

- FTP Server (requires busybox):
```
busybox tcpsvd -vE 0.0.0.0 2121 busybox ftpd -w path/to/serve
```
Warning: -w allows upload 
and don't use port below 1024 or else you may get permission denied error.

- SSH server:
[Check this if you are using sshd](https://github.com/tomhiggins/TermuxSSHDsetup)

- HTTP Server:
```
busybox httpd -p 0.0.0.0:8080
```

- HTTP Proxy Server
```
tinyproxy -d
```
[Tinyproxy](https://tinyproxy.github.io/)

- MySQL/MariaDB Server
[Read
wiki page here](https://wiki.termux.com/wiki/MariaDB)
or
[Read the blog post here](https://www.nosware.com/web/install-mysql-server-termux-android/290/)

- Music Player Daemon aka mpd
[Read the wiki page here](https://wiki.archlinux.org/index.php/Music_Player_Daemon)
Or 
[Watch the Video Here](https://youtu.be/mfs3TKj9DVA)

- Bypass NAT
[Read the wiki page here](https://wiki.termux.com/wiki/Bypassing_NAT)

* [Read wiki to learn more it includes setting up ftpd, sshd, port forwarding, tor](https://wiki.termux.com/wiki/Remote_Access)

### Termux Services
To install termux services, run
```
pkg i termux-services
```
To then enable and run a service, run
```
sv-enable <service> 
```
If you only want to run it once, run
```
sv up <service> 
```
To later stop a service, run:
```
sv down <service> 
```
Or to disable it
```
sv-disable <service>
```
* [Read wiki to learn more](https://wiki.termux.com/wiki/Termux-services)

### IRC

- ERC is an IRC client for Emacs.
- irssi is an IRC client.
- weechat is an IRC chat client.

### Proot (Run Linux Distributions inside Termux)
- Arch (Thanks to sdrausty)
- Archstrike (just modifies the pacman.conf file)
- Blackarch (just modifies the pacman.conf file)
- Debian (Thanks to sp4rkie)
- Fedora (Thanks to nmilosev)
- Slackware (Thanks to gwenhael)
- Ubuntu (Thanks to neo-oli)
- Alpine Linux (Thanks to Hax4us)
* [Read wiki to learn more](https://wiki.termux.com/wiki/PRoot)

### Termux Related Stuff That might be useful 
- [Termux-Launcher](https://github.com/amsitlab/termuxlauncher)
- [Termux-WebUI](https://github.com/wcchoi/swell.sh/)
- [Termux-ADB](https://github.com/MasterDevX/Termux-ADB)
- [Atilo (Automated Linux installer for termux)](https://github.com/YadominJinta/atilo)
- [Lazymux (Automated pentesting tools installer for termux)](https://github.com/Gameye98/Lazymux)
- [Graphical Environment(x-11) for termux](https://wiki.termux.com/wiki/Graphical_Environment)
- [Termux Machine Learning](https://github.com/sanheensethi/Installing-ML-In-Termux-Python)
-  phpmyadmin
[Read the blog post here](https://parzibyte.me/blog/en/2019/04/28/install-apache-php-7-android-termux/)
- Android as VPS using termux [Read Here](https://dev.to/b3nsh4/android-phone-into-a-vps-hosting-server-hosting-apps-nginx-music-server-and-a-lot-14on)
- Termux Dotfiles worth checking out [Click ME!](https://github.com/onlurking/termux)

### Keyboard Shortcuts
The following shortcuts are available when using Termux with a hardware (e.g. bluetooth) keyboard and also with [hacker's keyboard](https://f-droid.org/en/packages/org.pocketworkstation.pckeyboard/) on most devices:

* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>C</kbd> → Create new session
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>R</kbd> → Rename current session
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>↓</kbd> or <kbd>N</kbd> → Next session
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>↑</kbd> or <kbd>P</kbd> → Previous session
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>→</kbd> → Open drawer
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>←</kbd> → Close drawer
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>F</kbd> → Toggle full screen
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>M</kbd> → Show menu
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>U</kbd> → Select URL
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>V</kbd> → Paste
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>+</kbd> or <kbd>-</kbd> → Adjust text size
* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>1-9</kbd> → Go to numbered session
* [Source Termux-Wiki](https://wiki.termux.com/wiki/Main_Page)



### Some aliases that i use:
```
alias a='startarch' # For starting termux arch
alias cls='clear'
alias e='logout'
alias gcl='git clone'
alias h='htop'
alias j='jobs'
alias nano='nano -m' # Enable Touch/Mouse Support in nano
alias p='pwd'
alias q='exit'
alias rf='rm -rf'
alias weather='curl wttr.in/delhi-india' # change the place to yours
alias pst=termux-clipboard-get # paste
alias cpy=termux-clipboard-set # copy
alias open=termux-open # open with external app
```

### FAQ
[Read The FAQs here](https://wiki.termux.com/wiki/FAQ)

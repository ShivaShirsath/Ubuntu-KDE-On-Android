<h1 align=center>Ubuntu On Android</h1>

**TermUX → [Download](https://f-droid.org/packages/com.termux) / [Install](https://play.google.com/store/apps/details?id=com.termux)**
+ **Update & upgrade & SetUp Storage**
  ```bash
  pkg update -y && pkg upgrade -y && termux-setup-storage
  ```
+ **Install [Proot-Distro](https://github.com/termux/proot-distro) & Ubuntu CLI & Login to CLI**
  ```bash
  pkg install proot-distro -y && proot-distro install ubuntu && proot-distro login ubuntu
  ```
+ **Install sudo ( root / super user ) & Update & Upgrade**
  ```bash
  apt update -y && apt install sudo -y && sudo apt update -y && sudo apt upgrade -y && sudo apt install -y apt-utils dialog git wget
  ``` 
<!--
+ Add User
```bash
adduser <UserName> && echo "<UserName> ALL=(ALL:ALL) ALL" >> /etc/sudoers
```
+ **Install udisks2**
```bash
rm -rf /var/lib/dpkg/info/*.postinst && sudo dpkg --configure -a && sudo apt install udisks2 -y && rm -rf /var/lib/dpkg/info/*.postinst && sudo dpkg --configure -a
``` -->

<details>
<summary> DESKTOP </summary>
<ul>
<li><p><strong>Mate</strong></p>
<ul>
<li>DESKTOP <code>ubuntu-mate-desktop</code></li>
<li>START-UP <code>mate-session</code></li>
</ul>
</li>
<li><p><strong>Kubuntu</strong></p>
<ul>
<li>DESKTOP <code>kubuntu-desktop</code></li>
<li>START-UP <code>startplasma-x11</code></li>
</ul>
</li>
<li><p><strong>Light weight X11</strong></p>
<ul>
<li>DESKTOP <code>lxde</code></li>
<li>START-UP <code>startlxde</code></li>
</ul>
</li>
<li><p><strong>X Forms Common</strong></p>
<ul>
<li>DESKTOP <code>xfce4 xfce4-goodies</code></li>
<li>START-UP <code>startxfce4</code></li>
</ul>
</li>
</ul>

</details>

  ```bash
  sudo apt install -y `DESKTOP` 
  ```
###### vnc
+ **Setting Virtual Network Computing ( VNC ) Server**
  ```bash
  PWDx=$PWD && cd $HOME && rm -rf VNC && git clone https://github.com/ShivaShirsath/VNC.git && cd VNC && bash install && cd $PWDx
  ```
+ **cammand for start or stop vnc**
  ```bash
  vnc 
  ```
  

<details>

<summary>Bonus 🥳</summary>
<p>
<code>
sudo apt install -y firefox fonts-indic fonts-emojione openjdk-8-jdk

# Mozilla
# Indian Fonts - हिंदी, देवनागरी, मराठी, ગુજરાતી, ਪੰਜਾਬੀ, ಕನ್ನಡ, മലയാളം, తెలుగు, … etc, etc.
# Emojies - 😎, 😃, ❤, 😍, 😂, 👍, 😊, 🎉 … etc, etc.
# java, javac, appletviewer, jar … etc, etc.
</code></p>
</details>

[SS](Simple.md)

+ Install TermUX opener on Ubuntu
  ```bash
  wget https://raw.githubusercontent.com/ShivaShirsath/Ubuntu-On-Android/main/TermUX.desktop -O $HOME/Desktop/TermUX.desktop && chmod +x $HOME/Desktop/TermUX.desktop
  ```

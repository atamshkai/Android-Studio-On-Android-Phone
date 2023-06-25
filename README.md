# Android-Studio-On-Android-Phone

This is a preinstalled debian-linux distro with android studio.You can really create your own applications and many projects from github and others.
Before you install it , disable phantom process killer.Watch from here.

[Youtube](https://youtu.be/UxmQSETvAOc)

## Preview

![](https://raw.githubusercontent.com/atamshkai/Android-Studio-On-Android-Phone/main/Debian%20Android%20Studio.png)

# To Do

#### First,Download Debian Distro From Here,

[Link](https://www.mediafire.com/file/grzre0zxsrwmxkc/debian.tar.xz/file)

## Installation

Download debian.tar.xz to Device's Download folder first.

### Install zsh

```
pkg up -y && pkg i -y zsh wget

wget https://github.com/atamshkai/Termux-Zsh/raw/main/zsh.tar.xz

tar -xvJf zsh.tar.xz && mv zsh/.* ~/ && rm -rf zsh

chsh -s zsh
```

Then,

```
echo "killall pulseaudio &>/dev/null" >>~/.zshrc
```

``` 
echo "pulseaudio --start --exit-idle-time=-1; pacmd load-module module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" >>~/.zshrc
```

```
pkg up -y && pkg i -y x11-repo && pkg i -y proot-distro pulseaudio termux-x11-nightly
```

``` 
termux-setup-storage
```

``` 
proot-distro restore /sdcard/download/debian.tar.xz
```

```
exit
```

Login again to terminal

Before login to proot,start termux-x11 first.
 
```
termux-x11 :1
```
 
Then,open another session & login
 
```
proot-distro login debian --shared-tmp
```
 
Then
 
```
export PULSE_SERVER=127.0.0.1;env DISPLAY=:1 dbus-launch --exit-with-session xfce4-session
```
 
OR 
 
```
tm-x11
```

# Manual Installation


If you want to install android-studio manually,use debian or kali.Then install desktop-gui and download android-studio.


```
apt update && apt install -y apt-utils;apt install -y nano xfce4 xfce4-goodies default-jtk
```

### Download_Android_Studio

[Link](https://www.androiddevtools.cn/android-studio)

# Notic

To use Android Studio,You must set Gradle's home or you will get errors

Examples

```
export ANDROID_SDK_ROOT=$HOME/android-sdk
```
```
export GRADLE_USER_HOME=$HOME/.gradle
```
```
export ANDROID_SDK_ROOT=/Users/android/android-sdk-linux export PATH=$PATH:$ANDROID_SDK_ROOT/tools
```

##### Termux_x11

[Link](https://github.com/atamshkai/termux-x11)

##### Termux_monet

[Link](https://github.com/atamshkai/termux-monet)

##### Android_SDK 

[Download](https://github.com/AndroidIDEOfficial/androidide-tools/releases/download/sdk/android-sdk.tar.xz)

##### Android_Build_Tools(for_termux)

[Download](https://github.com/AndroidIDEOfficial/androidide-tools/releases/download/v33.0.3/build-tools-33.0.3-aarch64.tar.xz)

##### Android_Platform_Tools(for_termux)

[Download](https://github.com/AndroidIDEOfficial/androidide-tools/releases/download/v33.0.3/platform-tools-33.0.3-aarch64.tar.xz)

##### Android_Command_Line_Tools(for_termux)


[Download](https://github.com/AndroidIDEOfficial/androidide-tools/releases/download/sdk/cmdline-tools.tar.xz)

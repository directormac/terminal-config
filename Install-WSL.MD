### [🧑‍💻Git link](https://github.com/yuk7/ArchWSL)
### [⬇Download](https://github.com/yuk7/ArchWSL/releases/latest) | [📓Docs](https://wsldl-pg.github.io/ArchW-docs/)

### 💾Install
```sh 
.\Arch.exe
```

### Set up default user
```sh
>Arch.exe
[root@PC-NAME ~] echo "%wheel ALL=(ALL) ALL" > /etc/sudoers.d/wheel

[root@PC-NAME ~] useradd -m -G wheel -s /bin/bash artifex

[root@PC-NAME ~] passwd artifex

[root@PC-NAME ~] exit

> Arch.exe config --default-user artifex


```
### Init Keyring

```sh
>Arch.exe
[artifex@PC-NAME]$ sudo pacman-key --init

[artifex@PC-NAME]$ sudo pacman-key --populate

[artifex@PC-NAME]$ sudo pacman -Sy archlinux-keyring

[artifex@PC-NAME]$ sudo pacman -Su

```

# Proceed to README


Official Guide Here
https://wsldl-pg.github.io/ArchW-docs/How-to-Setup/


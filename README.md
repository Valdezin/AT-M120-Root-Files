# AT-M120-Root-Files
Definitely what you need to get ROOT in ALT Mive Style Folder


# Pre-requisites
- Unlocked Bootloader
    Make sure you have ADB and Fastboot Platform Tools
    1) Enable Developer Options in Settings by pressing `Build Number` until it says "You are now a Developer!"
    2) Navigate to Developer Options and enable OEM Unlocking
    3) Connect your device to your PC and send the command `adb reboot bootloader`
    4) After it boots to Flashboot mode, send the command `fastboot flashing unlock`
    5) Boot as normal by typing `fastboot reboot`

# HALT
Before anything else, check whether you have the same build number as in the [release](https://github.com/Valdezin/AT-M120-Root-Files/releases/tag/AT-M120KY1208S)
<img width="480" height="800" alt="image" src="https://github.com/user-attachments/assets/808e18f1-17de-42e1-b52d-1fbe9761a23e" />

If they do not match, ***STOP***, at this point you **must get the boot.bin yourself**

# How to get boot.bin yourself
At this point, I will assume that your bootloader is unlocked.
1) Download [SPFlashTool](https://spflashtool.com/download/)
2) Extract and open SPFlashTool and go to `Readback` Tab
3) Click add and double click the `Start Address`
   <img width="1011" height="677" alt="image" src="https://github.com/user-attachments/assets/059667ad-596d-474f-9906-4ea7a3a4bdd2" />
4) It will open File Explorer, name it however you like but for this I will name it `boot_sample.bin` (.bin is required)
   <img width="252" height="90" alt="image" src="https://github.com/user-attachments/assets/1b2bcf84-dfc2-4732-bebe-9c9d305e2606" />
5) Input `0x1F800000` as Start Address with the Length of `0x02000000` (32MB)
   <img width="432" height="503" alt="image" src="https://github.com/user-attachments/assets/bc6aac56-013a-433e-ba3d-ba8ed4a8be42" />
6) Click OK and Readback, make sure your phone is turned off
7) Plug the phone in your PC, if you see this checkmark then you have successfully got your `boot.bin`
   <img width="1017" height="622" alt="image" src="https://github.com/user-attachments/assets/03900963-c981-4826-97f3-fab6409a8eb2" />


# Installation
1) Go to [release](https://github.com/Valdezin/AT-M120-Root-Files/releases/tag/AT-M120KY1208S) and download the patched img that is the same as your build number
2) Install using your pc via `fastboot flash boot.img` (or whatever the name is)
3) You have successfully rooted your device!

*IF YOU GOT BOOT.BIN YOURSELF*
1) Copy the `boot.bin` to your phone
2) Install Magisk and patch the `boot.bin`
3) Copy the patched `boot.bin` to your pc
4) Install using your pc via `fastboot flash boot.img` (or whatever the name is)
5) You have successfully rooted your device!

# Acknowledgements
Magisk (https://github.com/topjohnwu/magisk)
SPFlashtool (https://spflashtool.com)



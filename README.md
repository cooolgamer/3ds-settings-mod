# 3DS System Settings Mod

## Making your own wallpaper
### Prerequites:
- Kuriimu, Karameru and Kukkii bundled in this [release page](https://github.com/IcySon55/Kuriimu/releases)
- A modded 3DS (use [This guide](https://3ds.hacks.guide/) if you didn't modded yours already)
- The [Background template file](https://raw.githubusercontent.com/cooolgamer/3ds-settings-mod/main/bg_white%20-%20template.bclim), [Top screen layout](https://raw.githubusercontent.com/cooolgamer/3ds-settings-mod/main/Bg_U_00.bclyt) and [Bottom screen layout](https://raw.githubusercontent.com/cooolgamer/3ds-settings-mod/main/Bg_D_00.bclyt)
- A good image editor (paint.net do the job)
  
### Extracting romfs:
- Open godmode9 (hold start while booting)
- Go to CTRNAND, titles, 00040010, 0002X000 (X can be any number), content and select the .tmd file
- Select TMD file options and mount cxi/nds image to drive then press A
- Open the romfs folder
- Highlight the ``base_LZ.bin`` file and press Y to copy it
- Press B two times to go to the main menu
- Go to sdcard then press Y to paste it
- Power off and insert the sdcard on your computer then copy the ``base_LZ.bin`` file on the folder you're doing the mod on

### Editing and injecting the wallpaper
- Let's start by opening the ``bg_white - template.bclim`` file on kukkii and export it to PNG

  ![image](https://github.com/cooolgamer/3ds-settings-mod/assets/64099608/caa087aa-e3e7-458d-bc7c-5590823ae64e)
- Edit the image and import it through kukkii, then save it (ctrl + s is your friend :p)
- Now the image file is done, you have to put it on the archive so first, open karameru
- Go to Tools > Compression > Nintendo > Decompress > General just like the image below

  ![image](https://github.com/cooolgamer/3ds-settings-mod/assets/64099608/936854d5-8cc2-443e-8844-de0de08677f7)
- Open base_LZ.bin file from the romfs folder previously copied and save the uncompressed file
- Open the uncompressed base_LZ file, go to timg, bg_white.bclim and press replace file

  ![image](https://github.com/cooolgamer/3ds-settings-mod/assets/64099608/1b7548ba-c75e-440e-b25f-d4dcf3eb8896)
- Replace it with the edited background (bg_white - template.bclim)
- Right click on blyt folder and select replace blyt
  
  ![image](https://github.com/cooolgamer/3ds-settings-mod/assets/64099608/eeaa3118-ed73-4ee8-9b7b-47f9b5b813f3)
- Select the folder you put the top and bottom screen layouts in (those files are important as they resize the wallpaper and remove the yellow gradient)
- Save the changes (again, ctrl+s is your friend)
- Go to Tools > Compression > Nintendo > Compress > LZ10

  ![image](https://github.com/cooolgamer/3ds-settings-mod/assets/64099608/5052318f-8add-4932-918e-f315b0497e40)
- Replace the ``base_LZ.bin`` file while compressing, the file should now be modded with your modifications

### Installation
- In your sdcard, go to luma/titles and create a folder named the following depending of your region:
  - ``0004001000022000`` for Europe
  - ``0004001000021000`` for USA
  - ``0004001000020000`` for Japan
- Create a "romfs" folder inside and put your base_LZ.bin file inside

  (A valid path for Europe would be `luma/titles/0004001000022000/romfs/base_LZ.bin`)
- Don't forget to enable game patching on luma config (hold select while booting)
- Enjoy!

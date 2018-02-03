# Windows 10 Setup Guide

Todos after installing Windows 10

## Table of Contents

* [Todos](#todos)
  * [Clean up Start menu](#clean-up-start-menu)
  * [Clean up Taskbar](#clean-up-taskbar)
  * [Remove bloatware I](#remove-bloatware-i)
  * [Remove bloatware II](#remove-bloatware-ii)
  * [Adjust Privacy settings](#adjust-privacy-settings)
  * [Disable content indexing on SSDs](#disable-content-indexing-on-ssds)
  * [Install Windows updates](#install-windows-updates)
  * [Make File Explorer open This PC by default instead of Quick Access](#make-file-explorer-open-this-pc-by-default-instead-of-quick-access)
  * [Remap default folder locations to a separate HDD](#remap-default-folder-locations-to-a-separate-hdd)
  * [Disable Start-up processes](#disable-start-up-processes)
* [References](#references)

## Todos

### Clean up Start menu

1. Unpin all tiles from Start.
2. After unpinning all tiles, you will be left with a wide empty space. Drag the edge of the Start menu to the left to remove the space.
3. Go to `Settings > Personalization > Start`.
4. Turn off all switchboxes except `Show app list in Start menu`.

### Clean up Taskbar

1. Go to `Settings > Personalization > Taskbar`.
2. Turn off `Show badges on taskbar buttons`.
3. Click `Turn system icons on or off`.
4. Turn off system icons you don't want to see. Personally, I'll turn off `Location`, `Action Center` and `Input Indicator`.
5. Under `People`, turn off all switchboxes.

### Remove bloatware I

1. Go to `Settings > Apps > Apps & Features`.
2. Uninstall all apps you don't need.

### Remove bloatware II

Download bloatware removal scripts from [W4RH4WK](https://github.com/W4RH4WK):
```
https://github.com/W4RH4WK/Debloat-Windows-10/archive/master.zip
```

NOTE: You don't need to run all scripts. Just select the ones you want.

1. Open Powershell as administrator.
2. Enable execution of scripts.

  ```
  > Set-ExecutionPolicy Unrestricted
  > cd \path\to\scripts
  > ls -Recurse *.ps1 | Unblock-File
  > ls -Recurse *.psm1 | Unblock-File
  ```

3. Select a script and run:

  ```
  > {script-filename}.ps1
  ```

### Adjust Privacy settings

1. Go to `Settings > Privacy`.
2. Under `General`, turn off all switchboxes.
3. Under `Background apps`, turn off `Let apps run in the background` (if you have a slow machine).
4. Go to `Settings > Search`.
5. Under `Permissions & History`, turn off `Windows Cloud Search` and `My device history`.

### Disable content indexing on SSDs

If you installed Windows 10 on an SSD, you might want to disable content indexing:

1. Go to `File Explorer > This PC`.
2. Right click on your disk then select `Properties`.
3. Under `General`, uncheck `Allow files on this drive to have contents indexed in addition to file properties`.
4. Click Apply.

## STOP. Reboot PC first before proceeding

### Install Windows updates

1. Go to `Settings > Update & Security`.
2. Click `Check for updates`.
3. Wait for all updates to install.

### Start downloading and installing your apps

### Make File Explorer open This PC by default instead of Quick Access

1. Open `File Explorer`.
2. Go to `File > Change folder and search options`.
3. On `Open File Explorer to`, select `This PC`.
4. Uncheck `Show recently used files in Quick Access`.
5. Uncheck `Show frequently used folders in Quick Access`.

### Remap default folder locations to a separate HDD

As much as possible, your SSD should only contain Windows 10 and your apps. The target locations of the default folders (`Documents`, `Downloads`, `Desktop`, etc.) can be remapped to a separate HDD.

1. Right click a default folder.
2. Go to `Properties > Location`.
3. Change the target location to the location of your HDD. For example, to move `Documents` to drive `D:`, set the target location to `D:\Documents`.
4. Click Apply.

### Disable Start-up processes

1. Hit `Ctrl + Shift + Esc`.
2. Under `Start-up`, select processes you want to disable.

## References

* http://darrellx.com/buildapc/setting-up-your-new-computer-right/
* http://darrellx.com/buildapc/how-to-remap-default-folder-locations-ssd-hdd/
* https://www.howtogeek.com/219936/how-to-disable-quick-access-in-file-explorer-on-windows-10/
* https://www.reddit.com/r/Windows10/comments/3f0gii/how_to_remove_start_junk/
* https://github.com/W4RH4WK/Debloat-Windows-10

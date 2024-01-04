# windows-post-install.bat

This batch script automatically installs the programs I use in my PC, runs updates and apply some personal preferences. Works fine on **Windows 10** & **Windows 11**.

### Winget

Winget is the Windows Package Manager (as good as '*apt install*' on Linux, no joke). The winget command line tool enables users to discover, install, upgrade, remove and configure applications on Windows 10 and Windows 11 computers. This tool is the client interface to the Windows Package Manager service. It's pre-installed by default on Windows 10 and 11, but it may needs to be updated just after installing the OS (relax, this script will do it for you).

For further information and troubleshooting, please visit [winget's Github repository](https://github.com/microsoft/winget-cli).

#
### Usage
1. Define the programs to be installed in file `apps.txt` by it's "winget ID". 
    - **Note:** In case you don't know the ID of an app, use `winget search <appname>` on terminal.

2. Define the download url of programs to be downloaded in file `urls.txt`.

3. Run `windows-post-install.bat` as admin.

#
### Customization Tools

* [Windows 11 Cursors Concept](https://www.deviantart.com/jepricreations/art/Windows-11-Cursors-Concept-v2-886489356) - a modern option to customize Windows mouse cursor.
* [TranslucentTB](https://apps.microsoft.com/store/detail/translucenttb/9PF4KZ2VN4W9?hl=en-us&gl=us) - a good choice for bringing a modern translucent look for Windows taskbar.

#
### Useful Commands

* Fix for TranslucentTB (making taskbar translucent):

    1. Download [ViVeTool](https://github.com/thebookisclosed/ViVe).

    2. Run this commands inside ViVe's directory as admin:

    ``` batch
    vivetool /disable /id:26008830 && vivetool /disable /id:38764045
    ```

#
**Popular App ID Names**:
- `9NKSQGP7F2NH` = *WhatsApp Desktop*
- `9NCBCSZSJRSB` = *Spotify Client*
- `9PF4KZ2VN4W9` = *TranslucentTB*
- `9WZDNCRF0083` = *Facebook Messenger*

#
**Old tools URLs**:
- https://github.com/thebookisclosed/ViVe/releases/latest/download/ViVeTool-v0.3.3.zip = *ViVeTool*
- https://github.com/liballeg/allegro5/releases/download/5.2.8.0/allegro-x86_64-w64-mingw32-gcc-12.1.0-posix-seh-static-5.2.8.0.zip = *Allegro*
- https://windows.php.net/downloads/releases/php-8.2.10-nts-Win32-vs16-x64.zip = *PHP*
- https://sonik.dl.sourceforge.net/project/luabinaries/5.4.2/Tools%20Executables/lua-5.4.2_Win64_bin.zip = *Lua*
- https://get.enterprisedb.com/postgresql/postgresql-16.0-1-windows-x64.exe = *PostgreSQL*

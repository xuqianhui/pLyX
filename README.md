# pLyX System
The pLyX system is a scripting system for LyX. Or rather, LyX has a built-in scripting system, but it seems to have been created by accident, few know of it, and it has certainly received no development to make its use convenient for the user. The pLyX system is an attempt to create a workable interface for this system out of the tools that LyX provides -- modules, custom insets, toolbar buttons -- and also to provide some initial scripts.
manipulate
# Docs
## Installation
### Windows
* Python:
  * Download and run the Python 2.7 installer (either the "Windows x86 MSI Installer" or "Windows x86-64 MSI installer").
  * Open the Windows Start menu.
  * Search for "Edit the system environment variables", and then click it.
  * Click `Environment Variables`.
  * Select `PATH` in the `System variables` section.
  * Click `Edit`.
  * Add `;C:\Python27;C:\Python27\Scripts` to the end of the list (the paths are separated by semicolons). For example: `C:\Windows;C:\Windows\System32;C:\Python27;C:\Python27\Scripts`.
  * Verify that it worked by opening your command prompt and entering `python`. You should see the `>>>` prompt.
  * Install `pip` by opening command prompt and entering `easy_install pip`.
  * Installed required packages for Python by running `pip install -r requirements.txt`.
* Copy files:
  * copy contents of `doc` folder to `C:\Users\<YourUserName>\AppData\Roaming\LyX2.1\doc`
  * copy contents of `layouts` folder to `C:\Users\<YourUserName>\AppData\Roaming\LyX2.1\layouts`
  * copy contents of `images` folder to `C:\Users\<YourUserName>\AppData\Roaming\LyX2.1\images`
  * copy contents of `scripts` folder to `C:\Users\<YourUserName>\AppData\Roaming\LyX2.1\scripts`
  * copy contents of `ui` folder to `C:\Users\<YourUserName>\AppData\Roaming\LyX2.1\ui`
* You ready to [setup LyX](#setup-lyx).

### Mac OS X
* Python:
  * Check that you have Python installed by running `python` in terminal. Normally Mac OS X comes with Python preinstalled.
  * Check that you have pip installed by running in terminal `pip freeze`. If not install with `sudo easy_install pip`.
  * Installed required packages for Python by running `sudo pip install -r requirements.txt`.
* Copy files:
  * copy contents of `doc` folder to `/Applications/LyX.app/Contents/Resources/doc`
  * copy contents of `layouts` folder to `/Applications/LyX.app/Contents/Resources/layouts`
  * copy contents of `images` folder to `/Applications/LyX.app/Contents/Resources/images`
  * copy contents of `scripts` folder to `/Applications/LyX.app/Contents/Resources/scripts`
  * copy contents of `ui` folder to `/Applications/LyX.app/Contents/Resources/ui`
* You ready to [setup LyX](#setup-lyx).

### Linux
* Python
  * Check that you have Python installed by running `python` in terminal. Normally Linux comes with Python preinstalled.
  * Check that you have pip installed by running in terminal `pip freeze`. If not install with `sudo apt-get install python-pip`.
  * Installed required packages for Python by running `sudo pip install -r requirements.txt`.
* Copy files:
  * copy contents of `doc` folder to `/home/<YourUserName>/.lyx/doc`
  * copy contents of `layouts` folder to `/home/<YourUserName>/.lyx/layouts`
  * copy contents of `images` folder to `/home/<YourUserName>/.lyx/images`
  * copy contents of `scripts` folder to `/home/<YourUserName>/.lyx/scripts`
  * copy contents of `ui` folder to `/home/<YourUserName>/.lyx/ui`
* You ready to [setup LyX](#setup-lyx).

### Setup LyX
* open LyX.
* define File format for `pLyX` in `Tools -> Preferences -> File Handling -> File Formats`:
  * click `New` button and enter `pLyX` in the Format box;
  * set the `Document format` check box;
  * enter `plyx` in the `Short Name` box;
  * enter `lyx` in the `Extension` box;
  * under `Viewer` choose `Custom` and enter `LyX` in the box on the right;
  * Click `Apply`.

![](screens/pLyX_fileformat.png)

* define File format for `qLyX` in `Tools -> Preferences -> File Handling -> File Formats`:
  * click `New` button and enter `qLyX` in the Format box;
  * enter `qlyx` in the `Short Name` box;
  * None of the other check boxes or slots should be filled;
  * Click `Apply`.

![](screens/qLyX_fileformat.png)

* define converter from LyX to pLyX in `Tools -> Preferences -> File Handling -> Converters`:
  * by scrolling in the list `From format` select `LyX`;
  * by scrolling in the list `To format` select `pLyX`;
  * enter in `Converter` box:
    * for Windows: `python C:\Users\<YourUserName>\AppData\Roaming\LyX2.1\scripts\pLyX.py $$i $$o`;
    * for Mac OS X: `python /Applications/LyX.app/Contents/Resources/scripts/pLyX.py $$i $$o`;
    * for Linux: `python /home/<YourUserName>/.lyx/scripts/pLyX.py $$i $$o`;
  * click `Add` and `Apply`.

![](screens/pLyX_converter.png)

* define converter from LyX to qLyX in `Tools -> Preferences -> File Handling -> Converters`:
  * by scrolling in the list `From format` select `LyX`;
  * by scrolling in the list `To format` select `qLyX`;
  * enter in `Converter` box:
    * for Windows: `python C:\Users\<YourUserName>\AppData\Roaming\LyX2.1\scripts\qLyX.py $$i $$o`;
    * for Mac OS X: `python /Applications/LyX.app/Contents/Resources/scripts/qLyX.py $$i $$o`;
    * for Linux: `python /home/<YourUserName>/.lyx/scripts/qLyX.py $$i $$o`;
  * click `Add` and `Apply`.

* Choose in menu `Tools -> Reconfigure`

![](screens/qLyX_converter.png)

## Using pLyX scripts
To be here


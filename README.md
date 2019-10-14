# 7zS_x64.sfx
7zS_x64.sfx compiled from source

# Steps to Produce
+ Download the 7-Zip source code from https://sourceforge.net/projects/sevenzip/files/7-Zip/17.00/7z1700-src.7z/download
  + Note: Newer versions may be available
+ Extract the 7-Zip source code to %userprofile%\Desktop\7z1700-src
+ Right-click %userprofile%\Desktop\7z1700-src, select Properties, un-check Read-only, and click OK
+ In the "Confirm Attribute Changes" window, click OK
+ Modify %userprofile%\Desktop\7z1700-src\CPP\Build.mak:
  +	Remove all content from lines 17 & 19-23 (so only line 18 remains with the value "MY_ML = ml64 -Dx64")
  +	Delete " -OPT:NOWIN98" from the end of line 33
+ Download "Build Tools for Visual Studio 2017" from https://www.visualstudio.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=15
+ Run the "Build Tools for Visual Studio 2017" installer
  +	Leave the default "Visual C++ build tools" option selected, click "Install", and let the installation complete
+ Launch "x64 Native Tools Command Prompt for VS 2017" from "C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Visual Studio 2017\Visual Studio Tools\VC"
+ In the "x64 Native Tools Command Prompt for VS 2017" (x64 Tool Prompt), run the following commands:
  + 	cd %userprofile%\Desktop\7z1700-src\CPP\7zip\Bundles\SFXSetup
  + 	nmake
+ The compilation process should complete and the 64-bit 7zS.sfx file should be located in %userprofile%\Desktop\7z1700-src\CPP\7zip\Bundles\SFXSetup\O\7zS.sfx

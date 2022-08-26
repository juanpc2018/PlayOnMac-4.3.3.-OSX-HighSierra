## PlayOnMac-4.3.3.-OSX-HighSierra </p>

OSX HighSierra 10.13.6 </br>
is the last 32/64-Bit OSX, with full support for NVMe, APFS. </br>
its the bridge between 64-Bit Only and 32-Bit OSX. </p>

OSX HighSierra 10.13.3 or 10.13.4 Beta1, Beta2, Beta3, Beta4 </br>
allow eGPU with TB2 macs, like MacMini 2014. </br>
since 10.13.4 TB2 support was Deleted, and Replaced with TB3 support, </br>
but Not all TB3 Macs are compatible with OSX HighSierra, research model on EveryMac.com </p>

...</br>
PlayOnMac last version for OSX HighSierra is 4.3.3 </br>
https://www.playonmac.com/en/download.html </br>
https://repository.playonmac.com/PlayOnMac/PlayOnMac_4.3.3.dmg </p>

But is completely broken, because the servers changed, MS deleted installers, etc... </br>
PlayOnMac 4.3.3 No longer works with Automatic Download & Install, </br>
Requires Manual Download & install. </p>

Simple steps: must follow order. </br>
0. Download and install XQuartz: </br>
https://www.xquartz.org </br>
https://github.com/XQuartz/XQuartz/releases </br>
https://github.com/XQuartz/XQuartz/releases/download/XQuartz-2.8.2/XQuartz-2.8.2.dmg </p>

1. Doanload All 2.47.x Gecko 32 & 64-bit .msi from: </br>
https://dl.winehq.org/wine/wine-gecko/ </p>

if using Wine 2 or lower:
select the version you want, and download recommended. </br>
https://wiki.winehq.org/Gecko </p>

2. Doanload All Mono .msi from: </br>
https://dl.winehq.org/wine/wine-mono/ </br>
https://github.com/madewokherd/wine-mono/releases </p>

if only want to install 1x Wine version, download recommended: </br>
https://wiki.winehq.org/Mono </p>

3. Download PlayOnMac.dmg and install, do Not Run. </br>
4. copy all Mono & Gecko .msi to 
/Users/$(whoami)/.cache/wine </p>
optional: </br>
/Users/$(whoami)/Library/PlayOnMac/wine/gecko </br>
/Users/$(whoami)/Library/PlayOnMac/wine/mono </p>

5. Download All: </br>
PlayOnLinux-wine-*.*-upstream-darwin-x86.tar.gz </br>
and </br>
all 
x64.tar.gz </br>
from: </br>
https://www.playonmac.com/wine/binaries/phoenicis/ </br>
https://www.playonmac.com/wine/binaries/phoenicis/upstream-darwin-x86 </br>
https://www.playonmac.com/wine/binaries/phoenicis/upstream-darwin-amd64/ </p>

Version 6.18 and Higher may have compatibility issues with PlayOnMac 4.3.3 </p>
 
6. Copy all tar.gz to a folder, and split the 32-it & 64-Bit to another folders. </p>
7. UnZip all .tar.gz inside the 32-bit & 64-bit forlder. </p>
8. Rename all extracted folders, remove everything exept the version number, </br>
from: </br>
/Downloads/POM433/32bit/PlayOnLinux-wine-7.11-upstream-darwin-x86 </br>
/Downloads/POM433/64bit/PlayOnLinux-wine-7.11-upstream-darwin-amd64 </br>
to: </br>
/Downloads/POM433/32bit/7.11 <br>
/Downloads/POM433/64bit/7.11 <br>
do the same for all extracted folders </br>
UnZip, Rename, leave Only version number. </p>

9. copy all 32-bit renamed folders to: </br>
/Users/$(whoami)/Library/PlayOnMac/wine/darwin-x86 </br>
all 64-bit renamed folders to: </br>
/Users/$(whoami)/Library/PlayOnMac/wine/darwin-amd64 </p>

Then you can Run PlayOnMac 4.3.3 </br>
install or run any .exe the usual way. </br>
create a Virtual Drive for 32-Bit </br>
another Virtual Drive for 64-Bit. </br>
Configure, Select Desired Wine version for each Virtual Drive. </br>
Run TaskManager to Test Wine version, and automatically install Gecko and Mono for that drive. </p>

IF does Not install Gecko & Mono automatically, is probably because you canceled / force quit a previous instalation, and Virtual Drive thinks its installed. </br>
Delete the Virtual Drive or Manual Force Install Gecko and Mono. </br>
$ wine start /i wine-mono-5.0.0-x86.msi </br>
$ sudo apt install winetricks </br>
$ winetricks </br>
$ wine start /i wine-gecko-2.47.1-x86.msi </br>
$ wine start /i wine-gecko-2.47.1-x86_64.msi </br>
$ winetricks </br>
select: [Select the default wine container] → [Run uninstaller]. In the pop-up interface, if you find wine-gecko related software, it means that the wine-gecko installation is successful. </br>
https://www.programmersought.com/article/93056517759/ </p>

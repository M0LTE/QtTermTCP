# QtTermTCP

See https://wiki.oarc.uk/packet:qttermtcp

## Building on Windows

As of 0.0.0.79 commit a5e1b1389cbd9b3718b9ae41277f90633154cf47 from git://vps1.g8bpq.net/QtTermTCP

With VS2022 on Windows 11

Requires:

 - C++ desktop development workload installed in VS Installer
 - Windows SDK 10.0.17763.0 (VS will tell you if the version needed is now different)
 - VS 2017 Build Tools
 - Qt Visual Studio Tools extension (Extension Manager)
 - Qt 5.14.2 (check version in QtInstall element in QtTermTCP.vcxproj) - you just need the msvc2017 bits

Notes:

- In the Qt VS Tools extension, add a Qt installation named “5.14.2” pointed at C:\Qt\Qt5.14.2\5.14.2\msvc2017\bin - this is referenced from the project file
- Run C:\Qt\Qt5.14.2\5.14.2\msvc2017\bin>windeployqt.exe C:\git\vps1.g8bpq.net\QtTermTCP\Win32\Debug

## Building on Debian-ish Linux

Tested on Ubuntu 24.04

```
sudo apt install -y qt5-qmake qtbase5-dev libqt5serialport5-dev qtmultimedia5-dev
mkdir build && cd build
qmake ..
make -j4
```

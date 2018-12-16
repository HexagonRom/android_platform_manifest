HexagonROM Pie Source 2018
===================


Getting Started

### Build Environment

- Tested and Working on any version of Ubuntu - 14.04,14.10,15.04 16.04 (64-bit)
- Any other distribution based of the Ubuntu Distro such as Lubuntu, Xubuntu and etc.
- Any form of Terminal
- Decent hardware (minimum of at least a dual core CPU and 4 GB of RAM)
- A storage unit of any kind (We recommend utilizing SSDs as Mechanical HDDs slow down the build proccess drastically and the minimum storage size is 70GB. Having more will be useful with CCache[More on that later])
- Required Packages should have been installed

### Required Package
### More copy and paste:
[Hint: Running this command installs the other required packages to build android]

# Initialize local repository

sudo apt-get install openjdk-8-jdk phablet-tools git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache libgl1-mesa-dev libxml2-utils xsltproc unzip schedtool meld lzop maven bc -y

# Sync
repo init -u https://github.com/HexagonRom/android_platform_manifest -b pie

repo sync -c -jx --force-sync --no-clone-bundle --no-tags

```

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -jX
```



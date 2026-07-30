# NebulaFD-Termux
Here's a test tutorial for anyone who wants to use NebulaFD on Termux, but I'm not 100% sure it actually works because no phone has enough RAW data for this. But let me know on Discord if you want to make a suggestion or find a bug.

## Special thanks to Yunivers, the creator of NebulaFD, who created this wonderful project. All credit goes to the original creator. Please follow the project here:
https://github.com/AITYunivers/NebulaFD

## How do I use NebulaFD (CLI) in Termux?
To do this, we first need to install Termux via F-Droid or GitHub. Here are the step-by-step commands:

```The code:
> pkg update && pkg upgrade -y
pkg install git proot-distro -y
proot-distro install ubuntu
proot-distro login ubuntu
apt update && apt upgrade -y
apt install -y wget curl git build-essential libicu-dev zlib1g zlib1g-dev
wget [https://dot.net/v1/dotnet-install.sh](https://dot.net/v1/dotnet-install.sh) -O dotnet-install.sh
chmod +x dotnet-install.sh
./dotnet-install.sh --channel 6.0
echo 'export DOTNET_ROOT=$HOME/.dotnet' >> ~/.bashrc
echo 'export PATH=$PATH:$HOME/.dotnet:$HOME/.dotnet/tools' >> ~/.bashrc
source ~/.bashrc
cd ~/NebulaRelease
cp runtimes/linux-arm64/native/libz.so ./
cp libz.so zlibwapi.dll
cp libz.so libzlibwapi.so
dotnet Nebula.dll


## NebulaFD-Termux

# How do I use NebulaFD (CLI) in Termux?
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


# RedmiBook16-QCA6174

Xiaomi RedmiBook 16 Ryzen Fedora 33 wifi Atheros QCA6174 fix

vendor=168c,device=003e,subsystem-vendor=11ad,subsystem-device=0847


yum remove linux-firmware*

mkdir -p /lib/firmware/ath10k/QCA6174/hw3.0

wget https://github.com/vpm/RedmiBook16-QCA6174/raw/main/board.bin -O /lib/firmware/ath10k/QCA6174/hw3.0/board.bin

wget https://github.com/vpm/RedmiBook16-QCA6174/raw/main/firmware-6.bin -O /lib/firmware/ath10k/QCA6174/hw3.0/firmware-6.bin

cat "options ath10k_core skip_otp=Y" > /etc/modprobe.d/ath10k_core.conf 

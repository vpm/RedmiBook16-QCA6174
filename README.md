# RedmiBook16-QCA6174

Xiaomi RedmiBook 16 Ryzen

vendor=168c,device=003e,subsystem-vendor=11ad,subsystem-device=0847

Fedora 33 wifi Atheros QCA6174 fix

mkdir -p /lib/firmware/ath10k/QCA6174/hw3.0

wget https://github.com/vpm/RedmiBook16-QCA6174/raw/main/board.bin -O /lib/firmware/ath10k/QCA6174/hw3.0/board.bin

wget https://github.com/vpm/RedmiBook16-QCA6174/raw/main/firmware-6.bin -O /lib/firmware/ath10k/QCA6174/hw3.0/firmware-6.bin


cat /etc/modprobe.d/ath10k_core.conf 
options ath10k_core skip_otp=Y

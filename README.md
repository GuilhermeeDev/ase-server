# ase-server
Ark Survival Evolved server in Codespace using arkmanager

# ase-server
Ark Survival Evolved server in Codespace using arkmanager

sudo apt update

sudo apt install -y \
    curl \
    lsof \
    libc6-i386 \
    lib32gcc-s1 \
    bzip2 \
    perl \
    rsync

curl -sL https://raw.githubusercontent.com/arkmanager/ark-server-tools/master/netinstall.sh | bash -s -- --me --perform-user-install --yes-i-really-want-to-perform-a-user-install

export PATH="$HOME/bin:$PATH"
source ~/.bashrc

arkmanager --version

arkmanager list-instances

mkdir -p ~/.config/arkmanager/instances && nano ~/.config/arkmanager/instances/main.cfg
''''
arkserverroot="$HOME/ARK"

serverMap="TheIsland"

ark_Port=7777
ark_QueryPort=27015
ark_RCONPort=32330

ark_SessionName="Meu ARK Server"

ark_MaxPlayers=10

ark_ServerPassword=""

ark_ServerAdminPassword="Admin123"

ark_ServerPVE=True

ark_DifficultyOffset=1.0
'''

arkmanager install && arkmanager update && arkmanager status
ls -lah ~/ARK && ls -lah ~/ARK/ShooterGame

# Instalando pelo SteamCMD 
~/steamcmd/linux32/steamcmd +login anonymous +app_info_update 1 +app_info_print 376030 +quit

para /home/codespace/ARK

rm -rf ~/ARK && mkdir -p ~/ARK

~/steamcmd/linux32/steamcmd \
    +force_install_dir /home/codespace/ARK \
    +login anonymous \
    +app_update 376030 \
    +quit

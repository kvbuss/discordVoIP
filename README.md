# discordVoIP 

###Installation 
```
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa # When prompted press Enter to continue
sudo apt install python3.8 python3-venv tmux
mkdir ~/discordVoIP_Server
cd ~/discordVoIP_Server
git clone "https://github.com/kvbuss/discordVoIP.git" ./
python3.8 -m venv env
``` 

###Usage
```
source ~/discordVoIP_Server/env/bin/activate
# right here you want to go to config.py and edit the fields according to the comments included in the file
tmux new-session -d -s discordVoIP_discordModule "python3.8 ~/discordVoIP_Server/discord_module.py"
tmux new-session -d -s discordVoIP_requestHandler "
python3.8 ~/discordVoIP_Server/requesthandler_module.py"
```

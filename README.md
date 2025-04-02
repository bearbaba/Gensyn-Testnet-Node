# Gensyn-Testnet-Node
Requirement	Details
CPU Architecture	arm64 or amd64
Recommended RAM	25 GB
CUDA Devices (Recommended)	RTX 3090, RTX 4090, A100, H100
Python Version	Python >= 3.10 (For Mac, you may need to upgrade)
Visit : Quick Pod Website
Sign Up using email address
Go to your email and verify your Quick Pod account
Click on Add button in the corner to deposit fund
You can deposit using crypto currency (from metamask) or using Credit card
Now go to template section and then select Ubuntu 22.04 jammy in the below
Now click on Select GPU and search RTX 4090 and choose it
Now choose a GPU and click on Create POD button
Your GPU server will be deployed soon
Now click on Connect option and then choose Connect to web terminal
 Installation
Install sudo
apt update && apt install -y sudo
Install other dependencies
sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl wget screen git && curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - && echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list && sudo apt update && sudo apt install -y yarn
Install Node.js and npm if not installed already
curl -sSL https://raw.githubusercontent.com/zunxbt/installation/main/node.sh | bash
Clone this repository
cd $HOME && [ -d rl-swarm ] && rm -rf rl-swarm; git clone https://github.com/zunxbt/rl-swarm.git && cd rl-swarm
Create a screen session
screen -S gensyn
Run the swarm
python3 -m venv .venv && . .venv/bin/activate && ./run_rl_swarm.sh
It will ask some questions, you should send response properly
Would you like to connect to the Testnet? [Y/n] : Write Y
Would you like to push models you train in the RL swarm to the Hugging Face Hub? [y/N] : Write N

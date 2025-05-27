# Blockcast
Setting up NODE
I already have a node running so I just used it to run this (Killing two birds with a stone)
Access Platform HERE
Signup with email on Blockcast
Connect spare Wallet (SOL)
Bind Twitter and Discord .
Complete quest in profile dashboard.
Node Installation
Supports Ubuntu Linux + Docker-based systems.
🔧 Requirements [ Minimum 2 CPU cores and 4GB RAM ]

Docker & Docker Compose installed
Basic terminal knowledge
Open ports (if behind NAT)
Update system & dependencies
sudo apt update && sudo apt upgrade -y
sudo apt install ca-certificates curl gnupg lsb-release -y
Add Docker Key & Install
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y
Enable and start Docker
sudo systemctl enable docker
sudo systemctl start docker
Verify Installation
docker --version
docker compose version
Clone Blockcast Repo
git clone https://github.com/Blockcast/beacon-docker-compose.git
cd beacon-docker-compose
Run Node
docker compose up -d
image

Check running container
docker ps
image

Get Hardware ID & Challenge Key
Run this command to generate the values:

docker compose exec blockcastd blockcastd init
You'll see output like Hardware ID: your-hardware-id and Challenge Key: your-challenge-key
Register Your Node
Visit Blockcast Website
Signup/sign in using email
Click the Manage Node and Register Node
Paste your Hardware ID and Challenge Key image
SUBMIT AND DONE!
Notes
Your node should remain online 24/7 to be eligible for rewards.
Use a VPS or cloud server if needed (e.g., Hetzner, Contabo).

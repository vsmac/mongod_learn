# mongod_learn

# Installtion of mongodb

# Check OS version

cat /etc/lsb-release

# Installation of dependencies

sudo apt-get install gnupg curl

# To import the MongoDB public GPG key, run the following command:

curl -fsSL https://www.mongodb.org/static/pgp/server-8.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-8.0.gpg \
   --dearmor

# Add mongodb repository

echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-8.0.gpg ] https://repo.mongodb.org/apt/ubuntu noble/mongodb-org/8.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-8.0.list

# Install mongodb

sudo apt-get update

sudo apt-get install -y mongodb-org

# You can start the mongod process by issuing the following command:

sudo systemctl start mongod

# To check mongodb status

sudo systemctl status mongod

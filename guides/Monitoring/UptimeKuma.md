# Monitoring and Telegram notifications by Uptime Kuma

### Update server:
> sudo apt update && sudo apt upgrade -y

### Install git

>sudo apt install git 

### Install Nodejs and npm

```
curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash - && \
sudo apt-get install nodejs -y && \
echo -e "\nnodejs > $(node --version).\nnpm  >>> v$(npm --version).\n"
```

### Install Uptime Kuma

```
cd $HOME
git clone https://github.com/louislam/uptime-kuma.git
cd uptime-kuma
npm run setup
```

### Install PM2 if you don't have it:

```
cd $HOME
sudo npm install pm2 -g && sudo pm2 install pm2-logrotate
```

### Start Server

> cd $HOME/uptime-kuma
sudo pm2 start server/server.js --name uptime-kuma

### Browse to http://localhost:3001 after starting.

> http://Your_Server_IP:3001

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

### Install PM2:

```
cd $HOME
sudo npm install pm2 -g && sudo pm2 install pm2-logrotate
```

### Start server.js

```
cd $HOME/uptime-kuma
sudo pm2 start server/server.js --name uptime-kuma
```

### Browse to http://localhost:3001 after starting.

> http://Your_Server_IP:3001

## Setup Monitoring

<img src="https://github.com/klochenko/klochenko/blob/main/guides/Monitoring/screens/0.png" width="400" alt="" />

<img src="https://github.com/klochenko/klochenko/blob/main/guides/Monitoring/screens/1.png" width="400" alt="" />


### Check your actual IP and port

<img src="https://github.com/klochenko/klochenko/blob/main/guides/Monitoring/screens/2.png" width="400" alt="" />

After success setup u will see:

<img src="https://github.com/klochenko/klochenko/blob/main/guides/Monitoring/screens/4.png" width="400" alt="" />

### Next - you need setup notifications in Telegram

<img src="https://github.com/klochenko/klochenko/blob/main/guides/Monitoring/screens/5.png" width="400" alt="" />

You can get a Bot token from https://t.me/BotFather
 | You can get Chat ID from https://t.me/userinfobot

After fill form - start your created bot and click Test and Save 

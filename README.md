# Gradient Network Bot

- Register: [https://app.gradient.network](https://app.gradient.network/signup?code=NK93Y3)
- Purchase proxies: Proxies Static Residental | [FREE 10 PREMIUM PROXIES](https://www.webshare.io/?referral_code=p7k7whpdu2jg) | [Free 100 Premium Proxies](https://proxyscrape.com/?ref=odk1mmj) | Good Premium Proxies (paid): [922proxy](https://www.922proxy.com/register?inviter_code=d03d4fed), [proxy-cheap](https://app.proxy-cheap.com/r/JysUiH), [infatica](https://dashboard.infatica.io/aff.php?aff=544)
- Usage document: [https://mirror.xyz](https://mirror.xyz/0xe8224b3E9C8d35b34D088BB5A216B733a5A6D9EA/jFFUw6Ew3rWThwMxXMoLaa1UMnV8axoQoMVN0EKEthY)

## Start with Node.js for single proxy usage
> This is OPTIONAL if you want to test a single proxy and check its support for Gradient or not
#### Install Node.js LTS
- [Windows 32-Bit](https://nodejs.org/dist/v20.9.0/node-v20.9.0-x86.msi) | [Windows 64-Bit](https://nodejs.org/dist/v20.9.0/node-v20.9.0-x64.msi)
- Linux: [Ubuntu/Debian](https://medium.com/@nsidana123/before-the-birth-of-of-node-js-15ee9262110c)

To install requirements, run command:
```bash
npm install 
```
Testing the proxy, run command:
- Linux:
```bash
sudo APP_USER='example@gmail.com' APP_PASS='password' PROXY=socks5://username@password@proxyhost:port node app.js
```
- Windows:
```bash
set APP_USER="example@gmail.com" && set APP_PASS="password" && set PROXY=socks5://username:password@proxyhost:port && node app.js
```

## Start with Docker with multiple proxies
#### Install Docker
- [Windows](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe)  | Tutorial : [English](https://medium.com/@supportfly/how-to-install-docker-on-windows-bead8c658a68) | [Indonesian](https://www.youtube.com/watch?v=u5hpc7jEx1U&ab_channel=BimaPutraPratama)
- Linux: [Ubuntu/Debian](https://phoenixnap.com/kb/install-docker-on-ubuntu-20-04) | [Video Tutorial](https://www.youtube.com/watch?v=1_l-TNKPw-0&ab_channel=FarukAlam-AI)

Pull the docker image:
```bash
docker pull overtrue/gradient-bot:latest
```

Save the proxy address to the `proxies.txt` file in the format, example:
```bash
socks5://username:password@proxyhost:port
http://username:password@proxyhost:port
socks5://proxyhost:port
http://proxyhost:port
```
Then start the container

- Linux:

```bash
docker run -d -e APP_USER=user@mail.com -e APP_PASS=password -v ./proxies.txt:/app/proxies.txt overtrue/gradient-bot
```
- Windows CMD:
>Change C:/Folder/Path/To/proxies.txt to your proxies.txt destination path
```bash
docker run -d -e APP_USER=user@mail.com -e APP_PASS=password -v C:/Folder/Path/To/proxies.txt:/app/proxies.txt overtrue/gradient-bot
```

Note: Please replace the `proxies.txt` path with the correct path, or `cd` to the directory where `proxies.txt` is located before executing the docker run command.

## View the running log

```bash
docker ps
```
This command will list all containers, find the corresponding container ID (the value corresponding to the "CONTAINER ID" column), and then execute:

```bash
docker exec -it <container_id> pm2 logs
```

## Delete the container

```bash
docker rm -f <container_id>
```

## Note

- Run this bot, and it will update your referrer code to my invite code if you don't have one.
- You can just run this bot at your own risk, I'm not responsible for any loss or damage caused by this bot. This bot is for educational purposes only.

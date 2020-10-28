# Task1-Cloud-Computing-Aws

Create Instance Aws

- Pilih launch image -> pilih AMI yang akan dipakai
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2001/01-Aws-choose%20image.jpg)

- Pilih Processor yang akan dipakai disini memakai 1core dan 1GB memory
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2001/02-aws-processor.jpg)

- Untuk storage capacity yang dipakai sebesar 8GB
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2001/03-aws-storage.jpg)

- Network untuk auto assign IP pilih disable. karna nantinya akan memakai elastic IP
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2001/05-aws-network.jpg)

- Security Group di allow port 22 80 443 dan port 3000 untuk aplikasi
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2001/04-aws-firewall.jpg)



App Instance Configuration

- Instalasi Nodejs dengan perintah "apt-get install nodejs -y"
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2002/01-aws-install-nodejs.jpg)

- Masuk ke folder Frontend dumbplay kemudian masukan perintah "npm install"
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2002/02-aws-npm-install.jpg)

- Untuk running app pada background install pm2
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2002/03-aws-pm2.jpg)

- Kemudian buat file dengan nama ecosystem.config.js dan isikan file seperti gambar dibawah
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2002/04-aws-pm2config.jpg)
- ketikan perintah pm2 start ecosystem.config.js
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2002/05-aws-pm2%20success.jpg)


Reverse Proxy Instance Configuration

- Instalasi Nginx dengan perintah "apt install nginx"
- Berikut konfigurasi file nginx yang mengarahkan ip private app server di port 3000
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2003/02-aws-dari-reverse%20proxy.jpg)
- Kemudian lakukan pengecekan pada browser ketikan ip public Server reverse proxy
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2003/01-aws-private-frontend.jpg)

Instalasi SSL With letsencrypt

- Untuk domain disini adalah azhari.instructype.com yang sudah didaftarkan pada cloudflare
- instalasi letsencrypt dengan perintah "sudo certbot --nginx"
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2004/aws-certbot.jpg)
- Pilih agree dan yes untuk instalasi 
- Terakhir check domain pada browser
![alt text](https://github.com/azhari7/Task1-Cloud-Computing-Aws/blob/main/Aws%2004/aws-https-sucess.jpg)

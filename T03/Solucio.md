# Solucio t03 FTP

![ftp portada](img\ftp.png)

## 1. instalacio del servei
``` bash
sudo apt install vsdtpd
```

![install ftp](img\installftp.png)

## 2 Fer una copia del archiu original
``` bash
cp /etc/vsftpd.conf /etc/vsftpd.bak
```
![](img\cpftp.png)

## 3 Archiu de configuracio
Habilitem la opcio anonymous_enable (yes) i reyniciem el servei

![yes](img\yes.png)

![restart](img\restart.png)

## 4. FTP Anonim
Comprovar que la carpeta "/srv/ftp" s'ha creat, i quins permisos te
Per punlicar harxius, ser descargats, cal copiarlos en acesta carpeta òbiament es pot crar una estructura de carpeta dins.
``` bash
tree  /rsv/
```
![carpeta](img\carpeta.png)

![anonymous](img\anonymous.png)

## 5.conexio al client
### 1 Instalar el ftp en el client 

``` bash
sudo apt install vsdtpd
```
![install ftp](img\installftp.png)

ens conectem emb els usuarirs que volem

``` bash
sudo apt install vsdtpd
```

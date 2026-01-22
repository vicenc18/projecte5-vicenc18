# Solucio t03 FTP

![ftp portada](img/ftp.png)

## 1. instalacio del servei
``` bash
sudo apt install vsdtpd
```

![install ftp](img/installftp.png)

## 2 Fer una copia del archiu original
``` bash
cp /etc/vsftpd.conf /etc/vsftpd.bak
```
![](img/cpftp.png)

## 3 Archiu de configuracio
Habilitem la opcio anonymous_enable (yes) i reyniciem el servei

![yes](img/yes.png)

![restart](img/restart.png)

## 4. FTP Anonim
Comprovar que la carpeta "/srv/ftp" s'ha creat, i quins permisos te
Per punlicar harxius, ser descargats, cal copiarlos en acesta carpeta òbiament es pot crar una estructura de carpeta dins.
``` bash
tree  /rsv/
```
![carpeta](img/carpeta.png)

## 5.conexio al client
### 1 Instalar el ftp en el client 

``` bash
sudo apt install vsdtpd
```
![install ftp](img/installftp.png)

ens conectem emb els usuarirs que volem

``` bash
sudo apt ftp 192.168.56.101
```
![anonymous](img/anonymous.png)

## 6 ftp autinticat
Configurem la via de l'accés FTP, dels usuaris, I auran de acedir amb les seves cradencials 


![autenticat](img/autenticat.png)

![prova1](img/prova1.png)

## 7 engavinat dels usuaris

Serveix perque els usuaris locals no puguin sortir de la seva carpeta en connectar-se pel ftp

![local user](img/localuser.png)

![/etc](img/etc.png)

## 8 Aspectes de seguretat
Aquets servidor FTP continua utilitza transmissions insegures.

Amb cualsavol analitzador de transit podem capturar els datagrames

![wireshark](img/t03wireshark.png)

## 9 FTP segur
L’FTP segur s’aconsegueix utilitzant TLS (FTPS) per evitar problemes de seguretat.
Per a l’ús a Internet és recomanable un certificat signat per una autoritat certificadora (CA), tot i que per a proves es pot fer servir un certificat autosignat del servidor.
Existeixen dos modes de FTPS:

Implícit (obsolet), que utilitza habitualment el port 990.

Explícit, que utilitza el port 21 i inicia TLS un cop establerta la connexió.

Quan s’instal·la un servei que utilitza TLS, el sistema operatiu sovint genera automàticament unes claus autosignades (anomenades “snake‑oil”), que només serveixen per a proves i no són segures per a producció.

També indica que s’ha de comprovar si existeix la clau privada del certificat, que habitualment es troba al directori:
``` bash
/etc/ssl/private
```

![](img/t03v12.png)

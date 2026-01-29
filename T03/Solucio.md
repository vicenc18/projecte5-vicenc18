# Solucio t03 FTP

![ftp portada](img/ftp.png)

## 1. instalacio del servei
``` bash
sudo apt install vsdtpd
```

![install ftp](img/installftp.png)

## 2 Fer una copia del archiu original

Aquest comandament crea una còpia de seguretat del fitxer de configuració original de *vsftpd*.  
Això permet restaurar la configuració anterior en cas que apareguin errors després de fer canvis.

``` bash
cp /etc/vsftpd.conf /etc/vsftpd.bak
```
![](img/cpftp.png)

## 3 Archiu de configuracio

Habilitem l’opció `anonymous_enable=yes` dins del fitxer de configuració de **vsftpd** per permetre l'accés anònim al servidor FTP.  
Un cop modificat el fitxer, reiniciem el servei perquè els canvis tinguin efecte.

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

Configurem la via d'accés FTP dels usuaris, que hauran d’accedir amb les seves pròpies credencials per iniciar sessió al servei.

![autenticat](img/autenticat.png)

![prova1](img/prova1.png)

## 7 engavinat dels usuaris


Serveix perquè els usuaris locals no puguin sortir de la seva carpeta quan es connecten pel servei FTP, mantenint-los confinats dins del seu directori personal.

![local user](img/localuser.png)

![/etc](img/etc.png)

## 8 Aspectes de seguretat

uest servidor FTP continua utilitzant transmissions insegures.  
Amb qualsevol analitzador de trànsit és possible capturar els datagrames que es transmeten per la xarxa.

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

Editem el archiu de configuracio " /etc/vsftpd.conf" i afegim les seguents lines de codi

![](img/t03v13.png)

Es comprova com no es permet una connexió ftp no segura:

![](img/t03v14.png)

## 10 Hacemptacio del certificat
La comanda FTP de PowerShell no admet connexions TLS (Microsoft aposta per sftp com alternativa).
• Opcions:
  Fer un script PowerShell que usi la funció de .NET FtpWebRequest.
  Usar un client extern com Filezilla o WinSCP. Si no hi ha cap instal·lat, es pot fer servir una versió portable.
## 10.1 comproba la conexio

![](img/t03v15.png)

login..

![](img/t03v16.png)

# Solucio sftp

## 1 Maquines

Utilitzarem las maquinnes de l' anterior activitat
- ubuntu server 
- zorin OS (client)

## 2 que es? 

- És un protocol de transferència de fitxers que es basa en el protocol SSH que serveix per fer connexions de terminal remot de forma segura.

- És un protocol que ha guanya força popularitat per la transferència d’arxius.

- Utilitza el port 22 del servidor (propi del protocol SSH) per realitzar tota la comunicació.



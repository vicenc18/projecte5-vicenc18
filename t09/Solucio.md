# t09 Vulnerabilitats

![](img/vulnerabilidad.png)

## 1 Crear las maquinas vulnerables 

Com a maquina vulnerable farem servir metasplitable, i com maquina escaner farem servir Openvas

![](img/t09v2.png)

![](img/t09v11%20(2).png)

## 2 Configuració de las maquinas 

Metasploit la deixem tal com esta i OpnesVas afeguim un HOS ONLY

![](img/t09v5.png)

## ips de las maquines 

Lo primer sera  hacdeir a metasplit amb msfadmin/msfadmin
i fer un, ip a. 

Molt important!!, ens quedem amb la ip

![](img/t09v3.png)

![](img/t09v4.png)

Hara configurarem OpenVas entrant a la maquina i configurarle, entrem amb admin/admin.

![](img/t09v6.png)

Quan estem dintre haurem de afegir un usuari (usuari/usuari).

![](img/t09v7.png)

Despues hem de accedir a la configuració de networks i activar el ipV4. 

![](img/t09v8.png)

![](img/t09v9.png)

Molt importrant quedarnos amb la ip. 

## 4 Scan

Lo primer sera accedir via web a Openvas amb la ip de la maquina anterior. 

Entrarem amb el usuari que hem afegit avans

![](img/t09v10.png)

Quan estem dintre Veurem aquest menu 

![](img/t09v11.png)

Haurem de entrar  a l' apartat d'anfritions en Actius.

![](img/t09v13.png)

Alla Afegim un nou amfritio, on haurem deposar un nom y la ip del metasplitable uqe ens hem guardat avans.

![](img/t09v14.png)

Hara em de fer el obejtiu jo li posare linux vulnerable 4, important que poser dels recursos del ambritio,

![](img/t09v15.png)

Tmabe em de afegir un fitxer ssh, es inportant afegir una contraseña i marcar los dues opcions com a NO.

![](img/t09v16.png)

![](img/t09v18.png)

Hara crehem una tasca nova, jo li poso el nom del afritio (linux vulnerable 4).

A qui haurem de marcar com a obextiu el amritio de avasns

![](img/t09v19.png)
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

Quan tinguem la tasca feta la iniciem, pot tardar bastant de temps 


![](img/t09v20.png)

![](img/t09v21.png)

![](img/t09v12.png)

## 5 Informa 
L’escaneig del sistema 10.0.2.10 ha detectat vulnerabilitats crítiques que posen en risc alt la seguretat. S’han identificat serveis insegurs en execució, una possible backdoor (Ingreslock), vulnerabilitats d’execució remota de comandes, i un sistema operatiu fora de suport (EOL). El servidor també presenta diversos ports crítics oberts, incrementant l’exposició.
En conjunt, el risc és molt elevat i es recomana actuar de manera immediata: tancar serveis i ports insegurs, actualitzar el sistema operatiu, aplicar pegats i comprovar si hi ha hagut compromís del sistema.


![](img/t09v22.png)

![](img/t09v23.png)

![](img/t09v24.png)

## 6 vulnerabilitats 

1. Possible Backdoor: Ingreslock (port 1524/tcp)
Indica la presència d’un servei associat habitualment a accessos il·legítims. Pot significar que el sistema hagi estat compromès o que un atacant hagi deixat una porta d’entrada.

2. TWiki < 4.2.4 – Execució remota de comandes
Una vulnerabilitat que permet a un atacant executar comandes al servidor de forma remota a través de la web, prenent control total del sistema.

3. Sistema Operatiu en Fi de Vida (EOL)
El sistema operatiu ja no rep actualitzacions de seguretat ni pegats. Qualsevol vulnerabilitat coneguda queda exposada i fàcilment explotable.
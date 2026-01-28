# T04 Windows server

![](img/windosserver.jpg)

## 1 Instalacio del servidor
Molt im portant selecionar l'opcio de eskip

![](img/t04v1.png)

### 1.2 selecionar la llengua , 
selcionarem idioma de instalacio ingles,
pro la altre opcio Spanish

![](img/t04v2.png)

### 1.3 Idioma del teclat
deixem Spanish per defcte

![](img/t04v3.png)

### 1.4 intala windows server
Instalem windows server

![](img/t04v4.png)

### 1.5 Seleciona la imtge
MOLT IMPORTANT, selecionar la imatge amb entorn gràfic,
i haceptem les lisencies

![](img/t04v5.png)

### 1.6 Selcionar el lloc de instalacio
Selecionar el disc on voleu instalar Windows server

![](img/t04v6.png)

![](img/t04v7.png)

## final de la instalacio
Domes cal esperar a que es completi la instalacio

![](img/t04v8.png)

## 2 configuracio del servidor
### 2.1 Contrasenya dal administrador

Afeigim una contrasenya al nostra usuari de adiminstrador, A de ser complexa 

![](img/t04v9.png)

### 2.2 canviar el nom 
Es important cambiar el nom del equip per mes eficiencia

![](img/t04v10.png)

Li donem ha change

![](img/t04v11.png)

![](img/t04v12.png)

### 2.3 Configuracio de xarxa
El controlador de domini s' apuntar a ell mateix, 
utlitzarem la ip (127.0.0.1)

![](img/t04v13.png)

![](img/t04v14.png)

### 2.4 Intalacio del Rol Domine service
Lo primer que ferem es entrar a la part de Manager, I entrar hon diu add Roles and features

![](img/t04v15.png)

Segint d'l apartatde installation Type

![](img/t04v16.png)

Next..

![](img/t04v17.png)

Permet Insta-lar roles de forma centrelitzada als diferents servidors del domini. 

Next...

![](img/t04v19.png)

Next...

![](img/t04v20.png)

Confirmation...

![](img/t04v21.png)

INSTALL..

![](IMG/T04V22.png)

## 2.5 Promoció a domain controller

![](img/t04v23.png)

Entrem on diu Promote this server to a domain controller

![](img/t04v24.png)

I selecionem el tipus de instalacio que volem fer,
Ens pregunta si volem afegir a undomini que ja existeix,

![](img/t0425.png)

Next...

El nivell funcional de bosc i domini 

![](img/P@ssword.png)

next...

Com utilitza DNS i no detecta cap operatiu que contingui el domini triat, ens avisa i procedirà a instal·lar aquest rol al DC. Cliquem directament a Next

![](img/t04v26.png)

next...

Per compatibilitat amb sistemes que encara usen NetBIOS (Samba3, XP en grup de treball...) assigna automàticament un nom NetBIOS al domini.

![](img/t04v27.png)

next....

![](img/t04v28.png)

next..

Ens mostra un resum de les configuracions triades i dóna l’opció de crear un script PowerShell amb elles. Això és molt útil per replicar configuracions.

![](img/T04V29.png)

![](img/t04v30.png)

Instala..

![](img/t04v32.png)

Un cop acabada la instal·lació, la màquina s’ha de reiniciar i ens demanarà loguejar-nos com Administrator del domini

![](img/t04v33.png)

![](img/t04v34.png)

## 2.6 Zona horaria 

 Cal ajustar la zona horària perquè per defecte posa horari Costa Oest d’Estats Units.
 Un cop fet això, ajusteau l’hora correcta.


![](img/t04v35.png)


![](img/t04v36.png)

## 2.7 Configuracio dns 

l nostre controlador de domini fa de servidor DNS, per tant, pot fer consultes directes a Internet.
Per millorar velocitat i reduir quantitat de consultes, configurarem un reenviador per totes les adreces de Internet.

![](img/t04v37.png)

![](img/t04v38.png)


![](img/t04v39.png)

## 2.8 Eines de gesto
Per gestionar el nostre servidor Windows Server disposem de diverses opcions:

Server Manager

Windows Admin Center

PowerShell

### Server Manager

Pantalla de gestió central, permet visualitzar mètriques, accedir a les eines.
En cas de tenir diversos servidors dins el domini, es poden administrar directament des d’una consola de Server Manager única.
 És l’eina amb la que treballarem nosaltres habitualment.

 ![](img/t04v34.png)

 ### Windows Admin Center
Nova eina de Microsoft per gestionar elements del Directori Actiu des d’un navegador.
Es pot utilitzar tant des del servidor com des d’un client.

![](img/t04v40.png)

 Abans de res, cal baixar-lo a l’equip des del qual vulguis administrar.
Es tracta d’un paquet msi que s’haurà d’instal·lar i després s’executarà en el navegador.

### powershell
Totes les accions relatives tant al servidor com a la gestió del Directori Actiu es poden fer mitjançant cmd-lets de PowerShell.
En un client es pot instal·lar el mòdul de PowerShell per Active Directory per fer la gestió remota.
El principal avantatge es que permet automatitzar tasques i gestions mitjançant scripts.”
Si quieres que siga, que compile todo en un solo documento o que lo traduzca, ¡te lo preparo encantado!
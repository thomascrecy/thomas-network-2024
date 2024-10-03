# TP1 : Maîtrise réseau du votre poste

## I. Basics

### ☀️ Carte réseau WiFi
```
Carte réseau sans fil Wi-Fi :

Adresse physique . . . . . . . . . . . : 40-1A-58-4B-44-84
Adresse IPv4. . . . . . . . . . . . . .: 10.33.73.82(préféré)
Masque de sous-réseau. . . . . . . . . : 255.255.240.0
CIDR : /20
```
### ☀️ Déso pas déso
```
Adresse de réseau : 10.33.64.0
Adresse de broadcast : 10.33.79.255
Nombre d'adresses IP disponibles : 4094
```
### ☀️ Hostname
```
PS C:\Users\crecy> hostname
Thomas
```
### ☀️ Passerelle du réseau
```
Passerelle par défaut. . . . . . . . . : 10.33.79.254
10.33.79.254          7c-5a-1c-d3-d8-76     dynamique
```
### ☀️ Serveur DHCP et DNS
```
Serveur DHCP . . . . . . . . . . . . . : 10.33.79.254
Serveurs DNS. . .  . . . . . . . . . . : 8.8.8.8
```
### ☀️ Table de routage
```
IPv4 Table de routage
===========================================================================
Itinéraires actifs :
Destination réseau    Masque réseau  Adr. passerelle   Adr. interface Métrique
        0.0.0.0          0.0.0.0     10.33.79.254      10.33.73.82     30
```

## II. Go further

### ☀️ Hosts ?
```
PS C:\Users\crecy> ping b2.hello.vous

Envoi d’une requête 'ping' sur b2.hello.vous [1.1.1.1] avec 32 octets de données :
Réponse de 1.1.1.1 : octets=32 temps=16 ms TTL=55
Réponse de 1.1.1.1 : octets=32 temps=50 ms TTL=55
Réponse de 1.1.1.1 : octets=32 temps=16 ms TTL=55
Réponse de 1.1.1.1 : octets=32 temps=17 ms TTL=55

Statistiques Ping pour 1.1.1.1:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 16ms, Maximum = 50ms, Moyenne = 24ms
```
### ☀️ Go mater une vidéo youtube et déterminer, pendant qu'elle tourne...
```
TCP    10.33.73.82:52912      172.65.251.78:443      ESTABLISHED
[chrome.exe]

IP : 172.65.251.78
Port serveur : 443
Port local : 52912
```
### ☀️ Requêtes DNS
```
PS C:\Users\crecy> nslookup www.thinkerview.com
Serveur :   dns.google
Address:  8.8.8.8

Réponse ne faisant pas autorité :
Nom :    www.thinkerview.com
Addresses:  2a06:98c1:3120::7
        2a06:98c1:3121::7
        188.114.96.7
        188.114.97.7

PS C:\Users\crecy> nslookup 143.90.88.12
Serveur :   dns.google
Address:  8.8.8.8

Nom :    EAOcf-140p12.ppp15.odn.ne.jp
Address:  143.90.88.12
```
### ☀️ Hop hop hop
```
PS C:\Users\crecy> tracert www.ynov.com

Détermination de l’itinéraire vers www.ynov.com [104.26.10.233]
avec un maximum de 30 sauts :

1     4 ms     1 ms     1 ms  10.33.79.254
2     1 ms     2 ms     2 ms  145.117.7.195.rev.sfr.net [195.7.117.145]
3     1 ms     2 ms     1 ms  237.195.79.86.rev.sfr.net [86.79.195.237]
4     2 ms     2 ms     2 ms  196.224.65.86.rev.sfr.net [86.65.224.196]
5    11 ms    12 ms    12 ms  164.147.6.194.rev.sfr.net [194.6.147.164]
6     *        *        *     Délai d’attente de la demande dépassé.
7    16 ms    19 ms    29 ms  162.158.20.240
8    16 ms    16 ms    15 ms  104.26.10.233

Itinéraire déterminé.
```
### ☀️ IP publique
```
PS C:\Users\crecy> (Invoke-WebRequest -uri "http://ifconfig.me").Content
195.7.117.146
```
## III. Le requin

### ☀️ Capture ARP
```

```
### ☀️ Capture DNS
```

```
### ☀️ Capture TCP
```

```
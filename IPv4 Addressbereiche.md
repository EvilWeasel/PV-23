- IPv4-Addressen insgesamt = 2^32 -> ca. 4 Milliarden Addressen
- Mehr Geräte im Internet als IP-Addressen
- IP-Addressen sind notwendig für korrektes Traffik-Routing
	- IP-Addressen sind quasi wie PLZ, Hausnummer, Stadt und Land im Postbereich
- Was tun gegen Addressmangel?


## Subnetting und Private Addressbereiche

- Lokale IP-Addressen -> Routing nur im internen Netzwerk
	- Gewisse IP-Addressen nicht Routbar
	- Warum?
		- Nicht genügen Addressen für alle einzelnen Geräte
		- Deswegen bekommt jeder von seinem Provider nur eine IP für das gesamte Netzwerk
	- Aber wenn ein PC aus dem Internet meinem Computer im privaten Netzwerk ein Datenpaket schickt, woher weiß mein Router, an welchen Client das Paket muss?
- Antwort: NAT

## NAT

- Steht für "Network Address Translation"
- Beim Versenden von Nachrichten übersetzt der Router die private IP-Addresse des Clients in eine öffentliche IP-Addresse.
- Das Ziel kennt nur die öffentliche IP-Addresse
- Beim erhalt von Nachrichten wird die Öffentliche Ziel-Addresse vom Router in eine private Addresse des Clients umgewandelt.

## Addressbereiche / Klassen

Standard von 1996, `RFC 1918`. Heute nicht mehr Notwendig weil NAT jede interne IP-Addresse in die öffentliche IP-Addresse übersetzt, welche ihr vom ISP (Internet Service Provider) bekommt.

### Klasse A Netz

Bereich:    10.0.0.0        -   10.255.255.255  (10/8 prefix)

### Klasse B Netz

Bereich:     172.16.0.0      -   172.31.255.255  (172.16/12 prefix)

### Klasse C Netz

Bereich:      192.168.0.0     -   192.168.255.255 (192.168/16 prefix)



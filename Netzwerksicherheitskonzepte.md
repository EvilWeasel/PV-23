## VLANs

- Virtuelles Netzwerk
- Logisch getrennte LANs
- Zugriffsbeschränkung
	- Ein Angreifer, welcher auf eine Maschine in VLAN A Zugriff hat, kann so nicht einfach auf Maschinen in VLAN B zugreifen.
- Operieren auf OSI-Schicht 2
- Veringerung der Broadcast
- Dynamische oder Statische Zuweisung
	- Statisch Portbasiert -> eg. Port 1 und Port 2 bilden ein VLAN A
	- Dynamisch: -> Tagged VLANs -> IP + MAC-Addresse
		- Besser über IEEE 802.1q
- Verbindung von 2 Switches mit gleichen VLANs (Sharing der VLANs) über einen Trunk-Port
	- Ein Port für 2 VLANs

## Firewall

### Packet-Inspektion

- Layer 3 -> IP-Header
- Layer 4 -> TCP- und UDP Header

### Proxy-Firewall

- Auf Anwendungsebene -> Layer 7
- Überwacht gesamten Netzwerk-Traffik inklusive Inhalte
- Zugriffskontrolle auf unerwünschte Dienste

### Stateful Package Inspection

- Datenpakete werden immer einer aktiven "Session" zugeordnet

### Hybride Firewalls

- Die meisten Firewalls nutzen mehrere Varianten der vorherig genannten Typen

Als Referenz, nicht für AP1 relevant.
![[Pasted image 20240911113223.png]]


## Proxy

- Vermittlt einen Client in einem internen Netzwerk mit dem großen weiten Internet
- Anfragen, welche der Client stellt, werden vom Proxy weitergeleitet
	- Zielserver sieht den Client nicht, sondern den Proxy
- Unerwünschte Dienste oder Benutzer sperren
- Antworten auf Anfragen werden im Cache gespeichert -> Zukünftige Anfragen können aus vorheriger Antwort bedient werden
- Unterstützt die meisten Netzwerkprotokolle

### Reverse-Proxy

- Nicht so relevant für AP1
- Woher kommt die Bezeichnung:
	- Proxy => internes Netz -> öffentliches Netz (Internet)
	- Reverse => öffentliches Netz -> internes Netz

## VPN

- Übertragung über TCP oder UDP
- Mehrere VPN in Reihe geschalten können die Sicherheit zusätzlich erhöhen
- Verschiedene Protokolle den Verbindungsaufbau:
	- L2TP -> Layer Two Tunneling Protocol
		- Authentifizierung über Pre-Shared Key
	- OpenVPN
	- Wireguard
- Alle Protokolle können und sollten verschlüsselt sein - Verschiedene Implementationen per Protokoll
	- MS-CHAPv2
	- EAP
	- PAP -> brutal unsicher



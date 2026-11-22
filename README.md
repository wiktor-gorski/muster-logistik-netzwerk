
# Muster Logistik AG – Netzwerkprojekt

## Über das Projekt

Dieses Projekt zeigt die Planung und Konfiguration
eines kleinen Firmennetzwerks für ein fiktives
Logistikunternehmen.

Erstellt im Rahmen meiner Vorbereitung auf eine
Informatiklehre EFZ Plattformentwicklung.

## Netzwerkaufbau

Das Netzwerk besteht aus:

- 1 Cisco-Router (2911)
- 1 Cisco-Switch (2960)
- 1 Büro-PC
- 1 Lager-PC
- 1 Server

## Netzwerkkonzept

| VLAN | Bereich | Netzwerk |
|------|---------|----------|
| 10 | Büro | 192.168.10.0/24 |
| 20 | Lager | 192.168.20.0/24 |
| 30 | Server | 192.168.30.0/24 |

Verwendete Technologien:

- VLANs zur logischen Netzwerktrennung
- Router-on-a-Stick für Inter-VLAN-Routing
- DHCP für automatische IP-Adressvergabe
- Statische IP-Adresse für den Server
- Cisco-IOS-Konfigurationsbefehle

## Projektdateien

- `netzwerkplan.md` – Netzwerk- und IP-Plan
- `switch.txt` – Switch-Konfiguration
- `router.txt` – Router- und DHCP-Konfiguration
- `server.md` – Serverkonzept
- `netzwerktests.md` – Prüf- und Diagnosebefehle

## Verbindung zur Lagerverwaltung

Das Netzwerk ist für den Betrieb einer
Python-Lagerverwaltung vorgesehen.

Der geplante Server befindet sich im VLAN 30
und besitzt die IP-Adresse 192.168.30.10.

## Projektstatus

Netzwerk geplant und Cisco-Konfigurationen
als Vorlagen erstellt.

Die Konfigurationen wurden noch nicht in
einer Netzwerksimulation ausgeführt oder getestet.

## Ziel

Mit diesem Projekt möchte ich meine Kenntnisse
in Netzwerktechnik, IP-Adressierung, VLANs,
Routing und DHCP vertiefen.

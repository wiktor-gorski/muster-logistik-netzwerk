
# Netzwerkprüfung – Muster Logistik AG

## 1. VLANs kontrollieren

Befehl auf dem Switch:

show vlan brief

Zeigt, welche VLANs existieren und
welche Switch-Ports ihnen zugeordnet sind.

Erwartet:
- Fa0/1: VLAN 10 (Buero)
- Fa0/2: VLAN 20 (Lager)
- Fa0/3: VLAN 30 (Server)

## 2. Router-Schnittstellen prüfen

Befehl auf dem Router:

show ip interface brief

Zeigt die IP-Adressen und den Status
der Router-Schnittstellen.

Erwartet:
- Gi0/0.10: 192.168.10.1
- Gi0/0.20: 192.168.20.1
- Gi0/0.30: 192.168.30.1

## 3. DHCP überprüfen

Befehl auf dem Router:

show ip dhcp binding

Zeigt die automatisch vergebenen IP-Adressen.

Erwartet:
- Büro-PC: 192.168.10.x
- Lager-PC: 192.168.20.x

## 4. Verbindung zum Server testen

Befehl auf einem PC:

ping 192.168.30.10

Prüft, ob der Server erreichbar ist.

Erwartet:
Antwort vom Server, sofern alle Geräte
korrekt verbunden und konfiguriert sind.

## 5. Fehler suchen

Wenn ein Ping nicht funktioniert:

1. IP-Adresse und Subnetzmaske prüfen.
2. Standardgateway kontrollieren.
3. VLAN-Zuordnung am Switch prüfen.
4. Trunk-Verbindung kontrollieren.
5. Router-Schnittstellen überprüfen.

## Teststatus

Noch nicht durchgeführt.

Die Konfigurationen wurden bisher
nur in VS Code vorbereitet.

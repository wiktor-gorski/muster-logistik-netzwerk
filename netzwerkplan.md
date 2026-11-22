
# Muster Logistik AG – Netzwerkplan

## Netzwerkaufbau

Router R1
    |
Switch SW1
    |
    +-- Büro-PC    (VLAN 10)
    |
    +-- Lager-PC   (VLAN 20)
    |
    +-- Server     (VLAN 30)

## IP-Adressplan

| Bereich | VLAN | Netzwerk | Gateway |
|---|---|---|---|
| Büro | 10 | 192.168.10.0/24 | 192.168.10.1 |
| Lager | 20 | 192.168.20.0/24 | 192.168.20.1 |
| Server | 30 | 192.168.30.0/24 | 192.168.30.1 |

Server-IP: 192.168.30.10

## Ziel

Die Abteilungen werden durch VLANs logisch getrennt.
Der Router ermöglicht die Kommunikation zwischen den VLANs.
Die Büro- und Lager-PCs erhalten ihre IP-Adressen per DHCP.
Der Server verwendet eine feste IP-Adresse.


## Netzwerkdiagramm

```mermaid
flowchart TD
    R1["Router R1<br/>Cisco 2911"]
    SW1["Switch SW1<br/>Cisco 2960"]

    PC1["Büro-PC<br/>VLAN 10"]
    PC2["Lager-PC<br/>VLAN 20"]
    SRV["Server<br/>VLAN 30<br/>192.168.30.10"]

    R1 ---|Trunk| SW1
    SW1 --- PC1
    SW1 --- PC2
    SW1 --- SRV
```

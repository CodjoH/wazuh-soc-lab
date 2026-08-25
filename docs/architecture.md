## Architecture 

Ce projet est un laboratoire virtualisé de Security Operations Center (SOC) basé sur Wazuh, Shuffle, Suricata et pfSense.

il comprend un Wazuh Manager et deux endpoints supervisés :

Wazuh Manager — Debian
Client1-W — Windows
Client2-L — Linux

## Architecture réseau

Les machines virtuelles communiquent via un réseau NAT Network dédié de VirtualBox.

## Communication Wazuh

Le Wazuh Manager expose les services suivants :

TCP/UDP 1514 — communication avec les agents Wazuh
TCP 1515 — enrôlement des agents
TCP 55000 — API Wazuh
## Validation de la connectivité

La connectivité entre le Wazuh Manager et l'endpoint Linux a été validée avec succès.

La connectivité TCP vers les ports utilisés par Wazuh a également été vérifiée depuis les endpoints Linux et Windows.

## Configuration réseau VirtualBox

Le laboratoire utilise deux interfaces réseau sur les machines virtuelles :

NAT — accès à Internet
NAT Network (NatNetwork) — communication entre les machines du SOC Lab

Cette séparation permet aux endpoints de communiquer avec le Wazuh Manager tout en conservant un accès à Internet pour les mises à jour et l'installation des différents composants.
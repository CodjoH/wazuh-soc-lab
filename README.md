
<h1 align="center">🛡️ Mise en place d'un SOC open source</h1>

## 📌 Introduction

Ce projet porte sur la conception et le déploiement d’un **Security Operations Center (SOC)** basé exclusivement sur des solutions open source : **Wazuh, Shuffle, Suricata et pfSense**.

L’objectif est de mettre en place une infrastructure permettant de **superviser, détecter et répondre aux incidents de sécurité**.

## 🎯 Objectifs


- 📊 Centraliser et analyser les logs de sécurité.
- 🔍 Détecter les menaces sur les endpoints et le réseau.
- ⚡ Automatiser la réponse aux incidents.
- 🛡️ Renforcer la sécurité périmétrique avec un firewall et un IDS/IPS.


## 🏗️ Infrastructure

- **SIEM — Wazuh**  
  Collecte, analyse et corrélation des logs.

- **SOAR — Shuffle**  
  Automatisation de la réponse aux incidents.

- **Firewall / IDS/IPS — pfSense + Suricata**  
  Protection et surveillance du réseau.

- **Endpoints — Windows / Linux**  
  Sources des événements de sécurité.

- **Hyperviseur — VirtualBox**  
  Virtualisation de l’infrastructure.

## 🔗 Architecture
![Architecture](docs/assets/architecture.png)


##  🔍 Visualisation & Analyse

## 🔹Agents Wazuh
![Agents Wazuh](docs/assets/Endpoints.jpg)

## 🔹Détection de vulnérabilités dans Wazuh
![Détection de vulnérabilités](docs/assets/Vulns_detection.png)

## 🔹Tableau de bord des menaces
![Threat Hunting](docs/assets/Threat%20Hunting.png)


## 🔹Logs IDS/IPS via pfSense + Suricata
![Logs IDS/IPS](docs/assets/pfSense.jpg)


## 🔹Playbooks - Scénario d'automatisation dans Shuffle
![Playbooks Shuffle](docs/assets/Playbooks_Suffle%28SOAR%29.png)

## 🔹Suivi des incidents - backlog Wazuh

![Security Events](docs/assets/Security-events.png)


## 🛠️ Implémentation

### 🔹 Étapes clés

📌 Définition du périmètre et choix des outils<br>
📌 Déploiement de l’infrastructure sous VirtualBox<br>
📌 Installation et configuration de pfSense, Wazuh, Shuffle et Suricata<br>
📌 Déploiement des endpoints Windows Server 2022 et Debian<br>
📌 Installation et configuration des agents Wazuh<br>
📌 Mise en place des règles de détection et mapping MITRE ATT&CK<br>
📌 Création de playbooks Shuffle pour automatiser la réponse aux incidents<br>
📌 Simulation de scénarios d’attaque et génération de logs<br>
📌 Mise en place des actions de remédiation et documentation

### 📈 Résultats

✔️ Détection et centralisation des événements de sécurité via Wazuh<br>
✔️ Automatisation de la réponse aux incidents via Shuffle<br>
✔️ Renforcement de la sécurité réseau via Suricata/pfSense<br>
✔️ Corrélation des événements et classification selon MITRE ATT&CK<br>
✔️ Architecture modulaire et évolutive


## 🔗 Documentation

- 📖 [Wazuh](https://documentation.wazuh.com/)
- 📖 [Shuffle](https://shuffler.io/docs)
- 📖 [Suricata](https://docs.suricata.io/)
- 📖 [pfSense](https://docs.netgate.com/pfsense/)



<p align="center">
  🛡️ <strong>Hubert Codjo</strong><br>
  <sub>Cybersecurity Engineer • SOC Analyst • Blue Team</sub><br><br>
  📧 <a href="mailto:houet.hubert@gmail.com"><strong>Click to contact me</strong></a><br><br>
  ─ · ─<br><br>
</p>



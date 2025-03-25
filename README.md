# infranerd-homelab-ci   COMMING SOON

# 🐳 Self-Hosted CI Boost – Eigene Docker Registry & GitHub Actions Runner fürs Homelab

## 🚀 Projektüberblick

Dieses Projekt bringt zwei wichtige CI/CD-Komponenten direkt in dein **Homelab**:

- Eine **eigene Docker Registry**
- Einen **selbstgehosteten GitHub Actions Runner**

Damit umgehen wir typische Limitierungen öffentlicher Dienste – wie **Rate Limits**, **Verfügbarkeiten** und **begrenzte Build-Kapazitäten** – und schaffen eine robuste, lokal kontrollierte Umgebung für Continuous Integration & Deployment.

## 🧭 Ziel des Projekts

🔧 **Weniger Abhängigkeit von Cloud-Providern**  
💡 **Mehr Kontrolle über eigene Build- & Release-Pipelines**  
🚀 **Schnellere, zuverlässigere Deployments im Homelab**  
🧰 **Erweiterung meines DevOps-Stacks um weitere Self-Hosted-Komponenten**

## 🧱 Projektbestandteile

| Komponente         | Beschreibung                                                                 |
|--------------------|------------------------------------------------------------------------------|
| 🐳 Docker Registry  | Lokaler Image-Store mit optionaler Authentifizierung und TLS                |
| ⚙️ GitHub Runner    | Eigener CI-Runner für GitHub Actions – persistent, selbstverwaltet          |
| 🔐 Wildcard-Zert.   | Unterstützung für bestehende Zertifikate (*.infranerd.de oder Let's Encrypt)|
| 📦 Image Caching    | Für häufig genutzte Base-Images & Layer                                     |
| 📈 Monitoring       | Optional via Prometheus, Grafana, Loki etc.                                 |

## 📦 Homelab Fokus

Dieses Projekt ist speziell für Homelabs mit folgenden Eigenschaften geeignet:

- 🖥️ Self-hosted Server (Proxmox, bare metal, VM oder Raspberry Pi)
- 🌐 Lokale Netzwerke mit statischer IP oder DNS via z. B. `*.infranerd.de`
- 🔐 Vorhandenes TLS-Zertifikat (z. B. Wildcard von IONOS oder Let's Encrypt)
- 🧱 Infrastruktur mit Docker, K3s oder MicroK8s

## 📋 Warum dieses Projekt?

Öffentliche Ressourcen sind gut – bis sie limitiert sind. Aus meiner täglichen Arbeit als DevOps Engineer weiß ich:

- Docker Hub blockiert bei zu vielen Requests
- GitHub Actions Runner stehen manchmal einfach nicht bereit
- Builds dauern, weil Caching fehlt oder Images neu gezogen werden müssen

Mit diesem Projekt schaffe ich eine Umgebung, die **verlässlich, schnell und unabhängig** ist – genau das, was ein modernes Homelab braucht.

## ✍️ Motivation & Wissenstransfer

Ich möchte damit nicht nur mein eigenes Setup verbessern, sondern auch mein Wissen im Bereich:

- DevOps & Automatisierung
- CI/CD-Pipelines
- Container-Infrastruktur
- Homelab-Architektur

öffentlich teilen. Dieses Projekt ist ein weiterer Baustein meiner **"Infrastructure as Portfolio"**-Philosophie.

## 📅 Roadmap

- [x] Docker Registry lokal mit Persistenz & Port-Forwarding
- [x] GitHub Runner als Docker Container mit Auto-Registration
- [ ] TLS-Support via Wildcard oder Let's Encrypt
- [ ] Registry UI (z. B. [docker-registry-ui](https://github.com/Joxit/docker-registry-ui))
- [ ] Monitoring mit Prometheus/Grafana
- [ ] Optional: K3s-native Version via Helm Chart

## 📁 Struktur (voraussichtlich)

```bash
📁 docker-registry-github-runner-homelab/
├── docker-compose.yml
├── registry/
│   └── config.yml
├── runner/
│   └── entrypoint.sh
├── certs/
│   └── *.infranerd.de.crt
└── README.md

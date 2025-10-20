# Scanner de Ports IP

Un scanner de ports simple et efficace en Python pour analyser les ports ouverts sur une adresse IP donnée.

## Fonctionnalités

- Scan de ports individuels ou par plages
- Identification automatique des services (HTTP, SSH, MySQL, etc.)
- Aucune dépendance externe requise

## Installation

### Linux/macOS

```bash
# 1. Cloner le projet
git clone https://github.com/TISEPSE/Scanner-IP-PORTS.git
cd Scanner-IP-PORTS

# 2. Lancer l'installation
chmod +x install.sh
./install.sh

# 3. Recharger votre shell
source ~/.bashrc  # ou source ~/.zshrc pour zsh

# 4. Tester
portscan -i 127.0.0.1 -p 80
```

### Windows

```powershell
# 1. Cloner le projet
git clone https://github.com/TISEPSE/Scanner-IP-PORTS.git
cd Scanner-IP-PORTS

# 2. Utiliser directement
python scan.py -i 127.0.0.1 -p 80
```

## Utilisation

```bash
# Scanner un port spécifique
portscan -i 192.168.1.1 -p 80

# Scanner plusieurs ports
portscan -i 192.168.1.1 -p 22 80 443

# Scanner une plage de ports
portscan -i 192.168.1.1 -r 20-100

# Combiner ports et plage
portscan -i 192.168.1.1 -p 22 443 -r 8000-8080
```

### Sans installation (avec Python directement)

```bash
python3 scan.py -i 192.168.1.1 -p 80
python3 scan.py -i 192.168.1.1 -r 1-1000
```

## Options

| Option | Description | Exemple |
|--------|-------------|---------|
| `-i, --ip` | Adresse IP cible | `-i 192.168.1.1` |
| `-p, --port` | Port(s) spécifique(s) | `-p 80 443 22` |
| `-r, --range` | Plage de ports | `-r 20-100` |

## Avertissement

Utilisation légale uniquement. Cet outil est destiné à des fins éducatives et de test sur vos propres systèmes ou avec autorisation explicite.

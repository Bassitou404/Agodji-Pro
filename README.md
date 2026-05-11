```
      █████╗  ██████╗  ██████╗ ██████╗      ██╗██╗███████╗
     ██╔══██╗██╔════╝ ██╔═══██╗██╔══██╗     ██║██║██╔════╝
     ███████║██║  ███╗██║   ██║██║  ██║     ██║██║█████╗
     ██╔══██║██║   ██║██║   ██║██║  ██║██   ██║██║██╔══╝
     ██║  ██║╚██████╔╝╚██████╔╝██████╔╝╚█████╔╝██║███████╗
     ╚═╝  ╚═╝ ╚═════╝  ╚═════╝ ╚═════╝  ╚════╝ ╚═╝╚══════╝
```

</div>
---

---
Fonctionnalités

---
Installation
```bash
# Cloner le repo
git clone https://github.com/T3RRIFI3R/agodjie
cd agodjie

# Dépendances (toutes optionnelles sauf stdlib)
pip3 install -r requirements.txt

# Rendre exécutable
chmod +x agodjie.py
```
Dépendances optionnelles :
```bash
pip3 install boto3              # Scan AWS SDK
pip3 install azure-identity     # Azure SDK
pip3 install google-cloud       # GCP SDK
```
---
Utilisation
```bash
# Scan complet (tous modules)
python3 agodjie.py <target>

# Exemples
python3 agodjie.py 10.10.110.50
python3 agodjie.py company.com
python3 agodjie.py 192.168.1.0/24

# Modules spécifiques
python3 agodjie.py 10.10.110.50 -m ports ssl headers
python3 agodjie.py company.com  -m dns subdomains buckets

# Options avancées
python3 agodjie.py company.com \
  -m all \
  -t 200 \                        # 200 threads
  --timeout 0.8 \                  # timeout 0.8s
  --region eu-west-1 \             # région AWS
  --bucket-name company \          # nom base buckets
  -o ./resultats                   # dossier de sortie
```
---
Options
```
usage: agodjie [-h] [-m MODULES [MODULES ...]] [-o OUTPUT] [-t THREADS]
               [--timeout TIMEOUT] [--region REGION] [--bucket-name NAME]
               [--port PORT] [-q] [--no-banner]
               target

Arguments:
  target                  IP, CIDR, ou domaine cible

Options:
  -m, --modules           Modules : ports metadata ssl headers dns subdomains buckets all
  -o, --output            Répertoire de sortie (défaut: ./agodjie_output)
  -t, --threads           Nombre de threads (défaut: 150)
  --timeout               Timeout socket en secondes (défaut: 1.0)
  --region                Région AWS pour buckets (défaut: us-east-1)
  --bucket-name           Nom de base pour les permutations de buckets
  --port                  Port pour SSL/HTTP (défaut: 443)
  -q, --quiet             Mode silencieux
  --no-banner             Masquer le banner ASCII
```
---
Ports Cloud Couverts
Agodjié cible 60+ ports spécifiquement liés aux infrastructures cloud :
```
Kubernetes  : 6443 · 8001 · 10250 · 10255 · 2379 · 2380
Docker      : 2375 · 2376 · 4243 · 5000
Monitoring  : 9090 (Prometheus) · 3000 (Grafana) · 5601 (Kibana) · 9200 (Elasticsearch)
Databases   : 3306 · 5432 · 27017 · 6379 · 7000 · 11211 · 1433
Messaging   : 9092 (Kafka) · 2181 (ZooKeeper)
AD/IAM      : 88 · 389 · 636 · 464
Network     : 179 (BGP) · 500 · 4500 (IPSec) · 4789 (VXLAN)
CI/CD       : 8080 (Jenkins) · 9000 (SonarQube) · 8888 (Jupyter)
```
---
Outputs
Chaque scan génère dans le dossier de sortie :
```
agodjie_output/
├── agodjie_report_20240315_143022.json    # Rapport complet JSON
└── agodjie_report_20240315_143022.md      # Rapport Markdown lisible
```
---
Avertissement légal
> **Agodjié est un outil de sécurité offensif destiné exclusivement à des fins éducatives, de pentest légalement autorisé, de bug bounty, et de recherche en sécurité.**
>
> L'utilisation de cet outil contre des systèmes sans autorisation explicite est **illégale** et contraire à l'éthique. L'auteur décline toute responsabilité en cas d'utilisation malveillante.
>
> **Utilisez uniquement sur des systèmes dont vous êtes propriétaire ou pour lesquels vous disposez d'une autorisation écrite.**
---
Auteur
@T3RRIFI3R — GitHub · Twitter/X
---
<div align="center">
<sub>Agodjié — Du Dahomey au Cloud, la précision reste la même.</sub>
</div>



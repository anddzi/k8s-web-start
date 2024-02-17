# Kubernetes und Minikube README

## Einführung

Diese README-Dokumentation bietet eine umfassende Anleitung zur Verwendung von Kubernetes, Minikube und Docker, einschließlich einer Vielzahl von Befehlen und Konzepten für die Verwaltung von containerbasierten Anwendungen.

## Minikube

Minikube ist ein Tool zur Erstellung und Verwaltung eines lokalen Kubernetes-Clusters.

### Grundlegende Minikube-Befehle

- **`minikube start`**: Startet den Minikube-Cluster.
- **`minikube stop`**: Stoppt den Minikube-Cluster.
- **`minikube status`**: Zeigt den Status des Minikube-Clusters.
- **`minikube start --driver=hyperv`**: Startet Minikube mit Hyper-V als Treiber.

### Erweiterte Minikube-Befehle

- **`minikube ip`**: Zeigt die IP-Adresse des Minikube-Clusters.
- **`minikube ssh`**: Ermöglicht SSH-Zugriff auf den Minikube-Cluster.
- **`minikube tunnel`**: Ermöglicht LoadBalancer-Services, auf externe Anfragen zu reagieren.

## Kubernetes Command-Line Tool: kubectl

`kubectl` ist ein mächtiges Werkzeug zur Interaktion mit Kubernetes-Clustern.

### Grundlegende kubectl-Befehle

- **`kubectl version`**: Zeigt die aktuelle Version von kubectl.
- **`kubectl get nodes`**: Listet alle Knoten des Clusters auf.
- **`kubectl apply -f [file.yaml]`**: Wendet eine Konfiguration aus einer YAML-Datei an.
- **`kubectl delete [resource] [name]`**: Löscht eine spezifizierte Ressource.

### Verwaltung von Deployments und Services

- **`kubectl create deployment [name] --image=[image]`**: Erstellt eine neue Deployment.
- **`kubectl expose deployment [name] --type=[type] --port=[port]`**: Exponiert eine Deployment als Service.
- **`kubectl set image deployment/[name] [container]=[new-image]`**: Aktualisiert das Image eines Containers in einer Deployment.
- **`kubectl rollout status deployment/[name]`**: Zeigt den Status der Aktualisierung einer Deployment.
- **`kubectl describe deployment/[name]`**: Zeigt detaillierte Informationen zu einer Deployment.

### Erweiterte Befehle

- **`kubectl get pods/svc/deploy`**: Listet Pods, Services oder Deployments auf.
- **`kubectl exec [pod-name] -- [command]`**: Führt einen Befehl in einem Pod aus.
- **`kubectl cluster-info`**: Zeigt Informationen zum Cluster.
- **`kubectl get namespaces`**: Listet alle Namensräume im Cluster auf.
- **`kubectl get --namespace=xxx`**: Listet Ressourcen in einem spezifischen Namespace auf.

### Alias-Einstellung

- **`alias k=kubectl`**: Setzt einen Alias `k` für den `kubectl`-Befehl.

## Docker

Docker ist eine wesentliche Komponente für das Arbeiten mit Containern und Kubernetes.

### Wichtige Docker-Befehle

- **`docker build . -t [username/imagename]:[tag]`**: Erstellt ein Docker-Image.
- **`docker push [username/imagename]`**: Lädt ein Docker-Image in ein Repository hoch.
- **`docker images`**: Listet alle lokalen Docker-Images auf.
- **`docker ps`**: Zeigt laufende Container an.
- **`docker ps -a`**: Zeigt alle Container an, auch die beendeten.

### Docker Compose

- **`docker-compose up`**: Startet die Services, die in `docker-compose.yml` definiert sind.
- **`docker-compose down`**: Stoppt und entfernt die durch `docker-compose up` gestarteten Container.

## Integration und Services

- **Minikube und Docker**: Minikube kann Docker als Container-Runtime verwenden.
- **Services in Kubernetes**: Beschreibung der Service-Typen wie ClusterIP, LoadBalancer und NodePort.
- **Docker Hub**: Anleitung zum Hochladen von Images auf Docker Hub.

## Abschluss

Diese Dokumentation bietet einen Einstieg in die Verwendung von Kubernetes, Minikube und Docker. Sie ist als Startpunkt gedacht und kann je nach Bedarf erweitert werden.

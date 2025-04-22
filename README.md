# Caddy Webserver Kubernetes Setup

Dieses Repository enthält eine einfache Kubernetes-Bereitstellung für den Caddy-Webserver. Der Fokus liegt auf minimaler Konfiguration und einfacher Bereitstellung.

## Struktur

```
kubernetes/
├── caddy-deployment.yaml   # Deployment-Konfiguration
├── caddy-service.yaml      # Service für ClusterIP
├── caddy-configmap.yaml    # ConfigMap mit der Caddyfile-Konfiguration
README.md                   # Diese Datei
.gitignore                  # Gitignore-Datei
```

## Schritte zur Nutzung

### 1. Voraussetzungen

- Kubernetes-Cluster (lokal oder cloudbasiert)
- `kubectl` lokal installiert und konfiguriert

### 2. Deployment

Wende die YAML-Dateien im Ordner `kubernetes/` an:

```bash
kubectl apply -f kubernetes/caddy-deployment.yaml
kubectl apply -f kubernetes/caddy-service.yaml
kubectl apply -f kubernetes/caddy-configmap.yaml
```

### 3. Zugriff auf den Webserver

Nach erfolgreicher Bereitstellung kannst du den Caddy-Webserver innerhalb des Clusters auf Port 80 erreichen. Für externen Zugriff kannst du entweder ein `NodePort`-Service oder ein Ingress verwenden.

### 4. Anpassung der Caddyfile

Die Datei `caddy-configmap.yaml` enthält die Konfiguration für den Caddy-Webserver. Du kannst sie anpassen, um weitere Funktionen wie Reverse Proxy, TLS, etc., hinzuzufügen.# caddy-webserver-kubernetes

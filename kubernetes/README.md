
Kommando | Beschreibung
-| - | - 
minikube start --cpus 2 --memory 2048 --disk-size 5GB | Cluster erzeugen
minikube kubectl -- get pods -A | kubectl aktualisieren
minikube delete | VM löschen
kubectl create deployment nginx –-image=nginx [--dry-run] [options] | Deployment (Pod und Replicaset) erzeugen
kubectl get deployment [NAME] | Deployment anzeigen
kubectl get pod [NAME] | Pod anzeigen
kubectl get replicaset [NAME] | Replicaset anzeigen
kubectl get secret | Secret anzeigen
kubectl scale --replicas=3 deployment/nginx | Deployment skalieren
kubectl edit deployment nginx | Konfiguration anzeigen
kubectl replace -f replicaset-app.yaml | Konfigurationsdatei einlesen und anwenden (z.B. Skalieren)
kubectl get pod -o wide | Pods mit mehr Details auflisten
kubectl describe pod mongo-56974b67f6-kml64 | Informationen zum Pod anzeigen
kubectl logs nginx-54f48578cf-22j86 | Log der Anwendung anzeigen
kubectl logs --tail=5 nginx-54f48578cf-22j86 | die aktuellsten 5 Zeilen
kubectl logs --since=2h nginx-54f48578cf-22j86 | die letzten 2 Stunden
kubectl exec -it nginx-54f48578cf-22j86 -- bash | Shell in einem laufenden Container öffnen
kubectl exec --stdin --tty nginx-54f48578cf-22j86 -- bash | alternative; -- trennt die Argumente
kubectl delete deployment nginx | Deployment löschen
kubectl apply -f kubernetes-config.yaml | Deployment über Datei erzeugen
kubectl get deployment nginx -o yaml > nginx-deployment.yaml | Konfiguration in YAML-Format erzeugen und in eine Datei umlenken
kubectl get pod --watch | Watchmodus
kubectl config get-context | Cluster anzeigen
kubectl use-context docker-for-desktop | Docker-Cluster verwenden
minikube service mongo-express-external-service | Externe Service-Kompononte eine externe IP geben
minikube addons enable ingress | Ingress Controller in Minikube installieren; bzw. startet die K8s Nginx Implementierung des Ingress Controller 
###### Nützliches
Anwendung | Beschreibung
-|-|-
kubens | default Namespace setzen; in Linux `brew install kubens`; in Windows `choco install kubens`
Kubernetes Dashboard | Dashboard UI
kubens | Namespaces anzeigen
kubens my-namespace | Default Namespace setzen
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.4.0/aio/deploy/recommended.yaml | Dashboard deployen
kubectl proxy | Dashboard zugreifbar machen: http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/.


###### Quellen
[Kubernetes](https://)
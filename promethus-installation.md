Steps to install promethus :
1. kubectl create namespace monitoring
2. helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
3. helm repo update
4. helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
5. helm repo update
6. helm install prometheus prometheus-community/prometheus -n monitoring
7. kubectl get svc -n monitoring
8. kubectl port-forward -n monitoring svc/prometheus-server 9090:80




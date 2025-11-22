Grafana setup steps:
1. helm repo add grafana https://grafana.github.io/helm-charts
2. helm repo update
3. helm install grafana grafana/grafana -n monitoring
4. kubectl get secret grafana -n monitoring \
  -o jsonpath="{.data.admin-password}" | base64 --decode ; echo
5. Access the grafana dahsboard: 
kubectl port-forward -n monitoring svc/grafana 3000:80



To generate a new `istio-dashboards.yaml` run:
```
kubectl -n prometheus create cm istio-dashboards \ 
--from-file=pilot-dashboard.json=pilot-dashboard.json \
--from-file=istio-workload-dashboard.json=istio-workload-dashboard.json \
--from-file=istio-service-dashboard.json=istio-service-dashboard.json \
--from-file=istio-performance-dashboard.json=istio-performance-dashboard.json \
--from-file=istio-mesh-dashboard.json=istio-mesh-dashboard.json \
--from-file=istio-extension-dashboard.json=istio-extension-dashboard.json \
--dry-run=client -o yaml > ../istio-dashboards.yaml
```
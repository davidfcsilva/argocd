Get argocd password
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
Port forwarding to the container
kubectl port-forward svc/argocd-server -n argocd 8080:443

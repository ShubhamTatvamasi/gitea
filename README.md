# gitea

https://artifacthub.io/packages/helm/gitea/gitea

Add repository
```bash
helm repo add gitea https://dl.gitea.com/charts
```

Install chart
```bash
helm upgrade -i gitea gitea/gitea \
  --version 12.5.3 \
  --namespace gitea \
  --create-namespace \
  --set service.http.type=LoadBalancer \
  --set service.http.port=80 \
  --set valkey-cluster.enabled=false \
  --set valkey.enabled=true \
  --set postgresql-ha.enabled=false \
  --set postgresql.enabled=true \
  --set gitea.admin.username=admin \
  --set gitea.admin.password=admin1234
```

---

Add gitea remote repo
```bash
git remote add gitea http://10.10.10.10/admin/gitea.git
```

Push changes to gitea:
```bash
git push gitea main
```

---

Run the server
```
docker-compose up -d
```

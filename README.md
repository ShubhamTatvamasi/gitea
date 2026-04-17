# gitea

Add repository
```
helm repo add gitea https://dl.gitea.com/charts
```

Install chart
```
helm upgrade -i gitea gitea/gitea \
  --version 12.5.3 \
  --namespace gitea \
  --create-namespace
```

---

Run the server
```
docker-compose up -d
```

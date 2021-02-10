# home-cluster

## Bootstrap command

```bash
flux bootstrap github \
  --owner sladkoff \
  --personal --private \
  --repository home-cluster \
  --path cluster \
  --branch master
```

Create sops-gpg secret
```
gpg --list-secret-keys leonid.koftun@gmail.com

gpg --export-secret-keys \
--armor xyz |
kubectl create secret generic sops-gpg \
--namespace=flux-system \
--from-file=sops.asc=/dev/stdin
```
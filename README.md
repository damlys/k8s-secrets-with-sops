Encrypt secret

```shell
sops --encrypt --output=manifests/mysql-envs.secret.enc.yaml manifests/mysql-envs.secret.dec.yaml
```

View secret

```shell
sops --decrypt manifests/mysql-envs.secret.enc.yaml
```

Apply secret

```shell
sops --decrypt manifests/mysql-envs.secret.enc.yaml | kubectl apply --filename=-
```

Edit secret

```shell
EDITOR="code --wait" sops manifests/mysql-envs.secret.enc.yaml
```

Decrypt secret

```shell
sops --decrypt --output=manifests/mysql-envs.secret.dec.yaml manifests/mysql-envs.secret.enc.yaml
```

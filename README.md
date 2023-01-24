# Deployment

## Create configMap

```$bash
kubectl apply -f postgres-config.yaml
```

## Create secret

```$bash
kubectl apply -f postgres-secret.yaml
```

## Create deployment postgres

```$bash
kubectl apply -f postgres-deployment.yaml
```

## describe a pods

```$bash
kubectl describe pods
```

## See logs deployment postres

```$bash
kubectl logs <POD_ID_POSTGRES_DEPLOYMENT>
```

## Create secret pg-admin

```$bash
kubectl apply -f pg-admin-secret.yaml
```

## Create deployment pg-admin

```$bash
kubectl apply -f pg-admin-deployment.yaml
```

## See logs pg-admin

```$bash
kubectl logs <POD_ID_PG_ADMIN_DEPLOYMENT>
```

## Create secret backend

```$bash
kubectl apply -f backend-secret.yaml
```

## Create deployment backend

```$bash
kubectl apply -f backend-deployment.yaml
```

## Delete

```$bash
kubectl delete -f postgres-deployment.yaml
kubectl delete -f postgres-secret.yaml
kubectl delete -f postgres-config.yaml
kubectl delete -f pg-admin-deployment.yaml
kubectl delete -f pg-admin-secret.yaml
kubectl delete -f backend-deployment.yaml
kubectl delete -f backend-secret.yaml
```

## Restart pod

```$bash
kubectl rollout restart deployment <NAME_DEPLOYMENT>
```

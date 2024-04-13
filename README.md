# Kubernetes Notes

## Basic cmds

### Delete resources

Scale pods down to 0

```sh
kube --namespace default scale deployment <my-deployment> --replicas 0
```

Delete all resources after scaling down

```sh
kube delete all —all —namespace default
```

If deployed with a file, remove in one go

```sh
kube delete -f <file_name>.yaml
```

### Create resource (deployment, service, etc...)

```sh
kube apply -f <file_name>.yaml
```

### Log into a pod that has shell

```sh
kube exec --stdin --tty <pod> -- /bin/sh
```
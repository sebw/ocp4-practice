# Build from S2I

```
oc new-project build-from-s2i
```

```
oc new-app --name build-from-s2i php:latest~https://github.com/sebw/ocp4-practice#master --context-dir build-from-s2i
```

```
oc expose svc/build-from-s2i
```
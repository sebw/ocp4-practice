# Deploy app from Dockerfile

Create project:

```
oc new-project build-from-dockerfile
```

Create the app:

`oc new-app --name build-from-dockerfile https://github.com/sebw/ocp4-practice.git\#master --context-dir=hello-world`

Expose the service:

`oc expose svc/hello-world`

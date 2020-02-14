# Deploy from template

```
oc new-project build-template
```

```
oc new-app --file php-mysql-ephemeral.json \
  -p NAME=quotesapi \
  -p APPLICATION_DOMAIN=quote-${RHT_OCP4_DEV_USER}.${RHT_OCP4_WILDCARD_DOMAIN} \
  -p SOURCE_REPOSITORY_URL=https://github.com/sebw/ocp4-practice \
  -p CONTEXT_DIR=build-from-template \
  -p DATABASE_SERVICE_NAME=quotesdb \
  -p DATABASE_USER=user1 \
  -p DATABASE_PASSWORD=mypa55 \
  --name quotes
```

Then

```
oc logs -f bc/quotesapi
```

Then

```
oc expose svc/quotesapi
```

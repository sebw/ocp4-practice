# OCP4 labs

Download CLI:

`wget https://mirror.openshift.com/pub/openshift-v4/clients/ocp/latest-4.2/openshift-client-linux-4.2.18.tar.gz`

Untar and copy `oc` and `kubectl` in $PATH.

Drop `~/.ocp4`:

```
RHT_OCP4_MASTER_API=https://api.ocp-eu2.prod.nextcle.com:6443
RHT_OCP4_DEV_USER=login
RHT_OCP4_DEV_PASSWORD=xxxxxx
```

Make sure the file is only readable by you.

Source the file:

`source ~/ocp4`

Login:

```
oc login -u $RHT_OCP4_DEV_USER -p $RHT_OCP4_DEV_PASSWORD $RHT_OCP4_MASTER_API
```

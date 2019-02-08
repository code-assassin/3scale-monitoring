Steps to provision Prometheus

```
oc process -f 3scale-prometheus-operator.yml -p NAMESPACE=3scale-v24 | oc create -f -
```



Steps to provision servicemonitor

```
oc process -f 3scale-servicemonitor.yml -p NAMESPACE=3scale-v24 APICAST_STAGING_SERVICE_NAME=apicast-staging | oc apply -f -
```

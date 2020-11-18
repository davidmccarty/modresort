# To deploy modresort project on MCM
## Edit the deployable.yaml
Get the ingress subdomain for your cloud instance and update the value here
```yaml
    spec:
      host: modresorts.<ingress-subdomain>
      port:
        targetPort: 9080
```
## Create modresort-deploy namespace and objects
```sh
oc new-project modresort-deploy
oc apply -f modresort-channel.yaml 
oc apply -f modresort-deployable.yaml 
```
## Create modresort-project namespace and objects
```sh
oc new-project modresort-project
oc apply -f modresort-application.yaml 
oc apply -f modresort-placement.yaml
oc apply -f modresort-subscription.yaml
```
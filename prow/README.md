# Deploy Prow Bot on Kubernetes

The Prow Bot deployment is a modified version based on the [Prow s3 starter](https://github.com/kubernetes/test-infra/blob/master/config/prow/cluster/starter-s3.yaml) for Kubernetes. Please follow the below instrctions to deploy/update the Bot.

1. Update the credentials under the `prow-parameters` section in [kustomize/kustomization.yaml](kustomize/kustomization.yaml). The Bot credentials are located within the internal team's folder.

2. Once the credentials are updated, modify any configuration within [kustomize/prow-kubernetes.yaml](kustomize/prow-kubernetes.yaml) if necessary. Then, run the following commands to deploy the Prow Bot on kubernetes.
```shell
kubectl apply -k kustomize
```

3. As the org admin, please update the [Github Webhook](https://github.com/organizations/open-labrador/settings/hooks) to the following
```
Payload URL: https://$(prow-ingress)/hook
Content type: application/json

Secret: $(hmac-token) in manifests

SSL verification: Enable
Which events would you like to trigger this webhook?: Send me everything.
```

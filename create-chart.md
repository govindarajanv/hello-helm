- Create a chart </br> $ helm create my-chart
```yaml
.
├── LICENSE
├── README.md
└── my-chart
    ├── Chart.yaml
    ├── charts
    ├── templates
    │   ├── NOTES.txt
    │   ├── _helpers.tpl
    │   ├── deployment.yaml
    │   ├── hpa.yaml
    │   ├── ingress.yaml
    │   ├── service.yaml
    │   ├── serviceaccount.yaml
    │   └── tests
    │       └── test-connection.yaml
    └── values.yaml

4 directories, 12 files

.helmignore to ignore including files in the chart
```
- Install the chart </br> $ helm install my-chart ./my-chart
- Package the chart </br> $ helm package ./my-chart --destination /tmp
- Check the release </br> $ helm list
- Upgrade a release </br> $ helm upgrade my-chart ./my-chart --set containerImage=nginx:1.18
- [Chart Museum](https://chartmuseum.com/) is an open source helm repository and the same can be installed via helm </br> $ helm install chartmuseum stable/chartmuseum --set env.open.DISABLE_API=false
- Set Chart Museum as local repo </br> $ helm repo add chartmuseum http://127.0.0.1:8080 
- Publish my-chart to chart museum </br> $ curl --data-binary "@my-chart-0.1.0.tgz" http:/127.0.0.1:8080/api/charts
- Update cache with the latest charts </br> $ helm repo update
- search for our chart </br> $ helm search repo chartmuseum/my-chart
- create a github repo and place the packaged chart into that clone repo </br> $ helm package ./hello-helm/my-chart/ --destination ./helm-charts
- Run </br> $ helm repo index .  # this creates index.yml file
```
apiVersion: v1
entries:
  my-chart:
  - apiVersion: v2
    appVersion: 1.16.0
    created: ""
    description: A Helm chart for Kubernetes
    digest: 
    name: my-chart
    type: application
    urls:
    - helm-charts/my-chart-0.1.0.tgz
    version: 0.1.0
generated: ""
```
- Get the raw path of index.yml </br> https://raw.githubusercontent.com/govindarajanv/helm-charts/master/index.yaml and remove index.yml from the end
- Add the repository </br> $ helm repo add govindarajanv https://raw.githubusercontent.com/govindarajanv/helm-charts/master

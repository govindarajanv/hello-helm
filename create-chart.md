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

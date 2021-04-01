# helm-charts
helm-charts

## pre-requisites
- vscode
- docker
- k8s

## Installing Helm
- $ sudo snap install helm --classic

## Commands
- version </br> $ helm version
- Add a repo </br> $ helm repo add stable https://charts.helm.sh/stable
- list repos </br> $ helm repo list
- Search a repo </br> $ helm search repo stable/mysql </br> $ helm search repo stable/mysql --versions
- Show chart </br> $ helm show chart stable/mysql
- Show chart README </br> $ helm show readme stable/mysql
- Show value </br> $ helm show values stable/mysql
- Install a chart dry-run </br> $ helm install mysql stable/mysql --dry-run --debug
- Install a particular version </br> $ helm install mysql stable/mysql --version=1.6.8
- Status of a release </br> $ helm list
- Status of releases incl uninstalled </br> $ helm list --all
- Delete the release and its history </br> $ helm delete mysql
- Detailed status</br> $ helm status mysql
- Get manifest of a release </br> $ helm get manifest mysql
- Get notes </br> $ helm get notes mysql
- Get all </br> $ helm get all mysql
- upgrade a release </br> $ helm upgrade mysql stable/mysql --version=1.6.9
- rollback of a release </br> $ helm rollback mysql 1
- Uninstall a release </br> $ helm uninstall mysql --keep-history
- history of a release </br> $ helm history mysql
- Pull down a chart </br> $ helm pull stable/mysql --untar
```
chart
  |______________________chart.yml  -   description and metadata about the chart
  |______________________values.yml -   default values of the chart
  |______________________charts/    -   dependent charts
  |______________________templates/ -   contains yaml files for the chart
                            |________________________   -   deployment.yaml
                            |________________________   -   service.yaml
                            |________________________   -   _helper.tpl
                            |________________________   -   NOTES.txt (help text for chart)
```
- create a new chart with a default yaml </br> $ helm create
- create an archive of chart for distribution </br> $ helm package

## Helm Hub
It is like a dockerhub but for Helm charts
[Helm Hub](https://hub.helm.sh)
It is now available as 'https://artifacthub.io/'


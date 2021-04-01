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
- Search a repo </br> $ helm search repo stable/mysql
- Show chart </br> $ helm show chart stable/mysql
- Show chart README </br> $ helm show readme stable/mysql
- Show value </br> $ helm show values stable/mysql
- Install a chart dry-run </br> $ helm install mysql stable/mysql --dry-run --debug
- Status of a release </br> $ helm list
- Detailed status</br> $ helm status mysql
- upgrade a release </br> $ helm upgrade
- rollback of a release </br> $ helm rollback
- history of a release </br> $ helm history
- create a new chart with a default yaml </br> $ helm create
- create an archive of chart for distribution </br> $ helm package

## Helm Hub
It is like a dockerhub but for Helm charts
[Helm Hub](https://hub.helm.sh)
It is now available as 'https://artifacthub.io/'


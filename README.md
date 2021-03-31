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
- Install a chart </br> $ helm install 
- Status of a release </br> $ helm list
- upgrade a release </br> $ helm upgrade
- rollback of a release </br> $ helm rollback
- history of a release </br> $ helm history
- create a new chart with a default yaml </br> $ helm create
- create an archive of chart for distribution </br> $ helm package

## Helm Hub
It is like a dockerhub but for Helm charts
[Helm Hub](https://hub.helm.sh)
It is now available as 'https://artifacthub.io/'


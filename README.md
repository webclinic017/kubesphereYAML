# kubesphereYAML

kubectl apply -f https://raw.githubusercontent.com/webclinic017/kubesphereYAML/main/kubesphere-installer.yaml

kubectl apply -f https://raw.githubusercontent.com/webclinic017/kubesphereYAML/main/cluster-configuration.yaml

kubectl logs -n kubesphere-system $(kubectl get pod -n kubesphere-system -l 'app in (ks-install, ks-installer)' -o jsonpath='{.items[0].metadata.name}') -f

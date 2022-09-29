Mit curl wird das neuste Installer Script für HELM heruntergeladen
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3

Die Berechigungen von dem script mit chmod 700 ändern. (Owner kann read write und execute)
chmod 700 get_helm.sh

Das Script ausführen und HELM installieren.
./get_helm.sh

Mit helm repo add das chart repository hinzufügen
helm repo add bitnami https://charts.bitnami.com/bitnami

Mit helm repo update die chart list updaten
helm repo update

Mit helm install wordpress installieren
helm install my-release bitnami/wordpress


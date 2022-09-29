Mit curl wird das neuste Installer Script für HELM heruntergeladen
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3

Die Berechigungen von dem script mit chmod 700 ändern. (Owner kann read write und execute)
chmod 700 get_helm.sh

Das Script ausführen und HELM installieren.
./get_helm.sh


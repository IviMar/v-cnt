Ein Pod kann neben normalen Containern auch mehrere init container beinhalten, welche laufen, bevor die app container gestarted sind.

Init Container sind wie normale container aussert:
Init Container laufen immer ganz durch
Der vorherige Init Container muss beendet sein, bevor der nächste startet.

Wenn ein Init container failt, wird er immer wieder ausgeführt, biss er erfolgreich durchläuf.
Aussert der Pod hat eine "restartPolicy" von "Never" dann wird der ganze Pod als failed angesehen, wenn ein init container failt.



Init containers in use



kubectl apply -f C/init.yaml
Führt yaml datei aus

kubectl get -f C/init.yaml
status überprüfen

kubectl describe -f C/init.yaml
Zeigt mehr details an

kubectl logs myapp-pod -c init-myservice
kubectl logs myapp-pod -c init-mydb
Zeigt logs an


myservice und mydb erstellt
kubectl apply -f C/my.yaml
erstellt die services

kubectl get -f C/my.yaml
Services laufen


Define a liveness command



kubectl apply -f B/healthy.yaml
Führt die yaml datei aus

kubectl describe pod liveness-exec
pod evemts anzeigen (keine liveness probes sind failed)

kubectl describe pod liveness-exec
erneut anzeigen (liveness probes sind failed)

kubectl get pod liveness-exec
nachschauen ob der container restarted ist (ja)



Define a liveness HTTP request




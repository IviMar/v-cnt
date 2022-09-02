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



kubectl apply -f B/http.yaml
Führt die yaml datei aus

kubectl describe pod liveness-http
Liveness probe failed: HTTP probe failed with statuscode: 500



Define a TCP liveness probe


kubectl apply -f B/tcp.yaml
Führt yaml Datei aus

kubectl describe pod goproxy
livelyness überprüfen ok



Define a gRPC liveness probe




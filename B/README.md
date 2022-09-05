Liveness Probes werden verwendet, um festzustellen, wann ein container neugestartet werden muss. Zum beispiel werdem mit liveness probes deadlocks festgestellt und dann ein container neugestartet.

Deadlock ist, wenn ein container zwar läuft, aber kein Fortschritt gemacht wid. Neustarten des containers kann dies beheben.

Readiness probes werden verwendet, um festzustellen wann ein pod bereit ist um traffic zu erhalten.
Wenn ein Pod nicht ready ist, wird er vom load balancer entfernt.

startup probes werden verwendet, um festzustellen, ob ein pod gestartet ist. Wird eine startup probe verwendet, disabled sie liveness und readiness probes, um sicherzustellen dass diese keinen einfluss auf die startup probe haben.

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



kubectl apply -f B/grcp.yaml
Führt yaml datei aus

kubectl describe pod etcd-with-grpc
livelyness check ist nicht fehlgeschlagen


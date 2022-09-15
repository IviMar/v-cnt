Im git Pot die config mit "cat config" ausgelesen und in einer txt datei gespeichert

Auf MAAS UI gegangen und die IP des Masters ausgelesen (Name und Range) (http://10.3.39.8:5240/)

Mit Putty auf dem Master eingeloggt

Mit "microk8s enable metrics-server" Metrics Server enabled

Mit "microk8s enable rbac" RBAC enabled (Dadurch wurde das MAAS gui abgeschaltet)

https://10.3.39.3:8443/ im Browser eingegeben, dort Kubeconfig angeklickt und das gespeicherte txt file mit den Settings ausgewählt

Das Dashboard https://10.3.39.3:8443/ ist nun abgesichert und funktionsfähig


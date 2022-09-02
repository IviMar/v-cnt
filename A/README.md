Hier kommt die Dokumentation

Cronjobs 
Cron ist ein zeitbasierter Job-Scheduler in Unix oder Unix-ähnlichen Computer-Betriebssystemen. Benutzer verwenden Cron, um Jobs, das heißt die Ausführung von Befehlen oder Shell-Skripts zu festgelegten Zeiten, Terminen oder Intervallen zu planen. Cron kann zur Automatisierung der Systemwartung oder -verwaltung, zum Download von Dateien aus dem Internet oder zum regelmäßigen E-Mail Versand genutzt werden. Es handelt sich hierbei um einen Daemon, also einen Hintergrundprozess, der immer auf dem Server läuft. Die Aufgaben, die Cron ausführen soll, werden als CronJob bezeichnet. Ursprünglich stammt der Name Cron vom griechischen Gott der Zeit "Chronos".

CronJobs können für einzelne Befehle oder für die automatisierte Ausführung periodisch wiederkehrender und aneinander gereihter Befehle eingesetzt werden, zum Beispiel für das Bereinigen von Datenbanken durch Entfernen veralteter Einträge, Logfiles und Kommentare oder zum Erstellen regelmäßiger Statistiken zur Anzahl der Benutzer einer Website.Weitere Anwendungsmöglichkeiten sind z.B. für Veröffentlichung neuer Inhalte auf einer Website zu einem bestimmten Termin, die gebündelte Generierung von Rechnungen oder der automatisierte Newsletterversand. Ebenso kann das Backup einer Datenbank mithilfe von CronJobs zeitgesteuert durchgeführt werden.

Yaml
Yaml ist eine Programmiersprache, mit ihr werden Codes ausgeführt. In unserem Beispiel zum Erstellen der Chronjobs.

Befehle
kubectl get pods

Führt die Config Datei aus und verbindet sich mit den Nodes.
gp open /workspace/.wg-config.conf


gp open $HOME/.kube/config

Startet den Code / die Jobs werden auf den Nodes nicht mehr ausgeführt
kubectl apply -f A/cronjob.yaml

Löscht die Jobs, der Code wird auf den Nodes nicht mehr ausgeführt bzw. die Jobs sind dan gelöscht
kubectl delete -f A/cronjob.yaml


kubectl create -f A/cronjob.yaml

Startet das Beobachten der Jobs, man sieht wie oft und in welchen Abständen diese ausgeführt werden.
kubectl get jobs --watch

Cloud-native Technology (Vertiefung)
====================================

In diesem Modul erfolgt eine Vertiefung im Themengebiet der Cloud-native Technologien.

In Theorie und Praxis werden aktuelle und zukünftige Cloud-native Konzepte vertieft. 

Themenfelder
------------

**Kubernetes Vertiefung**

In einem ersten Schritt werden, bis jetzt nur am Rande behandelte, Kubernetes Ressourcen vertieft.

* A - Jobs
* B - Health Probe Pattern
* C - Init Container
* D - Horizontal Pod Autoscaler
* E - Zugriffssteuerung (Role Based Access, RBAC)

**Weitergehende Konzepte (Add-ons)**

Anschliessend werden weitergehende Konzepte behandelt.

* H - Helm - der Paketmanager für Kubernetes
* I - Operator Pattern
* J - Monitoring
* K - Logging
* L - Service Mesh
* M - Serverless (Function as a Service, FaaS)

## Client Umgebung

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/IviMar/v-cnt)

Kompetenzmatrix
---------------

### Kubernetes Vertiefung

#### Jobs

Die Fachabteilungen legen mit grossen Batchjobs jeweils die ganze Informatik lahm.

Diese Batchjobs sollen unterteilt und so strukturiert werden, dass sie jederzeit im Hintergrund durchgeführt werden können.

#### Health Probe Pattern

Die von der Entwicklung angelieferten Microservices blockieren oder reagieren nicht mehr auf Kundenanfragen.

Mittels den "Health Probe Pattern" soll die Ausfallsicherheit der Microservices verbessert werden.

#### Init Container

Die angelieferten Container Images weissen erhebliche Sicherheitsmängel auf. Und/oder beinhalten Abhandlungen, z.B. Erstellen von 
Datenbanktabellen, die nicht in die Container Images gehören.

Mittels separaten Init Container sollen die Sicherheitsmängel verkleinert werden. Nicht zu Microservices gehörende Abhandlungen, 
z.B. Erstellen von Datenbanktabellen, soll in separate Init Container ausgelagert werden.

#### Horizontal Pod Autoscaler

Die Grundfunktionen von Kubernetes eine fixe Anzahl von Instanzen (Replicas) von Pods anzugeben, sind für einen produktiven Einsatz nicht ausreichend.

Statt einer fixen Angabe von Instanzen (Replicas), soll die Anzahl Instanzen Dynamisch zuwiesen werden können, z.B. anhand der Anzahl Requests.

#### Zugriffssteuerung (Role Based Access, RBAC)

Im Moment kann jeder Operator, praktisch unbegrenzt, auf die Cloud-native Infrastruktur zugreifen. 

Damit nicht jeder Operator jedes Password oder sonstige sensitive Informationen abfragen kann, soll der Zugriff mittels RBAC eingegrenzt werden.

### Weitergehende Konzepte (Add-ons)

#### Helm - der Paketmanager für Kubernetes

Durch den vermehrten Einsatz von Cloud-native mit Kubernetes sind die Anzahl Microservices rapide gestiegen.

Auch wird von den Kunden, mehr und mehr, ein Distributionen/Cloud Neutraler Einsatz (kein Vendor-lock) gewünscht.

Die bestehenden Deklarationen (YAML-Dateien) sollen nach Helm, dem Paketmanager von Kubernetes, überführt werden. Mit dem Ziel, dass die Microservices 
auf mehreren Kubernetes Distributionen einsetzbar sind.


#### Operator Pattern

Die Entwicklung und das Operating wollen noch mehr Abläufe automatisieren. Z.B. erfordert eine Änderungen an einer Datenbanktabelle immer noch 
manuelles Einwirken.

Diese Arbeiten sollten automatisiert werden und dazu das "Operator Pattern" eingesetzt werden.

#### Monitoring

Die Grundfunktionen von Kubernetes für das Überwachen der Systeme und Microservices genügen den Anforderungen nicht mehr. 
So sind z.B. keine "Alert Messages" oder die Behandlung von VIP-Kunden möglich.

Durch den Einsatz des Open Source Monitoring Stacks sollen diese Mängel beseitigt werden.

#### Logging

Da keine zentrale Verwaltung von Logfiles vorhanden ist, gehen diese immer wieder verloren.

Mittels einer zentralen Sammlung und Auswertung der Logfiles soll diesem Umstand abgeholfen werden.

#### Service Mesh

Über die Zeit sind die Applikationen gewachsen und bestehenden aus vielen einzelnen Microservices.

Um einen [Big Ball of Mud](https://de.wikipedia.org/wiki/Big_Ball_of_Mud) zu verhindern, sollen die Kommunikationswege visualisiert und zusätzlich Abgesichert werden.

#### Serverless (Function as a Service, FaaS)

Sehr viele Microservices laufen praktisch im Leerlauf und brauchen Prozessorzeit, obwohl sie nur ein paar Mal im Monat angewählt werden.

In Anlehnung an Serverless (FaaS) sollen nur selten benötigte Microservices nur noch auf Anfrage (On-Demand) gestartet werden.

- - - 

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/ch/"><img alt="Creative Commons Lizenzvertrag" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/ch/88x31.png" /></a><br />Dieses Werk ist lizenziert unter einer <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/ch/">Creative Commons Namensnennung - Nicht-kommerziell - Weitergabe unter gleichen Bedingungen 3.0 Schweiz Lizenz</a>.

- - - 

* Autor: Marcel Bernet 
* Mail: ![](x_gitressourcen/mailto.png)

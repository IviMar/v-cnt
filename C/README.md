Ein Pod kann neben normalen Containern auch mehrere init container beinhalten, welche laufen, bevor die app container gestarted sind.

Init Container sind wie normale container aussert:
Init Container laufen immer ganz durch
Der vorherige Init Container muss beendet sein, bevor der nächste startet.

Wenn ein Init container failt, wird er immer wieder ausgeführt, biss er erfolgreich durchläuf.
Aussert der Pod hat eine "restartPolicy" von "Never" dann wird der ganze Pod als failed angesehen, wenn ein init container failt.


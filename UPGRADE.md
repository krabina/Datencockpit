# Anleitung zum Updgrade einer bestehenden Version

#Upgrade V0.2 - > V1.0
* [DSG](https://github.com/krabina/Datencockpit/blob/master/wiki/Datencockpit-Content-DSG.xml) 
* [DSGVO](https://github.com/krabina/Datencockpit/blob/master/wiki/Datencockpit-Content-DSGVO.xml)
* [Strukturen](https://github.com/krabina/Datencockpit/blob/master/wiki/Datencockpit-Strukturen.xml)
via Spezial:Importieren in die bestehende Installation importieren (die anderen XML-Files haben sich nicht verändert)



#Beispiel V0.1 - > V0.2
* [Datencockpit-Update-V0-2.xml](https://github.com/krabina/Datencockpit/blob/master/wiki/Datencockpit-Update-V0-2.xml) via Spezial:Importieren in die bestehende Installation importieren
* File [Bearbeiten-Menü.png](https://github.com/krabina/Datencockpit/blob/master/wiki/Bearbeiten-Men%C3%BC.png) hochladen

Nach den Imports von XML-Files folgende Scripts ausführen
```
php maintenance/refreshLinks.php
php maintenance/runJobs.php
```

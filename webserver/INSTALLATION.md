# Installation - Variante Installation auf einem Webserver

Diese Varante der Installation ist die empfohlene Variante!

## Voraussetzungen
Sie benötigen grundsätzlich 
* einen Webserver (z. B. Apache)
* PHP
* einen Datenbank-Server (z. B. mySQL oder MariaDB)
  * Voraussetzungen für MediaWiki siehe https://www.mediawiki.org/wiki/Manual:Installation_requirements/de
  * Voraussetzungen für Semantic MediaWiki siehe https://www.semantic-mediawiki.org/wiki/Help:Installation#Requirements
  * Wegen mangelhafter PHP-Implementierung unter Windows wird von Windows-Servern abgeraten! Ein Linux-Server ist rasch installiert.

Das Datencockpit basiert auf
* MediaWiki 1.27.x
* Semantic MediaWiki 2.5.x 
* und einer Menge anderer Extensions, siehe http://www.datencockpit.at/Spezial:Version
  * (darum müssen Sie sich aber nicht kümmern, wenn Sie diese Installationsveriante wählen)

## Installation
* Installieren Sie einen Webserver, PHP sowie einen Datenbank-Server
  * [Aconomi](http://www.aconomi.com) hat uns dankenswerter Weise eine ausführliche Installationsanleitung für die Installation eines Ubuntu-Servers bis zum fertigen Datencockpit zur Verfügung gestellt: [Datencockpit_Installation_Ubuntu.pdf](https://github.com/krabina/Datencockpit/blob/master/webserver/Datencockpit_Installation_Ubuntu.pdf)
* Legen Sie eine Datenbank an, nennen Sie diese "kdz_datencockpit"
* Legen Sie einen DB-User an, nennen Sie diesen ebenfalls "kdz_datencockpit", geben Sie ihm alle Rechte und weisen Sie ihm der erzeugten Datenbank zu
* Importieren Sie den [Datenank-Dump](https://github.com/krabina/Datencockpit/blob/master/webserver/Datenbank.zip) (ca. 25 MB) in Ihre Datenbank 
      * (sehr einfach geht das mit https://www.phpmyadmin.net/ - aber auch über die [Kommandozeile](https://www.mediawiki.org/wiki/Manual:Restoring_a_wiki_from_backup#Import_the_database_backup))

* Laden Sie die Software-Komponenten herunter: https://github.com/krabina/Datencockpit/releases/download/1.0/datencockpit.tar.gz (Achtung: ca. 70MB)
* entpacken Sie das File Sie im Verzeichnis des Webservers
```
wget http://www.datencockpit.at/release/datencockpitV0-2.tar.gz
tar -xzvf datencockpitV0-2.tar.gz
```

Nun haben Sie ein Verzeichnis "datencockpit" mit der entpackten Software. Dieses muss das Web-Root-Verzeichnis des Webservers sein. Andernfalls müssen Sie den Inhalt des Verzeichnisses in <ihr Web-Root legen (häufig z. B. "public_html"). 

Passen Sie nun ein paar Einstellungen im File "LocalSettings.php" an - hier werden alle Konfigurationen vorgenommen, z. B. die URL der Installation, die DB-Zugangsdaten sowie die Mail-Adresse (normalerweise "apache@localhost"):
```
$wgServer = "http://www.datencockpit.at";

$wgEmergencyContact = "apache@www.datencockpit.at";
$wgPasswordSender = "apache@www.datencockpit.at";

$wgDBname = "kdz_datencockpit";
$wgDBuser = "kdz_datencockpit";
$wgDBpassword = "ihrDB-Passwort";
```
Weitere Infos zu LocalSettings.php finden Sie auf den  [MediaWiki-Hilfeseiten](https://www.mediawiki.org/wiki/Manual:LocalSettings.php/de)

* führen Sie das Wartungsscript "update.php" aus:
* Wir gehen nun davon aus, dass ihr Web-Root "datencockpit" heißt:

```
cd /datencockpit
php maintenance/update.php
```
Nun sollte das update-Script von MediaWiki durchlaufen. Rufen Sie anschließend die Website über die URL des Webservers auf.
Jetzt sollte Ihr Datencockpit erscheinen und so aussehen wie http://www.datencockpit.at

Sie können sich mit folgenden Zugangsdaten einloggen:
* User: Admin
* Pass: datenschutz
* **Ändern Sie das Passwort** rechts oben mit Klick auf das User-Icon und Auswahl von "Einstellungen". 

Nun sind Sie startbereit!

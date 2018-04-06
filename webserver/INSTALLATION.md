# Installation - Variante Installation auf einem Webserver

Diese Version ist die empfohlene Version!

## Voraussetzungen
Sie benötigen grundsätzlich 
* einen Webserver (z. B. Apache)
* PHP
* einen Datenbank-Server (z. B. mySQL oder MariaDB)
  * Voraussetzungen für MediaWiki siehe https://www.mediawiki.org/wiki/Manual:Installation_requirements/de
  * Voraussetzungen für SemanticMediaWiki siehe
  * Wegen mangelhafter PHP-Implementierung unter Windows wird von Windows-Servern abgeraten! Ein Linux-Server ist rasch installiert.

Das Datencockpit basiert auf
* MediaWiki 1.27.x
* SemanticMediaWiki 2.5.x 
* und einer Menge anderer Extensions, siehe http://www.datencockpit.at/Spezial:Version
  * (darum müssen Sie sich aber nicht kümmern, wenn Sie diese Installationsveriante wählen)

## Installation
* Installieren Sie einen Webserver, PHP sowie einen Datenbank-Server
* Legen Sie eine Datenbank an, nennen Sie diese "kdz_datencockpit"
* Legen Sie einen DB-User an, nennen Sie diesen ebenfalls "kdz_datencockpit", geben Sie ihm alle Rechte und weisen Sie ihm der erzeugten Datenbank zu
* Importieren Sie den [Datenank-Dump](https://github.com/krabina/Datencockpit/blob/master/webserver/kdz_datencockpit.sql) in Ihre Datenbank (sehr einfach geht das mit https://www.phpmyadmin.net/ - aber auch über die [Kommandozeile](https://www.mediawiki.org/wiki/Manual:Restoring_a_wiki_from_backup#Import_the_database_backup))

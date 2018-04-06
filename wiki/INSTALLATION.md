# Installation - Variante Import in ein bestehendes Wiki

Diese Version ist für Personen gedacht, die bereits über Erfahrung bei der Installation von MediaWiki verfügen!

## Voraussetzungen
* Sie benötigen eine möglichst idente MediaWiki-Installation inklusive einer Menge Erweiterungen, siehe: http://www.datencockpit.at/Spezial:Version
* Für die Installation von MediaWiki siehe https://www.mediawiki.org/wiki/Manual:Installation_guide/de
* Für die Installation von SemanticMediaWiki siehe: https://www.semantic-mediawiki.org/wiki/Help:Installation
* Weitere Installations-Anleitungen siehe die indivduellen Extension-Anleitungen
* Wenn Sie [Composer](https://getcomposer.org/) verwenden, können Sie das File [composer.local.json](https://github.com/krabina/Datencockpit/blob/master/wiki/composer.local.json) verwenden.
* Einige Extensions unterstützen Composer noch nicht, diese müssen Sie manuell installieren

## Import-Vorgang
In MediaWiki können BenutzerInnen mit Admin-Rechten über die Seite "Spezial:Importieren" XML-Files in das Wiki importieren

Für das Datencockpit auf jeden Fall benötigt ist das File
* Datencockpit-Strukturen-....xml 
es enthält alle benötigten Wiki-Seiten, mit denen die Struktur des Datencockpits aufgebaut wird.

Bei den Content-Seiten können Sie selbst entscheiden, was Sie importieren möchten:
* Datencockpit-Content-DSGVO-......xml (Gesetzestext der DSGVO)
* Datencockpit-Content-DSG-......xml (Gesetzestext des öst. DSG)
* Datencockpit-Content-Fragestellungen-......xml (Fragestellungen)
* Datencockpit-Content-Glossar-......xml (Glossar-Einträge)
* Datencockpit-Content-Testinhalte-......xml (ein paar Testinhalte)

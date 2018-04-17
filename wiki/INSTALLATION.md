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
In MediaWiki können BenutzerInnen mit Admin-Rechten über die Seite "Spezial:Importieren" XML-Files in das Wiki importieren. Die Files finden Sie im Ordner https://github.com/krabina/Datencockpit/tree/master/wiki

Für das Datencockpit auf jeden Fall benötigt ist das File
* Datencockpit-Strukturen-....xml 
es enthält alle benötigten Wiki-Seiten, mit denen die Struktur des Datencockpits aufgebaut wird.

Bei den Content-Seiten können Sie selbst entscheiden, was Sie importieren möchten:
* [Datencockpit-Content-DSGVO.xml](https://github.com/krabina/Datencockpit/blob/master/wiki/Datencockpit-Content-DSGVO.xml) (Gesetzestext der DSGVO)
* [Datencockpit-Content-DSG.xml](https://github.com/krabina/Datencockpit/blob/master/wiki/Datencockpit-Content-DSG.xml) (Gesetzestext des öst. DSG)
* [Datencockpit-Content-Fragestellungen.xml](https://github.com/krabina/Datencockpit/blob/master/wiki/Datencockpit-Content-Fragestellungen.xml) (Fragestellungen)
* [Datencockpit-Content-Glossar.xml](https://github.com/krabina/Datencockpit/blob/master/wiki/Datencockpit-Content-Glossar.xml) (Glossar-Einträge)
* [Datencockpit-Content-Testinhalte.xml](https://github.com/krabina/Datencockpit/blob/master/wiki/Datencockpit-Content-Testinhalte.xml) (ein paar Testinhalte)

## Weitere Files für das Skinning
Das Datencockpit verwendet ein Bootstrap-Basiertes Skin. Wenn Sie dieses auch verwenden wollen, müssen Sie zusätzlich die folgenden Files in ihr Installatiosverzeichnis kopieren:
* https://github.com/krabina/Datencockpit/blob/master/wiki/bootswatch.less
* https://github.com/krabina/Datencockpit/blob/master/wiki/kdz-layout.xml
* https://github.com/krabina/Datencockpit/blob/master/wiki/kdz-stylefixes.less
* https://github.com/krabina/Datencockpit/blob/master/wiki/variables.less
Weiters müssen Sie einige Icons in Ihr Wiki importieren, dies erfolgt entweder über die MediaWiki-Seite "Spezial:Hochladen" oder wesentlich bequemer (falls verfügbar) über Seite "Spezial:BatchUpload" der Extension [SimpleBatchUpload](https://www.mediawiki.org/wiki/Extension:SimpleBatchUpload)

## LocalSettings.php
Das File [LocalSettings.php](https://github.com/krabina/Datencockpit/blob/master/wiki/LocalSettings.php) enthält die Konfiguration von MediaWiki. Übernehmen Sie entweder die Teile daraus, die Sie in Ihrer Localsettings.php noch nicht haben oder nehmen Sie das File und ergänzen es um Ihre Einstellungen (Datenbank, E-Mail...)

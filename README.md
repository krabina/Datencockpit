# Datencockpit
Datencockpit.at zur Erfüllung der Dokumentationspflichten laut DSGVO (Fulfilling GDPR requrements with a data cockpit)

## English information
www.datencockpit.at is an internal knowledge management system to support organizations to fulfil their documentation requirements by the GDPR (General Data Protecton Regulatio) of the European Union. It is a customization of [Semantic MediaWiki](https://github.com/SemanticMediaWiki/SemanticMediaWiki) and several other extensions. What is presented here is mainly a configuration of SemanticMediaWiki so serve as a tool for documenting the record of processing activities, data breaches, data  protection impact assessments, etc. As the content is in German only, all futher documentation will be in German. 

## Deutsch: Einführung
Datencockpit ist das Open-Source-Repository zur Lösung www.datencockpit.at. Die Website demonstriert die Verwendung von [Semantic MediaWiki](https://github.com/SemanticMediaWiki/SemanticMediaWiki) und zahlreichen weiteren Extensions zur Erfüllung der Dokumentationspflichten der Datenschutz-Grundverordnung (DSGVO) der Europäischen Union. Die Idee ist, dass Organisationen eine Website wie www.datencockpit.at in einem internen Netzwerk (Einzelunternehmer auf ihrem PC) betreiben und ihr Datencockpit dazu benutzen, aktives Datenschutzmanagement zu betreiben. Das bedeutet, allen Dokumentationserfordernissen, wie z. B. das Verfahrensverzeichnis, Datenschutzverletzungen, Folgenabschätzungen etc. nachzukommen und laufend einen Überblick über datenschutzrelevante Themen und Vorkommnisse zu haben. 

Da für die Lösung keine eingene Programmierung erfolgt ist, sondern lediglich die Konfiguration von Semantic MediaWiki, wird dieses Repository dazu verwendet, die aktuellen Inhalte anzubieten, um eigene Installationen der Lösungen zu unterstützen.

## Installation
Es gibt grundsätzlich mehrere Möglichkeiten, wie man ein eigenes Datencockpit installieren kann, je nach eigenem Know-how bzw. technischen Voraussetzungen sollte man die Variante wählen, die am passendsten erscheint. Daher zunächst ein Überblick. Die Reihenfolge entspricht der Komplexität.

Installationsvariante | Anmerkungen
------------ | -------------
Starten einer VirtualBox | eine speziell hergerichtete virtuelle Maschine wird mittels https://www.virtualbox.org/ gestartet. Hierzu das von [Gesinn-IT](https://github.com/gesinn-it) zur Verfügung gestellte .OVA-File [datencockpit_1.0.1+02.ova](https://github.com/krabina/Datencockpit/releases/download/1.0/datencockpit_1.0.1+02.ova) herunterladen (ACHTUNG: ist 1,8GB groß), in die VirtualBox importieren und starten. Wenn die Box läuft, erreicht man das Datencockpit unter http://localhost:8080/Datencockpit/ Anpassungen können vorgenommen werden, siehe dazu die Dokumentation von [semantic::core go!](https://sourceforge.net/p/semantic-core-go/wiki/Home/), der Distribution auf der die VirtualBox-Variante vom Datencockpit basiert.
Installation auf einem [Webserver](https://github.com/krabina/Datencockpit/blob/master/webserver/INSTALLATION.md) | die Software wird auf einem Webserver entpackt, die Datenbank importiert
Integration in ein bestehendes [Wiki](https://github.com/krabina/Datencockpit/blob/master/wiki/INSTALLATION.md) | XML-Files mit den MediaWiki-Seiten werden in ein bestehendes Wiki importiert
Installation via Docker | Dank [soudis](https://github.com/soudis) gibt es eine Version zur Installation via [Docker](https://www.docker.com/): https://github.com/soudis/datencockpit-docker

Zugangsdaten für den Admin-User sind jeweils
* User: Admin
* Pass: datenschutz
* **Ändern Sie das Passwort** rechts oben mit Klick auf das User-Icon und Auswahl von "Einstellungen". 


Noch einfacher ist eine Hosting-Variante. Dabei wird ihr persönliches Datencockpit im Internet gehostet, selbstverständlich nur für Sie und Ihre User sichbar. Weitere Informationen dazu siehe: http://www.wikiahoi.at/dsgvo/

## Releases und Upgrade von Vorversionen
Beachten Sie die [RELEASE-NOTES](https://github.com/krabina/Datencockpit/blob/master/RELEASE-NOTES.md) sowie die Hinweise zum [UPGRADE](https://github.com/krabina/Datencockpit/blob/master/UPGRADE.md)

# Feedback und Support
Für Fragen und Feedback schreiben Sie bitte ein E-Mail an bernhard.krabina@km-a.net 

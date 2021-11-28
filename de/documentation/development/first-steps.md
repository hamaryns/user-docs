---
title: Erste Schritte
description: Foodsoft Installation und Entwicklung
published: true
date: 2021-11-28T12:57:58.051Z
tags: 
editor: markdown
dateCreated: 2021-10-01T12:20:11.258Z
---

Die Foodsoft ist eine frei zugängliche Software, geschrieben in der Sprache Ruby basierend auf Rails. Die Quelltexte dafür sind auf der Web-Plattform Github öffentlich zugänglich. 

# Github Repositories

Über diese Plattform kannst du 
- die Foodsoft herunterladen, um sie 
  - auf deinem Rechner lokal zu installieren, um sie dort auszuprobieren oder auch Änderungen im Quelltext durchzuführen und sie zu testen
  - auf einem Webserver zu installieren, um sie den Mitgliedern deiner Foodcoop zugänglich zu machen
- Issues einbringen, wenn du auf Fehler (Bugs) draufgekommen bist, oder dir neue Funktionen wünscht, und auch  Issues von anderen einsehen und kommentieren (z.B. in der Art wie: ja das ist für mich auch relevant)
-  Von dir modifizierte oder neu geschriebene Quellcodes für Änderungs- und Erweiterungsvorschläge hochladen (Pull Requests), die dann hoffentlich von den anderen für gut geheißen werden, sodass sie „commited“ werden und damit offiziell Teil der Foodsoft werden

Folgende Links führen zu den Github Repositories:
- https://github.com/foodcoops/foodsoft – der Hauptzweig der Foodsoft.
- https://github.com/foodcoopsat/foodsoft – eine Abspaltung („Fork“) des Hauptzweigs, der den Stand der Foodsoft am IG Foodcoops Server (https://app.foodcoops.at/...) wiederspiegeln sollte. Manche Erweiterungen sind hier für die österreichischen Foodcoops integriert, die für Foodcoops in anderen Ländern nicht „relevant“ sind.
- Sobald du dich registrierst und selbst Änderungen durchführst, solltest du einen Fork für deine Änderungen anlegen, der dann unter https://github.com/DEIN_GITHUB_BENUTZERNAME/foodsoft erreichbar ist.

# Installation der Foodsoft
- [Foodsoft setup manuell](https://github.com/foodcoops/foodsoft/blob/master)
- [Foodsoft setup Docker](https://github.com/foodcoops/foodsoft/blob/master/doc/SETUP_DEVELOPMENT_DOCKER.md)
{.links-list}


## Anleitung für Ubuntu Linux über Docker

> Diese Anleitung ist möglicherweise unvollständig und wurde schon länger nicht mehr getestet.
{.is-warning}


### Installation
1. Docker Engine installieren:  https://docs.docker.com/engine/install/ubuntu/ 
2. Docker Compose installieren: https://docs.docker.com/compose/install/ > Linux (Aktuelle Version 1.28 oder ähnlich ist höher als erforderliche Version 1.4)
3. Docker so konfigurieren, dass es die nötigen Berechtigungen hat: https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user 
4. Computer neu starten, damit Änderungen wirksam werden, zum Testem `docker run hello-world` ausführen, es dürfen keine Fehlermeldungen kommen 
5. Github installieren mit `sudo apt-get install git`, siehe auch https://git-scm.com/download/linux 
   - `sudo snap install gh`   
   - `sudo apt  install gitsome` 
6. Auf Github registrieren: Grundsätzlich kannst du dir den Quelltext mit „Download“ auch einfach herunterladen, um die Foodsoft lokal bei dir zu installieren. Sobald du jedoch veränderte Quellcodes wieder auf Github hochladen möchtest, kommt es zu  Problemen, wenn die Foodsoft in der Zwischenzeit durch andere auf Github verändert wurde. Daher zahlt es sich aus, den Quellcode gleich ordentlich „abzuzweigen“, sodass dann zu einem späteren Zeitunkt auch wieder ein reibungsloses Hochladen von Änderungen (push) möglich ist.
7. Fork erzeugen
8. Foodsoft herunterladen mit `git clone https://github.com/foodcoops/foodsoft.git`
9. Docker Compose aus dem Verzeichnis `foodsoft` aufrufen (dort befindet sich die Datei `docker-compose-dev.yml`), wie unter Setup beschrieben: https://github.com/foodcoops/foodsoft/blob/master/doc/SETUP_DEVELOPMENT_DOCKER.md 
     - `docker-compose -f docker-compose-dev.yml up -d mariadb`
     - `docker-compose -f docker-compose-dev.yml run --rm foodsoft bundle install`
     - `docker-compose -f docker-compose-dev.yml run --rm foodsoft bundle exec rake  foodsoft:setup_development_docker`
     - `docker-compose -f docker-compose-dev.yml run --rm foodsoft bundle exec rake db:schema:load db:seed:small.en`

### Lokale Instanz starten
1. Foodsoft „lokalen Server starten“: `docker-compose -f docker-compose-dev.yml up`
2. Falls es beim ersten Mal nach der Installation zu Fehlermeldungen kommt, den Computer neu starten und Schritt 1 wiederholen
3. Aufruf der lokalen Instanz im Webbrowser:  http://localhost:3000 
4. Anmelden mit Benutzer `admin` und Passwort `secret`

### Github mit SSH-Verbindung einrichten
1. https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh 
2. https://docs.github.com/en/github/using-git/changing-a-remotes-url#switching-remote-urls-from-https-to-ssh 


# Ruby on Rails 
Allgemeine Einführungen zum Ruby Framework für Web-Applikationen:
- https://www.tutorialspoint.com/ruby-on-rails/rails-introduction.htm 
- Ruby in 20 Minutes: https://www.ruby-lang.org/en/documentation/quickstart/  

# Foodsoft Dateistruktur

https://github.com/foodcoops/foodsoft/ 

Wo ist im Code was zu finden? 
- Datenbank Spezifikationen: app/models/...
  - Zeichenanzahl  Begrenzungen für Eingabefelder
  - Überprüfungen von Eingaben: z.B. unique (Name darf nur einmal vergeben werden, z.B. bei Artikelnamen)
- Übersetzungstexte für deutsche Foodsoft Version bearbeitbar über
  - https://crowdin.com/translate/foodsoft/ - wird nur 1-2 mal im Jahr übernommen, wenn ein „echtes Release“ herauskommt
  - `config/locales/de.yml` 

> Hier nur ein Auszug, bitte gerne erweitern!
{.is-danger}

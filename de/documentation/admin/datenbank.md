---
title: Datenbank - phpMyAdmin
description: Welche verstecken Features der Zugriff auf die Foodsoft-Datenbank bietet
published: false
date: 2023-04-09T02:10:13.914Z
tags: 
editor: markdown
dateCreated: 2023-04-09T02:10:13.914Z
---

# Datenbankzugriff via phpMyAdmin

> Über das Tool phpMyAdmin kannst du einfach im Browser auf die Datenbank deiner Foodsoft-Instanz zugreifen und Daten auslesen/verändern.
Dies ist für einige versteckte Features, für die es noch kein Menü in der Foodsoft-Benutzeroberfläche gibt, die einzige Möglichkeit sie zu aktivieren.
In anderen Fällen kann es einfach viel praktischer sein, als z.B. eine Reihe von Daten händisch über die Foodsoft-Benutzeroberfläche zu bearbeiten bzw. nachzuschlagen.
Für viele Zwecke brauchst du dabei gar keine speziellen SQL-Kenntnisse.
{.is-success}

> Sei aber äußerst vorsichtig, denn du kannst mit diesem Tool deine Foodsoft-Instanz zerstören bzw. darin viel kaputtmachen!
Sei daher behutsam mit dem Einsatz von phpMyAdmin und beachte u.a.:
	Verändere nicht die `id` eines Datensatzes, denn andere Datensätze verweisen auf diesen mittels dieser ID, außerdem dürfen zwei Datensätze in einer Tabelle nicht die gleiche ID haben.
{.is-warning}

> Den Zugang zu eurer Foodsoft-Datenbank musst du zunächst beim Host deiner Foodsoft-Instanz (z.B. IG FoodCoops in Österreich) anfordern.
Anschließend kannst du im Browser phpMyAdmin öffnen (die Adresse variiert je nach Installation).
{.is-info}


# Einführung in phpMyAdmin
## Navigation

In der linken Seitenleiste siehst du, für welche Foodsoft-Instanzen du Zugriffsrechte hast.

![grafik.png](/grafik.png)

Für jede Foodsoft-Instanz ist eine Reihe an Tabellen gespeichert:

![db_tabellen.png](/db_tabellen.png)

In jeder Tabelle wird eine Reihe an Datensätzen gespeichert, beispielsweise sämtliche Artikel von allen Lieferantinnen.

![db_datensaetze.png](/db_datensaetze.png)

## Datensätze bearbeiten

Um einen Wert in einem Datensatz zu bearbeiten, einfach auf den Wert doppelklicken:

![db_inline.png](/db_inline.png)

Bei mehrzeiligen Werten kann es jedoch mühsam sein, sie "inline" zu bearbeiten. Dafür links auf "Bearbeiten" klicken. Im folgenden Menü können die Werte in einem größeren Feld bearbeitet werden.

![db_bearbeiten.png](/db_bearbeiten.png)

Danach musst die Änderungen am Datensatz noch speichern, indem du unten auf OK klickst:

![db_speichern.png](/db_speichern.png)

Oder du klickst im Browser einfach auf Zurück oder in der oberen Leiste auf Anzeigen, um die Bearbeitung abzubrechen.

## Weitere Funktionen

Mit den entsprechenden Kenntnissen lassen sich auch SQL-Befehle und viele Funktionen anwenden. Diese brauchst du jedoch für die folgenden Anleitungen nicht.

# Benutzerdefinierte Felder (custom fields)

Mit diesem Feature kannst du zusätzliche Felder für
- Benutzerinnen
- Bestellgruppen
- Arbeitsgruppen
- Lieferantinnen (speichern funktioniert nicht)
- Rechnungen

anlegen, in die dann über die Benutzeroberfläche Daten eingetragen werden können.

> Die benutzerdefinierten Felder werden nicht in den Anzeige-Menüs aufgelistet, sondern nur in den Bearbeiten- bzw. Erstellen-Menüs.
{.is-danger}

Benutzerdefinierte Felder werden zusammen mit den Standard-Felder angezeigt:

![cf_bestellgruppe.drawio.png](/cf_bestellgruppe.drawio.png)

> Benutzerdefinierte Felder für Lieferantinnen werden zwar angezeigt, Eingaben werden jedoch nicht gespeichert: [Issue 952](https://github.com/foodcoops/foodsoft/issues/952)
{.is-danger}

## Felder konfigurieren

### Settings-Tabelle öffnen

Die Konfiguration der benutzerdefinierten Felder wird in einem einzigen Datensatz in der Tabelle settings gespeichert.

![db_settings.png](/db_settings.png)

### Datensatz für benutzerdefinierte Felder finden

Stelle die Anzahl der Datensätze auf das Maximum und gib bei "Zeilen filtern" `.custom` ein, dann sollte ein Datensatz mit var = `foodcoop.<name>.custom_fields` erscheinen. Wenn nichts erscheint, probiere auf Seite 2, 3 ... zu blättern, bis er erscheint.

![db_customfields.png](/db_customfields.png)

### Bearbeiten

Klicke auf **Bearbeiten** und verändere den Wert unter Value. Beispiel:

![db_cf_bearbeiten-.png](/db_cf_bearbeiten-.png)

### Syntax
#### Felder für unterschiedliche Objekte

So können jeweils beliebig viele Felder für Benutzerinnen, Bestellgruppen, Arbeitsgruppen, Lieferantinnen und Rechnungen konfiguriert werden.

--- !ruby/hash:ActiveSupport::HashWithIndifferentAccess
user:
  - name: user_field
    label: Benutzerinnen-Feld
ordergroup:
  - name: ordergroup_field
    label: Bestellgruppen-Feld
workgroup:
  - name: workgroup_field
    label: Arbeitsgruppen-Feld
supplier:
  - name: supplier_field
    label: Lieferantinnen-Feld
invoice:
  - name: invoice_field
    label: Rechnungen-Feld

#### Weitere Optionen

Für Felder gibt es noch weitere Optionen:

--- !ruby/hash:ActiveSupport::HashWithIndifferentAccess
user:
  - name: test_field
    label: Testfeld
    hint: Ein Hinweis, der unterhalb des Eingabefeldes angezeigt wird.
    placeholder: 'Hinweis innerhalb des Eingabefeldes'
  

## Foodsoft Anwendung

Wenn du neu in deiner Foodcoop bist, und die Foodsoft einfach mal zum Bestellen kennenlernen möchtest, bist du hier richtig. 
- [Starten und Navigieren](/de/documentation/usage/navigation)Grundlegende Informationen für Benutzerinnen, Navigation in der Foodsoft: wo finde ich was?
- [Mein Profil & Bestellgruppe](/de/documentation/usage/profile-ordergroup)Erklärung des eigenen Foodsoft-Kontos und der eigenen Bestellgruppe, persönliche Einstellungen, Verwendung des Zahlungsreferenzrechners
- [Bestellen](/de/documentation/usage/order)Überblick und Anleitungen zur Bestellung sowie Abholung
- [Kommunikation](/de/documentation/usage/communication)Foodsoft Nachrichten, Mitglieder Kontakte, Umfragen und ander Hilfsmittel zur Kommunikation in der Foodcoop
- [Mitmachen](/de/documentation/usage/tasks-cooperate)Beschreibung der Funktionen zur Koordination und transparenten Aufgabenverteilung 
- [Informationen & Dokumente](/de/documentation/usage/sharedocuments)Zentrale Ablage und gemeinsames Bearbeiten von Informationen sowie Dokumenten
{.links-list}

## Foodsoft Administration

Was die Foodosft alles kann, wobei und wie sie eure Foodcoop unterstützen kann, und wir ihr sie einrichten könnt. Auch im laufenden Betrieb der Foodcoop braucht die Foodsoft  Administratorinnen, die sich im Hintergrund darum kümmern, dass es regelmäßig etwas zu Bestellen gibt, Artikel in der Foodsoft aktuell sind, und auch die Bestellungen abgrechnet und die Rechnungen der Lieferantinnen bezahlt werden. 

- [Überblick](/de/documentation/admin/general)Funktionsüberblick und Einsatzmöglichkeiten der Foodsoft
- [Lieferantinnen, Artikeln und Kategorien](/de/documentation/admin/suppliers)Verwaltung von Lieferantinnen und Artikeln
- [Bestellungen](/de/documentation/admin/orders)Verwaltung von Bestellungen und Rechnungen
- [Lager](/de/documentation/admin/storage)Verwalten des Foodcoop-Lagers und Produktinventars
- [Finanzen](/de/documentation/admin/finances)Überblicksseite zu Finanzfunktionen sowie Verwendung
- [-- Mitglieder-Konten für Guthaben](/de/documentation/admin/finances/accounts)Verwaltung der Guthaben-Konten aller Foodcoop-Mitglieder und Transaktionen
- [-- Rechnungen](/de/documentation/admin/finances/invoices)Rechnungen von Lieferantinnen digital ablegen, mit Bestellungen verknüpfen und abgleichen sowie Bezahlstatus markieren
- [-- Bankkonto mit Foodsoft verknüpfen](/de/documentation/admin/finances/bank-accounts)Automatisierte Erfassung und Verarbeitung von Zahlungsein- und -ausgängen auf Foodcoop-Bankkonten, Zahlungsreferenzrechner aktivieren
- [-- Mehrwertsteuer, Brutto und Netto](/de/documentation/admin/finances/value-added-tax)Steuerliches in Foodcoop erfassen und verwalten
- [-- Pfand](/de/documentation/admin/finances/deposits)Wie Pfand in Foodcoops gehandhabt und in Foodsoft erfasst werden kann
- [Benutzerinnen](/de/documentation/admin/users)Verwaltung aller Mitglieder,  Bestellgruppen, Arbeits- und Nachrichtengruppen, Vergabe von administrativen Berechtigungen
- [Einstellungen](/de/documentation/admin/settings)Erklärung zu globalen/administrativen Einstellungen der Foodsoft
- [Begriffserklärungen](/de/documentation/admin/terms-definitions)Definitionen und Bedeutungen von Begriffen in der Foodsoft 
- [Häufige Fragen und Probleme](/de/documentation/admin/faq) Antworten und Lösungen für häufige Fragen und Probleme bei administrativen Funktionen
{.links-list}


## Foodsoft Entwicklung

Die Foodsoft ist eine frei zugängliche Software, und wird laufend verbessert und weiterentwickelt. Wenn du selbst eine Foodsoft installieren möchtest oder etwas zur Entwicklung beitragen möchtest, bist du hier am richtigen Platz.

- [Erste Schritte](/de/documentation/development/first-steps)Foodsoft Installation und Entwicklung
- [Leitfaden Foodsoft Dokumentation](/de/documentation/development/howtowrite)Leitfaden zur Bearbeitung von Beiträgen dieser Foodosoft Dokumentation
{.links-list}

# Andere Foodsoft Dokumentationen

Diese Dokumentationen sind unvollständig und nicht aktuell.

  - [Foodsoft@Github](https://github.com/foodcoops/foodsoft/wiki/Doku) 
  - [foodcoops.readthedocs.io](https://foodcoops.readthedocs.io/en/latest/)
{.links-list}


# Foodsoft Alternativen


- [Foodcoop-Shop](https://www.foodcoopshop.com/)
- Abrechnung über Papierlisten (vielleicht mag jemand eine Anleitung dazu schreiben?)
{.links-list}

> Warum in einer Doku für die Foodsoft "Werbung" für alternative Möglichkeiten? Falls sich jemand hierher z.B. auf der Suche nach einer Doku für den Foodcoopshop verirrt hat, oder sich einen Überblick über Foodsoft Apps verschaffen möchte, oder einfach mal wissen möchte, was es denn mit dieser "anderen Foodsoft" auf sich hat.
{.is-info}

# Andere Handbücher für Foodcoops

- [Foodcoop Gründungsleitfaden](https://handbuch.foodcoops.at/)Handbuch und Tipps zur Gründung von Lebensmittelkooperativen [PDF Download](http://www.bio-austria.at/app/uploads/FoodCoop-Handbuch-Juni-2017.pdf)
- [Organisiert euch!](https://organisiert-euch.org/)Handbuch und Tipps zum gemeinsamen Arbeiten und kooperativem Miteinander
{.links-list}


# Andere Hilfswerkzeuge für Foodcoops

## Österreichische Foodcoops: Forum und anderes
Über https://fcoop.at/ stehen folgende Services für österreichische FoodCoops zur Verfügung: 
- Forum
- Etherpad (Kollaborativer Texteditor)
- EtherCalc (Kollaborative Tabellenverarbeitung)
- URL Shortener
- BitPoll Terminfindung (Doodle)
- Nextcloud Online Speicherplatz (Dropbox)
- Jitsi Online Videkonferenz
> Für die Nutzung dieser Services ist ein Zugang zu einer österreichischen Foodsoft Instanz oder ein eigens beantragter **Zugang zum Forum** erforderlich. Nur nach der Anmeldung im Forum sind die Services zugänglich.
{.is-warning}

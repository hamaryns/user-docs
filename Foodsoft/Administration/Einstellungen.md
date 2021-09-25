---
title: Einstellungen
description: Foodsoft Menü "Administration" - alles was nicht mit Benutzerinnenverwaltung zu tun hat
published: true
date: 2021-05-25T13:55:45.601Z
tags: 
editor: markdown
dateCreated: 2021-04-21T00:20:52.701Z
---

<h1 id="einstellungen-usergruppen-verwaltung" class="toc-header"><a class="toc-anchor" href="#usergruppen-verwaltung"></a>BenutzerInnen, Bestell-, Arbeits- und Nachrichtengruppen</h1>

Siehe [Benutzerinnenverwaltung](Benutzerverwaltung).

<h1 id="einstellungen-email-probleme" class="toc-header"><a class="toc-anchor" href="#email-probleme"></a>E-Mail Probleme</h1>

Wenn Emails an Mitglieder oder Lierantinnen nicht zugestellt werden können, legt die Foodsoft hier einen Eintrag an. 

<h1 id="einstellungen-finanzen" class="toc-header"><a class="toc-anchor" href="#einstellungen-finanzen"></a>Finanzen</h1>


<h2 id="einstellungen-ktk-ktt" class="toc-header"><a class="toc-anchor" href="#einstellungen-ktk-ktt"></a>Kontotransaktionsklassen und -typen </h2>

Siehe auch  [Konten](Konten).


<h2 id="einstellungen-bankkonten-gateways" class="toc-header"><a class="toc-anchor" href="#einstellungen-bankkonten-gateways"></a>Bankkonten und Gateways</h2>

Siehe auch [Bankkonto](Finanzen/Bankkonto).


<h1 id="einstellungen-links" class="toc-header"><a class="toc-anchor" href="#einstellungen-links"></a>Links</h1>

Links im Foodsoft-Menü "Links" verwalten.

![links-menue.png](/links-menue.png)

<h1 id="einstellungen-einstellungen" class="toc-header"><a class="toc-anchor" href="#einstellungen-einstellungen"></a>Einstellungen</h1>

<h2 id="einstellungen-foodcoop" class="toc-header"><a class="toc-anchor" href="#einstellungen-foodcoop"></a>Foodcoop</h2>

- Name
- Straße
- Postleitzahl
- Stadt
- Land
- E-Mail
- Telefon
- Webseite


<h2 id="einstellungen-einstellungen-finanzen" class="toc-header"><a class="toc-anchor" href="#einstellungen-einstellungen-finanzen"></a>Finanzen</h2>

- Foodcoop Marge
- Mehrwertsteuer

- Minimaler Kontostand: minimal erforderliches verfügbares Guthaben(?), um bestellen zu können; leer = Null
- Mitglieder manuell abrechnen
- IBAN verwenden
- Selbstbedienung verwenden
- Bestellschema
- Kistenauffüllen 
- Bestellschluss
- Kistenauffüllphase


<h2 id="einstellungen-aufgaben" class="toc-header"><a class="toc-anchor" href="#einstellungen-aufgaben"></a>Aufgaben</h2>

- Wiederkehrende Aufgaben
- Apfelpunkte verwenden

<h2 id="einstellungen-nachrichten" class="toc-header"><a class="toc-anchor" href="#einstellungen-nachrichten"></a>Nachrichten</h2>

- E-Mails versenden
- Absenderadresse
- Antwortadresse
- Nachrichten
- Mailingliste
- Mailingliste anmelden


<h2 id="einstellungen-layout" class="toc-header"><a class="toc-anchor" href="#einstellungen-layout"></a>Layout</h2>

- Fußzeile Webseite
- Angepasstes CSS
- PDF-Dokumente
  - Schriftgrösse
  - Seitenformat
  - Seitenwechsel
  - Jede Bestellgruppe auf eine eigene Seite bringen
  - Jeden Artikel auf eine eigene Seite bringen

<h2 id="einstellungen-sprache" class="toc-header"><a class="toc-anchor" href="#einstellungen-sprache"></a>Sprache</h2>

- Standardsprache
- Browsersprache ignorieren
- Zeitzone
- Währung
  - Leerzeichen hinzufügen 

<h2 id="einstellungen-sicherheit" class="toc-header"><a class="toc-anchor" href="#einstellungen-sicherheit"></a>Sicherheit</h2>

- Zugriff auf: jedes Mitglied der Foodcoop hat automatisch Zugriff auf folgende Bereiche. Siehe Berechtigungen
- Api Titl:e de.config.keys.api\_key

<h2 id="einstellungen-sonstiges" class="toc-header"><a class="toc-anchor" href="#einstellungen-sonstiges"></a>Sonstiges</h2>

- Umfragen aktivieren
- Wiki verwenden
- Benutzernamen verwenden
- Bestelltoleranz maximal ausnutzen, um möglichst große Mengen zu bestellen
- Verteilungs-Strategie
- Einladungen deaktivieren
- URL Dokumentation
- Code für Websiteanalysetool
- Dokumente verwenden
  - Erlaubte Endungen
  - Drucker verwenden

<h2 id="einstellungen-liste" class="toc-header"><a class="toc-anchor" href="#einstellungen-liste"></a>Liste</h2>

Alle Einstellungen gemeinsam in einer Liste dargestellt


<h2 id="einstellungen-apps" class="toc-header"><a class="toc-anchor" href="#einstellungen-apps"></a>Apps</h2>


<h1 id="einstellungen-startseite" class="toc-header"><a class="toc-anchor" href="#einstellungen-startseite"></a>Login- und Startseite</h1>

<h2 id="einstellungen-anmeldseite-individuell" class="toc-header"><a class="toc-anchor" href="#einstellungen-anmeldseite-individuell"></a>Adaptierung der Foodsoft-Loginseite</h2>

Die Login-Seite der Foodsoft kann individuell an deine Foodsoft angepast werden, indem du eine Wiki-Seite mit dem Titel **Public\_frontpage** erstellst. Der Inhalt dieser Wiki-Seite könnte z.B. sein:

> === Foodcoop XY ===
> Bitte melde dich mit deinen Zugangsdaten an, um Zugang zu unserer Foodsoft zu erhalten. 
>
> Der Zugang ist nur für Mitglieder der Foodcoop Franckkistl möglich. 
>
> Wenn du noch kein Mitglied bist, kannst du über ... Probemitglied werden  und damit einen Zugang bekommen.

<h2 id="einstellungen-dashboard-individuell" class="toc-header"><a class="toc-anchor" href="#einstellungen-dashboard-individuell"></a>Adaptierung des Dashboards (Startseite)</h2>

Erstelle eine Wiki-Seite mit dem Titel **Dashboard**, die als erster Block am Dashboard angezeigt wird. 

Damit diese Wiki Seite leichter aufgefunden und bearbeitet werden kann, kannst du am Ende der Seite z.B. folgenden Text einfügen (bitte Link entsprechend deiner Foodcoop anpasssen): 


> \<p style="font-size:8px">''Text veränderbar über die Wiki Seite 
> \[https://app.foodcoops.at/...(foodcoop name).../wiki/Dashboard 
> Dashboard];  \</p>


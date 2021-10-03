---
title: Foodsoft-Konten für Guthaben der Mitglieder
description: Verwaltung der Guthaben-Konten aller Foodcoop-Mitglieder und Transaktionen (Menü "Finanzen" > "Konten verwalten")
published: true
date: 2021-10-03T10:58:59.751Z
tags: 
editor: markdown
dateCreated: 2021-04-20T23:12:07.102Z
---

Jede Bestellgruppe hat in der Foodsoft automatisch ein virtuelles Konto, das ein Guthaben für die Bestellgruppe darstellt. Die Guthabenstände können von Finanzberechtigten in der Foodsoft manuell verändert werden (z.B. aufgrund von Zahlunsgeingängen im Ebanking des Foodcoop Bankkontos), oder automatisch durch eine Anbindung der Foodsoft an das Bankkonto der Foodsoft. Die Foodsoft kann die Kosten für Bestellungen und Mitgliedsbeiträge von diesem Guthaben abbuchen. 

Auch die Foodccoop selbst hat ein Konto, auf das z.B. die Mitgliedsbeiträge, die von den Bestellgruppen abgeucht werden, gutgeschrieben werden können.

# Transaktionsklassen und Transaktionstypen

Das Guthaben der Foodsoftkonten der einzelen Bestellgruppen kann über **Transaktionsklassen** in mehrere Teilguthaben aufgeteilt werden, zum Beispiel für Bestellungen und für Mitgliedsbeitrag. Diese können getrennt aufgeladen werden (siehe auch Zahlungsreferenz-Rechner), und Kontostände werden auch für die Mitglieder separat angezeigt. In den Transaktionslisten (Foodsoft-Kontoauszüge) gibt es für jede Klasse eine eigene Spalte.

**Transaktionstypen** sind in Ergänzung zum Verwendungszweck (“Notiz”) bei Transaktionen zu sehen. Während bei Notiz der Text frei wählbar ist, können bei Transaktionstyp nur jene Typen ausgewählt werden, die auch vorher angelegt wurden. Dadurch wird es möglich, ähnliche Transaktionen zu gruppieren und einzeln zu bilanzieren, siehe dazu die Beispiele im Folgenden. Transaktionstypen sind jeweils einer Transaktionsklasse zugeordnet, sodass die Klasse automatisch über den Typ ausgewählt wird.

Bei folgenden Funktionen in der Foodsoft ist jeweils eine Transaktionsklasse auszuwählen:
- Finanzen \> Konten verwalten
  - neue Transaktion 
  - neue Überweisungen eingeben
- Finanzen \> Bestellungen abrechnen \> abrechnen
- Finanzen \> Bankkonten \> Transaktionen zuordnen (Auswahl erfolgt automatisch aufgrund der Zahlunsgreferenzcodes)
- Finanzen \> Bankkonten \> Finanzlink erstellen \> Kontotransaktion hinzufügen

Ist eine neue Foodcoop entstanden, gibt es standardmäßig (default) eine Klasse „Other“ mit einem Kontotransaktionstypen (KTT) „**Foodcoop**“. Das ist das Mindestmaß das vom System notwendig ist (und daher angelegt wird) um grundlegende Funktionalität anzubieten. Da alle Foodcoops (FCs) sehr unterschiedlich organisiert sind und arbeiten gibt es keinen Leitfaden für „Die Richtige Einstellung“. Sondern: Von FC zu FC gibt es unterschiedliche Herangehensweisen, Bedürfnisse und somit Einstellungen. Durch Erstellung einiger zusätzlicher Kontotransaktionstypen und der Anbindung des Vereinskontos bietet die Foodsoft zusätzlich zum Bestellen eine vereinfachte (doppelte) Buchführung.

## Transaktionsklassen und -typen erstellen und bearbeiten

*Administration \> Finanzen*

> Hier fehlt noch eine detaillierte Beschreibung.
{.is-info}

## Empfehlungen für Transaktionsklassen und -typen 

- Transaktionsklasse “Guthaben Bestellungen”
  - Transaktionstyp “Überweisung Guthaben”, Kürzel G für Aufbuchung Guthaben durch Mitglieder
  - Transaktionstyp ”Foodsoft” für Abbuchungen für Bestellungen durch Foodcoop 
  - Vorschläge für weitere Transaktionstypen (Franckkistl): Anfangsbuchstaben im Alphabet hinter F wichtig damit “Foodsoft” als Standard bei Auswahllisten an erster Stelle steht):
    - Spende 
    - Lieferung (wenn Foodcoop Mitglied Ware liefert und mit Foodsoft Guthaben bezahlt wird)
    - Zuschuss Fahrtkosten
    - Spesen für Anschaffungen (z.B. Mitglied besorgt und bezahlt aus eigener Tasche Glühbirnen für Lagerraum, bekommt Betrag über Foodsoft gutgeschrieben)
    - Pfandauszahlung
    - Vorschuss Guthaben (für Notfälle, wenn die Banktransaktion zu lange dauert, Transaktion soll dann wieder gelöscht werden wenn Guthaben eintrifft; Vorteil: man kann in der exportierten Kontodatei nach diesen Transaktionen suchen und prüfen, ob sie alle storniert wurden.)
- Transaktionsklasse “Guthaben Mitgliedsbeitrag” 
  - Transaktionstyp “Überweisung Mitgliedsbeitrag”, Kürzel M für Aufbuchung Mitgliedsbeitrag durch Mitglieder
  - Transaktionstyp “Mitgliedsbeitrag” für Abbuchung Mitgliedsbeitrag durch Foodcoop
    - Option *Für Kontostand ignorieren* sollte angewählt werden, damit das Guthaben Mitgliedsbeitrag nicht zum verfügbaren Guthaben hinzugerechnet wird.

In der Ansicht **Finanzen \> Konten verwalten** sind die Transaktionsklassen als Spalten abgebildet und ermöglichen einen Überblick der ev. noch nicht erfolgten Einzahlungen (zb. Mitgliedsbeitrag).

Forumsbeiträge zum Thema:

  - [*https://forum.foodcoops.at/t/bank-anbindung-verstehen-und-richtig-konfigueren/471*](https://forum.foodcoops.at/t/bank-anbindung-verstehen-und-richtig-konfigueren/471)
  - [*https://forum.foodcoops.at/t/neue-funktionen-in-der-foodsoft/4847/2*](https://forum.foodcoops.at/t/neue-funktionen-in-der-foodsoft/4847/2)
  
# Kontoauszüge anzeigen

*Finanzen \> Konten verwalten* 
- Liste Bestellgruppen: Kontoauszug \> Kontoauszug der Bestellgruppe anzeigen
  - gelöschte Bestellgruppen sind nicht auswählbar
- **Alle Transaktionen**: alle Transaktionen aller (auch bereits gelöschter Bestellgruppen, gekennzeichnet mit †) werden angezeigt
  - Kontoauszug von gelöschter Bestellgruppe rekonstruieren: Transaktion der Bestellgruppe suchen, in Spalte „Bestellgruppe“ auf Link klicken: alle Kontotransaktionen und End-Kontostand werden angezeigt
- **Foodcoop Transaktionen**: eigenes Konto für Foodsoft, wo z.B. Mitgliedsbeiträge hingebucht werden können, siehe *Sammeltransaktionen manuell durchführen*.
- **Finanzlink erstellen**: ...

## Summe aller Guthaben ermitteln

> Hier fehlt noch eine detaillierte Beschreibung.
{.is-info}

# Transaktionen durchführen

## Transaktionen einzeln manuell durchführen

Finanzen \> Konten verwalten
- Bestellgruppe suchen über Suchfeld, blättern oder Anzahl der dargstellten Einträge erhöhen
- Bei der entsprechenden Bestellgruppe “Neue Transaktion” anklicken
- Positiver Betrag: Guthaben erhöht sich, negativer Betrag: Guthaben verringert sich.
- Cent-Betrag mit Komma oder Punkt als Dezimaltrenner eingeben: 1,25 oder 1.25 möglich.

## Transaktionen automatisch durchführen

Bei Zahlungseingang am Foodcoop Bankkonto Guthaben für Bestellgruppe aufladen: siehe [Bankkonto mit Foodsoft verknüpfen](/de/documentation/admin/finances/bank-accounts). 

## Sammeltransaktionen manuell durchführen

Wenn mehreren Bestellgruppen unterschiedliche Beträge (egal ob positiv oder negativ) aber mit gleichem Text und gleichem Transaktionstyp zu buchen sind. 
Insbesondere für die Abbuchung von Mitgliedsbeiträgen, siehe unten eigener Abschnitt.

*Finanzen \> Konten verwalten \> Neue Überweisungen eingeben*
- **Cent-Beträge: Punkt statt Komma** als Dezimaltrenner verwenden\! 
Also z.B. **1.25** für 1,25 € = 1 € 25 Cent. Sonst wird der Cent-Betrag abgeschnitten, also 1,25 ergibt 1,00 €.
- Foodcoop Transaktion erstellen: Die Summe aller eingegeben Beträge wird mit umgekehrten Vorzeichen dem Foodsoft-Konto “Foodcoop” gegengebucht (siehe [Foodsoft-Kontoauszüge anzeigen](#anchor-139)). 
- Finanzlink erstellen: ...

## Bestellungen abbuchen

Wie Mitgliedern das Guthaben für Bestellungen abgebucht werden kann, findest du unter [Bestellung abrechnen](../Bestellungen).


## Mitgliedsbeiträge abbuchen

Empfohlene Vorgehensweise:
- Administration \> Finanzen: Transaktionsklassen anlegen wie oben beschrieben:
  - Mitglieder können über Zahlungsreferenzcodes selbst ihre Guthaben für Mitgliedsbeitrag und Bestellung aufladen. 
  - Monatlich wird der Mitgliedsbeitrag per Sammeltransaktion vom “Guthaben Mitgliedsbeitrag” abgebucht wie im Folgenden beschreiben.
  - Der Kontostand aller Transaktionsklassen wirkt sich grundsätzlich auf das verfügbare Guthaben für Bestellungen aus, solange bei einzelnen Transaktionsklassen nicht die Option *Für Kontostand ignorieren* aktiviert ist. Daher sollte diese Optiion für die Transaktionsklasse der Mitgliedsbeiträge aktiviert werden (neu März 2021). 


### Aktivierung und Vorbereitung

- Administration \> Einstellungen \> ...
- Einmalig erforderlich: Alle Bestellgruppen über *Administration \> Bestellgruppen* einzeln bearbeiten: Mitgliedsbeitrag mit minus eingeben, also z.B. -10 für 10 € Mitgliedsbeitrag
- Wenn neue Bestellgruppen angelegt werden: Mitgliedsbeitrag eintragen\!

### Abbuchung von Mitgliedsbeiträgen

- Finanzen \> Konten verwalten \> Neue Überweisungen eingeben
- Kontotransaktionstyp: empfohlen, eine Kategorie “Mitgliedsbeitrag” wie oben beschrieben anzulegen und auszuwählen
- Text: Empfehlung: für welchen Zeitraum wird der Mitgliedsbeitrag abgebucht, z.B. “Juli 2020”
- Alle Bestellgruppen mit Mitgliedsbeitrag hinzufügen
- Foodcoop Transaktion erstellen: Die Summe aller eingezogenen Mitgliedsbeiträge wird mit dem Foodsoft-Konto “Foodcoop” gutgeschrieben. Dadurch bekommst du einen Überblick, wieviele Mitgliedsbeiträge die Foodcoop bezieht.
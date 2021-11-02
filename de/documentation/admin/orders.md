---
title: Bestellungen
description: Verwaltung von Bestellungen und Rechnungen (Foodsoft-Menü: "Bestellungen" > "Bestellverwaltung" und "Abholtage" ; "Finanzen" > "Bestellungen abrechnen")
published: true
date: 2021-11-02T17:06:11.481Z
tags: 
editor: markdown
dateCreated: 2021-04-20T22:03:00.312Z
---

# Einleitung

## Lebenszyklus von Bestellungen

Eine Bestellung ist immer genau einer [Lieferantin](/de/documentation/admin/suppliers) zugeordnet. Es können gleichzeitig beliebig viele Bestellungen aktiv sein, von verschiedenen aber auch von der selben Lieferantin. 

Bestellungen durchlaufen in der Regel folgende Stadien, wobei eine Änderung meist nur vorwärts möglich ist:

1. Bestellung ist noch nicht offen, weil sie erst in der Zukunft startet (optional); sie ist in diese Stadium nur für Administratorinnen sichtbar.
2. Bestellung ist offen: Bestellgruppen ([Definition Bestellgruppe](/de/documentation/usage/profile-ordergroup), [Administration](/de/documentation/admin/users)) können ihre Bestellungen erstellen und bearbeiten. Das für die Bestellung benötigte Guthaben der Bestellgruppen wird "reserviert": das verfügbare Guthaben verringert sich entsprechend. Die  Kontostände der Bestellgruppen bleiben zunächst unverändert.  
3. Bestellung ist beendet: Bestellgruppen können ihre Bestellungen nicht mehr bearbeiten, Bestellungen werden an Lieferantinnen geschickt; Bestellung kann nicht mehr wieder geöffnet werden, um von Bestellgruppen bearbeitet zu werden. Nach der Lieferung kann die Bestellung grundsätzlich nur noch mit spezieller Berechtigung  angepasst werden (z.B. wenn nicht alles geliefert wurde, was bestellt wurde)
4. Bestellung ist abgrechnet: Bestellung kann nicht mehr verändert werden, die Beträge wurden den Bestellgruppen von ihren Foodsoft-Konten endgültig abgebucht.

Die folgende Skizze stellt diesen Lebenszyklus dar. Der blaue Pfeil in der Mitte deutet die Zeitachse an: 
![bestellung.png](/uploads-de/admin_orders_bestellung.png =400x)

## Bestellungen abrechnen und Rechnungen anlegen

Beim Bestellen werden die Beträge den Bestellgruppen noch nicht von ihren Konten abgebucht, es verringern sich zunächst nur die verfügbaren Guthaben. Erst beim Abrechnen einer Bestellung werden die Beträge für diese Bestellung den Bestellgruppen von ihren Foodsoft-Konten abgebucht.
Nur vorher können noch Anpassungen durchgeführt werden, wenn es z.B. bei der Lieferung Abweichungen zur Bestellung gibt. Weiters sollte die Rechnung des Produzenten angelegt und mit der Bestellung verknüpft werden, um vergleichen zu können, ob sich die Geldbeträge von Rechnung und Bestellung decken.

> Achtung auf die Einhaltung der Reihenfolge: sobald eine Bestellung abgerechnet ist, kann sie nicht mehr angepasst werden, und es können keine Rechnungen mehr mit dieser Bestellung verknüpft werden.
{.is-warning}

Daher sollte folgende Reihenfolge strikt eingehalten werden:

1. Bestellung an tatsächlich gelieferte Artikel anpassen
2. Rechnung in der Foodsoft für die Bestellung anlegen (Details siehe unten). Wenn die ProduzentInnen Rechnungen über mehrere Bestellungen gesammelt ausstellen, warten, bis die Rechnung kommt und für die betroffenen Bestellungen eine gemeinsame Rechnung in der Foodsoft anlegen. 
3. Rechnungsdaten der Rechnung von der ProduzentIn in die Foodsoft eingeben und prüfen: stimmen Beträge von Bestellung/Lieferung (“Total”) und der pfandbereinigten Rechnung überein? 
4. Rechnung bezahlen per Überweisung vom Foodcoop Bankkonto 
5. Bankdaten importieren und zuordnen: Rechnung wird in der Foodsoft als bezahlt gekennzeichnet 
6. Bestellung abrechnen 

## Erforderliche Berechtigungen für Bestellverwaltung

- Bestellungen anlegen, bearbeiten, beenden, anpassen, Lieferungen entgegenehmen, Rechnungen anlegen: **Bestellungen**
- Lagerbestellungen anlegen: **Lieferanten** oder **Artikeldatenbank**
- Bestellungen abrechnen: **Finanzen**

Berechtigungen vergeben siehe [Benutzerverwaltung](/de/documentation/admin/users).

# Bestellungen anlegen

Es gibt folgende zwei Arten von Bestellungen, die an unterschiedlichen Stellen erstellt werden:

- Bestellung der Foodcoop-Mitglieder (Bestellgruppen) bei Lieferantin: "Bestellung"
   - optional: Foodcoop bestellt (zusätzlich zu den Bestellgruppen) bei Lieferantin Artikel fürs Lager: "Lagerbestellung"
- Bestellung der Foodcoop-Mitglieder (Bestellgruppen) im Lager: "Lagerbestellung"



![lagerbestellung3.png](/uploads-de/admin_orders_lagerbestellung3.png =400x)

## Bestellung bei Lieferant

Bestellung bei Lieferantin anlegen: **Bestellungen > Bestellverwaltung > neue Bestellung anlegen** > Lieferant auswählen (Berechtigung Bestellen erforderlich)

![bestellung-anlegen1.png](/uploads-de/admin_orders_bestellung-anlegen1.png)


> *Bestellung kopieren* erspart bei regelmäßigen Bestellungen Aufwand. Allerdings werden dabei zunächst nur die Artikel der kopierten Bestellung übernommen. 
{.is-info}


> Die Foodsoft erlaubt derzeit noch keine automatisierte Erstellung von Bestellungen. Auch wenn sich z.B. eine Bestellung wöchentlich exakt wiederholt, muss sie dennoch jede Woche neu angelegt werden.
{.is-info}


## Bestellung aus Lager

Bestellung für Foodcoop-Mitglieder aus dem Foodcoop [Lager](/de/documentation/admin/storage) anlegen: 
**Artikel > Lager > Lagerbestellung online stellen** (Berechtigung Lieferanten oder Artikeldatenbank erforderlich)

![lagerbestellung.png](/uploads-de/admin_orders_lagerbestellung.png)



## Details für Bestellung

![admin-bestellung-neu-details.png](/uploads-de/admin_orders_neu-details.png)

### Bestellzeitraum: "Läuft vom", "Endet am"

Eine Bestellung ist im festgelegten Zeitraum „offen“, d.h. dass Bestellgruppen bestellen können bzw. ihre Bestellung verändern können. 
- Beginndatum und Zeit ("Läuft vom"): aktuelles Datum und Uhrzeit, bearbeitbar
- Enddatum und Zeit ("Endet am"): leer oder der Datum und Uhrzeit des nächsten Wochentags, der über Administration > Einstellungen > Finanzen als  Standard-Bestellschluss festgelegt wurde.

Sobald eine Bestellung beendet ist, 

- können die Bestellguppen ihre Bestellung nicht mehr verändern. Üblicherweise ist das erforderlich, weil dann die Bestellungen an die Lieferanten geschickt werden, und Änderungen daher nicht mehr berücksichtigt werden könnten.  
- kann das Abholdatum nicht mehr verändert werden

### Abholung

Das Abholdatum ist wichtig, wenn Abhhollisten über die Funktion *Bestellen \> Abholtage* erstellt werden, damit alle Bestellungen eines Abholtages gemeinsam auf den Listen erscheinen. Es kann nach dem Beenden der Bestellung nicht mehr geändert bzw. gesetzt sein. Daher die
Empfehlung, Bestellungen erst mit einem Enddatum zu versehen bzw. zu beenden, wenn auch das Abholdatum feststeht.

### Endeaktion: Optionen für Aktionen beim Bestellende

![bestellung-anlegen.png](/uploads-de/admin_orders_bestellung-anlegen-endaktion.png)

- **keine automatische Aktion:** die Bestellung bleibt offen. Sinnvoll, wenn eine Mindestbestellmenge erreicht werden soll, und die Bestellung so lange hinausgezögert werden soll, bis sie erreicht wird. Oder wenn unklar ist, wann die Lieferung genau erfolgen wird (Abholdatum unbekannt).
- **Bestellung beenden**: die Bestellung wird automatisch beendet, und kann dann auch nicht mehr geöffnet werden.
- **Bestellung beenden und an Lieferantin schicken:** die Bestellliste wird von der Foodsoft automatisch als PDF Anhang per Email an die Lieferantin und an das Foodsoft Mitglied geschickt. 
- **Bestellung beenden und an Lieferantin schicken sofern die Mindestbestellmenge erreicht wurde**: bei jeder Lieferantin kann eine Mindestbestellmenge als Geldbetrag angegeben werden. Dieser Mindestbetrag und wieviel davon schon erreicht wurde, wird den Bestellgruppen beim Bestellen angezeigt. Wenn die Bestellung nicht zustande kommt, sollte
  - Eine Nachricht an die Bestellgruppen geschickt werden (Funktion „An die Mitglieder schicken, die bei einer Bestellung etwas bestellt haben“, siehe [Kommunikation](/de/documentation/usage/communication)). Diese Funktion kann auch direkt über das Brief Symbol beim Bearbeiten der Bestellung ausgelöst werden.
  - Bestellen \> Bestellverwaltung \> Beendet \> Bestellung (Zeile mit der betroffenen Bestellung suchen)... \> in Empfang nehmen, Alle auf Null setzen, Bestellung in Empfang nehmen. Damit wird dann auch nichts abgerechnet, und die auf den Bestelllisten (Bestellen \> Abholtage) scheint bestellt: x, erhalten: 0 auf, in grau statt schwarz. Das sollte idealerweise möglichst rasch nachdem die Bestellung gescheitert ist, passieren, damit es bei den ausgedruckten Bestelllisten (siehe unten) berücksichtigt ist. 
  - Vorschlag für Automatisierung: [*https://github.com/foodcoops/foodsoft/issues/858*](https://github.com/foodcoops/foodsoft/issues/858)
       
### Notiz

Kommentar zur Bestellung, wird den Mitgliedern im Bestellfenster angezeigt.

![admin-bestellung-neu-details-notiz.png](/uploads-de/admin_orders_neu-details-notiz.png)



### Artikel für Bestellung auswählen

Es werden nur die Artikel des Lieferanten zur Bestellung hinzugefügt, die aktuell verfügbar sind (Lager: Lagerstand \> 0). 

> Wenn Artikel nachträglich verfügbar werden, hinzugefügt oder ins Lager geliefert werden, muss die Bestellung bearbeitet werden und die zusätzlichen Artikel ausgewählt werden (oder: „alle auswählen“ am unteren Ende der Liste).
{.is-warning}

### Bestellung erstellen

Mit "Bestellung erstellen" wird die Bestellung gespeichert und kann, solange sie noch nicht beendet ist, noch bearbeitet werden.






# Bestellungen bearbeiten

Beide Arten von Bestellungen (Lieferantin und Lager) können unter **Bestellungen > Bestellverwaltung > Bearbeiten** bearbeitet werden, solange sie noch nicht beendet sind. Es können Beginn und Ende der Bestellung, Endaktion, Notiz und die verfügbaren Artikel bearbeitet werden. 

Wenn Bestellungen beendet sind, können sie nur mehr an die Lieferung angepasst werden ("in Empfang nehmnen") und für eine neue Bestellung kopiert werden, jeodch nicht mehr bearbeitet werden.






# Bestellungen anzeigen

Beide Arten von Bestellungen (Lieferantin und Lager) können unter **Bestellungen > Bestellverwaltung > Anzeigen** angezeigt werden. Dabei wird der aktuelle Status der Bestellung angezeigt, also welche und wieviele Artikel von den Foodcoop Mitgliedern bisher bestellt wurden. 

## Standardansicht: Artikelübersicht
Komplette Artikelliste der Lieferantin wird angezeigt, nicht bestellte Artikel grau, bestellte Artikel grün mit der gesamten Anzahl bestellter Einheiten

## Sortiert nach Gruppen
Überschrift für jede Bestellgruppe, die etwas bestellt haben, darunter die bestellten Artikel der Bestellgruppe.

## Sortiert nach Artikeln
Überschrift für jeden Artikel (sofern mindestens 1 Einheit bestellt wurde), darunter die Bestellgruppen und die von ihnen jeweils bestellten Einheiten.

## Lagerbestellung bei Lieferantin

Zusätzlich zu den direkten Bestellungen der Mitglieder kann bei einer Bestellung bei der Lieferantin eine Lagerbestellung (Foodcoop bestellt bei Lieferant um Lagerbestand aufzufüllen) hinzugefügt werden, solange die Bestellung noch offen ist. Diese Artikel scheinen dann in der Bestellliste, die an den Lieferanten geht, auch auf, nicht aber in der Abrechnung und bei “Bestellung annehmen”(?). Wenn die Artikel geliefert sind, ist fürs Lager nochmal extra eine Lieferung für diese Artikel anzulegen, damit sie in den Lagerbestand aufgenommen werden. Für die Rechnung sind dann sowohl Bestellung und (Lager-)Lieferung anzugeben.

![lagerbestellung2.png](/uploads-de/admin_orders_lagerbestellung2.png)


# Bestellung beenden

Eine Bestellung endet automatisch, wenn dies vorher so eingestellt wurde (siehe oben), kann aber jederzeit auch manuell (vorzeitig) über "Beenden" beendet werden.

> "Beenden" kann nicht mehr rückgängig gemacht werden. Die Bestellung ist dann gesperrt und kann nicht mehr verändert werden  (keine Veränderung der Bestellung durch Bestellgruppen, keine Änderung des Abholdatums durch Administratorinnen möglich).  
{.is-warning}


# Bestelllisten für Lieferantinnen

- **Automatisch** (siehe oben beim Anlegen einer Bestellung: Endeaktion ...  an Lieferantin schicken) über die Foodsoft: Foodsoft versendet Email an Lieferantin mit automatisch erstellter Bestellliste als PDF und CSV Datei im Anhang, CC an FC Mitglied, das die Bestellung erstellt hat.
- **Manuell**:
    - Über die Funktion Bestellverwaltung > Bestellung anzeigen > **an Lieferantin schicken**: ...
    -  Bestelllisten herunterladen (Bestellungen > Bestellverwaltung > Bestellung anzeigen > **Download > Fax PDF/Text/CSV**) und z.B. per Email versenden

![bestellung-download.png](/uploads-de/admin_orders_bestellung-download.png)

> Die Funktion "Download" ist nur für beendete Bestellungen verügbar.
{.is-warning}

> Die Fax-Downloads enthalten nur jene Artikel, von denen etwas bestellt wurde, und hier auch nur die Gesamtzahl der Artikeleinheiten, ohne die Information, welche Bestellgruppe wieviel davon bestellt hat. 
{.is-info}


## Beispiel Fax PDF

In diesem Beispiel wurden bei den Artikel der Lieferantin keine Bestellnummern eingegeben, sodass die erste Spalte leer ist. 
> Die Liefarantin druckt diese Liste aus und vermerkt in der ersten Spalte händisch die tatsächlich gelieferte Menge, falls es Abweichungen gibt. So wird die Bestellliste zum Lieferschein und kommt mit der Lieferung in die Foodcoop zurück.

![bestellliste-faxpdf.png](/uploads-de/admin_orders_bestellliste-faxpdf.png) 

> Die Artikel sind alphabetisch nach Artikelname und im Gegensatz zu den Bestelllisten bei Bestellen auch nicht nach Kategorien sortiert. Achtung z.B. bei ähnlichen Produkten in verschiedenen Kategorien, z.B. Salat (Kategorie Gemüse) und Salat (Kategorie Pflanze).  
{.is-warning}

> Weitere Beispiel Screenshots
{.is-danger}

> Die Download-Optionen "Gruppen/Artikel/Matrix PDF" enthalten Foodcoop-interne Informationen (welche Bestellgruppe hat von welchem Artikel wieviel bestellt), die normalerweise für die Lieferantin nicht relevant sind.
{.is-info}


# Bestelllisten für die Foodcoop

Die Foodcoop benötigt Bestelllisten für die Aufteilung der eingegangenn Lieferungen auf die Bestellgruppen.
- Für einzelne Bestellungen über Bestellungen > Bestellverwaltung > Bestellung anzeigen > Download > Gruppen/Artikel/Matrix PDF" 
- Für die gesamten Bestellungen eines Abholtags besser über Bestellungen > [Abholtage](/de/documentation/usage/order)

> Die Funktion "Abholtage" muss für dich freigegeben sein - bitte eine Administratorin deiner Foodsoft darum
{.is-warning}

## Beispiel Gruppen PDF

![admin-bestellungen-gruppenpdf.png](/uploads-de/admin_orders_gruppenpdf.png)

## Beispiel Artikel PDF

![admin-bestellungen-artikelpdf.png](/uploads-de/admin_orders_artikelpdf.png)

## Beispiel Matrix PDF

![admin-bestellungen-matrixpdf.png](/uploads-de/admin_orders_matrixpdf.png)

## Beispiel Fax PDF

![admin-bestellungen-faxpdf.png](/uploads-de/admin_orders_faxpdf.png)


# Bestellungen an Lieferung Anpassen

Nicht immer wird genau das geliefert, was bestellt wird. Manchmal sind Artikel nicht mehr oder nur beschränkt verfügbar, oder die Lieferanten irrt sich - so können sowohl mehr als auch weniger Artikel als bestellt geliefert werden. Nur wenn ihr die Foodsoft auch zum Abrechnen verwendet, ist es wichtig, die Bestellungen an die tatsächliche Lieferung anzupassen, damit
- die Rechnung der Lieferantin mit der Bestellsumme in der Foodsoft zusammenstimmt, und
- den Mitgliedern  Beträge von ihrem Guthaben abgebucht werden, die dem entsprechen, was sie tatsächlich bekommen haben.

> Wenn ihr die Foodsoft nicht zum Abrechnen verwendet, könnt ihr diesen Schritt überspringen, und die Bestellung sofort abrechnen. Dieser Schritt ist wichtig, damit Bestellungen als abgeschlossen gelten und von der Foodsoft auch also solche (nicht mehr) dargestellt werden können. Auch wenn ihr euch zu einem späteren Zeitpunkt entscheidet, die Foodsoft doch für die Abrechnung zu verwenden, habt ihr dann einen sauberen Umstieg - sonst müsstet ihr nachträglich alle bisherigen Bestellungen abrechnen.
{.is-info}

## Bestellungen in Empfang nehmen

Die Funktion "In Empfang nehmen" ist so, dass du bei Artikeln, wo eine Anzahl abweichend von der bestellten geliefert wurde, die tatsächlich gelieferte Anzahl in das leere Feld schreibst. Es können auch Dezimalzahlen mit Punkt eingegeben werden (z.B: 3.5 für dreieinhalb Einheiten), wenn die gelieferte Menge von der bestellten abweicht.

Wenn die Bestellmenge mit der Liefermenge übereinstimmt, können die entsprechenden Felder frei gelassen werden. Es empfiehlt sich aber dennoch, alle Felder auszufüllen, da dadurch einfach nachvollziehbar ist, ob alle Mengen kontrolliert wurden.

Wenn die Bestellung komplett ausgefallen ist (z.B. weil die Mindestmenge nicht erreicht wurde), kannst du die Funktion „alle auf Null setzen“ verwenden.

Dann klickst du auf "Bestellung in Empfang nehmen".

Man sieht die bestellten, aber nicht gelieferten Artikel dann nur mehr in der Gruppen-PDF Ansicht.

## Mitglieder-Bestellungen anpassen

Der Vorgang „Bestellung abrechnen“ erfolgt in zwei Stufen, die – leider etwas verwirrend – gleich heißen:

1. **Bestellung zur Abrechnung vorbereiten**: In der Liste “Finanzen \> Bestellung abrechnen” bei der entsprechenden Bestellung auf „abrechnen“ oder den Datumslink klicken. In diesem Schritt bereitest du die Bestellung zur Abrechnung vor, indem du  noch Änderungen an der     Bestellung vornehmen kannst, wie unten beschrieben. Alle Änderungen an der Bestellung werden automatisch gespeichert (keine „Abbrechen“ Funktion\!), es wird aber das Guthaben der Bestellgruppen noch nicht belastet. Du kannst auch öfters zurückkehren und weitere Änderungen vornehmen, solange du nicht den 2. Schritt ausgeführt hast.
2. **Bestellung endgültig abrechnen**: Auf der Seite von Schritt 1 gibt es nochmals die Schattfläche „Bestellung abrechnen“, mit der die Bestellung dann endgültig abgerechnet wird. Damit werden den Bestellgruppen die entsprechenden Beträge von ihrem Guthaben endgültig abgezogen, die Bestellung kann nicht mehr verändert werden, und diese Bestellung kann auch keiner Rechnung mehr zugeordnet werden. 

> *Folgende Schritte überarbeiten...*
{.is-danger}


- Siehe oben Bestellung in Empfang nehmen, oder
- unter “Finanzen \> Bestellung abrechnen”: 
Bestellte Anzahl an gelieferte anpassen (mehr oder weniger Artikel als bestellt wurden geliefert): Bestellung bearbeiten \> Titel des Artikels anklicken \> Im Aufklappmenü Menge bei den Gruppen entsprechend ändern ODER Gruppenansicht \> Anpassen der gelieferten Menge, wenn diese von der Bestellung abweicht
 - Neue Bestellgruppe(n) hinzufügen (es wurde z.B. ein Alternativartikel für nicht gelieferte Produkte geliefert): Bestellung bearbeiten \> Titel des Artikels anklicken \> Im Aufklappmenü “Gruppe hinzufügen”, Anzahl eingeben, bei Bedarf (mehrere Gruppen betroffen) Schritt wiederholen
 - Es können auch Kommazahlen bei “Anzahl” eingeben werden. Das kann genützt werden, um Artikel mit schwankendem Gewicht bzw. Preis abzurechnen:

> **Beispiel: tatsächliches Gewicht bekannt**:
>
>Bestellt werden 2 Stück Krautkopf, in der Foodsofthinterlegt zu je 3,00 € für 2 kg/Stück und 1,50 € pro kg, also gesamt 6,00 € Bekommen: 1,8 kg und 2,5 kg = gesamt 4,3 kg
> - Umrechnung in Stück: 4,3 kg / 2 kg pro Stück = 2,15 Stück
> - Preis wird automatisch zu 2,15 \* 3,00 € = 6,45 €berechnet
{.is-info}

> **Beispiel: tatsächliche Kosten bekannt** 
>
> Bestellt werden 2 Stück Käse, in der Foodsoft hinterlegt zu je 10,00 € für 500 g/Stück und 20 € pro kg, also gesamt 20,00 €
> - Bekommen: 9,50 € und 9,10 € = gesamt 18,60 €
> - Umrechnung in Stück: 18,60 € / 10 € pro Stück = 1,86 Stück
> - Preis wird automatisch zu 1,86 \* 10,00 € = 18,60 € berechnet
{.is-info}

> Zusätzlich muss über *Lieferug in Empfang nehmen* die Gesamtmenge angepasst werden, damit die Abrechnung stimmt.
{.is-info}



## Artikeleigenschaften anpassen

Manchmal ändern sich z.B. Artikelpreise zwischen Bestellung und Lieferung und müssen in der bereits abgeschlossenen, aber noch nicht abgerechneten Bestellung korrigiert werden, damit sie der Rechnung entsprechen. Unter *Finanzen > Bestellungen abrechnen* kannst du jeden Artikel bearbeiten:

- Der Preis ist die einzige Artikeleigenschaft, die für jeden Artikel und jede Bestellung separat abgespeichert wird. Dadurch wirken sich Preisänderungen eines Artikels in einer Bestellung zunächst nicht auf andere Bestellungen aus: 
  - Bei vergangenen Bestellungen soll das ja immer so sein. 
  - Für zukünftige Bestellungen kannst du über die Option „Globalen Preis aktualisieren“ den Preis auch in der Artikelliste der Lieferantin ändern. Wird diese Option nicht angewählt, wird die Änderung nur für die aktuelle Bestellung übernommen und der Preis in der Artikelliste der Lieferantin bleibt unverändert.
  - Alle anderen Artikeleigenschaften wie Name, Einheit usw. können nur global verändert werden, sie ändern sich also sowohl bei vergangenen Bestellungen als auch in der Artikellliste der Lieferantin und damit auch in zukünftigen Bestellungen.

Nur wenn Artikel mit veränderten Eigenschaften in der Artikelliste der Lieferantin als neue Artikel angelegt werden (anstatt die bestehenden zu bearbeiten), werden die Eigenschaften der Artikel in früheren Bestellungen nicht beeinflusst. Die veränderten Artikel sind dann allerdings auch erst bei zukünftig neu angelegten Bestellungen verfügbar. 


## Transportkosten hinzufügen

Manche ProduzentInnen verrechnen pro Lieferung Transportkosten, manchmal auch abhängig von der Bestellsumme. So können die tatsächlich angefallenen Transportkosten für jede Bestellung im Nachhinein gerecht auf alle Bestellgruppen aufgeteilt werden:


1. *Finanzen > Bestellungen abrechnen*
2. Bestellung auswählen
3. rechts oben *Artikel hinzufügen > Transportkosten bearbeiten* 

![admin_finances_order_transportkosten_bearbeiten1.png](/uploads-de/admin_finances_order_transportkosten_bearbeiten1.png)

4. Gesamte Transportkosten für Bestellung eingeben (auch negativer Betrag möglich, falls z.B. zu viel bereits in die Artikelpreise einkalkulierte Transportkosten abgezogen werden sollen)

![admin_finances_order_transportkosten_bearbeiten2.png](/uploads-de/admin_finances_order_transportkosten_bearbeiten2.png)

5. Transportkostenverteilung auswählen:
   1. Kosten nicht auf die Bestellgruppen aufteilen
   2. Jede Bestellgruppe zahlt gleich viel
   3. Kosten anhand der Bestellsumme aufteilen
   4. Kosten anhand der Anzahl an erhaltenen Artikeln verteilen 
6. Speichern
7. *Ansichtsoptionen > Gruppenübersicht*: Anteil an Transportkosten für jede Bestellgruppe wird angezeigt
8. Solange die Bestellung noch nicht abgerechnet wurde, kann der Vorgang ab Schritt 3 wiederholt werden, um Korrekturen vorzunehmen, nachdem die Ansichtsoption wieder auf *Bestellung bearbeiten* zurückgesetzt wurde.

> Wenn die Bestellung über *Finanzen > Bestellungen abrechnen* verändert wird, müssen die Transportkosten neu berechnet werden, da sie nicht automatisch angepasst werden.
{.is-info}

> Wie die Transportkosten bei der Anzeige von Rechnungen berücksichtigt werden, findest du unter [Rechnungen](/de/documentation/admin/finances/invoices).
{.is-info}


> Der Fehler, dass Transportkosten den Mitgliedern beim Abrechnen aufgrund eines Fehlers nicht von ihren Konten abgebucht wurden (siehe https://github.com/foodcoops/foodsoft/issues/861), wurde am 20.10.2021 behoben. Transportkosten, die vor diesem Datum angelegt wurden, müssen vor dem Abrechnen der Bestellung nochmal bearbeitet werden, damit sie beim Abrechnen korrekt berücksichtigt werden.
{.is-success}


# Bestellung abrechnen

Beim Bestellen werden die Beträge den Bestellgruppen noch nicht von ihren Konten abgebucht, es verringern sich zunächst nur die verfügbaren Guthaben. Erst beim Abrechnen einer Bestellung werden die Beträge für diese Bestellung den Bestellgruppen von ihren Foodsoft-Konten abgebucht. Nur vorher können noch Anpassungen durchgeführt werden, wenn es z.B. bei der Lieferung Abweichungen zur Bestellung gibt. Weiters sollte die Rechnung des Produzenten angelegt und mit der Bestellung verknüpft werden, um vergleichen zu können, ob sich die Geldbeträge von Rechnung und Bestellung decken.

Die Bestellung sollte erst abgerechnet werden, wenn auch die [Rechnung](/de/documentation/admin/finances/invoices) angelegt und idealerweise auch bezahlt oder zumindest zur Bezahlung freigegeben wurde.

> Sobald eine Bestellung abgerechnet wurde, kann keine Rechnung mehr für
> diese Bestellung angelegt werden. Es kann zwar eine Rechnung erstellt
> werden, aber die bereits abgrechnete Bestellung kann nicht mehr ausgewählt werden, um mit der Rechnung verknüpft zu werden.
{.is-warning}

> In der .at-Testinstanz [foodsoft-demo](/de/documentation/admin/foodsoft-demo) ist möglich, auch nach abgerechneter Bestellung noch eine  Rechnung dazu anzulegen (2.10.2021 Mirko)
{.is-success}


## Eine Bestellung abrechnen

1. Menü Finanzen > Bestellungen abrechnen
1. Abzurechnende Bestellung aus der Liste suchen, in dieser Zeile den Link der Lieferantin oder "abrechnen" anklicken
1. Bestellung abrechnen
1. Bestätigen (kein Zurück!)

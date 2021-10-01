---
title: Bankkonto mit Foodsoft verknüpfen
description: Menü Finanzen > Bankkonten
published: true
date: 2021-10-01T15:33:40.921Z
tags: 
editor: markdown
dateCreated: 2021-04-20T23:17:42.160Z
---

<h1 id="bankkonteinleit" class="toc-header"><a class="toc-anchor" href="#bankkonteinleit"></a>Einleitung</h1>

<h2 id="bankkonteinleit-warum" class="toc-header"><a class="toc-anchor" href="#bankkonteinleit-warum"></a>Was ermöglicht die Bankanbindung?</h2>

Die Foodcoop bietet die Option einer Bankanbindung. Wenn eingerichtet, ermöglicht dies der Foodsoft einen Zugriff auf die Transaktionshistorie der Vereinskonten. Dies bietet folgende Vorteile:
- Überweisungen der Mitglieder\*innen auf das Vereinskonto können vom System automatisiert erkannt und den Bestellgruppen zugeordnet werden. So entfällt der manuelle Prozess das Kontoblatt einzusehen um z.B. Einkaufsguthaben oder Mitgliedsbeitrag den Bestellgruppen gut zu geschreiben. Für diese Funktion müssen die Mitglieder\*innen bei Überweisungen die Zahlungsreferenz (siehe Zahlungsreferenz-Rechner) eintragen.
  - Überweisungen von Rechnungen an die Lieferanten können von der Foodsoft erkannt, zugeornet und als bezahlt („Bezahlt am“-Feld) markiert werden.   Für diese Funktion muss das IBAN-Feld der Lieferanten befüllt sein. Die Foodsoft vergleicht IBAN, Rechnungsnummer und Betrag der Kontotransaktionen mit den Rechnungen
  - Es werden interne Querverweise genannt Finazlink (teilweise) automatisch erstellt. Dies ermöglicht es Buchungen zu verknüpfen um diese jederzeit nachvollziehbar zu gestalten.
  - Werden alle Banktransaktionen, Kontotransaktionen und Rechnungen mit einem Finanzlink verknüpft lässt sich eine nachvollziehbare (einfache) doppelte Buchhaltung umsetzten.
    - Dies spart eine externe Buchungssoftware bzw. redudantes mitschreiben.
    - In Verknüpfung mit Trennung in Kontotransaktoionstypen wie etwa Treuhand und Verein ermöglicht dies eine saubere Buchhaltung mit nur einem Vereinskonto
  - Es werden auch mehrere Vereinskonten unterstützt. 

> Die Foodsoft kann keine Transaktionen am Bankkonto selbst tätigen. Die  hierfür erforderliche Funktionialität wird gerade entwickelt (Stand  16.02.2021). 
{.is-info}


<h2 id="bankkonteinleit-suppbanken" class="toc-header"><a class="toc-anchor" href="#bankkonteinleit-suppbanken"></a>Unterstützte Banken</h2>

Die Bankkontozeilen werden je nach Bank und Unterstütztung der Bankanbindung händisch/halbautomatisch oder automatisiert importiert. 

Für folgende Banken unterstützt die Foodsoft eine Bankanbindung:


<h3 id="bankkonteinleit-suppbanken-vollauto" class="toc-header"><a class="toc-anchor" href="#bankkonteinleit-suppbanken-vollauto"></a>Vollautomatisch </h3>

> Synchronisation zwei mal Täglich um 08:00 und 18:00
{.is-info}
- Erste Bank Sparkasse (George)


<h3 id="bankkonteinleit-suppbanken-halbauto" class="toc-header"><a class="toc-anchor" href="#bankkonteinleit-suppbanken-halbauto"></a>Halbautomatisch </h3>

> Auslösen durch Mitglied mit Finanzzugriff via:  Menü Finanzen \> Bankkonten \> „Importieren“-Schaltfläche. Zweifaktoratentifizierung erforderlich.
{.is-info}
- Raiffeisen, Umweltcenter Gunskirchen
- Holvi
- Oberbank
- Sparda
- Bawag, Easybank: muss erst adaptiert werden bei Bedarf

> Falls die Bank deiner Foodcoop hier nicht vorkommt, wende dich bitte im Forum an @paroga. Bitte diese Liste ergänzen, falls eine  neue Bank hinzugefügt wurde.
{.is-warning}

<h3 id="bankkonteinleit-suppbanken-nicht" class="toc-header"><a class="toc-anchor" href="#bankkonteinleit-suppbanken-nicht"></a>Nicht unterstützte Banken </h3>

Banken, die von FC verwendet werden, wo es noch keine Anbinung gibt:
- *Bank Austria (prESSBAUM)*
- *Bawag (EKG Linz)*


<h2 id="bankkonteinleit-finanzlinks" class="toc-header"><a class="toc-anchor" href="#bankkonteinleit-finanzlinks"></a>Finanzlinks</h2>

Bankkontobuchungen können verknüpft werden mit
- Foodsoft Kontotransaktionen
- Rechnungen
- anderen Bankkontobuchungen

Diese Links werden großteils automatisch von der Foodsoft erstellt, in Einzelfällen kann es sinnvoll/notwendig sein, sie händisch zu erstellen bzw. zu bearbeiten.

<h2 id="bankkonteinleit-zahlrefc" class="toc-header"><a class="toc-anchor" href="#bankkonteinleit-zahlrefc"></a>Zahlungsreferenzcodes</h2>

Jedes Mitglied findet seinen Zahlungsreferenz-Rechner im Dropdownmenü des Profilnamens. Der Menüpunkt wird aber erst angezeigt, sobald [*Kontotransaktion Klassen und Typen*](#_h1llhyas485l) mit zumindest einem Kürzel eines Transaktionstyps angelegt wurden, mindestens ein Bankkonto hinzugefügt wurde, und du danach aus der Foodsoft aussteigst und wieder neu einloggst. Der Zahlungsreferenz-Rechner verwendet die Kürzel der Transaktionstypen für die Generierung des Codes, indem für jedes Kürzel ein Feld für einen Geldbetrag angezeigt wird.


<h1 id="bankkeinrichten" class="toc-header"><a class="toc-anchor" href="#bankkeinrichten"></a>Bankkonto einrichten</h1>

Um ein Bankkonto zu Verknüpfen ist eine Berechtigung als Administrator erforderlich. Im Menü auf **Administration \> Finanzen** die Schaltfläche „Neues Bankkonto anlegen“ wählen. Ein Dialofenster öffnet sich mit den selbsterklärenden Feldern 
- Name\*, 
- IBAN\*, 
- Beschreibung 
- Kontostand: hier einmalig den aktuellen Kontostand des Bankkontos eingeben. Dieser wird benötigt um aus den zukünftigen Transaktionen den aktuellen Kontostand in der Foodsoft anzeigen zu können
- .

Mit „Bank account erstellen“ wird das Konto in der Foodsoft angelegt. 

<h1 id="bankkeinrichtenimport" class="toc-header"><a class="toc-anchor" href="#bankkeinrichtenimport"></a>Bankkontozeilen importieren und weiterverarbeiten</h1>


<h2 id="bankkeinrichtenimport-import" class="toc-header"><a class="toc-anchor" href="#bankkeinrichtenimport-import"></a>Import</h2>
1.  Finanzen \> Bankkonten \> Importieren: Ebanking Zugangsdaten bei Disposer-Nr. und PIN eingeben; ![](Pictures/1000020100000181000001B8B44E18814C6D14C7.png) Mit der Option „Remember“ merkt sich der Browser deine Zugangsdaten, und du brauchst sie beim nächsten Mal nicht mehr einzugeben.
2.  Es sollte in deiner Bank-App am Smartphone eine Anfrage für eine Freigabe mit einem 4-stelligen Buchstaben/Zahlencode erscheinen, der auch in der Foodsoft angezeigt wird. Diese Freigabe bitte im Bank-App erteilen durch Eingabe deines Codes oder Fingerabdrucks.
3.  Neue Kontozeilen werden in die Foodsoft importiert. Die Buchungszeilen werden zunächst noch nicht bearbeitet, es finden während des Imports keine Foodsoft-Transaktioktionen für Mitglieder statt, es werden keine Rechnungen als bezahlt markiert, und noch keine Finanzlinks erstellt, erkennbar an den grünen Schaltflächen in der Spalte Finanzlink „Hinzufügen“:
![](Pictures/10000201000000480000001B2374D176D93924A2.png)
4.  Finanzen \> Bankkonten \> Transaktionen zuordnen: durch diese Funktion werden Foodsoft Transaktionen auf Basis der Zahlungsreferenzcodes in den Überweisungen durchgeführt, Rechnungen als bezahlt markiert und die neu importierten Kontozeilen mit Finanzlinks den enstprechenden Transaktionen und Rechnungen zugeordnet, wie im Folgenden beschrieben. 


<h2 id="bankkeinrichtenimport-zuord" class="toc-header"><a class="toc-anchor" href="#bankkeinrichtenimport-zuord"></a>Transaktionen zuordnen</h2>

Automatische Erstellung eines Finanzlinks, Guthaben aufladen, Rechnungen als bezahlt kennzeichnen

Finanzen \> Bankkonten \> Transaktionen zuordnen:

In folgenden Fällen wird mit der Funktion „Transaktionen zuordnen“ ein Finanzlink für Kontonbuchungen erstellt: 
- Buchung enthält **Zahlungsreferenzcode**: es wird eine entsprechende Foodsoft Kontotransktion durchgeführt, indem der entsprechenden Bestellgruppe der Betrag / die Beträge gutgeschrieben werden
- Buchung kann einer Rechnung zugeordnet werden: die **Rechnung wird als bezahlt markiert**, siehe unten. 

Falls eine Buchung nicht erkannt wird (z.B. weil Zahlungsreferenzcode fehlerhaft oder Rechnungsdaten stimmen nicht überein), erfolgt keine Aktion, die grüne Schaltfläche „Hinzufügen“ unter Finanzlinks bleibt erhalten. 


<h2 id="bankkeinrichtenimport-manerstbearb" class="toc-header"><a class="toc-anchor" href="#bankkeinrichtenimport-manerstbearb"></a>Manuelle Erstellung oder Bearbeitung eines Finanzlinks</h2>

Wenn in einer Buchung kein oder ein fehlerhafter (z.B. Tippfehler, ungültige Modifizierung des Codes durch Mitglied, Überweisung mittels Papier-Zahlschein, ...) Zahlungsreferenzcode vorhanden ist, muss manuell ein Finanzlink erstellt und eine Foodsoft-Kontotransaktion (Aufbuchen des Guthabens auf das entsprechende Foodosoft-Bestellgruppenkonto) erstellt werden. Ebenso kann bei Rechnungen z.B. durch abweichende Rechnungsbeträge, abweichende IBAN oder abweichende Zahlungsreferenz die Zuordnung fehlschlagen, sodass ein Finanzlink manuell erstellt und die Rechnung manuell als bezahlt markiert werden muss. Außerdem kann ein bestehender Finanzlink auch erweitert werden, z.B. falls die Zahlung einer Rechnung in mehreren Überweisungen erfolgte und daher einer Rechnung mehrere Banktransaktionen zuzuordnen sind. 

Folgend Funktionen stehen unter Finanzen \> Bankkonten in der Spalte Finanzlink über die Schaltfläche „Hinzufügen“ oder den Link „Anzeigen“ zur Verfügung:
- **Banktransaktion hinzufügen**: eine weitere Bankkontobuchung verknüpfen, z.B. wenn eine Rechnung in mehreren Teilbeträgen bezahlt wurde. 
- **Kontotransaktion hinzufügen**
  - Neu Kontotransaktion hinzufügen: es wird eine Foodsoft-Konotransakttion und der Finanzlink dazu erstellt. Anwedung z.B. wenn kein oder ein fehelrhafter Zahlungsreferenzcode vorliegt. Die Bestellgruppe wird wenn möglich aus dem IBAN vorausgewählt, falls es bereits vorher schonmal eine Zuordnung gab. Es können auch mehrere Transaktionen hintereinander z.B. für verschiedene Transaktionsklassen für Guthaben Bestellungen/Mitgliedsbeitrag erstellt werden, bei jeder weiteren Transaktion erscheint automatisch der noch nicht verbuchte Rest des Überweisungsbetrags.
- **Rechnung hinzufügen: **aus der Liste der Rechnungen auswählen

<h2 id="bankkeinrichtenimport-rechn" class="toc-header"><a class="toc-anchor" href="#bankkeinrichtenimport-rechn"></a>Foodsoft Rechnungen</h2>

Automatisch mit Finanzen \> Bankkonten \> Import \> Transaktionen zuordnen:
- Transaktion wird mit Rechnung verknüpft
- Rechnung wird als bezahlt mit entsprechendem Datum markiert und verschwindet damit aus der Liste Finanzen \> Übersicht \> unbezahlte Rechnungen

Was wird genau überprüft und muss ident sein, damit die Überweisung einer Foodsoft-Rechnung zugeordnet wird:

1.  Anhand der **IBAN** der LieferantIn werden offenen Rechnungen gesucht. Die IBAN muss in der Foodsoft unter Artikel \> Lieferanten bei der jeweiligen Lieferantin unter Bearbeiten im Feld IBAN eingegeben sein.
2.  Für jede **Rechnungsnummer** der Rechnung wird geprüft, ob diese im Verwendungszweck vorkommt.
3.  Wenn die Summe der "passenden" Rechnungen mit dem **Überweisungsbetrag** übereinstimmt, wird eine Finanzlink angelegt und die Rechnungen als bezahlt markiert.

**Beispiel zur Automatischen Erkennung von Rechnungsnummern** 

Angenommen, es gibt Rechnungen mit folgenden Rechnungsnummer:

a) "1"

b) "3"

c) "2020-10"

d) "\#789"

Die folgende Verwendungszwecke würde folgende Rechnungen matchen:

"1"         (a)

"Rechnung 1" (a)

"Re-Nr. \#1" (a)

"Irgendwas 123" (a) und (b)

"ReNr: 1, 3" (a) und (b)

"Nr 333"    (b)

"2020-10"   (a) und (c)

"\#789"      (d)

"789"       nichts

Leerstellen in der Rechnungsnummer sollten kein Problem sein, z.B. Rechnungsnummer in der Foodsoft "2020-1 bis 3", Überweisung mit Zahlungsreferenz "Rechnungen 2020-1 bis 3" ok.

Bei **mehreren unbezahlten Rechnungen desselben Produzenten** wird eine Summe der Rechnungen angezeigt. Diese Summe kann mit einer einzigen Überweisung bezahlt werden, die einzelnen Rechnungsnummern sind beim Verwendungszweck alle anzugeben. Die Rechnungen werden als bezahlt markiert und alle der Sammelüberweisung zugeordnet. 

Falls die automatische Zuordnung nicht erfolgreich war, weil eines oder mehreres der oben angeführten Kriterien nicht erfüllt war, sollten ersatzweise folgende Schritte zur **manuellen Zuordnung **durchgeführt werden:

1.  Finanzen \> Bankkonten \> Buchungszeile für Rechnung \> Finanzlink hinzufügen \> Rechnung(en) hinzufügen \> entsprechende Rechnung in der Liste auswählen (eventuel Fenster vergrößern oder mit F11 auf Vollbild schalten um „Speichern“ Schaltfläche anzuzeigen); Schritt mehrmals ausführen wenn mehrere Rechnungen zu verknüpfen sind
2.  Finanzlink anzeigen \> Rechnung auswählen \> Bearbeiten \> Datum bei bezahlt am“ eingeben
3.  Finanzen \> Überblick \> unbezahlte Rechnungen: prüfen, ob die manuell als bezahlt gekennzeichnete Rechnung dort nicht mehr aufscheint 

<h2 id="bankkeinrichtenimport-sonsttrans" class="toc-header"><a class="toc-anchor" href="#bankkeinrichtenimport-sonsttrans"></a>Sonstige Bankkonto-Transaktionen</h2>

Zusätzlich zu den bisher genannten Bankkonto-Transaktionen gibt es noch welche, die weder unter Guthaben Aufladen noch Porduzentinnen Rechnungen fallen, zum Beispiel:

- Bankspesen
- Lagerraum: Miete, Strom, Heizung, Internet, Versicherung, …
- Anschaffungen: Inventar, Vebrauchsmaterial wie Glühbirne usw.
- …

Oft handelt es sich hier um Einzieher, das heißt es werden monatlich, quartalsweise oder jährlich fixe Beträge vom Bankkonto der Foodcoop eingezogen. Um für eine korrekte Buchhaltung diesen Buchungen über Finanzlinks auch Rechnungen zuordnen zu können, ist es sinnvoll, für diese Transaktionen auch eigene Lieferantinnen und Rechnungen anzulegen, z.B:

- Wohnungsgenossenschaft: Einzug der monatlichen Miete des Lagerraums
- Stromlieferantin für Lagerraum: monatlicher Einzug der Vorschreibung
- Bank für quartalsweisen Abzug der Kontoführungsgebühren
- Sonstiges für nicht regelmäßge Aufgaben 

**Beispiel**: die Wohungsgenossenschaft, die den Lagerraum vermietet, bucht monatlich 200 Euro Miete vom Bankkonto der Foodcoop ab. 

1. In der Foodsoft wird eine **Lieferantin** „Wohnungsgenossenschaft“ angelegt der Kategorie „Betriebskosten“.
2. Nach Ablauf eines Jahres erstellt die FC in der Foodsoft eine (fiktive) Jahres-**Rechnung** für die Lieferantin „Wohnungsgenossenschaft“ über 12 x 200 = 2.400 Euro mit Rechnungsdatum = bezahlt-am-Datum = Enddatum des Rechnungszeitraums sowie einer Rechnungsbetreff z.B. für den Zeitraum („Oktober 2019 bis September 2020). Noch besser wäre es, die Jahresabrechnung und deren Zeitraum zu verwenden. 
3.  Unter *Finanzen \> Bankkonten* bei einer der 12 Abbuchungen (noch ohne Finanzlink) „hinzufügen“, Rechnung hinzufügen, die soeben erstellte Rechnung auswählen, dann 
4.  mit *Banktransaktion hinzufügen* die restlichen 11 Abbuchungen ebenfalls dem selben **Finanzlink zuweisen**. 

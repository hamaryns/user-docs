---
title: Rechnungen
description: Rechnungen von Liefernden digital ablegen und mit Bestellungen verknüpfen
published: true
date: 2021-10-18T09:06:12.278Z
tags: 
editor: markdown
dateCreated: 2021-04-20T23:05:17.349Z
---

Die Funktion “Rechnung” dient dazu, Rechnungen von Produzentinnen in die Foodsoft zu übertragen und sie mit den entsprechenden Lieferungen und Bestellungen zu vergleichen. Rechnungen scheinen zunächst unter den “unbezahlten Rechnungen” auf, und werden als bezahlt markiert, sobald ein entsprechender Zahlungsausgang am Foodsoft-Bankkonto auftritt. Rechnungen können in Papierform oder digital als PDF oder JPG vorliegen. 


# Rechnung anlegen


Eine neue Rechnung kann angelegt werden unter
- *Finanzen \> Rechnungen \> Neue Rechnung anlegen*
- *Finanzen \> Bestellungen abrechnen \> Bestellung auswählen \> Rechnung anlegen*
- *Bestellverwaltung \> beendete Bestellung auswählen \> Rechnung anlegen*
- *Artikel \> Lieferant \> Bestellung \> Rechnung anlegen*
- *Artikel \> Lieferant \> Letzte Lieferungen \> Rechnung anlegen*
- *Artikel \> Lager \> neue Lieferung ... > Rechnung anlegen*

> Empfehlung: Rechnungen, die in Papierform vorliegen, gehen einfacher mit einem Smartphone oder Tablet mit Kamerafunktion einzugeben. Sobald ein Rechnungsdatum eingegeben ist, kann die Eingabe jederzeit unterbrochen, die Rechnung unfertig gespeichert werden, um auf einem anderen Gerät fortgesetzt werden. Wichtig ist es, vor dem Speichern bei **Rechnungsdatum** das Datum der Rechnung (oder zumindest das aktuelle Datum) einzugeben, weil sie sonst schwer auffindbar ist. 
{.is-info}

Hier ein Beispiel für eine Papierrechnung und die entsprechenden Eingaben in der Foodsoft, wie im Folgenden im Detail beschrieben.

![rechnung-beispiel-fs.png](/uploads-de/admin_finances_invoices_rechnung-beispiel-fs.png)

In der neuen Rechnung ist anzugeben:

## Lieferant

Lieferantin auswählen.

> Wenn die Liste der Lieferantinnen recht lang ist, kannst du den ersten Buchstaben der Lieferantin tippen, um sie schneller zu finden.
{.is-info}


## Bestellungen und Lieferungen mit Rechnung verknüpfen

In den Feldern **Lieferung** und **Bestellung** solltest du jene Lager-Lieferung(en) und/oder jene Bestellung(en) auswählen, für die die Rechnung ausgestellt wurde. Damit ist klar, ob die Lieferantin für eine Lieferung/Bestellung eine Rechnung ausgestellt hat, und der Rechnungsberag kann mit dem Guthaben, das den Mitgliedern abgebucht wird (bzw. das als Warenwert ins Lager eingegangen ist), verglichen werden. Dies ist die einzige echte Kontrollmöglichkeit, um zu schauen, dass die Foodcoop keinen Verlust, aber auch keinen unerwünschten Gewinn macht - daher ist dieser Schritt sehr wichtig.

![rechnung-bestellung-lieferung.png](/uploads-de/admin_finances_invoices_rechnung-bestellung-lieferung.png =400x)
    
-  **[Lieferung](./Lager)**: **bei Rechnung für eine Bestellung leer lassen**. Wenn für diesen Produzenten [Lagerartikel](./Lager) über die Funktion *Artikel > Lager > neue Lieferung* eingebucht  wurden, die noch keiner Rechnung zugeordnet sind, können diese  hier ausgewählt werden. Mehrere Lieferungen können dabei in  einer gemeinsamen Rechnung ausgewählt werden.
-  **[Bestellung](./Bestellung)**: wenn es für diesen Produzenten abgeschlossene, aber noch nicht abgerechnete Bestellungen gibt, die noch keiner Rechnung zugeordnet sind, können diese hier ausgewählt werden. Mehrere Bestellungen können dabei in einer gemeinsamen  Rechnung ausgewählt werden.
    
> Angezeigter **Betrag** für Bestellung(en) und Lieferung(en)
> ist der Bruttobetrag (inkl. Mwst und Pfand)
{.is-info}

    
> Angezeigtes **Datum** für Bestellung(en) und Lieferung(en) ist jenes, an dem die Bestellung endete (nicht Liefer- oder  Abholdatum\!)
{.is-info}

> Es können mehrere Bestellungen und/oder Lieferungen ausgewählt werden, wenn dafür von der Lieferantin eine gemeinsame Rechnung gestellt wurde.
{.is-info}


> Eine Bestellung oder Lieferung kann nur einmal einer Rechnung zugeordnet werden. Wenn schon eine Rechnung angelegt und Bestellungen und/oder Lieferungen zugeordnet wurden, daher unbedingt diese suchen (siehe Rechnungsdatum) und bearbeiten, statt sie nochmal neu anzulegen. 
{.is-warning}

> Wenn eine Bestellung neben den Bestellungen für die Foodcoop Mitglieder auch eine Lagerbestellung enthält, und diese Lagerartikel dann mit einer Lieferung in den Lagerstand eingebracht werden, und sowohl die Bestellung als auch die Lieferung der Rechnung korrekter weise zugeordnet wird, würden sie bei der Rechnungsbilanz doppelt berücksichtigt - siehe [Lager](/de/documentation/admin/storage)
**Anschauen in Demoinstanz**: Bestellung, Bestellung+Lager,  Bestellung+Lager+Lieferung, Bestellung+Lieferung, Lieferung - was wird jeweils bei *Total* berücksichtigt und was bei der Differenz in *Unbezahlte Rechnungen?*
{.is-danger}


## Nummer

Rechnungsnummer von Rechnung übernehmen. Die Rechnungsnummer wird bei der Banküberweisung von der Foodsoft (oder von der Person, die in der Foodcoop die Rechnungen via Ebanking manuell bezahlt) in den Verwendungszweck eingetragen, und dient sowohl der Foodsoft als auch der Lieferantin zur eindeutigen Zuordnung der Rechnung. 

> Das Feld *Rechnungsnummer* ist ein Textfeld und kann neben Zahlen auch Buchstaben und Leerzeichen enthalten.
{.is-success}

> Falls auf der Rechnung keine Rechnungsnummer aufscheint, selbst eine (in Bezug auf die Lieferantin) eindeutige Rechnungsnummer erstellen, z.B. aus dem Datum, also z.B. `20210527` oder `2021-05-27` oder `270521`. Im Gegensatz zum Feld *Rechnungsdatum* ist hier das Datumsformat egal, weil die Rechnungsnummer nur ein Textfeld ist, und die Foodsoft die Eingabe nicht als Datum interpretiert. 
{.is-info}




## Rechnungsdatum

Von Rechnung übernehmen. Wenn nicht bekannt, das Datum der Lieferung (eruierbar z.B. aus der ausgewählten Bestellung) oder das aktuelle Datum eingeben.

Für die Eingabe des Datums gibt es folgende alternative Möglichkeiten:
1. Über die **Kalenderfunktion**: ins Eingabefeld klicken, es erscheinent ein Kalender, das aktuelle Datum ist gelb hinterlegt. Auf das gewünschte Datum klicken, wodurch dieses blau wird und im Eingebefeld erscheint. Diese Art ist auf mobilen Geräten aufgrund des kleinen Displays oft schwierig anzuwenden. ![admin_finances_invoices_date.png](/uploads-de/admin_finances_invoices_date.png)
1. **Eingabe im Textfeld genau im Format** `2021-09-30` (also zuerst Jahr 4-stellig, Bindestrich, in der Mitte Monat zweistellig ggf. mit führender Null, Bindestrich, am Ende Tag zweistellig ggf. mit führender Null). 

> Wenn das Datum im falschen Format eingegeben wird, interpretiert die Foodsoft das Datum und insbesondere das Jahr falsch, und die Rechnung ist nachher scheinbar verschwunden, weil die Rechnungen nach Datum sortiert werden (neuerste zuerst). Die Eingabe von `30.9.2021` ergibt z.B. `36-03-13`, also das Datum 13. März im Jahr 36 n.Chr., und die Rechnung wird ganz ans Ende der Liste gereiht.
{.is-warning}


> Auch wenn dieses Feld leer gelassen wird, erscheint die Rechnung ganz am Ende der Liste der Rechnungen, statt am Anfang, wo neue Rechnungen sonst zu finden sind. 
{.is-warning}



## Bezahlt am

### Rechnung noch unbezahlt

**Leer lassen**, wenn die Rechnung noch nicht bezahlt wurde. Die Rechnung scheint in der Foodsoft in der Liste "unbezahlte Rechnungen" auf. Die Person in deiner Foodcoop, die einen Bankkontozugang hat und die Überweisung der Rechnungen durchführt, weiß damit, dass diese Rechnung zu zahlen ist.  Wenn das Bankkonto der Foodcoop mit der Foodsoft verbunden ist, wird die Foodsoft hier automatisch das Datum des Zahlungsausgangs eintragen, und die Rechnung ist dann damit als bezahlt gekennzeichnet werden.

### Rechnung bereits bezahlt

Falls die Rechnung schon bezahlt wurde, das Datum eintragen, an dem dies erledigt wurde. Die Rechnung scheint dann **nicht** unter "unbezahlte Rechnungen" auf.  Die Person in deiner Foodcoop, die einen Bankkontozugang hat und die Überweisung der Rechnungen durchführt, weiß damit, dass diese Rechnung nicht mehr zu zahlen ist.


## Betrag

Rechnungsbetrag (inklusive [Mehrwertsteuer](/de/documentation/admin/finances/value-added-tax)) von der Rechnung übernehmen. Als Dezimaltrennzeichen kann dabei Komma oder Punkt verwendet werden, also für eine Rechnugssumme von z.B. 1.257,87 € entweder `1257,87` oder `1257.87` - angezeigt wird der Betrag dann in Folge mit einem Punkt als Dezimaltrennzeichen.

## Pfand berechnet

Leer lassen, falls in den Artikeln der Foodsoft ein Pfandbetrag bereits inkludiert ist, weil Bestellungen und Lieferungen nicht pfandbereinigt werden. Falls sich Pfand in der Foodsoft und auf der Rechnung des Produzenten nicht decken, kann hier die Differenz eingegeben werden: 
- (Pfand gesamt Produzent) - (Pfand gesamt Foodsoft). 
    
    
### Beispiele

Für 3 Flaschen und 50 Cent Pfand pro Flasche:
- Foodsoft-Artikel enthält 50 Cent Pfand pro Flasche, Produzent verrechnet ebenfalls 50 Cent pro Flasche, Differenz = 3 \* 0,50 - 3 \* 0,50 = **0 €**
- Foodsoft-Artikel enthält 50 Cent Pfand pro Flasche, Produzent verrechnet nur 10 Cent pro Flasche, Differenz = 3 \* 0,10 - 3 \* 0,50 = 3 \* (0,10-0,50) = **-1,20 €**
- Foodsoft-Artikel enthält 50 Cent Pfand pro Flasche, Produzent verrechnet kein Pfand, Differenz = 0 - 3 \* 0,50 = **-1,50 €** 
- Foodsoft-Artikel enthält kein Pfand, Produzent verrechnet 50 Cent pro Flasche, Differenz = 3 \* 0,50 - 0 = **+1,50 €**

Siehe auch [Pfand in Foodcoops](/de/documentation/admin/finances/deposits)

## Pfand gutgeschrieben

Pfandgutschrift des Produzenten Brutto (inkl. Mwst) **als positiven Wert** eintragen wie auf der Rechnung ausgewiesen, sofern im Rechnungsendbetrag berücksichtigt.

> Manche Lieferantinnen führen die Pfandgutschrift netto an. In diesem Fall musst du die Mehrwertsteuer noch dazurechnen. 
{.is-warning}


> Kann auch  für andere Gutschriften (z.B. Skonto) verwendet werden, die in den   Foodsoft-Bestellungen nicht berücksichtigt sind.
{.is-info}


## Anhang

Foto der Papierrechnung im JPEG Format oder PDF-Rechnungsdatei hochladen. Es kann nur eine Datei pro Rechnung hochgeladen werden. 

Falls die Rechnung aus mehreren Seiten bzw. Dokumenten besteht, müssen diese vorher zu einer Datei zusammengfügt werden. Tipps für Programme, mit denen das geht:
- PDF-Dateien 
  - https://pdfsam.org/
- JPEG-Bilder 
  - alle Seiten auf einmal fotografieren
  - im Bildbetrachter mehrer Bilder in eine PDF-Datei drucken (Drucker *in Datei drucken* auswählen)
  - https://imagemagick.org/ Kommandozeilenbefehl Beispiel für Zusammenfügen von 3 Bildern nebeneinander (3x1) in Originalgröße (100%): `montage -geometry 100% -tile 3x1 img1.jpg img2.jpg img3.jpg merged.jpg`
    
> Auf Smartphones oder Tablets kann oft direkt die Kamera das Geräts ausgewählt und eine Foto der Rechnung aufgenommen und hochgeladen werden. 
{.is-info}


## Notiz

Empfehlung, dass hier der Status der Rechnung kommentiert wird (kann bezahlt werden, oder es muss z.B. noch auf eine Anpassung an die Lieferung gewartet werden) und etwaige Differenzen zwischen Bestellung und Rechnung dokumentiert und erklärt werden (Vorschlag: “Differenz X,XX Euro zugunsten/zulasten der Foodcoop aufgrund ...”). Kann zunächst leer gelassen und später noch bearbeitet werden.


## Transportkosten

Wenn die Rechnung extra ausgewiesene Transportkosten enthält, können diese auf die Bestellung aufgeschlagen werden, sodass die Transportkosten auch von den Bestellgruppen anteilsmäßig übernommen werden. Siehe [Bestellungen > Transportkosten](/de/documentation/admin/orders).


# Rechnung anzeigen und bearbeiten

Um eine bereits angelegte Rechnung anzuzeigen: 
- *Finanzen \> Rechnungen*: Die Rechnungen sind nach Rechnungsdatum sortiert, beginnend mit aktuellen. Diese Rechnung sollte hier auch dann zu finden sein, wenn die Rechnung schon als bezahlt markiert wurde (= Datum bei "bezahlt am" eingegeben)
>  Wenn ein falsches Datum in der   Vergangenheit eingegeben wurde, kann es sein, dass die Rechnung sehr  weit hinten zu finden ist. Wie du sie in so einem Fall wieder findest, um das Datum richtig zu stelln, ist im nächsten Abschnitt beschrieben.
{.is-warning}


- *Finanzen \> Übersicht \> unbezahlte Rechnungen*: hier scheint die Rechnung nur dann auf, wenn kein Datum bei “bezahlt am” eingegeben wurde, unabhängig davon, ob die Rechnung auch wirklich bezahlt wurde\!

Um eine bereits angelegte Rechnung zu bearbeiten: zunächst wie oben beschrieben anzeigen und dann “bearbeiten” auswählen. Zusätzlich gibt es noch die Möglichkeit über *Finanzen \> Bestellungen abrechnen \> Bestellung auswählen \> Rechnung bearbeiten*.

## Verschollene Rechnung finden und wiederherstellen

Es gibt folgende Möglichkeiten, eine bereits angelegte Rechnung wieder zu finden, die in der Liste der Rechnungen nicht dort aufscheint, wo sie sein sollte: 

1. Gehe auf die letzte Seite der Rechnungsliste mit der Schaltfläche `>>`, wo du sie finden solltest
1. Gehe auf *Finanzen \> Übersicht \> unbezahlte Rechnungen*, wo du die Rechnung findest, wenn sie noch nicht bezahlt wurde (d.h. wenn noch kein Datum bei *bezahlt am* eingegeben wurde).
1. Wenn die Rechnung bereits mit einer Bestellung verknüpft wurde: gehe über *Finanzen > Bestellungen abrechnen* (Zugriffsrecht erforderlich) auf die entsprechende Bestellung und klicke hier auf *Rechnung > Rechnung bearbeiten*. 
1. [Exportiere die Liste der Rechnungen über die Schaltfläche *CSV* in eine Datei](/de/documentation/admin/lists), und suche in dieser Datei nach der Rechnung. Dabei kannst du z.B. in einem Tabellenprogramm wie unter dem Link beschrieben einen Filter verwenden, um nur die Rechnungen einer Lieferantin anzeigen zu lassen.

> Wenn du die Rechnung gefunden hast, gib bitte das richtige Datum ein und beachte wie oben unter *Rechnung anlegen* beschrieben, dass das Datumsformat richtig ist.
{.is-info}

# Rechnung prüfen

Unter *Finanzen \> Übersicht \> unbezahlte Rechnung* wir die Differenz zwischen Foodsoft Buchungen von den Mitgliederkonten und dem pfandbereinigten Rechnungsbetrag angezeigt, wenn sie nicht null ist:
- roter minus-Betrag: Foodcoop macht Verlust
- grüner plus-Betrag: Foodcoop macht Gewinn
- kein Differenzbetrag: exakte Übereinstimmung der Beträge

Das Vorzeichen hat sich Anfang März 2021 umgedreht, die Bedeutung der Farben in Bezug auf Verlust/Gewinn für die Foodcoop ist gleich geblieben.


Zusätzlich sind in der Rechnungsansicht noch folgende Details einzusehen:
- **Pfandbereinigter Betrag** = Rechnungsbetrag - Pfand berechnet + Pfand gutgeschrieben
- **Total** = Summe aus Bestellungen und Lieferungen Brutto (inkl. Pfand und Mwst, d.h. nicht Pfand-bereinigt\!), neu seit 2021-01: inklusive Transportkosten (werden bei Bestellung als zusätzlicher Plus-Betrag angezeigt; Transportkosten anlegen: siehe [Bestellungen](/de/documentation/admin/orders), Beispiel für Darstellung siehe unten).

> **Pfandbereinigter Betrag** und **Total** sollten übereinstimmen. 
{.is-warning}

Falls nicht:
- **Pfandbereinigter Betrag **größer als** Total**: Lieferant verrechnet mehr, als den Foodcoop Mitgliedern vom Guthaben abgezogen wird. Die Foodcoop macht Verlust.
- **Pfandbereinigter Betrag **kleiner als** Total**: Lieferant verrechnet weniger, als den Foodcoop Mitgliedern vom Guthaben abgezogen wird. Die Foodcoop macht “Gewinn”.

> Unter *Finanzen > Bestellungen abrechnen* findest du ebenfalls eine Gegenüberstellung von Bestellung und Rechnung, die allerdings nur dann brauchbar ist, wenn es genau eine Bestellung gibt, die der Rechnung zugeordnet wird. Werden mehrere Bestellungen zugeordnet, wird immer nur die aktuelle Bestellung mit der gesamten Rechnung verglichen.
{.is-warning}



## Transportkosten in Rechnungen
Beispiel:
- 19,20 Euro Bestellbetrag
- 10 Euro Transportkosten 
- 30 Euro Rechnungsbetrag (inkl. Transportkosten)

> Beim Erstellen oder Bearbeiten der Rechnung beim Auswählen der Bestellung scheinen die Transportkosten zunächst nicht auf, wenn sie vorher schon [zur Bestellung hinzugefügt wurden](/de/documentation/admin/orders): 
{.is-warning}

![admin_finances_order_transportkosten_rechnung_bearbeiten.png](/uploads-de/admin_finances_order_transportkosten_rechnung_bearbeiten.png)

> Transportkosten werden bei der Rechnungsbilanz beim Betrag der Bestellung berücksichtigt unter *Rechnung Detailansicht*, *Unbezahlte Rechnungen* :  
{.is-success}

![admin_finances_order_transportkosten_rechnung.png](/uploads-de/admin_finances_order_transportkosten_rechnung.png)
![admin_finances_order_transportkosten_unbezahlte_rechnungen.png](/uploads-de/admin_finances_order_transportkosten_unbezahlte_rechnungen.png)


## Freigabe Rechnung zur Bezahlung 

> Empfehlung: ins Notizfeld “bezahlen” schreiben, falls für das Bezahlen von Rechnungen andere Personen zuständig sind. 
{.is-info}


# Rechungen als bezahlt kennzeichnen

Rechnungen sollten erst dann als bezahlt gekennzeichnet werden, indem bei *bezahlt am* das Datum der Bezahlung eingetragen wird, wenn sie tatsächlich bezahlt wurden (z.B. indem im Ebanking eine Überweisung durchgeführt wurde). 

> Wenn die Foodsoft mit dem Bankkonto verknüpft ist, macht die Foodsoft das automatisch, siehe [Bankkonto](/de/documentation/admin/finances/bank-accounts).
{.is-info}


Bezahlte Rechnungen scheinen nicht mehr unter *Finanzen > Rechnungen > unbezahlte Rechnungen* und *Finanzen > Übersicht > unbezahlte Rechnungen* auf.
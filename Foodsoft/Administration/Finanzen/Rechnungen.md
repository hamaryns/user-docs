---
title: Rechnungen
description: Rechnungen von Lieferantinnen an die FC in der Foodsoft digital ablegen und mit Bestellungen verknüpfen
published: true
date: 2021-09-29T15:35:02.104Z
tags: 
editor: markdown
dateCreated: 2021-04-20T23:05:17.349Z
---

<h1 id="rechnunganlegen" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen"></a>Rechnung anlegen</h1>

Die Funktion “Rechnung anlegen” dient dazu, Rechnungen von ProdzentInnen in die Foodsoft zu übertragen und sie mit den entsprechenden Lieferungen und Bestellungen zu vergleichen. Rechnungen scheinen zunächst unter den “unbezahlten Rechnungen” auf, und werden als bezahlt markiert, sobald ein entsprechender Zahlungsausgang am Foodsoft-Bankkonto auftritt. Rechnungen können in Papierform oder digital als PDF vorliegen. 

Eine neue Rechnung kann angelegt werden unter
- Finanzen \> Rechnungen \> Neue Rechnung anlegen
- Finanzen \> Bestellungen abrechnen \> Bestellung auswählen \> Rechnung anlegen
- Bestellverwaltung \> beendete Bestellung auswählen \> Rechnung anlegen
- Artikel \> Lieferant \> Bestellung \> Rechnung anlegen
- Artikel \> Lieferant \> Letzte Lieferungen \> Rechnung anlegen
- Artikel \> Lager \> neue Lieferung… (?)

> Empfehlung: Rechnungen, die in Papierform vorliegen, gehen einfacher mit einem Smartphone oder Tablet mit Kamerafunktion einzugeben. Die Eingabe kann auch jederzeit unterbrochen, die Rechnung unfertig gespeichert werden, um auf einem anderen Gerät fortgesetzt werden. Wichtig ist es, das das Datum der Rechnung einzugeben, weil sie sonst schwer auffindbar ist. 
{.is-info}

![neue-rechnung.png](/neue-rechnung.png)


In der neuen Rechnung ist anzugeben:

<h2 id="rechnunganlegen-lieferantin" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-lieferantin"></a>Lieferant</h2>

Lieferantin auswählen.

> Wenn die Liste der Lieferantinnen recht lang ist, kannst du den ersten Buchstaben der Lieferantin tippen, um sie schneller zu finden.
{.is-info}


<h2 id="rechnunganlegen-bestliefverk" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-bestliefverk"></a>Bestellungen und Lieferungen mit Rechnung verknüpfen</h2>

In den Feldern **Lieferung** und **Bestellung** solltest du jene Lager-Lieferung(en) und/oder jene Bestellung(en) auswählen, für die die Rechnung ausgestellt wurde. Damit ist klar, ob die Lieferantin für eine Lieferung/Bestellung eine Rechnung ausgestellt hat, und der Rechnungsberag kann mit dem Guthaben, das den Mitgliedern abgebucht wird (bzw. das als Warenwert ins Lager eingegangen ist), verglichen werden. Dies ist die einzige echte Kontrollmöglichkeit, um zu schauen, dass die Foodcoop keinen Verlust, aber auch keinen unerwünschten Gewinn macht - daher ist dieser Schritt sehr wichtig.

![rechnung-bestellung-lieferung.png](/rechnung-bestellung-lieferung.png =400x)
    
-  **Lieferung**: **bei Rechnung für eine Bestellung leer lassen**. Wenn für diesen Produzenten Lagerartikel über die Funktion “Artikel \> Lager \> neue Lieferung” eingebucht  wurden, die noch keiner Rechnung zugeordnet sind, können diese  hier ausgewählt werden. Mehrere Lieferungen können dabei in  einer gemeinsamen Rechnung ausgewählt werden.
-  **Bestellung**: wenn es für diesen Produzenten abgeschlossene, aber noch nicht abgerechnete Bestellungen gibt, die noch keiner Rechnung zugeordnet sind, können diese hier ausgewählt werden. Mehrere Bestellungen können dabei in einer gemeinsamen  Rechnung ausgewählt werden.
    
> Angezeigter **Betrag** für Bestellung(en) und Lieferung(en)
> ist der Bruttobetrag (inkl. Mwst und Pfand)
{.is-info}

    
> Angezeigtes **Datum** für Bestellung(en) und Lieferung(en) ist jenes, an dem die Bestellung endete (nicht Liefer- oder  Abholdatum\!)
{.is-info}

> Es können mehrere Bestellungen und/oder Lieferungen ausgewählt werden, wenn dafür von der Lieferantin eine gemeinsame Rechnung gestellt wurde.
{.is-info}


> Eine Bestellung oder Lieferung kann nur einmal einer Rechnung zugeordnet werden. Wenn schon eine Rechnung angelegt und Bestellungen und/oder Lieferungen zugeordnet wurden, daher unbedingt diese suchen (siehe Rechnungsdatum) und bearbeiten, statt sie nochmal neu anzulegen. 
{.is-warning}

> Wenn eine Bestellung neben den Bestellungen für die Foodcoop Mitglieder auch eine Lagerbestellung enthält, und diese Lagerartikel dann mit einer Lieferung in den Lagerstand eingebracht werden, und sowohl die Bestellung als auch die Lieferung der Rechnung korrekter weise zugeordnet wird, würden sie bei der Rechnungsbilanz doppelt berücksichtigt - siehe [Lager](../Lager).
{.is-danger}


<h2 id="rechnunganlegen-nummer" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-nummer"></a>Nummer</h2>

Rechnungsnummer von Rechnung übernehmen. Die Rechnungsnummer wird bei der Banküberweisung von der Foodsoft (oder von der Person, die in der Foodcoop die Rechnungen via Ebanking manuell bezahlt) in den Verwendungszweck eingetragen, und dient sowohl der Foodsoft als auch der Lieferantin zur eindeutigen Zuordnung der Rechnung. 
> Falls auf der Rechnung keine Rechnungsnummer aufscheint, selbst eine (in Bezug auf die Lieferantin) eindeutige Rechnungsnummer erstellen, z.B. aus dem Datum, also z.B. `20210527` oder `2021-05-27` oder `270521`. 
{.is-info}




<h2 id="rechnunganlegen-rechndatum" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-rechndatum"></a>Rechnungsdatum</h2>

Von Rechnung übernehmen. 

Für die Eingabe des Datums gibt es folgende alternative Möglichkeiten
1. Über die Kalenderfunktion: im erscheinenden Kalender das Datum auswählen; diese Art ist auf mobilen Geräten aufgrund des kleinen Displays oft schwierig anzuwenden.
1. Eingabe im Textfeld **genau im Format** `2021-09-29` (also zuerst Jahr 4-stellig, Bindestrich, in der Mitte Monat zweistellig ggf. mit führender Null, Bindestrich,am Ende Tag zweistellig ggf. mit führender Null). 

> Wenn das Datum im falschen Format eingegeben wird, interpretiert die Foodsoft das Datum und insbesondere das Jahr falsch, und die Rechnung ist nachher scheinbar verschwunden, weil sie z.B. im Jahr 21 n.Chr. (statt 2021) angelegt ist.
{.is-warning}


> Rechungen werden in der Liste der Rechnungen nach dem Rechnungsdatum sortiert. Wenn dieses Feld leer gelassen wird, erscheint die Rechnung ganz am Ende der Liste der Rechnungen, statt am Anfang, wo neue Rechnungen sonst zu finden sind. Auch wenn ein falsches Datum (z.B. falsches Jahr) eingegeben wird, ist die Rechnung in der Liste schwerer aufzufinden.
{.is-warning}

<h2 id="rechnunganlegen-bezahltam" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-bezahltam"></a>Bezahlt am</h2>

### Rechnung noch unbezahlt

**Leer lassen**, wenn die Rechnung noch nicht bezahlt wurde. Die Rechnung scheint in der Foodsoft in der Liste "unbezahlte Rechnungen" auf. Die Person in deiner Foodcoop, die einen Bankkontozugang hat und die Überweisung der Rechnungen durchführt, weiß damit, dass diese Rechnung zu zahlen ist.  Wenn das Bankkonto der Foodcoop mit der Foodsoft verbunden ist, wird die Foodsoft hier automatisch das Datum des Zahlungsausgangs eintragen, und die Rechnung ist dann damit als bezahlt gekennzeichnet werden.

### Rechnung bereits bezahlt

Falls die Rechnung schon bezahlt wurde, das Datum eintragen, an dem dies erledigt wurde. Die Rechnung scheint dann **nicht** unter "unbezahlte Rechnungen" auf.  Die Person in deiner Foodcoop, die einen Bankkontozugang hat und die Überweisung der Rechnungen durchführt, weiß damit, dass diese Rechnung nicht mehr zu zahlen ist.


<h2 id="rechnunganlegen-betrag" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-betrag"></a>Betrag</h2>

Rechnungsbetrag (inklusive [Mehrwertsteuer](Mehrwertsteuer)) von Rechnung übernehmen.

<h2 id="rechnunganlegen-pfandberech" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-pfandberech"></a>Pfand berechnet</h2>

Leer lassen, falls in den Artikeln der Foodsoft ein Pfandbetrag bereits inkludiert ist, weil Bestellungen und Lieferungen nicht pfandbereinigt werden. Falls sich Pfand in der Foodsoft und auf der Rechnung des Produzenten nicht decken, kann hier die Differenz eingegeben werden: 
- (Pfand gesamt Produzent) - (Pfand gesamt Foodsoft). 
    
    
<h3 id="rechnunganlegen-pfandberech-beisp" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-pfandberech-beisp"></a>Beispiele </h3>

Für 3 Flaschen und 50 Cent Pfand pro Flasche:
- Foodsoft-Artikel enthält 50 Cent Pfand pro Flasche, Produzent verrechnet ebenfalls 50 Cent pro Flasche, Differenz = 3 \* 0,50 - 3 \* 0,50 = 0 €
- Foodsoft-Artikel enthält 50 Cent Pfand pro Flasche, Produzent verrechnet nur 10 Cent pro Flasche, Differenz = 3 \* 0,10 - 3 \* 0,50 = 3 \* (0,10-0,50) = -1,20 €
- Foodsoft-Artikel enthält 50 Cent Pfand pro Flasche, Produzent verrechnet kein Pfand, Differenz = 0 - 3 \* 0,50 = -1,50 € Foodsoft-Artikel enthält kein Pfand, Produzent verrechnet 50 Cent pro Flasche, Differenz = 3 \* 0,50 - 0 = +1,50 €

Siehe auch [Pfand in Foodcoops](Pfand).

<h2 id="rechnunganlegen-pfandgut" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-pfandgut"></a>Pfand gutgeschrieben</h2>

Pfandgutschrift des Produzenten Brutto (inkl. Mwst) als positiven Wert eintragen wie auf der Rechnung ausgewiesen, sofern im Rechnungsendbetrag berücksichtigt.

> Kann auch  für andere Gutschriften (z.B. Skonto) verwendet werden, die in den   Foodsoft-Bestellungen nicht berücksichtigt sind.
{.is-info}


<h2 id="rechnunganlegen-anhang" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-anhang"></a>Anhang</h2>

Foto der Papierrechnung oder PDF-Rechnungsdatei hochladen. 
    
> Auf Smartphones oder Tablets kann hier direkt die Kamera das Geräts ausgewählt und eine Foto der Rechnung aufgenommen und hochgeladen werden.
{.is-info}


<h2 id="rechnunganlegen-notiz" class="toc-header"><a class="toc-anchor" href="#rechnunganlegen-notiz"></a>Notiz</h2>

Empfehlung, dass hier der Status der Rechnung kommentiert wird (kann bezahlt werden, oder es muss z.B. noch auf eine Anpassung an die Lieferung gewartet werden) und etwaige Differenzen zwischen Bestellung und Rechnung dokumentiert und erklärt werden (Vorschlag: “Differenz X,XX Euro zugunsten/zulasten der Foodcoop aufgrund ...”). Kann zunächst leer gelassen und später noch bearbeitet werden.

<h1 id="rechnunganzmod" class="toc-header"><a class="toc-anchor" href="#rechnunganzmod"></a>Rechnung anzeigen und bearbeiten</h1>

Um eine bereits angelegte Rechnung anzuzeigen: 
- Finanzen \> Rechnungen; Die Rechnungen sind nach Rechnungsdatum sortiert, beginnend mit aktuellen. Diese Rechnung sollte hier auch dann zu finden sein, wenn die Rechnung schon als bezahlt markiert wurde (= Datum bei "bezahlt am" eingegeben)
>  Wenn ein falsches Datum in der   Vergangenheit eingegeben wurde, kann es sein, dass die Rechnung sehr  weit hinten zu finden ist.
{.is-warning}

- Finanzen \> Übersicht \> unbezahlte Rechnungen: hier scheint die Rechnung nur dann auf, wenn kein Datum bei “bezahlt am” eingegeben wurde, unabhängig davon, ob die Rechnung auch wirklich bezahlt wurde\!

Um eine bereits angelegte Rechnung zu bearbeiten: zunächst wie oben beschrieben anzeigen und dann “bearbeiten” auswählen. Zusätzlich gibt es noch die Möglichkeit über Finanzen \> Bestellungen abrechnen \> Bestellung auswählen \> Rechnung bearbeiten.

<h1 id="rechpruef" class="toc-header"><a class="toc-anchor" href="#rechpruef"></a>Rechnung prüfen</h1>

Unter Finanzen \> Übersicht \> unbezahlte Rechnung wir die Differenz zwischen Foodsoft Buchungen von den Mitgliederkonten und dem pfandbereinigten Rechnungsbetrag angezeigt, wenn sie nicht null ist:
- roter minus-Betrag: Foodcoop macht Verlust
- grüner plus-Betrag: Foodcoop macht Gewinn
- kein Differenzbetrag: exakte Übereinstimmung der Beträge

Das Vorzeichen hat sich Anfang März 2021 umgedreht, die Bedeutung der Farben in Bezug auf Verlust/Gewinn für die Foodcoop ist gleich geblieben.

Lieferungen ins Lager werden bei dieser Differenz leider nicht berücksichtigt(?)

Zusätzlich sind in der Rechnungsansicht noch folgende Details einzusehen:
- **Pfandbereinigter Betrag** = Rechnungsbetrag - Pfand berechnet + Pfand gutgeschrieben
- **Total**= Summe aus Bestellungen und Lieferungen Brutto (inkl. Pfand und Mwst, d.h. nicht Pfand-bereinigt\!), neu seit 2021-01: inklusive Transportkosten (werden bei Bestellung als zusätzlicher Plus-Betrag angezeigt; Transportkosten anlegen: siehe eigener Punkt unten).

> **Pfandbereinigter Betrag** und **Total** sollten übereinstimmen. 
{.is-warning}

Falls nicht:
- **Pfandbereinigter Betrag **größer als** Total**: Lieferant verrechnet mehr, als den Foodcoop Mitgliedern vom Guthaben abgezogen wird. Die Foodcoop macht Verlust.
- **Pfandbereinigter Betrag **kleiner als** Total**: Lieferant verrechnet weniger, als den Foodcoop Mitgliedern vom Guthaben abgezogen wird. Die Foodcoop macht “Gewinn”.

Unter Finanzen \> Bestellungen abrechnen \> … findest du ebenfalls eine Gegenüberstellung von Bestellung und Rechnung, die allerdings nur dann brauchbar ist, wenn es genau eine Bestellung gibt, die der Rechnung zugeordnet wird. Werden mehrere Bestellungen zugeordnet, wird immer nur die aktuelle Bestellung mit der gesamten Rechnung verglichen.


<h2 id="rechpruef-bezfreig" class="toc-header"><a class="toc-anchor" href="#rechpruef-bezfreig"></a>Rechnung zur Bezahlung freigeben</h2>

Empfehlung: ins Notizfeld “bezahlen” schreiben, falls für das Bezahlen von Rechnungen andere Personen zuständig sind. 

<h1 id="rechbezkenn" class="toc-header"><a class="toc-anchor" href="#rechbezkenn"></a>Rechungen als bezahlt kennzeichnen</h1>

Rechnungen sollten erst dann als bezahlt gekennzeichnet werden, wenn sie tatsächlich bezahlt wurden (z.B. indem im Ebanking eine Überweisung durchgeführt wurde). 

> Wenn die Foodsoft mit dem Bankkonto verknüpft ist, macht die Foodsoft das automatisch, siehe [Foodsoft Rechnungen](#anchor-134) im Abschnitt [Bankkonto mit Foodsoft verknüpfen](#anchor-19).
{.is-info}


Bezahlte Rechnungen scheinen nicht mehr unter Finanzen \> Rechnungen \> unbezahlte Rechnungen und Finanzen \> Übersicht \> unbezahlte Rechnungen auf.
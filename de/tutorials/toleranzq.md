---
title: Tutorial - How to do Toleranzen
description: 
published: true
date: 2021-10-02T16:20:04.290Z
tags: 
editor: markdown
dateCreated: 2021-03-25T01:33:06.077Z
---

# Tutorial - How to do Toleranzen
Manche LieferantInnen liefern keine einzelnen Packungen, sondern nur ganze Gebinde an, die wir aber unter uns aufteilen können. Ähnlich ist es bei Waren, die lose in einer Großpackung bestellt werden, aus der sich dann jede Bestellgruppe ihre bestellte Menge herausschöpft. Durch die Bestellungen der Bestellgruppe wird die Gebindegröße wahrscheinlich nicht genau erreicht. Beispiel: 28 Packungen wurden bestellt, es gibt 10 Packungen je Gebinde – daher werden nur 2 Gebinde, also 20 Packungen bestellt und viele Bestellgruppen gehen leer aus. Wenn sich aber jemand bereit erklärt hätte, in so einem Fall 2 Packungen zusätzlich zu nehmen, könnten 30 (also 3 Gebinde) bestellt werden. Das man mit der Toleranz angeben: Wie viele Einheiten würde man zusätzlich maximal nehmen, damit die Anzahl aufgeht?

**Achtung:** Es wird nicht angezeigt, wie viel einem die Toleranzmenge kosten würde - ihr werdet nicht daran gehindert so euer Konto zu überziehen. Passt auf, dass ihr spätestens bei der Abrechnung genug Guthaben auf eurem Konto habt!

Geht die Anzahl im Moment nicht auf, ist die Zeile rötlich eingefärbt und unter "Fehlend" wird angezeigt, wie viele Einheiten aktuell noch bis zum nächsten vollen Gebinde fehlen. Bei der Menge und Toleranz stehen jeweils zwei Zahlen (hier "0 + 0"): Die erste Zahl gibt die Anzahl Stück an, die man aktuell auch erhalten würde (für sich selbst). Die zweite könnte man zusätzlich bekommen, wenn sich die Bestellung verändert. Ich empfehle euch, einfach immer beide Zahlen zusammenzuzählen und nicht nach dem aktuellen Stand zu gehen, denn es kann sich ja immer noch was verändern. Damit es aber nicht vollkommen verwirrend ist, im Folgenden ein Beispiel für eine Bestellung mit drei Bestellgruppen:

![](/tutorials/images/uvrmx7c.jpg)

Hier hat noch niemand bestellt. Nun bestellt die erste Bestellgruppe 1 Stück:

![](/tutorials/images/9yahykx.jpg)

Nun springt die Zahl bei "Fehlend" auf 9, da noch 9 Stück bestellt werden müssten, damit es aufgeht. Deshalb ist das bestellte 1 Stück in der zweiten Zahl angegeben ("0 + 1") - momentan würde man es nicht erhalten.

![](/tutorials/images/eeggroe.jpg)

Die erste Bestellgruppe erhöht ihre Toleranz um 1 Stück, d.h. sie möchte mindestens 500g erhalten, würde aber auch 1 kg abnehmen. Dadurch verringert sich die fehlende Menge auf 8.

![](/tutorials/images/ariqequ.jpg)

Die Bestellübersicht zeigt bei "Bestellt" nun "Menge + Toleranz" an. Da es nicht für ein Gebinde ausreicht, würde sie nichts erhalten.

![](/tutorials/images/gfmew7q.jpg)

Nun ist die zweite Bestellgruppe an der Reihe. Die Zeile ist gleich rot eingefärbt, obwohl die Bestellgruppe selbst noch gar nichts bestellt hat.

![](/tutorials/images/7imktlt.jpg)

Die zweite Bestellgruppe möchte 1 kg, könnte aber im Notfall auch bis zu 2,5 kg nehmen, daher gibt sie bei Menge 2 und bei Toleranz 3 an.

![](/tutorials/images/ucq6bi5.jpg)

Nun ist die dritte Bestellgruppe an der Reihe. Sobald sie bei der Menge 2 einträgt, wird die Zeile nicht mehr rot, sondern gelb eingefärbt, da nur noch 1 Stück fehlt, damit es aufgeht.

![](/tutorials/images/eezwjmh.jpg)

Die dritte Bestellgruppe gibt noch eine Toleranz von 1 an: Damit geht es auf, die Zeile wird grün eingefärbt und die Zahlen springen auf die linke Seite vom + (also Menge "2 + 0" statt vorher "0 + 2"), weil diese Menge nun erhalten werden würde.

![](/tutorials/images/hfrtws7.jpg)

Erhöht die dritte Bestellgruppe ihre Toleranz noch mal um 1 Stück, wird das jedoch auf die rechte Seite vom + geschrieben, da das nach aktuellem Stand nicht erhalten werden würde.

![](/tutorials/images/zztcv89.jpg)

Erhöht die dritte Bestellgruppe hingegen wiederum ihre Menge um 1 Stück, ist die Toleranz im Moment nicht mehr relevant und wird komplett auf die rechte Seite vom + geschrieben.

![](/tutorials/images/ehqd0qk.jpg)

Bestellergebnis für die dritte Bestellgruppe: Bei "Bestellt" wird Menge+Toleranz angegeben. Da jedoch aktuell nur die Menge erhalten werden würde, steht bei "Zu erhalten" 3.

![](/tutorials/images/pdo5gpc.jpg)

Nun ein Blick in die Bestellübersicht, die nur für Admins einsehbar ist: Die Foodsoft ordnet automatisch zu, wie das Gebinde aufgeht. Da LLTest und lea zuerst bestellt haben, wird deren Toleranz dafür genutzt. Die Toleranz von OG3 (dritte Bestellgruppe) ist dann nicht mehr nötig, daher steht bei "Bekommen" nur die Menge.

![](/tutorials/images/hdf39va.jpg)

Die erste Bestellgruppe erhöht ihre Menge nun um 3 Stück.

![](/tutorials/images/clncdim.jpg)

Dadurch verringert sich die Menge, die die anderen Bestellgruppen erhalten würden. Da die erste Bestellgruppe zuerst bestellt hatte, wird ihre Toleranz weiterhin als erstes berücksichtigt und die Toleranz der anderen Bestellgruppen ist aktuell nicht relevant.

![](/tutorials/images/aodvsoy.jpg)

Die erste Bestellgruppe erhöht ihre Menge nochmals um 1, wodurch auch ihre eigene Toleranz irrelevant wird.

![](/tutorials/images/flecj1c.jpg)

Nun gehen die Bestellmengen auch ohne Toleranz genau auf, daher wird überall die Toleranz ignoriert.

![](/tutorials/images/xxtosxu.jpg)

Die erste Bestellgruppe erhöht ihre Menge ein weiteres Mal um 1 Stück. Das ist nun nicht mehr im Gebinde erhalten, daher könnte es im Moment nicht geliefert werden und wird auf die rechte Seite vom + geschrieben. Bei "Fehlend" wird nun "3" angezeigt, da drei Stück fehlen, bis sich ein zweites Gebinde ausgeht (dank Toleranz).

![](/tutorials/images/bzzlnqc.jpg)

Die Bestellübersicht teilt der ersten Bestellgruppe ihr 6. Stück nicht zu, da sie es zuletzt bestellt hat.

![](/tutorials/images/gx0okgo.jpg)

Nun schaut wieder die zweite Bestellgruppe hinein und erhöht ihre Menge auf 5. Damit fehlt nur noch 1 Stück, damit zwei Gebinde bestellt werden können, somit die Zeile wird gelb eingefärbt.

![](/tutorials/images/wxkj6uo.jpg)

Die zweite Bestellgruppe erhöht auch noch ihre Toleranz um 1 Stück, wodurch es nun aufgeht und alle Zahlen auf die linke Seite springen.

![](/tutorials/images/j3ioosa.jpg)

Denn bei allen Bestellgruppen wird nun wieder die Toleranz hinzugenommen, um insgesamt auf 20 Stück (2 Gebinde à 10 Stück) zu kommen.

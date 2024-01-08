---
title: "Fraktionsverträge"
date: 2022-12-05T10:30:49+02:00
weight: 3
---

## Allgemeine Informationen

Von Zeit zu Zeit senden Ihnen AgentInnen Ihrer [Fraktion](/wiki/packages-factions/#factions) eine Liste mit Vertragsangeboten. Diese Verträge umfassen eine Reihe von Aufgaben, die Sie erfüllen müssen, gewähren aber Belohnungen in Form von Währung, Materialien oder Ruf bei Ihrer Fraktion. Die Annahme dieser Verträge ist optional.

## Fraktionsverträge erhalten und annehmen

Sobald Sie Ihre erste Basis gegründet haben, werden Ihnen FraktionsrepräsentantInnen Vertragsangebote machen. Diese Angebote kommen in der Regel in Dreierpaketen. Sie erhalten eine Benachrichtigung und die Verträge werden im `CONTS`-Command mit dem Status `"Offen"` angezeigt.

![CONTS](./conts.png)

Sie können jeden Vertrag einsehen, indem Sie auf "Anzeigen" klicken. Obwohl es bestimmte Arten von Verträgen gibt, ist jeder ein wenig anders. Schauen Sie sich den Vertrag daher genau an, bevor Sie ihn annehmen.

Hier ist ein Beispielvertrag:

![CONT example](./cont_example.png)

Die Präambel ist in zwei Abschnitte unterteilt. Der Teil "Angebotene Fraktionsverträge" beschreibt, dass dieser Vertrag Teil eines Vertragsangebots ist und Links zu den anderen Vertragsangeboten enthält. 

Der zweite Teil "Missionsbeschreibung" enthält eine Textbeschreibung der Mission und ist im Wesentlichen eine Zusammenfassung der unten aufgeführten Vertragsbedingungen. 

An dieser Stelle haben Sie drei Möglichkeiten:
* **Akzeptieren:** Sie akzeptieren den Vertrag. Der Vertrag wechselt vom offenen in den geschlossenen Zustand und verhält sich wie jeder andere Vertrag.
* **Ablehnen:** Sie lehnen den Vertrag ab. Dadurch wird der Vertrag als abgelehnt markiert.
* **Warten:** Sie warten. Nach 48 Stunden werden offene Verträge automatisch gekündigt.

{{% notice style="primary" title="Annahme eines Vertragsangebots" icon="exclamation" %}}
Bitte beachten Sie, dass die Annahme eines Vertragsangebots automatisch zur Stornierung der anderen Vertragsangebote führt. 
{{% /notice %}}

## Belohnungen und Ruf

Das Annehmen und Erfüllen von Fraktionsverträgen ist optional. Es hat keinen Nachteil, sie zu ignorieren oder abzulehnen, außer dass man die Belohnungen und den Ruf bei der Fraktion nicht erhält.

Es gibt Fraktionsvertragstypen, die sehr verbreitet sind, wie das oben gezeigte Beispiel, aber ab und zu erhalten Sie auch einen selteneren Typ. Je seltener der Vertragstyp ist, desto höher sind seine Belohnungen.

Fraktionsverträge bieten eine Kombination aus Belohnungen in Form von Währung, Waren und Reputationspunkten der Fraktion.

Die Höhe der Geldprämie hängt von der Vertragsart und dem Vorliegen einer Warenprämie ab. In der Regel ist die monetäre Belohnung geringer, wenn auch eine Warenprämie vorhanden ist.

Warenprämien müssen immer am Standort Ihres Firmensitzes abgeholt werden.

Durch die erfolgreiche Erfüllung von Fraktionsverträgen erhalten Sie Reputationspunkte der Fraktion. Alle BenutzerInnen beginnen mit einem Fraktionsruf von 100. Je höher der Ruf, desto höher sind die Belohnungen für zukünftige Fraktionsverträge. Der aktuelle Fraktionsruf kann über den `CO`-Command mithilfe Ihres Firmencodes eingesehen werden:

![Faction reputation in CO command](./reputation.png)

## Fraktionsverträge deaktivieren

Wenn Sie keine Angebote mit Fraktionsverträgen erhalten möchten, können Sie diese im jeweiligen FA-Befehl deaktivieren. Klicken Sie hierfür einfach auf den Namen eines Fraktionsrepräsentanten / einer Fraktionsrepräsentantin.

![Disable faction contract offers in FA command](./disable.png)

{{% about-this-page %}}

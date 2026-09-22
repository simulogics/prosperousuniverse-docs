---
title: "Command-Liste"
date: 2018-09-18T17:13:49+02:00
---

Dies ist eine umfassende Liste aller Commands, die Ihnen in APEX zur Verfügung stehen. Sie sind nach ihren jeweiligen Einsatzgebieten gruppiert. Um diese Liste zu verstehen, müssen Sie bereits mit der [Funktionsweise von Commands](../../tutorials/legacy-tutorials/commands) vertraut sein. Sie können die gesamte Liste durchlesen, um sich einen Überblick zu verschaffen, oder sie als Referenz zum Nachschlagen bestimmter Commands verwenden.

Parameter in `<spitzen Klammern>` sind obligatorisch, Parameter in `[eckigen Klammern]` optional.

| Kategorie | Commands |
|-----------|----------|
| [Basen](#bases) | [`BS`](#bs), [`BSC`](#bsc), [`BBL`](#bbl), [`BBC`](#bbc), [`BUI`](#bui), [`WF`](#wf), [`EXP`](#exp), [`HQ`](#hq), [`BRA`](#bra) |
| [Produktion](#production) | [`PROD`](#prod), [`PRODQ`](#prodq), [`PRODCO`](#prodco) |
| [Bestände](#inventory) | [`INV`](#inv), [`MTRA`](#mtra), [`UPCK`](#upck) |
| [Schiffe und Flüge](#ships-and-flights) | [`FLT`](#flt), [`SHP`](#shp), [`SHPF`](#shpf), [`SHPI`](#shpi), [`SFC`](#sfc), [`SI`](#si), [`RT`](#rt), [`RTE`](#rte) |
| [Schiffsbau](#ship-building) | [`BLU`](#blu), [`SHY`](#shy), [`SHYP`](#shyp) |
| [Verträge](#contracts) | [`CONTS`](#conts), [`CONT`](#cont), [`CONTD`](#contd) |
| [Warenbörse](#commodity-exchange) | [`CXL`](#cxl), [`CX`](#cx), [`CXM`](#cxm), [`CXP`](#cxp), [`CXPC`](#cxpc), [`CXOB`](#cxob), [`CXPO`](#cxpo), [`CXOS`](#cxos), [`CXO`](#cxo), [`MAT`](#mat) |
| [Devisenhandel](#foreign-exchange) | [`FX`](#fx), [`FXP`](#fxp), [`FXPC`](#fxpc), [`FXOB`](#fxob), [`FXPO`](#fxpo), [`FXOS`](#fxos), [`FXO`](#fxo) |
| [Lokale Marktplätze](#local-markets) | [`LMOS`](#lmos), [`LM`](#lm), [`LMA`](#lma), [`LMP`](#lmp) |
| [Karten und Orte](#maps-and-locations) | [`MU`](#mu), [`MS`](#ms), [`SYSI`](#sysi), [`PLI`](#pli), [`STNS`](#stns) |
| [Planetare Projekte](#planetary-projects) | [`PPS`](#pps), [`PP`](#pp), [`PPI`](#ppi), [`POPR`](#popr), [`WAR`](#war) |
| [Infrastruktur](#infrastructure) | [`INF`](#inf), [`INFU`](#infu), [`ASTS`](#asts), [`GTW`](#gtw), [`GTWI`](#gtwi), [`GTWT`](#gtwt) |
| [Politik](#politics) | [`ADM`](#adm), [`GOV`](#gov), [`LR`](#lr), [`MOTS`](#mots), [`MOT`](#mot), [`POL`](#pol) |
| [Soziales](#social) | [`FA`](#fa), [`CO`](#co), [`USR`](#usr), [`BDGS`](#bdgs), [`CONS`](#cons), [`COM`](#com), [`COMC`](#comc), [`COMP`](#comp), [`COMG`](#comg), [`COMU`](#comu) |
| [Benachrichtigungen](#notifications) | [`NOTS`](#nots), [`NOTIG`](#notig), [`NOTPNS`](#notpns) |
| [Unternehmen und Finanzen](#company-and-finances) | [`FIN`](#fin), [`FINBS`](#finbs), [`FINIS`](#finis), [`FINLA`](#finla), [`LEAD`](#lead), [`ARC`](#arc), [`GIFT`](#gift), [`COLIQ`](#coliq) |
| [Interface und Übertragungen](#interface-and-transmissions) | [`CS`](#cs), [`SCRN`](#scrn), [`LIC`](#lic), [`TRA`](#tra), [`XIT`](#xit), [`XYTV`](#xytv) |

## Basen {#bases}

Basis-Commands geben eine Basis über den Planeten an, auf dem sie liegt, zum Beispiel `BS XK-745a`.

### BS – Basen {#bs}

`BS [Planeten-ID]`

Zeigt eine Übersicht all Ihrer Basen oder die Details Ihrer Basis auf dem angegebenen Planeten. Die Basisansicht bietet Schaltflächen für die meisten anderen Basis-Commands.

### BSC – Basiskonstruktion {#bsc}

`BSC <Planeten-ID>`

Errichtet eine neue Basis auf einem Planeten. Zeigt die benötigten Baumaterialien und lässt Sie eine Parzelle auswählen.

### BBL – Gebäude einer Basis {#bbl}

`BBL <Planeten-ID>`

Listet die Gebäude einer Basis auf. ABREISSEN entfernt ein Gebäude und erstattet je nach Alter einen Teil der Materialien. Die mögliche Erstattung wird unter "Zurückgewinnbare Baumaterialien" aufgeführt.

**Schnellzugriff:** die Schaltfläche GEBÄUDE in `BS`.

### BBC – Gebäude bauen {#bbc}

`BBC <Planeten-ID>`

Baut ein neues Gebäude in einer Basis. Die Registerkarten oben wechseln zwischen den Gebäudekategorien. "Fläche" zeigt den Flächenbedarf des Gebäudes und die verbleibende Fläche Ihrer Basis, "Belegschaft" die benötigten Arbeitskräfte.

**Schnellzugriff:** die Schaltfläche BAUEN in `BS`.

### BUI – Gebäudeinformationen {#bui}

`BUI <Gebäude-Ticker>`

Zeigt einen Gebäudetyp: die Belegschaft, die er beschäftigt, die Fläche, die er einnimmt, und die zum Bau benötigten Materialien.

**Schnellzugriff:** Klick auf einen Gebäudetyp in `BBC`.

### WF – Belegschaft {#wf}

`WF <Planeten-ID>`

Zeigt die Belegschaft einer Basis und ihre Bedürfnisse. Höhere Belegschaftsstufen haben mehr Bedürfnisse. Erhalten die Arbeitskräfte nicht die benötigten Versorgungsgüter, sinkt die Effizienz ihrer Gebäude.

**Schnellzugriff:** die Schaltfläche BELEGSCHAFT in `BS`.

### EXP – ExpertInnen {#exp}

`EXP <Planeten-ID>`

Zeigt die Bereiche, die ExpertInnen verbessern können, und die einer Basis zugewiesenen ExpertInnen. ENTFERNEN deaktiviert eine Expertin oder einen Experten, AKTIVIEREN schickt sie wieder an die Arbeit.

**Schnellzugriff:** die Schaltfläche EXPERTEN in `BS`.

### HQ – Firmensitz {#hq}

`HQ`

Zeigt, welche Ihrer Basen Ihr Firmensitz ist. Verlegen Sie ihn für andere [Fraktionsboni](../headquarters) an eine andere Basis, oder bauen Sie ihn aus, um zusätzliche Basisgenehmigungen und Slots in der Produktionswarteschlange freizuschalten.

### BRA – Reparaturassistent {#bra}

`BRA [Planeten-ID]`

Repariert mehrere Gebäude einer Basis auf einmal: Alle Gebäude, deren Zustand dem festgelegten Wert entspricht oder darunter liegt, werden einbezogen.

## Produktion {#production}

### PROD – Produktion {#prod}

`PROD [Planeten-ID]`

Zeigt die Produktionslinien all Ihrer Basen oder der Basis auf dem angegebenen Planeten. Jede Produktionslinie besteht aus einem oder mehreren Gebäuden desselben Typs.

**Schnellzugriff:** die Schaltfläche PRODUKTION in `BS`.

### PRODQ – Produktionswarteschlange {#prodq}

`PRODQ <Produktionslinien-ID>`

Zeigt die Auftragswarteschlange einer Produktionslinie. Aufträge in der Warteschlange können storniert werden, laufende Aufträge nicht. Die angezeigte Effizienz hängt von der Zufriedenheit der Arbeitskräfte, von ExpertInnen und bei manchen Gebäuden von der Fruchtbarkeit des Planeten ab.

**Schnellzugriff:** die Schaltfläche DETAILS in `PROD`.

### PRODCO – Produktionsauftrag {#prodco}

`PRODCO <Produktionslinien-ID>`

Stellt einen neuen Produktionsauftrag in die Warteschlange. Wählen Sie das Produkt und die Auftragsgröße, und stellen Sie sicher, dass die unten angezeigten Input-Materialien verfügbar sind.

**Schnellzugriff:** die Schaltfläche AUFTRAG ERSTELLEN in `PROD`.

## Bestände {#inventory}

### INV – Bestände {#inv}

`INV [Adresse oder Lager-ID]`

Listet all Ihre Bestände auf: Basislager, Frachträume, Treibstofftanks und Lager-Einheiten in Lagerhäusern. Mit einem System oder Planeten (zum Beispiel `INV XK-745` oder `INV XK-745a`) werden nur die Bestände an diesem Ort angezeigt. Mit einer Lager-ID öffnet sich dieser Bestand.

Innerhalb eines Bestands können Sie nach Anzahl (ANZ), Gewicht (MAS) oder Volumen (VOL) sortieren. Die Rasteransicht zeigt Gewicht, Volumen und Buchwert jedes Materials.

### MTRA – Materialtransfer {#mtra}

`MTRA [Material-Ticker] [Ursprungslager-ID] [Ziellager-ID]`

Überträgt eine Menge eines Materials zwischen zwei Beständen. Was nicht als Parameter angegeben wird, kann im Fenster ausgewählt werden.

**Schnellzugriff:** Ziehen Sie ein Material aus dem Ursprungsbestand und legen Sie es auf dem "AMT"-Slot des Zielbestands ab.

### UPCK – Auspacken {#upck}

`UPCK <Lager-ID>`

Listet die Konsumgüterpakete in einem Lager auf und packt sie aus. Pakete werden in das Lager ausgepackt, in dem sie liegen.

## Schiffe und Flüge {#ships-and-flights}

Beginnen Sie mit `FLT`: Die meisten anderen Schiffs-Commands lassen sich von dort aus öffnen. Das [Weltraumflug-Tutorial](../../tutorials/legacy-tutorials/space-flight) zeigt sie in Aktion.

### FLT – Flotte {#flt}

`FLT [System- oder Planeten-ID]`

Listet all Ihre Schiffe mit Transpondercode, Name, Status, Ladung, Standort und aktuellem Flug auf. Mit einer System- oder Planeten-ID werden nur die Schiffe an diesem Ort angezeigt.

### SHP – Schiff {#shp}

`SHP <Transpondercode>`

Zeigt die Details eines Ihrer Schiffe. Klicken Sie auf den Namen des Schiffs, um es umzubenennen.

**Schnellzugriff:** Klick auf den Transpondercode eines Schiffs in `FLT`.

### SHPF – Schiffstreibstoff {#shpf}

`SHPF <Transpondercode>`

Zeigt die Treibstoffstände eines Schiffs.

**Schnellzugriff:** Klick auf die Treibstoffleiste eines Schiffs in `FLT`.

### SHPI – Schiffsbestand {#shpi}

`SHPI <Transpondercode>`

Zeigt den Frachtraum eines Schiffs. Der Frachtraum ist durch Gewicht und Volumen begrenzt.

**Schnellzugriff:** Klick auf die Ladungsleiste eines Schiffs in `FLT`.

### SFC – Schiffsflug-Steuerung {#sfc}

`SFC <Transpondercode>`

Plant und startet einen Flug. Geben Sie einen Planeten oder eine Station als Ziel ein, legen Sie den Treibstoffverbrauch fest und klicken Sie auf "Start".

**Schnellzugriff:** die Schaltfläche STARTEN in `FLT`.

### SI – Schiffsinformationen {#si}

`SI <Transpondercode>`

Zeigt die öffentlichen Informationen zu einem beliebigen Schiff, auch zu Schiffen anderer SpielerInnen.

**Schnellzugriff:** Klick auf das Dreieck eines Schiffs in einer Systemkarte oder in `PLI`.

### RT – Routen {#rt}

`RT [Routen-ID]`

Listet all Ihre Routen auf oder öffnet eine einzelne Route. Erstellen und bearbeiten Sie Routen und weisen Sie ihnen Schiffe zu. Siehe [Routen](../routes).

### RTE – Routenausführungen {#rte}

`RTE [Transpondercode]`

Zeigt den Fortschritt aller Schiffe auf Routen oder eines einzelnen Schiffs. Siehe [Routen](../routes/#monitoring-route-execution).

## Schiffsbau {#ship-building}

### BLU – Blueprints {#blu}

`BLU [Blueprint-ID]`

Listet all Ihre Schiffsentwürfe auf oder öffnet einen davon.

### SHY – Schiffswerft {#shy}

`SHY [Planeten-ID]`

Zeigt die Schiffswerft eines Planeten.

### SHYP – Schiffswerftprojekte {#shyp}

`SHYP [Projekt-ID]`

Listet all Ihre Schiffbauprojekte auf oder öffnet eines davon.

## Verträge {#contracts}

### CONTS – Verträge {#conts}

`CONTS`

Listet all Ihre Verträge auf. Klicken Sie auf einen Vertrag, um ihn in `CONT` zu öffnen. Ausstehende Verträge werden auch in der rechten Seitenleiste aufgeführt, die Sie mit der Schaltfläche SEITL auf der linken Seite ein- und ausblenden. Siehe das [Vertrags-Tutorial](../../tutorials/legacy-tutorials/contracts).

### CONT – Vertrag {#cont}

`CONT <Vertrags-ID>`

Zeigt einen einzelnen Vertrag. Vertrags-IDs sind lang, daher ist es einfacher, Verträge über `CONTS` zu öffnen.

### CONTD – Vertragsentwürfe {#contd}

`CONTD [Entwurfs-ID]`

Listet Ihre Vertragsentwürfe auf oder öffnet einen davon, um ihn zu bearbeiten und zu versenden. Siehe [Benutzerdefinierte Verträge](../custom-contracts).

## Warenbörse {#commodity-exchange}

Ein Warenbörsen-Ticker kombiniert ein Material und eine Börse, zum Beispiel `RAT.NC1`. [Ein Guide zum Markt](../../tutorials/current-tutorials/05-market-guide) zeigt diese Commands in Aktion.

### CXL – Warenbörsen {#cxl}

`CXL`

Listet alle Warenbörsen auf.

### CX – Warenbörse {#cx}

`CX <Börsencode>`

Zeigt eine Warenbörse und ihre Materialien, nach Kategorien sortiert. Jedes Material hat Schaltflächen für die unten beschriebenen Ticker-Commands.

**Schnellzugriff:** Klick auf eine Börse in `CXL`.

### CXM – Materialvergleich {#cxm}

`CXM <Material-Ticker> [Planeten-ID]`

Vergleicht ein Material über alle Warenbörsen hinweg. Mit einer Planeten-ID werden die Börsen nach ihrer Entfernung zu diesem Planeten sortiert.

### CXP – Preisinformationen {#cxp}

`CXP <Ticker>`

Zeigt aktuelle Gebote und Angebote, Allzeithochs und -tiefs und mehr.

**Schnellzugriff:** die Schaltfläche INFO in `CX`.

### CXPC – Preischart {#cxpc}

`CXPC <Ticker>`

Zeigt ein Kerzenchart des Preises im Zeitverlauf. "Keine Daten" bedeutet, dass im gewählten Zeitraum nichts gehandelt wurde. Wählen Sie einen längeren Zeitraum.

**Schnellzugriff:** die Schaltfläche CHART in `CX`.

### CXOB – Orderbuch {#cxob}

`CXOB <Ticker>`

Zeigt die offenen Kauf- und Verkaufsorders.

**Schnellzugriff:** die Schaltfläche ORDERS in `CX`.

### CXPO – Order aufgeben {#cxpo}

`CXPO <Ticker>`

Gibt eine Kauf- oder Verkaufsorder innerhalb der aktuellen Preisspanne auf. Die Spanne basiert auf einem Drei-Tage-Durchschnitt und ist für PRO-NutzerInnen breiter. Die Schaltflächen "setzen" übernehmen das aktuell beste Gebot bzw. Angebot, unter "Bestand" wählen Sie, von wo aus verkauft wird.

**Schnellzugriff:** die Schaltfläche HANDEL in `CX`.

### CXOS – Warenbörsen-Orders {#cxos}

`CXOS`

Listet Ihre Kauf- und Verkaufsorders auf. Wenn Sie eine nicht vollständig ausgeführte Order löschen, ziehen Sie sie vom Markt zurück.

### CXO – Warenbörsen-Order {#cxo}

`CXO <Order-ID>`

Zeigt eine Ihrer Orders.

**Schnellzugriff:** die Schaltfläche ANSEHEN in `CXOS`.

### MAT – Material {#mat}

`MAT <Material-Ticker>`

Zeigt ein Material: was daraus hergestellt werden kann ("Verarbeitung") und wie es produziert wird ("Produktion"). Der Ticker ist das Kürzel im Symbol des Materials, zum Beispiel STL für Stahl.

**Schnellzugriff:** Klick auf das Symbol eines Materials, zum Beispiel in `CX`.

## Devisenhandel {#foreign-exchange}

Ein Währungspaar besteht aus zwei Währungscodes, getrennt durch einen Schrägstrich oder einen Punkt, zum Beispiel `AIC/CIS`. Siehe das [Devisenhandel-Tutorial](../../tutorials/legacy-tutorials/foreign-exchange).

### FX – Wechselkurse {#fx}

`FX`

Zeigt eine Matrix der Wechselkurse, mit den Basiswährungen vertikal und den Notierungswährungen horizontal angeordnet.

### FXP – Wechselkursinformationen {#fxp}

`FXP <Währungspaar>`

Zeigt Wechselkursinformationen für ein Währungspaar.

**Schnellzugriff:** Klick auf einen Kurs in `FX`.

### FXPC – Wechselkurschart {#fxpc}

`FXPC <Währungspaar>`

Zeigt den Wechselkursverlauf eines Währungspaares.

### FXOB – Orderbuch {#fxob}

`FXOB <Währungspaar>`

Zeigt die offenen Orders für ein Währungspaar.

### FXPO – Order aufgeben {#fxpo}

`FXPO <Währungspaar>`

Gibt eine Devisenorder auf, mit der Sie eine Währung gegen eine andere kaufen. Mengen werden in Lots zu je 1.000 Einheiten jeder Währung angegeben.

### FXOS – Devisenorders {#fxos}

`FXOS`

Listet all Ihre Devisenorders auf.

### FXO – Devisenorder {#fxo}

`FXO <Order-ID>`

Zeigt eine Ihrer Devisenorders.

**Schnellzugriff:** Klick auf eine Benachrichtigung über einen Devisenhandel.

## Lokale Marktplätze {#local-markets}

### LMOS – Anzeigen auf lokalen Marktplätzen {#lmos}

`LMOS`

Listet all Ihre Anzeigen auf lokalen Marktplätzen auf.

### LM – Lokaler Marktplatz {#lm}

`LM <Planeten- oder Stations-ID>`

Zeigt die Anzeigen auf einem lokalen Marktplatz.

**Schnellzugriff:** der Infrastruktureintrag "Lokaler Marktplatz" in `PLI`.

### LMA – Anzeige {#lma}

`LMA <Anzeigen-ID>`

Zeigt die Details einer Anzeige.

**Schnellzugriff:** Klick auf eine Anzeige in `LM`.

### LMP – Anzeige erstellen {#lmp}

`LMP <Planeten- oder Stations-ID>`

Erstellt eine Anzeige auf einem lokalen Marktplatz.

**Schnellzugriff:** die Schaltfläche ANZEIGE ERSTELLEN in `LM`.

## Karten und Orte {#maps-and-locations}

Ziehen Sie eine Karte mit der linken Maustaste, um sie zu verschieben, und mit der rechten Maustaste, um sie zu drehen. Manche Karten lassen sich mit der Option "Fix 2D" in 2D anzeigen.

### MU – Karte des Universums {#mu}

`MU [CX | NAV]`

Zeigt die Karte des Universums. Die verbundenen Punkte sind Sternensysteme. Fahren Sie mit der Maus über eines, um seine ID zu sehen. Mit den Schaltern unten blenden Sie Kartenebenen ein und aus, und manche Daten lassen sich nach Zeitraum filtern.

* `MU CX` zeigt die Warenbörsen.
* `MU NAV` zeigt den Verkehr. Solange "Flotte" aktiviert ist, sind Ihre Schiffe mit gelben Pfeilen markiert. Siehe das [Weltraumflug-Tutorial](../../tutorials/legacy-tutorials/space-flight).

### MS – Systemkarte {#ms}

`MS <System-ID>`

Zeigt ein Sternensystem mit seinem Stern in der Mitte. Kreise sind Gesteinsplaneten (weiß) oder Gasplaneten (orange), Quadrate sind Raumstationen. Fahren Sie mit der Maus darüber, um die ID zu sehen. Ihre Schiffe sind mit gelben Pfeilen markiert. Aktivieren Sie "traffic", um die Schiffe anderer NutzerInnen als weiße Pfeile zu sehen.

**Schnellzugriff:** Klick auf ein System in der Karte des Universums.

### SYSI – Systeminformationen {#sysi}

`SYSI [System-ID]`

Zeigt Name, Sternenklasse, Mikrometeoriten-Dichte und Fraktionszugehörigkeit eines Systems sowie eine Liste seiner Planeten und Stationen. Eine System-ID besteht aus der Sektor-ID (zwei Buchstaben) und der Systemnummer, zum Beispiel `XK-745`. Ohne ID können Sie nach Systemen suchen.

### PLI – Planeteninformationen {#pli}

`PLI [Planeten-ID]`

Zeigt einen Planeten: die Ressourcen im Boden und in der Atmosphäre, seine Fruchtbarkeit sowie Typ und Temperatur, die bestimmen, ob eine Basis [zusätzliche Baumaterialien](../building-costs) benötigt. Enthält außerdem Links zu Ihrer Flotte und Ihren Beständen auf dem Planeten. Eine Planeten-ID besteht aus der System-ID gefolgt von einem Buchstaben, zum Beispiel `XK-745a`. Ohne ID können Sie nach Planeten suchen.

Der Fruchtbarkeitsbalken beginnt in der Mitte: Je weiter er nach links reicht, desto unfruchtbarer ist der Planet, je weiter nach rechts, desto fruchtbarer.

Klicken Sie auf eine farbige Parzelle, um Details zu sehen:

* Blau: andere Unternehmen
* Dunkelblau: Projekt eines anderen Konzerns
* Gelb: Ihr Unternehmen
* Dunkelgelb: Projekt Ihres Konzerns
* Grün: Globale Handelskammer
* Rot: Warenbörse

**Schnellzugriff:** Klick auf einen Planeten in einer Systemkarte.

### STNS – Stationen {#stns}

`STNS [Stations-ID]`

Listet alle Raumstationen auf oder zeigt die öffentlichen Informationen und die Infrastruktur einer Station.

**Schnellzugriff:** Klick auf eine Station (quadratisches Symbol) in einer Systemkarte oder in `PLI`.

## Planetare Projekte {#planetary-projects}

### PPS – Planetare Projekte {#pps}

`PPS <Planeten-ID>`

Listet alle planetaren Projekte eines Planeten auf.

### PP – Planetares Projekt {#pp}

`PP <Planeten-ID> <Projekt-ID>`

Zeigt ein planetares Projekt. Einfacher öffnen Sie es über die Schaltfläche DETAILS in `PPS`.

### PPI – Parzelleninformationen {#ppi}

`PPI <Parzellen-ID>`

Zeigt Informationen über eine Parzelle auf der Oberfläche eines Planeten.

### POPR – Bevölkerungsbericht {#popr}

`POPR <Planeten-ID>`

Zeigt die Bevölkerungsberichte eines Planeten: Größe, Bedürfniserfüllung und Wachstum der Bevölkerung.

### WAR – Lagerhaus {#war}

`WAR <Planeten- oder Stations-ID>`

Zeigt öffentliche und private Informationen zu Lagerhäusern, etwa die verfügbaren Lager-Einheiten und die Mietgebühren.

## Infrastruktur {#infrastructure}

Siehe [Infrastruktur](../infrastructure) und [Sprungtore](../infrastructure-gateway).

### INF – Infrastruktur {#inf}

`INF [System-ID]`

Listet die Infrastruktur der Planeten eines Systems auf, einschließlich planetarer Projekte.

### INFU – Infrastruktur-Instandhaltung {#infu}

`INFU <Infrastruktur-ID>`

Zeigt die Instandhaltung einer Infrastruktur: die pro wöchentlicher Instandhaltungsphase benötigten Materialien, die aktuelle Phase und einen Verlauf vergangener Phasen. Siehe [Infrastrukturverwaltung](../infrastructure/#infrastructure-management).

### ASTS – Assets {#asts}

`ASTS`

Listet Infrastrukturprojekte im Bau, eigene Infrastruktur und selbst errichtete Infrastruktur auf. Die Liste hängt vom Kontext ab: Ein Unternehmen besitzt nie Infrastruktur, eine Regierung errichtet nie selbst welche. Siehe [Assets](../infrastructure/#assets).

### GTW – Sprungtore {#gtw}

`GTW [System-, Planeten- oder Sprungtor-ID]`

Listet alle Sprungtore auf oder nur die in einem System oder bei einem Planeten, zum Beispiel `GTW LS-300` oder `GTW LS-300c`. Mit einer Sprungtor-ID werden die Details dieses Sprungtors angezeigt.

### GTWI – Sprungtor-Informationen {#gtwi}

`GTWI`

Plant neue Sprungtore und Ausbauten bestehender Sprungtore. Zeigt Kapazität, Volumen und Distanz einer Konfiguration, die Bau- oder Ausbaukosten, die wöchentliche Instandhaltung und die Systeme in Reichweite. Siehe [Design und Bau von Sprungtoren](../infrastructure-gateway/#gateway-design-and-construction).

### GTWT – Sprungtor-Verkehr {#gtwt}

`GTWT <Sprungtor-ID>`

Zeigt Verkehr und Treibstoff eines Sprungtors: Sprünge der letzten 24 Stunden, die aktuelle Kapazität, den verfügbaren Treibstoff, die Treibstoff-Auftragnehmer sowie ausgehende und eingehende Sprünge pro Phase, einschließlich fehlgeschlagener Sprünge und ihrer Gründe. Siehe [Sprungtor-Verkehr](../infrastructure-gateway/#gateway-traffic).

## Politik {#politics}

### ADM – Planetare Verwaltung {#adm}

`ADM <Planeten-ID>`

Zeigt die [Planetare Verwaltung](../planetary-projects/#administration-center) eines Planeten: den aktuellen Gouverneur, die Fraktion oder den Konzern, der Gebühren und Steuern einzieht, und die KandidatInnen für die nächste Amtszeit. Hier kann jeder für das Gouverneursamt kandidieren, und die BewohnerInnen des Planeten stimmen hier ab.

### GOV – Regierung {#gov}

`GOV <Planeten-ID>`

Zeigt die aktuelle und die vorherigen Regierungen eines Planeten sowie die Anträge, über die sie abgestimmt haben.

### LR – Lokale Gesetze {#lr}

`LR <Planeten-ID>`

Zeigt die [Lokalen Gesetze](../local-rules) eines Planeten mit Planetarer Verwaltung, etwa Produktionsgebühren und Gebühren für Anzeigen auf lokalen Marktplätzen.

### MOTS – Anträge {#mots}

`MOTS [Antrags-ID]`

Listet die Anträge des aktuell aktiven Regierungskontexts auf.

### MOT – Antrag {#mot}

`MOT <Planetare Verwaltung> <Antrags-ID>`

Zeigt einen Antrag mit seinen Komponenten, dem aktuellen Status und den Stimmen.

### POL – Politische Ämter {#pol}

`POL [Nutzername]`

Zeigt die aktuellen und vergangenen politischen Ämter eines Nutzers bzw. einer Nutzerin, einschließlich laufender Kandidaturen.

## Soziales {#social}

### FA – Fraktion {#fa}

`FA <Fraktionscode>`

Zeigt Informationen über eine Fraktion.

### CO – Unternehmen {#co}

`CO <Firmencode>`

Zeigt Informationen über ein Unternehmen, einschließlich der Firmenleitung, die Sie von hier aus kontaktieren können.

### USR – Nutzer {#usr}

`USR <Nutzername>`

Zeigt das Unternehmen, das Registrierungsdatum und den Online-Status eines Nutzerkontos. NUTZER STUMMSCHALTEN blendet alle Nachrichten dieser Person für Sie aus.

**Schnellzugriff:** Klick auf die Geschäftsführung in `CO`.

### BDGS – Abzeichen {#bdgs}

`BDGS`

Listet alle Nutzerabzeichen auf und erklärt, wofür sie stehen.

### CONS – Nutzer online {#cons}

`CONS`

Zeigt, wer gerade in APEX online ist.

**Schnellzugriff:** die Schaltfläche CONS unten rechts in APEX.

### COM – Kanäle {#com}

`COM`

Listet die Kanäle auf, denen Sie beigetreten sind. Wenn Sie einen Kanal öffnen, treten Sie ihm bei. Um ihn zu verlassen, öffnen Sie den Kanal und wählen Sie VERLASSEN.

### COMC – Kanalkatalog {#comc}

`COMC`

Listet alle öffentlichen Kanäle auf. Wählen Sie einen aus, um ihm beizutreten.

### COMP – Öffentlicher Kanal {#comp}

`COMP <Kanal>`

Öffnet einen öffentlichen Kanal wie "global" oder "help". Öffentliche Kanäle können nicht erstellt werden.

### COMG – Gruppenchat {#comg}

`COMG <Kanal>`

Öffnet einen privaten Gruppenchat. Wenn er noch nicht existiert oder Sie ihm noch nicht beigetreten sind, öffnen Sie ihn über "Konversation beginnen".

**Schnellzugriff:** die Schaltfläche NEUE GRUPPE in `COM`.

### COMU – Privatchat {#comu}

`COMU <Nutzername>`

Startet eine private Unterhaltung mit einem Nutzer bzw. einer Nutzerin.

**Schnellzugriff:** die Schaltfläche NEUER PRIVATKANAL in `COM`.

## Benachrichtigungen {#notifications}

### NOTS – Benachrichtigungen {#nots}

`NOTS`

Listet Ihre In-Game-Benachrichtigungen auf. Klicken Sie auf eine, um Details zu sehen.

### NOTIG – In-Game-Benachrichtigungseinstellungen {#notig}

`NOTIG`

Legt fest, welche Benachrichtigungen in `NOTS` angezeigt werden.

### NOTPNS – Push-Benachrichtigungseinstellungen {#notpns}

`NOTPNS`

Legt fest, welche Benachrichtigungen Ihnen per E-Mail zugesendet werden und wie oft.

## Unternehmen und Finanzen {#company-and-finances}

### FIN – Finanzen {#fin}

`FIN`

Zeigt eine Finanzübersicht und die letzten Bargeldbuchungen.

### FINBS – Bilanz {#finbs}

`FINBS`

Zeigt Ihr Vermögen und Ihre Verbindlichkeiten.

### FINIS – Gewinn- und Verlustrechnung {#finis}

`FINIS`

Zeigt Ihren Gewinn und Verlust.

### FINLA – Liquide Mittel {#finla}

`FINLA`

Zeigt Ihre liquiden Mittel, etwa Bargeld.

### LEAD – Leaderboards {#lead}

`LEAD`

Zeigt Leaderboards auf Unternehmensebene. Wählen Sie das Leaderboard oben aus. Manche bieten zusätzliche Filter, etwa einen Zeitraum.

### ARC – APEX-Repräsentanzzentrum {#arc}

`ARC`

Zeigt das Level Ihres APEX-Repräsentanzzentrums und ermöglicht es Ihnen, Mittel zu seiner Aufwertung beizusteuern.

### GIFT – PRO-Lizenz verschenken {#gift}

`GIFT`

Verschenkt PRO-Lizenzzeit an andere SpielerInnen und listet Ihre gesendeten und erhaltenen Geschenke auf.

### COLIQ – Unternehmen liquidieren {#coliq}

`COLIQ`

Liquidiert Ihr Unternehmen, sodass Sie mit demselben Account von vorne beginnen können. Laden Sie APEX anschließend neu.

Abklingzeiten:

* die erste Liquidation ist direkt nach der Firmengründung verfügbar
* die zweite 3 Tage nach der ersten
* die dritte 21 Tage nach der zweiten
* jede weitere 60 Tage nach der vorherigen

Eine sofortige Liquidation kann möglich sein, wenn Sie weder an einer Warenbörse noch auf einem lokalen Marktplatz gehandelt und nicht zu planetaren oder Konzernprojekten beigetragen haben.

**Ein Missbrauch von `COLIQ` kann zur (vorübergehenden) Sperrung Ihres Kontos führen.**

## Interface und Übertragungen {#interface-and-transmissions}

### CS – Screen erstellen {#cs}

`CS`

Erstellt einen neuen Screen, wie die Schaltfläche NEU oben. Siehe den [Interface-Guide](../../tutorials/current-tutorials/07-interface-guide).

### SCRN – Screens {#scrn}

`SCRN`

Listet Ihre Screens auf. Benennen Sie sie um, kopieren oder löschen Sie sie, und verwalten Sie Screenvariablen.

### LIC – Lizenz {#lic}

`LIC`

Zeigt Ihre aktuelle APEX-Lizenz und wann sie abläuft. Von hier aus können Sie Ihre Lizenz verwalten oder anderen SpielerInnen PRO-Zeit schenken.

### TRA – Übertragungen {#tra}

`TRA`

Listet alle Übertragungen (Video-Tutorials) auf.

### XIT – Greenscreen {#xit}

`XIT [Titel]`

Zeigt einen Greenscreen, mit dem Sie Ihre eigene Übertragung aufzeichnen können, optional mit Titel.

### XYTV – YouTube-Video {#xytv}

`XYTV <Video-ID>`

Bettet ein YouTube-Video ein. Die ID ist der Teil nach `v=` in der URL des Videos.

{{% about-this-page %}}

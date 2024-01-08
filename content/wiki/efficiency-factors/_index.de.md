---
title: "Effizienzfaktoren"
date: 2018-09-18T17:13:49+02:00
weight: 3
---

## Allgemeine Informationen

Jede Produktionslinie arbeitet im aktiven Zustand mit einer bestimmten Effizienz. Die Effizienz bestimmt, wie lange die Fertigstellung eines Produktionsauftrags dauert: Eine geringere Effizienz führt zu längeren Produktionszeiten, eine höhere Effizienz verkürzt sie. Die aktuelle Effizienz einer Produktionslinie kann im Buffer zur Produktionswarteschlange (PRODQ) nachgeschlagen werden:

![PRODQ](prodq.png)

Der Gebäudezustand, die Verfügbarkeit der Arbeitskräfte sowie die Zufriedenheit liefern den Basiseffizienzwert. ExpertInnen gewähren für Produktionslinien in ihrem Fachgebiet Prämien in dieser Höhe. Aktive CoGC-Programme können auch bestimmten Branchen oder Arbeitnehmertypen zugute kommen. Schließlich bietet die Bodenfruchtbarkeit (oder deren Abwesenheit) einen weiteren Bonus (oder Nachteil) für die Effizienz bestimmter Produktionslinien.

### Gebäudezustand

Produktionsgebäude sind gleich nach dem Bau am effizientesten, danach beginnt sich ihr Zustand zu verschlechtern. Mit der Zeit nimmt die Verschlechterung langsam zu, bis das Gebäude nur noch 33% der ursprünglichen Effizienz erreicht und sich nicht mehr verschlechtert. Es ist erwähnenswert, dass alle Gebäude repariert werden können (und sollten), wenn sie zu ineffizient sind.

### Verfügbarkeit der Arbeitskräfte

Jede Produktionslinie beschäftigt eine bestimmte Anzahl und Art von Arbeitskräften, die unter "Belegschaft" im BUI-Fenster angezeigt wird:

![Workforces](workforces.png)

Steht nur ein Teil der benötigten Arbeitskräfte zur Verfügung, kann das Gebäude zwar noch betrieben werden, allerdings mit geringerer Effizienz. Gebäude mit dem gleichen Personalbedarf werden addiert.

Neben der Zufriedenheit (mehr dazu weiter unten) werden im Fenster "Bevölkerung" drei Kennzahlen für jeden Arbeitnehmertyp aufgeführt:
1. Bevölkerungsgröße: Die tatsächliche Anzahl der in Ihrer Basis vorhandenen ArbeiterInnen. Bestimmt die Rate, mit der Versorgungsgüter verbraucht werden.
2. Kapazität: Die Anzahl der ArbeiterInnen, die Ihre Basis derzeit aufnehmen kann.
3. Benötigt: Die Anzahl der ArbeiterInnen, die alle Produktionslinien zusammen beschäftigen können.

![Total workforce](total-workforce.png)

Es gelten folgende Regeln:
- Ist die Kapazität kleiner als erforderlich, wird die Effizienz aller Produktionslinien, die die entsprechende Art von Arbeitskräften erfordern, negativ beeinflusst. Genauer gesagt wird die Effizienz mit dem Prozentsatz der verfügbaren Arbeitskräfte multipliziert, d.h.: Effizienz x (Belegschaftsgröße / Benötigt)
- Ist die Kapazität größer als erforderlich, werden die Wohnmodule nicht vollständig gefüllt, die tatsächliche Anzahl der anwesenden ArbeiterInnen – die Bevölkerungsgröße – liegt also unter der Kapazität.
- Alle Produktionslinien beschäftigen MitarbeiterInnen, auch wenn keine Bestellungen in der Warteschlange sind oder die Produktion gestoppt ist. Untätige ArbeiterInnen können nicht von einem Gebäude in ein anderes versetzt werden.

### Zufriedenheit der Belegschaft

Jeder Arbeitnehmertyp hat seine eigenen Bedürfnisse, die erfüllt werden müssen, um die Effizienz aufrechtzuerhalten. Der Bedarf an ArbeiterInnen kann im Belegschaftsfenster einer Basis nachgeschlagen werden. Beispielsweise benötigen 100 Pioniere 4 DW, 4 RAT, 0,5 OVE, 0,5 COF und 0,2 PWO pro Tag, um vollständig zufrieden zu sein, während 100 SiedlerInnen 5 DW, 6 RAT, 3 HI, 0,5 EXO und 0,5 PT benötigen.

Die Effizienz bleibt bei 100%, wenn sowohl Luxus- als auch Nicht-Luxusbedürfnisse erfüllt werden, und niedriger, wenn nur das Nötigste verfügbar ist. Pioniere beispielsweise werden zu 79% zufrieden sein, wenn nur DW, RAT und OVE zum Konsum verfügbar sind. Eine Belegschaft wird so lange weiterarbeiten, wie ihnen noch mindestens eine ihrer wesentlichen Ressourcen zur Verfügung steht. Erst wenn alle aufgebraucht sind, wird die Produktion eingestellt. Steht nur ein Teil der benötigten Ressourcen zur Verfügung, sinkt die Zufriedenheit der Belegschaft und damit auch ihre Produktivität.

Manche Versorgungsgüter sind nicht essentiell: Der Produktivitätsverlust durch ein fehlendes, nicht essentielles Versorgungsgut ist geringer als bei essentiellen Versorgungsgütern. Eine Belegschaft wird ihre Arbeit ganz einstellen, wenn das einzige Versorgungsgut, das ihr zur Verfügung steht, nicht essentiell ist. Das Belegschaftsfenster listet auf, welche Versorgungsgüter wichtig sind und welche nicht:

![Non-essentials](non-essentials.png)

#### Wie Versorgungsgüter verbraucht werden

Die erste volle Menge eines Versorgungsguts, das für die folgenden 24 Stunden benötigt wird (z.B. 4 RAT für 100 Pioniere), wird von der Bevölkerung einer Basis beansprucht (und verschwindet somit aus dem Inventar), sobald die Ware im Inventar der Basis verfügbar wird. Das Gleiche passiert 24 Stunden später noch einmal, immer wieder, bis das Versorgungsgut aufgebraucht ist. Dies gilt für jede Art von Versorgungsgut: Wenn eine Bevölkerung um 12:00 Uhr DW und um 16:00 Uhr RAT zu verbrauchen beginnt, ist die nächste DW-Charge am nächsten Tag um 12:00 Uhr aufgebraucht und die nächste RAT-Charge um 16 Uhr am nächsten Tag.

__Hinweis: Es muss keine Produktion laufen, damit eine Bevölkerung Ressourcen verbraucht!__ Untätige Arbeitskräfte haben genau die gleichen Bedürfnisse wie aktive und verbrauchen dennoch Versorgungsgüter im Inventar der Basis.

![Pioneers and Settlers](pioneers-and-settlers.png)

### ExpertInnen

Alle Gebäude können von sogenannten ExpertInnen mit Boni versehen werden. Sie können Ihre ExpertInnen einsehen, indem Sie in Ihrer Basis auf die Schaltfläche EXPERTEN klicken. Um sie einzusetzen, klicken Sie auf AKTIVIEREN, um ihren Bonus zu entfernen, klicken Sie auf ENTFERNEN.

![Experts](experts.png)

Jede Expertin / jeder Experte gewährt einer bestimmten Industrie einen Bonus. Jede Industrie umfasst wiederum unterschiedliche Gebäude:

| Expertise	   			| Gebäude (+ BUI-Ticker)														|
|-----------------------|-------------------------------------------------------------------			|
| Ressourcengewinnung	| Gasanlage (COL), Extraktor (EXT), Förderanlage (RIG), Verbrennungsanlage (INC)				|
| Fertigung  		| Fabrik für Basismaterialien (BMP), Textilmanufaktur (CLF), 3D-Druckerei (PPF), Weberei (WPL), Komponentenfertigung (MCA), Kleinstkomponenten-Fertigung (SCA), Raumfahrt-Fertigbauteile-Fabrik (SPP), Anwendergerätefabrik (APF), Fortgeschrittene Anwendergerätefabrik (AAF), Raumfahrt-Antriebsfabrik (SPF)	|
| Landwirtschaft  			| Farm (FRM), Hydroponik-Farm (HYF), Plantage (ORC)        				|
| Lebensmittelindustrie		| Nahrungsverarbeitung (FP), Fermenter (FER), Lebensmittellabor (IVP)                     |
| Bauwesen			| Fertigbauteile-Fabrik MK1 (PP1), Schweißerei (WEL), Fertigbauteile-Fabrik MK2 (PP2), Fabrik für Fertigmodule (UPF), Fertigbauteile-Fabrik MK3 (PP3), Fertigbauteile-Fabrik MK4 (PP4) |
| Metallurgie			| Schmelzerei (SME), Feinschmiede (FS), Glasofen (GF), Schiffsrumpf-Schweißerei (HWP), Schiffsbausatz-Fertigung (SKF), Hochenergieofen (ASM) |
| Chemie				| Chemiefabrik (CHP), Polymer-Fabrik (POL), Chemielabor (LAB), Medikamentenfabrik (PHF), Technetium-Verarbeitung (TNP), Labor für komplexe Materialien (AML), Einsteinium-Anreicherung (EEP) |
| Treibstoffherstellung | Raffinerie (REF) |
| Elektronik			| Fabrik für Elektrogeräte (EDM), Reinraum (CLR), Energiekomponenten-Fertigung (ECA), Elektronikfabrik (ELP), Softwareentwicklung (SD), Dronenfertigung (DRS), Software-Labor (SL) |


#### ExpertInnen: Spawnraten und Boni

Die ersten ExpertInnen eines Unternehmens sind im [Starterpaket](../packages-factions) enthalten, alle weiteren ExpertInnen kommen im Laufe der Zeit dazu. __Wenn man eine Produktionslinie am Laufen hält__, entsteht eine neue Expertin / ein neuer Experte auf ihrem / seinem Gebiet. Durch die Produktion von Gütern auf einer Farm entstehen mit der Zeit LandwirtschaftsexpertInnen. Sobald in einer bestimmten Industrie insgesamt 5 ExpertInnen erreicht sind, werden in dieser Industrie keine neuen ExpertInnen geschaffen. Pro Industrie können insgesamt 5 ExpertInnen und industrieübergreifend in einer Basis insgesamt 6 ExpertInnen gleichzeitig aktiv sein.

| Experte Nr.	| Nötige Tage   | Bonus		   |
|---------------|---------------|--------------|
| 1			   	| 10.00 		| 3.06%	   	   |
| 2			   	| 12.50		   	| 6.96%	 	   |
| 3			   	| 57.57		   	| 12.48%	   |
| 4			   	| 276.50	   	| 19.74%	   |
| 5			   	| 915.10	   	| 28.40%	   |

Die oben angegebenen Tage beziehen sich auf ein einzelnes Gebäude mit 100% Effizienz. Der Betrieb von zwei Gebäuden in der gleichen Industrie (d.h. im gleichen Feld der Expertise) halbiert die erforderliche Zeit, der Betrieb von drei Gebäuden reduziert sie auf ein Drittel usw. Dies geschieht auch, wenn beide Gebäude Teil derselben Produktionslinie sind, d.h. zwei (drei, vier, fünf ...) Farmen verkürzen die Zeit gleichermaßen.

Beachten Sie, dass die **Anzahl der erforderlichen Tage** nach jeder Expertin / jedem Experten zurückgesetzt wird. Der Übergang von 0 auf 2 ExpertInnen wird also 22,50 Tage dauern.

Der von einer Expertin / einem Experten gewährte Bonus ist ein fester Wert, der mit der Effizienz der Belegschaft multipliziert wird. Beispielsweise erreicht eine Belegschaft, die mit einer Effizienz von 90% arbeitet, eine Effizienz von 101,2%, sobald drei ExpertInnen in der Basis aktiviert werden. `90% * (100% + 12,48%) = 101,2%`

### Bodenfruchtbarkeit

Die Effizienz bestimmter Gebäude wird von der Bodenfruchtbarkeit eines Planeten beeinflusst. Ist dies der Fall, wird dies neben dem Gebäudeeintrag im BSC-Fenster angezeigt. Die Gebäude, die derzeit fruchtbaren Boden benötigen, sind Farmen (FRM) und Plantagen (ORC).

![Fertile soil](fertile-soil.png)

Die Bodenfruchtbarkeit eines Planeten kann im PLI-Fenster angezeigt werden. Je weiter der gelbe Teil des Balkens nach rechts reicht, desto fruchtbarer ist der Planet, je weiter es nach links reicht, desto niedriger ist der Fruchtbarkeitswert. __Hinweis: Wenn anstelle eines Balkens zwei Striche angezeigt werden, ist der Planet unfruchtbar, was bedeutet, dass Gebäude, die von der Bodenfruchtbarkeit betroffen sind, hier überhaupt nicht betrieben werden können.__

![Soil fertility](soil-fertility.png)

Neutrale Fruchtbarkeit (d.h. kein Gelb) weist auf einen Modifikator von +0% hin. Eine schlechte Fruchtbarkeit (gelb links von der Mitte) ist ein negativer Modifikator, während eine hohe Fruchtbarkeit (gelb rechts von der Mitte) ein positiver Modifikator ist. Je weiter der gelbe Balken reicht, desto größer ist die Auswirkung, mit einer maximalen Spanne von etwa -33% bis +33%.

### CoGC-Programme

Die [Globale Handelskammer](../../tutorials/planetary-projects#chamber-of-global-commerce-cogc) kann, sofern sie auf einem Planeten existiert und aktiv ist, einen vorübergehenden Produktivitätsbonus bieten. Wie bei ExpertInnen üblich, wird der jeweilige Prozentsatz einfach hinzuaddiert. Beispielsweise gewährt das CoGC-Programm "Bildungsinitiative: Pioniere" einen Bonus von 10% auf alle von Pionieren betriebenen Gebäude, solange es aktiv ist, und das Programm "Werbekampagne: Landwirtschaft" einen Bonus von 25% auf alle Einrichtungen im Agrarsektor.

{{% about-this-page %}}

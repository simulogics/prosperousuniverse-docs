---
title: "Command-Liste"
date: 2018-09-18T17:13:49+02:00
weight: 2
---

Dies ist eine umfassende Liste aller Commands, die Ihnen in APEX zur Verfügung stehen. Sie sind nach ihren jeweiligen Einsatzgebieten gruppiert. Um diese Liste zu verstehen, müssen Sie bereits mit der [Funktionsweise von Commands](../../tutorials/commands) vertraut sein. Sie können die gesamte Liste durchlesen, um sich einen Überblick zu verschaffen, oder sie als Referenz zum Nachschlagen bestimmter Befehle verwenden.

## Grundlegende Commands

__BS__  
_Optionaler Parameter: Basis-ID_  
Öffnet einen Überblick all Ihrer Basen. Zeigt weitere Informationen zu einer konkreten Basis an, wenn eine Basis-ID folgt, z.B. indem Sie im allgemeinen BS-Fenster auf "Basis anzeigen" klicken. Bietet Zugriff auf die meisten anderen basisbezogenen Befehle.

__BSC__  
_Obligatorischer Parameter: Planeten-ID_  
Ermöglicht die Erstellung einer neuen Basis auf einem Planeten. Zeigt notwendige Baumaterialien und ermöglicht die Auswahl einer Parzelle auf der Oberfläche. 

__BSL__  
_Obligatorischer Parameter: Basis-ID_  
Öffnet eine Übersicht der Gebäude in einer bestimmten Basis. Zugriff über die Schaltfläche GEBÄUDE in einem konkreten BS-Fenster. Klicken Sie auf "ABREISSEN", um ein Gebäude zu zerstören. Dadurch erhalten Sie je nach Alter einen Teil der für den Bau aufgewendeten Ressourcen zurück. Die erstatteten Materialien werden unter "Zurückgewinnbare Baumaterialien" aufgeführt.

__BSC__  
_Obligatorischer Parameter: Basis-ID_  
Öffnet das Konstruktionsfenster einer bestimmten Basis. Zugriff über die Schaltfläche "BAUEN" in einem konkreten BS-Fenster. Verwenden Sie die Registerkarten oben, um sich die verschiedenen Gebäudekategorien anzusehen. Unter "Fläche" finden Sie den Flächenbedarf eines Gebäudes sowie (nach dem Schrägstrich) die in Ihrer Basis verfügbare Fläche. Unter "Belegschaft" sehen Sie die Anzahl und Art der Arbeitskräfte, die für den Betrieb dieses Gebäudes erforderlich sind.

__BUI__  
_Obligatorischer Parameter: Gebäude-Ticker_  
Zeigt Informationen zu einem Gebäudetyp an: Welche Art von Arbeitskräften hier beschäftigt sind, wie viel Platz das Gebäude einnimmt und welche Teile beim Bau benötigt werden. Zugriff durch Klicken auf einen Gebäudetyp im BSC-Fenster.

__INV__  
_Optionaler Parameter: Addresse oder Lager-ID_  
Werden keine Parameter angegeben, zeigt dieser Command eine Liste all Ihrer Bestände an, einschließlich der Basislager, Frachträume, Treibstofftanks und Lager-Einheiten. Durch Klicken auf die Schaltfläche "ANZEIGEN" wird der Inhalt des ausgewählten Inventars angezeigt. Oben links finden Sie mehrere Sortiermöglichkeiten (ANZ: Anzahl, MAS: Gewicht, VOL: Volumen). Klicken Sie auf das Symbol links daneben, können Sie zwischen Listen- und Rastermodus umschalten. Letzterer zeigt weitere Informationen zu jeder Ware, wie Gewicht, Volumen und Buchwert.

Enthält der Parameter eine System- oder Planetenadresse (z. B. `INV XK-745` oder `INV XK-745a`), werden nur die Bestände an diesem Standort angezeigt.

__MTRA__  
_Optionaler Parameter: Material-Ticker_  
_Optionaler Parameter: Ursprungslager-ID_  
_Optionaler Parameter: Ziellager-ID_  
Ermöglicht Ihnen, eine bestimmte Menge an Artikeln zwischen zwei Lagern zu übertragen. Das zu übertragende Material sowie die Ursprungs- und Ziellager können über die Parameter des Befehls angegeben oder aus Dropdown-Menüs im Command-Fenster ausgewählt werden. Dieser Command lässt sich auch ausführen (mit vorab ausgefüllten Details zum Transfer), indem Sie ein Element aus dem Ursprungslager in das Ziellager ziehen und es auf dem "AMT"-Slot ablegen.

__WF__  
_Obligatorischer Parameter: Basis-ID_  
Zeigt einen Überblick zur Belegschaft einer Basis, einschließlich deren Bedürfnisse. Je anspruchsvoller die Belegschaftsstufe, desto höher sind ihre Anforderungen. Wenn Sie Ihre Mitarbeitenden nicht mit den benötigten Versorgungsgütern versorgen, sinkt die Effizienz der von ihnen betriebenen Gebäude. Erreichbar über die Schaltfläche "Belegschaft" in einem konkreten BS-Fenster.

__EXP__  
_Obligatorischer Parameter: Basis-ID_  
Listet alle Bereiche auf, die Boni von ExpertInnen erhalten können, und zeigt an, welche ExpertInnen derzeit in der angegebenen Basis eingesetzt werden. Klicken Sie auf "ENTFERNEN", um ExpertInnen zu deaktivieren, die dann in der Spalte ganz rechts als verfügbar aufgeführt werden. Klicken Sie auf "AKTIVIEREN", um sie wieder an die Arbeit zu schicken. Erreichbar über die Schaltfläche "Experten" in einem konkreten BS-Fenster.  

## Produktionslinien-Commands

__PROD__  
_Obligatorischer Parameter: Basis-ID_  
Zeigt die Produktionslinien einer bestimmten Basis. Erreichbar über die Schaltfläche "Produktion" in einem konkreten BS-Fenster. Jede Produktionslinie kann aus einem oder mehreren Gebäuden desselben Typs bestehen.

__PRODQ__  
_Obligatorischer Parameter: Produktionslinien-ID_  
Ermöglicht Ihnen, in der Warteschlange befindliche Aufträge zu stornieren, jedoch nicht diejenigen, die bereits verarbeitet werden. Der Effizienzwert wird von mehreren Faktoren beeinflusst, darunter der Zufriedenheit Ihrer Mitarbeitenden, dem von ExpertInnen bereitgestellten Bonus und in einigen Fällen der Bodenfruchtbarkeit des Planeten. Zugriff über die Schaltfläche "Details" in einem PROD-Fenster.

__PRODCO__  
_Obligatorischer Parameter: Produktionslinien-ID_  
Ermöglicht Ihnen, einen neuen Produktionsauftrag zu erteilen. Wählen Sie im Dropdown-Menü einen Primär-Output aus, legen Sie eine Auftragsgröße fest und stellen Sie Ihre Bestellung in die Warteschlange. Wenn für Ihre Bestellung Input-Materialien erforderlich sind (wie unten gezeigt), stellen Sie zunächst sicher, dass diese verfügbar sind. Zugriff über die Schaltfläche "AUFTRAG ERSTELLEN" in einem PROD-Fenster.

__HQ__  
_Keine möglichen Parameter_  
Zeigt Ihnen, welche Ihrer Basen derzeit Ihr Firmensitz ist, und ermöglicht Ihnen, Ihren Hauptsitz an eine andere Basis zu verlegen, um andere Fraktionsboni zu erhalten. Außerdem können Sie hier Ihren Hauptsitz ausbauen, um zusätzliche Basisgenehmigungen und Slots in der Produktionswarteschlange freizuschalten.

__BRA__  
_Optionaler Parameter: Planeten-ID_
Ermöglicht Ihnen, eine Ihrer Basen auszuwählen und mehrere ihrer Gebäude gleichzeitig zu reparieren, indem Sie einen Mindestzustand für das Gebäude festlegen. Alle Gebäude in der ausgewählten Basis, die sich in diesem Zustand befinden oder darunter liegen, werden in die Reparaturen einbezogen.

## Soziale Commands

__FA__  
_Obligatorischer Parameter: Fraktionscode_  
Zeigt Informationen zur angegebenen Fraktion an.

__CO__  
_Obligatorischer Parameter: Firmencode_  
Zeigt Informationen zum angegebenen Unternehmen an. (Hier kommt der vierstellige Code zum Einsatz, den Sie gleich zu Beginn für Ihr Unternehmen gewählt haben.) Ermöglicht unter anderem, Firmenleitung einzusehen und zu kontaktieren.

__USR__  
_Obligatorischer Parameter: User name_  
Zeigt das Unternehmen, das Registrierungsdatum und den Verbindungsstatus eines Benutzerkontos an. Erreichbar über die Spalte "Geschäftsführer" in einem CO-Fenster. Durch Klicken auf die Schaltfläche "NUTZER STUMMSCHALTEN" werden alle Nachrichten, die diese Person sendet, für Sie unsichtbar.

__COM__  
_Keine möglichen Parameter_  
Listet alle Kommunikationskanäle auf, denen Sie in der Vergangenheit beigetreten sind. Sie treten automatisch einem Kanal bei, wenn Sie zum ersten Mal darauf klicken. Um einen Kanal wieder zu verlassen, öffnen Sie ihn und wählen Sie "VERLASSEN".

__COMC__  
_Keine möglichen Parameter_  
Listet alle öffentlichen Kommunikationskanäle auf. Sie können einem Kanal beitreten, indem Sie ihn aus der Liste auswählen.

__COMG__  
_Obligatorischer Parameter: Kanal-ID_  
Öffnet einen privaten Gruppenchat. Sind Sie diesem zuvor bereits beigetreten, wird er durch die Eingabe des Namens direkt geöffnet. Wenn Sie den Namen eines Raums eingeben, der noch nicht existiert oder den Sie noch nicht betreten haben, öffnen Sie den Chat über "Konversation beginnen". Auch über die Schaltfläche "NEUE GRUPPE" im COM-Fenster erreichbar.

__COMP__  
_Obligatorischer Parameter: Kanal-ID_  
Öffnet einen bestehenden öffentlichen Chat wie "Global" oder "Hilfe". Sie können keinen neuen öffentlichen Chat erstellen.

__COMU__  
_Obligatorischer Parameter: Nutzername_  
Startet ein privates Zwei-Personen-Gespräch mit dem angegebenen Benutzerkonto. Beginnen Sie mit der Eingabe des Kontonamens, bis er in der Liste angezeigt wird, und klicken Sie dann darauf. Erreichbar über die Schaltfläche "NEUER PRIVATKANAL" im COM-Fenster.

__CONS__  
_Keine möglichen Parameter_  
Zeigt Ihnen, wer gerade in APEX online ist. Zugriff über die Schaltfläche "CONS" unten rechts in APEX.

## Vertrags-Commands

__CONT__  
_Obligatorischer Parameter: Vertrags-ID_  
Mit diesem Befehl können Sie einen bestimmten Vertrag anzeigen. Nach dem Command muss ein langer und komplexer Parameter folgen, der den Vertrag identifiziert. Aus diesem Grund wird allgemein empfohlen, den Befehl "CONTS" zu verwenden und dann auf den/die gewünschten Vertrag/Verträge zu klicken.

__CONTS__  
_Keine möglichen Parameter_  
Zeigt eine Liste all Ihrer Verträge von Warenbörsen und lokalen Marktplätzen an. Klicken Sie auf einen beliebigen Vertrag, um seinen CONT-Buffer zu öffnen. Beachten Sie, dass Sie ausstehende Verträge auch anzeigen können, indem Sie sie aus der Liste in der rechten Seitenleiste auswählen. (Wenn Sie die Seitenleiste nicht sehen können, schalten Sie sie mit der SEITL-Schaltfläche auf der linken Seite ein.) Erfahren Sie mehr über Verträge in den Tutorials "Handel" und "Lokale Marktplätze".

__CONTD__
_Optionaler Parameter: Vertrags-ID_
Zeigt eine Liste aller Ihrer Vertragsentwürfe an. Wenn Sie eine Vertrags-ID angeben oder auf einen Entwurf klicken, wird die Detailansicht des Entwurfs geöffnet, in der der Entwurf bearbeitet und versendet werden kann.

## Warenbörsen-Commands
Die folgenden Commands beziehen sich auf Warenbörsen. Die ersten beiden sind wahrscheinlich die nützlichsten.

__CXOS__  
_Keine möglichen Parameter_  
Zeigt einen Verlauf Ihrer Ver- und Ankaufsorders an, den Sie hier anzeigen und löschen können. Durch das Löschen einer noch nicht oder zumindest nicht vollständig ausgeführten Order ziehen Sie diese vom Markt zurück.

__CXO__  
_Obligatorischer Parameter: Vertrags-ID_  
Zeigt Informationen zu einer Order an, die Sie in der Vergangenheit getätigt haben. Zugriff über die "ANSEHEN"-Schaltflächen im CXOS-Fenster.

__CXL__  
_Keine möglichen Parameter_  
Listet alle vorhandenen Warenbörsen auf. Von hier aus können Sie schnell auf eine konkrete Warenbörse zugreifen, ohne sich deren spezielle Parameter für den CX-Befehl merken zu müssen.

__CXM__  
_Obligatorischer Parameter: Material-Ticker_  
_Optionaler Parameter: Planeten-ID_  
Vergleicht Warenbörseninformationen für das angegebene Material über alle Warenbörsen hinweg. Die Börsen werden nach ihrer Entfernung zum angegebenen Planeten sortiert (falls einer eingegeben wurde).

__CX__  
_Obligatorischer Parameter: Warenbörsen-ID_  
Hier können Sie Artikel auf einem bestimmten Markt kaufen und verkaufen. Wählen Sie im Dropdown-Menü die Warenkategorie aus. Zugriff zum Beispiel durch Klicken auf den Namen einer Warenbörse im CXL-Fenster.

__MAT__  
_Obligatorischer Parameter: material ID_  
Materialien und Waren sind im Wesentlichen dasselbe. Ihr Ticker ist die aus zwei oder drei Buchstaben bestehende Kennung, die auch im Symbol des Materials bzw. der Ware auftaucht. Der Ticker für Stahl lautet beispielsweise STL. "Verarbeitung" gibt an, was aus diesem Material in welcher Produktionslinie hergestellt werden kann, während "Produktion" zeigt, wie und wo das Material hergestellt werden kann. Zugriff zum Beispiel durch Klicken auf das Symbol einer Ware im CX-Fenster.

__CXP, CXPC, CXOB, CXPO__  
_Obligatorischer Parameter: Waren-ID + Warenbörsen-ID_  
Diese vier Befehle beziehen sich auf konkrete Waren auf einem konkreten Markt. Neben einem Wareneintrag im CX-Fenster finden Sie die Schaltflächen "INFO", "CHART", "ORDERS" und "HANDEL". "INFO": CXP, das einen Überblick über aktuelle Gebote, angebotene Mengen, Allzeit-Hoch und -Tiefs usw. zeigt. "CHART": CXPC. Zeigt ein Kerzenchart des Warenpreises im Zeitverlauf. Wenn "Keine Daten" angezeigt wird, wurde die Ware im angegebenen Zeitraum nicht verkauft. Wählen Sie ein längeres Zeitfenster, um das Problem zu beheben. "ORDERS": CXOB-Command, mit dem Sie ausstehende Anfragen und Angebote sehen können. "TRADE": CXPO, mit dem Sie Kauf- und Verkaufsorders innerhalb der aktuellen Preisspanne platzieren können. Letztere wird anhand eines Drei-Tage-Durchschnitts ermittelt und ist für BenutzerInnen mit PRO-Lizenz breiter als für Konten mit FREE-Lizenz. Um schnell den aktuell niedrigsten Ankaufs- oder Verkaufspreis festzulegen, verwenden Sie die Schaltflächen "setzen" in der Zeile „Ankauf / Verkauf". In der Zeile "Lagerort" können Sie den Lagerort auswählen, von dem aus Sie Ihre Waren verkaufen möchten.

## Weltraumflug-Commands
Es wird empfohlen, den FLT-Befehl zu verwenden und von dort aus auf die anderen Befehle zuzugreifen. Um all diese Befehle in Aktion zu sehen, werfen Sie einen Blick auf das Tutorial "Aufrechterhaltung der Basis und Flug".

__FLT__  
_Optionaler Parameter: System-ID / Planeten-ID_  
Der Flotten-Commandl wird einzeln eingegeben und zeigt all Ihre Schiffe an. In jeder Zeile werden Daten zu einem Ihrer Schiffe angezeigt, z.B. dessen Transpondercode, Name, Status, Füllstand und Standort sowie Informationen zu einem laufenden Flug. Wenn Sie nach dem Flotten-Command die ID eines Systems oder Planeten eingeben, werden all Ihre Schiffe angezeigt, die derzeit dort stationiert sind. (Die ID ist der Parameter, den Sie oben in einem Buffer sehen können, wenn Sie ein System in der Karte des Universums oder einen Planeten in einer Systemkarte auswählen.)

__SHP__  
_Obligatorischer Parameter: Schiffstranspondercode_  
Zeigt Informationen zu einem Ihrer Schiffe an. Benennen Sie Ihr Schiff um, indem Sie auf seinen aktuellen Namen (oder "unbenannt") klicken und einen neuen Namen eingeben. Zugriff durch Klicken auf den Transpondercode eines Schiffes im FLT-Fenster.

__SHPF__  
_Obligatorischer Parameter: Schiffstranspondercode_  
Zeigt den Treibstoffstatus eines Schiffes an. Zugriff durch Klicken auf die Treibstoffleiste eines Schiffes im FLT-Fenster.

__SHPI__  
_Obligatorischer Parameter: Schiffstranspondercode_  
Zeigt den Bestand eines Schiffes an, der durch Gewicht und Volumen seiner Ladung begrenzt ist. Zugriff durch Klicken auf die Inventarleiste eines Schiffes im FLT-Fenster.

__SFC__  
_Obligatorischer Parameter: Schiffstranspondercode_  
Die Schaltfläche "STARTEN" neben jedem Schiff in der FLT-Liste ruft den SFC-Command gefolgt vom Transpondercode des Schiffs auf. Wenn Sie eine Planeten-ID oder Stations-ID im Bereich "Ziel" eingeben, den gewünschten Treibstoffverbrauch festlegen und auf "Start" klicken, können Sie ein Schiff zu einem neuen Ziel schicken.

__SI__  
_Obligatorischer Parameter: Schiffstranspondercode_  
Zeigt alle öffentlichen Informationen zu dem ausgewählten Schiff an. Zugriff durch Klicken auf ein dreieckiges Schiffssymbol in einer Systemkarte oder einem Planeteninfofenster.

## Schiffsbau-Commands

__BLU__
_Optionaler Parameter: Blueprint-ID_
Öffnet eine Liste all Ihrer Schiffsentwürfe oder eines bestimmten Entwurfs, wenn eine ID angegeben wurde.

__SHY__
_Obligatorischer Parameter: Planeten-ID_
Öffnet den Schiffswerft-Buffer des gewünschten Planeten.

__SHYP__
_Obligatorischer Parameter: Projekt-ID_
Öffnet das gewünschte Schiffbauprojekt.

## Devisenhandel-Commands

__FX__  
_Keine möglichen Parameter_  
FX zeigt Ihnen eine Wechselkursmatrix, in der Sie sehen können, wie viel eine Währung im Vergleich zu einer anderen wert ist. Die Basiswährungen sind vertikal angeordnet, die Notierungswährungen horizontal.

__FXP__  
_Obligatorischer Parameter: Währungspaar-Ticker_  
Verwenden Sie FXP in Kombination mit einem Ticker aus zwei Währungskennungen, getrennt durch einen Schrägstrich oder Punkt, zum Beispiel: FXP AIC/CIS. Alternativ klicken Sie einfach auf den entsprechenden Wert in der FX-Matrix.

__FXOB__  
_Obligatorischer Parameter: Währungspaar-Ticker_  
Verwenden Sie diesen Befehl, um offene Orders eines beliebigen Währungspaares anzuzeigen, zum Beispiel: FXOB AIC/CIS.

__FXPC__  
_Obligatorischer Parameter: Währungspaar-Ticker_  
Zeigt den Wechselkursverlauf eines beliebigen Währungspaares an, zum Beispiel: FXPC AIC/CIS.

__FXPO__  
_Obligatorischer Parameter: Währungspaar-Ticker_  
Verwenden Sie diesen Befehl, um eine Devisenhandelorder zu erteilen, d.h. eine Währung auszugeben, um eine andere zu kaufen. Geben Sie FXPO gefolgt vom gewünschten Ticker ein, zum Beispiel AIC/NCC. Wählen Sie anschließend die entsprechende Registerkarte aus, um die gewünschte Währung zu kaufen oder zu verkaufen. Beachten Sie, dass es sich bei den von Ihnen angegebenen Zahlen um Lots handelt, also um 1.000 von jeder Währung.

__FXOS__  
_Keine möglichen Parameter_  
Zeigt alle von Ihnen aufgegebenen Devisenhandelorders an.

## Karten-Commands
Karten können per Drag & Drop mit der linken Maustaste verschoben und mit der rechten Maustaste rotiert werden.

__MU__  
_Obligatorischer Parameter: CX/NAV/INV/POL_  
Öffnet eine der vier verschiedenen Karten des Universums. Sie zeigen alle dasselbe Universum, dienen jedoch unterschiedlichen Zwecken, wie unten beschrieben. Die miteinander verbundenen Punkte auf der Karte sind Sternensysteme. Wenn Sie mit der Maus über ein System fahren, können Sie dessen Kennung sehen. Auf allen Karten können Sie unten die Anzeige verschiedener Arten von Informationen ein- oder ausschalten. Sie können diese Daten auch nach Zeitraum filtern (z.B. 1 Stunde, 12 Stunden, 24 Stunden).

MU CX: Zeigt an, wo Ihre Warenbörsen stattfinden.

MU NAV: Zeigt Verkehrsdaten an. Solange "Flotte" aktiviert ist, werden die Standorte Ihrer Schiffe durch gelbe Pfeile markiert.

MU INV: Ermöglicht Ihnen, die Verteilung Ihrer Lagerflächen im Universum anzuzeigen. Dieses Feature ist noch nicht verfügbar.

MU POL: Zeigt eine politische Karte. Dieses Feature ist noch nicht verfügbar.

__MS__  
_Obligatorischer Parameter: System-ID_  
Wie auf der Karte des Universums markieren gelbe Pfeile Ihre Schiffe. Die Wireframe-Struktur in der Mitte ist der Star des Systems. Die Kreise, die ihn umringen, sind entweder erdähnliche Planeten (weiß) oder Gasriesen (orange). Weiße Quadrate stehen für Stationen. Wenn Sie mit der Maus über einen Planeten oder eine Station fahren, wird die zugehörige ID angezeigt. Anstatt die System-ID manuell einzugeben, können Sie auch auf das gewünschte System in der Karte des Universums klicken.

__SYSI__
_Optionaler Parameter: System-ID_
Alle Systeme, ob benannt oder unbenannt, haben eine ID, die aus der Sektor-ID (zwei Buchstaben) und der Systemkennung besteht. Der Systeminformations-Command zeigt grundlegende Informationen über das System an, wie seinen Namen, Sternenklasse, Mikrometeorid-Dichte und Fraktionszugehörigkeit. Er enthält eine Liste aller Planeten und Stationen in diesem System. Wird keine System-ID angegeben, wird anstelle der Systemdaten ein Suchfeld angezeigt, mit dem nach Systemen gesucht werden kann.

__PLI__
_Optionaler Parameter: Planeten-ID_
Alle Planeten, ob benannt oder unbenannt, haben eine ID, die aus der System-ID gefolgt von einem eindeutigen Buchstaben besteht. PLI enthält Shortcuts zu Ihrer Flotte und Ihrem Inventar auf diesem Planeten. Hier können Sie unter anderem sehen, welche Ressourcen aus diesem Planeten und seiner Atmosphäre gewonnen werden können und ob sich der Planet für den Pflanzenanbau eignet oder nicht. Der Balken, der Letzteres anzeigt, beginnt in der Mitte und je weiter er sich nach links oder rechts erstreckt, desto unfruchtbarer bzw. fruchtbarer ist der Planet. Schließlich geben Typ und Temperatur an, ob Sie zusätzliche Baumaterialien benötigen, um eine Basis auf diesem Planeten zu errichten. Jeder nicht-graue Bereich auf einem Planeten kann angeklickt werden, um weitere Informationen darüber zu erhalten. Bisher gibt es folgende Farben: Blau (andere Unternehmen), Dunkelblau (Projekt eines anderen Konzerns), Gelb (eigenes Unternehmen), Dunkelgelb (Projekt eines eigenen Konzerns), Grün (CoGC), Rot (Warenbörse). Anstatt die Planeten-ID manuell einzugeben, können Sie auch direkt auf den Planeten in der Systemkarte klicken, um auf das PLI-Fenster zuzugreifen. Wird keine Planeten-ID angegeben, wird anstelle der Planetendaten ein Suchfeld angezeigt, mit dem nach Planeten gesucht werden kann.

__STI__  
_Obligatorischer Parameter: Stations-ID_  
Zeigt allgemeine Informationen zu einer Station an und ermöglicht den Zugriff auf deren Infrastruktur. Erreichbar durch Klicken auf eine Station (quadratisches Symbol) auf einer Systemkarte oder in einem Planeteninfofenster.

## Commands für planetare Projekte

__PPS__  
_Obligatorischer Parameter: Planeten-ID_  
Zeigt alle planetaren Projekte auf dem gewünschten Planeten an.

__PP__  
_Obligatorischer Parameter: Planeten- & Projekt-ID_  
Zeigt Informationen zu einem konkreten planetaren Projekt. Aufgrund der langen und komplexen Parameter empfiehlt es sich, diese Informationen über den "Details"-Button neben dem gewünschten Projekt im PPS-Buffer abzurufen.

__POPR__
_Obligatorischer Parameter: Planeten-ID_   
Zeigt die Bevölkerungsberichte des angegebenen Planeten mit Informationen zur Größe, Bedürfniserfüllung und Wachstum der Planetenbevölkerung.

### Commands für lokale Marktplätze

__LMOS__
_Keine möglichen Parameter_  
Zeigt eine Übersicht all Ihrer Anzeigen.

__LM__
_Obligatorischer Parameter: Planeten-ID_  
Zeigt alle verfügbaren Anzeigen auf einem bestimmten lokalen Marktplatz an. Zugriff per Klick auf den Infrastruktureintrag "Lokaler Marktplatz" (falls vorhanden) in einem beliebigen PLI-Fenster.

__LMA__
_Obligatorischer Parameter: Anzeigen-ID_  
Zeigt Details zur gesuchten Anzeige an. Zugriff durch Auswahl einer Anzeige im LM-Fenster.

__LMP__
_Obligatorischer Parameter: Planeten-ID_  
Ermöglicht die Platzierung einer Kauf- oder Verkaufsanzeige auf einem bestimmten lokalen Marktplatz. Zugriff über die Schaltfläche "Anzeige erstellen" in einem LM-Fenster.

### Politische Commands

__ADM__
_Obligatorischer Parameter: Planeten-ID_  
Zeigt Informationen zur [Planetaren Verwaltung](../../tutorials/planetary-projects/#administration-center) des Planeten (sofern vorhanden), z.B. den aktuellen Gouverneur, die Organisation (Fraktion oder Konzern), die Gebühren und Steuern einzieht, sowie alle KandidatInnen für die kommende Amtszeit. Ermöglicht es jedem, für das Gouverneursamt des Planeten zu kandidieren, und den BewohnerInnen des Planeten, für ihre bevorzugten KandidatInnen zu stimmen.

__GOV__
_Obligatorischer Parameter: Planeten-ID_ 
Zeigt Informationen über die aktuelle und vergangene Regierungen eines Planeten sowie die Anträge, über die abgestimmt wurde.

__LR__
_Obligatorischer Parameter: Planeten-ID_  
Zeigt die Lokalen Gesetze eines Planeten an, sofern dieser über eine Planetare Verwaltung verfügt. Zu den Lokalen Gesetzen gehören Produktionssteuern sowie Gebühren für Anzeigen auf lokalen Marktplätzen.

__POL__
_Optionaler Parameter: Nutzername_
Zeigt die aktuellen und vergangenen Ämter eines Nutzers inklusive der aktuellen Kandidaturen.

### Lagerhaus-Commands

__WAR__
_Obligatorischer Parameter: Planeten-ID_  
Zeigt öffentliche und private Informationen zu Lagerhäusern an, so etwa die Anzahl der verfügbaren Lager-Einheiten, die Mietgebühren usw.

## Commands für Benachrichtigungen

__NOTS__
_Keine möglichen Parameter_  
Zeigt eine Liste der In-Game-Benachrichtigungen an. Klicken Sie auf eine Benachrichtigung, um weitere Informationen zu erhalten.

__NOTIG__
_No possible paramter_  
Ermöglicht Ihnen, Ihre Benachrichtigungseinstellungen im Spiel zu ändern. Deaktivierte Benachrichtigungstypen werden im `NOTS`-Befehl nicht angezeigt.

__NOTPNS__
_Keine möglichen Parameter_  
Ermöglicht Ihnen, Ihre Push-Benachrichtigungseinstellungen zu ändern. Wählen Sie aus, welche Arten von Benachrichtigungen Ihnen per E-Mail in welcher Häufigkeit zugesendet werden sollen.

## Commands für Übertragungen

__TRA__  
_Keine möglichen Parameter_  
Öffnet eine Liste mit allen Übertragungen, z.B. Video-Tutorials.

__XIT__  
_Optionaler Parameter: Titel_  
Öffnet einen grünen Bildschirm, der Ihnen bei der Aufzeichnung Ihrer eigenen Übertragung hilft. Verwenden Sie den optionalen Parameter, um ihm einen Titel zu geben.

__XYTV__  
_Obligatorischer Parameter:_ YouTube-ID  
Bettet ein YouTube-Video ein. Die ID ist die Folge von Zahlen und Buchstaben nach "v=" in der URL des Videos.

## Sonstige Commands

__ARC__  
_Keine möglichen Parameter_  
Zeigt den aktuellen Status Ihres APEX-Repräsentanzzentrums an und ermöglicht es Ihnen, Mittel zur Erhöhung seines Levels beizusteuern.

__COLIQ__  
_Keine möglichen Parameter_  
Ermöglicht Ihnen, Ihr Unternehmen zu liquidieren. Das Unternehmen wird hierdurch gelöscht, sodass Sie mit demselben Account ganz von vorne beginnen können. Aktualisieren Sie den APEX-Tab nach der Verwendung. Für den COLIQ-Befehl gelten folgende Abklingzeiten: Die erste COLIQ ist sofort nach Firmengründung verfügbar, die zweite 3 Tage nach Verwendung des ersten. Die Wartezeit für die dritte COLIQ beträgt 21 Tage und jede weitere Abklingzeit beträgt 60 Tage. Wenn es keinen Warenhandel, Geschäfte auf lokale Marktplätzen und keine Beiträge zu planetaren oder Konzernprojekten gegeben hat, kann eine sofortige COLIQ möglich sein. Bitte beachten Sie, dass ein Missbrauch des COLIQ-Befehls zur (vorübergehenden) Sperrung Ihres Kontos führen kann!

__CS__  
_Keine möglichen Parameter_  
Ermöglicht Ihnen, einen neuen Screen zu erstellen. Um diesen Befehl aufzurufen, können Sie oben die Schaltfläche "NEU" verwenden. Alles über Screens erfahren Sie im Tutorial zum APEX-Interface.

__FIN, FINLA, FINIS, FINBS__  
Mithilfe dieser vier Befehle erhalten Sie einen detaillierten Überblick über die finanzielle Situation Ihres Unternehmens. Weitere Informationen zu diesen Commands folgen bald.

__LEAD__  
_Keine möglichen Parameter_  
Zeigt Leaderboards auf Unternehmensebene an. Die Art des Leaderboards kann über das Dropdown-Menü oben ausgewählt werden. Einige Leaderboards unterstützen zusätzliche Selektoren (z.B. die Angabe der Daten-Zeitspanne).

{{% about-this-page %}}
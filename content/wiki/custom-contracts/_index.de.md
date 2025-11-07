---
title: "Benutzerdefinierte Verträge"
date: 2022-07-25T10:30:49+02:00
---

## Allgemeine Informationen

Der `CONTD`-Command ermöglicht das Erstellen, Bearbeiten und Versenden von Vertragsentwürfen, um benutzerdefinierte Verträge mit anderen Parteien abzuschließen. Diese wurden mit dem **Convergence**-Release eingeführt, zusätzliche Entwurfstypen kamen dann mit der Veröffentlichung von **Liquidity** hinzu.

## Liste der Vertragsentwürfe

Wenn Sie den `CONTD`-Command ohne Parameter öffnen, wird die Liste aller Vertragsentwürfe angezeigt:

![contract draft list](contd.png)

Es ist möglich, Entwürfe zu erstellen, zu kopieren und zu löschen sowie bereits vorhandene Entwürfe zu öffnen, um sie zu bearbeiten.

## Bearbeiten eines Vertragsentwurfs

Ein Vertragsentwurf besteht aus zwei Abschnitten, einem für allgemeine Informationen und einem für die Bedingungen.

Im ersten Abschnitt kann der Vertrag benannt werden. Der Name ist privat und für VertragspartnerInnen nicht sichtbar. Er ist als Hilfe gedacht, damit Sie sich merken können, wozu der Vertragsentwurf dient. Das Vertragsvorwort ist ein Freitextfeld, das übermittelt wird, sobald der Entwurf an eine andere Partei gesendet wird. VertragserstellerInnen können ihre Absichten mit Verträgen also nicht nur in den Vertragsbedingungen zum Ausdruck bringen, sondern auch hier.

Im zweiten Abschnitt geht es um die Vertragsbedingungen. Durch Klicken auf die Schaltfläche "Vorlage auswählen" öffnet sich ein Overlay, über das Sie eine Vorlage für einen Vertragsentwurf auswählen können. Es gibt drei Vertragsvorlagen ("Kauf von Waren", "Verkauf von Waren" und "Versand von Waren"), die den auf lokalen Marktplätzen verfügbaren Anzeigen ähneln. Darüber hinaus gibt es noch drei Vorlagen zu Darlehensverträgen.

Ähnlich wie bei Schiffsentwürfen werden alle Änderungen erst gespeichert, wenn Sie auf die Schaltfläche "Speichern" klicken. Wählen Sie "VERWERFEN", wird der Entwurf auf seinen letzten Status zurückgesetzt.
Einzelne Bedingungen können über den Button "Kondition" angepasst werden. Je nach Kondition ermöglicht ein Overlay die Änderung von Materialien, Standortwährungen, Mengen usw. Über die Schaltfläche "Parameter" können Sie die Frist einer Kondition ändern.

![contract draft](contd2.png)

## Zusenden eines Vertragsentwurfs

Ein Vertragsentwurf kann jeder Lizenzinhaberin / jedem Lizenzinhaber zugesandt werden. Durch das Versenden des Vertrags wird eine Kopie des Vertragsentwurfs erstellt, welche dann in einen regulären Vertrag umgewandelt und in der Liste der Verträge `CONTS` angezeigt wird.

Die Empfängerin / der Empfänger erhält eine Benachrichtigung über den neuen Vertrag und kann diesen einsehen. Ein Vertrag kann dann entweder akzeptiert oder abgelehnt werden. In beiden Fällen erhält die Absenderin / der Absender eine Benachrichtigung.

Änderungen am Vertragsentwurf, nachdem dieser zum Erstellen eines Vertrags verwendet wurde, haben keine Auswirkungen auf bereits erstellte Verträge. Ein Vertragsentwurf kann mehrfach verwendet werden.

Durch das Hinzufügen einer Person zur Blockliste wird der Empfang von Vertragsentwürfen dieser Lizenznehmerin / dieses Lizenznehmers verhindert.

Zum Versenden eines Vertragsentwurfs ist eine `PRO`-Lizenz erforderlich, zum Abschluss eine `BASIC`- oder `PRO`-Lizenz.

{{% about-this-page %}}

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/warnings-in-mdl-graphs.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über und lösen Sie Warnungen in MDL-Diagrammen auf, um eine ordnungsgemäße Materialdefinition und -wiedergabe sicherzustellen.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Warnings in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Warnungen in MDL-Diagrammen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 0%

---


# Warnungen in MDL-Diagrammen

Auf dieser Seite werden Warnungen und Fehlermeldungen aufgelistet, die von MDL-Diagrammen in [Substance 3D Designer](https://www.adobe.com/de/products/substance3d-designer.html) ausgelöst werden können. Außerdem werden für jedes dieser Diagramme häufige Schritte zur Fehlerbehebung angeboten.

Warnungen werden in der QuickInfo des Warnsymbols für die Diagrammressource im Bereich [Explorer](../../interface/the-explorer-window/the-explorer-window.md) sowie in der unteren linken Ecke der [Diagrammansicht](../../interface/the-graph-view/the-graph-view.md) angezeigt, wenn das Diagramm geladen ist.

>[!NOTE]
>
> Die Abbildungen in diesem Abschnitt wurden in <b>Substance-Modellgrafiken</b> aufgezeichnet, die *eingestellt* in der Version <b>13.0.0</b> von Substance 3D Designer waren. Sie gelten jedoch auch für MDL-Grafiken.

## ![(Fehler)](warnings-in-mdl-graphs.resources/error.svg) Kein Ausgabeknoten definiert

Für das Diagramm ist kein Ausgabeknoten definiert.

<b>![(tick)](warnings-in-mdl-graphs.resources/check.svg) Lösung</b>

Wählen Sie einen beliebigen Knoten im Diagramm aus, der einen Wert ausgibt, dessen Typ dem erwarteten Typ für diese Funktion entspricht (falls vorhanden), klicken Sie dann auf RMB und wählen Sie im Kontextmenü die Option <b>Als Stamm festlegen</b> oder doppelklicken Sie auf LMB auf dem Knoten.\
Der Ausgabeknoten eines Substance-Modelldiagramms ist *orange*.

![&#39;Kein Ausgabeknoten definiert&#39; Lösung &#x200B;](warnings-in-mdl-graphs.resources/warnings-model-output.gif "&#39;Kein Ausgabeknoten definiert&#39; Lösung ")

### ![(Fehler)](warnings-in-mdl-graphs.resources/error.svg) Mindestens ein Eingabewert wurde abgelehnt.

Der für einen Parameter angegebene Wert führt nicht zu einer gültigen Berechnung des Knotens.

<b>![(tick)](warnings-in-mdl-graphs.resources/check.svg) Lösung</b>

Passen Sie den Wert so an, dass er für den Zielparameter sinnvoll ist.

![&#39;Mindestens ein Eingabewert wurde abgelehnt&#39; Lösung &#x200B;](warnings-in-mdl-graphs.resources/warnings-model-rejected-value.gif "&#39;Mindestens ein Eingabewert wurde abgelehnt&#39; Lösung ")

### ![(Fehler)](warnings-in-mdl-graphs.resources/error.svg) Kein Eingabewert

Ein Eingabewert, der von einem Knoten zur Durchführung seiner Berechnung erwartet wird, wird nicht bereitgestellt.

<b>![(tick)](warnings-in-mdl-graphs.resources/check.svg) Lösung</b>

Einige Knotenparameter können nicht auf einen Standardwert zurückgreifen, wenn keine Daten an den Eingangsanschluss geliefert werden. Dies ist häufig der Fall bei Szeneneingaben.

Schließen Sie die Knoteneingänge an den entsprechenden Ausgangsanschluss eines anderen Knotens an.

![&#x200B; Lösung &quot;Kein Eingabewert&quot; &#x200B;](warnings-in-mdl-graphs.resources/warnings-model-no-input-value.gif " Lösung &quot;Kein Eingabewert&quot; ")

### ![(Fehler)](warnings-in-mdl-graphs.resources/error.svg) Knoten wurde nicht berechnet

Die dem Knoten bereitgestellten Informationen sind unvollständig oder ungültig, sodass der Knoten seine Berechnungen nicht durchführen konnte.

<b>![(tick)](warnings-in-mdl-graphs.resources/check.svg) Lösung</b>

Gehen Sie im Diagramm stromaufwärts und suchen Sie nach Warnungen, die durch Probleme ausgelöst werden, die Knoten daran hindern, eine gültige Ausgabe bereitzustellen.

![&#x200B; &#39;Knoten wurde nicht berechnet&#39; Lösung &#x200B;](warnings-in-mdl-graphs.resources/warnings-model-no-input-value.gif " &#39;Knoten wurde nicht berechnet&#39; Lösung ")

### ![(Fehler)](warnings-in-mdl-graphs.resources/error.svg) Die referenzierten Daten enthalten einige Warnungen.

Die Ressource, auf die von einem Knoten verwiesen wird, enthält eine oder mehrere Warnungen. Im Folgenden finden Sie einige Knoten, die auf eine Ressource verweisen:

* Ein Grapheninstanzknoten verweist auf ein Diagramm
* Ein Szenenressourcenknoten verweist auf eine Bitmap-3D-Szenenressource

<b>![(tick)](warnings-in-mdl-graphs.resources/check.svg) Lösung</b>

Suchen Sie im Explorer-Bedienfeld nach der referenzierten Ressource und beheben Sie alle von der Ressource ausgelösten Warnungen:

* Weitere Diagramme finden Sie auf dieser Seite.
* Informationen zu anderen Ressourcentypen finden Sie auf der Seite Warnungen von Abhängigkeiten .

![&quot;Für die referenzierten Daten gibt es einige Warnungen&quot; Lösung &#x200B;](warnings-in-mdl-graphs.resources/warnings-model-referenced-data.gif " &quot;Die referenzierten Daten haben einige Warnungen&quot; Lösung ")

### ![(Fehler)](warnings-in-mdl-graphs.resources/error.svg) Referenzierte Ressource nicht gefunden

Die Ressource, auf die von einem Knoten verwiesen wird, wurde unter dem in der Substance 3D-Datei (SBS) gespeicherten Pfad nicht gefunden. Im Folgenden finden Sie einige Knoten, die auf eine Ressource verweisen:

* Ein Grapheninstanzknoten verweist auf ein Diagramm
* Ein Szenenressourcenknoten verweist auf eine Bitmap-3D-Szenenressource

<b>![(tick)](warnings-in-mdl-graphs.resources/check.svg) Lösung</b>

Für Knoten der Diagramminstanz

Überprüfen Sie, ob das Quelldiagramm im Paket vorhanden ist, das sich in dem Pfad befindet, der in ihrem <b>Package</b>-Attribut gespeichert ist.\
Ist dies nicht der Fall, löschen Sie den Instanzknoten und ersetzen Sie ihn durch einen Instanzknoten, der auf ein gültiges Paket verweist. Alternativ können Sie das Paket und das Diagramm, auf das der Instanzknoten verweist, neu erstellen und dann das Hostpaket neu laden, indem Sie im Bedienfeld [Explorer](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion) auf *RMB* klicken und im Kontextmenü die Option <b>Erneut laden</b> auswählen.

Für Szenenressourcenknoten

Suchen Sie die referenzierten Ressourcen im Bereich [Explorer](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion) und überprüfen Sie, ob sie an dem Speicherort vorhanden sind, der in ihrem <b>Dateipfad</b>-Attribut gespeichert ist.\
Wenn dies nicht der Fall ist, klicken Sie auf *RMB* auf dem Ressourcenelement im Explorer, und wählen Sie <b>Verschieben...Option &quot;</b>&quot; im Kontextmenü, um eine neue gültige Zieldatei für diese Ressource festzulegen.

![&#x200B; &quot;Referenzierte Ressource nicht gefunden&quot; Lösung &#x200B;](warnings-in-mdl-graphs.resources/warnings-model-referenced-resource.gif " &quot;Referenzierte Ressource nicht gefunden&quot; Lösung ")

### ![(Fehler)](warnings-in-mdl-graphs.resources/error.svg) Der weiche Bereich enthält den Wert nicht.

Der Standardwert eines exponierten Parameters ist nicht in dem für diesen Parameter definierten weichen Bereich enthalten.

<b>![(tick)](warnings-in-mdl-graphs.resources/check.svg) Lösung</b>

Passen Sie den Standardwert bzw. den Soft-Range so an, dass Erstere in Letztere aufgenommen wird.

>[!NOTE]
>
> Diese Warnung kann nicht über die Benutzeroberfläche ausgelöst werden, da *den Soft-Bereich automatisch so anpasst, dass er den Standardwert enthält.* Nur das Ändern der Daten in der Substance 3D-Datei (SBS) *direkt* kann dazu führen, dass diese Warnung ausgelöst wird.

![&quot;Der weiche Bereich enthält nicht die Lösung &quot;](warnings-in-mdl-graphs.resources/warnings-model-ranges.gif "&quot; des Werts. Der weiche Bereich enthält nicht die Lösung &quot;")&quot; des Werts.

### ![(Fehler)](warnings-in-mdl-graphs.resources/error.svg) Der weiche Bereich liegt außerhalb des festen Bereichs.

Der weiche Bereich von und der exponierte Parameter sind nicht vollständig in dem für diesen Parameter definierten harten Bereich enthalten.

<b>![(tick)](warnings-in-mdl-graphs.resources/check.svg) Lösung</b>

Passen Sie den Soft- oder Hard-Bereich so an, dass Erstere vollständig in Letztere aufgenommen wird.

>[!NOTE]
>
> Diese Warnung kann nicht über die Benutzeroberfläche ausgelöst werden, da *automatisch den weichen Bereich anpasst, der vollständig in den harten Bereich einbezogen werden soll.* Nur das Ändern der Daten in der Substance 3D-Datei (SBS) *direkt* kann dazu führen, dass diese Warnung ausgelöst wird.

![&#39;Der weiche Bereich liegt außerhalb des festen Bereichs&#39; Lösung](warnings-in-mdl-graphs.resources/warnings-model-ranges.gif "&#39;Der weiche Bereich liegt außerhalb des festen Bereichs&#39; Lösung")

### ![(Fehler)](warnings-in-mdl-graphs.resources/error.svg) Der Wert liegt außerhalb des zulässigen Bereichs.

Der Standardwert eines angezeigten Parameters ist nicht in dem für diesen Parameter definierten festen Bereich enthalten.

<b>![(tick)](warnings-in-mdl-graphs.resources/check.svg) Lösung</b>

Passen Sie den Standardwert bzw. den festen Bereich so an, dass Erstere in Letztere einbezogen werden.

>[!NOTE]
>
> Diese Warnung kann nicht über die Benutzeroberfläche ausgelöst werden, da *automatisch den Standardwert anpasst, der in den festen Bereich aufgenommen werden soll.* Nur das Ändern der Daten in der Substance 3D-Datei (SBS) *direkt* kann dazu führen, dass diese Warnung ausgelöst wird.

![&#x200B; &quot;Der Wert liegt außerhalb des festen Bereichs&quot; Lösung &#x200B;](warnings-in-mdl-graphs.resources/warnings-model-ranges.gif " &quot;Der Wert liegt außerhalb des festen Bereichs&quot; Lösung ")

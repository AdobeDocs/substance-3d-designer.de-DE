---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/warnings-and-errors.html"
breadcrumb-title: ''
description: Finden Sie Lösungen für häufig auftretende Warnungen und Fehler in Substance 3D Designer, um Probleme schnell zu beheben.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Warnings and errors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Warnungen und Fehler
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 6%

---


# Warnungen und Fehler

Auf dieser Seite werden die Berichterstellung für Warnungen und Fehlermeldungen erläutert, die in [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) angezeigt werden können, sowie Links zur Fehlerbehebung für Warnungen anhand ihrer Quelle.

## Überblick

Bei der Arbeit an Projekten in Designer können Warnungen und Fehlermeldungen angezeigt werden, die Sie über ein Problem im Projekt informieren:

* **Warnungen** werden in *gelbem* Text angezeigt und machen Sie auf ein Problem aufmerksam, das aufgrund fehlender Eingabe oder fehlerhafter Konfiguration zu einem unerwünschten Ergebnis führen kann. Normalerweise *wird Ihre Arbeit nicht blockiert*.
* **Fehler** werden im Text *Rot* angezeigt und weisen auf einen Fehler bei der Berechnung, ein unerwartetes Ergebnis oder die Unfähigkeit zur Ausführung einer Aufgabe hin. Normalerweise *wird Ihre Arbeit blockiert*.

Im Allgemeinen werden Warnungen und Fehler für das Element angezeigt, das sie ausgelöst hat, und *werden für jedes übergeordnete* Element dieses Elements angezeigt. Im Folgenden finden Sie eine Liste der häufigsten Stellen, an denen Warnungen und Fehler gemeldet werden:

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Explorer

Für jedes Element im Bereich [Explorer](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), das eine Warnung enthält, wird diese Warnung mit einem Symbol ![](../../assets/warning-icon.png) am rechten Rand des Eintrags des Elements in der Liste angezeigt. Lassen Sie den Cursor einige Sekunden auf diesem Symbol, um eine *QuickInfo* anzuzeigen, in der alle Warnungen detailliert aufgeführt sind.

Sie befolgen die folgenden Regeln:

* Wenn das Element unter einem anderen Element verschachtelt ist (z. B. einem Ordner), werden Warnungen zu diesem Element angezeigt, wenn es ausgeblendet ist.
* Warnungslisten sind *kumulativ*, da sie die Summe der Warnungen eines Elements *und* aller angezeigten Warnungen seiner untergeordneten Elemente sind.
* Alle Warnungen, die vom Inhalt eines Pakets gemeldet werden, werden dem Element *Paket* hinzugefügt und den *eigenen* Warnungen des Pakets hinzugefügt.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-explorer.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Diagrammansicht

Für jedes Element im Bereich &quot;[Diagrammansicht](../../interface/the-graph-view/the-graph-view.md)&quot;, das eine Warnung enthält, wird diese Warnung mit farbigem Text in der *linken unteren Ecke* des Ansichtsports angezeigt. Wenn die Warnung von einem bestimmten Knoten ausgelöst wird, verfügt dieser Knoten über ein Warnzeichen ![](../../assets/warning-badge.png). Lassen Sie den Cursor einige Sekunden auf diesem Abzeichen, um eine *QuickInfo* anzuzeigen, in der alle Warnungen detailliert aufgeführt sind.

Sie befolgen die folgenden Regeln:

* Wenn ein Quelldiagramm *instanziiert* in einem anderen Hostdiagramm eine oder mehrere Warnungen enthält, hat der [Instanzknoten](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) für dieses Quelldiagramm eine *einzelne* `The referenced data has some warnings` Warnung.
* Warnungslisten sind *kumulativ*, da sie die Summe der Warnungen des Diagramms *und* aller Warnungen der untergeordneten Knoten sind.
* Alle Warnungen eines Diagramms werden für das Element ausgegeben, das dieses Diagramm im Explorer-Bedienfeld darstellt.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-graph.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Eigenschaften

Für jedes Element im Bereich [Eigenschaften](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html), das eine Warnung enthält, wird diese Warnung mit einem Symbol ![](../../assets/warning-icon.png) am rechten Rand des Eintrags des Elements in der Liste angezeigt. Lassen Sie den Cursor einige Sekunden auf diesem Symbol, um eine *QuickInfo* anzuzeigen, in der alle Warnungen detailliert aufgeführt sind.

Sie befolgen die folgenden Regeln:

* Wenn das Element unter einem anderen Element verschachtelt ist (z. B. einer Abschnittsüberschrift), werden Warnungen zu diesem Element angezeigt, wenn es ausgeblendet wird.
* Warnungslisten sind *kumulativ*, da sie die Summe der Warnungen eines Elements *und* aller angezeigten Warnungen seiner untergeordneten Elemente sind.
* Wenn das [Funktionsdiagramm ](../../function-graphs/function-graphs.md), das auf einen [Eingabeparameter ](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) angewendet wurde, eine oder mehrere Warnungen enthält, enthält das Parameterelement eine *einzelne* `The [x] parameter's function has some warnings` Warnung.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-properties.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Konsole

Im Bedienfeld **Konsole** werden sowohl Warnungen als auch Fehler gemeldet. Sie können über das Menü **Windows** im [Hauptmenü](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-main-menu-143720673.html) darauf zugreifen. Sie können Warnungen und Fehler von den restlichen Konsoleneinträgen isolieren, indem Sie die Einstellung **Kanal** auf `ErrorMgr` festlegen.

>[!NOTE]
>
> Da der gesamte Text in der Konsole *auswählbar* ist, können Sie dieses Fenster verwenden, um *Warnungen und Fehlermeldungen einfach zu kopieren* und in das Tool **Lokale Suche** dieser Dokumentation oder in eine beliebige Internet-Suchmaschine einzufügen. Dies beschleunigt die Suche nach Anleitungen zur Fehlerbehebung.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-console.png){width="256px"}

</td>
</tr>
</table>

### Nachrichten mit &quot;(# Mal)&quot;

In der *exakt gleichen* Warnung oder dem Fehler wird *mehr als einmal* für ein Element *und* für eines seiner untergeordneten Elemente ausgelöst. Diese Warnungen werden *in* zusammengeführt, und das Suffix `(# times)` wird angezeigt, sodass Sie wissen, wie oft diese Warnung oder dieser Fehler gemeldet wurde.

## Kategorien

Im Folgenden finden Sie eine Liste der Warnungen und Fehler, die in Designer auftreten können, sortiert nach ihrer Quelle. Kategorietitel werden auf die entsprechende Seite mit Erläuterungen und Anleitungen zur Fehlerbehebung für die Lösung der einzelnen Probleme verknüpft.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Warnungen in Substance-Graphen

* Kein Ausgabeknoten definiert
* Die Funktion des Parameters [x] enthält einige Warnungen.
* Die referenzierten Daten enthalten einige Warnungen.
* Referenzressource nicht gefunden
* Textknoten verwendet ungültige Schriftart

</td>
<td style="border: 0;" valign="top">

### Warnungen in Funktionsdiagrammen

* Kein Ausgabeknoten definiert
* Der aktuelle Ausgabeknoten gibt einen Wert vom Typ x zurück.
* Einige Get-Knoten haben keinen Variablennamen.
* Einige Set-Knoten haben keinen Variablennamen.

</td>
</tr>
</table>

### Warnungen von Abhängigkeiten

* Ungültiges abhängiges Paket
* Überprüfen Sie, ob der Alias &quot;x&quot; in Ihrem Projekt definiert ist.
* Es wurde keine Datei gefunden, die dieser Ressource entspricht
* Verknüpfte Datei wurde nicht gefunden
* Farbraum nicht gefunden
* Referenzressource nicht gefunden
* UV-Kacheln werden mehrfach zugewiesen
* Ungültige UV-Kacheln

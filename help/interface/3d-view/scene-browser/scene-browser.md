---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/scene-browser.html"
breadcrumb-title: ''
description: Verwenden Sie den Szenenbrowser, um im Viewport zu 3D-Szenenelementen, Materialien und Objekten zu navigieren und diese zu verwalten.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Scene browser
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Szenenbrowser
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 1%

---


# Szenenbrowser

Der Szenenbrowser der 3D-Ansicht listet alle Elemente in der Szene und ihre Hierarchie auf.

Es bietet Steuerelemente zum Auswählen von Objekten, zum Umschalten ihrer Sichtbarkeit sowie zum Auswählen, welches Material [&#x200B; ein Szenenmaterial überschreiben soll](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md).

Da Designer [USD](https://openusd.org/release/index.html) für die Beschreibung und Verwaltung seiner Szenen verwendet, befinden sich die Terminologie und Konzepte in dieser Szenenstruktur.

Sie wird angezeigt, indem Sie auf die dedizierte Umschaltfläche &quot;![](scene-browser.resources/sceneBrowser-toggleButton.png)&quot; in der [3D-Ansichtsszene-Symbolleiste &#x200B;](../../../interface/3d-view/3d-view.md) klicken.

![Szenenbrowser - Geladene 3D-Szene](scene-browser.resources/loaded3DScene.png "Szenenbrowser - Geladene 3D-Szene"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Szenenbaum

</td>
<td style="border: 0;" valign="top">

### Umschalten von Objekten in der Szene

</td>
<td style="border: 0;" valign="top">

### Verbundene Materialien

</td>
</tr>
</table>

## Szenenbaum

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Der Szenenbrowser zeigt eine Liste von Objekten an, die in einer hierarchischen Baumstruktur angeordnet sind.

Objekte werden anderen Objekten übergeordnet, bis zum Stamm der Szene. Ein übergeordnetes Objekt verfügt über eine Pfeilschaltfläche, mit der die Liste der ihm untergeordneten Objekte ein- oder ausgeblendet wird.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Szenenbrowser - Szenenbaum](scene-browser.resources/sceneBrowser-sceneTree.png "Szenenbrowser - Szenenbaum"){zoomable="yes"}

</td>
</tr>
</table>

Lassen Sie den Cursor einige Sekunden auf einem Element in der Struktur, um eine QuickInfo mit den folgenden Informationen anzuzeigen:

* <b>Pfad:</b> Der vollständige Pfad des Objekts in der Szene.
* <b>TypeName:</b> Der USD-Typ des Objekts.
* <b>Dokumentation:</b> Ausführliche Informationen zum Objekt als USD-Szenenelement.

Gitter verfügen über zusätzliche Informationen: Scheitelpunktzahl, Gesichtszahl und UV-Zahl.

### Von Designer hinzugefügte Objekte

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Designer fügt jeder geladenen Szene einige Objekte hinzu. Von Designer hinzugefügte Objekte sind mit <b>bold</b> gekennzeichnet.

Bei Verwendung des Editors ... in den Menüs &quot;Licht&quot;, &quot;Kamera&quot; und &quot;Umgebung&quot;. Dabei handelt es sich um die Objekte, die bearbeitet werden, unabhängig davon, ob andere Lichter, Kameras oder Umgebungen in der Szene vorhanden sind.

Diese Objekte sind in der Szene enthalten, wenn [&#x200B; &#x200B;](../../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md) exportiert hat.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Szenenbrowser: Von Designer hinzugefügte Objekte in Fettschrift](scene-browser.resources/sceneBrowser-addedByDesigner.png "Szenenbrowser: Von Designer hinzugefügte Objekte in Fettschrift"){zoomable="yes"}

</td>
</tr>
</table>

* <b>Kamera:</b> Die Standardkamera der Szene. Dies ist die einzige Kamera, mit der Sie in Designer interagieren können. Alle Kameras, die in einer geladenen Szene enthalten sind, werden als Vorgaben für die Standardkamera hinzugefügt.
* <b>Umgebung:</b> Die Standardumgebung der Szene. Jede auf die Umgebung der Szene angewendete Textur wird nur auf diese Umgebung angewendet. Ebenso wirkt sich das Drehen der Umgebung nur auf diese Umgebung aus.\
  Wenn eine geladene Szene eine oder mehrere Umgebungslichter enthält ([DomeLight](https://openusd.org/release/user_guides/schemas/usdLux/DomeLight.html) in USD), wird die Standardumgebung automatisch deaktiviert, um die Umgebungsbeleuchtung der Szene nicht zu beeinträchtigen.
* <b>Punktlicht #:</b> Wenn eines der Punktlichter von Designer unter &quot;Lichtquellen&quot; > &quot;Eigenschaften bearbeiten&quot; aktiviert ist, wird jedes Punktlicht der Szene hinzugefügt.

## Umschalten von Objekten in der Szene

### Alle Typen

Jedes Objekt kann in der Szene aktiviert und deaktiviert werden. Wenn diese Option deaktiviert ist, wird ein Objekt nicht mehr zur Szene hinzugefügt: es wirft keine Schatten, strahlt oder reflektiert Licht.

Der Status eines übergeordneten Objekts wird auf seine untergeordneten Objekte übertragen. Wenn Sie also ein übergeordnetes Objekt deaktivieren, werden auch seine untergeordneten Objekte deaktiviert.

Die Sichtbarkeit eines Objekts kann durch Klicken auf die Augenschaltfläche &quot;![](scene-browser.resources/sceneBrowser-eyeButton.png)&quot; oder über das Kontextmenü umgeschaltet werden. Das Menü bietet einige weitere Aktionen zum Verwalten der Sichtbarkeit von Szenenobjekten:

* <b>Ausblenden:</b> Deaktivieren Sie das ausgewählte Objekt.
* <b>Anzeigen:</b> Aktivieren Sie das ausgewählte Objekt.

Einige Aktionen wirken sich insbesondere auf die Sichtbarkeit von Gittern aus:

* <b>Nur anzeigen:</b> Deaktivieren aller Gitter außer dem ausgewählten und den zugehörigen untergeordneten Gittern.
* <b>Alle anzeigen:</b> Aktivieren Sie alle Gitter.

Übergeordnete Objekte verfügen über diese zusätzlichen Aktionen:

* <b>Untergeordnete Elemente ausblenden:</b> Alle untergeordneten Elemente des ausgewählten Objekts werden rekursiv deaktiviert.
* <b>Untergeordnete Elemente anzeigen:</b> Aktivieren Sie alle untergeordneten Elemente des ausgewählten Objekts rekursiv.
* <b>Alle untergeordneten Elemente erweitern:</b> Erweitern Sie alle untergeordneten Listen unter dem ausgewählten Objekt rekursiv.
* <b>Alle untergeordneten Elemente reduzieren:</b> Reduzieren aller untergeordneten Listen unter dem ausgewählten Objekt, rekursiv.

![Szenenbrowser - Objektsichtbarkeit umschalten](scene-browser.resources/sceneBrowser-toggleVisibility.gif "Szenenbrowser - Objektsichtbarkeit umschalten"){zoomable="yes"}

### Umgebungen

Die Sichtbarkeit einer Umgebungsbeleuchtung (DomeLight) kann wie andere Objekte aktiviert und deaktiviert werden.

Wenn eine Umgebungsbeleuchtung deaktiviert ist, wird auch ihr Lichtbeitrag zur Szene deaktiviert.

Wenn mehr als eine Umgebungsbeleuchtung aktiviert ist, werden ihre Beleuchtungsbeiträge *kumulativ* hinzugefügt.

![Szenenbrowser - Umgebungssichtbarkeit umschalten](scene-browser.resources/sceneBrowser-toggleEnvLights.gif "Szenenbrowser - Umgebungssichtbarkeit umschalten"){zoomable="yes"}

### Lichter

Dasselbe gilt für alle Lichter in der Szene: können einzeln aktiviert und deaktiviert werden.

![Szenenbrowser - Umschalten der Lichtsichtbarkeit](scene-browser.resources/sceneBrowser-toggleLights.gif "Szenenbrowser - Umschalten der Lichtsichtbarkeit"){zoomable="yes"}

## Verbundene Materialien

Mit dem Szenenbrowser können Sie auch überschriebenes Material mit einem anderen Material verbinden, das von Designer im Menü [Materialien](../../../interface/3d-view/3d-view.md) der 3D-Ansicht aufgelistet wird.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Bei den in Designer aufgelisteten Materialien handelt es sich um die Material-Objekte in der Szenenstruktur, die in mindestens einem Gitter verwendet werden.

Wenn [diese Materialien überschreiben](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), wird eine Kopie von Designer mit einem numerischen Suffix erstellt.

Ein überschriebenes Material bietet ein zusätzliches Element in seinem Kontextmenü: Das Untermenü &quot;[Verbundenes Material](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)&quot; listet alle anderen verfügbaren Materialien auf, die verwendet werden können, um dieses Material zu überschreiben.

</td>
<td style="border: 0;" valign="top">

![Szenenbrowser - Verbundenes Material](scene-browser.resources/sceneBrowser-connectedMaterial.png "Szenenbrowser - Verbundenes Material"){zoomable="yes"}

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: Verwenden Sie den Filterknoten "Abgeflachte Kante", um abgeflachte Kanten auf Formen und Mustern zu erstellen, um Tiefe und Abmessung hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Abgeflachte Kante (Filterknoten)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---


# Abgeflachte Kante (Filterknoten)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

## Abgeflachte Kante

**In:** *Filter/Effekte*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt einen Kantenabflachungseffekt für eine Graustufen-Höhenkarte aus. Gibt sowohl die abgeflachte Höhenkarte als auch die Normalmap basierend auf dieser Höhenkarte zurück.

Dies ist ein nützlicher Knoten zum Anwenden von exakten Kurvenprofilen auf eine idealerweise binäre (High Contract Black/White), einfache Höhenzuordnung.

## Parameter

### Eingaben

* **Eingabe**: *Graustufen-Eingabe*\
  Zu konvertierende Höhenzuordnung.
* **Benutzerdefinierte Kurve**: *Graustufen-Eingabe*\
  Farbverlauf, der die exakte Kurve/Steigung bestimmt. Im Idealfall ein linearer Verlaufsknoten, für den Sie beliebige Korrekturen wie [Tonwertkorrektur](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) oder [Gradationskurven](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) ausführen können. Nur aktiv, wenn &quot;Benutzerdefinierte Kurve verwenden&quot; auf &quot;True&quot; gesetzt ist.

### Parameter

* **Entfernung**: *-1.0 - 1.0* Wie weit der Abschrägungseffekt reichen sollte.
* **Eckentyp**: *Rund, Angular* Ob das Abschrägungsprofil abgerundet oder gerade sein soll.
* **Glättung**: *0.0 - 5.0* Wie viel zusätzliche Glättung (Weichzeichnen) muss nach der Abschrägung ausgeführt werden.
* **Uneinheitlichen Weichzeichner verwenden**: *Falsch/Wahr* Ob die Glättung ungleichmäßig erfolgen soll.
* **Benutzerdefinierte Kurve verwenden**: *Falsch/Wahr* Schaltet die Verwendung Ihrer eigenen Kurve für benutzerdefinierte Heights um. Weitere Informationen finden Sie oben.
* **Normalintensität**: *0.0 - 50.0* Intensität der generierten Normalmap.
* **Normales Format**: *DirectX, OpenGL*\
  Wechseln Sie zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/bevel-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

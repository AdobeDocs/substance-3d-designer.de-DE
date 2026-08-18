---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kantenauswahl", um Masken für die Auswahl von Gitterkanten zu generieren, um kantenbasierte Verwitterungs- und Abnutzungseffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Select
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Edge Select

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

## Edge Select

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske ist die beste Methode, um jede Art von Kante basierend auf der Krümmung auszuwählen. Konvex, konkav auf jeder Ebene oder mit jedem Kontrast kann isoliert werden. Dies stellt eine hervorragende Verknüpfung bereit, um dies manuell über einen Knoten mit [Ebenen zu vermeiden](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md).

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map zum Hervorheben von Kanten. Erforderlich!
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt den Gesamtbetrag der Kantenhervorhebung für &quot;Konvex&quot; und &quot;Konkav&quot; fest.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast der Markierung für &quot;Konvex&quot; und &quot;Konkav&quot; an.
* **Konvex**
  * **Konvexe Kanten, Breite**: *0.0 - 1.0* Legt die Breite der Markierung für konvexe Kanten fest. Denke daran, dass eine Erhöhung der Glätte leicht zu dünneren Kanten führen kann.
  * **Konvexe Weichheit**: *0.0 - 1.0* Stellen Sie die Weichheit des Übergangs für konvexe Kanten ein.
  * **Konvexe Intensität**: *0.0 - 1.0* Legt die maximale Intensität der Kantenmarkierung für konvexe Kanten fest. Auf 0 setzen, um keine Hervorhebung vorzunehmen.
* **Konkav**
  * **Konkave Kanten, Breite**: *0.0 - 1.0* Legen Sie die Breite der Markierung für konkave Kanten fest. Denke daran, dass eine Erhöhung der Glätte leicht zu dünneren Kanten führen kann.
  * **Konkave Weichheit**: *0.0 - 1.0* Stellen Sie die Weichheit des Übergangs für konkave Kanten ein.
  * **Konkave Intensität**: *0.0 - 1.0* Legen Sie die maximale Intensität der Kantenmarkierung für konkave Kanten fest. Auf 0 setzen, um keine Hervorhebung vorzunehmen.

## Beispielbilder

![](../../../../../../assets/edge-select-ex.gif)

</td>
</tr>
</table>

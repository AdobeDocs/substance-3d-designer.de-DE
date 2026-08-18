---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Sicheres Transformieren", um Transformationen anzuwenden, während Texturgrenzen beibehalten und Artefakte vermieden werden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sicheres Transformieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# Sicheres Transformieren

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Sicheres Transformieren (Graustufen)

**In:** *Filter/Transformationen*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Kachelsichere Version von [2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) transformieren. Ermöglicht Ihnen Skalierung, Drehung und Versatz, ohne dass die Kachelung unterbrochen wird und ohne dass Pixeldetails (Verlust von Knittergenauigkeit/Schärfe) aufgrund kleiner Versätze und Drehungen verloren gehen.

Nützlich für die Umwandlung von Rauschen, wenn maximale Kontrolle oder perfekte Schärfe erforderlich ist.

## Parameter

* **Kachel**: *1 - 16* Skaliert die Eingabe durch Kacheln nach unten.
* **Offset-Modus**: *Manuell, Zufällig* Wechselt zu einem zufälligen Offset anstelle eines manuell definierten Offsets.
* **Offset**: *0.0 - 1.0*\
  Verschiebt oder verschiebt das Ergebnis. Vergewissert sich, dass die Pixel ausgerichtet und nicht interpoliert sind.
* **Drehung**: *0.0 - 1.0* Dreht die Eingabe um einen Winkel.
* **Sichere Drehung der Kachel**: *Falsch/Wahr* Bestimmt das Verhalten der Drehung, ob sie an sicheren Werten ausgerichtet werden soll, bei denen keine Pixel verwischt werden.
* **Symmetrie**: *keine, X, Y, X+Y*
* **Hintergrundfarbe**: *(Farbwert) (Nur Farbversion)*
* **MIPMAP-Modus**: *Automatisch, Manuell* Bestimmt den Mipmapping-Modus. Die Einstellung auf Manuell führt zu schärferen Ergebnissen.
* **Mipmap-Stufe**: *0 - 10* Wenn der Mipmap-Modus auf &quot;Manuell&quot; eingestellt ist, können Sie eine andere Mipmap auswählen.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

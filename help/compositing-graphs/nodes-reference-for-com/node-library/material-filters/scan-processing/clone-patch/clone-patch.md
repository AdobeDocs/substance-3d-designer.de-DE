---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: Verwenden Sie den Klonausbesserungsknoten zum Klonen und Ausbessern von Bereichen in gescannten Materialien, um Artefakte und Makel zu entfernen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Klonausbesserung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Klonausbesserung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch.png){width="128px"}

![](../../../../../../assets/clone-patch-grayscale.png){width="128px"}

## Klonpflaster/Klonpflaster Graustufen

**In:** *Materialfilter/Scanverarbeitung*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Clone Patch ist ein prozeduraler, parametrischer Knoten &quot;Clone Stamp&quot;. Es klont einen Bereich einer Eingabe in einen anderen und blendet möglicherweise unerwünschte Details aus. Diese Methode ist nicht so schnell und einfach wie die Verwendung eines vertrauten Werkzeugs in einer pinselbasierten Anwendung. Sie bietet jedoch den entscheidenden Vorteil, dass sie nicht-destruktiv ist und in einem knotenbasierten Workflow funktioniert. Darüber hinaus führt dieser Knoten eine intelligente Analyse sowohl des Ziel- als auch des Quellbereichs durch und versucht, die Elemente auf der Grundlage von Kontrast, Werten und Formen so gut wie möglich zu mischen.

Dies ist vor allem für die seltenen Momente gedacht, in denen Sie eine manuelle Korrektur eines bestimmten Bereichs vornehmen möchten, falls irgendwo ein unerwünschtes Detail vorhanden ist.

Beachten Sie, dass dies nicht wie ein einfacher &quot;Stempel&quot;-Standardpinsel funktioniert. Die Form des angeglichenen Bereichs basiert auf den Formen und Werten der Bereiche, mit denen Sie arbeiten. Das bedeutet, dass es sich um einen ziemlich schweren Knoten handelt, der Geduld erfordert - aber hervorragende Ergebnisse liefert.

Es ist auch wichtig zu verstehen, dass Sie den Zielbereich mit einem Gizmo verschieben können, aber der Quellbereich muss durch Ändern der Parameter der &quot;Quellmatrix&quot; festgelegt werden.

>[!NOTE]
>
> Wenn Sie dies für ein vollständiges Material wünschen (wie dies meistens der Fall ist), finden Sie weitere Informationen unter [Material Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md).
> 
> Informationen zu den Fällen, in denen Sie diesen Vorgang für mehrere Eingaben gleichzeitig ausführen möchten (ohne dass es sich um ein Material handelt), finden Sie unter [Patch für mehrere Klone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md).

## Parameter

* **Ist normal (nur für Farbe)**: *False/True*\
  Legt fest, ob die Eingabe eine Normalmap ist und ob die Füllmethode als solche behandelt werden soll.
* **Form**: *Quadrat, Datenträger* Legt die Stempelform fest. Wird nur als Basis verwendet.
* **Edge**
  * **Schwellenwert**: *0.0 - 1.0* Legt fest, wie weit der angeglichene Bereich reichen soll. Dieser Effekt wächst stufenweise entlang der Formen im Zielbereich und hat bei einheitlichen Hintergründen sehr wenig Effekt.*
  * **Weichzeichnen**: *0.0 - 2.0* Weichzeichnet die Kanten des Stempelbereichs, falls ein weicherer Übergang erforderlich ist.
  * **Smoothness**: *0.0 - 2.0* Rundet die Kanten der Stempelform ab und sorgt so für glattere Konturen.
  * **Rasterauflösung**: *1 - 11* Legt die Qualitätsauflösung der Füllmethode fest. Je höher der Wert, desto präziser kann die Füllmethode sein.
* **Transformationen**
  * **Quellmatrix**: *(Transformationsmatrix)*Transformiert die Quelle (Skalierung und Drehung). Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden.
  * **Quellversatz**: *-0.5 - 0.5*&#x200B;Übersetzt den Quellspeicherort. Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden. *Dieser Parameter ist wahrscheinlich der Hauptparameter, den Sie ändern möchten!*
  * **Zielmatrix**: *(Transformationsmatrix)*Transformiert die Zielposition (Skalierung und Drehung). Kann auch durch Gizmo auf der Arbeitsfläche erfolgen.
  * **Zielversatz**: *-0.5 - 0.5*&#x200B;Übersetzt den Zielspeicherort. Kann auch durch Gizmo auf der Arbeitsfläche erfolgen.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

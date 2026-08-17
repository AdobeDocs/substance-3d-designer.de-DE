---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/crop.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Zuschneiden", um Materialausgaben auf bestimmte Bereiche zuzuschneiden, um gescannte Materialien und Texturen zu verarbeiten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Zuschneiden
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# Zuschneiden

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-10.png){width="128px"}

![](../../../../../../assets/crop-grayscale.png){width="128px"}

## Zuschneiden (Graustufen)

**In:** *Materialfilter/Scanverarbeitung*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Beim Freistellen handelt es sich um eine parametrische, nicht-destruktive Version des bekannten Freistellungswerkzeugs. Wenn Sie einen Bereich eines Bildes auswählen, wird das Ergebnis mit den nicht ausgewählten Bereichen zurückgegeben.

Es kann in vielerlei Hinsicht nützlich sein, da die Durchführung eines Freistellungsvorgangs mit Atomknoten nicht so einfach ist. Dieser Knoten ist besonders für die Konvertierung von nicht quadratischen Bildern nützlich. Stellen Sie in diesem Fall sicher, dass die Eingangsauflösung korrekt eingestellt ist.

Es ist sehr wichtig zu verstehen, dass Sie, um diesen Knoten problemlos verwenden zu können, die Möglichkeit nutzen müssen, eine Vorschau eines anderen Knotens als des Knotens anzuzeigen, dessen Parameter Sie bearbeiten!\
Kurz gesagt: **Doppelklicken Sie auf** den Knoten, den Sie als Eingabe für diesen Knoten verwenden (das ursprüngliche, nicht zugeschnittene Bild), und **klicken Sie einmal** auf den Zuschneideknoten, der direkt danach folgt. Sie können dann das Zuschneide-Gizmo an den Bereich anpassen, auf den Sie zuschneiden möchten.

## Parameter

* **Eingabegröße**: *0 - 8192* Auflösung und Proportionen des Eingabebildes. Sehr wichtig für nicht quadratische Bilder.
* **Hintergrund**: *(Farbwert) / (Graustufenwert)*Einheitlicher Hintergrundwert für Bereiche, die nicht von der Freistellung abgedeckt werden.
* **Transformieren**: *(Transformationsmatrix)*\
  Dreht und skaliert das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden.
* **Offset**: *0.0 - 1.0*\
  Verschiebt oder verschiebt das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden.
* **Ist normal (nur für Farbversion)**: *Falsch/Wahr* Ob die Eingabe als Normalmap behandelt werden soll oder nicht.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/crop.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Zuschneiden", um Material-Ausgaben auf bestimmte Bereiche zuzuschneiden, um gescannte Materialien und Texturen zu verarbeiten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Zuschneiden
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 3%

---


# Zuschneiden

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](crop.resources/crop-10.png){width="128px"}

![](crop.resources/crop-grayscale.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Beim Freistellen handelt es sich um eine parametrische, nicht-destruktive Version des bekannten Freistellungswerkzeugs. Wenn Sie einen Bereich eines Bildes auswählen, wird das Ergebnis mit den nicht ausgewählten Bereichen zurückgegeben.

Dies kann auf viele Arten nützlich sein, da die Durchführung eines Freistellungsvorgangs mit elementaren Knoten nicht so einfach ist. Dieser Knoten ist besonders für die Konvertierung von nicht quadratischen Bildern nützlich. Stellen Sie in diesem Fall sicher, dass die Eingangsauflösung korrekt eingestellt ist.

Es ist sehr wichtig zu verstehen, dass Sie, um diesen Knoten problemlos verwenden zu können, die Möglichkeit nutzen müssen, eine Vorschau eines anderen Knotens als des Knotens anzuzeigen, dessen Parameter Sie bearbeiten!\
Kurz gesagt: **Doppelklicken Sie auf** den Knoten, den Sie als Eingabe für diesen Knoten verwenden (das ursprüngliche, nicht zugeschnittene Bild), und **klicken Sie einmal** auf den Zuschneideknoten, der direkt danach folgt. Sie können dann das Zuschneide-Gizmo an den Bereich anpassen, auf den Sie zuschneiden möchten.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Eingabegröße</b> <i>0 - 8192</i> | Eingabebilds Auflösung und Proportionen. Sehr wichtig für nicht quadratische Bilder. |
| <b>Hintergrund</b> <i>(Farbwert) / (Graustufenwert)</i> | Einheitlicher Hintergrundwert für Bereiche, die nicht von der Freistellung abgedeckt sind. |
| <b>Transformieren</b> <i>(Transformationsmatrix)</i> | Dreht und skaliert das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Offset</b> <i>0.0 - 1.0</i> | Verschiebt oder Kamera bewegt das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Ist normal (nur für Farbversion)</b> <i>False/True</i> | Gibt an, ob die Eingabe als Normalmap behandelt werden soll. |

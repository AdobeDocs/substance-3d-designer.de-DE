---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kantenerkennung", um Kanten in Texturen zum Erstellen von Konturen und Kantenmasken-Effekten zu erkennen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kantenerkennung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# Kantenerkennung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-detect.resources/edge-detect-01.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erkennt den Kontrast in Schwarz-Weiß-Bildern und erzeugt dann eine Schwarz-weiße Maske, die den Kontrast hervorhebt.

Dies ist in vielen Fällen nützlich, wenn eine Maske für Kanten benötigt wird. Beachten Sie, dass dies am besten mit kontrastreichen Inputs funktioniert. Passen Sie bei Bedarf den Kontrast an, bevor Sie etwas an diesen Knoten übergeben.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kantenbreite</b> <i>1.0 - 16.0</i> | Breite der erkannten Bereiche um die Kanten. |
| <b>Kantenrundung</b> <i>0.0 - 16.0</i> | Rundet, verwischt und glättet die generierte Maske. |
| <b>Umkehren</b> <i>False/True</i> | Kehrt das Ergebnis um. |
| <b>Toleranz</b> <i>0.0 - 1.0</i> | Der Toleranzschwellenwert bestimmt, wo Kanten erscheinen sollen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-detect.resources/edge-detect-02.png" />
        </td>
    </tr>
</table>

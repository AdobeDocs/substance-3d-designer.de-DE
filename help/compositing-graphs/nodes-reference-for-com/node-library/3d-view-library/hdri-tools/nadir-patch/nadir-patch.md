---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Verwenden Sie den Nadir Patch -Knoten, um den Tiefpunkt der HDR-Panoramen zu korrigieren, um Artefakte am unteren Rand in Umgebungs-Map zu beheben.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir Patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 5%

---


# Nadir Patch

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](nadir-patch.resources/nadir-patch-01.png){width="200px"}

<b>In:</b> 3D-Ansicht > HDRI-Werkzeugs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Boden bietet Funktionen zum Überflicken des mittleren Knotenpunkts (Nadir) eines kugelförmig zugeordneten Bilds. Es kann verwendet werden, um ein hässliches Nadir, eine sichtbare Kamera oder ein Stativ auszublenden oder &quot;auszuklonen&quot;. Es funktioniert wie ein [Klon-Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md), jedoch mit Anpassungen für sphärisch zugeordnete Bilder. Der Benutzer wählt einen Punkt an einer anderen Stelle im Bild aus, das ist der geklonte Punkt, der am Nadir eingeblendet wird. Es sind keine weiteren externen Eingaben erforderlich, außer einer einzelnen HDRI, aber für den Patch-Effekt kann eine externe Maske als Alpha verwendet werden.

Der Effekt kann schnell mit [Nadir Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md) überprüft und validiert werden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Farbeingabe</i> |  |
| <b>Maskeneingabe</b> <i>Graustufen-Eingabe</i> | Optionaler Maskenschlitz zum Maskieren des Patches. Funktioniert wie ein Alpha. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Aktivieren</b> <i>False/True</i> | Aktivieren oder Deaktivieren des Patching-Effekts. |
| <b>Rahmen-Helfer anzeigen</b> <i>False/True</i> | Ein- oder Ausblenden der Helfer-Zeilen zum Debuggen. |
| <b>Rahmen Thickness</b> <i>0.0 - 1.0</i> | Thickness von Helfern. |
| <b>Patch-Skalierung</b> <i>0.0 - 1.0</i> | Globale, einheitliche Patch-Skalierung. Wirkt sich sowohl auf Quell- als auch auf Zielebene aus. |
| <b>Patch-Größe</b> <i>0.0 - 1.0</i> | Uneinheitliche Größe des Pflasters. |
| <b>Patch-Drehung</b> <i>0.0 - 1.0</i> | Drehen des Pflasters. Betrifft Quelle und Ziel. |
| <b>Patch-Alpha</b> <i>Quadratisch glätten, Gaußsch, Maskeneingabe</i> | Lege fest, mit welcher Alpha-Zahl die Farbfläche mit dem Hintergrund überblendet wird. |
| <b>Patch-Härte</b> <i>0.0 - 1.0</i> | Legen Sie die Härte/den Kontrast von Alpha fest. |
| <b>Offset für Quelldrehung</b> <i>0.0 - 1.0</i> | Drehung nur für Quelle des Pflasters. |
| <b>Positionskoordinaten</b> |  |
| <b>Quellposition</b> | Position der Quelle. Hat in der 2D-Ansicht Einfluss. |
| <b>Patch-Position</b> | Zielposition. Hat in der 2D-Ansicht Einfluss. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="nadir-patch.resources/nadir-patch-02.gif" />
        </td>
    </tr>
</table>

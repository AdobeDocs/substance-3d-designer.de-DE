---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Licht formen , um HDRI-Umgebungen benutzerdefinierte Lichtquellen für kreative Beleuchtungseffekte hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape Light
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 5%

---


# Shape Light

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

<b>In:</b> 3D-Ansicht > HDRI-Werkzeugs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine sphärisch projizierte rechteckige Form. Die Formtransformation wird durch ein Transformations-Gizmo gesteuert.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Hintergrundbildeingabe</b> <i>Farbeingabe</i> | Optionaler Hintergrund, auf dem das erzeugte Licht komponiert werden soll. |
| <b>Shape-Image-Eingabe</b> <i>Farbeingabe</i> | Optionales Bild für die Zuordnung zu Sphäre-Licht. Wird nur verwendet, wenn der Formfarbmodus auf &quot;Bildeingabe&quot; eingestellt ist. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Formmatrix</b> |  |
| <b>Matrix</b> <i>(Transformationsmatrix)</i> | Transformationssteuerung für das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Offset</b> <i>-2.0 - 2.0</i> | Verschiebt oder verschiebt das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Form</b> <i>Rechteck, Datenträger</i> | Wähle die Form aus, die platziert werden soll. |
| <b>Formfarbmodus</b> <i>RGB, Temperatur (Kelvin), Bildeingabe</i> | Wählen Sie die Methode aus, die zum Festlegen der Formfarbe verwendet werden soll. Image Input ermöglicht die Verwendung des zweiten Eingangssteckplatzes. |
| <b>Farbe</b> <i>(Farbwert)</i> | Nur bei RGB als Formfarbmodus. Wählt Farbe für die Form. |
| <b>Formtemperatur</b> <i>800.0 - 20000.0</i> | Nur, wenn der Formfarbmodus auf &quot;Temperatur&quot; eingestellt ist. Legt den Kelvin-Wert für die Formfarbe fest. |
| <b>Gamma für Shape-Image-Eingabe</b> <i>sRGB, linear</i> | Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Legen Sie fest, wie die Formbildeingabe interpretiert wird. |
| <b>Formexposition (EV)</b> <i>0.0 - 10.0</i> | Belichtungswert für generierte Form festlegen, optimal abgestimmt auf den Belichtungswert des Hintergrundbilds. |
| <b>Shape-Härte</b> <i>0.0 - 1.0</i> | Härte von Formkanten festlegen. |
| <b>Hotspot-Belichtung (EV)</b> <i>0.0 - 10.0</i> | Belichtung des zentralen Hotspots festlegen. Beachten Sie, dass dies im RGB-Modus nicht sehr sichtbar ist. |
| <b>Hotspot-Größe</b> <i>0.0 - 1.0</i> | Größe des zentralen Hotspots. |
| <b>Hotspot-Falloff</b> <i>0.0 - 1.0</i> | Abfall des zentralen Hotspots. |
| <b>Hotspot-Position</b> <i>0.0 - 1.0</i> | X- und Y-Position des zentralen Hotspots. |
| <b>Hintergrundeingabe aktivieren</b> <i>False/True</i> | Schaltet die Verwendung des optionalen Hintergrundbilds um. Kompositionen generierten Licht auf dem Hintergrund. |
| <b>Hintergrundfarbe</b> <i>(Farbwert)</i> | Wenn die Option &quot;Hintergrundeingabe&quot; nicht verwendet wird, legen Sie hier einen Wert für einen einfarbigen Hintergrund fest. |
| <b>Hintergrund-Gamma</b> <i>sRGB, linear</i> | Wenn die Hintergrundeingabe verwendet wird, legen Sie fest, wie die Hintergrundeingabe interpretiert werden soll. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shape-light-ex.gif" />
        </td>
    </tr>
</table>

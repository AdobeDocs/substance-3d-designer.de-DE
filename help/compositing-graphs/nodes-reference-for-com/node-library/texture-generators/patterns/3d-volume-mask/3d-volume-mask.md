---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten 3D-Volumenmaske , um Volumenmasken basierend auf der 3D-Position für erweiterte Material-Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Volumenmaske
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# 3D-Volumenmaske

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-volume-mask.resources/3dvolumemask.png){width="256px"}

<b>In:</b> Generator > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Volume Mask** generiert eine Darstellung einer *primitiven Form*, die auf der **Position**-Eingabe-Map basiert.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Position</b> <i>Farbe</i> | Die Karte, die die *3D-Raumkoordinaten* beschreibt, in denen die Grundform dargestellt wird.<br><br>Die **X/Y/Z**-Koordinaten werden den **R/G/B**-Kanälen zugeordnet. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Form</b> <i>Integer</i> | Die Grundform, die dargestellt werden soll:<br><br>- *Cube*<br>- *Zylinder*<br>- *Kugel* |
| <b>Skalierung</b> <i>Gleitend</i> | Definiert die *globale*-Skalierung der primitiven Ebene, die *einheitlich* auf alle Achsen angewendet wird. |
| <b>Größe</b> <i>Float3</i> | Legt die Größe der Form auf jeder Achse fest. |
| <b>Positionseingabe</b> <i>Integer</i> | Die Methode von *, die Leerzeichen* durch die **Position**-Eingabe darstellt:<br><br>- *UV Position*: Verwenden Sie eine *UV-Map*. Die X/Y (U/V)-Koordinaten werden den R/G-Kanälen zugeordnet. Die Z-Achse wird als *orthogonaler Vorwärtsvektor* angenommen.<br>- *Welt-Raum Position*: Verwenden Sie eine *Positionszuordnung*, um die Grundform im 3D-Raum zuzuordnen. Die X/Y/Z-Koordinaten werden den R/G/B-Kanälen zugeordnet. |
| <b>UV</b> positionieren <i>Float2</i> | Die Position der Grundform im UV-Raum.<br><br>*Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Positionseingabe** auf *UV-Position* festgelegt ist. |
| <b>Position</b> <i>Float3</i> | Die Position der Grundform im Welt-Raum.<br><br>*Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Positionseingabe** auf *Weltraumposition* festgelegt ist. |
| <b>Drehung</b> <i>Float3</i> | Definiert die Drehung der Form im Welt-Raum. |
| <b>Weiche Kante</b> <i>Gleitend</i> | Passt die Breite des *verblassenden Farbverlaufs* von der Oberfläche der Grundform nach innen an. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant4.jpg" />
        </td>
    </tr>
</table>

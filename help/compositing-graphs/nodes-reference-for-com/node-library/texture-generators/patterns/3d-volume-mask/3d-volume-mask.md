---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten 3D-Volumenmaske , um volumetrische Masken basierend auf der 3D-Position für erweiterte Materialeffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Volumenmaske
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# 3D-Volumenmaske

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask.png){width="256px"}

**In:** Generator*/Pattern*

**Einfach**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Volume Mask** generiert eine Darstellung einer *primitiven Form* basierend auf der Eingabezuordnung **Position**.

</td>
</tr>
</table>

## Parameter

### Eingaben

* **Position** *Farbe*\
  Die Karte, die die *3D-Raumkoordinaten* beschreibt, in denen die Grundform dargestellt wird.\
  Die **X/Y/Z**-Koordinaten werden den **R/G/B**-Kanälen zugeordnet.

### Parameter

* **Shape** *Integer*\
  Die Grundform, die dargestellt werden soll:
  * *Cube*- *Zylinder*- *Kugel*
* **Skalierung** *Gleitend*\
  Definiert die *globale*-Skalierung der primitiven Ebene, die *einheitlich* auf alle Achsen angewendet wird.
* **Größe** *Gleitend3*\
  Definiert die Größe der Form auf jeder Achse.
* **Positionseingabe** *Ganzzahl*\
  Die Methode von *, die Leerzeichen* durch die **Position**-Eingabe darstellt:
  * *UV-Position*: Verwenden Sie eine *UV-Karte*. Die X/Y (U/V)-Koordinaten werden den R/G-Kanälen zugeordnet. Die Z-Achse wird als *orthogonaler Vorwärtsvektor* angenommen.
  * *Weltraumposition*: Verwenden Sie eine *Positionszuordnung*, um die Grundform im 3D-Raum zuzuordnen. Die X/Y/Z-Koordinaten werden den R/G/B-Kanälen zugeordnet.
* **UV** *Gleitkomma2* positionieren\
  Die Position der Grundform im UV-Raum.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Positionseingabe** auf *UV-Position* festgelegt ist.
* **Position** *Gleitkomma3*\
  Die Position des Primitiven im Weltraum.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Positionseingabe** auf *Weltraumposition* festgelegt ist.
* **Drehung** *Gleitend3*\
  Definiert die Drehung der Form im Welt-Raum.
* **Breite der weichen Kante** *Gleitend*\
  Passt die Breite des *verblassenden Farbverlaufs* von der Oberfläche der Grundform nach innen an.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant4.jpg){width="256px"}

</td>
</tr>
</table>

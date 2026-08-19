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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# Shape Light

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

## Shape Light

**In:** *3D-Ansicht/HDRI-Werkzeuge*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine sphärisch projizierte rechteckige Form. Die Formtransformation wird durch ein Transformations-Gizmo gesteuert.

## Eingaben

* **Hintergrundbildeingabe**: *Farbeingabe* Optionaler Hintergrund, auf dem das erzeugte Licht zusammengesetzt werden soll.
* **Shape Image Input**: *Farbeingabe* Optionales Bild zur Zuordnung zu Sphäre-Licht. Wird nur verwendet, wenn der Formfarbmodus auf &quot;Bildeingabe&quot; eingestellt ist.

## Parameter

* **Formmatrix**
  * **Matrix**: *(Transformationsmatrix)*\
    Transformationssteuerung für das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden.
  * **Offset**: *-2.0 - 2.0*\
    Verschiebt oder verschiebt das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden.
* **Form**: *Rechteck, Datenträger*\
  Wähle die Form aus, die platziert werden soll.
* **Formfarbmodus**: *RGB, Temperatur (Kelvin), Bildeingabe*\
  Wählen Sie die Methode aus, die zum Festlegen der Formfarbe verwendet werden soll. Image Input ermöglicht die Verwendung des zweiten Eingangssteckplatzes.
* **Farbe**: *(Farbwert)*\
  Nur bei RGB als Formfarbmodus. Wählt Farbe für die Form.
* **Formtemperatur**: *800.0 - 20000.0*\
  Nur, wenn der Formfarbmodus auf &quot;Temperatur&quot; eingestellt ist. Legt den Kelvin-Wert für die Formfarbe fest.
* **Gamma für Shape-Image-Eingabe**: *sRGB, linear*\
  Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Legen Sie fest, wie die Formbildeingabe interpretiert wird.
* **Formexposition (EV)**: *0.0 - 10.0*\
  Belichtungswert für generierte Form festlegen, optimal abgestimmt auf den Belichtungswert des Hintergrundbilds.
* **Formhärte**: *0.0 - 1.0*\
  Härte von Formkanten festlegen.
* **Hotspot-Exposition (EV)**: *0.0 - 10.0*\
  Belichtung des zentralen Hotspots festlegen. Beachten Sie, dass dies im RGB-Modus nicht sehr sichtbar ist.
* **Hotspot-Größe**: *0.0 - 1.0*\
  Größe des zentralen Hotspots.
* **Hotspot-Falloff**: *0.0 - 1.0*\
  Abfall des zentralen Hotspots.
* **Hotspot-Position**: *0.0 - 1.0*\
  X- und Y-Position des zentralen Hotspots.
* **Hintergrundeingabe aktivieren**: *False/True*\
  Schaltet die Verwendung des optionalen Hintergrundbilds um. Kompositionen generierten Licht auf dem Hintergrund.
* **Hintergrundfarbe**: *(Farbwert)*\
  Wenn die Option &quot;Hintergrundeingabe&quot; nicht verwendet wird, legen Sie hier einen Wert für einen einfarbigen Hintergrund fest.
* **Gamma im Hintergrund**: *sRGB, linear* Wenn die Hintergrundeingabe verwendet wird, legen Sie fest, wie die Hintergrundeingabe interpretiert werden soll.

## Beispielbilder

![](../../../../../../assets/shape-light-ex.gif)

</td>
</tr>
</table>

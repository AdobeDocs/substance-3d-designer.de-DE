---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kugellicht", um HDRI-Umgebungen kugelförmige Lichtquellen hinzuzufügen, um eine verbesserte Beleuchtungssteuerung zu ermöglichen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kugellicht
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Kugellicht

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-sphere-light.png){width="200px"}

## Kugellicht

**In:** *3D-Ansicht/HDRI-Werkzeuge*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine kugelförmig projizierte Kugelform. Die Transformation der Kugel wird von einem Transformations-Gizmo gesteuert.

Das Kugellicht ist ziemlich vielseitig und verfügt über Optionen, mit denen es nicht nur einfache runde Lichter erzeugen kann, sondern auch Planeten oder andere Himmelskörper. Wenn Sie die erweiterten Beleuchtungs- und Drehungsoptionen nicht benötigen, sehen Sie sich stattdessen [Formenlicht](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) an.

## Eingaben

* **Hintergrundbildeingabe**: *Farbeingabe* Optionaler Hintergrund, auf dem das erzeugte Licht zusammengesetzt werden soll.
* **Shape Image Input**: *Farbeingabe* Optionales Bild zur Zuordnung zu Sphäre-Licht. Wird nur verwendet, wenn der Formfarbmodus auf &quot;Bildeingabe&quot; eingestellt ist.

### Parameter

* **Positionsmodus**: *Abstand zum Ursprung, Weltposition*\
  Wählen Sie zwischen zwei Platzierungsmodi. Abstand zum Ursprung ist ähnlich wie Polarkoordinaten, die Kugel ist relativ zum Mittelpunkt des Panoramas festgelegt, die Weltposition funktioniert wie Standard-3D-Koordinaten.
* **Positionskoordinaten**
  * **Vektor nach oben**: *Z nach oben, J nach oben*\
    Nur mit dem Modus &quot;Weltposition&quot; bestimmen Sie die Ausrichtung des Koordinatensystems.
  * **Sphere World Position**: *-2.0 - 2.0*\
    Nur im Modus &quot;Weltposition&quot; wird die Kugelposition im Weltraum festgelegt.
  * **Position**:\
    Nur im Abstand zum Ursprung-Modus. Legt die Position relativ zur Mitte fest. Kann in der 2D-Ansicht bearbeitet werden.
  * **Abstand zum Ursprung**: *0.0 - 20.0* Nur mit Abstand zum Ursprung-Modus. Legt den Abstand zum Ursprung fest und beeinflusst die sichtbare Größe der Kugel.
* **Formfarbmodus**: *RGB, Temperatur (Kelvin), Bildeingabe*\
  Wählen Sie die Methode aus, die zum Festlegen der Formfarbe verwendet werden soll. Image Input ermöglicht die Verwendung des zweiten Eingangssteckplatzes.
* **Farbe**: *(Farbwert)*\
  Nur bei RGB als Formfarbmodus. Wählt Farbe für die Form.
* **Formtemperatur**: *800.0 - 20000.0*\
  Nur, wenn der Formfarbmodus auf &quot;Temperatur&quot; eingestellt ist. Legt den Kelvin-Wert für die Formfarbe fest.
* **Sphere Image Input Gamma**: *sRGB, linear*\
  Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Legen Sie fest, wie die Formbildeingabe interpretiert wird.
* **Drehung der Kugel**: *0.0 - 1.0*\
  Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Dreht die Kugel um ihren Mittelpunkt, um das zugeordnete Bild auszurichten.
* **Exposition (EV)**: *0.0 - 10.0*\
  Belichtungswert für generierte Form festlegen, optimal abgestimmt auf den Belichtungswert des Hintergrundbilds.
* **Kugelradius**: *0.0 - 1.0*\
  Legt den Radius/die Größe der Kugel fest.
* **Kugelhärte**: *0.0 - 1.0*\
  Legt die Härte/Abfall der Kugel fest.
* **Schattierung**: *Keiner, Gliedmaßenabdunklung, Schattierung leicht*\
  Stellen Sie ein, ob eine Schattierung auf die Kugel angewendet werden soll. Erlaubt, dass die Kugel nicht als durchgehendes, unbeleuchtetes Objekt angezeigt wird. Gliedmaßenabdunklung bedeutet, dass an den Kanten eine leichte Abdunklung auftritt. &quot;Schattierung-Licht&quot; bedeutet, dass die Kugel mit einem optionalen &quot;Schattierung-Licht&quot; beleuchtet wird.
* **Schattierung Lichtweltposition**: *-1.0 - 1.0*\
  Ist die Schattierung auf &quot;Lichtposition&quot; eingestellt, wird die Schattierung des Lichtes auf die Kugel gesteuert.
* **Penombra-Transparenz**: *0.0 - 1.0*\
  Wenn Schattierung auf Schattierung-Licht eingestellt ist, steuert den Abfall der Schattierung.
* **Hintergrundeingabe aktivieren**: *False/True*\
  Schaltet die Verwendung des optionalen Hintergrundbilds um. Kompositionen generierten Licht auf dem Hintergrund.
* **Hintergrundfarbe**: *(Farbwert)*\
  Wenn die Option &quot;Hintergrundeingabe&quot; nicht verwendet wird, legen Sie hier einen Wert für einen einfarbigen Hintergrund fest.
* **Gamma im Hintergrund**: *sRGB, linear* Wenn die Hintergrundeingabe verwendet wird, legen Sie fest, wie die Hintergrundeingabe interpretiert werden soll.

## Beispielbilder

![](../../../../../../assets/sphere-light-ex.gif)

![](../../../../../../assets/spherelight-ex1.png)

</td>
</tr>
</table>

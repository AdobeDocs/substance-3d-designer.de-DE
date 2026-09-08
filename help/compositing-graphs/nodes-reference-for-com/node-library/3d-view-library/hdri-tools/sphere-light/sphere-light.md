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
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 4%

---


# Kugellicht

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/panorama-sphere-light.png){width="200px"}

<b>In:</b> 3D-Ansicht > HDRI-Werkzeugs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine kugelförmig projizierte Kugelform. Die Transformation der Kugel wird von einem Transformations-Gizmo gesteuert.

Das Kugellicht ist ziemlich vielseitig und verfügt über Optionen, mit denen es nicht nur einfache runde Lichter erzeugen kann, sondern auch Planeten oder andere Himmelskörper. Wenn Sie die erweiterten Beleuchtungs- und Drehungsoptionen nicht benötigen, sehen Sie sich stattdessen [Formenlicht](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) an.

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
| <b>Positionsmodus</b> <i>Abstand zum Ursprung, Weltposition</i> | Wählen Sie zwischen zwei Platzierungsmodi. Abstand zum Ursprung ist ähnlich wie Polarkoordinaten, die Kugel ist relativ zum Mittelpunkt des Panoramas festgelegt, die Weltposition funktioniert wie Standard-3D-Koordinaten. |
| <b>Positionskoordinaten</b> |  |
| <b>Vektor nach oben</b> <i>Z nach oben, J nach oben</i> | Nur mit dem Modus &quot;Weltposition&quot; bestimmen Sie die Ausrichtung des Koordinatensystems. |
| <b>Sphere World Position</b> <i>-2.0 - 2.0</i> | Nur im Modus &quot;Weltposition&quot; wird die Kugelposition im Weltraum festgelegt. |
| <b>Position</b> | Nur im Abstand zum Ursprung-Modus. Legt die Position relativ zur Mitte fest. Kann in der 2D-Ansicht bearbeitet werden. |
| <b>Abstand zum Ursprung</b> <i>0.0 - 20.0</i> | Nur im Abstand zum Ursprung-Modus. Legt den Abstand zum Ursprung fest und beeinflusst die sichtbare Größe der Kugel. |
| <b>Formfarbmodus</b> <i>RGB, Temperatur (Kelvin), Bildeingabe</i> | Wählen Sie die Methode aus, die zum Festlegen der Formfarbe verwendet werden soll. Image Input ermöglicht die Verwendung des zweiten Eingangssteckplatzes. |
| <b>Farbe</b> <i>(Farbwert)</i> | Nur bei RGB als Formfarbmodus. Wählt Farbe für die Form. |
| <b>Formtemperatur</b> <i>800.0 - 20000.0</i> | Nur, wenn der Formfarbmodus auf &quot;Temperatur&quot; eingestellt ist. Legt den Kelvin-Wert für die Formfarbe fest. |
| <b>Sphere Image Input Gamma</b> <i>sRGB, linear</i> | Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Legen Sie fest, wie die Formbildeingabe interpretiert wird. |
| <b>Drehung der Kugel</b> <i>0.0 - 1.0</i> | Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Dreht die Kugel um ihren Mittelpunkt, um das zugeordnete Bild auszurichten. |
| <b>Belichtung (EV)</b> <i>0.0 - 10.0</i> | Belichtungswert für generierte Form festlegen, optimal abgestimmt auf den Belichtungswert des Hintergrundbilds. |
| <b>Kugelradius</b> <i>0.0 - 1.0</i> | Legt den Radius/die Größe der Kugel fest. |
| <b>Sphere-Härte</b> <i>0.0 - 1.0</i> | Legt die Härte/Abfall der Kugel fest. |
| <b>Schattierung</b> <i>Keine, Gliedmaßenabdunklung, Schattierung leicht</i> | Stellen Sie ein, ob eine Schattierung auf die Kugel angewendet werden soll. Erlaubt, dass die Kugel nicht als durchgehendes, unbeleuchtetes Objekt angezeigt wird. Gliedmaßenabdunklung bedeutet, dass an den Kanten eine leichte Abdunklung auftritt. &quot;Schattierung-Licht&quot; bedeutet, dass die Kugel mit einem optionalen &quot;Schattierung-Licht&quot; beleuchtet wird. |
| <b>Schattierung Lichtweltposition</b> <i>-1.0 - 1.0</i> | Ist die Schattierung auf &quot;Lichtposition&quot; eingestellt, wird die Schattierung des Lichtes auf die Kugel gesteuert. |
| <b>Penombra-Transparenz</b> <i>0.0 - 1.0</i> | Wenn Schattierung auf Schattierung-Licht eingestellt ist, steuert den Abfall der Schattierung. |
| <b>Hintergrundeingabe aktivieren</b> <i>False/True</i> | Schaltet die Verwendung des optionalen Hintergrundbilds um. Kompositionen generierten Licht auf dem Hintergrund. |
| <b>Hintergrundfarbe</b> <i>(Farbwert)</i> | Wenn die Option &quot;Hintergrundeingabe&quot; nicht verwendet wird, legen Sie hier einen Wert für einen einfarbigen Hintergrund fest. |
| <b>Hintergrund-Gamma</b> <i>sRGB, linear</i> | Wenn die Hintergrundeingabe verwendet wird, legen Sie fest, wie die Hintergrundeingabe interpretiert werden soll. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/sphere-light-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/spherelight-ex1.png" />
        </td>
    </tr>
</table>

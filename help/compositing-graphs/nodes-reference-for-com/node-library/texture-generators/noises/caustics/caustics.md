---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kaustik", um kaustische Lichtmuster zum Erzeugen von Unterwasser- und refraktiven Lichteffekten zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kaustik
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# Kaustik

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](caustics.resources/caustics-01.png){width="128px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt projizierte Kaustik basierend auf einem Höhen-Map und einer Lichtrichtung.Die Optionen sind in den Versionen &quot;Graustufen&quot; und &quot;Farbe&quot; verfügbar. Die Unterschiede sind dezent. Mit der Farbversion werden jedoch Effekte für die Farbstreuung hinzugefügt. Licht wird von einem einzigen Punkt Geworfen, es wird kein Umgebungs-Map verwendet.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ausgabefarbraum</b> <i>Raw, sRGB</i> | Festlegen des Ausgabefarbraums. |
| <b>Größe des Foton-Rasters</b> <i>Auto, 512, 1024, 2048, 4096</i> | Legt die Qualität durch Anpassung der Raster-Größe fest, standardmäßig jedoch durch Anpassen der Eingabe. Kann zur Beschleunigung der Berechnung verwendet werden. |
| <b>Surface Height Scale</b> <i>0.0 - 1.0</i> | Multiplikator, um festzulegen, wie das Height interpretiert wird. |
| <b>Position des Surface-Heights</b> <i>0.0 - 1.0</i> | Abstand der brechenden Fläche von der Projektion einstellen. |
| <b>Surface IOR</b> <i>1.0 - 2.0</i> | Legen Sie den Brechungsindex fest, um in der Farbversion mehr Streuung zu erhalten. |
| <b>Fotonengröße</b> <i>1.0 - 50.0</i> | Die Fotonengröße beeinflusst die Knautschigkeit des Effekts. |
| <b>Dispersion</b> <i>0.0 - 0.01 (nur Farbversion)</i> | Nur die Farb-Streuung. Nicht sichtbar, wenn der IOR niedrig ist. |
| <b>Jittering</b> <i>0.0 - 1.0</i> | Unregelmäßiges Jittern zu den Geworfen Foton-Partikeln hinzufügen. |
| <b>Lichtposition</b> | Verschiebt die Lichtposition. Auch durch ein Gizmo in der 2D-Ansicht. |
| <b>Hintergrundfarbe</b> <i>(Farbwert) (nur Farbversion)</i> | Ändern Sie die Hintergrundfarbe. Beschränkt auf Schwarz in der Graustufenversion. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Aktivieren Sie die Kompensation von Quetschen und Dehnen mit nicht quadratischen Verhältnissen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="caustics.resources/caustics-02.png" />
        </td>
    </tr>
</table>

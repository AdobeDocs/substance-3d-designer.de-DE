---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Kaustik

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

**In:** *Texturgeneratoren**/Noises*

**Komplex**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt projizierte Kaustik basierend auf einem Höhen-Map und einer Lichtrichtung.Die Optionen sind in den Versionen &quot;Graustufen&quot; und &quot;Farbe&quot; verfügbar. Die Unterschiede sind dezent. Mit der Farbversion werden jedoch Effekte für die Farbstreuung hinzugefügt. Licht wird von einem einzigen Punkt Geworfen, es wird kein Umgebungs-Map verwendet.

</td>
</tr>
</table>

## Parameter

* **Ausgabefarbraum**: *Raw, sRGB*\
  Festlegen des Ausgabefarbraums.
* **Foton Raster Size**: *Auto, 512, 1024, 2048, 4096*\
  Legt die Qualität durch Anpassung der Raster-Größe fest, standardmäßig jedoch durch Anpassen der Eingabe. Kann zur Beschleunigung der Berechnung verwendet werden.
* **Surface Height Scale**: *0.0 - 1.0*\
  Multiplikator, um festzulegen, wie das Height interpretiert wird.
* **Position des Surface-Heights**: *0.0 - 1.0*\
  Abstand der brechenden Fläche von der Projektion einstellen.
* **Surface IOR**: *1.0 - 2.0*\
  Legen Sie den Brechungsindex fest, um in der Farbversion mehr Streuung zu erhalten.
* **Fotonengröße**: *1.0 - 50.0*\
  Die Fotonengröße beeinflusst die Knautschigkeit des Effekts.
* **Streuung**: *0.0 - 0.01 (nur Farbversion)*\
  Nur die Farb-Streuung. Nicht sichtbar, wenn der IOR niedrig ist.
* **Jittering**: *0.0 - 1.0*\
  Unregelmäßiges Jittern zu den Geworfen Foton-Partikeln hinzufügen.
* **Lichtposition**:\
  Verschiebt die Lichtposition. Auch durch ein Gizmo in der 2D-Ansicht.
* **Hintergrundfarbe**: *(Farbwert) (nur Farbversion)*\
  Ändern Sie die Hintergrundfarbe. Beschränkt auf Schwarz in der Graustufenversion.
* **Quadratische Ausbreitung**: *False/True*\
  Aktivieren Sie die Kompensation von Quetschen und Dehnen mit nicht quadratischen Verhältnissen.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-caustics-grayscale-1.png" width="300px"/></div> |
| --- |
|  |

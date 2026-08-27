---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Spline Mapper Grayscale, um Graustufen-Texturen entlang von Spline-Pfaden mit anpassbaren Parametern zuzuordnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Mapper Graustufen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---


# Spline Mapper Graustufen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-mapper-grayscale-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ordnet ein Graustufenbild einer Grundform zu, die entlang der Eingabesplines gestreckt ist.

Die Grundform kann eine Ebene, ein Halbzylinder oder ein Zylinder sein. Die Zylinder können entlang der Spline verdreht werden, um das abgebildete Bild entsprechend zu verformen.

</td>
</tr>
</table>

Der Knoten gibt das zugeordnete Bild als Graustufenbild sowie weitere Informationen wie Height, UVs (d. h. Bildkoordinaten) und eine ID-Maske aus, mit der jeder zugeordnete Spline einzeln ausgewählt werden kann.

>[!IMPORTANT]
>
> Das Ergebnis kann unerwünschte Artefakte außerhalb der Hülle des Spline-Effekts sein, wenn sehr niedrige Werte für die Thickness verwendet werden. Dies ist ein bekanntes Problem.

>[!NOTE]
>
> Siehe auch [Spline Mapper Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md).

## Eingangsanschlüsse

<b>Spline-Kabel</b> *Farbe* Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:\
<b> R</b> - X-Position\
<b> G</b> - Y-Position\
<b> B</b> - Height\
<b>A</b> - Paketdaten:\
* Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).\
* Absoluter Wert: Thickness + 1.

<b>Spline-Daten</b> *Farbe* Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
<b> R</b> - Tangenten X\
<b> G</b> - Tangenten Y\
<b> B</b> - Nicht verwendet\
<b> A</b> - Nicht verwendet

<b>Spline-Betrag</b> *Integer* Die Anzahl der Eingabe-Splines.

<b>Farbzuordnung</b> *Graustufen* Das Graustufeneingabebild, das entlang der Eingabesplines zugeordnet werden soll.

<b>Height-Map</b> *Graustufen* Die Graustufen-Height-Zuordnungsdatei für die Eingabe, die entlang der Splines für die Eingabe zugeordnet werden soll.

<b>Twist Curve</b> *Graustufen* Das Bild, das eine Kurve anhand der Werte der ersten Pixelzeile beschreibt.\
Wenn der Parameter <b>Form</b> auf *Halbzylinder* oder *Zylinder* festgelegt ist, wird diese Eingabe verwendet, um die Verdrillung der UVs um die Form herum zu steuern. Die Auswirkungen werden mithilfe des Parameters <b>UVs-Kurvenmultiplikator verdrehen</b> gesteuert.\
Die Kurve bietet ein Profil für den Umfang der Drehung entlang der Spline, wobei das erste Pixel in der Zeile die Drehung am Anfang der Spline und das letzte die Drehung am Ende ist. Der Graustufenwert stellt eine Anzahl von Windungen dar.\
Sie können einen Knoten [Kurve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) verwenden, um die Kurve zu erstellen.

## Ausgangsanschlüsse

<b>Farbe</b> *Graustufen* Das Ergebnis der Zuordnung des Eingabefarbbilds über die Eingabesplines als Graustufenbild.

<b>Height</b> *Graustufen* Das Ergebnis der Zuordnung des Height-Eingabebilds über die Eingabe-Splines als Graustufenbild.

<b>UV</b> *Farbe* Die UVs (d. h. Koordinaten) der Zuordnung über die Eingabesplines hinweg, codiert in einem Farbbild.

<b>ID</b> *Graustufen* Eine Maske der Bilder, die entlang der Eingabe-Splines zugeordnet sind, wobei die weißen Werte von einem Spline zum nächsten um 1 erhöht werden, sodass jede Form unabhängig ausgewählt werden kann.

## Parameter

<b>Segmentierungsbetrag</b> *Integer* Splines werden in Segmente vereinfacht, bevor Bildkoordinaten sie durchlaufen.\
Eine größere Anzahl von Segmenten führt zu einer glatteren Zuordnung entlang von Kurven.

<b>UVs automatisch skalieren</b> *Boolean* Passt die Skalierung der Koordinaten automatisch an, um ein quadratisches Bild beizubehalten, wenn es den Splines zugeordnet wird.<b></b>

<b>UV-Skalierung</b> *Gleitkomma2* Passt die Skalierung der zugeordneten Koordinaten in X (horizontal) und Y (vertikal) an.\
Höhere Werte führen zu einem Bild mit dichteren Kacheln.<b></b>

<b>Modus</b> *Integer* Die Methode zum Auswählen der Splines, denen das Bild zugeordnet werden soll:\
*- Spline-Liste zeichnen*: Alle Splines in der Eingabeliste werden verwendet.\
*- Einzelne Spline zeichnen*: Es wird nur der Spline-Code mit dem angegebenen Index verwendet.\
*- Spline-Bereich zeichnen*: Es werden nur die Splines verwendet, deren Index im angegebenen Bereich enthalten ist.

<b>Spline-Index zeichnen</b> *Integer* (verfügbar, wenn &quot;Modus&quot; auf &quot;Einzelne Spline zeichnen&quot; festgelegt ist)Der Index der Spline, der das Bild zugeordnet werden soll.

<b>Spline-Bereich zeichnen</b> *Integer2* (verfügbar, wenn &quot;Modus&quot; auf &quot;Spline-Bereich zeichnen&quot; festgelegt ist)Der Indexbereich für die Splines, denen das Bild zugeordnet werden soll.

<b>Start</b> *Gleitend* Verschiebt den Anfang des Abschnitts des Splines, der zugeordnet werden soll.\
Der Wert stellt die normalisierte Länge des Splines dar.

<b>Ende</b> *Gleitend* Verschiebt das Ende des Abschnitts des Splines, der zugeordnet werden soll.\
Der Wert stellt die normalisierte Länge des Splines dar.

<b>Thickness-Modus</b> *Integer* Die Methode zum Festlegen der Thickness des zugeordneten Abbilds:\
*- Manuell*: Legen Sie die Thickness explizit mit einem beliebigen Wert fest.\
*- Aus Spline*: Verwenden Sie die Thickness des Splines.

<b>Thickness</b> *Gleitkommawert* (verfügbar, wenn &quot;Thickness-Modus&quot; auf &quot;Manuell&quot; festgelegt ist)Der willkürliche Wert für die Thickness des zugeordneten Bildes entlang der Splines.<b></b>

<b>Thicknessen-Multiplikator</b> *Gleitkommawert* (verfügbar, wenn &quot;Thickness-Modus&quot; auf &quot;Von Spline&quot; festgelegt ist)Ein globaler Multiplikator für die Thickness des zugeordneten Bildes entlang der Splines, wenn diese Thickness von der der Splines gesteuert wird.

<b>Form</b> *Integer* Die primitive Form, die zum Zuordnen von Bildkoordinaten entlang der Splines verwendet wird:\
*- Ebene*: Koordinaten werden einer flachen Ebene zugeordnet;\
*- Halbzylinder*: Koordinaten werden einem Halbzylinder zugeordnet, dessen Achse des Grundkreises der Richtung der Spline folgt;\
*- Zylinder*: Koordinaten werden einem Zylinder zugeordnet, dessen Achse des Grundkreises der Richtung der Spline folgt.<b></b>

<b>Zylinder-Height-Multiplikator</b> *Gleitend* (verfügbar, wenn &quot;Form&quot; auf &quot;Halbzylinder&quot; oder &quot;Zylinder&quot; festgelegt ist)Ein Multiplikator für die Intensität des Zylinderbeitrags zum Height in der Height-Ausgabe.\
Height-Anpassungen sind kumulierbar.

<b>Versatz des Heights des Zylinders</b> *Gleitend* (verfügbar, wenn &quot;Form&quot; auf &quot;Halbzylinder&quot; oder &quot;Zylinder&quot; eingestellt ist)\
Versetzt den Mittelpunkt des Formprofils &quot;Zylinder&quot; oder &quot;Halbzylinder&quot; von der Oberfläche des Splines auf einen Durchmesser unter der Oberfläche.

<b>UVs-Intensität verdrehen</b> *Gleitend* (verfügbar, wenn &quot;Form&quot; auf &quot;Halbzylinder&quot; oder &quot;Zylinder&quot; eingestellt ist)Die Verdrehung der Bildkoordinaten um den Zylinder in der Anzahl der Windungen.\
Beim Verdrehen wird der Zylinder nur am Ende der Keilverzahnung gedreht. Die Drehung wird dann entlang der Spline interpoliert.

<b>UVs-Kurvenmultiplikator verdrehen</b> *Gleitkommawert* (verfügbar, wenn &quot;Form&quot; auf &quot;Halbzylinder&quot; oder &quot;Zylinder&quot; eingestellt ist)Ein Multiplikator für die Intensität des Beitrags der Eingabe der Twist Curve zur Drehung des Zylinders.\
Die Kurve bietet ein Profil für den Umfang der Drehung entlang der Spline, wobei das erste Pixel in der Zeile die Drehung am Anfang der Spline und das letzte die Drehung am Ende ist. Der Graustufenwert stellt eine Anzahl von Windungen dar.

<b>UVs-Kurvenversatz verdrehen</b> *Gleitend* (verfügbar, wenn &quot;Form&quot; auf &quot;Halbzylinder&quot; oder &quot;Zylinder&quot; eingestellt ist)Wendet einen globalen Versatz auf die von der Twist Curve bereitgestellten Drehungswerte in der Anzahl der Windungen an.

<b>Spline-Height-Multiplikator</b> *Gleitend* Passt die Intensität des Beitrags der Spline-Height-Eingabe zur Height-Ausgabe an.\
Height-Anpassungen sind kumulativ.<b></b>

<b>Eingabe-Height-Multiplikator</b> *Gleitend* Passt die Intensität des Beitrags der Height-Map-Eingabe zur Height-Ausgabe an.\
Height-Anpassungen sind kumulierbar.

<b>Nicht-quadratische Korrektur </b>*Boolesch* Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht-quadratischen Auflösungen beizubehalten.\
Dies wirkt sich auch auf die einheitliche Verteilung aus.

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMapperGrayscale-Variant1-After.jpg" alt="SplineMapperGrayscale-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplineMapperGrayscale-Demo.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 3](../../../../../../assets/SplineMapperGrayscale-Variant1-After1.jpg "Knotenbeispiel 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

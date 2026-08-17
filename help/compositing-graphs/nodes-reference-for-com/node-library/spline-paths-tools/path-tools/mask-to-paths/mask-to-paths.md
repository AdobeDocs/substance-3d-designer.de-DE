---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "In Pfade maskieren", um Maskentexturen in Pfaddaten für die prozedurale Pfadgenerierung zu konvertieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Mask to Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Auf Pfade maskieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# Auf Pfade maskieren

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/mask-to-paths-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Konvertiert ein Graustufen-Eingabemuster <b>Maske</b> in eine Liste von Pfadsegmenten, die in der Ausgabe <b>Pfade</b> codiert sind.

Es stehen Steuerelemente über die Startposition von generierten Pfaden sowie deren Reihenfolge in der Liste zur Verfügung.

Die generierten Pfade können mithilfe dedizierter Knoten weiter verarbeitet werden - z. B. [Pfad 2D transformieren](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md), [Pfadeverkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md) - oder mithilfe des Knotens [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) in Splines konvertiert werden, um Formen entlang dieser Pfade zuzuordnen oder Streuungen zu erstellen.

</td>
</tr>
</table>

>[!NOTE]
>
> Die zum Codieren von Pfaden verwendete Methode wird auf der Seite [Paths Format Specifications](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) erläutert.

## Eingangsanschlüsse

<b>Maske</b> *Graustufen*\
Das Eingabemuster, das in eine Liste von Pfaden konvertiert werden soll.

## Ausgangsanschlüsse

<b>Vorschau</b> *Farbe* Eine Vorschau, die über der Maske erstellt wurde, um die Auswirkungen der Parameter zu veranschaulichen.

<b>Pfade</b> *Farbe*\
Eine Liste von in einem Farbbild codierten Pfaden. Jeder Pfad beschreibt eine Liste von codierten Segmenten.\
Das Ergebnis kann mit einem anderen Pfad verarbeitenden Knoten verarbeitet oder an einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)-Knoten gesendet werden, um es als Splines weiter zu verarbeiten.

## Parameter

<b>Maske glätten</b> *Gleitend*\
Wenden Sie Glättung auf die Eingabemaske an.\
Dies ist nützlich, wenn das Eingabemuster sehr scharfe Kanten aufweist, was in der Regel Artefakte verursacht.

<b>Schwellenwert für Maske</b> *Unverankert* Der Graustufenwert von <b>Maske</b>, der verwendet wird, um die Außenseite (Werte &lt; Schwellenwert für Maske) und die Innenseite (Werte > Schwellenwert für Maske) der Form zu trennen.

<b>Pfad dezimieren</b> *Float* Steuert implizit die Anzahl der zu generierenden Segmente.\
Bei einem hohen Dezimationswert sind runde Formen etwas polygonal, während bei keiner Dezimation fast ein Segment pro Pixel generiert wird.\
Ein angemessener Betrag entspricht besser der Form von Geraden und Kurven, ohne viele Zwischenpunkte für Geraden zu schaffen.

<b>Offene Pfade schließen</b> *Boolesch* Erstellen Sie ein Segment zwischen dem Anfangs- und dem Endscheitelpunkt offener Pfade.\
Wenn Sie diese Option deaktivieren, können unerwünschte Linien, die Ihr Muster auf unerwartete Weise durchlaufen, korrigiert werden. Pfade werden jedoch möglicherweise nicht mehr geschlossen.

<b>Eckschwellenwert</b> *Gleitkomma*\
Jeder in Pfaden codierte Scheitelpunkt kann ein Flag enthalten, das angibt, ob er hart (d. h. eine Ecke) oder glatt ist.\
Mit diesem Parameter können Sie mehr oder weniger Ecken entsprechend dem Winkel zwischen ihren benachbarten Segmenten markieren.\
*Hinweis:* Dieses &#39;corner&#39;-Flag wird derzeit von keinem vorhandenen Knoten unterstützt, ist aber für die Verwendung in einem [Path Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)-Knoten verfügbar. Sie können auch die Ecken mit dem Knoten [Vorschaupfade](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) anzeigen.

<b>Pfad-Startmodus</b> *Integer* Die Methode zum Auswählen, welcher Scheitelpunkt der Anfang jedes generierten Pfads um die Formen in der Maske sein soll.\
Dies hat erhebliche Auswirkungen auf die Konvertierung der generierten <b>Pfade in Splines</b> mithilfe des dedizierten Knotens, da mehrere Spline-Knoten den Start- und Endpunkt der Splines verwenden.\
*- Höchster Scheitelpunkt:* Der Scheitelpunkt, der den niedrigsten Winkel mit seinem vorherigen und nächsten Scheitelpunkt bildet\
*- Scheitelpunkt am äußersten Ende einer angegebenen Richtung:* Der letzte Scheitelpunkt in einer angegebenen Richtung\
*- Scheitelpunkt, der einer angegebenen Position am nächsten liegt
* Scheitelpunkt am weitesten von einer angegebenen Position
* Benutzerdefinierte Startfunktion:* Verwenden Sie eine benutzerdefinierte Funktion, um den Scheitelpunkt auszuwählen, der als Start für jeden Pfad verwendet werden soll

<b>Startrichtung</b> *Gleitend* Der Winkel, der die Richtung beschreibt, die zum Auswählen des Startscheitelpunkts verwendet wird. Für jeden Pfad wird der letzte Scheitelpunkt in dieser Richtung ausgewählt.\
Der Wert ist eine *Anzahl der Windungen*, die zum Drehen eines Vektors mit der Richtung X links verwendet werden. Das bedeutet, dass 0 einen Richtungsvektor von (-1, 0) und 0,25 (90 Grad) einen Richtungsvektor von (0, 1) festlegt.\
*Hinweis:* Dieser Parameter ist verfügbar, wenn <b>Pfad-Startmodus</b> auf &quot;Scheitelpunkt am äußersten Rand einer angegebenen Richtung&quot; festgelegt ist

<b>Startzielposition</b> *Float2* Die Position im Bild, an der der Startscheitelpunkt ausgewählt wurde.\
Für jeden Pfad wird der Scheitelpunkt ausgewählt, der dieser Position am nächsten bzw. am weitesten davon entfernt ist, entsprechend dem ausgewählten <b>Pfad-Startmodus</b>.\
*Hinweis:* Dieser Parameter ist verfügbar, wenn <b>Pfad-Startmodus</b> auf &quot;Scheitelpunkt, der einer angegebenen Position am nächsten liegt&quot; oder &quot;Scheitelpunkt, der von einer angegebenen Position am weitesten entfernt liegt&quot; festgelegt ist

<b>Startfunktion</b> *Gleitkommawert* Die Funktion, mit der der Startscheitelpunkt ausgewählt wurde. Es gibt einen Float -Wert zurück.\
Für jeden Scheitelpunkt wird die Funktion ausgeführt und der Scheitelpunkt ausgewählt, für den die Funktion das *höchste Ergebnis* zurückgibt.\
Verfügbare Variablen:\
*-* vertex.cornerness(Float)*:* Die Punktzahl des Vertexes als Kandidat für eine Ecke\
*-* vertex.pos(Float2)*:* Die Scheitelpunktposition im Bildbereich\
*Hinweis:* Dieser Parameter ist verfügbar, wenn der Pfad-Startmodus auf &quot;Scheitelpunkt, der einer angegebenen Position am nächsten liegt&quot; oder auf &quot;Benutzerdefinierte Startfunktion&quot; festgelegt ist

<b>Bestellmodus</b> *Integer* Die Methode zum Anordnen der generierten Pfade.\
Der Begrenzungsrahmen *der Pfade für die Position oder Größe* (Bbox) kann als Kriterium für die Anordnung der Pfade verwendet werden.\
Dies hat erhebliche Auswirkungen auf die Konvertierung der generierten <b>Pfade in Splines</b> mithilfe des dedizierten Knotens, da mehrere Spline-Knoten die Splines-Reihenfolge verwenden.\
*- Legacy (schnell):* Die in der vorherigen Version dieses Knotens verwendete Methode, die eine deutlich bessere Leistung bietet\
*- Nach B-Box-Mittelposition entlang der Richtung:* Die Pfade werden entsprechend der Position des Mittelpunkts ihres B-Boxes angeordnet, vom ersten zum letzten entlang der angegebenen Richtung\
*- Nach B-Box B-Box oben links entlang der Richtung:* Die Pfade werden entsprechend der Position der oberen linken Ecke ihres B-Boxes sortiert, von der ersten bis zur letzten entlang der angegebenen Richtung\
*- Nach Box-Größe - Größte bis kleinste:* Pfade werden entsprechend der Größe ihrer Bbox von der größten bis zur kleinsten angeordnet\
*- Nach Box-Größe - Kleinste bis größte:* Pfade werden entsprechend der Größe ihrer Bbox sortiert, von der kleinsten bis zur größten\
*- Benutzerdefinierte Ordnungsfunktion:* Verwenden Sie eine benutzerdefinierte Funktion, um Pfade zu sortieren.

<b>Ordnungsrichtung</b> *Gleitend* Der Winkel, der die Richtung beschreibt, in der die Pfade entlang dieser Richtung von der ersten bis zur letzten angeordnet werden.\
Der Wert ist eine *Anzahl der Windungen*, die zum Drehen eines X-Links-Richtungsvektors verwendet werden. Das bedeutet, dass 0 einen Richtungsvektor von (-1, 0) und 0,25 (90 Grad) einen Richtungsvektor von (0, 1) festlegt.

<b>Bestellfunktion</b> *Float* Die Funktion, die zum Ordnen der Pfade verwendet wird. Es gibt einen Float -Wert zurück.\
Pfade werden gemäß dem Wert dieser Funktion in *aufsteigender Reihenfolge* sortiert. Mit anderen Worten, das Ergebnis der Funktion für jeden Pfad ist die *Sortiertaste*, die zum Sortieren der Pfade verwendet wird.\
Verfügbare Variablen:
* bbox.center (Float2): Die Position der Mitte des Pfads bbox
* bbox.topleft (Float2): Die Position der linken oberen Ecke des Pfads bbox
* bbox.size (Float2): Die Größe des Pfadrahmens (X: width, Y: Height)

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-After.jpg" alt="MaskToPaths-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/MaskToPaths-Demo2.gif "Knotenbeispiel 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/MaskToPaths-Demo1.gif "Knotenbeispiel 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 3: Startmodi](../../../../../../assets/MaskToPaths-Demo3.gif "Knotenbeispiel 3: Startmodi"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 3: Bestellmodi](../../../../../../assets/MaskToPaths-Demo4.gif "Knotenbeispiel 3: Bestellmodi"){zoomable="yes"}

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/anisotropic-kuwahara-grayscale.html"
breadcrumb-title: ''
description: Verwenden Sie den Anisotropic Kuwahara-Graustufenfilter, um stilisierte, malerische Effekte mit Richtungsglättung zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Anisotropic Kuwahara Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Anisotropes Kuwahara-Graustufen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 0%

---


# Anisotropes Kuwahara-Graustufen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Anisotropes Kuwahara-Graustufen-Symbol](https://helpx.adobe.com/content/dam/substance-3d-designer/substance-graphs/nodes/filters/effects/anisotropic-kuwahara/AnisotropicKuwaharaGrayscale.png "Anisotropisches Kuwahara-Graustufen-Symbol"){width="200px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wendet eine anisotrope Richtungsunschärfe an, die den Bilddetails entspricht. Das Ergebnis ist ein Bild, das in Richtung der darin enthaltenen Formen als *Fluss* angezeigt wird.

Dieser anpassbare Weichzeichner berechnet oder empfängt eine *Richtungs-Map*, um diesen Fluss zu bestimmen, der in flachere, klarere Bereiche geschärft werden kann.

</td>
</tr>
</table>

Die Strömung kann auch durch Drehen der Weichzeichnungsrichtung unterbrochen werden. Ebenso kann eine benutzerdefinierte Richtungs-Map verwendet werden, um die aus dem Bild berechnete Version zu überschreiben.

Dieser Filter kann einen malerischen Effekt erzeugen und ist für die Stilisierung nützlich.

<b>Anisotropie</b>

Die Flussintensität wird hauptsächlich durch den Parameter [Anisotropie](#parameters) bestimmt, wie in der Abbildung unten gezeigt.

Links: Anisotropie 0.0 / Rechts: Anisotropie 1.0

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Eine Obstschale mit dem Kuwahara-Filter, aufgetragen mit 0 Anisotropien.](https://helpx.adobe.com/content/dam/substance-3d-designer/substance-graphs/nodes/filters/effects/anisotropic-kuwahara/anisotropic_kuwahara_gray_example_3_before.jpg){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Eine Obstschale mit dem Kuwahara-Filter, aufgetragen mit 0 Anisotropien.](https://helpx.adobe.com/content/dam/substance-3d-designer/substance-graphs/nodes/filters/effects/anisotropic-kuwahara/anisotropic_kuwahara_gray_example_3_after.jpg){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Parameter

</td>
</tr>
</table>

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen* <b>PRIMÄR</b> | Das Graustufenbild, das verarbeitet werden soll. |
| <b>Anisotropie-Winkelzuordnung</b> *Graustufen* | Das Graustufenbild, das die zusätzliche Drehung beschreibt, die auf die berechnete Richtung angewendet wird, wobei der Graustufenwert eine Anzahl von Windungen ist.   Die Map hat immer noch Auswirkungen, wenn der Parameter &#39;Anisotropie&#39; auf 0 gesetzt ist, da er die Rotation des Kernels beeinflusst, der vom Kuwahara-Filter verwendet wird. |
| <b>Steigungen-Map</b> *Graustufen* | Die Map, die die Steigungen darstellt, denen der Richtungs-Map gemäß dem Parameterwert &quot;Steigung Map Input Multiplier&quot; entspricht. |
| <b>Radiuszuordnung (optional)</b> *Graustufen* | Wenn die Verbindung hergestellt ist, wird der weichzeichnende &#39;Radius&#39; mit dem Eingabebild multipliziert. |
| <b>Richtungs-Map</b> *Farbe* | Die Karte, die die Richtung beschreibt, die vom anisotropen Filterkernel verwendet wird.   Die Map hat immer noch Auswirkungen, wenn der Parameter &#39;Anisotropie&#39; auf 0 gesetzt ist, da er die Rotation des Kernels beeinflusst, der vom Kuwahara-Filter verwendet wird.   Hinweis: Diese Eingabe wird nur verwendet, wenn der Parameter &quot;Richtungs-Map verwenden&quot; auf &quot;True&quot; festgelegt ist. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen* | Das Ergebnis der anisotropen Unschärfe, die der Knoten auf das Eingabebild angewendet hat. |
| <b>Richtungs-Map</b> *Farbe* | Die Richtungs-Map, die aus dem Eingabebild berechnet und zum Ansteuern der anisotropen Weichzeichnung verwendet wurde.   Wenn der Parameter &quot;Input Richtungs-Map verwenden&quot; auf &quot;True&quot; festgelegt ist, wird das für den Richtungs-Map-Eingang bereitgestellte Image verwendet und unverändert ausgegeben. |

## Parameter

|  |  |
| --- | --- |
| <b>Radius</b> *Gleitend* | Der Weichzeichnungsradius, wenn ein höherer Wert zu einem stärkeren Weichzeichnungseffekt führt.   Der Höchstwert ist 32. |
| <b>Smoothness</b> *Gleitend* | Passt den Grad der Farbüberblendung in die berechnete Richtung an.   Ist dieser Wert 0, werden die Farben meist in diese Richtung verschoben und es findet nur eine sehr geringe Füllmethode statt. |
| <b>Schärfe</b> *Gleitend* | Erhöht den Kontrast in den unscharfen Bereichen und sorgt dafür, dass sie flacher und klarer definiert aussehen. |
| <b>Anisotropie</b> *Gleitend* | Passt den Beitrag des Richtungs-Map bei der Weichzeichnung an.   Die Richtungs-Map und alle ihre Modifizierer (sowohl Parameter als auch Eingabemaps) haben weiterhin eine Wirkung, wenn dieser Parameterwert 0 ist, da die Richtungs-Map im Kuwahara-Filterkernel verwendet wird. |
| <b>Richtungs-Map verwenden</b> *Boolescher Wert* | Wenn &#39;True&#39;, wird keine Richtungs-Map aus dem Eingabebild berechnet, und das mit dem &#39;Richtungs-Map&#39;-Eingang verbundene Bild wird stattdessen verwendet, um die anisotrope Weichzeichnung zu steuern. |
| <b>Smoothness testen</b> *Float* *Verfügbar, wenn &quot;Eingabe-Richtungs-Map verwenden&quot; auf &quot;Falsch&quot; festgelegt ist* | Passt die Intensität der Weichzeichnung an, die auf die aus dem Bild berechneten und auf der Richtungs-Map gespeicherten Richtungen angewendet wird.   Eine Erhöhung dieses Werts sorgt für ein glatteres Ergebnis, wenn das Bild viele hochfrequente Details enthält. |
| <b>Winkel der Anisotropie</b> *Float* *Verfügbar, wenn &quot;Eingabe-Richtungs-Map verwenden&quot; auf &quot;Falsch&quot; festgelegt ist* | Fügt dem Richtungs-Map eine Drehung in der Anzahl der Umdrehungen hinzu.   Diese zusätzliche Drehung ist *kumulativ* mit der durch die Eingabe &quot;Anisotropie Angle Map&quot; angegebenen Drehung. |
| <b>Multiplikator der Winkelzuordnung der Anisotropie</b> *Float* *Verfügbar, wenn &quot;Eingabe-Richtungs-Map verwenden&quot; auf &quot;Falsch&quot; festgelegt ist* | Passt die Intensität der Werte in der Eingabe &quot;Drehwinkelkarte&quot; an, die dann über der auf den Richtungs-Map angewendeten Anisotropie in der Anzahl der Windungen hinzugefügt werden.   Diese zusätzliche Drehung ist *kumulativ* mit der durch den Parameter &#39;Winkel der Anisotropie&#39; angegebenen Drehung. |
| <b>Multiplikator für die Steigungen-Zuordnungseingabe</b> *Float* *Verfügbar, wenn &quot;Eingabe-Richtungs-Map verwenden&quot; auf &quot;Falsch&quot; festgelegt ist* | Passt die Intensität an, mit der der Richtungs-Map an die Steigungen angepasst wird, die durch den Eingang &quot;Steigung Map&quot; bereitgestellt werden. |

## Beispiele

<table>
  <tr>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_gray_example_1_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_gray_example_1_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_gray_example_2_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_gray_example_2_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_gray_example_4_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_gray_example_4_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

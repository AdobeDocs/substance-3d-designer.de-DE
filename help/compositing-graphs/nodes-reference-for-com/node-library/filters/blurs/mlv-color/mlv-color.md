---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: Verwenden Sie den MLV-Farbunschärfefilter, um Bewegungsunschärfeeffekte auf Farbstrukturen anzuwenden und dynamische visuelle Looks zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MLV-Farbe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# MLV-Farbe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLV-Farbe: Symbol &#x200B;](../../../../../../assets/MLV_Color_Icon.png "MLV-Farbe: Symbol ")

<b>In:</b> Filters > Blurs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

MLV steht für <b>&#39;Mittel der geringsten Abweichung&#39;</b>. Dieser Filter optimiert Kanten und glättet Bildrauschen.

Der Filter findet strukturierende Bereiche in einem Bild und verwendet sie sowohl zum Scharfzeichnen als auch zum Reduzieren. Dies kann in manchen Fällen zu Stufen entlang von Gradienten führen, die breiter als die Strukturierungsbereiche sind.

</td>
</tr>
</table>

>[!NOTE]
>
> Siehe auch [MLV-Graustufen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-grayscale/mlv-grayscale.md).

## Eingangsanschlüsse

<b>Eingabe </b>*Farbe* Das Farbbild, das verarbeitet werden soll.

## Ausgangsanschlüsse

<b>Ausgabe</b> *Farbe* Das gefilterte Farbbild.

## Parameter

<b>Intensität</b> *Gleitend* Die Stärke der auf das Bild angewendeten Filterung.\
Höhere Werte führen zu einer stärkeren Glättung von Details und Rauschen in flachere Bereiche.

<b>Smoothness</b> *Float* Die Intensität der Glättung, die auf die strukturierenden Bereiche angewendet wird, was zu runderen Bereichen führt und den Schritteffekt verringert, der bei höheren Filterintensitäten auftreten kann.

<b>Kriterium</b> *Integer* Das Kriterium, das zum Auswählen der Werte verwendet wird, die die Strukturierungsbereiche im Bild definieren.\
Mit anderen Worten, wie Pixel *in Bereiche gruppiert* werden sollen, die geglättet werden sollen.\
*- Varianz:* Wählen Sie Werte mit der niedrigsten Streuung um den Mittelwert aus, was zu Clustern von Pixeln führt, die einander ähnlich sind\
*- Variationskoeffizient:* Wählen Sie Werte unter Berücksichtigung des Mittelwerts aus, was umgekehrt zu weniger Variationen in helleren Bereichen führt

<b>Gaußsch</b> *Boolesch* Verwenden Sie eine Gaußsche Verteilung zum Gruppieren von Pixeln in strukturierenden Bereichen.\
Bei &quot;True&quot; werden glattere Bereiche und ein reduzierter Abflachungseffekt erzeugt.

<b>Alpha betreffen</b> *Boolean* Wenn &quot;True&quot; festgelegt ist, wird die Filterung auch auf den Alphakanal des Bildes angewendet.\
Wenn &quot;False&quot; festgelegt ist, wird der Alphakanal vollständig ignoriert und in der Ausgabe unverändert gelassen.

<b>Iterationen</b> *Integer* Die Anzahl der Filterausführungen, wobei jede Iteration auf das Ergebnis des vorherigen angewendet wird.\
Mehr Iterationen führen zu flacheren und schärferen Strukturierungsbereichen.

## Beispiele

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant4A.png" alt="MLV_Variant4A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant4B.png" alt="MLV_Variant4B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant5A.png" alt="MLV_Variant5A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant5B.png" alt="MLV_Variant5B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant3A.png" alt="MLV_Variant3A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant3B.png" alt="MLV_Variant3B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

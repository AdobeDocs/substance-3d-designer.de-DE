---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
breadcrumb-title: ''
description: Verwenden Sie den MLV-Graustufen-Weichzeichnungsfilter, um Bewegungsunschärfeeffekte auf Graustufen-Texturen anzuwenden und dynamische Looks zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MLV-Graustufen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# MLV-Graustufen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLV-Graustufen: Symbol ](../../../../../../assets/MLV_Grayscale_Icon.png "MLV-Graustufen: Symbol ")

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
> Siehe auch [MLV-Farbe](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-color/mlv-color.md).

## Eingangsanschlüsse

<b>Eingabe </b>*Graustufen* Das Graustufenbild, das verarbeitet werden soll.

## Ausgangsanschlüsse

<b>Ausgabe </b>*Graustufen* Das gefilterte Graustufenbild.

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

<b>Iterationen</b> *Integer* Die Anzahl der Filterausführungen, wobei jede Iteration auf das Ergebnis des vorherigen angewendet wird.\
Mehr Iterationen führen zu flacheren und schärferen Strukturierungsbereichen.

## Beispiele

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant1A.png" alt="MLV_Variant1A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant1B.png" alt="MLV_Variant1B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2B.png" alt="MLV_Variant2B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2C.png" alt="MLV_Variant2C">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

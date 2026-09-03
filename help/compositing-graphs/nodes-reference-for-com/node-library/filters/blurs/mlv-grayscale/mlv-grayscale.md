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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# MLV-Graustufen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLV-Graustufen: Symbol ](mlv-grayscale.resources/mlv-grayscale-01.png "MLV-Graustufen: Symbol ")

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

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen</i> | Das Graustufenbild, das verarbeitet werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das gefilterte Graustufenbild. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> *Gleitend* | Die Stärke der Filterung, die auf das Bild angewendet wurde.<br><br>Höhere Werte führen zu einer stärkeren Glättung von Details und zum Rauschen in flachere Bereiche. |
| <b>Smoothness</b> *Gleitend* | Die Intensität der auf die Strukturierungsflächen aufgebrachten Glättung, die zu runderen Flächen führt und die bei höheren Filterungen auftreten kann, vermindert. |
| <b>Kriterium</b> *Integer* | Das Kriterium zur Auswahl der Werte, die die Strukturierungsbereiche im Bild definieren.<br><br>Mit anderen Worten, wie Pixel *gruppiert* werden sollten in Bereiche, die geglättet werden sollen.<br><br>*- Varianz:* Wählen Sie Werte mit der niedrigsten Streuung um den Mittelwert aus, was zu Clustern von Pixeln führt, die einander ähnlich sind <br>*- Variationskoeffizient:* Wählen Sie Werte aus, während Sie den Mittelwert berücksichtigen, was umgekehrt zu weniger Variationen in helleren Bereichen führt |
| <b>Gaußsch</b> *Boolescher Wert* | Verwenden Sie eine Gaußsche Verteilung zum Gruppieren von Pixeln in strukturierende Bereiche.<br><br>Wenn &quot;True&quot; festgelegt ist, führt dies zu glatteren Bereichen und einem reduzierten Abflachungseffekt. |
| <b>Iterationen</b> *Integer* | Gibt an, wie oft der Filter ausgeführt wird, wobei jede Iteration auf das Ergebnis der vorherigen angewendet wird.<br><br>Mehr Iterationen führen zu flacheren und schärferen Strukturierungsbereichen. |

## Beispiele

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-02.png" alt="MLV_Variant1A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-03.png" alt="MLV_Variant1B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-04.png" alt="MLV_Variant2A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-05.png" alt="MLV_Variant2B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-04.png" alt="MLV_Variant2A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-06.png" alt="MLV_Variant2C">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

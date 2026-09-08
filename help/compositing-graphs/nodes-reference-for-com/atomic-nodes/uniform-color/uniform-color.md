---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Einheitliche Farbe", um Texturen für die einheitliche Farbe zum Erstellen von Farbflächen und Basisebenen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gleichmäßige Farbe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 8%

---


# Gleichmäßige Farbe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elementare Knoten: Einheitliche Farbe](../../../../assets/comp_uniform_1.png "Elementare Knoten: Einheitliche Farbe"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Generiert einen Flächengraustufen- oder -farbwert.

Es handelt sich um einen einfachen Knoten, der sehr häufig als Ausgangspunkt zum Hinzufügen von Farben oder zum Erstellen bestimmter Werte verwendet wird.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> Leistungsoptimierung
> 
> Beide Anpassungen reduzieren die Berechnung und den Speicherbedarf des Knotens:
> 
> * Wenn ein Graustufenwert benötigt wird, stellen Sie sicher, dass Sie den [Farbmodus](#parameters) des Knotens in &#39;Graustufen&#39; ändern.
> * Da die Ausgabe des Knotens eine flache Farbe ist, können Sie die niedrigste mögliche Auflösung verwenden. Legen Sie den Parameter &quot;[Ausgabegröße](../../../../compositing-graphs/output-size/output-size.md)&quot; des Knotens so fest, dass die Absolute [Vererbung-Methode &#x200B;](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) und eine Auflösung von 16x16 Pixel verwendet werden.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parameter

</td>
<td style="border: 0;" valign="top">

### Ausgabe-Verbindungen

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolesche Wert* | Schaltet zwischen einem Graustufen- und einem Farbausgabebild um. |
| <b>Ausgabefarbe</b> *Fließkommazahl/Fließkommazahl4* | Wählt die einheitliche Farbe aus, die im Ausgabebild verwendet werden soll.   Bei Verwendung des Farbmodus &quot;Farbe&quot; wird der Alphakanal für die Deckkraft verwendet, wobei 0 vollständig transparent und 1 vollständig deckend ist. |

## Ausgabe-Verbindungen

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Farbe/Graustufen* |  |

## Beispiele

*Demnächst verfügbar.*

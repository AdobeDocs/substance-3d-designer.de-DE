---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten "Gleichmäßige Farbe", um einheitliche Farbstrukturen für die Erstellung von Farbflächen und Basisebenen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gleichmäßige Farbe
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 7%
---

# Gleichmäßige Farbe

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Atomknoten: Einheitliche Farbe](uniform-color.resources/comp_uniform_1.png "Atomarer Knoten: Einheitliche Farbe"){width="100%"}

<b>In:</b> Atomknoten

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Generiert einen Flächengraustufen- oder -farbwert.

Es handelt sich um einen einfachen Knoten, der sehr häufig als Ausgangspunkt zum Hinzufügen von Farben oder zum Erstellen bestimmter Werte verwendet wird.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="uniform-color.resources/uniform-color-tooltip.gif" alt="Uniform-Color-QuickInfo" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>



>[!TIP]
>
> Leistungsoptimierung
> 
> Beide Anpassungen reduzieren die Rechenzeit und den Speicherbedarf des Knotens:
> 
> * Wenn ein Graustufenwert benötigt wird, stellen Sie sicher, dass Sie den [Farbmodus](#parameters) des Knotens in &#39;Graustufen&#39; ändern.
> * Da die Ausgabe des Knotens eine flache Farbe ist, können Sie die niedrigste mögliche Auflösung verwenden. Legen Sie den Parameter &quot;[Ausgabegröße](../../../../compositing-graphs/output-size/output-size.md)&quot; des Knotens so fest, dass die &quot;Absolute&quot; [Vererbungsmethode ](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) und eine Auflösung von 16x16 Pixeln verwendet werden.


## Parameter

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolescher Wert* | Schaltet zwischen einem Graustufen- und einem Farbausgabebild um. |
| <b>Ausgabefarbe</b> *Gleitend/Gleitend4* | Wählt die einheitliche Farbe aus, die im Ausgabebild verwendet werden soll.   Bei Verwendung des Farbmodus &quot;Alpha&quot; wird der Farbkanal für die Deckkraft verwendet, wobei 0 vollständig transparent und 1 vollständig deckend ist. |


## Beispiele

*Demnächst verfügbar.*

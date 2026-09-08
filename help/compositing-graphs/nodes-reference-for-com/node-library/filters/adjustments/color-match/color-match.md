---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: Mit dem Knoten "Farbabgleich" können Sie die Farben zwischen Texturen abgleichen, um konsistente Farbpaletten zu erstellen und Texturen zu harmonisieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbabgleich
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# Farbabgleich

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Versucht, den definierten Bereich &quot;*Quellfarbe*&quot; mit einem Bereich &quot;*Zielfarbe*&quot; abzugleichen, mit Unterstützung für Eingabefächer zum Definieren von Quelle und Ziel.

Einfachere Versionen finden Sie unter [Farbbereich ersetzen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) oder [Farbe ersetzen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Farbeingabe</i> | Haupteingabe zum Ändern des Ergebnisses. |
| <b>Quellfarbe</b> <i>Farbeingabe</i> | Eingabeschacht für Quellfarbe, wird nur verwendet, wenn der Quellfarbmodus auf *Eingabe* festgelegt ist. |
| <b>Zielfarbe</b> <i>Farbeingabe</i> | Eingabebereich für Zielfarbe, wird nur verwendet, wenn &quot;Zielfarbmodus&quot; auf *Eingabe* festgelegt ist. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Quellfarbmodus</b> <i>Durchschnitt, Parameter, Eingabe</i> | Legt fest, ob die Quellfarbe durch Mittelwertbildung des Eingabebilds, Parametereinstellung oder Verwendung eines Eingangssteckplatzes definiert wird. |
| <b>Quellfarbe</b> <i>(Farbwert)</i> | Wenn der Quellfarbmodus auf *Parameter* festgelegt ist, bestimmt dieser Parameter die Quellfarbe. |
| <b>Zielfarbmodus</b> <i>Parameter, Bildeingabe</i> | Legt fest, ob die Quellfarbe durch Mittelwertbildung des Eingabebilds, Parametereinstellung oder Verwendung eines Eingangssteckplatzes definiert wird. |
| <b>Zielfarbe</b> <i>(Farbwert)</i> | Wenn der Zielfarbmodus auf *Parameter* festgelegt ist, bestimmt dieser Parameter die Zielfarbe. |
| <b>Benutzerdefinierte Farbvariation</b> <i>False/True</i> | Aktiviert eine zusätzliche Farbvariation. |
| <b>Farbvariation</b> | Legt Farbton-, Chrominanz- oder Luminanzvarianten auf das Ergebnis fest, wenn diese Option aktiviert ist. |
| <b>Maske verwenden</b> <i>False/True</i> | Schaltet die Verwendung von &quot;Maskeneingabe&quot; oder &quot;Ausgabe&quot; je nach dem unten stehenden Maskenmodus um. |
| <b>Maskenmodus</b> <i>Parameter, Eingabe</i> | Im Parametermodus wird eine Maske ausgegeben, in der detailliert angegeben ist, wie die Farbe geändert wurde. Im Eingabemodus kann eine Maske die Stärke des Effekts &quot;Farbabgleich&quot; steuern. |
| <b>Maske</b> | Gibt eine Maske aus, die anzeigt, wo genau der Effekt &quot;Farbabgleich&quot; angewendet wurde, mit zusätzlichen Steuerelementen zum Glätten und Weichzeichnen der resultierenden Maske. |

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# Farbabgleich

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

## Farbabgleich

**In:** *Filter/Korrekturen*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Versucht, den definierten Bereich &quot;*Quellfarbe*&quot; mit einem Bereich &quot;*Zielfarbe*&quot; abzugleichen, mit Unterstützung für Eingabefächer zum Definieren von Quelle und Ziel.

Einfachere Versionen finden Sie unter [Farbbereich ersetzen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) oder [Farbe ersetzen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md).

## Parameter

### Eingaben

* **Eingabe**: *Color*-Eingabe\
  Haupteingabe zum Ändern des Ergebnisses.
* **Quellfarbe**: *Farbeingabe*\
  Eingabeschacht für Quellfarbe, wird nur verwendet, wenn der Quellfarbmodus auf *Eingabe* festgelegt ist.
* **Zielfarbe**: *Farbeingabe* Eingabeschacht für Zielfarbe, wird nur verwendet, wenn &quot;Zielfarbmodus&quot; auf *Eingabe* festgelegt ist.

### Parameter

* **Quellfarbmodus**: *Durchschnitt, Parameter, Eingabe* Legt fest, ob die Quellfarbe durch Mittelwertbildung des Eingabebildes, durch Festlegen eines Parameters oder durch Verwendung eines Eingabefelds definiert wird.
* **Quellfarbe**: *(Farbwert)* Wenn der Quellfarbmodus auf *Parameter* festgelegt ist, bestimmt dieser Parameter die Quellfarbe.
* **Zielfarbmodus**: *Parameter, Bildeingabe* Legt fest, ob die Quellfarbe durch Mittelwertbildung des Eingabebildes, durch Festlegen eines Parameters oder durch Verwendung eines Eingabefelds definiert wird.
* **Zielfarbe**: *(Farbwert)* Wenn der Zielfarbmodus auf *Parameter* festgelegt ist, bestimmt dieser Parameter die Zielfarbe.
* **Benutzerdefinierte Farbvariation**: False/True\
  Aktiviert eine zusätzliche Farbvariation.
* **Farbvariation**\
  Legt Farbton-, Chrominanz- oder Luminanzvarianten auf das Ergebnis fest, wenn diese Option aktiviert ist.
* **Maske verwenden**: *False/True*\
  Schaltet die Verwendung von &quot;Maskeneingabe&quot; oder &quot;Ausgabe&quot; je nach dem unten stehenden Maskenmodus um.
* **Maskenmodus**: *Parameter, Eingabe* Parametermodus gibt eine Maske aus, in der detailliert angegeben ist, wie die Farbe geändert wurde. Im Eingabemodus kann eine Maske die Stärke des Effekts &quot;Farbabgleich&quot; steuern.
* **Maske**\
  Gibt eine Maske aus, die anzeigt, wo genau der Effekt &quot;Farbabgleich&quot; angewendet wurde, mit zusätzlichen Steuerelementen zum Glätten und Weichzeichnen der resultierenden Maske.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

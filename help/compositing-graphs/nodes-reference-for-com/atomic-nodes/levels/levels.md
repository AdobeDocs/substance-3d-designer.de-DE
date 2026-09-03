---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/levels.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Tonwertkorrektur", um Helligkeit, Kontrast und Farbtonbereich von Texturen für Farbkorrekturen und Verbesserungen anzupassen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Levels
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tonwertkorrektur
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 4%

---


# Tonwertkorrektur

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Ebenen](levels.resources/levels-01.png "Atomknoten: Stufen"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Passt den globalen Farbtonbereich und die Farbbalance der Tiefen, Mitteltöne und Lichter eines Bildes an.

Mit dem Knoten &quot;Tonwertkorrektur&quot; können Sie die Tonwerte einer Eingabe neu zuordnen, indem Sie die Eingabe- und Ausgabe-Umstellungsfaktoren festlegen, die in einer Histogrammschnittstelle dargestellt werden, die von anderen 2D-Bildeditoren gewohnt ist.

</td>
</tr>
</table>

Er ist einer der wichtigsten und hilfreichsten Knoten in Substance 3D Designer und wird sehr oft verwendet, um Werte in einem Diagramm neu zuzuordnen und anzupassen, da er die präziseste und genaueste Schnittstelle für sich ändernde Werte bietet.

Obwohl es sich um einen wichtigen Knoten handelt, kann die Schnittstelle in einigen Anwendungsfällen etwas umständlich sein. Überprüfen Sie daher [Auto Levels](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md), [Kontrast/Luminanz](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md) und [Histogramm Scan](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) auf Alternativen.

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

## Beispiele

## Parameter

Der Knoten bietet zwei Schnittstellen zur Anpassung seiner Werte: Histogramm und Schieberegler. Sie können zwischen ihnen mit der rechten Schaltfläche in der Kopfzeile &quot;Spezifische Parameter&quot; wechseln:

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Die hervorgehobene gelbe Schaltfläche schaltet die Schnittstelle zwischen den Schiebereglern für den Histogrammwert (oben) um (unten)

</td>
<td width="66.67%" style="border: 0;" valign="top">

![](levels.resources/levels-02.png)

![](levels.resources/levels-03.png)

</td>
</tr>
</table>

|  |  |
| --- | --- |
| <b>Ebene niedrig</b> *Gleitend/Gleitend4* | Definiert die niedrigen Lichtpegel des Eingabebilds. Ordnet die eingegebenen niedrigen Werte neu zu, um vollständig schwarz zu werden. |
| <b>Ebene hoch</b> *Gleitend/Gleitend4* | Definiert die Lichtebenen des Eingabebilds.  Ordnet die eingegebenen hohen Werte neu zu, um vollständig weiß zu werden. |
| <b>Ebene in der Mitte</b> *Gleitend/Gleitend4* | Definiert die Mitteltöne des Eingabebildes.  Ordnet die eingegebenen Mittelwerte neu zu, sodass sie mittelgrau sind. |
| <b>Ebene niedrig</b> *Gleitend/Gleitend4* | Definiert die niedrigen Helligkeitsstufen des Ausgabebilds.  Klammert die Ausgabewerte für Schwarz, um den Grenzwert festzulegen. |
| <b>Ebene hoch</b> *Gleitend/Gleitend4* | Definiert die Markierungsstufen des Ausgabebilds.  Beschränkt die Ausgabe Weißwerte, um Limit festzulegen. |
| <b>Zwischenklemme</b> *Boolescher Wert* | Bestimmt, ob der transformieren Eingangswert vor der Berechnung des Ausgangspegels auf [0, 1] geklemmt wird. |

## Benutzerhandbuch

Sehen Sie sich diese Videoübersicht über den Knoten &quot;Ebenen&quot; und seinen Histogramm-Editor an:

### Schnellaktionen

In der Kopfzeile &quot;Spezifische Parameter&quot; finden Sie Schaltflächen, mit denen Sie auf praktische Funktionen des Histogramms zugreifen können:

![Schnellzugriffe für Knoten auf Ebenen](levels.resources/levels-04.png "Schnellzugriffe für Knoten auf Ebenen")

<b>1 - Umkehren:</b> Tauscht die Werte der Parameter &quot;Level out low&quot; und &quot;Lichter in Ausgabebild&quot; aus.

<b>2 - Automatischer Pegel:</b> Passt die Werte der Parameter &quot;Tiefen in Eingabebild&quot; und &quot;Lichter in Eingabebild&quot; automatisch an den niedrigsten bzw. höchsten im Bild vorhandenen Wert an.

<b>3 - Schnittstellen wechseln:</b> Schaltet zwischen dem Histogramm- und dem Schiebereglereditor um.

### Histogramm

Der Histogramm-Editor ist für visuelle, schnelle Anpassungen gedacht, bei denen präzise Werte nicht wirklich benötigt werden und der leg von Parametern nicht von Bedeutung ist. Dies ist in der Regel der schnellste und einfachste Weg, mit Tonwertkorrektur zu arbeiten.

![](levels.resources/levels-05.gif)

Abhängig vom Eingabetyp (Farbe oder Graustufen) können Sie in der Dropdown-Liste über dem Histogramm auswählen, welchen Kanal Sie ändern möchten.

### Schieberegler

Der Schieberegler-Editor verzichtet auf jeden visuellen Editor und stellt nur numerische Schieberegler bereit, was vor allem nützlich ist, wenn Sie auf sehr exakte Werte klammern oder zuordnen möchten oder wenn Sie beabsichtigen, einen dieser Parameter [legen](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), da dies nur im Schieberegler-Editor möglich ist.

Die Schieberegler ändern sich je nach Farb- oder Graustufeneingabe: Farbeingaben erzeugen vier Regler für jeden RGBA-Kanal. Graustufen verfügt nur über einen Regler, was die Arbeit erleichtert. Eine Erklärung zu jedem Regler finden Sie oben in der Parameterliste.

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen/Farbe* PRIMÄR | Das zu verarbeitende Bild. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

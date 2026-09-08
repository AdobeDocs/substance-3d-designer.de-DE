---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/mask-builder.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Maskenbildner", um mehrere Maskeneingaben zu kombinieren und komplexe Maskenmuster für Material-Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Mask Builder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maskenbildner
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 10%

---


# Maskenbildner

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/mask-builder.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Das ist so ziemlich die Designer-Version von Painters Mask Builder.

Es ist ein kompliziertes Tool, das als allumfassender Maskenbildner gedacht ist, der auf durch Baking erzeugte Map, Benutzerparametern und Schmutz-Mustern und -Maps basiert. Es ist vor allem als ein sehr fortgeschrittener, voller Kontrolle Knoten in Falten Dirt und Kantenverschleiß zu mischen. Dieser Knoten ist leistungsstark genug, um jeden anderen Maskengenerator nachzuahmen.

Es sind keine expliziten Baking führte erforderlich, aber je mehr Sie angeben, desto mehr kann dieser Knoten tun.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> |  |
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> |  |
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> |  |
| <b>Schmutz-Eingabe</b> <i>Graustufen-Eingabe</i> |  |
| <b>Schmutz-Eingang 2</b> <i>Graustufen-Eingabe</i> |  |
| <b>Streuung-Eingabe</b> <i>Graustufen-Eingabe</i> | Benutzerdefinierter Streuung-Stempel, der erforderlich ist, um die Parameter für die Streuung zu verwenden. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |
| <b>Position</b> <i>Farbeingabe</i> | Wird für Triplanar- und Top-Bottom-Effekte verwendet. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ebene</b> <i>0.0 - 1.0</i> | Legt die Gesamtstärke des Effekts fest, die nach und nach zum Vorschein kommt. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. |
| <b>Umkehren</b> <i>False/True</i> | Kehrt das Ergebnis um. Nützlich, um das Gegenteil der Maske zu erreichen, die Sie erstellen. |
| <b>Triplanar verwenden</b> <i>False/True</i> | Ermöglicht die Triplanare Projektion und vermeidet Nähte mit Schmutz-Maps. |
| <b>Triplanarer Mischkontrast</b> <i>0.0 - 1.0</i> | Legt den Kontrast für die Triplanar-Überblendung fest. |
| <b>Schmutz</b> <i>0.0 - 1.0</i> | Legt die Menge an Schmutz fest, die global gemischt wird. |
| <b>Schmutz</b> |  |
| <b>Skalierung</b> <i>0 - 10</i> | Legt die Größe des globalen Schmutzes fest. |
| <b>Benutzerdefinierten Schmutz verwenden</b> <i>False/True</i> | Aktiviert die benutzerdefinierte Schmutz-Eingabe. |
| <b>Sekundärer benutzerdefinierter Schmutz</b> <i>0.0 - 1.0</i> | Aktiviert einen zweiten benutzerdefinierten Schmutz. |
| <b>Umkehren</b> <i>False/True</i> | Kehrt den Schmutz um. |
| <b>AO</b> <i>-1.0 - 1.0</i> | Legt fest, inwieweit der Effekt in verdeckten AO-Bereichen auftreten soll. Kann mit der folgenden Gruppe optimiert werden. |
| <b>AO</b> |  |
| <b>Bereich</b> <i>0.0 - 1.0</i> | Legt den Schwellenwert oder Bereich für das Erscheinungsbild von Dirt fest. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des AO-Effekts an. |
| <b>Rauschen</b> <i>0.0 - 1.0</i> | Legt die Menge an Rauschen/Schmutz fest, die in den AO-Effekt integriert werden soll. |
| <b>Rauschen-Skalierung</b> <i>0 - 10</i> | Legt die Skalierung des AO-Rauschen/Schmutz fest. |
| <b>Rauschen-Typ</b> <i>Flecken, Wolke, Feuchtigkeit, weißer Rauschen</i> | Wechselt zwischen 4 verschiedenen AO-Rauschen-Typen. |
| <b>Umkehren</b> <i>False/True</i> | Kehrt die Interpretation der AO-Map um: Rauschen wird in hellen AO-Bereichen angezeigt, in dunklen nicht. |
| <b>Krümmung</b> <i>0.0 - 1.0</i> | Legt fest, wie viel Effekt an den Kanten der Krümmung angewendet werden soll. kann sowohl konvex als auch konkav sein. Optimiere dies mit der Gruppe unten. |
| <b>Krümmung</b> |  |
| <b>Konvexbereich</b> <i>-1.0 - 1.0</i> | Legt fest, wie stark der Effekt an den Kanten der konvexen (hellen) Krümmung angewendet wird. |
| <b>Konvexkontrast</b> <i>0.0 - 1.0</i> | Legt den Kontrast des Effekts &quot;Konvex&quot; fest. |
| <b>Konvex invertieren</b> <i>False/True</i> | Kehrt die Interpretation der konvexen Kanten um. |
| <b>Konkaver Bereich</b> <i>-1.0 - 1.0</i> | Legt fest, wie stark der Effekt an Kanten konkaver (dunkler) Krümmungen angewendet wird. |
| <b>Konkaver Kontrast</b> <i>0.0 - 1.0</i> | Legt den Kontrast des konkaven Bereichs fest. |
| <b>Konkave Umkehr</b> <i>False/True</i> | Kehrt die Interpretation der konkaven Kanten um. |
| <b>Smoothness</b> <i>0.0 - 16.0</i> | Weichzeichnungs- und Glättungsbetrag, der auf Kanten der Krümmung angewendet werden soll. |
| <b>Leistungssteigerung</b> <i>0.0 - 1.0</i> | Zusätzlicher Booster, wenn der Effekt nicht sichtbar genug ist. |
| <b>Rauschen</b> <i>0.0 - 1.0</i> | Legt den Einfluss des Rauschen/Schmutz auf den Effekt &quot;Krümmung&quot; fest. |
| <b>Rauschen-Skalierung</b> <i>0 - 10</i> | Legt die Skalierung der Rauschen fest. |
| <b>Rauschen-Typ</b> <i>Flecken, Wolke, Feuchtigkeit, weißer Rauschen</i> | Wählen Sie zwischen 4 verschiedenen Rauschen-Typen. |
| <b>Verlauf oben/unten</b> <i>-1.0 - 1.0</i> | Überblendungen oder Masken mit einem von oben nach unten verlaufenden Verlauf, der auf der Positionsmap basiert. Positive Werte machen die Dinge heller, negative Werte maskieren vorhandene Effekte. |
| <b>Verlauf</b> |  |
| <b>Bereich</b> <i>0.0 - 1.0</i> | Legt die Position des Verlaufs fest. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Verlaufs an. |
| <b>Umkehren</b> <i>False/True</i> | Kehrt den Verlauf um. Tauscht unten und oben aus. |
| <b>Normaler Weltraum</b> <i>0.0 - 1.0</i> | Ähnlich wie &quot;Verlauf oben/unten&quot;, jedoch mit der Positionskarte und in sechs Richtungen, ähnlich wie bei einer gefälschten Beleuchtung. Positive Werte werden aufgehellt, negative Werte werden abgedunkelt. |
| <b>Normaler Weltraum</b> |  |
| <b>Höchste Intensität</b> <i>-1.0 - 1.0</i> |  |
| <b>Tiefe unten</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensität vorne</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensität zurücksetzen</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensität rechts</b> <i>-1.0 - 1.0</i> |  |
| <b>Linke Intensität</b> <i>-1.0 - 1.0</i> |  |
| <b>Scratches</b> <i>-1.0 - 1.0</i> | Überblendung kratzt sich in den weißen Bereichen. |
| <b>Scratches</b> |  |
| <b>Betrag</b> <i>0 - 4096</i> | Legt die Gesamtzahl der Kratzer fest. |
| <b>Skalierung</b> <i>0.0 - 1.0</i> | Legt die Skalierung einzelner Arbeitsschritte fest. |
| <b>Streuung</b> <i>-1.0 - 1.0</i> | Streuung eines benutzerdefinierten Stempels in weißen Bereichen. |
| <b>Streuung</b> |  |
| <b>Skalierung</b> <i>0 - 50</i> | Gesamtumfang des Effekts. |
| <b>Dichte</b> <i>0.0 - 1.0</i> | Streuungsdichtesteuerung, Zahl, die angezeigt werden sollte. |
| <b>Größe</b> <i>0.0 - 4.0</i> | Größe des Streustempels. |
| <b>Größenänderung</b> <i>0.0 - 1.0</i> | Variation innerhalb der Stempelgröße. |
| <b>Deckkraftvariation</b> <i>0.0 - 1.0</i> | Variation innerhalb der Stempeldeckkraft. |

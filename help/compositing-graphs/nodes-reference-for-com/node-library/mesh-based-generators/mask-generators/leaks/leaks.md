---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Lecks", um Leckmuster basierend auf der Geometrie des Meshs zu generieren, um Wasserflecken und Flüssigkeitseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lecks
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# Lecks

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leaks.resources/leaks.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Dieser Knoten stellt undichte Streifen von Dirt und Schmutz dar, die von scharfen Kanten stammen. Da Streifen mit Baking geführt Lage erzeugt werden, laufen sie immer nach unten.

Stellen Sie sicher, dass Sie die Variationsmaske ändern: Da sie die Platzierung von Streifen vorantreibt, kann sie einen viel größeren Einfluss haben als bei anderen Maskengeneratoren.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Position</b> <i>Graustufen-Eingabe</i> | Baking geführt Lageplan, verwendet für Streakrichtungen. Erforderlich! |
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für die Platzierung von Streifen. Erforderlich! |
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. Empfohlen, aber Sie können stattdessen flaches Weiß verwenden. |
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> | Baking geführt Normalmap des Welt-Raums, verwendet für die Streifenrichtung. Erforderlich! |
| <b>Variationsmaske</b> <i>Graustufen-Eingabe</i> | Optionale Variationsmaske, aktivieren Sie diese Option, indem Sie die Überschreibung auf &quot;True&quot; setzen. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ebene</b> <i>0.0 - 1.0</i> | Gesamtwert des Ergebnisses. Blendet den Effekt schrittweise ein und beeinflusst auch die Länge. Sollte ziemlich hoch eingestellt werden, um lange Tropfen zu erhalten. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. |
| <b>Variation</b> <i>0.0 - 1.0</i> | Legt die Stärke der großformatigen Variation fest, die zum Maskieren der Streifen verwendet wird. Wenn Sie diesen Wert auf 0 setzen, werden vollständig gleichmäßige Streifen erzeugt, also vermeiden Sie dies. |
| <b>Länge</b> <i>0.0 - 8.0</i> | Länge der Streifen tropft. Wenn dieser Wert in kleinem Maßstab zu hoch eingestellt wird, führt dies zu einer sichtbaren Schrittweite. Experimentiere auch mit dem Level. |
| <b>Schließen</b> <i>X, Y, Z, Ohne</i> | Legt fest, welche Richtung der AO-Effekt haben soll. |
| <b>Variationsmaske überschreiben</b> <i>False/True</i> | Ermöglicht das Überschreiben der Variationsmaske mit einem benutzerdefinierten Eingabebereich. Die Verwendung von Masken mit geringerer Dichte kann interessant sein und ist eine gute Möglichkeit, die Tropfenbildung zu steuern. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leaks.resources/leaks-ex.gif" />
        </td>
    </tr>
</table>

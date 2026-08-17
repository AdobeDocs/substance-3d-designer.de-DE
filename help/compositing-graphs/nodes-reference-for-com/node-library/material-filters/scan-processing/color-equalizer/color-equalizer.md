---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Color Equalizer", um Farbvariationen in gescannten Materialien für ein konsistentes Texturaussehen auszugleichen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

## Color Equalizer

**In:** *Materialfilter/Scanverarbeitung*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten funktioniert wie ein hochwertiger [Hochpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) für Farbunterschiede. Während ein normaler Hochpass die Sättigung entfernt und unerwünschte Schärfe verursachen kann, entfernt Color Equalizer unerwünschte Farbtöne in einer vom Benutzer auswählbaren Skala und sorgt so für einen gleichmäßigen Farbverlauf.

Dies ist sehr nützlich, wenn ein Foto oder Scan unerwünschte Farbunterschiede oder einen Farbton aufweist, den Sie entfernen möchten. Wenn Sie [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) verwendet haben, sollte dieser Knoten Ihnen bekannt vorkommen.

Die Maskierungsoptionen sind dazu bestimmt, sehr spezifische Farbtöne zu entfernen oder nur in bestimmten Wertebereichen zu arbeiten. Verwenden Sie diese, wenn Sie der Meinung sind, dass der Effekt zu breit ist.

## Parameter

### Eingaben

* **Eingabe**: *Farbeingabe*
* **Maskeneingabe**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte. Nur aktiv, wenn Maske auf &quot;Eingabe&quot; eingestellt ist.

### Parameter

* **Eingabetabelle**: *Falsch/Wahr* Behält optional die Unterteilung an Kanten bei.
* **Radius**: *0.0 - 50.0* Legt einen Ausgleichsradius fest. Bei einem größeren Radius werden nur große Farbunterschiede entfernt. Dies erfordert Nachbearbeitung für jedes Bild.
* **Helle/dunkle Balance**: *0.0 - 1.0* Voreinstellung, um dunklere Farbtöne zu belassen oder zu entfernen.
* **Benutzerdefinierte Farbvariation**: *Falsch/Wahr* Aktiviert die Möglichkeit, den Effekt in Richtung einer benutzerdefinierten Farbe zu variieren.
* **Farbvariation**\
  Nur aktiv, wenn &quot;Benutzerdefinierte Farbvariation&quot; aktiviert ist. Mit den Einstellungen können Sie einen Farbtonversatz auswählen, zu dem die Entzerrung erfolgen soll.
  * **Farbton**: *0.0 - 360.0*
  * **Chroma**: *0.0 - 1.0*
  * **Luminanz**: *0.0 - 1.0*
* **Maskenquelle**: *Keine, Bilddurchschnitt, Farbparameter, Eingabe* Festlegen, ob eine Maskierung erfolgen soll. Der Farbparameter aktiviert die folgenden zusätzlichen Einstellungen, die Eingabe wechselt zu einer benutzerdefinierten Maskeneingabe.
* **Maske**\
  Diese Option ist nur bei der Maskierung von Farbparametern aktiv. Zusätzliche Maskierungsparameter, um die Maske basierend auf dem Bild selbst zu bestimmen. Mit den folgenden Parametern können Sie einen Farbton präzise in eine Binärmaske konvertieren, auf die der Equalizer angewendet wird. Beachten Sie, dass die Effekte des Parameters &quot;Radius&quot; bei Verwendung dieser Einstellungen deutlich weniger ausgeprägt sein können.
  * **Farbe**: *(Farbwert)*
  * **Farbtonbereich**: *0.0 - 360.0*
  * **Chrominanzbereich**: *0.0 - 1.0*
  * **Luminanzbereich**: *0.0 - 1.0*
  * **Weichzeichnen**: *0.0 - 2.0*
  * **Smoothness**: *0.0 - 2.0*

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

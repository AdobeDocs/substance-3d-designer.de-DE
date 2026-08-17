---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Mehrere Color Equalizer", um die Farben über mehrere Texturkanäle hinweg auszugleichen und so eine konsistente Verarbeitung des gescannten Materials zu gewährleisten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mehrere Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---


# Mehrere Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

## Mehrere Color Equalizer

**In:** *Materialfilter/Scanverarbeitung*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dies ist die Multieingabeversion von [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md). Er gleicht Farbunterschiede aus und entfernt unerwünschte Farbtöne in einem vom Benutzer auswählbaren Maßstab. Es ist hauptsächlich für die Verwendung mit Mehrfachwinkelfotos vorgesehen, die dann mit [Mehrfachwinkel zu Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) oder [Mehrfachwinkel zu Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) kombiniert werden.

>[!NOTE]
>
> Weitere Informationen finden Sie im ursprünglichen [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md).

## Parameter

### Eingaben

* **Eingabe 1-8**: *Farbeingabe* Mehrere zu verarbeitende Eingaben.
* **Maskeneingabe**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Eingabeanzahl**: *1 - 8* Legt die Anzahl der parallel zu verarbeitenden Eingaben fest.
* **Eingabetabelle**: *Falsch/Wahr* Behält optional die Unterteilung an Kanten bei.
* **Radius**: *0.0 - 50.0* Legt einen Ausgleichsradius fest. Bei einem größeren Radius werden nur große Farbunterschiede entfernt. Dies erfordert Nachbearbeitung für jedes Bild.
* **Helle/dunkle Balance**: *0.0 - 1.0* Voreinstellung, um dunklere Farbtöne zu belassen oder zu entfernen.
* **Benutzerdefinierte Farbvariation**: *Falsch/Wahr* Ermöglicht es Ihnen, den Effekt in Richtung einer benutzerdefinierten Farbe zu variieren.
* **Farbvariation**\
  Nur aktiv, wenn &quot;Benutzerdefinierte Farbvariation&quot; aktiviert ist. Mit den Einstellungen können Sie einen Farbtonversatz auswählen, zu dem die Entzerrung erfolgen soll.
  * **Farbton**: *0.0 - 360.0*
  * **Chroma**: *0.0 - 1.0*
  * **Luminanz**: *0.0 - 1.0*
* **Maskenquelle**: *Keiner, Bilddurchschnitt, Farbparameter, Eingabe* Legt fest, ob Maskierung erfolgen soll. Der Farbparameter aktiviert unten zusätzliche Einstellungen, die Eingabe wechselt zu einer benutzerdefinierten Maskeneingabe.
* **Maske**\
  Nur aktiv mit Farbparameter-Maskierung. Enthält zusätzliche Maskierungsparameter, um die Maske basierend auf dem Bild selbst zu bestimmen. Mit den folgenden Parametern können Sie einen Farbton präzise in eine binäre Maske konvertieren, auf die die Entzerrung angewendet wird. Beachten Sie, dass die Effekte des Parameters &quot;Radius&quot; bei Verwendung dieser Einstellungen deutlich weniger ausgeprägt sein können.
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

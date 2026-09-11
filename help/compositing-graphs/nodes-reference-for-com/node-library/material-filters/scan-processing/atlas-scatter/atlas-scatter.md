---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Atlas Scatter", um Texturen über einen Atlas in Streuung zu setzen, um Kachelmuster aus gescannten Materialien zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas Scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 7%

---


# Atlas Scatter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](atlas-scatter.resources/atlas-scatter.png){width="200px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Extrahieren von Elementen aus einem Atlas und Streuung auf einem Hintergrund. Atlas-Eingänge sind vollständige Material, die aus Einzelelementen bestehen, die auf einer einzigen Textur angeordnet und verpackt sind. Dieser Knoten teilt sie (mithilfe eines internen [Atlas Splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md)-Prozesses) auf und Streuung sie, ähnlich wie [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md). Für die Atlas Scatter ist mindestens ein Eingang für die Deckkraftzuordnung und ein Höhen-Map-Eingang für den Atlas erforderlich, um funktionieren zu können.

</td>
</tr>
</table>

>[!NOTE]
>
> Hunderte von [Atlasen](https://source.substance3d.com/allassets?assetType=substanceAtlas), die im Knoten &quot;Atlas Scatter&quot; verwendet werden können, sind auf [Substance Source](https://source.substance3d.com/) verfügbar.

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Atlas-Eingabeauflösung</b> <i>Auflösung, 1 bis 12</i> | Stellen Sie die Auflösung des gesamten Eingabeatlas manuell ein, um ein gutes Leistungs-/Qualitätsverhältnis zu gewährleisten. |
| <b>X Betrag</b> <i>1 - 64</i> | Anzahl der X Wiederholungen des Musters. |
| <b>Y Betrag</b> <i>1 - 64</i> | Anzahl der Y-Wiederholungen des Musters. |
| <b>Muster</b> |  |
| <b>Musterbereich</b> <i>0 - 10</i> | Definiert den Bereich der zu streuenden Muster. Wenn auf 0 gesetzt, werden alle Muster verwendet. |
| <b>Musterverteilungsmodus</b> <i>Zufällig, Musterindex, Zeilenindex, Spaltenindex</i> | Definiert die Reihenfolge, in der Atlaselemente verwendet werden. |
| <b>Zuordnungsmultiplikator für Musterverteilung</b> <i>0.0 - 1.0</i> | Wählen Sie ein Formmuster in Abhängigkeit vom Graustufenwert des Eingabebilds aus. |
| <b>Musterrotation</b> <i>0, 90, 180, 270</i> | Wendet eine feste Drehung auf jedes Atlaselement an, und zwar um den ausgewählten Wert in Grad. |
| <b>Musterrotation zufällig</b> <i>0.0 - 1.0</i> | Wendet eine zufällige Drehung auf den festgelegten Abschnitt der Atlaselemente an. |
| <b>Genauigkeit bei der Erkennung von Atlasformen</b> <i>Einfache oder kleine Formen, komplexe oder große Formen, kein Fehlermodus</i> | Legt die Genauigkeit fest, mit der Formen erkannt werden. Je genauer sie sind, desto stärker wirken sie sich auf die Leistung aus. |
| <b>Atlas-Deckkraft reduzieren (schnellere Erkennung)</b> <i>-4 - 0</i> | Ermöglicht die Steuerung des Downskalierungsverhältnisses der Deckkraftmap des Eingabeatlas, die für die Formerkennung verwendet wird. Eine niedrigere Auflösung verbessert die Leistung auf Kosten der Genauigkeit. |
| <b>Form ignorieren, die kleiner ist als </b> <i>0.0 - 1.0</i> | Legt die Mindestgröße fest, die eine Form erkannt werden muss, ausgedrückt als Verhältnis zum Gesamtbild |
| <b>Größe</b> |  |
| <b>Skalierung</b> <i>0.0 - 5.0</i> | Legt den relativen Maßstab von gestreuten Formen fest. |
| <b>Zufällige Skalierung</b> <i>0.0 - 1.0</i> | Definiert den Multiplikator für die Anwendung der zufälligen Skalierung auf jede gestreute Form. |
| <b>Keine Überlappung skalieren</b> <i>0.0 - 1.0</i> | Reduziert die Formskalierung, sodass sie sich nicht überlappen. |
| <b>Zuordnungsmultiplikator skalieren</b> <i>0.0 - 1.0</i> | Multipliziert die Formskala mit dem Graustufenwert des Eingabebilds. |
| <b>Größe</b> <i>0.0 - 1.0</i> | Legt den relativen Maßstab der gestreuten Formen nach Länge (X) und Breite (Y) fest. |
| <b>Größenverhältnis von Bg-Steigung</b> <i>0.0 - 1.0</i> | Ändert das Größenverhältnis der Form in Abhängigkeit von der Steigung des Heights im Hintergrund. |
| <b>Seitenverhältnis beibehalten</b> <i>0.0 - 1.0</i> | Legt fest, um welchen Wert die ursprünglichen Proportionen der gestreuten Formen beibehalten werden sollen, anstatt das Zellverhältnis des Rasters zu verwenden, d. h. das Verhältnis der Werte für &quot;x-Stärke&quot; und &quot;y-Stärke&quot;. |
| <b>Position</b> |  |
| <b>Position zufällig</b> <i>0.0 - 2.0</i> | Ein Multiplikator, um jede Form in einer zufälligen Richtung von ihrem Raster-Startpunkt zu bewegen. |
| <b>Zufallsverteilung</b> <i>Gaußsch, einheitlich</i> | Wechselt für die zufällige Position von einer Gaußschen Verteilung zu einer gleichmäßigen Verteilung. Die Gaußsche Verteilung wird ein organischeres Ergebnis erzeugen als die Uniform-Verteilung. |
| <b>Vektorzuordnungsvervielfacher</b> <i>0.0 - 1.0</i> | Steuert den Einfluss der Vektormap-Eingabe auf das Verschieben der Formen in die Richtung des Vektors, der durch die roten (X) und grünen (Y) Kanäle der Karte angegeben wird. |
| <b>Horizontaler Versatz</b> <i>-2.0 - 2.0</i> | Ein Multiplikator für den Positionsversatz entlang der X-Achse. |
| <b>Vertikaler Versatz</b> <i>-2.0 - 2.0</i> | Ein Multiplikator für den Positionsversatz entlang der Y-Achse. |
| <b>Out-of-Bounds-Option</b> <i>Form skalieren, Position beschränken</i> | Aufgrund des technischen Charakters des Spritzers können Formen nicht mehr als 2 Zellen von ihrer ursprünglichen Position entfernt gezeichnet werden. Wenn eine Form zu groß wird oder zu weit verschoben wird, stehen Ihnen zwei Optionen zur Verfügung: - &quot;Form skalieren&quot; reduziert die Formgröße, wenn es auf eine Grenze trifft - &quot;Position beschränken&quot; verschiebt die Form zurück an ihre ursprüngliche Position |
| <b>Drehung</b> |  |
| <b>Drehung</b> <i>0.0 - 1.0</i> | Ermöglicht die Steuerung der lokalen Drehung für alle Formen. |
| <b>Drehung zufällig</b> <i>0.0 - 1.0</i> | Ein Multiplikator für einen zufälligen Betrag an Drehung, der pro Form angewendet wird. |
| <b>Drehung aus Bg-Steigung</b> <i>0.0 - 1.0</i> | Ändert die Drehung der Form in Abhängigkeit von der Steigung des Heights im Hintergrund. Wird gewöhnlich in Kombination mit dem Parameter &quot;Größenverhältnis von Bg-Steigung&quot; verwendet |
| <b>Rotation Map-Multiplikator</b> <i>0.0 - 1.0</i> | Multipliziert die Formdrehung in Funktion des Graustufenwerts für das Eingabebild. |
| <b>Vektorzuordnungsvervielfacher</b> <i>0.0 - 1.0</i> | Legt die Formdrehung in Abhängigkeit von der Vektorbildeingabe fest. |
| <b>Height</b> |  |
| <b>Automatische Anpassung der Skalierung des Heights</b> <i>False/True</i> | Passt das Height automatisch an die Musterskala an, damit das Height der Form proportional zum Hintergrund-Height bleibt. |
| <b>Füllmethode</b> <i>Height-Überblendung, Alpha-Test</i> | Legt die Methode zum Auflösen von Formenüberlappungen fest. |
| <b>Height-Offset</b> <i>-1.0 - 1.0</i> | Wendet einen globalen Versatz auf das Formen-Height an |
| <b>Height-Offset zufällig</b> <i>0.0 - 1.0</i> | Ein Multiplikator für einen zufälligen Height-Versatz, der pro Form angewendet wird |
| <b>Height-Versatzzuordnungs-Multiplikator</b> <i>0.0 - 1.0</i> | Multipliziert den Offset des Formenbilds in Abhängigkeit vom Graustufenwert des Heights. |
| <b>Height-Skalierung</b> <i>0.0 - 1.0</i> | Ermöglicht die Steuerung der globalen Height-Skalierung für die verstreuten Formen |
| <b>Zufällige Skalierung des Heights</b> <i>0.0 - 1.0</i> | Ein Multiplikator für eine zufällige Height-Skalierung, die pro Form angewendet wird |
| <b>Height-Skalierungszuordnungsvervielfacher</b> <i>0.0 - 1.0</i> | Multipliziert den Maßstab des Heights in Abhängigkeit vom Graustufenwert des Eingabebilds. |
| <b>Mit Hintergrund konform</b> <i>0.0 - 1.0</i> | Bei 0 bleibt das Form-Height intakt, bei 1 wird das Form-Height durch den zugrunde liegenden Hintergrund des Heights deformiert. |
| <b>Glätten des konformen Hintergrunds</b> <i>0.0 - 2.0</i> | Hier können Sie den Grad der Glättung steuern, der auf die Height-Deformation der Form angewendet wird, wenn sie an ihren Hintergrund angepasst wird. |
| <b>Neigung von Bg-Steigung</b> <i>0.0 - 1.0</i> | Deformiert das Form-Height in Abhängigkeit von der Steigung des lokalen Hintergrund-Heights: Ein linearer Verlauf, der der Steigung des Hintergrunds entspricht, wird zum Height &quot;Form&quot; hinzugefügt. |
| <b>Smoothness der Hintergrund-Steigung</b> <i>0.0 - 2.0</i> | Steuert den Grad der Glättung, der auf die Steigung des Hintergrunds angewendet wird, wenn die Form basierend auf dieser Steigung geneigt wird. |
| <b>Schwarze Pixel ausschneiden</b> <i>False/True</i> | Ignoriert den Schwarzwert der Mustereingaben. |
| <b>Reduzierte Musterbasis</b> <i>False/True</i> | Erlaubt es Ihnen, das Hintergrund-Height unter einer Form zu reduzieren, damit es dem Anfangs-Height entspricht. |
| <b>Maskieren</b> |  |
| <b>Zufällige Maske</b> <i>0.0 - 1.0</i> | Maskiert eine zufällige Anzahl von Formen, ausgedrückt als Verhältnis der Gesamtmenge. |
| <b>Zufällige Maskenzuordnungsvervielfacher</b> <i>0.0 - 1.0</i> | Legt die zufällige Formmaskierung in Abhängigkeit von der Graustufenbildeingabe fest. |
| <b>Maske aus Bg-Steigung</b> <i>-1.0 - 1.0</i> | Steuert die Maskierung der Formen anhand der Steigung des Hintergrunds an ihrer Position. |
| <b>Farbe</b> |  |
| <b>Farbkorrektur</b> <i>-1.0 - 1.0</i> | Ermöglicht die globale Anpassung der Farben für die verstreuten Elemente. |
| <b>Farbzufall</b> <i>0.0 - 1.0</i> | Ein Multiplikator zum Verschieben der Farbwerte um einen zufälligen Betrag pro Form. |
| <b>Farbe aus Hintergrund</b> <i>0.0 - 1.0</i> | Verschiebt die Formenfarben an die Hintergrundfarbe an ihrer Position. |
| <b>Normal</b> |  |
| <b>Neigung von Bg-Steigung</b> <i>0.0 - 1.0</i> | Neigen Sie die Form normal entsprechend der Hintergrundnormalität. |
| <b>Normaler Zufallswert</b> <i>0.0 - 1.0</i> | Ein Multiplikator zum Neigen der normalen Form um einen zufälligen Betrag pro Form. |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Zwischen verschiedenen Normalen-Map-Format wechseln (invertiert den grünen Kanal) |
| <b>Raueit</b> |  |
| <b>Anpassung der Rauheit</b> <i>-1.0 - 1.0</i> | Ermöglicht das Versetzen der globalen Formrauhigkeit. |
| <b>Rauheit aus dem Hintergrund</b> <i>0.0 - 1.0</i> | Verschiebt die Raueit der Formen an die Hintergrundrauheit an ihrer Position. |
| <b>Rauheit zufällig</b> <i>0.0 - 1.0</i> | Ein Multiplikator zum Versetzen der Rauheit um einen zufälligen Betrag pro Form. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="atlas-scatter.resources/atlas-scatter-11.png" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Atlas Scatter", um Texturen in einem Atlas für die Erstellung von Kachelmustern aus gescannten Streuungen zu verwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas Scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 0%

---


# Atlas Scatter

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/atlas-scatter.png){width="200px"}

## Atlas Scatter

**In:** *Materialfilter/Scanverarbeitung*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Extrahieren von Elementen aus einem Atlas und Streuung auf einem Hintergrund. Atlas-Eingänge sind Vollmaterialien, die aus einzelnen Elementen bestehen, die auf einer einzigen Texturfolie angeordnet und verpackt sind. Dieser Knoten teilt sie (mithilfe eines internen [Atlas Splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md)-Prozesses) auf und Streuung sie, ähnlich wie [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md). Für die Atlas Scatter ist mindestens ein Eingang für die Deckkraftmap und ein Eingang für die Height-Map erforderlich, damit der Atlas funktioniert.

>[!NOTE]
>
> Hunderte von [Atlasen](https://source.substance3d.com/allassets?assetType=substanceAtlas), die im Knoten &quot;Atlas Scatter&quot; verwendet werden können, sind auf [Substance Source](https://source.substance3d.com/) verfügbar.

## Eingaben und Parameter

### Parameter

* **Atlas-Eingabeauflösung**: *Auflösung, 1 bis 12*\
  Stellen Sie die Auflösung des gesamten Eingabeatlas manuell ein, um ein gutes Leistungs-/Qualitätsverhältnis zu gewährleisten.
* **X Betrag**: *1 - 64*\
  Anzahl der X Wiederholungen des Musters.
* **Y Betrag**: *1 - 64*\
  Anzahl der Y-Wiederholungen des Musters.
* **Muster**
  * **Musterbereich**: *0 - 10*\
    Definiert den Bereich der zu streuenden Muster. Wenn auf 0 gesetzt, werden alle Muster verwendet.
  * **Musterverteilungsmodus**: *Zufällig, Musterindex, Zeilenindex, Spaltenindex* Definiert die Reihenfolge, in der Atlaselemente verwendet werden.
  * **Zuordnungsmultiplikator für Musterverteilung**: *0.0 - 1.0*\
    Wählen Sie ein Formmuster in Abhängigkeit des Graustufenwerts des Eingabebilds aus.
  * **Musterrotation**: *0, 90, 180, 270*\
    Wendet eine feste Drehung auf jedes Atlaselement an, und zwar um den ausgewählten Wert in Grad.
  * **Zufällige Musterdrehung**: *0.0 - 1.0*\
    Wendet eine zufällige Drehung auf den festgelegten Abschnitt der Atlaselemente an.
  * **Genauigkeit der Atlasformerkennung**: *Einfache oder kleine Formen, komplexe oder große Formen, kein Fehlermodus*\
    Legt die Genauigkeit fest, mit der Formen erkannt werden. Je genauer sie sind, desto stärker wirken sie sich auf die Leistung aus.
  * **Atlas-Deckkraft reduzieren (schnellere Erkennung)**: *-4 - 0*\
    Ermöglicht die Steuerung des Downskalierungsverhältnisses der Deckkraftmap des Eingabeatlas, die für die Formerkennung verwendet wird. Eine niedrigere Auflösung verbessert die Leistung auf Kosten der Genauigkeit.
  * **Form ignorieren, die kleiner ist als**: *0.0 - 1.0* Legt die Mindestgröße fest, die eine Form erkannt werden muss, ausgedrückt als Verhältnis zum Gesamtbild
* **Größe**
  * **Skalierung**: *0.0 - 5.0*\
    Legt den relativen Maßstab von gestreuten Formen fest.
  * **Zufällige Skalierung**: *0.0 - 1.0*\
    Definiert den Multiplikator für die Anwendung der zufälligen Skalierung auf jede gestreute Form.
  * **Keine Überlappung skalieren**: *0.0 - 1.0*\
    Reduziert die Formskalierung, sodass sie sich nicht überlappen.
  * **Zuordnungsmultiplikator skalieren**: *0.0 - 1.0*\
    Multipliziert den Formmaßstab in Funktion des Graustufenwerts für das Eingabebild.
  * **Größe**: *0.0 - 1.0*\
    Legt den relativen Maßstab der gestreuten Formen nach Länge (X) und Breite (Y) fest.
  * **Größenverhältnis von Bg-Steigung**: *0.0 - 1.0*\
    Ändert das Größenverhältnis der Form in Abhängigkeit von der Steigung des Heights im Hintergrund.
  * **Seitenverhältnis beibehalten**: *0.0 - 1.0*\
    Legt fest, um welchen Betrag die ursprünglichen Proportionen der gestreuten Formen beibehalten werden sollen, anstatt das Rasterzellenverhältnis zu verwenden, d. h. das Verhältnis der Werte für &quot;x-Betrag&quot; und &quot;y-Betrag&quot;.
* **Position**
  * **Position zufällig**: *0.0 - 2.0*\
    Ein Multiplikator zum Verschieben jeder Form in einer zufälligen Richtung von ihrem Startpunkt im Raster.
  * **Zufallsverteilung**: *Gaußsch, einheitlich*\
    Wechselt für die zufällige Position von einer Gaußschen Verteilung zu einer gleichmäßigen Verteilung. Die Gaußsche Verteilung wird ein organischeres Ergebnis erzeugen als die Uniform-Verteilung.
  * **Vektorkartenmultiplikator**: *0.0 - 1.0*\
    Steuert den Einfluss der Vektormap-Eingabe auf das Verschieben der Formen in die Richtung des Vektors, der durch die roten (X) und grünen (Y) Kanäle der Karte angegeben wird.
  * **Horizontaler Versatz**: *-2.0 - 2.0*\
    Ein Multiplikator für den Positionsversatz entlang der X-Achse.
  * **Vertikaler Versatz**: *-2.0 - 2.0*\
    Ein Multiplikator für den Positionsversatz entlang der Y-Achse.
  * **Out-of-Bounds-Option**: *Form skalieren, Position beschränken*\
    Aufgrund des technischen Charakters des Spritzers können Formen nicht mehr als 2 Zellen von ihrer ursprünglichen Position entfernt gezeichnet werden. Wenn eine Form zu groß wird oder zu weit verschoben wird, stehen Ihnen zwei Optionen zur Verfügung: - &quot;Form skalieren&quot; reduziert die Formgröße, wenn es auf eine Grenze trifft - &quot;Position beschränken&quot; verschiebt die Form zurück an ihre ursprüngliche Position
* **Drehung**
  * **Drehung**: *0.0 - 1.0*\
    Ermöglicht die Steuerung der lokalen Drehung für alle Formen.
  * **Drehung zufällig**: *0.0 - 1.0*\
    Ein Multiplikator für einen zufälligen Betrag an Drehung, der pro Form angewendet wird.
  * **Drehung aus Bg-Steigung**: *0.0 - 1.0*\
    Ändert die Drehung der Form in Abhängigkeit von der Steigung des Heights im Hintergrund. Wird gewöhnlich in Kombination mit dem Parameter &quot;Größenverhältnis von Bg-Steigung&quot; verwendet
  * **Rotation Map-Multiplikator**: *0.0 - 1.0*\
    Multipliziert die Formdrehung in Funktion des Graustufenwerts für das Eingabebild.
  * **Vektorkartenmultiplikator**: *0.0 - 1.0*\
    Legt die Formdrehung in Abhängigkeit von der Vektorbildeingabe fest.
* **Height**
  * **Automatische Anpassung der Height-Skalierung**: *False/True*\
    Passt das Height automatisch an die Musterskala an, damit das Height der Form proportional zum Hintergrund-Height bleibt.
  * **Füllmethode**: *Height-Überblendung, Alpha-Test*\
    Legt die Methode zum Auflösen von Formenüberlappungen fest.
  * **Height-Offset**: *-1.0 - 1.0*\
    Wendet einen globalen Versatz auf das Formen-Height an
  * **Height-Offset zufällig**: *0.0 - 1.0*\
    Ein Multiplikator für einen zufälligen Height-Versatz, der pro Form angewendet wird
  * **Height-Versatzzuordnungs-Multiplikator**: *0.0 - 1.0*\
    Multipliziert den Offset des Formenbilds in Abhängigkeit vom Graustufenwert des Heights.
  * **Height-Skalierung**: *0.0 - 1.0*\
    Ermöglicht die Steuerung der globalen Height-Skalierung für die verstreuten Formen
  * **Zufällige Skalierung des Heights**: *0.0 - 1.0*\
    Ein Multiplikator für eine zufällige Height-Skalierung, die pro Form angewendet wird
  * **Height-Skalierungszuordnungsvervielfacher**: *0.0 - 1.0*\
    Multipliziert den Maßstab des Heights in Abhängigkeit vom Graustufenwert des Eingabebilds.
  * **Mit Hintergrund konform**: *0.0 - 1.0*\
    Bei 0 bleibt das Form-Height intakt, bei 1 wird das Form-Height durch den zugrunde liegenden Hintergrund des Heights deformiert.
  * **Glätten konformer Hintergrund**: *0.0 - 2.0*\
    Hier können Sie den Grad der Glättung steuern, der auf die Height-Deformation der Form angewendet wird, wenn sie an ihren Hintergrund angepasst wird.
  * **Neigung von Bg-Steigung**: *0.0 - 1.0*\
    Deformiert das Form-Height in Abhängigkeit von der Steigung des lokalen Hintergrund-Heights: Ein linearer Verlauf, der der Steigung des Hintergrunds entspricht, wird zum Height &quot;Form&quot; hinzugefügt.
  * **Smoothness der Hintergrund-Steigung**: *0.0 - 2.0*\
    Steuert den Grad der Glättung, der auf die Steigung des Hintergrunds angewendet wird, wenn die Form basierend auf dieser Steigung geneigt wird.
  * **Schwarze Pixel ausschneiden**: *False/True*\
    Ignoriert den Schwarzwert der Mustereingaben.
  * **Reduzierte Musterbasis**: *False/True*\
    Erlaubt es Ihnen, das Hintergrund-Height unter einer Form zu reduzieren, damit es dem Anfangs-Height entspricht.
* **Maskieren**
  * **Zufällige Maske**: *0.0 - 1.0*\
    Maskiert eine zufällige Anzahl von Formen, ausgedrückt als Verhältnis der Gesamtmenge.
  * **Zufällige Maskenzuordnungsvervielfacher**: *0.0 - 1.0*\
    Legt die zufällige Formmaskierung in Abhängigkeit von der Graustufenbildeingabe fest.
  * **Maske aus Bg-Steigung**: *-1.0 - 1.0*\
    Steuert die Maskierung der Formen anhand der Steigung des Hintergrunds an ihrer Position.
* **Farbe**
  * **Farbkorrektur**: *-1.0 - 1.0*\
    Ermöglicht die globale Anpassung der Farben für die verstreuten Elemente.
  * **Farbzufall**: *0.0 - 1.0*\
    Ein Multiplikator zum Verschieben der Farbwerte um einen zufälligen Betrag pro Form.
  * **Farbe aus Hintergrund**: *0.0 - 1.0*\
    Verschiebt die Formenfarben an die Hintergrundfarbe an ihrer Position.
* **Normal**
  * **Neigung von Bg-Steigung**: *0.0 - 1.0*\
    Neigen Sie die Form normal entsprechend der Hintergrundnormalität.
  * **Normaler Zufallswert**: *0.0 - 1.0*\
    Ein Multiplikator zum Neigen der normalen Form um einen zufälligen Betrag pro Form.
  * **Normales Format**: *DirectX, OpenGL*\
    Zwischen verschiedenen Normalen-Map-Format wechseln (invertiert den grünen Kanal)
* **Raueit**
  * **Raueitskorrektur**: *-1.0 - 1.0*\
    Ermöglicht das Versetzen der globalen Formrauhigkeit.
  * **Raueit aus dem Hintergrund**: *0.0 - 1.0*\
    Verschiebt die Raueit der Formen an die Hintergrundrauheit an ihrer Position.
  * **Unregelmäßigkeit zufällig**: *0.0 - 1.0* Ein Multiplikator zum Versetzen der Raueit um einen zufälligen Betrag pro Form.

## Beispielbilder

![](../../../../../../assets/atlas-scatter-11.png){width="512px"}

</td>
</tr>
</table>

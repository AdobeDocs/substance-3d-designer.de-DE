---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ''
description: Verwenden Sie den Bitmap-Knoten, um Bitmapbilder als Texturen in Substance-Kompositionsdiagrammen zu importieren und zu verwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 1%

---


# Bitmap

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Bitmap](../../../../assets/comp_bitmap.png "Atomischer Knoten: Bitmap"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Lädt eine [Bitmapressource](../../../../resources/bitmap-resource/bitmap-resource.md) in das Diagramm.

Dieser Knoten wird verwendet, um entweder eine [Bitmap](../../../../glossary/glossary.md) in Ihr Diagramm zu importieren oder eine neue Bitmap zur Verwendung mit den [Bitmap-Malwerkzeugen](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) zu erstellen.

Es gibt verschiedene Möglichkeiten, diesen Knoten zu erstellen. Für alle diese Möglichkeiten müssen Sie [ den Unterschied zwischen dem Verknüpfen und dem Importieren von Ressourcen verstehen.](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
</tr>
</table>

Sie können den Knoten entweder von Grund auf neu erstellen oder eine [Bitmap](../../../../glossary/glossary.md) in einem unterstützten Format in der Diagrammansicht ablegen.

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

>[!TIP]
>
> Generierte oder importierte 8-Bit-Bitmaps können mit den [Bitmap-Malwerkzeugen](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) im Dock [2D view](../../../../interface/2d-view/2d-view.md) gemalt werden.

>[!IMPORTANT]
>
> Dieser Knoten ist von einer externen Ressource abhängig, daher gibt es einige Punkte, die Sie bei der Arbeit mit ihnen beachten sollten:
> 
> * Bitmap-Knoten können entweder Farbe oder Graustufen zurückgeben, die Standardfarbe ist jedoch Farb, selbst wenn die Ressource eine Graustufen-Bitmap ist. Dies kann sich auf die Leistung und Komplexität des Diagramms auswirken. Stellen Sie daher immer sicher, dass Sie bei Bedarf zum [Graustufen-Farbmodus](#parameters) wechseln.
> * Durch das Löschen eines Bitmapknotens wird die [Bitmapressource](../../../../resources/bitmap-resource/bitmap-resource.md) in Ihrem [Paket](../../../../glossary/glossary.md) nicht gelöscht. Sie müssen dies manuell im [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) tun.
> * Seien Sie jedoch vorsichtig, wenn Sie eine [Bitmapressource](../../../../resources/bitmap-resource/bitmap-resource.md) im Explorer löschen: Es funktioniert weiterhin im Diagramm für diese Sitzung, da es im Cache gespeichert wird, aber die Ressource wird als fehlend markiert, wenn Sie das [Paket](../../../../glossary/glossary.md) das nächste Mal laden.
> * Wenn ein Substance-Diagramm [gekocht](../../../../glossary/glossary.md) ist, wird die Bitmapauflösung an ihrer Auflösung im Diagramm und nicht an ihrer Originalgröße festgelegt. Es wird empfohlen, sicherzustellen, dass der [Basisparameter für die Ausgabegröße](../../../../glossary/glossary.md) eines Bitmap-Knotens die [-Vererbungsmethode &quot;Absolut&quot; verwendet ](../../../../glossary/glossary.md) und dem Knoten ein [Knoten für 2D](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)-Transformieren folgt, der auf &quot;Relativ zu übergeordnetem Knoten&quot; festgelegt ist (d. h. die Auflösung des Hostdiagramms).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parameter

</td>
<td style="border: 0;" valign="top">

### Bitmap-Malwerkzeuge

</td>
<td style="border: 0;" valign="top">

### Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolescher Wert* | Bestimmt den Ausgabetyp des Knotens, der entweder in Farbe oder in Graustufen zurückgegeben wird. |
| <b>PKG-Ressourcenpfad</b> *Zeichenfolge* | Pfad zur [Bitmapressource](../../../../resources/bitmap-resource/bitmap-resource.md), auf die vom Knoten verwiesen wird.   Es wird empfohlen, eine Ressource nicht manuell einzugeben, sondern entweder aus dem Explorer zu kopieren und in das Parametertextfeld einzufügen, oder eine Bitmapressource direkt aus dem [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) auf den Bitmapknoten im Diagramm zu ziehen und abzulegen. |
| <b>Methode zur Größenänderung</b> *Integer* | Die Neuberechnungsmethode für das Hoch- oder Herunterskalieren einer Bitmap:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Ruhige Dehnung:</i> Wenden Sie [bilineare Filter](../../../../glossary/glossary.md) an, um die Quellpixel des gedehnten Bildes zu interpolieren.</li> <li data-preserve-html="true"><i>Nächste Dehnung:</i> Dehnen Sie das Bild und verwenden Sie die Farbe des nächstgelegenen Quellpixel so, wie sie ist.</li> </ul> |

## Bitmap-Malwerkzeuge

Bitmaps können in Designer bearbeitet werden. Weitere Informationen zu den Bearbeitungswerkzeugen in [diesem Abschnitt](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

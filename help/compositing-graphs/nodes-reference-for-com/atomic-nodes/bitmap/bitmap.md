---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ''
description: Verwenden Sie den Bitmap-Knoten, um Bitmapbilder als Texturen in Substance-Compositing-Grafen zu importieren und zu verwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 989234054615406114d2f7664ebee6f8c86f4bf2
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---


# Bitmap

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elementare Knoten: Bitmap](bitmap.resources/comp_bitmap.png "Elementare Knoten: Bitmap"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Lädt eine [Bitmapressource](../../../../resources/bitmap-resource/bitmap-resource.md) in den Graf.

Dieser Knoten wird verwendet, um entweder eine [Bitmap](../../../../glossary/glossary.md) in Ihren Graf zu importieren oder eine neue Bitmap zur Verwendung mit den [Bitmap-Malwerkzeugen](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) zu erstellen.

Es gibt verschiedene Möglichkeiten, diesen Knoten zu erstellen. Für alle diese Möglichkeiten müssen Sie [den Unterschied zwischen dem Verknüpfen und dem Importieren von Ressourcen verstehen.](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
</tr>
</table>

Sie können den Knoten entweder von Grund auf neu erstellen oder eine [Bitmap](../../../../glossary/glossary.md) in einem unterstützten Format in der Graphansicht ablegen.

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
> Generierte oder importierte 8-Bit-Bitmaps können mit den [Bitmap-Malwerkzeugen](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) im [2D-Ansicht](../../../../interface/2d-view/2d-view.md)-Dock gemalt werden.

>[!IMPORTANT]
>
> Dieser Knoten ist von einer externen Ressource abhängig, daher gibt es einige Punkte, die Sie bei der Arbeit mit ihnen beachten sollten:
> 
> * Bitmap-Knoten können entweder Farbe oder Graustufen zurückgeben, die Standardfarbe ist jedoch Farb, selbst wenn die Ressource eine Graustufen-Bitmap ist. Dies kann sich auf die Leistung und Komplexität des Grafen auswirken. Stellen Sie daher immer sicher, dass Sie bei Bedarf zum [Graustufen-Farbmodus](#parameters) wechseln.
> * Durch das Löschen eines Bitmapknotens wird die [Bitmapressource](../../../../resources/bitmap-resource/bitmap-resource.md) in Ihrem [Paket](../../../../glossary/glossary.md) nicht gelöscht. Sie müssen dies manuell im [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) tun.
> * Seien Sie andererseits vorsichtig, wenn Sie eine [Bitmapressource](../../../../resources/bitmap-resource/bitmap-resource.md) im Explorer löschen: Sie funktioniert weiterhin im Graf für diese Sitzung, da sie im Cache gespeichert wird. Die Ressource wird jedoch als fehlend markiert, wenn Sie das [Paket](../../../../glossary/glossary.md) das nächste Mal laden.
> * Wenn ein Substance-Graf [gekocht](../../../../glossary/glossary.md) ist, wird die Bitmapauflösung an ihrer Auflösung innerhalb des Grafen und nicht an ihrer Originalgröße festgelegt. Es wird empfohlen, sicherzustellen, dass der [Basisparameter](../../../../glossary/glossary.md) für die Ausgabegröße eines Bitmapknotens die [Absolutauflösungsmethode &#x200B;](../../../../glossary/glossary.md) verwendet und dass auf den Graf ein [Transformieren 2D](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)-Knoten folgt, der auf &quot;Relativ zum übergeordneten Element&quot; (d. h. die Vererbung des Hostknotens) festgelegt ist.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parameter

</td>
<td style="border: 0;" valign="top">

### Bitmap-Malwerkzeuge

</td>
<td style="border: 0;" valign="top">

### Ausgabe-Verbindungen

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolesche Wert* | Bestimmt den Ausgabetyp des Knotens, der entweder in Farbe oder in Graustufen zurückgegeben wird. |
| <b>PKG-Ressourcenpfad</b> *Zeichenfolge* | Pfad zur [Bitmapressource](../../../../resources/bitmap-resource/bitmap-resource.md), auf die vom Knoten verwiesen wird.   Es wird empfohlen, eine Ressource nicht manuell einzugeben, sondern entweder vom Explorer zu kopieren und in das Parametertextfeld einzufügen, oder eine Bitmapressource direkt vom [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) auf den Bitmapknoten im Graf zu ziehen und abzulegen. |
| <b>Methode zur Größenänderung</b> *Ganzzahl* | Die Neuberechnungsmethode für das Hoch- oder Herunterskalieren einer Bitmap:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Ruhige Dehnung:</i> Wenden Sie [bilineare Filter](../../../../glossary/glossary.md) an, um die Quellpixel des gedehnten Bildes zu interpolieren.</li> <li data-preserve-html="true"><i>Nächste Dehnung:</i> Dehnen Sie das Bild und verwenden Sie die Farbe des nächstgelegenen Quellpixel so, wie sie ist.</li> </ul> |

## Bitmap-Malwerkzeuge

Bitmaps können in Designer bearbeitet werden. Weitere Informationen zu den Bearbeitungswerkzeugen in [diesem Abschnitt](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

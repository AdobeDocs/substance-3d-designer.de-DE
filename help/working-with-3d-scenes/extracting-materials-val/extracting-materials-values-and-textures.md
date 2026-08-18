---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/extracting-materials-values-and-textures.html"
breadcrumb-title: ''
description: Extrahieren Sie Materialeigenschaften aus 3D-Szenen, um sie in Substance-Graphen für Workflows zur Materialerstellung zu verwenden.
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Extracting materials values and textures
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extrahieren von Materialwerten und Texturen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# Extrahieren von Materialwerten und Texturen

Die Materialeigenschaften können extrahiert und in Substance-Graphen verwendet werden.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Neues Diagramm aus Texturen

</td>
<td style="border: 0;" valign="top">

### Textur extrahieren.

</td>
<td style="border: 0;" valign="top">

### Wert extrahieren

</td>
</tr>
</table>

## Neues Diagramm aus Texturen

Die Aktion &quot;Graph aus Textureingaben erstellen&quot; erstellt ein neues Substance-Graph mit allen Texturen, die von einem Material verwendet werden.

Mit dieser Aktion können Sie u. a. Folgendes tun:

* Ein Substance-Diagramm, das nach dem Material benannt ist, wird an der ausgewählten Position erstellt.
* Für jede vom Material verwendete Textur wird eine [Bitmapressource](../../resources/bitmap-resource/bitmap-resource.md) erstellt und in einem nach dem Material benannten Ordner unter einem Ordner &quot;Resources&quot; abgelegt.
* Im Diagramm werden [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) Knoten für jede dieser Bitmap-Ressourcen erstellt und automatisch mit [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) Knoten verbunden, die nach den Materialeigenschaften mithilfe von Texturen konfiguriert wurden.
* Wenn jeder Kanal mit derselben Textur verwendet wird, um unterschiedliche Materialeigenschaften zu steuern (die Technik wird als [Kanalknoten](../../glossary/glossary.md) bezeichnet), werden automatisch [Graustufen-Packing](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md) hinzugefügt, um die entsprechenden Kanäle auszuwählen.
* Das Diagramm wird automatisch mit dem Material verbunden und sein Erscheinungsbild sollte sich erst ändern, wenn Sie Änderungen am Diagramm vornehmen.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Diagramm aus Textureingaben erstellen - Aktion im Viewport &quot;3D-Ansicht&quot;](../../assets/createGraphFromTexturesActionViewport.png "Diagramm aus Textureingaben erstellen - Aktion im Viewport &quot;3D-Ansicht&quot;"){zoomable="yes"}

*Aktion im Ansichtsport der 3D-Ansicht*

</td>
<td style="border: 0;" valign="top">

![Diagramm aus Textureingaben erstellen - Aktion im Menü &quot;Materialien&quot;](../../assets/createGraphFromTexturesActionMaterials.png "Diagramm aus Textureingaben erstellen - Aktion im Menü &quot;Materialien&quot;"){zoomable="yes"}

*Aktion im Materialmenü*

</td>
<td style="border: 0;" valign="top">

![Diagramm aus Textureingaben erstellen - Aktion im Dock &quot;Eigenschaften&quot;](../../assets/createGraphFromTexturesActionProps.png "Diagramm aus Textureingaben erstellen - Aktion im Dock &quot;Eigenschaften&quot;"){zoomable="yes"}

*Aktion im Eigenschaftendock*

</td>
</tr>
</table>

![Ergebnis der Diagrammerstellung aus Materialtexturen](../../assets/createGraphFromTexturesResult.png "Ergebnis der Diagrammerstellung aus Materialtexturen"){zoomable="yes"}

*Ergebnis der Diagrammerstellung aus Materialtexturen*

+++Demonstration
![Diagramm aus Textureingaben erstellen - Demonstration](../../assets/createGraphFromTextures.gif "Diagramm aus Textureingaben erstellen - Demonstration"){zoomable="yes"}



+++

>[!TIP]
>
> Sie können schnell und direkt im Ansichtsfenster der 3D-Ansicht auf die Aktion zugreifen, indem Sie den Cursor auf das Objekt setzen und <b>Umschalt+LMB</b> drücken, um es auszuwählen. und dann auf RMB klicken, um auf ein Kontextmenü zuzugreifen, das die Aktion hostet.

>[!NOTE]
>
> Für Formate mit *eingebetteten Texturen* (z. B.: USDZ), müssen die Texturen extrahiert und auf die Festplatte kopiert werden. Dies führt zu einem zusätzlichen Schritt, in dem Sie den Speicherort auswählen, an dem die Texturen extrahiert werden sollen.

## Textur extrahieren.

Mit der Aktion &quot;Textur in Diagramm extrahieren&quot; wird in einem vorhandenen Diagramm ein neuer Bitmap-Knoten für eine Textur erstellt, die von einem Material verwendet wird.

Mit dieser Aktion können Sie u. a. Folgendes tun:

* Eine [Bitmapressource](../../resources/bitmap-resource/bitmap-resource.md) wird für die vom Material verwendete Textur erstellt und in einem nach dem Material benannten Ordner unter einem Ordner &quot;Resources&quot; abgelegt.
* Im ausgewählten Diagramm wird ein [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)-Knoten für diese Bitmapressource erstellt und automatisch mit einem [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)-Knoten verbunden, der nach der Materialeigenschaft konfiguriert ist und diese Texturen verwendet.

Wenn eine für die Materialeigenschaft &quot;*&quot; konfigurierte Ausgabe bereits vorhanden ist* im Diagramm, werden *keine Knoten erstellt* und nur die Bitmapressourcenerstellung ausgeführt.

Beispiel: Wenn eine Textur für die Eigenschaft &quot;Grundfarbe&quot; in ein Diagramm extrahiert wird, das bereits einen Ausgabeknoten hostet, der für &quot;Grundfarbe&quot; konfiguriert ist, werden im Diagramm keine Knoten erstellt.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Textur in Diagramm extrahieren - Aktion im Eigenschaften-Dock](../../assets/extractTextureAction.png "Textur in Diagramm extrahieren - Aktion im Eigenschaften-Dock"){zoomable="yes"}

Aktion für Materialeigenschaft im Eigenschaften-Dock

</td>
<td style="border: 0;" valign="top">

![Textur in Diagramm extrahieren - Dialogfeld &quot;Zieldiagramm auswählen&quot;](../../assets/extractTextureSelectGraph.png "Textur in Diagramm extrahieren - Dialogfeld &quot;Zieldiagramm auswählen&quot;"){zoomable="yes"}

Dialogfeld &quot;Zieldiagramm auswählen&quot;

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

![Ergebnis der Texturextraktion](../../assets/extractTextureResult.png "Ergebnis der Texturextraktion"){zoomable="yes"}

Ergebnis der Texturextraktion

+++Demonstration
![Textur in Diagramm extrahieren - Demonstration](../../assets/extractTextureToGraph.gif "Textur in Diagramm extrahieren - Demonstration"){zoomable="yes"}



+++

Die Aktion &quot;Textur als Ressource extrahieren&quot; erstellt nur eine Bitmapressource für die vom Material verwendete Textur und platziert sie in einem Ordner, der nach dem Material benannt ist, und zwar in einem Ordner &quot;Ressourcen&quot;.

>[!NOTE]
>
> Für Formate mit *eingebetteten Texturen* (z. B.: USDZ), muss die Textur extrahiert und auf die Festplatte kopiert werden. Dies führt zu einem zusätzlichen Schritt, in dem Sie die Stelle auswählen, an der die Textur extrahiert werden soll.

## Wert extrahieren

Die Aktion &quot;Wert in Diagramm extrahieren&quot; erstellt einen neuen [Wertprozessor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)-Knoten in einem vorhandenen Diagramm für einen Materialeigenschaftswert.

Mit dieser Aktion können Sie u. a. Folgendes tun:

* Im ausgewählten Diagramm wird ein Knoten vom Typ [Wertprozessor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) für diesen Eigenschaftswert erstellt und automatisch mit einem Knoten vom Typ [Ausgabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) verbunden, der nach dieser Materialeigenschaft konfiguriert ist.
* Im Funktionsdiagramm [Substance des Werteprozessorknotens &#x200B;](../../function-graphs/function-graphs.md) wird ein [Konstantenknoten](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md), der dem Werttyp entspricht, erstellt und auf den extrahierten Wert als Ausgabe des Diagramms festgelegt.

Wenn eine für die Materialeigenschaft *konfigurierte Ausgabe bereits vorhanden ist* im Diagramm, werden *keine Knoten erstellt*.

Beispiel: Wenn Sie einen Wert für die Eigenschaft &quot;Anisotropie-Ebene&quot; in ein Diagramm extrahieren, das bereits einen Ausgabeknoten hostet, der für &quot;Anisotropie-Ebene&quot; konfiguriert ist, werden im Diagramm keine Knoten erstellt.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Wert in Diagramm extrahieren - Aktion im Eigenschaftendock](../../assets/extractValueAction.png "Wert in Diagramm extrahieren - Aktion im Eigenschaftendock"){zoomable="yes"}

Aktion für Materialeigenschaft im Eigenschaften-Dock

</td>
<td style="border: 0;" valign="top">

![Wert in Diagramm extrahieren - Dialogfeld &quot;Zieldiagramm auswählen&quot;](../../assets/extractValueSelectGraph.png "Wert in Diagramm extrahieren - Dialogfeld &quot;Zieldiagramm auswählen&quot;"){zoomable="yes"}

Dialogfeld &quot;Zieldiagramm auswählen&quot;

</td>
<td style="border: 0;" valign="top">

![Wert in Diagramm extrahieren - Konstantenknoten in der Funktion des Werteprozessorknotens](../../assets/extractValueResult2.png "Wert in Diagramm extrahieren - Konstantenknoten in der Funktion des Werteprozessorknotens"){zoomable="yes"}

Konstanter Knoten in der Funktion des Werteprozessorknotens

</td>
</tr>
</table>

![Ergebnis der Wertextraktion](../../assets/extractValueResult.png "Ergebnis der Wertextraktion"){zoomable="yes"}

Ergebnis der Wertschöpfung

+++Demonstration
![Wert in Diagramm extrahieren - Demonstration](../../assets/extractValueToGraph.gif "Wert in Diagramm extrahieren - Demonstration"){zoomable="yes"}



+++

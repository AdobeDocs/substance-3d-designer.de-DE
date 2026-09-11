---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/interface/2d-view/color-sampler.html"
breadcrumb-title: ''
description: Verwenden Sie das Sampler-Farbwerkzeug in der 2D-Ansicht, um Farben aus Texturen für eine präzise Farbübereinstimmung aufzunehmen.
helpx_creative_field: ""
helpx_description: Designer > Interface > 2D view > Color sampler tool
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbaufnahme-Werkzeug
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# Farbaufnahme-Werkzeug

![Farbaufnahme-Werkzeug](../../../assets/color-sampler-demo.png "Farbaufnahme-Werkzeug"){zoomable="yes"}

Mit dem Color Sampler-Tool können Sie <b>den Wert eines bestimmten Pixels</b> in der [2D-Ansicht](../../../interface/2d-view/2d-view.md) verfolgen, während Sie Parameter anpassen oder Knoten wechseln.

Es platziert eine Nadel im Viewport und tastet die Farbe und Position des Pixels an dieser Position ab.

## Verwenden des Werkzeugs

Führen Sie die folgenden Schritte aus, um auf das Tool zuzugreifen und es zu verwenden:

1. Klicken Sie in der Datasymbolleiste auf die Schaltfläche ![](../../../assets/color-sampler-information-button.png) <b>2D-Ansicht</b>, um das Informationsdock und die Symbolleiste zu öffnen.
1. Klicken Sie in der Informationssymbolleiste auf die Schaltfläche ![](../../../assets/color-sampler-tool-icon.png) <b>Sampler-Farbwerkzeug</b>.
1. Klicken Sie im Viewport auf das Pixel, das Sie aufnehmen möchten, um eine ![](../../../assets/color-sampler-pin-icon.png) <b>Nadel</b> zu platzieren.
1. Prüfen Sie die Stichprobenwerte im Abschnitt &quot;Spezielle Daten&quot; im Informationsdock.
1. Wenn Sie mit dem Tool fertig sind, klicken Sie auf die Schaltfläche ![](../../../assets/color-sampler-remove-pin.png) <b>Löschen</b>, um die Nadel vom Viewport zu entfernen.\
   Sie können die Nadel auch entfernen, indem Sie auf RMB klicken und die Aktion &quot;Löschen&quot; im Kontextmenü auswählen.

Hier ist eine Demonstration des Werkzeugs in Aktion:

![Farbaufnehmer: mit dem Tool](../../../assets/color-sampler-demo.gif "Farbaufnehmer: Verwenden des Tools "){zoomable="yes"}

*Zum Vergrößern klicken*

+++Kopieren der aufgenommenen RGBA-Werte
Sie können die aufgenommenen Werte kopieren, indem Sie auf RMB auf der Nadel klicken und die Aktion &quot;RGBA-Werte kopieren&quot; im Kontextmenü auswählen.

Die kopierten Werte können mithilfe einer Farbminiatur </b> <b> in Parameter eingefügt werden.

Die Farbminiaturen im Informationsbedienfeld können auch direkt auf die Farbminiaturen dieser Parameter gezogen und abgelegt werden.

![Farbaufnehmer: RGBA-Werte kopieren](../../../assets/color-sampler-demo-copy-rgba-values.gif "Farbaufnehmer: RGBA-Werte kopieren"){zoomable="yes"}



*Zum Vergrößern klicken*

+++

## Aufgenommene Informationen

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Die Informationen sind in drei Typen und zwei Formate unterteilt.

* <b>Aufgenommene Werte</b>, die in jedem der RGBA-Kanäle des Bildes gespeichert sind:\
  Variierend\* / Gleitkomma
* <b>Aufgenommene Farbe</b> in der HSV-Darstellung:\
  8-Bit-Ganzzahl/Gleitkomma
* <b>Position</b> des Pixels in Pixel und normalisiertem Bildbereich:\
  Ganzzahl / Gleitkomma

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Aufgenommene Informationen](../../../assets/color-sampler-information.png "Aufgenommene Informationen"){zoomable="yes"}

</td>
</tr>
</table>

Der Wert hängt von der im Bild verwendeten Bittiefe ab. In einem Substance-Graf wird die Bittiefe durch das <b>Ausgabeformat</b> gesteuert. [Basisparameter](../../../compositing-graphs/graph-parameters/graph-parameters.md).

Die verfügbaren Bittiefen sind:

* <b>8-Bit-Ganzzahl:</b> 256 Werte für die Ganzzahl von 0 bis 255.
* <b>16-Bit-Ganzzahl:</b> 65.536 Ganzzahl-Werte von 0 bis 65.535.
* <b>HDR. niedrige Genauigkeit (16 Bit)</b>: Ein Fließkommawert, der mit 16-Bit codiert ist.
* <b>HDR. hohe Genauigkeit (32 Bit)</b>: Ein Fließkommawert, der mit 32-Bit codiert ist. Dies ist die höchste in Designer verfügbare Präzision.

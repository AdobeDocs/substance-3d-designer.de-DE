---
helpx_url: ""
breadcrumb-title: ''
description: Mit dem Popup "Versatz" können Sie den Versatz und die Tesselierung, die auf Gitter in einer 3D-Szene angewendet wurden, schnell anpassen.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Ansicht - Versatz-Popup
user-guide-description: ''
user-guide-title: ''
source-git-commit: c7b3b375144c8b58a8e7a7a408895a23e9bd1143
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---


# Versatz-Popup

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>Das in der 3D-Ansichtssymbolleiste verfügbare Popup "Versatz" bietet direkte Steuerelemente zum Versatz und zur Tesselierung von Gittern.</p>
            <p>Es gibt drei Parameter:<ul>
                <li>Höhenskala</li>
                <li>Höhenebene</li>
                <li>Tessellierung</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/3d-view-displacement-popup-mograph.gif" alt="Versatz-Popup in der 3D-Ansicht" />
        </td>
    </tr>
</table>

## Höhenskala

Die maximale Entfernung des Versatzes für die Gitterscheitelpunkte entlang ihrer Normalen in Szeneneinheiten.<br>
Dies ist die zurückgelegte Strecke für einen Wert von 1,0 in der Karte des Heights.

Wenn ein Substance-Diagramm mit einem Material verbunden ist und dieses Diagramm einen [Ausgabeknoten](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) mit
<code>heightScale</code> verwendet wird, ist der Materialskalierungsparameter im Popup *deaktiviert* für dieses Height.
da es derzeit durch den Graphen gesteuert wird.

>[!TIP]
> 
>Verwenden Sie den Knoten [Height zu normalen weltweiten Einheiten ](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md), und der Parameter &#39;Height-Tiefe&#39; muss mit dem Wert &#39;Height-Skalierung&#39; übereinstimmen.
>, um die richtige Schattierung bei der Verwendung von Versatz sicherzustellen.

## Höhenebene

Der Graustufenwert in der Height-Map, der als *Mittelpunkt* für das Versatz-Height verwendet wird.
d. h. der als 0,0-Höhenangabe verwendete Schwellenwert.

Werte unter diesem Schwellenwert führen dazu, dass Scheitelpunkte rückwärts verschoben werden, während Werte über dem Schwellenwert zu
Scheitelpunkte, die nach vorn verschoben werden.

## Tessellierung

Bei der Tesselierung werden einzelne Gitterflächen unterteilt, indem ein Scheitelpunkt auf ihren Segmenten hinzugefügt und dann
alle Scheitelpunkte auf einen neuen Scheitelpunkt in ihrer Mitte, sodass 1 Fläche zu **6** wird.

Der Parameter legt fest, wie oft Gesichter rekursiv unterteilt werden sollen.

Der *Bereich* des Tesselationsparameters variiert je nach dem derzeit verwendeten *Renderer*: sie kann angewendet werden
je Masche oder je Material.

### Pro Gitter

Bei Verwendung des Renderers [Rasterizer](../3d-renderers/3d-renderers.md#rasterizer) oder [GPU-Pathtracer](../3d-renderers/3d-renderers.md#gpu-pathtracer) weist jedes Mesh-Objekt in der Szene ein *separates Objekt auf.*
Unterteilungswert.

Unterteilung ist kontextabhängig: so optimiert, dass nur Flächen mit einem *ungleichmäßigen Height-Wert* oder
Eine *nicht-flache Height-Map* wird unabhängig vom Parameterwert unterteilt.

### Pro Material

Wenn Sie den Renderer [OpenGL](../3d-renderers/3d-renderers.md#opengl) verwenden, weist jedes Material in der Szene einen Unterteilungswert *Separat* auf, der
wird auf *alle Gesichter angewendet, die dieses Material verwenden*.

Unterteilung ist nicht kontextabhängig: die Flächen werden unabhängig von ihrem Strom um die angegebene Zeit unterteilt
Height oder Struktur.

## Visualisierung der Tesselierung

Sie können das Ergebnis der Tesselierung anzeigen, indem Sie das **Drahtgitter** des Gitters überprüfen.<br>
Die Schritte zum Anzeigen des Drahtgitter für jeden Renderer werden im Folgenden beschrieben:

### Rastereffekt/GPU-Pathtracer

Verwenden Sie die <img src="../3d-view.resources/3d-view-scene-toolbar-render-settings.png" width="22" /> **Rendereinstellungen**
 Schaltfläche, gehen Sie dann im Eigenschaftendock zu **Rendereinstellungen > Diagnosemodus** und wählen Sie das **Drahtgitter
 (World Space)**-Option.

### OpenGL

Verwenden Sie die <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **Drahtgitter**
 klicken.

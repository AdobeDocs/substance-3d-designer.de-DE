---
helpx_url: ""
breadcrumb-title: ''
description: Mit dem Popupfenster "Versatz" können Sie schnell den Versatz und die Tessellation anpassen, die Meshs in einer 3D-Szene zugewiesen wurden.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Ansicht - Popup "Versatz"
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---


# Versatz-Popup

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>Das in der Datensymbolleiste verfügbare Popup "Versatz" bietet direkte Steuerelemente zum Versatz und zur Tessellation von Meshs.</p>
            <p>Es gibt drei Parameter:<ul>
                <li>Höhenskala</li>
                <li>Höhenebene</li>
                <li>Tessellierung</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/displacement-01.gif" alt="Versatz-Popup in der 3D-Ansicht" />
        </td>
    </tr>
</table>

## Höhenskala

Die maximale Entfernung des Versatzes für die Scheitelpunkt des Meshs in Szene.<br>
Dies ist die zurückgelegte Strecke für einen Wert von 1,0 auf der Höhen-Map.

Wenn ein Substance-Graf mit einem Material verbunden ist und dieser Graf einen [Ausgabeknoten](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) mit
<code>heightScale</code> Verwendung, dann ist der Height-Skalierungsparameter im Popup *deaktiviert* für dieses Material
da es derzeit vom Graf angetrieben wird.

>[!TIP]
> 
>Verwenden Sie den Knoten [Height zu normalen weltweiten Einheiten &#x200B;](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md), und der Parameter &#39;Height-Tiefe&#39; muss mit dem Wert &#39;Height-Skalierung&#39; übereinstimmen.
>, um die richtige Schattierung bei der Verwendung von Versatz sicherzustellen.

## Höhenebene

Der Graustufenwert auf der Höhen-Map, der als *Mittelpunkt* für das Versatz-Height verwendet wird.
d. h. der als 0,0-Höhenangabe verwendete Schwellenwert.

Werte unterhalb dieses Schwellenwerts führen dazu, dass Scheitelpunkt rückwärts verschoben werden, während Werte oberhalb des Schwellenwerts
Scheitelpunkt werden nach vorne verdrängt.

## Tessellierung

Bei der Tessellation werden die Flächen der einzelnen Mesh unterteilt, indem ein Scheitelpunkt zu den Segmenten hinzugefügt und anschließend
alle Scheitelpunkt auf einen neuen Scheitelpunkt in ihrer Mitte, sodass 1 Fläche zu **6** wird.

Der Parameter legt fest, wie oft Flächen rekursiv unterteilt werden sollen.

Der *Bereich* des Tessellation-Parameters variiert je nach dem derzeit verwendeten *Renderer*: sie kann angewendet werden
pro Mesh oder pro Material.

### Pro Mesh

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

Verwenden Sie die <img src="../3d-view.resources/3d-view-18.png" width="22" /> **Rendereinstellungen**
 Schaltfläche, gehen Sie dann im Eigenschaftendock zu **Rendereinstellungen > Diagnosemodus** und wählen Sie das **Drahtgitter
 (World Space)**-Option.

### OpenGL

Verwenden Sie die <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **Drahtgitter**
 klicken.

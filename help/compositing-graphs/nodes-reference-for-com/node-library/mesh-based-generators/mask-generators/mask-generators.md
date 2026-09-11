---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators.html"
breadcrumb-title: ''
description: Greifen Sie in Substance 3D Designer auf Maskengenerator zu, um Masken basierend auf der Geometrie und den Eigenschaften des Meshs zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maskengeneratoren
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# Maskengeneratoren

Diese Kategorie enthält eine Auswahl an schwarz-weiß-weiße Maske-erzeugenden Knoten. Basierend auf durch Baking erzeugte Map-Informationen erzeugen sie Masken, die dann verwendet werden können, um Materialien und andere Effekte miteinander zu vermischen. Diese Knoten ähneln [Intelligente Masken](https://experienceleague.adobe.com/de/docs/substance-3d-painter/using/features/smart-materials-and-masks) und [Generatoren](https://experienceleague.adobe.com/de/docs/substance-3d-painter/using/content/creating-custom-effects/generators) im Substance Painter.

Für alle diese Knoten sind [durch Baking erzeugte Map,](../../../../../bakers/bakers.md) erforderlich, da ohne [durch Baking erzeugte Map](../../../../../bakers/bakers.md) kein großes Ergebnis erzielt werden kann.

Die beabsichtigte Hauptverwendung besteht darin, diese Maskengeneratoren mit [Mehrkanal-Materialien](../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/material-filters.md) zu verwenden. Nachdem eine Maske generiert wurde, wird sie als Mischmaske für [Material Überblendung](../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md) verwendet.

Einige interessante Knoten in dieser Kategorie sind:

* [Tropfender Rost](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dripping-rust/dripping-rust.md)
* [Edge Damages](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md)
* [Von unten nach oben](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md)
* [Maskenbildner](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/mask-builder/mask-builder.md)

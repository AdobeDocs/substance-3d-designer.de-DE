---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: Erfahren Sie, wie FXMaps in Substance 3D Designer funktionieren, um Funktionsdiagramme auf Texturen anzuwenden und prozedurale Effekte zu erzielen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > How it works
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: So geht‘s
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---


# So geht‘s

Um diese leistungsstarke Funktion zu beherrschen, ist es wichtig zu wissen, wie ein FX-Map-Diagramm funktioniert.

Ein FX-Map-Diagramm kann einen oder mehrere der drei FX-Map-Knotentypen enthalten: Quadrant, Iterate und Switch. Der Knoten, den Sie am häufigsten verwenden werden, ist der Quadrant, mit dem Knoten &quot;Iterieren&quot; (Iterate), eine knappe Sekunde.

Der Knoten &quot;Parametersatz&quot; ist der Hauptbeweger von FX-Maps. Es erstellt das Kernbereich-Quad-Tree-Diagramm, auf das sich FX-Maps verlassen, aber es wird nicht als eins angezeigt. Visuell ist das Quad-Tree-Diagramm in Form einer Markov-Kette dargestellt.

Beim Rendern der FX-Map wird das vereinfachte FX-Map-Diagramm so &quot;ausgepackt&quot;, dass es wie das große baumartige Diagramm aussieht. Die Maschine &quot;geht&quot; den gesamten Quad-Baum, arbeitet von oben nach unten, dann von links nach rechts.

FX-Map-Knoten kopieren und fügen ihre Bilder nicht blind ein. Wenn jedes Bild gerendert wird, werden alle dynamischen Funktionen, die es hat, ausgeführt. Die Funktionen wirken sich auf jedes Bild aus, das vom Knoten gerendert wird. Sie können daher jedem einzelnen Bild einen zufälligen Drehungs- oder Skalierungsfaktor oder eine Reihe anderer Anpassungen zuweisen.

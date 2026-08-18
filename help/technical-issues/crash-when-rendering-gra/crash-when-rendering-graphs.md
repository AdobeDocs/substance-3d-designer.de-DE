---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/crash-when-rendering-graphs.html"
breadcrumb-title: ''
description: Beheben Sie Abstürze beim Rendern von Graphen in Substance 3D Designer und finden Sie Lösungen, um sie zu verhindern.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Crash when rendering graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Absturz beim Rendern von Graphen
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# Absturz beim Rendern von Graphen

Auf dieser Seite werden Abstürze aufgelistet, die während des Renderings von Diagrammen in Substance 3D Designer auftreten, und es werden Schritte zur Fehlerbehebung für die einzelnen Diagramme angeboten.

## TDR (nur Windows)

<b>[![(Fehler)](../../assets/error.svg)](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) Problem</b>

Der Zeitgeber <b>Timeout Detection &amp; Recovery (TDR)</b> des Systems ist *zu kurz*, damit Substance 3D Designer seine aktuellen Berechnungen abschließen kann, bevor der Grafiktreiber *neu gestartet wird*.

Die von Substance 3D Designer ausgeführten Berechnungen können sehr intensiv sein und die Grafiktreiber in einem Maße verwenden, in dem *eine Weile nicht auf das Betriebssystem reagiert*.\
Als Stabilitäts- und Sicherheitsmaßnahme startet das Betriebssystem *den Grafiktreiber* neu, wodurch die Berechnungen verkürzt werden und Substance 3D Designer *abstürzt*.

<b>![(tick)](../../assets/check.svg) Empfohlene Schritte</b>

Die TDR-Zeitgeberwerte müssen *erhöht* sein, um solche Abstürze zu verhindern. Sie können dies tun, indem Sie die Anweisungen in [dieser Seite](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) der Substance 3D Painter-Dokumentation befolgen, die auch für Substance 3D Designer gelten.

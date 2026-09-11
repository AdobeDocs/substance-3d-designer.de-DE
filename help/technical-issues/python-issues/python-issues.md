---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/technical-issues/python-issues.html"
breadcrumb-title: ''
description: Beheben Sie Python-Skriptprobleme in Substance 3D Designer, einschließlich Plug-in- und API-Problemen.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Python issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Python-Probleme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Python-Probleme

Auf dieser Seite werden technische Probleme im Zusammenhang mit der [Python-API](../../scripting/scripting.md) von Substance 3D Designer sowie in Python implementierte Funktionen aufgelistet und Schritte zur Fehlerbehebung für die einzelnen Funktionen angeboten.

Zu den in Python implementierten Funktionen gehören die [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Senden an](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)-Aktionen in der Symbolleiste von [Explorer](../../interface/the-explorer-window/the-explorer-window.md) sowie das Tool zum Entfernen nicht verwendeter Knoten in Diagrammen.

## Das Modul &quot;QtForPython&quot; kann nicht geladen werden

<b>![(Fehler)](../../assets/error.svg) Problem </b>

Das Python-Modul &quot;QtForPython&quot; kann nicht geladen werden. Dies führt zu fehlenden Features, die in Python implementiert sind, wie z. B. die Aktionen [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Senden an](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) in der Symbolleiste von [Explorer](../../interface/the-explorer-window/the-explorer-window.md) sowie das Tool zum Entfernen nicht verwendeter Graf in Knoten.

Darüber hinaus können viele [Python-Plug-ins](../../scripting/plugin-basics/plugin-basics.md) nicht geladen werden oder funktionieren nicht wie erwartet.

<b>![(tick)](../../assets/check.svg) Empfohlene Schritte</b>

Es besteht wahrscheinlich ein Konflikt zwischen der Installation von QtForPython durch Designer und ihren Abhängigkeiten und einer vorhandenen Installation auf dem System.

Entfernen Sie alle anderen Systeminstallationen von [QtForPython](https://doc.qt.io/qtforpython-5/index.html) ([PySide2](https://pypi.org/project/PySide2/)) und [Shiboken2](https://pypi.org/project/shiboken2/).

Anstelle einer systemweiten Installation von QtForPython können Sie auch Python *virtuelle Umgebungen* oder einen *Paketmanager* wie [Rez](https://github.com/AcademySoftwareFoundation/rez) verwenden.

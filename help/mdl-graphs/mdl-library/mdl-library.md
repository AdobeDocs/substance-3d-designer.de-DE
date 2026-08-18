---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/mdl-library.html"
breadcrumb-title: ''
description: Greifen Sie in Substance 3D Designer auf die Materialdefinitionssprachbibliothek zu, um benutzerdefinierte Materialien zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > MDL library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL-Bibliothek
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# MDL-Bibliothek

Auf dieser Seite wird die Bibliothek mit Inhalten für [MDL-Grafiken](../../mdl-graphs/mdl-graphs.md) und Materialien angezeigt, die in Substance 3D Designer enthalten sind. Außerdem wird erläutert, wie benutzerdefinierte Inhalte in der [Bibliothek](../../interface/the-library/the-library.md) installiert und verwaltet werden.

## MDL-Inhalte in der Bibliothek

In MDL-Graphen verwendbare Knoten sind im Abschnitt <b>mdl</b> der [Bibliothek](../../interface/the-library/the-library.md) verfügbar. Die Knoten sind nach dem MDL-Modul, in dem sie definiert sind, in Filtern angeordnet.\
Wenn Module in Unterordnern gespeichert sind, wird diese Hierarchie *gespiegelt* in der Bibliothek als *Kategorien*.

Dieser Abschnitt enthält Inhalte aus den folgenden Quellen:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Integrierte Inhalte.

Designer umfasst MDL-Module, die grundlegende Bausteine für das Erstellen von MDL-Grafiken sowie vollständige, gebrauchsfertige Materialdefinitionen enthalten.

Dieser Inhalt wird an diesem Speicherort unter dem Installationsverzeichnis gespeichert: `./resources/view3d/iray/`

### Benutzerdefinierter Inhalt

Zusätzlich zum integrierten Inhalt können Sie der Bibliothek *Ihre eigenen* MDL-Module hinzufügen.

Tatsächlich werden alle MDL-Module, die unter den im Abschnitt <b>MDL</b> der [Projekteinstellungen](../../interface/preferences-window/project-settings/project-settings.md) aufgeführten Verzeichnissen gefunden wurden, diesem Abschnitt *kumulativ* in allen Projektdateien hinzugefügt.

### NVIDIA vMaterials

Wenn die Bibliothek [vMaterials](https://developer.nvidia.com/vmaterials) von NVIDIA installiert ist, wird sie *automatisch* in der Bibliothek unter der *eigenen Kategorie* hinzugefügt.

</td>
<td style="border: 0;" valign="top">

![MDL-Ressourcen in Bibliothek](../../assets/mdl-library.png "MDL-Ressourcen in Bibliothek")

*&quot;mdl&quot;-Abschnitt in der Bibliothek, die vMaterials-Bibliothek und der benutzerdefinierte Inhalt werden eingerahmt*

</td>
</tr>
</table>

## MDL-Inhalte in der 3D-Ansicht

Alle in der Bibliothek verfügbaren MDL-Module können in der [3D-Ansicht](../../interface/3d-view/3d-view.md) verwendet werden, wenn der Iray-Renderer verwendet wird.

Öffnen Sie das Menü <b>Materialien</b> und das Untermenü *eines* Szenenmaterials, um die verfügbaren MDL-Module zu durchsuchen. Die Listen umfassen:

* Integrierte Inhalte.
* Benutzerdefinierter Inhalt
* NVIDIA [vMaterials](https://developer.nvidia.com/vmaterials)
* [MDL-Diagramme geladen](../../mdl-graphs/mdl-graphs.md)

![MDL-Materialien in der 3D-Ansicht](../../assets/mdl-apply-in-3dview-material-list.png "MDL-Materialien in der 3D-Ansicht")

*MDL-Materialien in der 3D-Ansicht*

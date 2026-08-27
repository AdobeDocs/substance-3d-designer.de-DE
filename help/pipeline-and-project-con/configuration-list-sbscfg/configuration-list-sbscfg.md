---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/pipeline-and-project-configuration/configuration-list-sbscfg.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie SBSCFG-Konfigurationslisten in Substance 3D Designer verwenden, um Projekteinstellungen und Vorgaben zu verwalten.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Configuration List - SBSCFG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Konfigurationsliste - SBSCFG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Konfigurationsliste - SBSCFG

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Die Konfigurationsdatei ist viel einfacher als die [Projektkonfigurationsdateien](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md), da sie nur eine Liste von Projekten sowie einen Modulkompatibilitätsmodus enthält. Sie dienen als übergeordnete Projekt-/Umgebungskonfigurationsliste als die einzelnen Projektdateien.

Sie können mehrere Konfigurationen für verschiedene Umgebungen haben. Diese Dateien können zusammen mit den SBSPRJ-Dateien unter Versionskontrolle gehalten werden.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![SBSCFG-Dateisymbol](../../assets/sbscfg.png "SBSCFG-Dateisymbol")

</td>
</tr>
</table>

## Konfigurationsdateien ändern

Diese Dateien sind einfach, können aber auf zwei verschiedene Arten geändert werden, genau wie die SBSPRJ-Dateien.

### In den Projekteinstellungen

Der hervorgehobene Abschnitt ist der Teil, der sich auf die Konfigurationsdateien bezieht. Sie fügen einfach weitere Projekte zur Liste hinzu, die in der oben definierten SBSCFG-Datei gespeichert sind.

![Projekteinstellungen](../../assets/config-ui.png "Projekteinstellungen")

### Externe Bearbeitung als XML

Für Windows <b>ist Notepad++</b> eine gute kostenlose Option, für macOS <b>Sublime Text</b> eine Alternative. Jeder Editor mit korrektem Einzug, reduziertem Abschnittsbereich und einer Syntaxhervorhebung erleichtert Ihnen das Leben erheblich.

Sobald Sie die SBSCFG-Datei in einem Editor geöffnet haben, sollten Sie ein relativ einfaches, strukturiertes Layout sehen, dessen Abschnitte der Benutzeroberfläche entsprechen.

```
<?xml version="1.0" encoding="UTF-8"?> 

<root> 

 <projects> 

  <projectfiles> 

   <size>1</size> 

   <_1 prefix="_"> 

    <path>custom_project.sbsprj</path> 

   </_1> 

  </projectfiles> 

 </projects> 

 <preferences> 

  <configuration> 

   <compatibilitymode>sbs_engine_v6</compatibilitymode> 

  </configuration> 

 </preferences> 

</root>
```


Beachten Sie, dass die Standard- und Benutzerprojekte nicht explizit aufgeführt sind und dass danach weitere Projekte definiert werden.

Im obigen Beispiel werden auch [relative Pfade](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) verwendet. Beachten Sie, dass sich die Logik für relative Pfade zwischen CFG- und PRJ-Dateien leicht unterscheidet: für CFG-Dateien wie oben **Sie sollten vor dem Pfad** nicht &quot;file:/&quot; eingeben. Stattdessen wird der Pfad lediglich an den Speicherort der CFG-Datei angehängt, in der er definiert ist.

## Entfernen der Standardbibliothek

Vorerst kann die Standardbibliothek nicht entfernt werden. Es ist wahrscheinlich ohnehin keine gute Idee, dies zu tun, da Sie viele Funktionen von Designer verlieren würden.

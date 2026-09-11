---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/pipeline-and-project-configuration.html"
breadcrumb-title: ''
description: Konfigurieren Sie Pipeline- und Projekteinstellungen in Substance 3D Designer, um Ihren Workflow und Ihre Ausgabe zu optimieren.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pipeline- und Projektkonfiguration
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Pipeline- und Projektkonfiguration

Substance 3D Designer verfügt über ein leistungsstarkes System zum Konfigurieren der Anwendung für die Pipelinenutzung. Über ein erweitertes System hierarchischer &quot;**Project**&quot;-Dateien kann die Anwendung sofort gemäß Studio- oder Projektstandards konfiguriert werden, wobei alle Konfigurationen und Bibliotheksinhalte unter Versionskontrolle stehen. Das Hauptziel des Systems besteht darin, alle Pipeline-relevanten Einstellungen zu zentralisieren, gleichzeitig jedoch mehrere Konfigurationen zu überschreiben und sich gegenseitig zu erweitern.

>[!WARNING]
>
> Dieses System ist nicht für einzelne Benutzer mit einfacheren Anforderungen gedacht, sondern für *Studios mit großen Projekten und Teams* und einem höheren Organisationsbedarf. Um dieses System in vollem Umfang nutzen zu können, empfiehlt sich eine angemessene Planung und Vorbereitung sowie ein gewisses Maß an automatisierter Einrichtung!

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Hierarchie der Konfigurationsdateien

Designer verfügt über drei Ebenen oder Konfigurationsdateien, die jeweils einen anderen Zweck verfolgen. Unter Windows befinden sich alle Dateien in *~User\AppData\Local\Adobe\Adobe Substance 3D Designer.*

Die Abbildung veranschaulicht die Beziehung zwischen den verschiedenen Dateien im Standardsetup von Designer nach einer Neuinstallation.

</td>
<td style="border: 0;" valign="top">

![Hierarchie der Konfigurationsdateien](../assets/filestructureoverview.png "Hierarchie der Konfigurationsdateien")

</td>
</tr>
</table>

* <b>[User\_Preferences.XML](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)</b> enthält allgemeine Programmeinstellungen, von denen bis auf eine alle für Projekt-Pipelines nicht relevant sind. Diese Datei ist eindeutig und kann nicht ausgetauscht werden. Designer ist zur Verwendung dieser Datei hartcodiert.\
  Es enthält einen einzelnen Verweis auf eine Konfigurationsdatei.
* <b>[Default\_Configuration.SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)</b> kann gegen andere SBSCFG-Dateien mit unterschiedlichen Namen ausgetauscht werden, es kann jedoch nur eine SBSCFG-Datei gleichzeitig verwendet werden.\
  Es enthält mehrere Verweise auf Projektdateien. *Beachten Sie, dass diese Dateien für die Standardkonfiguration nicht explizit definiert, sondern hartcodiert sind!*
* <b>[Project.SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)</b> Dateien enthalten projektbezogene/Pipeline-relevante Einstellungen. Mehrere Projekte können in einer Hierarchie definiert werden, wobei das zuvor definierte Projekt überschrieben oder erweitert wird.

## Designer Pipeline-Einrichtung

Jeder Dateityp wird auf den untergeordneten Seiten dieser Seite ausführlicher erläutert, aber der kurze Überblick darüber, wie Sie idealerweise eine benutzerdefinierte Einrichtung für Designer definieren können, ist wie folgt:

1. <b>Identifizieren und gruppieren Sie die Einstellungen, die Ihren Projektdateien hinzugefügt werden sollen.</b> Das ist für jedes Studio anders und erfordert eine gewisse Planung!\
   In fast allen Fällen sollten mindestens zwei Projekte definiert werden: eine für globale, studioweite Standardeinstellungen (wie Standardvorlagen, Shader-Dateien, Baking-Einstellungen) und eine mit spezifischeren Inhalten wie Bibliotheksinhalten. Wenn verschiedene Projekte gleichzeitig ausgeführt werden, können Sie für jedes Projekt mehrere Projektkonfigurationen erstellen (also insgesamt 3 oder mehr).
1. <b>Erstellen Sie die entsprechenden [SBSPRJ-Dateien](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md), und platzieren Sie sie und ihren Inhalt in der Versionskontrolle.</b> Es wird dringend empfohlen, die Designer-Pipeline und den Bibliotheksinhalt von den eigentlichen Projektinhalten und Ressourcen (3D-Modelle, Texturen, Code) zu trennen, indem ein *separates Repository* dafür erstellt wird.
1. <b>Erstellen Sie eine [&#x200B; SBSCFG-Konfiguration](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)-Datei, in der alle Projektdateien aufgelistet sind, und platzieren Sie sie unter Versionskontrolle</b>. Wenn Sie mehrere Projekte haben, können Sie für jedes Projekt eine Konfiguration erstellen.
1. <b>Richten Sie die [User\_Preferences.xml](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) für jeden Benutzer so ein, dass er auf seine relevante Konfigurationsdatei verweist.</b>\
   Sie können dies von jedem Benutzer manuell erledigen lassen oder Sie können dies Skript erstellen, indem Sie Zeilen in ihre XML-Datei einfügen. [Weitere Informationen auf der entsprechenden Seite](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md).

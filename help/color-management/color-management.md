---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/color-management.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über das Farbmanagement in Substance 3D Designer, einschließlich Farbräumen, Profilen und Volltonfarben-Workflows.
helpx_creative_field: ""
helpx_description: Designer > Color Management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbmanagement
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1693'
ht-degree: 1%

---


# Farbmanagement

Auf dieser Seite werden die Funktionen und Einstellungen für das Farbmanagement in Substance 3D Designer erläutert.

Substance 3D Designer kann so konfiguriert werden, dass [OpenColorIO](https://opencolorio.org/) (OCIO) oder Adobe Color Engine (ACE) für das Farbmanagement verwendet wird. Dadurch können Sie *konsistente* Farbtransformationen und Bilddarstellung über mehrere Anwendungen hinweg durchführen.

In diesem Modus arbeitet Designer intern mit **linearen RGB**-Farben. Da 8 Bittiefen normalerweise nicht ausreichen, um Linearfarben darzustellen, wird empfohlen, mindestens **&#x200B; **&#x200B;16-bit** Tiefen für Farbtexturen im [Diagramm](../compositing-graphs/substance-compositing-graphs.md) zu verwenden.

>[!WARNING]
>
> Ein effektiver Farbmanagement-Workflow basiert auf der Arbeit mit einem korrekt *kalibrierten* Display. Es gibt Lösungen von Drittanbietern, um Ihren Monitor mithilfe spezieller Hardware für Ihre Arbeitsumgebung korrekt zu kalibrieren.
> 
> OpenColorIO-Benutzer sollten für ihre Monitore passende OpenColorIO-Farbräume verwenden.\
> Adobe ACE-Benutzer sollten sicherstellen, dass die in OS *ausgewählten ICC-Profile* mit *ihren* Monitoren übereinstimmen.

## Konfiguration

Die Farbmanagementeinstellungen können auf der Registerkarte &quot;[Projekte](../interface/preferences-window/project-settings/project-settings.md)&quot; des Dialogfelds &quot;[Voreinstellungen](../interface/preferences-window/preferences-window.md)&quot; konfiguriert werden. Sie können die folgenden Einstellungen festlegen:

### Farbmanagementmodus

|  |  |
| --- | --- |
| <b>Farbmanagement</b> | Mit dieser Einstellung können Sie die Modi [Legacy](../color-management/color-management.md), [OpenColorIO](#opencolorio) oder [Adobe ACE](#adobe-ace) für das Farbmanagement in Substance 3D Designer auswählen. *Standard: Veraltet* |

## OpenColorIO

### OpenColorIO-Konfiguration

Bei Verwendung des OpenColorIO-Modus für das Farbmanagement verwendet Designer die Informationen, die in einer <b>Konfigurationsdatei </b> (*\*.config*) gespeichert sind, um Farbtransformationen durchzuführen, Farbräume zu identifizieren und Standardwerte festzulegen.

Substance 3D Designer wird mit den folgenden Konfigurationen ausgeliefert:

* Substance: eine einfache Konfiguration mit gemeinsamen Farbräumen
* [ACES 1.0.3](https://github.com/hpd/OpenColorIO-Configs/tree/master/aces_1.0.3): die vollständige [Academy Color Encoding System](https://www.oscars.org/science-technology/sci-tech-projects/aces) (ACES)-Konfiguration mit vollem Funktionsumfang, ein Branchenstandard für Farbmanagement-Workflows

Sie finden diese Konfigurationsdateien im Ordner <b>Ressourcen > ocio</b> der Designer-Installationsdateien.

|  |  |
| --- | --- |
| <b>OpenColorIO-Konfiguration</b> | Mit dieser Einstellung können Sie die OpenColorIO-Konfigurationsdatei auswählen, die in Designer verwendet werden soll. Alternativ können Sie die OpenColorIO-Konfigurationsdatei mithilfe der OCIO-Umgebungsvariable festlegen.  Wenn sie vorhanden ist, ist die Konfigurationsdatei in Designer *gesperrt*. Es ist weiterhin möglich, Standardfarbräume und -transformationen zu ändern (siehe Einstellungen unten).  **Warnung:** Nach dem Hinzufügen der Umgebungsvariable empfehlen wir, Designer zu schließen, sich *von Ihrer Benutzersitzung im Betriebssystem abzumelden* und sich dann erneut anzumelden. Dadurch wird sichergestellt, dass die Umgebungsvariable beim Starten von Designer wirksam wird. Sie können auch die Befehlszeile verwenden, um eine temporäre Umgebungsvariable zu erstellen und Designer aus der *gleichen* Befehlszeilenumgebung zu starten.  *Standard: Substance* |
| **Benutzerdefinierte Konfigurationsdatei** | Wenn die Option **Benutzerdefiniert** in **OpenColorIO-Konfiguration** festgelegt ist, können Sie die *spezifische \*.config-Datei *auswählen, die als Konfigurationsdatei in diesem Feld verwendet werden soll.* Standard: festgelegt durch OpenColorIO-Konfigurationsdatei oder OCIO-Umgebungsvariable* |

### Standardwerte für den Bitmap-Farbraum

|  |  |
| --- | --- |
| <b>8-Bit-Bilder</b> | Legt den Standardfarbraum für 8-Bit-Bitmaps fest. *Standard: Durch OpenColorIO-Konfigurationsdatei* festgelegt |
| <b>16-Bit-Bilder</b> | Legt den Standardfarbraum für 16-Bit-Bitmaps fest. *Standard: Durch OpenColorIO-Konfigurationsdatei* festgelegt |
| <b>Gleitkommabilder</b> | Legt den Standardfarbraum für Gleitkomma-Präzisions-Bitmaps fest, z. B. *HDR*-Bilder in den Formaten *\*.exr *oder*\*.hdr*. *Standard: Durch OpenColorIO-Konfigurationsdatei* festgelegt |
| <b>Dateiname zum Erkennen des Farbraums verwenden</b> | Ermöglicht Designer das automatische Zuweisen eines Farbraums, wenn das *Suffix* eines Bitmap-Dateinamens *genau mit dem Kleinbuchstaben eines Farbraums übereinstimmt, der in der aktuellen OpenColorIO* Konfiguration *enthalten ist.* Beispiel: Eine Bitmapressource *mybitmap\_aces\_acescg.png* wird automatisch auf den Farbraum *ACES - ACEScg* festgelegt, und die entsprechende Transformation wird auf den Arbeitsfarbraum angewendet. *Standard: Aktiviert* |

### Anzeigestandard in 2D- und 3D-Ansicht

|  |  |
| --- | --- |
| <b>Standardanzeige für 2D- und 3D-Ansicht </b> | Legt den Standardfarbraum *display* für die Viewports [2D view](../interface/2d-view/2d-view.md) und [3D view](../interface/3d-view/3d-view.md) fest. *Standard: Durch OpenColor IO-Konfigurationsdatei* festgelegt |
| <b>Miniaturansichten farbverwalten</b> | Erlaubt Designer das automatische Transformieren des Knotens *Miniaturansichten* in den *Arbeitsfarbraum* im Diagramm. *Standard: Aktiviert* |

## Adobe ACE

### Farbeinstellungen

Bei Verwendung des Adobe ACE-Modus für das Farbmanagement verwendet Substance 3D Designer die in <b>ICC-Profilen</b> (*\*.icc / \*.icm*) gespeicherten Informationen, um Farbtransformationen durchzuführen und Farbräume zu identifizieren.

Designer wird mit einer Reihe von ICC-Profilen geliefert. Sie finden die Dateien für diese Profile im Ordner &quot;`resources > icc`&quot; der Designer-Installationsdateien.\
Sie können *Ihre eigenen* ICC-Profile hinzufügen, indem Sie diese Dateien im Ordner *Dokumente* für den aktuellen Systembenutzer am Speicherort `Adobe/Adobe Substance 3D Designer/icc` platzieren.

|  |  |
| --- | --- |
| <b>Arbeitsbereich</b> | Mit dieser Einstellung können Sie den Arbeitsfarbraum auswählen, um *Farbvorgänge* in Substance 3D Designer durchzuführen. *Standard: sRGB IEC61966-2.1* |
| <b>Renderpriorität</b> | Mit dieser Option können Sie steuern, wie Farben transformiert werden sollen, wenn sie sich außerhalb des Farbumfangs *des* Arbeitsfarbraums *befinden.**Standard: Relativ farbmetrisch* |

### Standardwerte für den Bitmap-Farbraum

|  |  |
| --- | --- |
| <b>8-Bit-Bilder</b> | Legt das ICC-Standardprofil für 8-Bit-Bitmaps fest. *Standard:* sRGB IEC61966-2.1 ** |
| <b>16-Bit-Bilder</b> | Legt das ICC-Standardprofil fest, das 16-Bit-Bitmaps verwendet. **Standard: *sRGB IEC61966-2.1*** |
| <b>Gleitkommabilder</b> | Legt das ICC-Standardprofil fest, das für Gleitkomma-Präzisionsbitmaps verwendet werden soll, z. B. *HDR*-Bilder in den Formaten *\*.exr *oder*\*.hdr*. *Standard: Raw (d. h. kein Profil angewendet)* |
| <b>Integrierte ICC-Profile verwenden, wenn verfügbar</b> | Ermöglicht Designer die Verwendung des in einer Bitmap eingebetteten ICC-Profils anstelle der oben aufgeführten Standardwerte. *Standard: Aktiviert* |

### Standardraum für 2D- und 3D-Ansicht-Anzeige

|  |  |
| --- | --- |
| <b>Standardanzeige für 2D- und 3D-Ansicht </b> | Legt den Standardfarbraum *display* für die Viewports [2D view](../interface/2d-view/2d-view.md) und [3D view](../interface/3d-view/3d-view.md) fest. *Standard:*** ICC-Profil für den Hauptbildschirm, vom Betriebssystem abgerufen &#x200B;**&#x200B;** |

### Diagrammanzeige

|  |  |
| --- | --- |
| <b>Miniaturansichten farbverwalten</b> | Wenn *aktiviert* ist, wandelt Designer die *Knoten-Miniaturansichten* in den aktuellen *Arbeitsfarbraum* um. *Standard:*** Nicht aktiviert &#x200B;**&#x200B;** |

## Legacy-Modus

Bei Verwendung des <b>Legacy</b>-Modus ist das Farbmanagement *deaktiviert* in Designer-

In diesem Modus verhalten sich Grafiken und Bilder genau so wie in früheren Versionen. Das bedeutet, dass Ihr Workflow aus früheren Versionen *völlig unberührt* ist, wenn diese Einstellung *unberührt* bleibt. Es gibt jedoch einige nützliche Ergänzungen:

Sie können <b>ACES sRGB</b> verwenden. *Tonzuordnung* in der <b>3D-Ansicht</b>, um der Ausgabe anderer Software, wie z. B. *[Unreal Engine](https://docs.unrealengine.com/en-US/Engine/Rendering/PostProcessEffects/ColorGrading/index.html)*, zu entsprechen.

Sie können einen Farbraum für *exportierte Bitmaps* festlegen, wie im Abschnitt [Exportieren von Ausgaben](#exporting-outputs) auf dieser Seite beschrieben. Folgende Farbräume sind verfügbar:

* sRGB
* Linear
* Raw

Im Legacy-Modus verwendet Designer den Arbeitsfarbraum <b>sRGB</b>, der von den meisten Bildschirmen wiedergegeben werden kann.

Wenn die Option &quot;Raw&quot; berücksichtigt wird, werden die Bilddaten *wie vorhanden* aus dem Diagramm geschrieben - d. h. unter Verwendung des Diagrammarbeitsfarbraums. Dies bedeutet, dass die Optionen <b>Raw</b> und <b>sRGB</b> zu der *gleichen Farbausgabe* führen.

Standardmäßig wird die Option &quot;sRGB&quot; für Ausgaben festgelegt, die *Farbinformationen* enthalten (z. B. Grundfarbe, emittierend), und die Option &quot;Raw&quot; ist für Ausgaben festgelegt, die *reine Daten* enthalten (z. B. Raueit, Metallisch, Height, Normal). Wie oben erläutert, führen diese Standardwerte effektiv zu denselben Farben und sind nur auf *zur Unterscheidung der Endverwendung* ihrer Ausgaben festgelegt.

Die Option <b>Linear</b> ist die Option *Nur*, die dazu führt, dass eine *Farbtransformation* auf das Bild angewendet wird. Sie kann nur für <b>Bilder der High Dynamic Range</b> (HDR) verwendet werden, die häufig *Gleitkomma-Präzision* (d. h. 16F oder 32F Bittiefe) im linearen Farbraum verwenden. Dadurch können diese Bilder in einer Vielzahl von Farbräumen und Produktionsumgebungen verwendet werden.

>[!NOTE]
>
> Weitere Informationen zu Bildexporten finden Sie auf der Seite [Exportieren von Bitmaps](../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) der Dokumentation.

## Importieren von Bitmaps

Sie können importierten und verknüpften Bitmaps einen <b>Farbraum</b> (OCIO) oder ein <b>ICC-Profil</b> (Adobe ACE) zuweisen.

Beim Importieren oder Verknüpfen von Bitmaps wird ein Farbraum oder ICC-Profil standardmäßig ** für die Bitmapressource festgelegt, wobei die Optionen im Abschnitt <b>Bitmapfarbraumstandard</b> der Registerkarte <b>Farbmanagement</b> in den [Projekteinstellungen](../interface/preferences-window/project-settings/project-settings.md) verwendet werden.

Sie können den Farbraum einer Bitmap jederzeit ändern. Die Option befindet sich in den <b>Eigenschaften</b> der Bitmap-Ressource.

>[!NOTE]
>
> **Nur OpenColorIO**
> 
> Insbesondere kann der **Dateiname** verwendet werden, um den entsprechenden Farbraum *automatisch* festzulegen. Beachten Sie, dass der Farbraumname im Dateinamen *mit dem Namen* in der OpenColorIO-Konfigurationsdatei übereinstimmen muss (z. B. *myImage\_utility - linear -srgb.png* wird auf *Utility - Linear - sRGB* (Farbraum) festgelegt.

![Einstellung des Bitmap-Farbraums](../assets/2019-3-0-bitmap-clr-space.png "Einstellung des Bitmap-Farbraums")

## Exportieren von Ausgaben

Bei Verwendung des Dialogfelds <b>Exportausgaben</b> ist es möglich, einen <b>Farbraum</b> (OCIO) zuzuweisen oder ein <b>ICC-Profil</b> (Adobe ACE) für *jede*-Ausgabe anzuhängen.\
Designer konvertiert *Bilder in die angegebenen Farbräume, bevor die Bilddateien gespeichert werden.*

![Dialogfeld für Exportausgaben](../assets/2019-3-0-clr-mgt-export-outputs.png "Dialogfeld für Exportausgaben"){width="512px"}

Sie können auch einen Farbraum (OCIO) zuweisen oder ein ICC-Profil (Adobe ACE) an Bilder *Gespeichert* aus der [2D-Ansicht](https://helpx.adobe.com/de/substance-3d/unlisted/documentation/sddoc/2d-view-deprecated-129368155.html) anhängen.

![2D-Exportoptionen anzeigen](../assets/2019-3-0-clr-mgt-save-image.png "2D-Exportoptionen anzeigen")

## 2D- und 3D-Ansichten

### Symbolleiste anzeigen

Sie können das *Farbmanagement* aktivieren/deaktivieren und die *Anzeigetransformation* für die Ansicht jederzeit mithilfe des Dropdown-Menüs in der Anzeigesymbolleiste ändern.

![Farbraumeinstellung in 2D-Ansicht](../assets/2019-3-0-clr-mgt-display-toolbar.png "Farbraumeinstellung in 2D-Ansicht"){width="512px"}

### Library HDRI-Umgebungen

Die mit Designer ausgelieferten HDRI-Umgebungen befinden sich im <b>linearen sRGB</b>-Farbraum.\
Wenn Sie eine OpenColorIO-Konfiguration verwenden, bei der der lineare Farbraum der Szene *nicht* Linear sRGB ist, z. B. die Konfiguration [ACES](https://acescentral.com/t/getting-started-with-aces/1372), zeigt die Umgebung *falsche Farben* an.

In diesem Fall sollte der Farbraum für Bibliotheks-HDRI-Umgebungen in den Umgebungseigenschaften, die im Menü des Bedienfelds &quot;3D-Ansicht&quot; <b>Umgebung</b> verfügbar sind, auf *manuell* festgelegt werden.

![Farbraumeinstellung der 3D-Ansichtsumgebung](../assets/2019-3-0-clr-mgt-hdri-env.png "Farbraumeinstellung der 3D-Ansichtsumgebung"){width="512px"}

## Farbkonvertierungsknoten

Die [Library](../interface/the-library/the-library.md) enthält die folgenden Knoten zum Ausführen von <b>Konvertierungen</b> in und aus dem ACEScg-Farbraum:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[Substance-Graph](../compositing-graphs/substance-compositing-graphs.md)

* ACEScg auf lineares sRGB
* Linear sRGB in ACEScg
* ACEScg auf sRGB
* sRGB in ACEScg

</td>
<td style="border: 0;" valign="top">

[Substance Funktions-Diagramm](../function-graphs/function-graphs.md)

* ACEScg auf lineares sRGB
* Linear sRGB in ACEScg

</td>
</tr>
</table>

Diese sind nützlich, wenn Sie mit Diagrammen arbeiten, die *ohne* Farbmanagement erstellt wurden, oder mit Materialien aus der [Substance 3D Assets](https://helpx.adobe.com/de/substance-3d/unlisted/assets.html)-Bibliothek.

![Farbkonvertierungsknoten in Bibliothek](../assets/2019-3-0-clr-mgt-nodes.png "Farbkonvertierungsknoten in Bibliothek"){width="512px"}

## Bekannte Einschränkungen

Die aktuelle Implementierung des Farbmanagements in Substance 3D Designer hat die folgenden Einschränkungen:

* Das Farbmanagement wird derzeit *nicht* in der [Python-API &#x200B;](../scripting/scripting.md) angezeigt.
* [OpenColorIO](https://opencolorio.org/) *Looks* werden *nicht* unterstützt.

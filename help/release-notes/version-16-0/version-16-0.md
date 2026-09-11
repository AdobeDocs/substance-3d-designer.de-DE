---
helpx_url: ""
breadcrumb-title: ''
description: Lesen Sie die Versionshinweise für Substance 3D Designer 16.0, um mehr über neue Funktionen, Verbesserungen und Fehlerbehebungen zu erfahren.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 16.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 16.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '2246'
ht-degree: 0%

---


# Version 16.0

Diese Version 16.0 bietet einen kreativeren Arbeitsablauf für Musterstreuung und -bearbeitung dank des neuen Shape-Splatters und der SDF-Knoten. Es unterstützt auch nativ OpenPBR und verbessert die Versatz-Einstellungen in der 3D-Ansicht.

*Freigabedatum: 14. April 2026*

<img src="./version-16-0.resources/version-16-0-banner.jpg" alt="Banner für Substance 3D Designer Version 16.0" style="margin-top: 32px; margin-bottom: 32px">

<a name="shape-splatter-v2-nodes"></a>

## Form splatter v2 knoten

### Neue Möglichkeiten zum Streuen von Formen

Die neuen [Shape-Splatter v2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md)-Knoten ermöglichen komplexe Streuungsverhalten, die bisher mit **weiteren Formverteilungsmethoden** (Poisson-Festplatte, Uniform), die standardmäßig *kollisionslos* sind, und steuern die *saubere Sammlung* von Formen in bestimmten Bereichen mit einer **Dichte-Map**.\
Erweiterte Benutzer können *benutzerdefinierte Distributionen* einrichten, die durch einen Funktions-Graf definiert sind.

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-poisson.gif" alt="Formspritzer v2: Poisson-Verteilung" /><br><i>Poisson-Verteilung</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-uniform.gif" alt="Formspritzer v2: Einheitliche Verteilung." /><br><i>Einheitliche Verteilung</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-density-map.gif" alt="Dichte-Map" /><br><i>Formspritzer v2: Dichte-Map</i>
        </td>
    </tr>
</table>

### 3D-Formen

Verstreute Formen sind jetzt **3D-Objekte**, die auf allen XYZ-Achsen verschoben, gedreht und skaliert werden können.

Verwenden Sie **einfache Grundformen** wie Würfel, Kugeln und Zylinder oder **komplexe benutzerdefinierte Formen**, die durch *Extrudieren einer Höhen-Map* oder Erstellen von *3D-SDF-Formen* gebildet werden. (Mehr dazu weiter unten)

Dadurch werden Streuungen ermöglicht, die dynamischer, vielfältiger und glaubwürdiger sind. Und jetzt ist es möglich, 3D-Formen für Variationen wiederzuverwenden, indem Sie sie spiegeln. (Wir sehen dich, Umweltkünstler!)

<table style="margin-top: 32px; margin-bottom: 32px; border: none">
    <tr style="border: 0">
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-3d-rotation.gif" alt="Formspritzer v2: Zufällige 3D-Drehung" /><br><i>Zufällige 3D-Drehung</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-shape-extrusion.gif" alt="Formspritzer v2: Formextrusion" /><br><i>Formextrusion</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-sdf.jpg" alt="Formspritzer v2: 3D-SDF-Formen" /><br><i>3D-SDF-Formen</i>
        </td>
    </tr>
</table>

### Companion-Knoten

Ähnlich wie die Shape-Splatter v1-Knotenfamilie verfügt Shape-Splatter v2 über eine eigene Kohorte von Begleitknoten.

[Shape Splater v2 Mapper](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md) Knoten ermöglichen die Projektion von Texturen auf die gestreuten 3D-Formen, mit Unterstützung für *triplanare Projektion* und *Material-IDs* für die Zuordnung mehrerer Texturen. Die Ergebnisse können global oder pro Form angepasst werden, um Textur-Offsets und Farbvariationen zu erreichen.\
Auch hier können erweiterte Benutzer *benutzerdefinierte Texturzuordnungen* einrichten, die durch ein Funktionsdiagramm definiert sind.

[Der Formspritzer v2 zum Maskieren von &#x200B;](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md) erstellt Masken für eine bestimmte Auswahl von Formen und/oder Material-IDs, wodurch eine granularere Verwendung von Formen im Graphen nachgelagert ermöglicht wird.

<table style="margin-top: 32px; margin-bottom: 32px; border: none">
    <tr style="border: 0">
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-tiling.gif" alt="Form Splint v2 Farbabbildung: Triplanare Kartierung" /><br><i>Triplanare Zuordnung</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-normal.gif" alt="Form Splint v2 Farbabbildung: Normale Zuordnung" /><br><i>Normale Zuordnung</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-matID-02.jpg" alt="Form Splint v2 Farbabbildung: Zuordnung pro Material-ID aus SDF-Formen" /><br><i>Zuordnung pro Material-ID aus SDF-Formen</i>
        </td>
    </tr>
</table>

### Rasteratlas

<table>
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>Benutzerdefinierte Muster können separat für den Shape-Splater v2-Knoten bereitgestellt oder in einen Rasteratlas verpackt werden, um schlankere und effizientere Workflows zu ermöglichen.</p><p>Packing-Muster werden durch die neuen <a href="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/grid-atlas-color/grid-atlas-color.md">Rasteratlas</a>-Knoten vereinfacht.</p>
        </td>
        <td style="text-align: right; width: 33%; margin-left: 32px; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/grid-atlas-color/grid-atlas-color.resources/grid-atlas-color-graph.png" alt="Rasteratlas-Farbknoten" />
        </td>
    </tr>
</table>

<a name="3d-sdf-nodes"></a>

### Materialprobe

<table style="border: none">
    <tr style="border: none">
        <td style="border: none; vertical-align: top">
            <p>Die <b>rostigen Bolzen</b> <a href="../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md">Materialprobe</a> ist verfügbar, um die Shape-Splater v2-Familie von Knoten und deren Funktionen zu springen.</p><p>Das Diagramm ist organisiert und mit Anmerkungen versehen, um Sie durch die Struktur, die Knoteneinstellungen und die Techniken zu führen.</p><p>Es ist auch <i>vollständig bearbeitbar</i>, sodass es als Sandbox verwendet werden kann, um ein praktischeres Verständnis der Werkzeuggruppe Shape Splater v2 zu erhalten. Du kannst beliebig viele Beispieldiagramme erstellen. Experimentiere einfach mit den Beispieldiagrammen.</p>
        </td>
        <td style="border: none; width: 20%; vertical-align: top; text-align: right">
            <img src="../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.resources/working-with-sdf-functions-material-sample.png" alt="Begrenzungsrahmenfunktion des 3D-Anzeigeknotens für SDF-Funktionen." />
        </td>
    </tr>
</table>

## 3D SDF-Knoten (Feld für vorzeichenbehaftete Abstände)

<table>
    <tr style="vertical-align: top; width: 75%; border: 0">
        <td style="border: 0">
            <p>Designer 16.0 bietet eine leistungsstarke Methode zum Generieren von 3D-Formen in einem Funktionsdiagramm mithilfe eines umfangreichen Knotenkatalogs für Authoring-SDF-Funktionen.</p><p>Vorzeichenbehaftete Abstandsfelder sind Darstellungen des Raums als Abstand zu mathematisch definierten Flächen. Sie können verwendet werden, um Formen mit zunehmender Komplexität zu definieren, da diese Flächen mit verschiedenen Operatoren transformiert und kombiniert werden.</p>
        </td>
        <td style="text-align: right; width: 25%; margin-left: 32px; border: 0">
            <img src="./version-16-0.resources/version-16-0-SDFFunctionsBreakdown.gif" alt="Formen mithilfe von SDF-Funktionen erstellen" />
        </td>
    </tr>
</table>

### Erstellen von 3D-SDF-Funktionen

SDF-Funktionen umfassen eine [neue Knotenfamilie](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions), die in vier Kategorien unterteilt ist:

* **Primitive** sind die grundlegenden Bausteine. Sie generieren einfache, anpassbare Formen mit einigen Steuerelementen, mit denen Sie sie nach Bedarf anpassen können.
* **Operatoren** kombinieren oder replizieren Formen auf einfache oder komplexe Weise, je nach Knoten: von einfachen booleschen Operatoren bis hin zu Morphen, Schalen und Symmetrien erweitern sie die Möglichkeiten, welche Art von 3D-Form erreicht werden kann, um ein Vielfaches
* Mit **Transformationen** können Sie Position, Drehung und Größe der Formen anpassen, wie Sie es erwarten und darüber hinaus mit Biegung, Verdrillung und Dehnung.
* Mit **Material**-Knoten können Sie einige grundlegende Materialattribute festlegen, z. B. Farbe und Material-ID, die von der [Shape-Splatter v2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md)-Familie von Knoten zum Maskieren oder Färben von Formen verwendet werden können.

>[!INFO]
> 
> Wechseln Sie zur Seite [Arbeiten mit SDF-Funktionen](../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md), um mit der Arbeit mit diesen Knoten zu beginnen.

<img style="display: block; margin: auto" src="../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.resources/working-with-sdf-mograph.gif" alt="SDF-Funktion" />

Leichte Knotenpunkte mit übersichtlichen und gut lesbaren Icons machen das Erstellen von 3D-SDF-Funktionen leichter, als du vielleicht denkst, vor allem mit dieser nächsten Erweiterung des Toolsets...

### 3D-Anzeigeknoten

Beim Erstellen von 3D-SDF-Funktionen müssen Sie die resultierenden Formen im 3D-Raum visualisieren. Der [3D-Betrachterknoten](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md) rendert 3D-SDF oder Schnittfunktionen als 3D-Szene mit anpassbaren Kamerasteuerungselementen, benutzerdefiniertem Umgebungslicht und Unterstützung für das Rendern von Basismaterialien. (Farbe, Raueit und Metallität)

Der Knoten enthält außerdem Features zum detaillierten Überprüfen der generierten Formen und zum Debuggen von Problemen: Separate Renderingdurchläufe (AOV), SDF-Isolinien und visuelle Helfer. (E.g. B. Anschnittfarben, Raster und Drehbögen)

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="width: 50%; border: 0">
        <td style="text-align: center; width: 50%; border: 0; padding: 15px">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-01.jpg" alt="Beispiel 1" />
        </td>
        <td style="width: 50%; border: 0; padding: 0">
            <table>
                <tr style="vertical-align: top; border: 0">
                    <td style="text-align: center; border: 0">
                        <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-02a.jpg" alt="Beispiel 1" />
                    </td>
                    <td style="text-align: center; border: 0">
                        <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-02b.jpg" alt="Beispiel 2" />
                    </td>
                </tr>
                <tr style="vertical-align: top; border: 0; background: transparent">
                    <td style="text-align: center; border: 0; background: transparent">
                        <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-02c.jpg" alt="Beispiel 3" />
                    </td>
                    <td style="text-align: center; border: 0; background: transparent">
                        <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-02d.jpg" alt="Beispiel 4" />
                    </td>
                </tr>
            </table>
    </tr>
</table>

<a name="openpbr-support"></a>

## Unterstützung für OpenPBR

[OpenPBR Surface](https://academysoftwarefoundation.github.io/OpenPBR/) ist eine Schattierung eines Oberflächengrafikmodells, das als Standard für Computergrafiken gedacht ist und in der Lage ist, die meisten Materialien genau zu modellieren.

Dieses Materialmodell wird jetzt in der gesamten Anwendung unterstützt, mit [dedizierten Shadern](../../interface/3d-view/material-properties/material-properties.md#openpbr) in unseren neuen Renderern (Rasterizer, GPU-Pathtracer) und dem OpenGL-Renderer.

<img style="display: block; margin: auto" src="./version-16-0.resources/OpenPBRShort.gif" alt="OpenPBR-Unterstützung in Substance 3D Designer und Vergleiche mit anderen DCCs" />

Beginnen Sie mit diesem weit verbreiteten Branchenstandard mit neuen Graf-Vorlagen, oder sehen Sie sich die integrierten Material-Beispiele an, die jetzt auf OpenPBR basieren.

<table style="border: none; margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="text-align: center; border: 0">
            <img src="./version-16-0.resources/version-16-0-openpbr-01.png" alt="Vorlagen für OpenPBR" />
        </td>
        <td style="text-align: center; border: 0">
            <img src="./version-16-0.resources/version-16-0-openpbr-02.png" alt="Beispiele für OpenPBR-Materialien" />
        </td>
    </tr>
</table>

Der OpenPBR-Shader ist jetzt die Standardeinstellung für die 3D-Ansicht und unterstützt nativ Graf aus Vorgängerversionen, indem er ältere PBR-Nutzungen den OpenPBR&#39;s zuordnet.

OpenPBR-Shader unterstützen mehr Effekte als die vorhandenen Shader, z. B. Thin Film und Thin Wall. Alle Effekte sind in Rastern (Rasterung, OpenGL) verfügbar, einschließlich der Refraktion endlich!

<table style="border: none;">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            Es ist auch einfacher, Arbeitsabläufe mit bestimmten Shadern synchron zu halten, da das neue <a href="../../compositing-graphs/graph-parameters/graph-parameters.md#attributes">-Materialmodell-Attribut </a> für Substance-Graf sicherstellt, dass die in der 3D-Ansicht angezeigten Graf den entsprechenden Shader für das Materialmodell des Grafen verwenden.
        </td>
        <td style="text-align: right; margin-left: 32px; border: 0">
            <img src="./version-16-0.resources/version-16-0-materialModel.png" alt="Beispiele für OpenPBR-Materialien" />
        </td>
    </tr>
</table>

>[!NOTE]
> 
>Das Attribut ist auch in veröffentlichten SBSAR-Dateien enthalten, um in Ihren Material-Workflow integriert zu werden.

<a name="displacement-popup"></a>

## Versatz-Steuerelemente in der 3D-Ansicht

Es ist jetzt schneller und einfacher, Versatz und Tessellation in der 3D-Ansicht anzupassen, mit direktem Zugriff in einem [neuen Versatz-Popup](../../interface/3d-view/displacement/displacement.md), das in der 3D-Ansicht-Symbolleiste verfügbar ist.

Passen Sie die **Height-Skalierung**, **Height-Ebene** und **Tessellation**-Werte an, ohne in den Material-Eigenschaften und in den Renderereinstellungen wiederholt zu werden.

Diese Steuerelemente stehen sowohl für die neuen Renderer (Rasterprogramm, GPU-Pathtracer) als auch für den OpenGL-Renderer zur Verfügung.

<img style="display: block; margin: auto" src="../../interface/3d-view/displacement/displacement.resources/3d-view-displacement-popup-mograph.gif" alt="Versatz-Popup in der 3D-Ansicht" />

Wenn die Szene mehrere Material enthält, wählen Sie das Objekt der Szene aus, das Sie zuvor anpassen möchten, indem Sie <code>Umschalttaste gedrückt halten.</code> und klicken (nur Rastereffekt und GPU-Pathtracer) oder wählen Sie den Effekt im Szene-Browser aus.

>[!NOTE]
> 
>Die Tessellation beträgt *pro Objekt* in Rasterizer und GPU-Pathtracer und *pro Material* in OpenGL.

<a name="other-changes"></a>

## Andere Änderungen

### Knoten mit konstanten Werten

<table style="border: none; margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>Für einen leichteren Zugriff auf konstante Werte in Substance-Graf wurden <a href="../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md">neue Knoten</a> hinzugefügt, um einen einfachen Wert für jeden Typ zu generieren.</p><p>Sie finden alle im Abschnitt <b>Werte &gt; Konstanten</b> der Bibliothek.</p>
        </td>
        <td style="width: 60%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.resources/constants-float-01.png" alt="Konstanter Knoten &apos;Fließkommazahl&apos;" />
        </td>
    </tr>
</table>

### Ende der Lebensdauer von MDL-Diagrammen und Irays

Wie Sie in Version 15.1 benachrichtigt wurden, werden die MDL-Diagramm-Funktionen und der Iray-Renderer jetzt aus Designer entfernt.\
Unser hauseigener GPU-Pathtracer ist der Renderer der Wahl für hochwertiges fotorealistisches Rendering in Designer.

Designer entfernt sich von MDL zugunsten von MaterialX als bevorzugte Schattierung für austauschbare, weit unterstützte Material-Definitionen.\
MaterialX hat in der Computergrafikbranche schnell an Bedeutung gewonnen und kann von USD-Dateien mitgenommen werden, um eine vollständige Szene-Übertragbarkeit über DCCs und Renderer hinweg zu ermöglichen.

>[!NOTE]
> 
>Die Dokumentation für MDL-Diagramms und den Iray-Renderer ist auf der [dedizierten Seite zum Ende der Lebensdauer](../../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md) verfügbar.

### VFX-Plattform-Upgrades und macOS-Minimalversion

Die folgenden Bibliotheken wurden auf den neuesten VFX-Plattformstandard aktualisiert:

* C++ 20
* Python 3.13
* Qt 6.8
* Boost 1,88
* OpenColorIO 2.5
* OpenSubDiv 3.7
* OpenEXR 3.4
* oneTBB 2022

Die Anforderung für die minimale unterstützte Version von macOS wurde auf macOS 14 Sonoma aktualisiert.

<a name="release-notes"></a>

## Versionshinweise

### 16.0.0

*(veröffentlicht am 14. April 2026)*

### Hinzugefügt

* [Inhalt] Shape-Splatter v2-Knoten
* [Inhalt] Shape Splater v2 Mapper Color/Grayscale Nodes
* [Inhalt] Form Splint v2 zu Maskenknoten
* [Inhalt] Rasteratlas
* [Content] 3D-Viewer-Knoten
* [Content] 3D SDF-Operatorknoten
* [Content] 3D SDF primitive Knoten
* [Content] 3D SDF-Transformationsknoten
* [Content] 3D SDF-Materialknoten
* [Inhalt] Winkel zum Vektorknoten
* [Content] Knoten mit konstanten Werten
* [3D-Ansicht] OpenPBR-Shader für OpenGL-Renderer
* [3D-Ansicht] OpenPBR-Shader für Rasterizer und GPU-Pathtracer-Renderer
* [3D-Ansicht] Versatz-Fenster zum Festlegen der Height-Skalierung, der Height-Ebene und der Tesselierung
* [3D-Ansicht] Neuorganisieren der Symbolleistenelemente
* [3D-Ansicht] Legen Sie in der 3D-Ansicht OpenPBR als Standardansicht für das Materialmodell fest.
* [3D-Ansicht] Lassen Sie die 3D-Ansicht das Grafikattribut &quot;Materialmodell&quot; berücksichtigen.
* [3D-Ansicht] Synchronisieren von Materialmodellen beim Wechsel zwischen Rasterbildern/GPU-Pathtracer und OpenGL-Renderern
* [3D-Ansicht] Vergewissern Sie sich, dass das Materialmodell beim Wechseln von 3D-Renderern und Änderungen an der Material-Definition dauerhaft ist
werden synchronisiert
* [3D-Ansicht] GPU-Pathtracer: Pixelwiederholung für blaues Rauschen aktivieren
* [3D-Ansicht] Deckkraftsteuerung &quot;Umgebungs-Verdeckung belichten&quot;
* [3D-Ansicht] Stellen Sie den Parameterbereich &quot;Kacheln&quot; für alle Shader auf [0, 10] ein.
* [3D-Ansicht] Benennen Sie die Aktion &quot;Fokus&quot; in &quot;Frame&quot; um
* [3D-Ansicht] Verarbeiten Sie den neuen Parameter refineLevel, der tesselationFactor ersetzt.
* [3D-Ansicht] FPS-Zähler hinzufügen
* [3D-Ansicht] Verschieben Sie den Fortschrittsbalken in derselben horizontalen Symbolleiste wie den Farbraum unten
* [Bäcker] Anzeigen der UV-Werte des ausgewählten Bäckers in der Vorschau
* [Graph] Neues Materialmodell-Attribut zu Substance-Graphen hinzufügen
* [NewGraph] Hinzufügen von Trennlinien in der Miniaturansicht
* [Parameter] Definieren Sie einen standardmäßigen konstanten Wert für Eingabeparameter mit dem Editor &quot;Funktion&quot;
* [Parameter] Kombinationsfeld aus `Set` und `Is defined` Knotenparametern mit verfügbaren Variablen auffüllen
* [Voreinstellungen] Entfernen der veralteten Option &quot;Skalierungsfaktor deaktivieren&quot; auf der Registerkarte &quot;3D-Ansicht&quot;
* [Publish] Dialogfeld &quot;Publish&quot;: Materialmodell in Diagramminformationen einbeziehen
* [Python] Fügen Sie die neue Klasse SDMaterialModelDescription hinzu, um die Informationen eines Materialmodells abzurufen.
* [Python] Erlaubt das Abrufen/Festlegen der Materialmodell-Eigenschaft von SDSBSCompGraph-Objekten.
* [Python-Editor] Erhöhung der Schriftgröße auf 12
* [Vorlagen] OpenPBR-Vorlagen hinzufügen
* [Vorlagen] Materialproben in OpenPBR konvertieren
* [Drittanbieter] Update Boost auf Version 1.88
* [Drittanbieter] C++-API auf C++20 aktualisieren
* [Drittanbieter] NGL-Aktualisierung auf 1.42
* [Drittanbieter] OneTBB auf Version 2022.x aktualisieren
* [Drittanbieter] Update OpenColorIO auf Version 2.5.x
* [Drittanbieter] Update OpenEXR auf Version 3.4.x
* [Drittanbieter] Update Qt &amp; QtForPython auf 6.8.x und Python auf 3.13.x
* [Drittanbieter] Update TBB auf oneTBB 2021.x
* [Deprecation] Entfernen Sie Iray und den MDL-Editor.

### Fehlerbehebungen

* [2D-Ansicht] Der Histogrammauswahlbereich wird nicht beibehalten, wenn die Breite des Widgets klein wird
* [3D-Export] Aus Designer exportierte Gitter werden in usdview nicht gleich gerendert
* [3D-Ansicht] Wenn der 3D-Ansicht Nicht-Audiomaterial zugewiesen wird, bleibt der Einzelkachel-Rendermodus erhalten.
* [3D-Ansicht] Eingeklemmtes Ergebnis bei Verwendung von OCIO
* [3D-Ansicht] Absturz beim Anwenden einer Diagrammtextur auf ein nicht überschriebenes Material für eine bestimmte Szene
* [3D-Ansicht] Absturz beim Erstellen von Frame-Puffern
* [3D-Ansicht] Eclair-GPU-Pathtracer: Fehlerhafte Geometrie und geringe Leistung beim Rendern eines bestimmten Modells
* [3D-Ansicht] Falsche Texturtransformation für bestimmte Szenen
* [3D-Ansicht] Inkonsistentes Framing von Szene/Auswahl bei Verwendung einer festen Renderauflösung
* [3D-Ansicht] Falsche diffuse Farbe beim Rendern bestimmter GLTF-Datei
* [3D-Ansicht] Unsichtbare Umgebung beim Wechseln von Renderern in einem bestimmten Fall
* [3D-Ansicht] Materialien werden beim Importieren einiger .fbx-Dateien nicht korrekt erkannt
* [3D-Ansicht] mehrmaliges Überschreiben von Materialien setzt die Kachelung auf 1 zurück
* [3D-Ansicht] Eigenschaften in der Kategorie &quot;UVs&quot; werden nicht in SBSSCN-Dateien gespeichert
* [3D-Ansicht] &quot;Ausgaben in 3D-Ansicht zurücksetzen und anzeigen&quot; aus Diagrammen mit einer Ausgabe setzt Materialien nicht zurück
* [3D-Ansicht] &quot;Rendering speichern&quot;: Das bearbeitete Bildformat bleibt nicht erhalten
* [3D-Ansicht] Auswahl funktioniert nicht auf AMD-GPUs
* [3D-Ansicht] Die eigenständige 3D-Szene wird nicht aktualisiert, wenn sie auf der Festplatte geändert wird
* [3D-Ansicht] Einige Farbmaterialeigenschaften werden beim Überschreiben nicht korrekt farbverwaltet
* [3D-Ansicht] UDIM-Texturen werden auf ein bestimmtes Gitter nicht korrekt angewendet
* [3D-Ansicht] USD-Szene mit Material aus MaterialX wird nicht mehr korrekt gerendert
* [Bäcker] Abstürze mit einigen Netzen
* [Bäcker] Texturübertragung: Absturz in bkBufferViewCopy
* [Cooker] Endlose Schleife im While-Schleifen-Knoten in einem Fall, der verhindert werden konnte
* [Engine] Beenden Sie die Substance-Engine beim Schließen der Anwendung.
* [Allgemein] Vermeiden von zufälligen Abstürzen beim Beenden der Anwendung (nur Windows)
* [Diagramm] Funktionsdiagramm: Typweitergabe funktioniert in einigen Situationen nicht richtig
* [Graph] Graph-Links werden gelöscht, wenn ein Bildeingabeknoten umbenannt wird
* [Diagramm] Verknüpfungen und Pins zeigen manchmal Artefakte an
* [Voreinstellungen] &quot;Viewport-Skalierung&quot; ist invertiert
* [Eigenschaften] Absturz beim Ändern der Diagrammeingabe-Optimierung beim Anzeigen der Instanzparameter
* [Python] PySide6-Module können nicht importiert werden (möglicher Konflikt mit der vorhandenen PySide6-Installation)
* [Python] Bestehende PySide- und Shiboken-Module stehen im Konflikt mit Designers
* [UI] Hover-Stil verschwindet bei Schaltflächen in bestimmten Fällen (nur Windows)
* [UI] Hover-Stil ist nicht auf Dropdown-Schaltflächen sichtbar, wenn darauf geklickt wird (nur macOS)
* [UI] Schaltfläche &quot;Weitere Informationen&quot; in &quot;?&quot; QuickInfo funktioniert nicht, wenn sich die QuickInfo außerhalb der Dialogfeldgrenzen befindet (nur Windows)

### BEKANNTE FRAGEN

* [Graph] Generierte Symbole für OpenPBR-Graphen sind ungenau
* [3D-Ansicht] Szenen mit animierten Grundelementen werden nicht ordnungsgemäß unterstützt.
* [3D-Ansicht] Pathtracer wird nicht auf allen AMD-Grafikkarten unterstützt


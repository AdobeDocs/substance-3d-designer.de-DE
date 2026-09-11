---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/interface/3d-view/material-properties.html"
breadcrumb-title: ''
description: Konfigurieren Sie die Material-Eigenschaften in der 3D-Ansicht, um eine Vorschau anzuzeigen und anzupassen, wie Ihre Substance-Materials auf 3D-Objekten angezeigt werden.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Material properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialeigenschaften
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 29%

---


# Materialeigenschaften

Die [3D-Ansicht](../../../interface/3d-view/3d-view.md) rendert die Oberfläche von Modellen mithilfe eines Programms, das als *Shader* bezeichnet wird. Der Shader definiert das Material
die mithilfe einer Liste von Eigenschaften, die sich auf verschiedene Aspekte des Aussehens des Modells auswirken, auf das Modell angewendet werden.

Im Menü **Materialien** der 3D-Ansicht können Sie überprüfen, welcher Shader für jedes Material der Szene verwendet wird.

<a name="openpbr"></a>

## OpenPBR

Designer verwendet standardmäßig das [OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/)-Materialmodell, das mehrere komplexe Effekte unterstützt, z. B. Anisotropie,
Übertragung und Fuzz.

Die standardmäßigen [Graphvorlagen](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#graph-templates) und die [Materialproben](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#material-samples), die in Designer enthalten sind, basieren alle auf dem OpenPBR-Modell.

Die Eigenschaften dieses Shader folgen dem [OpenPBR-Parameterverweis](https://academysoftwarefoundation.github.io/OpenPBR/#parameterreference) und sind *für den Rasterbildner freigegeben*.
GPU-Pathtracer- und OpenGL [3D-Renderer &#x200B;](../3d-renderers/3d-renderers.md).

+++ UVs

| Parameter | Typ | Standard | Beschreibung |
|---------------------------------|---------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kacheln | Float | 1.0 | Die Anzahl der Zellwiederholungen in einer UV-Textur, wobei ein höherer Wert <br/> zu mehr Zellwiederholungen in der Textur führt. |
| Physische Größe aus Graphen aktivieren | Boolescher Wert | Falsch | Passen Sie die Kachelung automatisch entsprechend der [Physische Größe](../../../compositing-graphs/graph-parameters/graph-parameters.md)<br/> des Grafen an, um das Material in der entsprechenden Skala darzustellen. |
| UV-Skala | Float2 | 1.0, 1.0 | Passt die Skalierung der Unterteilung um einen separaten Faktor für U und V an, wobei ein <br/>höherer Wert zu mehr Texturwiederholungen führt. |

+++

+++ Basis

| Parameter | Typ | Standard | Beschreibung |
|-------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------|
| Stärke | Float | 1.0 | Multiplikator für die Intensität der Reflexion von der diffusen und metallischen Basis. |
| Color | Fließkommazahl3 (RGB) | 0.8, 0.8, 0.8 | Farbe der Reflexion von der diffusen und metallischen Basis. |
| Metallisch | Float | 0.0 | Legt fest, wie metallic das Basismaterial angezeigt wird. (Wählt die Basis vom reinen Dielektrikum zum reinen Metall) |
| Diffuse Rauheit | Float | 0.0 | Rauheit der diffusen Reflexion. Höhere Werte führen dazu, dass die Oberfläche flacher erscheint. |

+++

+++ Glanz

| Parameter | Typ | Standard | Beschreibung |
|------------|--------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Stärke | Float | 1.0 | Multipliziert die Glanzlichtreflexion. |
| Color | Fließkommazahl3 (RGB) | 1.0, 1.0, 1.0 | Die Farbe der Specular-Reflexion. (Steuert den physischen Kantenfarbton für Metalle,<br/>, und einen nicht physischen Gesamtfarbton für Dielektrika.) |
| Rauheit | Float | 0.3 | Die Rauheit der Specular-Reflexion. Niedrigere Zahlen erzeugen schärfere<br/> Reflexionen, höhere Zahlen erzeugen unschärfere Reflexionen. |
| Anisotropie | Float | 0.0 | Die Richtungsvorspannung der Rauheit der metallischen/dielektrischen Unterlage, die zu zunehmend gedehnt Glanzlichtern entlang der Tangente führt.<br/> |
| IOR | Float | 1.5 | Brechungsindex der dielektrischen Basis. |

+++

+++ Übertragung

| Parameter | Typ | Standard | Beschreibung |
|------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stärke | Float | 0.0 | Mischungsgewicht zwischen der transparenten und der opaken dielektrischen Basis.<br/>Je größer der Wert ist, desto transparenter ist das Material. |
| Color | Fließkommazahl3 (RGB) | 1.0, 1.0, 1.0 | Steuert die Farbe der durchsichtigen Basis aufgrund der volumetrischen <br/>Absorption des Biergesetzes unter der Oberfläche. |
| Tiefe | Float | 0.0 | Gibt die Entfernung an, die das Licht innerhalb der transparenten Basis zurücklegt, bevor es nach Biergesetz genau zu `transmission_color` wird.<br/> |
| Streuung | Fließkommazahl3 (RGB) | 0.0, 0.0, 0.0 | Steuert die Farbe des in der transparenten Basis volumetrisch gestreuten Lichts. |
| Anisotropie | Float | 0.0 | Der Betrag der Richtungsvorspannung (Anisotropie) der volumetrischen Streuung <br/> in der durchsichtigen Grundfläche. |
| Streuungsskala | Float | 0.0 | Skaliert linear die Stärke der Streuung. |
| Abbe-Nummer | Float | 20.0 | Physikalische Abbe-Nummer des dielektrischen Mediums, die beschreibt, wie viel<br/>der dielektrische Brechungsindex über Wellenlängen variiert. |

+++

+++ Volumen

| Parameter | Typ | Standard | Beschreibung |
|--------------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stärke | Float | 0.0 | Mischungsgewicht, das die undurchsichtige dielektrische Basis zwischen <br/>diffuser Reflexion und Volumenstreuung wählt. |
| Color | Fließkommazahl3 (RGB) | 0.8, 0.8, 0.8 | Die beobachtete Reflexionsfarbe des Volumenstreuungs-Mediums. |
| Radius | Float | 1.0 | Längenskala der Volumenstreuung des Mittelwertes des freien Pfads. |
| Radiusskala | Fließkommazahl3 (RGB) | 1.0, 0.5, 0.25 | RGB-Multiplikator auf subsurface_radius, wobei die Streuung pro Kanal <br/>mittlere freie Pfade ergibt. |
| Anisotropie | Float | 0.0 | Steuert die Phasenfunktion der Volumenstreuung, bei der Null-<br/>-Streuungen gleichmäßig leuchten, positive Werte vorwärts und negative<br/>-Werte rückwärts Streuung werden. |

+++

+++ Beschichtung

| Parameter | Typ | Standard | Beschreibung |
|------------|--------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Stärke | Float | 0.0 | Das Anwesenheitsgewicht einer reflektierenden Klarlackschicht auf dem Material.<br/>Verwenden Sie diese Option für Material wie Malen oder eine Ölschicht. |
| Color | Fließkommazahl3 (RGB) | 1.0, 1.0, 1.0 | Die Farbe der Transparenzschicht bedingt durch die Absorption in der Beschichtung. |
| Rauheit | Float | 0.0 | Die Rauheit der Klarlack-Reflexionen.<br/>Je niedriger der Wert, desto schärfer die Spiegelung. |
| Anisotropie | Float | 0.0 | Die Richtungsabweichung der Rauheit der Klarlackschicht,<br/>, was zu zunehmend gedehnt Glanzlichtern entlang der Tangente der Beschichtung führt. |
| IOR | Float | 1.6 | Der Brechungsindex der Transparenzschicht. |
| Abdunkeln | Float | 1.0 | Moduliert den physikalischen Effekt der Schichtabdunkelung. |

+++

+++ Fuzz

| Parameter | Typ | Standard | Beschreibung |
|-----------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Stärke | Float | 1.0 | Das Anwesenheitsgewicht einer Fuzz-Schicht, die zur Näherung von Mikrofasern verwendet werden kann,<br/>für Gewebe wie Samt und Satin sowie für Körner aus Dust. |
| Color | Fließkommazahl3 (RGB) | 1.0, 1.0, 1.0 | Die Farbe der Fuzz-Ebene. |
| Rauheit | Float | 0.5 | Die Rauheit der Fuzz-Ebene. |

+++

+++ Emission

| Parameter | Typ | Standard | Beschreibung |
|-----------|--------------|---------------|------------------------------------------------------|
| Luminanz | Float | 0.0 | Die Stärke des ausgestrahlten Lichts, als Luminanz in Nits. |
| Color | Fließkommazahl3 (RGB) | 1.0, 0.0, 0.0 | Die Farbe des ausgestrahlten Lichts. |

+++

+++ Dünnfilm

| Parameter | Typ | Standard | Beschreibung |
|-----------|-------|---------|-------------------------------------------------------------------------------------------------------|
| Stärke | Float | 0.0 | Deckungsgewicht der Dünnschicht.<br/>Für Material wie mehrfarbiges Malen oder Seifenblasen verwenden. |
| Stärke | Float | 0.5 | Die Thickness der Dünnfilmschicht auf der Unterlage. (in Mikrometern) |
| IOR | Float | 1.4 | Der Brechungsindex des Dünnfilms. |

+++

+++ Geometrie

| Parameter | Typ | Standard | Beschreibung |
|-------------------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Deckkraft | Float | 1.0 | Die Deckkraft des gesamten Materials. |
| Dünnwandig | Boolescher Wert | Falsch | Wenn dieser Wert wahr ist, ist die Oberfläche doppelseitig und stellt eine unendlich dünne Schale dar.<br/>Geeignet für extrem geometrisch dünne Objekte wie Blätter oder Papier. |
| Normale | Fließkommazahl3 (RGB) | 0.5, 0.5, 1.0 | Eingabe der geometrischen Normale für die Fläche. |
| Tangent | Fließkommazahl3 (RGB) | 1.0, 0.5, 0.0 | Eingabe der geometrischen Tangente. |
| Beschichtungs-Normale | Fließkommazahl3 (RGB) | 0.5, 0.5, 1.0 | Eingabe der Normalen für die Beschichtungsebene. |
| Beschichtungs-Tangente | Fließkommazahl3 (RGB) | 1.0, 0.5, 0.0 | Eingabe der geometrischen Tangente für die Beschichtungsebene. |
| Höhe | Float | 0.5 | Versatz (bzw. Bump) in der Normalenrichtung.<br/>Wenn das Height der Ebene des Heights entspricht, ist kein Versatz vorhanden.<br/>Versatz ist eine skalare Änderung der Oberflächenposition in Richtung einer ungestörten, <br/>vermischten Normalfläche.<br/>In Fällen, in denen der tesselierte Versatz nicht möglich oder erwünscht ist, kann das <br/>Height als Bumpmap implementiert werden. |
| Höhenebene | Float | 0.5 | Wert des Heights, das keinem Versatz entspricht (Nullwert).<br/>Der Height-Pegel verschiebt (aber skaliert oder spiegelt nicht) den Versatz relativ<br/> zur Oberfläche des unversetzten Objekts.<br/>Wenn die Ebene des Heights 0 ist, ist der gesamte Versatz höher.<br/>Wenn die Ebene des Heights 1 ist, befindet sich der gesamte Versatz unter der Fläche, aber es bleibt <br/>die gleiche Skalierung und Richtung. |
| Höhenskala | Float | 1.0 | Skalierung von Versatz oder Bump in Szenen.<br/>Die Größe und die Richtung der Skalierung sind unabhängig vom Wert des Heights. |
| Umgebungsverdeckung | Float | 1.0 | Ambient occlusion-Karte zum Abdunkeln verdeckter Bereiche.<br/>Weiß (1.0) bedeutet vollständig beleuchtet, Schwarz (0.0) bedeutet vollständig verdeckt. |

+++

### Kompatibilität mit bestehenden Grafen

Für einige Modelle in Designer gelten andere Identifizierungen als für andere Material.
Designer gleicht automatisch einige Identifizierungen ab, um die Kompatibilität mit OpenPBR als Standardmodell sicherzustellen.

+++ Zuordnungen zwischen Legacy- und OpenPBR-Nutzung

| Ältere Version | OpenPBR |
|-------------------------|-----------------------------|
| Metallisch | Metallisierung |
| specularEdgeColor | specularColor |
| Rauheit | specularRoughness |
| anisotropyLevel | specularRoughnessAnisotropy |
| IOR | specularIOR |
| absorptionColor | transmissionColor |
| absorptionDistance | transmissionDepth |
| translucency | subsurfaceWeight |
| scatteringColor | subsurfaceColor |
| scatteringDistance | subsurfaceRadius |
| scatteringDistanceScale | subsurfaceRadiusScale |
| coatOpacity | coatWeight |
| sheenOpacity | fuzzWeight |
| sheenColor | fuzzColor |
| sheenRoughness | fuzzRoughness |
| Ausstrahlend | emissionColor |

+++

### Weitere Informationen

Weitere Informationen über OpenPBR finden Sie in den folgenden Ressourcen:

* [Blog-Artikel über Adobe](https://blog.adobe.com/en/publish/2023/08/08/openpbr-strengthens-interoperability-enabling-enhanced-creativity)
* [Whitepaper](https://academysoftwarefoundation.github.io/OpenPBR/)
* [Adobe OpenPBR BSDF auf GitHub](https://github.com/adobe/openpbr-bsdf)
* [Designer 16.0: Unterstützung der OpenPBR](../../../release-notes/version-16-0/version-16-0.md#openpbr-support)

<a name="adobe-standard-material"></a>

## Adobe-Standardmaterial

Das Adobe Standard Material (ASM)-Modell wurde in Designer 11.2 eingeführt und war Designers Standard-Shader.
bis Version 15.1.

Während Designer als neues Standardmodell in die OpenPBR gewechselt ist, ist ASM weiterhin enthalten und die Eigenschaften werden ebenfalls gemeinsam genutzt
auf den Rasterbildern GPU-Pathtracer und OpenGL [3D-Renderer](../3d-renderers/3d-renderers.md).

Das Modell ist hier [dokumentiert](https://experienceleague.adobe.com/de/docs/substance-3d/general-knowledge/asm/adobe-standard-material).

<a name="usdpreviewsurface"></a>

## UsdPreviewSurface

Der Zweck des UsdPreviewSurface-Modells ist die Vorschau von Materialien mit einem grundlegenden Funktionssatz, der die Kompatibilität fördert.
über Renderer hinweg, die USD und/oder Hydra enthalten.

In Designer wird dieses Materialmodell nur von den Rasterbildern und dem GPU-Pathtracer [3D-Renderer &#x200B;](../3d-renderers/3d-renderers.md) unterstützt.

Das Modell ist hier [dokumentiert](https://openusd.org/dev/spec_usdpreviewsurface.html).

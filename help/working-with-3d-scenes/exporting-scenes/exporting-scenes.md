---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/exporting-scenes.html"
breadcrumb-title: ''
description: Exportieren Sie 3D-Szenen mit allen in Designer vorgenommenen Bearbeitungen mithilfe der Aktion "Szene exportieren" im Menü "3D-Szene anzeigen".
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Exporting scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportieren von Szenen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---


# Exportieren von Szenen

Wenn Sie eine Szene mit allen in Designer vorgenommenen Änderungen exportieren müssen, verwenden Sie die Option &quot;Szene exportieren...&quot;. Aktionen im Menü &quot;Szene&quot; von [3D View](../../interface/3d-view/3d-view.md).

Bei Exporten in USD-Formate stimmt der Inhalt der Szene mit der Struktur überein, die im [Szenenbrowser](../../interface/3d-view/scene-browser/scene-browser.md) angezeigt wird.

Bei anderen Formaten hängen der Inhalt der Szene und ihre interne Struktur von den Funktionen ab, die vom ausgewählten Dateiformat unterstützt werden.

>[!NOTE]
>
> Alle von Designer zur Szene hinzugefügten Elemente werden in die exportierte Szene aufgenommen: die Standardkamera, die Standardumgebung, alle Materialien kopiert alle zusätzlichen Lichter.

![Szenenexportaktionen](../../assets/exportActions.png "Szenenexportaktionen"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Szene exportieren

</td>
<td style="border: 0;" valign="top">

### Szene als Ebenen exportieren

</td>
<td style="border: 0;" valign="top">

### Texturen

</td>
</tr>
</table>

## Szene exportieren

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Die Aktion &quot;Szene exportieren...&quot; im Menü &quot;Szene&quot; exportiert bearbeitete 3D-Szenen destruktiv: Die Szene ist *reduziert*, und alle Verweise auf das Original gehen verloren.

Das bedeutet, dass Änderungen an der ursprünglichen Szene die exportierte Szene überhaupt nicht beeinflussen.

</td>
<td style="border: 0;" valign="top">

![Exportierte Szenendateien - Reduziert](../../assets/exportFlattened.png "Exportierte Szenendateien - Reduziert"){zoomable="yes"}

</td>
</tr>
</table>

## Szene als Ebenen exportieren

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Die Aktion &quot;Szene als Ebenen exportieren...&quot; wird in <b>USD</b>-Formate (.usd, .usda, .usdc, .usdz) exportiert und ist *nicht destruktiv*: Die exportierte Hauptdatei enthält eine *Verweiskette*, in der alle bearbeiteten Aspekte der neuen Szene in separaten USD-Dateien gespeichert werden.

Das bedeutet, dass Änderungen an der ursprünglichen Szene in die exportierte Szene übernommen werden.

</td>
<td style="border: 0;" valign="top">

![Exportierte Szenendateien - Ebenen](../../assets/exportLayered.png "Exportierte Szenendateien - Ebenen"){zoomable="yes"}

</td>
</tr>
</table>

Die exportierten Dateien folgen dieser Struktur:

* <b>Hauptdatei</b>
  * <b>.layers</b>: Verweist auf die folgenden Unterebenen und deklariert die Materialmodifikationen, die die Geometrie an die von Designer erstellten Materialkopien binden.
    * <b>.assembly</b>: Verweist auf die .scene#-Datei und deklariert die Geometrieüberschreibungen, die die von Designer neu berechneten Daten der von überschriebenen Materialien betroffenen Geometrie enthalten.
      * <b>.scene#</b>: Verweist auf die ursprüngliche Szene.
    * <b>.camera</b>: Deklariert die von Designer zur Szene hinzugefügte Kamera.
    * <b>.light</b>: Deklariert die Lichter, die der Szene von Designer hinzugefügt wurden.
    * <b>.material</b>: Deklariert die Materialkopien, die Designer der Szene hinzugefügt hat und die exportierten Texturen verwenden.

## Texturen

Texturen werden in ein Verzeichnis neben der exportierten Datei exportiert und nach dieser benannt, mit dem Suffix &quot;<b>\_textures</b>&quot;.

Sie verwenden das Format <b>PNG</b>, mit Ausnahme von HDR. Texturen (Gleitkommaformat), die das Format <b>EXR</b> verwenden.

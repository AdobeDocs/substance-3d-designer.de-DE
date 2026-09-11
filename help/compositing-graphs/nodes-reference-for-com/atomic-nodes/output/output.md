---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/output.html"
breadcrumb-title: ''
description: ''
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ausgabe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---


# Ausgabe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elementare Knoten: Ausgabe](output.resources/comp_output_1.png "Elementare Knoten: Ausgabe "){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Der Ausgabeknoten gibt das <b>Ergebnis</b> eines Substance-Grafen oder eines seiner Ergebnisse an, wenn mehr als ein Ausgabeknoten darin vorhanden ist.

Das Bild oder der Wert, das bzw. der mit dem Ausgabeknoten eines Grafen verbunden ist, wird von jedem [Instanzknoten](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) ausgegeben, der diesen Graf darstellt, und [kann als Graphausgabe &#x200B;](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) exportiert werden.

</td>
</tr>
</table>

Wenn eine [veröffentlichte Sbsar-Datei](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) diesen Graf enthält, kann diese Datei dieses Bild in jeder Integration oder in jedem Plug-In ausgeben, die die Datei verwendet.

Er verfügt über einen einzigen Eingangssteckplatz, der typunabhängig ist, d. h., er tippt sich selbst nach dem mit ihm verbundenen Datentyp ein.

Es hat keine Parameter, sondern Attribute, die von großer Bedeutung sind, um die Ausgabe ordnungsgemäß zu beschriften und ihrer beabsichtigten Verwendung zuzuführen.

Jeder Substance-Graf muss über *mindestens einen* Ausgabeknoten verfügen. Wenn keine Ausgabe vorhanden ist, kann der Graf nie ein tatsächliches Ergebnis zurückgeben, und es wird eine [Warnung](../../../../technical-issues/warnings-and-errors/warnings-and-errors.md) ausgelöst.

## Attribute

|  |  |
| --- | --- |
| <b>Identifizierung</b> *Zeichenfolge* | Die eindeutige Identifizierung der Ausgabe. Diese Eigenschaft darf nicht leer gelassen werden und darf keine Sonderzeichen oder Leerzeichen enthalten.   Die Identifizierung wird verwendet, da die Bezeichnung des Knotens lautet, dass die Eigenschaft &#39;Label&#39; leer gelassen wird. Sie kann auch verwendet werden, um [exportierte Texturen](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) zu benennen. |
| <b>Beschreibung</b> *Zeichenfolge* | Die optionale Beschreibung, die als QuickInfo für die Ausgabe verwendet wird, lautet Substance-Graf. |
| <b>Bezeichnung</b> *Zeichenfolge* | Dies wird als Bezeichnung für den Ausgabeknoten verwendet und die zugehörige Verbindung in [Instanzknoten](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), die diesen Graf darstellt. Die Beschriftung kann Leerzeichen und Sonderzeichen enthalten. |
| <b>Benutzerdaten</b> *Zeichenfolge* | Optionale Metadaten, die für bestimmte Filtervorgänge verwendet werden können. [Substance 3D Painter](https://www.adobe.com/de/products/substance3d/apps/painter.html) nutzt diese Daten, um [einige Funktionen zu steuern](https://experienceleague.adobe.com/de/docs/substance-3d-painter/using/content/creating-custom-effects/user-data). |
| <b>Gruppe</b> *Zeichenfolge* | Attribut, das zum Gruppieren von Ausgaben für die [Linkerstellungsmodi von Designer verwendet wird](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md).   Ausgaben mit einem identischen &#39;Group&#39;-Attribut werden als einzelne Verbindung im &#39;Compact Material&#39;-Verknüpfungserstellungsmodus angezeigt. |

## Integrationsattribute

Dies sind Attribute, die von Integrationen/Plug-ins verwendet werden sollen, die das Diagramm in einer [veröffentlichten SBSAR-Datei verwenden](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md).

Daher haben sie keine Auswirkungen auf das Format von [Bitmapexporten](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). Darüber hinaus wird in Designer nur das Attribut <b>Nutzung</b> verwendet. Weitere Informationen finden Sie unten.

<b>Nutzung</b>

|  |  |
| --- | --- |
| <b>Komponente</b> *Zeichenfolge* | Wird verwendet, um den entsprechenden SVBRDF-Shader-Eingaben in AxF-Workflows einige Texturkanäle zuzuordnen. |
| <b>Nutzung</b> *Zeichenfolge* | Definiert den Typ und die Verwendung des Ausgabeknotens. Diese Eigenschaft ist wichtig, da sie Folgendes bewirkt:<ul data-preserve-html="true"> <li data-preserve-html="true">Knotenverbindung in Substance-Graphen bei Verwendung einiger [Link-Erstellungsmodi](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) </li> <li data-preserve-html="true">Verbindung von Texturen mit Shadern in der 3D-Ansicht (siehe unten: &#39;[Informationen zur Rolle von Benutzern in der 3D-Ansicht](#usages-role-3dview)&#39;)</li> <li data-preserve-html="true">Verbindung von Texturen mit Materialien in Integrationen/Plug-ins</li> </ul> |
| <b>Farbraum</b> *Zeichenfolge* | Legt den Farbraum fest, in dem diese Ausgabe interpretiert werden soll. Wird von einigen Integrationen in anderen Anwendungen verwendet und hat keine Auswirkungen in Designer. |

### Die Rolle der Benutzer in der 3D-Ansicht

Da Graphausgaben häufig das Endergebnis für einen bestimmten Textur-Kanal sein sollen, können Ausgänge automatisch an den entsprechenden Sampler des in der 3D-Ansicht verwendeten Shader geschickt werden.

Eine Ausgabe, deren <b>Syntax</b>-Eigenschaft *mit einer Samplerverwendung* in der 3D-Ansicht übereinstimmt, wird mit diesem Sampler verbunden. Beispiel: Ein Ausgang mit einer `basecolor`-Nutzung wird mit dem `basecolor`-Sampler des 3D-Ansicht-Shader verbunden. Weitere Informationen finden Sie im Abschnitt &quot;[Daten anzeigen&quot; im Abschnitt &quot;3D-Ansichten](../../../../interface/3d-view/3d-view.md)&quot; der Seite &quot;[3D-Ansichten](https://substance3d.adobe.com/documentation/display/draftdesigner/.3d%20view%20vdraftversion)&quot;.

Klicken Sie in einem leeren Bereich in der [Graphansicht](../../../../interface/the-graph-view/the-graph-view.md) auf RMB und wählen Sie im Kontextmenü die Option <b>3D-Ansichten in 3D-Ansicht anzeigen</b> aus, um alle Ausgaben mit Datensamplern zu verbinden, die *mit  übereinstimmen*.

>[!IMPORTANT]
>
> Wenn mehrere Verwendungen eingerichtet werden, um beispielsweise den Kanälen in einer gepackten Textur Benutzungen zuzuweisen, wird nur die *erste Nutzung* in der Liste mit der 3D-Ansicht verbunden. Dies ist eine bekannte Einschränkung.

## Standardausgabe

Wenn ein Graf mehr als eine Ausgabe hat, kann eine dieser Ausgaben als Standardausgabe für diesen Graf festgelegt werden. Hiermit wird festgelegt, welche der Ausgaben für Folgendes verwendet werden sollen:

* Die Miniaturansicht eines beliebigen Instanzknotens, der diesen Graf darstellt
* Anzeigen dieser Instanzknoten in der 2D-Ansicht
* Die Miniaturansicht dieses Grafen in der Bibliothek (erfahren Sie hier, wie Sie Ihre eigenen Ressourcen [hinzufügen](../../../../interface/preferences-window/project-settings/project-settings.md)).

Mit dieser Funktion können Sie Graphausgaben in beliebiger Reihenfolge anordnen, unabhängig davon, wie der Graf als Knoten dargestellt wird.

So legen Sie einen Ausgabeknoten als Standardausgabe eines Grafen fest:

* Klicken Sie mit der rechten Maustaste auf einen Ausgabeknoten und wählen Sie im Kontextmenü die Aktion Als Standardausgabe festlegen aus.
* Verwenden Sie in den Eigenschaften des Ausgabeknotens die Schaltfläche &quot;Als Standard festlegen&quot; in der Kopfzeile des Abschnitts &quot;Attribute&quot;.

Hier ist ein Beispiel für Instanzknoten vor und nach dem Festlegen einer Standardausgabe:

<table>
  <tr style="border: 0">
    <td style="border: 0">
      <img src="output.resources/defaultouput2.png" alt="defaultouput2">
      <br><i>Vorher</i>
    </td>
    <td style="border: 0">
      <img src="output.resources/defaultouput1.png" alt="defaultouput1">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

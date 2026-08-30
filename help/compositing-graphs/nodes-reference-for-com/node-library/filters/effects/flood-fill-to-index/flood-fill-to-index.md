---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: Verwenden Sie den Flood Fill-zu-Index-Knoten, um Bereiche mit Indexwerten zu füllen, um nummerierte und beschriftete Muster zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill in Index
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# Flood Fill in Index

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-index.resources/floodfill-index.png){width="200px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Mit &quot;Flood Fill in Index&quot; wird jede Indexzelle in einen Wert entsprechend ihrer Indexnummer konvertiert. Der Wert beginnt mit 0 links oben. Es kann verwendet werden, um Graustufenfarben in einer normalisierten Form (0,0 bis 1,0, dividiert durch so viele Zellen, wie durch Flood Fill gefunden wurden) oder als HDR-Wert (0 bis n, wobei n die Anzahl der Zellen ist) ohne Klammerung zurückzugeben.

Darüber hinaus verwendet Flood Fill in Index [Werte](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md) und gibt die Anzahl der gefundenen Formen und die optionale interne Datentabelle zurück.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Bbox für Flood Fill</b> <i>Farbeingabe</i> | Standard-Flood Fill-Eingabe-Map. Erforderlich. |
| <b>Spezielle Forminformationen</b> <i>Farbeingabe</i> | Zusätzliche Knotenkarte, muss explizit auf dem vorherigen Flood Fill aktiviert werden und muss mit dem Flood Fill verbunden werden!. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Normalisiert, Ganzzahl</i> | Stellen Sie fest, ob die Ausgabedarstellung im LDR-0-1-Bereich oder im HDR-0-n-Bereich liegt. |
| <b>Form ignorieren, die kleiner ist als </b> <i>0.0 - 1.0</i> | Toleranzwert zum Ignorieren kleiner Formen. |
| <b>Flood Fill-Datentabelle anzeigen</b> <i>False/True</i> | Gibt zusätzliche (Debug-)Daten für die erweiterte Verwendung zurück. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-index.resources/flood-fill-ex02.jpg" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 2%

---


# Flood Fill in Index

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

## Flood Fill in Index

**In:** *Filter/Effekte*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Mit &quot;Flood Fill in Index&quot; wird jede Indexzelle in einen Wert entsprechend ihrer Indexnummer konvertiert. Der Wert beginnt mit 0 links oben. Es kann verwendet werden, um Graustufenfarben in einer normalisierten Form (0,0 bis 1,0, dividiert durch so viele Zellen, wie durch Flood Fill gefunden wurden) oder als HDR-Wert (0 bis n, wobei n die Anzahl der Zellen ist) ohne Klammerung zurückzugeben.

Darüber hinaus verwendet Flood Fill in Index das neue [Value-System und gibt zusätzliche Werte](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/values-in-substance-3d-graphs-180192235.html) zurück, die die Anzahl der gefundenen Formen und die optionale interne Datentabelle enthalten.

### Eingaben

* **Flood Fill-Box**: *Farbeingabe* Standardzuordnung für Flood Fill-Eingabe. Erforderlich.
* **Spezielle Forminformationen**: *Farbeingabe* Zusätzliche Flood Fill-Map, muss explizit auf dem vorherigen Flood Fill-Knoten aktiviert werden und muss verbunden werden!.

### Parameter

* **Ausgabe**: *Normalisiert, Integer* Ermitteln Sie, ob die Ausgabe im LDR-0-1-Bereich oder im HDR-0-n-Bereich liegt.
* **Form ignorieren, die kleiner ist als**: *0.0 - 1.0* Toleranzwert zum Ignorieren kleiner Formen.
* **Flood Fill-Datentabelle anzeigen**: *Falsch/Wahr* Gibt zusätzliche (Debug-)Daten für die erweiterte Verwendung zurück.

## Beispiele

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>

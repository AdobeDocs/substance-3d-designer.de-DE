---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: Verwenden Sie den Metallic PBR BaseColor Validate-Knoten zum Validieren und Korrigieren der Grundfarben- und metallic Werte für PBR-Material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR BaseColor Metallic validieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# PBR BaseColor/Metallic Validierung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-basecolor-metallic-validate.resources/pbr-basecolor-metallic-validate.png){width="128px"}

<b>In:</b> Materialfiltern > PBR-Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein Hilfsknoten, der eine Gut-zu-Schlecht-Heatmap generiert, auf der Werte gemäß PBR-Standards korrekt oder falsch sind.

Es ist sehr nützlich als Lernwerkzeug für PBR, da es eine sehr klare visuelle Rückmeldung darüber gibt, was die Fehler sind und wo sie gefunden werden können.

Verwenden Sie dies nicht als das Allerletzte, aber stellen Sie dennoch sicher, dass Sie immer ein klares Verständnis dafür haben, warum Sie gegen Regeln verstoßen, die dieses Werkzeug hervorheben könnte.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Validierungsmodus</b> <i>Albedo, Metall, kombiniert</i> | Legt fest, ob nur Albedo, Metall oder beide als Übersichtsmodus kombiniert überprüft werden. |
| <b>Schwellenwert für dunklen Bereich der Albedo</b> <i>50 sRGB, 30 sRGB</i> | Setzt die untere Albedo entweder auf 50 oder 30 sRGB. Kann die Toleranz für rote Bereiche verringern oder erhöhen. |
| <b>Reflexionsbereich des Metalls</b> <i>70-100 % reflektierend, 60-100 % reflektierend</i> | Ändert den Metallic Bereich so, dass er als richtig gilt. Kann die Toleranz für rote Bereiche verringern oder erhöhen. |
| <b>Überlagerungszuordnung</b> <i>False/True</i> | Der Schnelldebugmodus zum Überlagern von Eingabe-Map ermöglicht eine schnellere Nachverfolgung von Problembereichen. |

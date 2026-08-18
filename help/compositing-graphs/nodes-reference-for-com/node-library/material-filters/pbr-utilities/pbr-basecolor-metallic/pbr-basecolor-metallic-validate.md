---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten PBR BaseColor Metallic Validate zum Validieren und Korrigieren der Grundfarben- und Metallwerte für PBR-Materialien.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR BaseColor Metallic-Validierung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# PBR BaseColor/Metallic-Validierung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

## PBR BaseColor/Metallic-Validierung

**In:** *Materialfilter/PBR-Dienstprogramme*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Ein Hilfsknoten, der eine Gut-zu-Schlecht-Heatmap generiert, auf der Werte gemäß PBR-Standards korrekt oder falsch sind.

Es ist sehr nützlich als Lernwerkzeug für PBR, da es eine sehr klare visuelle Rückmeldung darüber gibt, was die Fehler sind und wo sie gefunden werden können.

Verwenden Sie dies nicht als das Allerletzte, aber stellen Sie dennoch sicher, dass Sie immer ein klares Verständnis dafür haben, warum Sie gegen Regeln verstoßen, die dieses Werkzeug hervorheben könnte.

## Parameter

* **Validierungsmodus**: *Albedo, Metall, Kombiniert* Legt fest, ob nur Albedo, Metall oder beide als Übersichtsmodus kombiniert überprüft werden.
* **Schwellenwert für dunklen Bereich der Albedo**: *50 sRGB, 30 sRGB* Setzt die untere Albedo entweder auf 50 oder 30 sRGB. Kann die Toleranz für rote Bereiche verringern oder erhöhen.
* **Reflexionsbereich des Metalls**: *70-100% reflektierend, 60-100% reflektierend*&#x200B;Ändert den metallischen Bereich so, dass er als korrekt angesehen wird. Kann die Toleranz für rote Bereiche verringern oder erhöhen.
* **Überlagerungszuordnung**: *Falsch/Wahr* Der Schnelldebugmodus zum Überlagern von Eingabemaps ermöglicht ein schnelleres Nachverfolgen von Problembereichen.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

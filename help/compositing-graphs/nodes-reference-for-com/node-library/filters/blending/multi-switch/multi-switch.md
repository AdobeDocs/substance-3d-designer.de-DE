---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Multi Switch", um zwischen mehreren Eingabetexturen zu wechseln, basierend auf einem Selektor für die Auswahl bedingter Texturen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mehrfachschalter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# Mehrfachschalter

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-switch-greyscale.png){width="128px"}

![](../../../../../../assets/multi-switch.png){width="128px"}

## Multiswitch (Graustufen)

**In:** *Filters/Blending*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Funktioniert als Schaltkasten und durchläuft nur den Eingang, der durch den Parameter &#39;Eingabeauswahl&#39; definiert ist. Wenn also zwei Eingänge verbunden sind, wird nur einer davon zurückgegeben (unverändert), je nach Wahl des Benutzers.

Sehr nützlich zum Hinzufügen vieler verschiedener Optionen in einem Diagramm. In Kombination mit [Verfügbarmachen von ](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) (vorzugsweise als Dropdown-Liste) ist eine Menge Anpassung möglich.

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Multi Switch&quot; für Farbeingaben, &quot;Multi Switch Grayscale&quot; für Graustufeneingaben.

## Parameter

### Eingaben

* **Eingabe 1-20**: *Farbeingabe*

### Parameter

* **Eingabenummer**: *2 - 20* Anzahl der zu veröffentlichenden Eingaben. Wichtig: entfernt keine Verbindungen, wenn die Anzahl verringert wird!
* **Eingabeauswahl**: *1 - 20* Welche Eingabe als Ergebnis zurückgegeben werden soll.

## Beispielbilder

</td>
</tr>
</table>

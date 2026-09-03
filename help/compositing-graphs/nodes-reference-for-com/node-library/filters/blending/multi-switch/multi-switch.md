---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Mehrere Switches", um zwischen mehreren Eingabe-Texturen zu wechseln, die auf einem Selektor für die Auswahl einer bedingten Textur basieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mehrfachschalter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Mehrfachschalter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-switch.resources/multi-switch-01.png){width="128px"}

![](multi-switch.resources/multi-switch-02.png){width="128px"}

<b>In:</b> Filters > Blending

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Funktioniert als Schaltkasten und durchläuft nur den Eingang, der durch den Parameter &#39;Eingabeauswahl&#39; definiert ist. Wenn also zwei Eingänge verbunden sind, wird nur einer davon zurückgegeben (unverändert), je nach Wahl des Benutzers.

Diese Option ist sehr praktisch, wenn Sie einem Graf viele verschiedene Optionen hinzufügen möchten. In Kombination mit [leg](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) (vorzugsweise als Dropdown-Liste) ist eine große Anpassung möglich.

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Multi Switch&quot; für Farbeingaben, &quot;Multi Switch Grayscale&quot; für Graustufeneingaben.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe 1-20</b> <i>Farbeingabe</i> |  |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Eingabenummer</b> <i>2 - 20</i> | Anzahl der zu legend Eingaben. Wichtig: entfernt keine Verbindungen, wenn die Anzahl verringert wird! |
| <b>Eingabeauswahl</b> <i>1 - 20</i> | Welche Eingabe als Ergebnis zurückgegeben werden soll. |

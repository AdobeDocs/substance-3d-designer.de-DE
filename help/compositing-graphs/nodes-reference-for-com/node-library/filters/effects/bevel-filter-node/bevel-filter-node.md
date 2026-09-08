---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: Mit dem Filterknoten "Abgeflachte Kante" erstellen Sie abgeflachte Kanten an Formen und Mustern, um Tiefe und Dimension hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Abgeflachte Kante (Filterknoten)
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 4%

---


# Abgeflachte Kante (Filterknoten)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt einen Kantenabflachungseffekt für eine Graustufen-Höhenkarte aus. Gibt sowohl die abgeflachte Höhenkarte als auch die Normalmap basierend auf dieser Höhenkarte zurück.

Dies ist ein nützlicher Knoten zum Anwenden von exakten Kurvenprofilen auf eine idealerweise binäre (High Contract Black/White), einfache Höhenzuordnung.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen-Eingabe</i> | Zu konvertierende Höhenzuordnung. |
| <b>Benutzerdefinierte Kurve</b> <i>Graustufen-Eingabe</i> | Farbverlauf, der die exakte Kurve/Steigung bestimmt. Im Idealfall ein linearer Verlaufsknoten, für den Sie beliebige Korrekturen wie [Tonwertkorrektur](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) oder [Gradationskurven](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) ausführen können. Nur aktiv, wenn &quot;Benutzerdefinierte Kurve verwenden&quot; auf &quot;True&quot; gesetzt ist. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Entfernung</b> <i>-1.0 - 1.0</i> | Wie weit der Effekt &quot;Abgeflachte Kante&quot; reichen soll. |
| <b>Eckentyp</b> <i>Rund, Angular</i> | Legt fest, ob das Abschrägungsprofil abgerundet oder gerade sein soll. |
| <b>Glättung</b> <i>0.0 - 5.0</i> | Gibt an, wie viel zusätzliche Glättung (Weichzeichnung) nach der abgeflachten Kante durchgeführt werden soll. |
| <b>Uneinheitlichen Weichzeichner verwenden</b> <i>False/True</i> | Ob die Glättung ungleichmäßig erfolgen soll. |
| <b>Benutzerdefinierte Kurve verwenden</b> <i>False/True</i> | Schaltet die Verwendung Ihrer eigenen benutzerdefinierten Height-Kurve um. Weitere Informationen finden Sie oben. |
| <b>Normalintensität</b> <i>0.0 - 50.0</i> | Intensität der generierten Normalmap. |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechseln Sie zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/bevel-example.png" />
        </td>
    </tr>
</table>

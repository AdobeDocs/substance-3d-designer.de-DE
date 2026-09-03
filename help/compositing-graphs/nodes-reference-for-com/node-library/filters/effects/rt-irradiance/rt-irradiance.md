---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten RT-Bestrahlungsstärke, um Informationen zur Bestrahlungsstärke in Echtzeit aus der Geometrie für realistische Beleuchtungsberechnungen zu berechnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT-Bestrahlung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 4%

---


# RT-Bestrahlung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rt-irradiance.resources/rt-irradiance-01.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Raytraced-Bestrahlung auf einem Höhen-Map-Eingang, der von einer Umgebungs-Map und einer emissive-Map generiert wird. Kann verwendet werden, um das Licht in eine Textur innerhalb eines Grafen &quot;Baking führen&quot;. Wird für gefälschte globale Beleuchtung und Leuchten verwendet.Dieser Knoten sollte aufgrund der Berechnungszeit nicht in Kombination mit der CPU-Engine (SSE) verwendet werden. Gibt zwei Zuordnungen zurück: eine Bestrahlungsausgabe, bei der die Bestrahlungsstärke auf die Material-Eingänge angewendet wird, eine Roh-Bestrahlungskarte, die nur die berechneten Bestrahlungswerte enthält.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Height</b> <i>Graustufeneingabe</i> | Height ist die einzige erforderliche Eingabe aus dem Steckplatz des Materials. Ohne sie funktioniert der Knoten nicht gut. |
| <b>Ausstrahlend</b> <i>Farbeingabe</i> | Emissive sollte in einem Format vorliegen, bei dem reines Schwarz kein Licht aussendet, jeder andere Farbwert Licht aussendet. Alpha wird ignoriert. Eine Verbindung mit diesem Steckplatz oder dem Umgebungssteckplatz ist erforderlich, um ein Ergebnis zu sehen. |
| <b>Umgebung</b> <i>Farbeingabe</i> | HDR. Lichtumgebung, mit der die Bestrahlung berechnet wird. Eine Verbindung zu diesem Steckplatz oder dem Emissive-Steckplatz ist erforderlich, um ein Ergebnis zu sehen. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Height-Skalierung</b> <i>0.0 - 1.0</i> | Skalierung zum Interpretieren des Heights bei. Wirkt sich auf das gesamte Aussehen der Szene aus. |
| <b>Qualität</b> <i>32 Strahlen, 64 Strahlen, 128 Strahlen</i> | Bestimmt die Ergebnisqualität, beeinflusst aber auch die Leistung. Weniger Strahlen bedeutet mehr Rauschen. |
| <b>Absprungwerte berechnen</b> <i>False/True</i> | Rechnerzugriffe ein-/ausschalten. Beeinflusst Qualität und Geschwindigkeit. |
| <b>Umgebungsdrehung</b> <i>0.0 - 1.0</i> | Drehen Sie die Umgebung. |
| <b>Umgebungsbelastung (EV)</b> <i>-4.0 - 4.0</i> | Der für die Umgebung zu verwendende Belichtungswert wirkt sich auf die Gesamthelligkeit des Effekts aus. |
| <b>Emissive-Intensität</b> <i>0.0 - 20.0</i> | Multiplikator für den Emissive-Eingang wirkt sich auf die Stärke der Bestrahlung durch emissive aus. |
| <b>Emissive-Farbraum</b> <i>sRGB, linear</i> | Farbraum, der zum Interpretieren der ENISsive-Eingabe verwendet wird. |
| <b>IBL Shadows in Raw Irradiance Alpha</b> <i>False/True</i> | Legen Sie fest, ob der |
| <b>Emissive LOD-Bias</b> <i>-1.0 - 1.0</i> | Die Qualität der emissive-Bestrahlung einstellen. Ein niedrigerer Wert bedeutet mehr Rauschen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-04.jpg" />
        </td>
    </tr>
</table>

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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---


# RT-Bestrahlung

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

**In:** *Filter/Effekte*

**Komplex**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Raytraced-Bestrahlung auf einem Height-Map-Eingang, der aus einer Umgebungskarte und einer Emissionskarte generiert wird. Kann verwendet werden, um Beleuchtung in eine Textur innerhalb eines Diagramms zu &quot;backen&quot;. Wird für gefälschte globale Beleuchtung und Leuchten verwendet.Dieser Knoten sollte aufgrund der Berechnungszeit nicht in Kombination mit der CPU-Engine (SSE) verwendet werden. Gibt zwei Zuordnungen zurück: eine Bestrahlungsstärke-Ausgabe, bei der die Bestrahlungsstärke auf die Materialeingänge angewendet wird, eine Roh-Bestrahlungsstärke-Karte, die nur die berechneten Bestrahlungsstärken enthält.

</td>
</tr>
</table>

## Parameter

### Eingaben

* **Height:** *Graustufeneingabe* Height ist die einzige erforderliche Eingabe aus dem Materialschlitz. Ohne sie funktioniert der Knoten nicht gut.
* **Ausstrahlend:** *Farbeingabe* Ausstrahlend sollte in einem Format vorliegen, in dem reines Schwarz kein Licht ausstrahlt, jeder andere Farbwert Licht ausstrahlt. Alpha wird ignoriert. Eine Verbindung mit diesem Steckplatz oder dem Umgebungssteckplatz ist erforderlich, um ein Ergebnis zu sehen.
* **Umgebung**: *Farbeingabe*\
  HDR-Lichtumgebung zur Berechnung der Bestrahlung mit. Eine Verbindung zu diesem Slot oder dem Emissive Slot ist erforderlich, um ein Ergebnis zu sehen.

### Parameter

* **Height-Skalierung**: *0.0 - 1.0*\
  Skalierung zum Interpretieren des Heights bei. Wirkt sich auf den gesamten Szenenlook aus.
* **Qualität**: *32 Strahlen, 64 Strahlen, 128 Strahlen*\
  Bestimmt die Ergebnisqualität, beeinflusst aber auch die Leistung. Weniger Strahlen bedeuten mehr Rauschen.
* **Rückschläge berechnen**: *False/True*\
  Rechnerzugriffe ein-/ausschalten. Beeinflusst Qualität und Geschwindigkeit.
* **Umgebungsrotation**: *0.0 - 1.0*\
  Drehen Sie die Umgebung.
* **Umgebungsbelastung (EV)**: *-4.0 - 4.0*\
  Der für die Umgebung zu verwendende Belichtungswert wirkt sich auf die Gesamthelligkeit des Effekts aus.
* **Emissionsintensität**: *0.0 - 20.0*\
  Multiplikator für den Emissionseintrag, beeinflusst die Stärke der Bestrahlung von emittierenden Stoffen.
* **Ausstrahlender Farbraum**: *sRGB, linear*\
  Farbraum, der zum Interpretieren der ENISsive-Eingabe verwendet wird.
* **IBL Shadows in Raw Irradiance Alpha**: *False/True*\
  Legen Sie fest, ob der
* **Verzerrung durch Emissions-LOD**: *-1.0 - 1.0* Die Qualität der emittierenden Strahlung abstimmen. Ein niedrigerer Wert bedeutet mehr Rauschen.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-irr-03-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/rt-irr-01-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/rt-irr-02-1.jpg" width="300px"/></div> |
| --- | --- | --- |
|  |  |  |

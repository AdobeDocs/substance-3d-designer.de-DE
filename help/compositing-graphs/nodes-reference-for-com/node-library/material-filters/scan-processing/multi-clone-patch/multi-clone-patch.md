---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Multi Clone Patch", um mehrere Texturkanäle zu klonen und auszubessern und so gescannte Materialartefakte zu reparieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch für mehrere Klone
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Patch für mehrere Klone

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-multi.png){width="128px"}

![](../../../../../../assets/clone-patch-multi-grayscale.png){width="128px"}

## Patch für mehrere Klone (Graustufen)

**In:** *Materialfilter/Scanverarbeitung*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ist die Multieingabeversion von [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Es verbindet bis zu acht Eingänge miteinander und führt für alle die exakt gleiche Kopierpatchoperation durch. Es ist hauptsächlich für die Verwendung mit Mehrfachwinkelfotos vorgesehen, die dann mit [Mehrfachwinkel zu Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) oder [Mehrfachwinkel zu Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) kombiniert werden.

>[!NOTE]
>
> Weitere Informationen finden Sie unter [Klonpatch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Weitere Informationen finden Sie unter [Materialklonpatch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) für die Materialversion.

## Parameter

### Parameter

* **Eingabeanzahl**: *1 - 8* Legt die Anzahl der Eingaben fest, die den gleichen Patch-Vorgang erhalten.
* **Ist normal (nur für Farbe)**: **Falsch/Wahr** Legt fest, ob die Eingabe eine Normalmap ist und ob die Füllmethode als solche behandelt werden soll.
* **Form**: **Quadrat, Datenträger** Legt die Stempelform fest. Wird nur als Basis verwendet.
* **Edge**
  * **Schwellenwert**: *0.0 - 1.0* Legt fest, wie weit der angeglichene Bereich reichen soll. Dieser wächst schrittweise entlang der Formen im Zielbereich. Es hat sehr wenig Wirkung mit einheitlichen Hintergründen*.*
  * **Weichzeichnen**: *0.0 - 2.0* Weichzeichnet die Kanten des Stempelbereichs, falls ein weicherer Übergang erforderlich ist.
  * **Smoothness**: *0.0 - 2.0* Rundet die Kanten der Stempelform ab und sorgt so für glattere Konturen.
  * **Rasterauflösung**: *1 - 11* Legt die Qualitätsauflösung der Füllmethode fest. Je höher der Wert, desto präziser kann die Füllmethode sein.
* **Transformationen**
  * **Quellmatrix**: *(Transformationsmatrix)*Transformiert die Quelle (Skalierung und Drehung). Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden.
  * **Quellversatz**: *-0.5 - 0.5*&#x200B;Übersetzt den Quellspeicherort. Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden. *Dieser Parameter ist wahrscheinlich der Hauptparameter, den Sie ändern möchten!*
  * **Zielmatrix**: *(Transformationsmatrix)*Transformiert die Zielposition (Skalierung und Drehung). Kann auch durch Gizmo auf der Arbeitsfläche erfolgen.
  * **Zielversatz**: *-0.5 - 0.5*&#x200B;Übersetzt den Zielspeicherort. Kann auch durch Gizmo auf der Arbeitsfläche erfolgen.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

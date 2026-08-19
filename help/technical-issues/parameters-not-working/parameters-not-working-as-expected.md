---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: Beheben Sie Probleme mit Substance-Diagrammparametern, die nicht wie erwartet funktionieren, und finden Sie Lösungen.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parameter funktionieren nicht wie erwartet
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 5%

---


# Parameter funktionieren nicht wie erwartet

Auf dieser Seite werden häufige Ursachen für Parameter aufgelistet, die in Substance 3D Designer nicht wie erwartet funktionieren, und für jeden dieser Parameter werden Schritte zur Fehlerbehebung angezeigt.

## Parameter funktioniert nicht im Vorschaumodus und veröffentlichten Substance 3D-Assets (SBSAR)

<b>![(Fehler)](../../assets/error.svg) Problem </b>

Einige der angezeigten Parameter für ein Diagramm sind *nicht aufgelistet*, wenn Sie den [Vorschaumodus](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) in Designer verwenden, oder in der Parameterliste von [Substance 3D Assets](https://helpx.adobe.com/de/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) (SBSAR), die aus diesem Diagramm veröffentlicht wurde.

<b>![(tick)](../../assets/check.svg)Empfohlene Schritte</b>

Bei den fehlenden Parametern handelt es sich wahrscheinlich um [statische Parameter](../../glossary/glossary.md), die *nicht sofort bearbeitet werden können*, nachdem das Diagramm *gekocht* wurde - d. h. verarbeitet wurde, um seinen Algorithmus schnell und effizient auszuführen. Das Kochen erfolgt in Designer jedes Mal, wenn das Diagramm *bearbeitet* oder *veröffentlicht* ist. Von solchen Einschränkungen betroffene Parameter sind im Abschnitt [Einschränkungen](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) der Seite [Verfügbarmachen eines Parameters](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) dieser Dokumentation aufgeführt.

Daher sind statische Parameter in Designer sichtbar und bearbeitbar, in einem veröffentlichten Substance 3D-Asset jedoch *ausgeblendet*. Sie können den [Vorschaumodus](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) verwenden, um diese Einschränkungen vor der Veröffentlichung auf einem Substance 3D-Asset zu sehen.

Im Folgenden finden Sie eine Liste der statischen Parameter:

| Knoten | Parameter |
| --- | --- |
| Alle Knoten | Pixelverhältnis im Kachelmodus |
| [Einheitliche Farbe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | Farbmodus |
| [Pixelprozessor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | Farbmodus |
| [Überblendung](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | Füllmethode Alpha-Füllmethode Zuschneidebereich |
| [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | Mischmodus |
| [Quadrant](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | Alpha-Eingabebildfilter für Muster |

## Falsches Ergebnis für Substance-Funktionsdiagramm, das auf den Parameter angewendet wird

<b>![(Fehler)](../../assets/error.svg) Problem </b>

Ein auf einen Knotenparameter angewendetes Substance-Funktionsdiagramm gibt nicht den erwarteten Wert aus, wenn eine negative Ganzzahl verwendet wird.

<b>![(tick)](../../assets/check.svg) Empfohlene Schritte</b>

Negative Ganzzahlen werden derzeit nicht richtig unterstützt. Verwenden Sie als Problemumgehung den negativen ganzzahligen Wert in einem [Integer2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)-Wert und extrahieren Sie ihn mit einem [Swizzle Integer](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md)-Knoten.

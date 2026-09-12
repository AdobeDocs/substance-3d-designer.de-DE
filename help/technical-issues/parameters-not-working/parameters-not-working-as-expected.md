---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: Beheben Sie Probleme mit Substance Graf-Parametern, die nicht wie erwartet funktionieren, und finden Sie Lösungen.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parameter funktionieren nicht wie erwartet
user-guide-description: ''
user-guide-title: ''
source-git-commit: f72773d86b681ce0e815c5595067b1593cdd1f0a
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 6%

---


# Parameter funktionieren nicht wie erwartet

Auf dieser Seite werden häufige Ursachen für Parameter aufgelistet, die in Substance 3D Designer nicht wie erwartet funktionieren, und für jeden dieser Parameter werden Schritte zur Fehlerbehebung angezeigt.

## Parameter funktioniert nicht im Vorschaumodus und veröffentlichten Substance 3D-Assets (SBSAR)

<b>![(Fehler)](parameters-not-working-as-expected.resources/error.svg) Problem</b>

Einige freigelegte Parameter für einen Graf sind *nicht aufgelistet*, wenn Sie den [Vorschaumodus](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) in Designer verwenden, oder in der Parameterliste von Substance 3D Assets (SBSAR) [veröffentlicht](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) in diesem Graf.

<b>![(tick)](parameters-not-working-as-expected.resources/check.svg)Empfohlene Schritte</b>

Bei den fehlenden Parametern handelt es sich wahrscheinlich um [statische Parameter](../../glossary/glossary.md), die *nicht sofort bearbeitet werden können*, nachdem der Graf *gekocht* wurde - d. h. verarbeitet wurde, um den Algorithmus schnell und effizient auszuführen. In Designer wird jedes Mal gekocht, wenn der Graf *bearbeitet* oder *veröffentlicht* ist. Die von diesen Einschränkungen betroffenen Parameter sind im Abschnitt [Einschränkungen](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) der Seite [Leg eines Parameters](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) dieser Dokumentation aufgelistet.

Daher sind statische Parameter in Designer sichtbar und bearbeitbar, in einem veröffentlichten Substance 3D-Asset jedoch *ausgeblendet*. Sie können den [Vorschaumodus](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) verwenden, um diese Einschränkungen vor der Veröffentlichung auf einem Substance 3D-Asset zu sehen.

Im Folgenden finden Sie eine Liste der statischen Parameter:

| Knoten | Parameter |
| --- | --- |
| Alle Knoten | Kachelung-Modus Pixelverhältnis |
| [Einheitliche Farbe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | Farbmodus |
| [Pixelprozessor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | Farbmodus |
| [Überblendung](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | Alpha-Überblendung-Zuschneidebereich im Mischmodus |
| [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | Mischmodus |
| [Quadrant](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | Muster Eingabebild Alpha Eingabebild Filterung |

## Falsches Ergebnis für den auf den Graf angewendeten Substance-Funktionsparameter

<b>![(Fehler)](parameters-not-working-as-expected.resources/error.svg) Problem</b>

Ein auf einen Knotenparameter angewendeter Substance-Funktionsparameter gibt nicht den erwarteten Wert aus, wenn eine Graf-Ganzzahl verwendet wird.

<b>![(tick)](parameters-not-working-as-expected.resources/check.svg) Empfohlene Schritte</b>

Negative Ganzzahlen werden derzeit nicht richtig unterstützt. Verwenden Sie als Problemumgehung den negativen ganzzahligen Wert in einem [Integer2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)-Wert und extrahieren Sie ihn mit einem [Swizzle Integer](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md)-Knoten.

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/control-nodes.html"
breadcrumb-title: ''
description: Greifen Sie in Substance 3D Designer-Funktionsknoten zu, um Flow- und Ausführungslogik zu steuern. Graf
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Steuerung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 1%

---


# Steuerungsknoten

Auf dieser Seite werden Graf von [Function Knoten](../../../../function-graphs/the-function-graph/the-function-graph.md) beschrieben, die den *Ausführungsfluss* steuern.

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Wenn...Anderer Knoten](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/IfElse_Node.jpg "If...Else-Knoten")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## If...Else

Ähnlich wie bei Programmiersprachen wird die If... Andernfalls wird die Möglichkeit eingeführt, das Ergebnis nach vordefinierten Bedingungen zu filtern.

</td>
</tr>
</table>

Sie verwenden diesen Knoten in Verbindung mit den [logischen Knoten](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) und den [Vergleichsknoten](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md), die Sie beim Erstellen der zu überprüfenden Bedingung unterstützen.

+++Eingabe-Verbindungen
<b>Bedingung</b> *Boolesche Wert*\
Die Bedingung, die die Ausgabe des Knotens steuert.

<b>If</b> *Variablentyp* Der vom Knoten ausgegebene Wert, wenn <b>Bedingung</b> *Wahr* ist.

<b>Sonst</b> *Variablentyp* Der vom Knoten ausgegebene Wert, wenn <b>Bedingung</b> *Falsch* ist.

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Sequenzknoten](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/Sequence_Node.jpg "Sequenzknoten")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Abfolge

Stellt sicher, dass ein Teil des Grafen vor einem anderen berechnet wird.

</td>
</tr>
</table>

Dies ist entscheidend für die Steuerung des Status von Variablen, wenn sie erstellt, gelesen und aktualisiert werden.

Weitere Informationen zum Sequenzknoten finden Sie auf der Seite [Verwenden der Set-/Sequenzknoten](../../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) dieser Dokumentation.

+++Eingabe-Verbindungen
<b>In</b> *Variablentyp*\
Der Teil des Grafen, der zuerst berechnet werden soll

<b>Letzte</b> *Variablentyp*\
Der Teil des Grafen, der zuletzt berechnet werden soll

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knoten &quot;Ganze Schleife&quot;](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/WhileLoop-Node.jpg "Ganzer Loop-Knoten")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Während-Schleife

Führt die Verzweigung <b>Init</b> einmal aus, und iteriert dann die Verzweigung <b>Exit Cond.</b>. und <b>Schleifentext</b> verzweigt bis zur <b>Exit-Kond.</b> Branch gibt *True* zurück.

Sobald die Schleife abgeschlossen ist, gibt der Knoten das Ergebnis der letzten Iteration des <b>Schleifentextes</b> aus.

</td>
</tr>
</table>

Loops verfügen über eine implizite maximale Anzahl von Iterationen, die durch Setzen auf -1 deaktiviert werden können.

Variablen behalten ihren Wert über Iterationen hinweg bei und können in der Exitbedingung (Exitbedingung) aufgerufen werden.\
Dies bedeutet, dass Sie jede Iteration zu einem Indexwert hinzufügen und seinen Wert in der Beendigungsbedingung überprüfen können, um die Anzahl der erforderlichen Schleifen zu steuern.

>[!IMPORTANT]
>
> Mit <b>Exit Cond.</b> verbundene Knoten und <b>Schleifenbody</b>-Verzweigungen können nicht mit anderen Verzweigungen des Grafen verbunden werden.

+++Eingangsanschlüsse
<b>Init.</b> *Variablentyp*\
Der Teil des Grafen, der vor der ersten Iteration berechnet wird, d. h. der Beginn der Schleife.

<b>Abschlusskennung </b> *Boolescher Wert*\
Die Bedingung, die &quot;true&quot; sein muss, damit die Schleife beendet wird. Er wird bei jeder Iteration neu berechnet.\
*Hinweis:* Die maximale Anzahl von Iterationen ist weiterhin auf den Parameter <b>Max. Iterationen</b> beschränkt.

<b>Schleifentext</b> *Variablentyp*\
Der Graph, der von der Schleife profitiert. Er wird bei jeder Iteration neu berechnet.

+++

+++Parameter
<b>Max. Iterationen</b> *Integer*\
Die maximale Anzahl der vom Knoten ausgeführten Iterationen.\
Der Knoten beendet die Iteration, wenn eines der folgenden Kriterien zuerst erfüllt wird: Diese maximale Anzahl wird erreicht oder die Beendigungsbedingung wird wahr .\
Dieser Höchstwert kann deaktiviert werden, indem der Wert auf *-1* festgelegt wird. An diesem Punkt kann nur die Beendigungsbedingung die Iterationen stoppen.

Einstellung &quot;Max. iterations&#39; to -1 verbessert die Leistung in kleinen Schleifen, da es einen Zähler weniger gibt, der verfolgt und aktualisiert werden kann.

Beachten Sie jedoch, wie der Knoten konfiguriert ist, da es möglich ist, eine <b>Endlosschleife</b> zu erstellen, die dazu führen kann, dass Designer nicht mehr reagiert.

+++

Sehen Sie sich dieses Tutorial zum While-Schleifen-Knoten an:

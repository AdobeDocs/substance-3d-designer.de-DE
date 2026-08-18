---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/get-nodes.html"
breadcrumb-title: ''
description: Greifen Sie auf Get-Knoten in Substance 3D Designer-Funktionsdiagrammen zu, um Variablenwerte und Daten abzurufen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variablen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 6%

---


# Variablen

Variablen sind eine Möglichkeit, <b>Werte</b> zu speichern, um sie später abzurufen (<b>Get</b>) und/oder zu ändern (<b>Set</b>).

![Substance-Funktionsdiagramm - Get float](../../../../assets/assign-getfloat.gif "Substance-Funktionsdiagramm - Get float"){zoomable="yes"}

Ein Get-Knoten übernimmt im Grunde eine dynamische Variable, die er aus der Ausgabe des Get-Nodes zur Verwendung in einer Funktion zurückgibt. Diese Get-Knoten bilden die Verknüpfung zwischen den Eingabeparametern, die in den [Diagrammeigenschaften](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html) und [Parameterfunktionen](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) definiert sind.

Jedes Mal, wenn Sie einen Get-Knoten verwenden, müssen Sie einen verfügbaren Wert aus dem Dropdown-Menü auswählen. Die Get-Knoten nehmen <b> einen Wert des entsprechenden Typs </b>. Das bedeutet, dass Sie nur gültige Optionen im Menü eines Get-Knotens sehen. Sie können niemals eine ungültige Option auswählen. Wenn eine Variable nicht verfügbar ist, bedeutet dies, dass ein Typkonflikt vorliegt

Es gibt eine Reihe von <b> &quot;System&quot;-Variablen</b>: vordefinierten speziellen Variablen, die Sie nicht selbst deklarieren können. Diese sind sehr wichtig, und für die unten stehenden Knoten wird aufgelistet, welche Systemvariablen verfügbar sind.

Wenn ein Parameter [verfügbar gemacht](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) wird, besteht er darin, eine Parameterfunktion darauf anzuwenden, die nur einen Get-Knoten des richtigen Typs enthält.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Herunterladen

</td>
<td style="border: 0;" valign="top">

### Festgelegt

</td>
<td style="border: 0;" valign="top">

### Ist definiert

</td>
</tr>
</table>

## Herunterladen

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Gleitkomma2 abrufen - Symbol](../../../../assets/fn_variables_getfloat2.png "Gleitkomma2 abrufen - Symbol"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Mit diesen Knoten können Sie den Wert einer Variablen abrufen, die im aktuellen Bereich *vorhanden ist*.

Der Name der abgerufenen Variable wird im Eigenschaften-Dock festgelegt.

</td>
</tr>
</table>

&quot;Get&quot;-Knoten einige Einschränkungen, die Sie beachten müssen:

* <b>Sie sind typisiert</b>. Daher müssen Sie sicherstellen, dass die Variable einen Wert vom gleichen Typ wie der Knoten enthält. In der Konsole werden nicht übereinstimmende Typen gemeldet.
* <b>Sie prüfen nicht, ob die Variable </b> im aktuellen Bereich vorhanden ist. In der Konsole werden nicht gefundene Variablen gemeldet.
* Achten Sie bei komplexen Funktionen, die Kontrollflussknoten wie Sequenz verwenden, auf die <b>Reihenfolge, in der Sie Variablen festlegen und abrufen</b>. Wenn Designer einen Fall von &quot;Get before Set&quot; erkennt, wird dieser in der Konsole gemeldet.

>[!NOTE]
>
> Integrierte Variablen
> 
> Mehrere Get-Knoten bieten integrierte Variablen für den Zugriff auf vorhandene Werte entsprechend dem aktuellen Kontext an, z. B.: die aktuelle Pixelposition in einem Pixelprozessor, der aktuelle Kachelmodus eines Knotens, ...
> 
> Alle integrierten Variablen sind in [dieser dedizierten Seite ](../../../../function-graphs/variables/system-variables/system-variables.md) aufgeführt.

### Knoten abrufen

+++Floats
![Gleitkommawert abrufen - Symbol](../../../../assets/fn_variables_getfloat.png "Gleitkommawert abrufen - Symbol"){width="200px"}



Float abrufen

![Gleitkomma2 abrufen - Symbol](../../../../assets/fn_variables_getfloat2.png "Gleitkomma2 abrufen - Symbol"){width="200px"}



Float2 abrufen

![Gleitkommawert abrufen3 - Symbol](../../../../assets/fn_variables_getfloat3.png "Gleitkommawert abrufen3 - Symbol"){width="200px"}



Float3 abrufen

![Gleitkomma4 abrufen - Symbol](../../../../assets/fn_variables_getfloat4.png "Gleitkomma4 abrufen - Symbol"){width="200px"}



Float4 abrufen

+++

+++Ganzzahlen
![Ganzzahl abrufen - Symbol ](../../../../assets/fn_variables_getint.png "Ganzzahl abrufen - Symbol "){width="200px"}



Integer abrufen

![Ganzzahl abrufen2 - Symbol ](../../../../assets/fn_variables_getint2.png "Ganzzahl abrufen2 - Symbol "){width="200px"}



Integer2 abrufen

![Ganzzahl abrufen3 - Symbol](../../../../assets/fn_variables_getint3.png "Ganzzahl abrufen3 - Symbol"){width="200px"}



Integer3 abrufen

![Ganzzahl abrufen4 - Symbol ](../../../../assets/fn_variables_getint4.png "Ganzzahl abrufen4 - Symbol "){width="200px"}



Integer4 abrufen

+++

+++Sonstige
![Boolesch abrufen - Symbol](../../../../assets/fn_variables_getboolean.png "Boolesch abrufen - Symbol"){width="200px"}



Booleschen Wert abrufen

![Zeichenfolge abrufen - Symbol](../../../../assets/fn_variables_getstring.png "Zeichenfolge abrufen - Symbol"){width="200px"}



Zeichenfolge abrufen

+++

## Festgelegt

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Festlegen: Knotensymbol ](../../../../assets/fn_variables_set.png "Festlegen: Knotensymbol "){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Text

</td>
</tr>
</table>

## Ist definiert

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![&quot; ist definiert: Knotensymbol ](../../../../assets/fn_variables_isdefined.png "Ist definiert: Knotensymbol "){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Text

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/visible-if-control-visibility-of-inputs-outputs-and-parameters.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie die Sichtbarkeit von Parametern in Substance 3D Designer mithilfe von "visible if"-Expressions auf der Grundlage von Bedingungen steuern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Visible if expressions
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sichtbar, wenn Expressions
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# Sichtbar, wenn Expressions

Mit dem Ausdruck &quot;Sichtbar, wenn&quot; können Sie <b>die Sichtbarkeit </b> von Eingängen, Ausgaben und Parametern in Diagrammen steuern.

Wenn [Parameter &#x200B;](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) verfügbar gemacht werden, sollten Sie Parameter oder Knotenkonnektoren basierend auf dem Status anderer Parameter ein- oder ausblenden. Beispiel: Ein Schieberegler wird nur angezeigt, wenn eine boolesche Parameterschaltfläche auf &quot;`true`&quot; festgelegt ist, da er sonst keine Auswirkungen hätte und Benutzer möglicherweise verwirrt werden.

Um dies zu erreichen, können Sie einen *logischen Ausdruck* in die <b>Visible if</b>-Eigenschaft von eingeben:

* [-Eingabeparameter eines Diagramms](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md);
* Knoten [Eingabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) eines Diagramms;
* Knoten &quot;[Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)&quot; eines Diagramms.

![Sichtbarkeit von Eingabeparametern umschalten](visible-if-control-visibility-of-inputs-outputs-and-parameters.resources/visible-if-control-visibility-of-inputs-outputs-and-parameters-01.gif "Sichtbarkeit von Eingabeparametern umschalten"){width="512px"}

Wenn die Auswertung des logischen Ausdrucks &quot;`true`&quot; ergibt, wird der Parameter, die Eingabe oder die Ausgabe in allen [Instanzknoten](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) angezeigt, die das aktuelle Diagramm darstellen. Andernfalls ist sie *ausgeblendet*.

Komplexe Bedingungen sind möglich, sofern der logische Ausdruck, der diese Bedingungen angibt, gültig ist.

>[!NOTE]
>
> Caveats
> 
> * Dieses Feature *only* wirkt sich darauf aus, ob ein Parameter oder ein Connector in der Benutzeroberfläche angezeigt wird, und hat *keine Auswirkungen* auf die Berechnungen und das Ergebnis eines Diagramms.
> * Wenn eine Funktion für einen Parameter verfügbar gemacht oder angewendet wird, der in &#39;Visible if&#39;-Anweisungen verwendet wird, werden diese Anweisungen *ignoriert* und standardmäßig auf &#39;true&#39; festgelegt.

>[!IMPORTANT]
>
> Diese Funktion kann für das Substance 3D-Ökosystem genutzt werden, ist aber in einigen Integrationen möglicherweise nicht verfügbar. Wenn diese Option nicht unterstützt wird, wird die Sichtbarkeitsbedingung standardmäßig auf &quot;`true`&quot; festgelegt.

## Schreiben von &quot;Visible if&quot;-Ausdrücken

### ZUGRIFF AUF EINGABEPARAMETER

&quot;Beliebig&quot; Wenn für &quot;Ausdruck&quot; mindestens eine Eingabe erforderlich ist, kann dies durch die folgende Syntax erfolgen:

```
input.identifier 

input["identifier"]
```


>[!WARNING]
>
> Der **Bezeichner** muss der *genaue* Name der **Bezeichner**-Eigenschaft eines vorhandenen Eingabeparameters sein, und er muss *Groß- und Kleinschreibung beachten* eingegeben werden. *kann nicht* auf einen Parameter über dessen Bezeichnung verweisen.\
>  Wenn kein referenzierter Parameter vorhanden ist oder der logische Ausdruck ungültig ist, wird eine *Warnung* in der **Visible if**-Eigenschaft angezeigt.

### VERFÜGBARE OPERATOREN

Die Felder &quot;Sichtbar wenn&quot; akzeptieren die folgenden Parameter:

* Boolesche, Float- und Integer-Eingaben.
* `true` und `false` Werte (Groß- und Kleinschreibung beachten, keine Großbuchstaben!)
* `.x` : auf den Unterparameter zugreifen
* `&&`<b> </b> und
* `||`<b> </b> oder
* `!`<b> </b> nicht
* `<`<b>, </b>`>`<b>, </b>`<=`<b>, </b>`>=`<b>, </b>`==`<b>, </b>`!=`: Vergleich
* `()` : Klammern

### MUSS IMMER AUF BOOLESCHE AUSWERTEN

Ein &quot;Sichtbar, wenn Ausdruck als Bedingung für eine &quot;IF&quot;-Anweisung verwendet wird, d. h., er muss immer `true` oder `false` ergeben.

* Boolesche Werte können direkt als Bedingung ausgewertet werden. Eine einfache Schaltfläche mit einem booleschen Wert erfordert nicht mehr als diesen Wert. Siehe nachstehende Beispiele, erster Fall;
* Für nicht boolesche Parameter ist im Allgemeinen ein *Vergleichsvorgang* erforderlich. Vergleichsoperatoren finden Sie oben, Beispiele unten.
* Einige nicht-boolesche Werte können *wahrheitsgetreu* oder *falsch* sein, was bedeutet, dass sie als `true` von `false` ausgewertet werden können - z. B. Ein Ganzzahl-Wert von `0` wird als false ausgewertet.

## Beispiele

| Bedingung (&quot;If&quot;) | Formel | Anmerkung |
| --- | --- | --- |
| Wahr | ` input["my_input"]   input.my_input `  ` input["my_input"] == true   input.my_input == true ` | my\_input ist ein boolescher Wert. |
| Falsch | ` !input["my_input"]   !input.my_input `  ` input["my_input"] == false   input.my_input == false `  ` input["my_input"] != true   input.my_input != true ` | my\_input ist ein boolescher Wert. |
| Unterer als | ` input["my_input"] < 3   input.my_input < 3 ` | my\_input ist eine Ganzzahl |
| Equal | ` input["param1"] == 2   input.param1 == 2 ` | param1 ist ein float- oder integer-Wert |
| Unterer als | ` input["my_input"].y < 3   input.my_input.y < 3 ` | my\_input ist ein float- oder integer-Wert mit einer oder mehreren Komponenten - z.B. float2(x, y), integer3(x, y, z) |
| Or | ` input["param1"] \|\| input["param2"]   input.param1 \|\| input.param2 ` | param1 und param2 sind boolesche Werte |
| Und | ` input["param1"] > 0 && input["param2"] > 1   input.param1 > 0 && input.param2 > 1 ` | param1 und param2 sind float- oder integer-Werte. |

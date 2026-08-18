---
title: Splint V2 zu Maske formen
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > Generator > Muster > Formspritzer v2 zum Maskieren
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---


# Splint V2 zu Maske formen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Form platzieren v2 zum Maskensymbol](shape-splatter-v2-to-mask.png "Form platzieren v2 zur Maske")

<b>In:</b> Generator > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Berechnet eine Maske aus einer Auswahl von Formen, die vom [Shape-Splatter v2](../shape-splatter-v2/shape-splatter-v2.md)-Knoten generiert werden.<br><br>Verfügbare Optionen umfassen die Zufallsauswahl sowie die Auswahl von Formenbereichen anhand einer eindeutigen Kennung und/oder Material-ID/Muster-ID*.<br><br>Formen werden vom [Shape-Splatter v2](../shape-splatter-v2/shape-splatter-v2.md)-Knoten aus ihrer <i>Height-Überblendung</i> mit dem Hintergrund-Height vormaskiert.<br>Sowohl der Hintergrund als auch die nicht ausgewählten Formen sind reines Schwarz. (d. h. ein Wert von 0)<br><br><b>*:</b> Einer der von der Shape-Splatter-UVW-Eingabe abgerufenen Werte ist entweder die Material-ID oder die Muster-ID, abhängig vom <b>Shape-Typ</b>, der im Shape-Splatter-v2-Knoten verwendet wird:<br>- <i>SDF/primitive</i>: Materialkennung<br>- <i>Mustereingabe/-Rasteratlas:</i> Musterkennung, d. h. der Index des Musters in der Liste/im Atlas.

</td>
</tr>
</table>

>[!INFO]
>
> Dieser Knoten erfordert Eingabedaten, die vom Knoten [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) generiert werden.
> 
> Weitere Knoten in der Shape-Splatter-V2-Familie:
> * [Graustufen-Zuordnungs-Splatter v2](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md)
> * [Zuordnungsfarbe für Shape-Splatter v2](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md)

>[!TIP]
> 
> Das [**-Materialmuster &quot;Rusty bolts&quot;**](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample) ist verfügbar, um mit Shape-Splatter v2-Knoten zu beginnen.
> 
> Weitere Informationen zu Konzepten und Workflows mit SDF-Funktionen finden Sie auf der entsprechenden Seite: [Arbeiten mit SDF-Funktionen](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Eingaben

|                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:----------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Splatter UVW</b> *Farbe* | <b>R</b> - U-Komponente der UVs der Formen.<br><b>G</b> - V-Komponente der UVs der Formen.<br><b>B</b> - Height der Formen. (W)<br><b>A</b> - Packed data:<br> - <i>Integer part:</i> Der eindeutige Bezeichner der Formen. (ID)<br> - <i>Bruchteil:</i> hängt vom <b>Formtyp ab</b>: Materialkennung bei SDF/primitive, Musterkennung* bei Mustereingabe/Rasteratlas.<br><br><b>*:</b> Die Musterkennung ist der Indexwert der Form in der Liste/im Atlas. |

<a name="outputs"></a>

## Ausgaben

|               |                                           |
|:--------------|:------------------------------------------|
| <b>Ausgabe</b> | Die berechnete Maske der ausgewählten Formen. |

<a name="parameters"></a>

## Parameter

|                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Ausgabe</b> *Integer* | Die für die ausgewählten Formen in der Ausgabemaske verwendeten Werte.<br><br>- <b>Binärmaske:</b> Ausgewählte Formen verwenden alle den Wert 1.<br>- <b>Form-ID (Ganzzahl):</b> Ausgewählte Formen verwenden ihren eindeutigen Bezeichner. (ID)<br>- <b>Material ID (Ganzzahl):</b> Ausgewählte Formen verwenden ihre Material-ID.<br>- <b>Form ID (normalisiert):</b> Ausgewählte Formen verwenden ihre eindeutige Kennung (ID), die dem Bereich [0, 1] von der niedrigsten ausgewählten ID bis zur höchsten zugeordnet ist.<br>- <b>Material ID (normalisiert):</b> Ausgewählte Formen verwenden ihre Material-ID, die dem Bereich [0, 1] von der niedrigsten ausgewählten Material-ID bis zur höchsten zugeordnet ist. |
| <b>Startbereich für Shape-ID</b> *Integer* | Die eindeutige Kennung (ID) der Form, die als Anfang des Auswahlbereichs verwendet wird. (Inbegriffen) |
| <b>Endbereich der Shape-ID</b> *Integer* | Die eindeutige Kennung (ID) der Form, die als Ende des Auswahlbereichs verwendet wird. (Inbegriffen) |
| <b>Offset für Shape-ID</b> *Integer* | Verschiebt die eindeutigen Bezeichner der Formen im Kontext des Auswahlbereichs um den angegebenen Wert.<br><br>Dies erleichtert das Versetzen der aktuellen Auswahl um den angegebenen Wert, ohne die Start- und Endbegrenzungen manuell anpassen zu müssen. |
| <b>Kombination aus Material/Muster-ID-Maske</b> *Integer* | Es wurde der logische Operator angegeben, der zum Kombinieren der Auswahl durch einen eindeutigen Bezeichner (ID) mit der Auswahl durch Material-ID/Muster-ID verwendet wird.<br><br>- <b>Keine:</b> Ignorieren Sie die Material-ID/Muster-ID vollständig für die Auswahl.<br>- <b>AND:</b> Ausgewählte Formen müssen sowohl in den ID- als auch in den Material-ID/Muster-ID-Bereichen enthalten sein. (Umfasst weniger Formen)<br>- <b>OR:</b> Ausgewählte Formen müssen entweder in den ID- oder den ID-/Pattern-ID-Bereichen enthalten sein. (Umfasst weitere Formen) |
| <b>Startbereich für Material/Muster-ID</b> *Integer* | Die Material-ID oder Muster-ID*, die als Beginn des Auswahlbereichs verwendet wird. (Inbegriffen)<br><br><b>*:</b> Weitere Informationen finden Sie in der Knotenbeschreibung. |
| <b>Endbereich Material/Muster-ID</b> *Integer* | Die Material-ID oder Muster-ID*, die als Ende des Auswahlbereichs verwendet wird. (Inbegriffen)<br><br><b>*:</b> Weitere Informationen finden Sie in der Knotenbeschreibung. |
| <b>Zufällige Formmaske</b> *Gleitend* | Ein Faktor für die zufällige Maskierung von Formen, wobei 1 bedeutet, dass alle Formen maskiert sind. |


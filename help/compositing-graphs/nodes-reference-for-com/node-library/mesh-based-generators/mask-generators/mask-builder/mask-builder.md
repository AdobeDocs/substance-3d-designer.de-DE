---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/mask-builder.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Maskenbildner", um mehrere Maskeneingaben zu kombinieren und komplexe Maskenmuster für Materialeffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Mask Builder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maskenbildner
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---


# Maskenbildner

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mask-builder.png){width="128px"}

## Maskenbildner

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Das ist so ziemlich die Designer-Version von Painters Mask Builder.

Es ist ein kompliziertes Tool, das als allumfassender Maskenbildner gedacht ist, der auf durch Baking erzeugte Map, Benutzerparametern und Schmutz-Mustern und -Maps basiert. Es ist vor allem als ein sehr fortgeschrittener, voller Kontrolle Knoten in Falten Dirt und Kantenverschleiß zu mischen. Dieser Knoten ist leistungsstark genug, um jeden anderen Maskengenerator nachzuahmen.

Es sind keine Backs explizit erforderlich, aber je mehr Sie angeben, desto mehr kann dieser Knoten tun.

## Parameter

### Eingaben

* **Ambient-Verdeckung**: *Graustufen-Eingabe*
* **Krümmung**: *Graustufen-Eingabe*
* **Normaler Weltraum**: *Farbeingabe*
* **Schmutz-Eingabe**: *Graustufen-Eingabe*
* **Schmutz-Eingang 2**: *Graustufen-Eingabe*
* **Streuung-Eingabe**: *Graustufen-Eingabe*\
  Benutzerdefinierter Streuung-Stempel, der erforderlich ist, um die Parameter für die Streuung zu verwenden.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.
* **Position**: *Farbeingabe*\
  Wird für Triplanar- und Top-Bottom-Effekte verwendet.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt die Gesamtstärke des Effekts fest, die nach und nach zum Vorschein kommt.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Umkehren**: *False/True*\
  Kehrt das Ergebnis um. Nützlich, um das Gegenteil der Maske zu erreichen, die Sie erstellen.
* **Triplanar verwenden**: *Falsch/Wahr* Aktiviert die triplanare Projektion und vermeidet alle Nähte mit Schmutz-Maps.
* **Triplanarer Mischkontrast**: *0.0 - 1.0* Legt den Kontrast für die triplanare Überblendung fest.
* **Schmutz**: *0.0 - 1.0* Legt die Menge an Schmutz fest, die global gemischt werden soll.
* **Schmutz**
  * **Skalierung**: *0 - 10* Legt die Skalierung des globalen Schmutzes fest.
  * **Benutzerdefinierten Schmutz verwenden**: *Falsch/Wahr* Aktiviert die benutzerdefinierte Schmutz-Eingabe.
  * **Sekundärer benutzerdefinierter Schmutz**: *0.0 - 1.0* Aktiviert einen zweiten benutzerdefinierten Schmutz.
  * **Umkehren**: *False/True*\
    Kehrt den Schmutz um.
* **AO**: *-1.0 - 1.0* Legt fest, inwieweit der Effekt in verdeckten AO-Bereichen angezeigt werden soll. Kann mit der folgenden Gruppe optimiert werden.
* **AO**
  * **Bereich**: *0.0 - 1.0* Legt den Schwellenwert oder den Bereich für das Erscheinungsbild von Dirt fest.
  * **Kontrast**: *0.0 - 1.0*\
    Passt den Kontrast des AO-Effekts an.
  * **Rauschen**: *0.0 - 1.0* Legt den Umfang des Rauschens/Schmutzes fest, der in den AO-Effekt übergeht.
  * **Rauschskalierung**: *0 - 10* Legt die Skalierung des AO-Rauschens/Schmutzes fest.
  * **Störungstyp**: *Bereiche, Wolke, Feuchtigkeit, weißes Rauschen* Wechselt zwischen 4 verschiedenen Arten von AO-Rauschen.
  * **Umkehren**: *False/True*\
    Kehrt die Interpretation der AO-Map um: Rauschen tritt in hellen AO-Bereichen auf, in dunklen nicht.
* **Krümmung**: *0.0 - 1.0* Legt fest, wie viel Effekt an den Kanten der Krümmung angezeigt werden soll; kann sowohl konvex als auch konkav sein. Optimiere dies mit der Gruppe unten.
* **Krümmung**
  * **Konvexbereich**: *-1.0 - 1.0* Legt fest, wie viel Effekt an konvexen (hellen) Krümmungskanten angezeigt werden soll.
  * **Konvexkontrast**: *0.0 - 1.0* Legt den Kontrast des Effekts &quot;Konvex&quot; fest.
  * **Konvex invertieren**: *Falsch/Wahr* Kehrt die Interpretation der konvexen Kanten um.
  * **Konkaver Bereich**: *-1.0 - 1.0* Legt fest, wie viel Effekt an konkaven (dunklen) Krümmungskanten angezeigt werden soll.
  * **Konkaver Kontrast**: *0.0 - 1.0* Legt den Kontrast des konkaven Bereichs fest.
  * **Konkave Umkehr**: *Falsch/Wahr* Kehrt die Interpretation der konkaven Kanten um.
  * **Smoothness**: *0.0 - 16.0* Umfang der Weichzeichnung und Glättung, die auf Krümmungskanten angewendet werden soll.
  * **Level-Verstärkung**: *0.0 - 1.0* Zusätzlicher Booster, wenn der Effekt nicht sichtbar genug ist.
  * **Rauschen**: *0.0 - 1.0* Legt den Einfluss des Rauschens/Schmutzes auf den Kurveneffekt fest.
  * **Rauschskalierung**: *0 - 10* Legt die Skalierung des Rauschens fest.
  * **Störungstyp**: *Störstellen, Wolke, Feuchtigkeit, weißes Rauschen* Wählen Sie zwischen 4 verschiedenen Störungstypen.
* **Verlauf nach oben/unten**: *-1.0 - 1.0*&#x200B;Überblendungen oder Masken mit einem Verlauf von oben nach unten, der auf der Positionszuordnung basiert. Positive Werte machen die Dinge heller, negative Werte maskieren vorhandene Effekte.
* **Verlauf**
  * **Bereich**: *0.0 - 1.0* Legt die Position des Verlaufs fest.
  * **Kontrast**: *0.0 - 1.0*\
    Passt den Kontrast des Verlaufs an.
  * **Umkehren**: *False/True*\
    Kehrt den Verlauf um. Tauscht unten und oben aus.
* **Normaler Weltraum**: *0.0 - 1.0*&#x200B;Ähnlich wie &quot;Top/Down Gradient&quot;, jedoch mit der Positionskarte und in sechs Richtungen, ähnlich einer gefälschten Beleuchtung. Positive Werte werden aufgehellt, negative Werte werden abgedunkelt.
* **Normaler Weltraum**
  * **höchste Intensität**: *-1.0 - 1.0*
  * **Intensität unten**: *-1.0 - 1.0*
  * **Intensität vorne**: *-1.0 - 1.0*
  * **Back Intensity**: *-1.0 - 1.0*
  * **Intensität rechts**: *-1.0 - 1.0*
  * **Linke Intensität**: *-1.0 - 1.0*
* **Scratches**: *-1.0 - 1.0* Vermischt Kratzer in die weißen Bereiche.
* **Scratches**
  * **Betrag**: *0 - 4096* Legt die Gesamtzahl der Kratzer fest.
  * **Skalierung**: *0.0 - 1.0* Legt die Skalierung einzelner Kratzer fest.
* **Streuung**: *-1.0 - 1.0* Streuung eines benutzerdefinierten Stempels in weißen Bereichen.
* **Streuung**
  * **Skalierung**: *0 - 50* Gesamtskala des Effekts.
  * **Dichte**: *0.0 - 1.0* Streuungsdichtesteuerung, Zahl, die angezeigt werden sollte.
  * **Größe**: *0.0 - 4.0* Größe des Streustempels.
  * **Größenänderung**: *0.0 - 1.0* Variation innerhalb der Stempelgröße.
  * **Deckkraftvariation**: *0.0 - 1.0* Variation innerhalb der Stempeldeckkraft.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Planares Licht , um HDRI-Umgebungen planare Lichtquellen für die Steuerung der gerichteten Beleuchtung hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flächenlicht
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# Flächenlicht

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-plane-light.png){width="200px"}

## Flächenlicht

**In:** *3D-Ansicht/HDRI-Werkzeuge*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine sphärisch projizierte Ebenenform. Die Ebene kann mithilfe der Eingabeparameter in 3D platziert und ausgerichtet werden.

Es unterscheidet sich von dem einfacheren [Formenlicht](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) dadurch, dass es über erweiterte Platzierungsoptionen außerhalb der einfacheren Musterprojektion verfügt und mehr Abstand zum Ursprung und Masken angewendet werden können, ähnlich wie [Linienlicht](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md).

## Eingaben

* **Hintergrundbildeingabe**: *Farbeingabe*\
  Optionaler Hintergrund, auf dem das erzeugte Licht komponiert werden soll.
* **Shape Image Input**: *Farbeingabe*\
  Optionales Bild für die Zuordnung zum Linienlicht. Wird nur verwendet, wenn der Formfarbmodus auf &quot;Bildeingabe&quot; eingestellt ist.
* **Musterbildeingabe**: *Graustufen-Eingabe*\
  Benutzerdefiniertes Musterbild, das verwendet wird, wenn der Parameter &quot;Muster&quot; auf &quot;Bildeingabe&quot; eingestellt ist.

## Parameter

* **Positionsmodus**: *Boden/Decke, Abstand zum Ursprung, Weltpositionen*\
  Sie können aus drei verschiedenen Platzierungsmodi auswählen. Boden/Decke und Abstand zum Ursprung unterstützen die Bearbeitung in der 2D-Ansicht, Weltpositionen können nur über Eigenschaften geändert werden, aber es wird eine exaktere Platzierung unterstützt.
* **Grundraster anzeigen**: *False/True*\
  Hilfsfunktion, um das Zeichnen eines Debug-Bodenrasters zu ermöglichen. Hilft bei der Schätzung der Position von Linien im Raum.
* **Positionskoordinaten**
  * **Vektor nach oben**: *Z nach oben, J nach oben*\
    Nur mit dem Modus &quot;Weltposition&quot; bestimmen Sie die Ausrichtung des Koordinatensystems.
  * **Ebene UV-Position**:\
    Nur mit Boden / Decke und Abstand zum Ursprung. Legt die Ebenenposition im UV-Raum fest.
  * **Weltposition der Ebene**: *-2.0 - 2.0*\
    Nur im Modus &quot;Weltpositionen&quot;. Legt den Weltraum für die Ebenenposition fest. Keine 2D-Ansichtsinteraktion unterstützt.
  * **Absolutes Height der Ebene**: *0.0 - 1.0*\
    Nur bei der Positionsart &quot;Boden/Decke&quot; wird das absolute Height von der Decke eingestellt. Verwenden Sie &quot;Bodenraster anzeigen&quot;, um die Position besser zu schätzen.
  * **Abstand zum Ursprung**: *0.0 - 1.0*\
    Nur mit Abstand zum Ursprung-Positionsmodus. Legt für beide Punkte den Abstand vom Mittelpunkt des Panoramas fest.
* **Formfarbmodus**: *RGB, Temperatur (Kelvin), Bildeingabe*\
  Wählen Sie die Methode aus, die zum Festlegen der Formfarbe verwendet werden soll. Image Input ermöglicht die Verwendung des zweiten Eingangssteckplatzes.
* **Farbe**: *(Farbwert)*\
  Nur bei RGB als Formfarbmodus. Wählt Farbe für die Form.
* **Temperatur**: *800.0 - 20000.0*\
  Nur, wenn der Formfarbmodus auf &quot;Temperatur&quot; eingestellt ist. Legt den Kelvin-Wert für die Formfarbe fest.
* **UV-Modus für Formenbild**: *Dehnen, Nur Mitte dehnen, Wiederholen + Abstand*\
  Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Legt fest, wie das Bild auf die Linienform angewendet wird, und bestimmt das Verhalten der UV-Wiederholung.
* **Abstand für wiederholte Formbilder**: *0.0 - 1.0*\
  Nur bei &quot;Formfarbmodus&quot; auf &quot;Bildeingabe&quot; und &quot;UV-Modus&quot; auf &quot;Wiederholen + Abstand&quot; eingestellt. Legt den Abstand fest, der zwischen den Bildern auf einer Linie liegt.
* **Gamma für Formenbild**: *sRGB, linear*\
  Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Legen Sie fest, wie die Formbildeingabe interpretiert wird.
* **Exposition (EV)**: *0.0 - 10.0*\
  Belichtungswert für generierte Form festlegen, optimal abgestimmt auf den Belichtungswert des Hintergrundbilds.
* **Ebenenskalierung**: *0.0 - 1.0*\
  Legen Sie die einheitliche Skalierung der Form &quot;Ebene&quot; fest.
* **Ebenengröße**: *0.0 - 1.0*\
  Festlegen einer ungleichmäßigen Größe der Form &quot;Ebene&quot;.
* **Ebenendrehung**: *0.0 - 1.0*\
  Ebene entlang ihrer Mittelachse drehen.
* **Muster**: *Quadrat glätten, Quadrat scharf, Kegel, Hemisphäre, Bildeingabe*\
  Wählen Sie die zu verwendende Musterform aus.
* **Musterhärte**: *0.0 - 1.0*\
  Härte/Kontrast für das Muster festlegen.
* **Muster-UV-Modus**: *Dehnen, nur Mittel dehnen*\
  Legen Sie fest, wie eine sekundäre Mustermaske verwendet wird, die über dem Formenbild angewendet wird.
* **Bodenbeschneidung aktivieren**: *False/True*\
  Aktivieren Sie diese Option, wenn die Ebene durch eine Grundebene beschnitten werden kann oder immer noch angezeigt wird, wenn sie darunter liegt. Verwenden Sie &quot;Bodenraster anzeigen&quot;, um dies besser einzuschätzen.
* **Ground-Height**: *-2.0 - 0.0*\
  Passe das Height der Grundebene für die Beschneidung an.
* **Hintergrundeingabe aktivieren**: *False/True*\
  Schaltet die Verwendung des optionalen Hintergrundbilds um. Kompositionen generierten Licht auf dem Hintergrund.
* **Hintergrundfarbe**: *(Farbwert)*\
  Wenn die Option &quot;Hintergrundeingabe&quot; nicht verwendet wird, legen Sie hier einen Wert für einen einfarbigen Hintergrund fest.
* **Gamma im Hintergrund**: *sRGB, linear* Wenn die Hintergrundeingabe verwendet wird, legen Sie fest, wie die Hintergrundeingabe interpretiert werden soll.

## Beispielbilder

![](../../../../../../assets/plane-light-ex.gif)

</td>
</tr>
</table>

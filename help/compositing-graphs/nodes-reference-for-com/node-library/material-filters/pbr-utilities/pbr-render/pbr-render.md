---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
breadcrumb-title: ''
description: Verwenden Sie den PBR-Rendering-Knoten, um physikalisch basierte Materialien mit realistischer Beleuchtung für die Vorschau des Materialaussehens zu rendern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR-Rendering
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 1%

---


# PBR-Rendering

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render.png){width="250px"}

**In:** *Materialfilter/PBR-Dienstprogramme*

**Komplex**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Rendert ein PBR-Material auf eine Kugel, eine Ebene oder einen Zylinder mithilfe von Image Based Lighting (IBL). Dies ist eine Render-Engine innerhalb eines Knotens, die sehr nützlich sein kann, um Miniaturen, Vorschauen oder 2D-Assets zu generieren. Es handelt sich nicht um ein Rendering wie die 3D-Ansicht, sondern um eine tatsächliche Textur, die in Ihrem Diagramm generiert wird.

Dieser Knoten erfordert, dass mindestens ein vollständiges PBR-Material angeschlossen wird. Idealerweise verwenden Sie die Link Creation Modes, um das Material mit dem PBR-Rendering zu verbinden. Darüber hinaus benötigen Sie eine kugelförmig ausgewickelte HDRI-Umgebung für den Render, aus dem die Beleuchtung berechnet werden soll. Testmaterialien finden Sie unter PBR-Materialien. Umgebungszuordnungen finden Sie unter [3D-Ansicht in der Bibliothek.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/3d-view-library.md)

</td>
</tr>
</table>

>[!WARNING]
>
> **CPU-Modul (SSE2)**
> 
> Der PBR-Rendering Node ist sehr schwer und funktioniert nicht gut mit der SSE2 CPU Engine. Wechseln Sie durch Drücken von F9 zu einer anderen Engine, wenn der Knoten extrem schlecht funktioniert.

## Eingaben

* **Materialkanal** **Eingaben**\
  Mehrere Materialeingaben werden verwendet, um das Material auf der Geometrie zu rendern:
  * Grundfarbe
  * Normale
  * Ausstrahlend
  * Rauheit
  * Metallisch
  * Reflexionsebene
  * Höhe
  * Umgebungsverdeckung
  * Deckkraftmaske
  * Anisotropiestufe
  * Anisotropiewinkel
  * Lichtdurchlässigkeit
  * Skalierung des Streuungs-Abstands
* **Objektiv-Dirt-Map**: *Graustufen-Eingabe* Benutzerdefinierte Karte für Dirt auf dem Objektiv, die angezeigt wird, wenn Blendenflecken sichtbar sind.
* **Objektivblendenkarte**: *Graustufen-Eingabe* Kann verwendet werden, um Bokeh, eine unscharfe Form, zu überschreiben. Je kontrastreicher, desto sichtbarer. Denke daran, dass nur ein Kreis innerhalb der Textur aufgenommen wird, sodass jede Form in einen Kreis passen muss.
* **Hintergrundeingabe**: *Farbeingabe*\
  Benutzerdefinierte Zuordnung wird als Hintergrund verwendet, wenn der Parameter **Hintergrundmodus** auf *Hintergrundeingabe* festgelegt ist
* **Umgebungszuordnung**: *Farbeingabe* Umgebungszuordnung zum Berechnen der Beleuchtung verwendet. Muss sphärisch abgebildet und in HDR vorliegen.

Ausgaben

* **Schönheit**\
  Das endgültige Rendering
* **Rohbestrahlung**\
  Die Bestrahlungsdaten des endgültigen Renderings\
  *Alpha:* Deckkraftzuordnung
* **Raw-Specular**\
  Die Specular-Daten des endgültigen Renderings\
  *Alpha:* Specular-Schattenkarte
* **Normaler Weltraum**\
  Die Daten der Weltraum-Normalen des endgültigen Renderings\
  *Alpha:* Weltraum-Height-Map
* **Normaler Tangentialraum**\
  Der Tangentenraum normalisiert die Daten des endgültigen Renderings.\
  *Alpha:* Tangentialraum-Height-Map
* **UVs**\
  Die UV-Daten des endgültigen Renderings\
  *Alpha:* Deckkraftzuordnung

## Parameter

* **Form**: *Kugel, Ebene, Zylinder*\
  Legt die zum Rendern verwendete Form fest. Benutzerdefinierte Formen sind nicht möglich.
* **Versatz-Intensität**: *0.0 - 0.5* Stellen Sie die Intensität des Versatzes vom Height ein.
* **Umgebungsrotation**: *0.0 - 1.0*\
  Dreht die Lichtumgebung. Vordrehung im Vergleich zur Bewegung der Kamera.
* **Hintergrundmodus**: *Farbe, Umgebung, Umgebungslicht, Hintergrundeingabe*\
  Legt fest, was im Hintergrund angezeigt wird. Die Farbe ist eine Volltonfarbe, &quot;Umgebung&quot; ist die Karte, die Sie mit einem optionalen Weichzeichner angeschlossen haben. Umgebungslicht ist eine sehr verschwommene Version der Umgebung.
* **Hintergrundfarbe**: *(Farbwert)*\
  Nur verfügbar, wenn der Hintergrundmodus auf &quot;Farbe&quot; eingestellt ist.
* **Hintergrundunschärfe der Umgebung**: *0.0 - 1.0*\
  Nur verfügbar, wenn der Hintergrundmodus auf &quot;Umgebung&quot; eingestellt ist.
* **Form**
  * **Skalierung**: *0.0 - 2.0*\
    Lege die Skalierung für die Kugel fest.
  * **Ebenengröße**: *0.0 - 1.0*\
    Legen Sie die Skalierung für die Ebene fest.
  * **Zylinderradius**: *0.0 - 1.0*\
    Legen Sie den Radius für den Zylinder fest.
  * **Zylinderlänge**: *0.0 - 1.0*\
    Stellen Sie die Länge für den Zylinder ein.
  * **Drehung**: *0.0 - 1.0*\
    Dreht die Form, ohne die Beleuchtung zu drehen.
  * **Drehrichtung**: *0.0 - 1.0*\
    Stellt die Drehachse in 2D ein.
  * **Drehung um Richtung**: *0.0 - 1.0*\
    Dreht die Form auf der Drehachse.
  * **Formenposition**: *-1.0 - 1.0*\
    Verschiebt Formen.
  * **UV-Kachel**: *1.0 - 6.0*\
    Legt die Menge der UV-Kachelung fest.
  * **Sphere-UV-Skalierung**: *0.0 - 4.0*\
    Legt die Skalierung der UVs auf der Kugel fest.
  * **Ebene UV-Skalierung**: *1.0 - 4.0*\
    Legt die Skalierung der UVs auf der Ebene fest.
  * **UV-Skalierung des Zylinders**: *1.0 - 6.0*\
    Legt die Skalierung der UVs auf dem Zylinder fest.
  * **UV-Versatz**: *0.0 - 1.0*\
    Versetzt UVs
  * **UVs neigen**: *False/True*\
    Neigt UVs um 45 Grad für die Kugel.
* **Kamera**
  * **Exposition**: *-4.0 - 4.0*\
    Legt die Kamerabelichtung fest.
  * **Farbtonzuordnung**: *Linear, ACES, Filmic Hejl*\
    Legen Sie fest, welche Farbtonzuordnungslösung für das endgültige Bild verwendet werden soll.
  * **Kameramodus**: *Perspektive, Orthographie*\
    Wechseln der Kamera zwischen zwei Projektionsmodi.
  * **Blickfeld**: *0.01 - 100.0*\
    Legt den FOV-Winkel der Kamera fest.
  * **Entfernung**: *0.0 - 4.0*\
    Legen Sie den Abstand der Kamera vom Objektzentrum fest.
  * **Vignettenintensität**: *0.0 - 1.0*\
    Legen Sie die Intensität des Vignetteneffekts fest.
  * **Vignettenradius**: *0.0 - 1.0*\
    Legen Sie den Radius des Vignetteneffekts fest.
  * **Bildschirmposition**:\
    Verschiebt die Kamera um das Objekt, kann aber auch durch ein Gizmo in der 2D-Ansicht geändert werden.
* **Tiefe von Feld**
  * **Blendenradius** : *0.0 - 0.1* Legt den Radius der Blende fest. Höhere Werte bedeuten, dass Bereiche außerhalb des Fokus unschärfer werden (Bokeh).
  * **Blendenblätter**: *3 - 9*\
    Legt die Form der Bokeh-Weichzeichnung fest.
  * **Blendenring**: *0.0 - 1.0*\
    Fügt einen inneren Verlauf zur Bokeh-Form hinzu.
  * **Blendendifferenz**: *0.0 - 2.0*\
    Fügt dem Bokeh chromatische Aberration hinzu.
  * **Swirly Bokeh**: *0.0 - 1.0*\
    Fügt unscharfen Bokeh-Weichzeichnungsbereichen einen Wirbel oder eine sich drehende Wirkung hinzu.
  * **Fokusmodus**: *Auto, Punkt*\
    Festlegen, ob der Fokus vorbestimmt oder vom Benutzer festgelegt ist. Mit dem Punktfokus können Sie einen Punkt in der 2D-Ansicht verschieben, um den Fokusabstand zu bestimmen.
  * **Fokuspunkt**:\
    Wenn der Fokus auf &quot;Punkt&quot; gesetzt ist, können Sie diesen Punkt verschieben. hat ein Gizmo mit 2D-Ansicht.
  * **Fokusversatz**: *-0.5 - 0.5*\
    Wenn der Fokus auf &quot;Auto&quot; eingestellt ist, können Sie ihn vor und zurück verschieben.
  * **Benutzerdefinierte Blendenzuordnung verwenden**: *False/True*\
    Überschreibt die oben genannten Blendeneinstellungen und verwenden Sie die Blendenmap-Eingabe, um die Bokeh-Form zu bestimmen. Benötigt eine Eingabe.
* **Post-Effekte**
  * **Post-Effekte aktivieren**: *False/True*\
    Schaltet *alle* Nacheffekte im endgültigen Rendering um.
  * **Blütenintensität** : *0.0 - 2.0* Legt die Stärke des Blüteneffekts fest.
  * **Bloom-Schwellenwert** : *0.0 - 2.0* Legt einen niedrigen Schwellenwert für die Anzeige der Blüte fest.
  * **Bloom Chroma Shift** : *0.0 - 1.0*
  * **Halo-Intensität der Linse** : *0.0 - 1.0* Legt die Intensität für den Linsenhalo-Effekt fest.
  * **Intensität der Blendenflecken** : *0.0 - 1.0* Legt die Intensität für den Blendenfleck fest. Stelle sicher, dass das Licht deines Umgebungshintergrunds sichtbar ist, um diesen Effekt richtig zu sehen.
  * **Linsenintensität des Dirts** : *0.0 - 1.0* Legt den Effekt der Linseneffekt-Dirt-Map auf die Blendenflecken fest.
* **Rendereinstellungen**
  * **Diffuse Qualität**: *16 Samples, 32 Samples, 64 Samples, 128 Samples*\
    Wechseln Sie zwischen den Qualitätsstufen für die diffuse Karte.
  * **Diffuse Emissive Multiplier**: *0.0 - 1.0*\
    Steuert, wie stark die emittierenden Teile zur Bestrahlung beitragen.
  * **Intensität des diffusen Schattens**: *0.0 - 1.0*\
    Steuert die Intensität der diffusen Schatten.
  * **Specular-Dithering**: *0.0 - 1.0*\
    Stellen Sie die Dithering-Rate für den Specular ein.
  * **Specular-Schattenmultiplikator**: *0.0 - 1.0*\
    Steuert die Schattenintensität in den Specular-Reflexionen.
  * **Deckkraftmodus** *Dithering-Alpha-Test, Simple Alpha Blend*\
    Steuert die Methode zum Anwenden von Transparenz. Der Modus *Einfache Alpha-Überblendung* wird am besten auf einheitlichen Hintergründen angezeigt.
  * **Umgebungsintensität der Verdeckung**: *0.0 - 1.0*\
    Legt die Intensität der Umgebungsschatten für die Verdeckung fest.
* **Materialanpassungen**
  * **Normale neu berechnen**: *False/True*\
    Die Normale werden anhand der Intensität des Versatzes aus der Height-Map neu berechnet.
  * **Normales Format**: *DirectX, OpenGL*\
    Zwischen verschiedenen Normalen-Map-Format wechseln (invertiert den grünen Kanal)
  * **Dielektrischer F0-Eingang**: *Konstanter Wert, Specular level-Eingabe*\
    Festlegen, was F0-Werte antreibt. Specular level-Eingabe bedeutet, dass sie von einer Eingabemap gesteuert wird.
  * **Dielektrisches F0**: *0.0 - 0.08*\
    Wenn &quot;Konstanter Wert&quot; für den dielektrischen F0-Eingang ausgewählt ist, können Sie mit diesem Schieberegler den globalen Wert einstellen.
* **Überzug löschen**
  * **Clear Coat aktivieren**: *False/True*\
    Ermöglicht eine zusätzliche, einfache Klarlackschicht auf dem Eingangsmaterial.
  * **Beschichtungsgewicht löschen**: *0.0 - 1.0*\
    Legt die Intensität oder Stärke der Klarlackschicht fest.
  * **Specular level löschen**: *0.0 - 1.0*\
    Legt die Raueit der Klarlackschicht fest.
  * **Normal von Basisebene erben**: *Falsch/Wahr* Festlegen, wenn ClearCoat Normalwerte aus dem Basismaterial ignoriert oder verwendet.
* **Ausstrahlend**
  * **Emissionsbeleuchtung aktivieren** *Wahr/Falsch* Schaltet den diffusen Beitrag der Emissionsbeleuchtung um.
  * **Emissionsintensität**: *0.0 - 10.0*\
    Legt den globalen Multiplikator für die Emissionskarte fest.
* **Untergrundstreuung**
  * **Untergrundstreuung aktivieren** *Wahr/Falsch*\
    Schaltet die Volumenstreuung im endgültigen Rendering um.\
    *Hinweis:* Für die Untergrundstreuung muss der Eingabewert **Transluzenz** *höher als 0,0* sein.
  * **Streuungsabstand** *0.0 - 1.0*\
    Passt den maximalen Abstand des Streueffekts an.\
    *Hinweis:* Dieser Wert wird mit dem Eingabewert *für die **Streuungsentfernungsskala**pro Farbkanal* multipliziert.
  * **Red Shift** *0.0 - 1.0*\
    Passt die Intensität des Effekts &quot;Rote Verschiebung&quot; bei der Streuung an.
  * **Rayleigh** *0.0 - 1.0*\
    Passt die Intensität des Rayleigh-Effekts bei der Streuung an.

## Beispielbilder

Alle Bilder wurden direkt in Designer im 2D-Ansichtsfenster mithilfe von Materialien aus der Bibliothek [Substance 3D Assets](https://substance3d.adobe.com/assets) generiert.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/pbr-render-v2.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/sphere-thermal-insulation-panel.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/sphere-ominous-obsidian.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/sphere-forest-gravel-1.jpg" width="300px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_image" src="../../../../../../assets/sphere-chesterfield-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_image" src="../../../../../../assets/sphere-carbon-fiber.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c2_image" src="../../../../../../assets/plane-inclined-lumber-tiles.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c3_image" src="../../../../../../assets/cylinder-medieval-leaded-glass-window.jpg" width="300px"/></div> |
|  |  |  |  |

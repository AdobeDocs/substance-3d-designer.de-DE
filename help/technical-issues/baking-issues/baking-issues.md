---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: Hier finden Sie Schritte zur Fehlerbehebung für technische Probleme im Zusammenhang mit dem Baking von Texturen in Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Probleme beim Baking
user-guide-description: ''
user-guide-title: ''
source-git-commit: f72773d86b681ce0e815c5595067b1593cdd1f0a
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# Probleme beim Baking

Auf dieser Seite werden technische Probleme im Zusammenhang mit [dem Baking von Texturen](../../bakers/bakers.md) in Substance 3D Designer aufgelistet. Für jedes Problem werden Fehlerbehebungsschritte angeboten.

## Auf dieser Seite

&quot;Mit Namen abgleichen&quot; funktioniert nicht

## &quot;Mit Namen abgleichen&quot; funktioniert nicht

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>![(Fehler)](baking-issues.resources/error.svg) Problem</b>

Wenn die Option &quot;Abgleich&quot; auf &quot;Nach Mesh-Name&quot; festgelegt ist, scheint die Zuordnung nicht oder nicht konsistent auf alle Szenenobjekt angewendet zu werden.

<b>![(tick)](baking-issues.resources/check.svg) Empfohlene Schritte</b>

In den Designer-Versionen 14.1 und niedriger wurden Objekte mit niedrigem und hohem Poly mit dem Namen ihrer *übergeordneten* Objekte abgeglichen - in den meisten Fällen transformieren ihr übergeordnetes Objekt.

Seit Designer 15.0 wird der Name der *Geometrie*-Objekte direkt verwendet.

</td>
<td style="border: 0;" valign="top">

![Geometry-Objekt und übergeordnetes Objekt in der Szene &#x200B;](baking-issues.resources/sceneTree_objectsName.png "Geometry-Objekt und übergeordnetes Objekt in der Szene "){zoomable="yes"}

</td>
</tr>
</table>

Es gibt zwei Pfade, die Sie verwenden können, um die erwartete Übereinstimmung zu erzielen:

* Passen Sie den Namen der Geometrieobjekte an, um passende Namen anzuwenden.
* Stellen Sie das Verhalten oder frühere Designer-Versionen wieder her, indem Sie die Option [&#39;Name Filtermethode&#39;](../../interface/preferences-window/project-settings/project-settings.md) in den Projekteinstellungen anpassen:
  1. Gehen Sie zu Bearbeiten > Voreinstellungen > Projekte .
  1. Die letzte Projektdatei in der Liste auswählen
  1. Wählen Sie unter der Liste der Projektdateien die Registerkarte &quot;Baker&quot; aus.
  1. Legen Sie die Filtermethode &quot;Name&quot; auf &quot;Übergeordneter Name (veraltet)&quot; fest.

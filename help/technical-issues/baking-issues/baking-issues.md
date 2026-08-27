---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: Hier finden Sie Schritte zur Fehlerbehebung für technische Probleme im Zusammenhang mit dem Backen von Texturen in Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Backprobleme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Backprobleme

Auf dieser Seite werden technische Probleme im Zusammenhang mit [Backtexturen](../../bakers/bakers.md) in Substance 3D Designer aufgeführt. Für jedes dieser Probleme werden Fehlerbehebungsschritte angeboten.

## Auf dieser Seite

&quot;Mit Namen abgleichen&quot; funktioniert nicht

## &quot;Mit Namen abgleichen&quot; funktioniert nicht

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>![(Fehler)](../../assets/error.svg) Problem </b>

Wenn die Option &quot;Abgleich&quot; auf &quot;Nach Gitternamen&quot; festgelegt ist, wird die Zuordnung anscheinend nicht oder nicht konsistent auf alle Szenenobjekte angewendet.

<b>![(tick)](../../assets/check.svg) Empfohlene Schritte</b>

In Designer 14.1 und niedriger wurden Objekte mit niedrigem Poly- und hohem Poly-Wert mit dem Namen ihrer *übergeordneten* Objekte abgeglichen - in den meisten Fällen ihrer übergeordneten Transformation.

Seit Designer 15.0 wird der Name der *Geometrie*-Objekte direkt verwendet.

</td>
<td style="border: 0;" valign="top">

![Geometry-Objekt und übergeordnetes Objekt im Szenenbaum](../../assets/sceneTree_objectsName.png "Geometry-Objekt und übergeordnetes Objekt im Szenenbaum"){zoomable="yes"}

</td>
</tr>
</table>

Es gibt zwei Pfade, die Sie verwenden können, um die erwartete Übereinstimmung zu erzielen:

* Passen Sie den Namen der Geometrieobjekte an, um passende Namen anzuwenden.
* Stellen Sie das Verhalten oder frühere Designer-Versionen wieder her, indem Sie die Option &quot;[&quot; &quot;Namensfiltermodus&quot; &quot;](../../interface/preferences-window/project-settings/project-settings.md)&quot; in den Projekteinstellungen anpassen:
  1. Gehen Sie zu Bearbeiten > Voreinstellungen > Projekte .
  1. Die letzte Projektdatei in der Liste auswählen
  1. Wählen Sie unter der Liste der Projektdateien die Registerkarte &quot;Bäcker&quot; aus.
  1. Legen Sie den &quot;Namensfiltermodus&quot; auf &quot;Übergeordneter Name (veraltet)&quot; fest.

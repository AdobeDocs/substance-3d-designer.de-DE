---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/bakers.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie mit Substance 3D Designer Baker Mesh-basierte Informationen in Textur-Dateien berechnen können.
helpx_creative_field: ""
helpx_description: Designer > Bakers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Baker
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---


# Baker

Baking bezieht sich auf die Aktion **Übertragen von Mesh-basierten Informationen in Texturen**. Diese Informationen werden dann von Shadern und/oder Substance-Filtern gelesen, um komplexere Effekte oder Texturen zu erzeugen.

>[!NOTE]
>
> Weitere Informationen zum Baking finden Sie in der [Dokumentation zum Baking](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/home).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Auf das Fenster &quot;Baking&quot; kann über die Meshdatei im Fenster &quot;[Explorer](../interface/the-explorer-window/the-explorer-window.md)&quot; zugegriffen werden. Klicken Sie mit der rechten Maustaste auf den Namen des Meshs, und wählen Sie &quot;**Modellinformationen Baking geführt**&quot; aus, um das Baking führend Fenster zu öffnen.

</td>
<td width="33.33%" style="border: 0;" valign="top">

Option ![&#x200B; &#39;Baking-Modus-Informationen&#39; im Kontextmenü der 3D-Szene-Ressource](bakers.resources/bakers-01.png " &#39;Baking-Modus-Informationen&#39; im Kontextmenü der 3D-Szene-Ressource")

</td>
</tr>
</table>

![Fenster wird Baking geführt](bakers.resources/bakers-02.png "Fenster wird Baking geführt")

## Überblick

Das Baking-Fenster von ist in mehrere Bedienfelder unterteilt, die im Folgenden beschrieben werden.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Zu Baking führend Elemente

Dieses Bedienfeld steuert, welcher Teil des Low-Poly-Meshs für den Baking führ verwendet wird.

Es listet die Geometrie auf, die in der Meshdatei mit niedriger Poly zu finden ist. Standardmäßig basiert die Liste auf den einzelnen Materialien, die in der Datei gefunden wurden, kann jedoch bei Bedarf auf Unter-Mesh umgestellt werden. Sie können Elemente deaktivieren, die beim Baking ignoriert werden sollen.

</td>
<td style="border: 0;" valign="top">

![](bakers.resources/bakers-03.png)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Ausgabe

Dieses Bedienfeld steuert, wo sich die Baking geführt Textur befindet.

</td>
<td style="border: 0;" valign="top">

![](bakers.resources/bakers-04.png)

</td>
</tr>
</table>

| *Parameter* | *Beschreibung* |
| --- | --- |
| **Methode** | Steuert, wie die Baking geführt Texturen mit dem Substance-Paket gespeichert werden.Mögliche Werte:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Eingebettet</strong> : Die Baking geführt Texturen werden in einem Unterordner neben dem Substance-Paket mit einem bestimmten Namen gespeichert.</li><li data-preserve-html="true"><strong>Verknüpft</strong> (Standard) : Die gebackene Textur wird in dem definierten Ordner gespeichert und dann in das Substance-Paket aufgenommen.</li></ul> |
| **Ordner** | Speicherort der Texturen, die als Stapel vorliegen. Klicken Sie auf drei Punkte, um ein Dateidialogfeld zu öffnen, und wählen Sie den Exportordner aus. Rechts wird ein Häkchen angezeigt, das angibt, ob der Ordner tatsächlich existiert oder nicht. |
| **Name** | Namenskonvention der gebackenen Texturen. Klicken Sie auf die Schaltfläche mit den drei Punkten, um eine Dropdown-Liste zu öffnen und andere Platzhalter einzufügen (Backname, benutzerdefiniert, Material, Gitter). |
| **Beispiel** | Simulieren Sie einen Dateinamen, um die Namenskonvention zu testen. |
| **Ressource in einen netzspezifischen Ordner platzieren** | Wenn diese Option aktiviert ist, werden die Texturen in einem Ordner gespeichert, der als Gitterdatei bezeichnet wird. |

### HD-Meshes

Dieses Bedienfeld steuert die Liste der Gitter mit hohem Poly-Wert und die zugehörigen Einstellungen. Weitere Informationen finden Sie in den [allgemeinen Parametern](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/common-parameters).

![High-Definition-Meshes](bakers.resources/bakers-05.png "High-Definition-Meshes")

### Standardwerte

Weitere Informationen finden Sie in den [allgemeinen Parametern](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/common-parameters).

![Standardwerte](bakers.resources/bakers-06.png "Standardwerte")

### Renderliste und Einstellungen für Bäcker

In der Renderliste &quot;**Bäcker&quot; &quot;**&quot; können Sie auswählen, welche gebackene Textur Sie generieren möchten. Standardmäßig ist die Liste leer.

* **Neuen Bäcker hinzufügen:** Klicken Sie auf die Schaltfläche &quot;Bäcker hinzufügen&quot;.
* **Einen Bäcker entfernen:** Wählen Sie den Bäcker in der Liste aus und klicken Sie dann auf die Schaltfläche &quot;Bäcker löschen&quot;.
* **Einen Bäcker nach oben verschieben:** Wählen Sie den Bäcker in der Liste aus und klicken Sie dann auf die Schaltfläche &quot;Nach oben ziehen&quot;.
* **Einen Bäcker nach unten bewegen:** Wählen Sie den Bäcker in der Liste aus und klicken Sie dann auf die Schaltfläche &quot;Nach unten schieben&quot;.

Jeder Bäcker in der erbt standardmäßig die Standardwerte (siehe oben). Die Größe (Auflösung) kann beispielsweise überschrieben werden, indem man auf die Zelle in der Zeile des Bakers klickt. Dies gilt auch für die anderen Einstellungen in der Zeile.

Wenn Sie auf einen Baker in der Liste klicken, wird die Parameteransicht des Bakers mit ihren spezifischen Parametern aktualisiert.

Weitere Informationen zu den spezifischen Parametern finden Sie unter: [Baker-Einstellungen](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings).

![Liste zum Rendern von Bakern](bakers.resources/bakers-07.png "Liste zum Rendern von Bakern")

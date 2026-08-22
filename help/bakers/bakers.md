---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/bakers.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie mit Substance 3D Designer-Bäcker netzbasierte Informationen in Texturdateien umwandeln können.
helpx_creative_field: ""
helpx_description: Designer > Bakers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Baker
user-guide-description: ''
user-guide-title: ''
source-git-commit: 68389d2a09ef1db6c14073029efdbfd9d48c83c8
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---


# Baker

Backen bezieht sich auf die Aktion **Übertragen von netzwerkbasierten Informationen in Texturen**. Diese Informationen werden dann von Shadern und/oder Substance-Filtern gelesen, um komplexere Effekte oder Strukturen zu erzeugen.

>[!NOTE]
>
> Weitere Informationen zum Backen finden Sie in der [Backdokumentation](https://experienceleague.adobe.com/de/docs/substance-3d/bakers/home).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Auf das Backing-Fenster kann über die Gitterdatei im Fenster [Explorer](../interface/the-explorer-window/the-explorer-window.md) zugegriffen werden. Klicken Sie mit der rechten Maustaste auf den Netznamen und wählen Sie &quot;**Informationen zum Backmodell**&quot; aus, um das Backing-Fenster zu öffnen.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![&#x200B; Option &quot;Backmodusinformationen&quot; im Kontextmenü der 3D-Szenenressource &#x200B;](../assets/sd-mesh-right-click.png " Option &quot;Backmodusinformationen&quot; im Kontextmenü der 3D-Szenenressource ")

</td>
</tr>
</table>

![Sicherungsfenster](../assets/sd-window-overview.png "Sicherungsfenster")

## Überblick

Das Backfenster von ist in mehrere Paneele unterteilt, die im Folgenden beschrieben werden.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Einzubackende Elemente

Dieses Bedienfeld steuert, welcher Teil des Gitters mit niedrigem Poly-Anteil zum Backen verwendet wird.

Es listet die Geometrie auf, die in der Gitterdatei mit niedriger Poly gefunden wird. Standardmäßig basiert die Liste auf den einzelnen Materialien, die in der Datei gefunden wurden, kann jedoch bei Bedarf auf Subnetze umgestellt werden. Sie können Elemente deaktivieren, die während des Backvorgangs ignoriert werden sollen.

</td>
<td style="border: 0;" valign="top">

![](../assets/sd-mesh-selection.png)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Ausgabe

Dieses Bedienfeld steuert, wo die Textur platziert wird.

</td>
<td style="border: 0;" valign="top">

![](../assets/sd-output.png)

</td>
</tr>
</table>

| *Parameter* | *Beschreibung* |
| --- | --- |
| **Methode** | Steuert, wie die Texturen mit dem Substance-Paket gespeichert werden.Mögliche Werte:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Eingebettet</strong> : Die gebackenen Texturen werden in einem Unterordner neben dem Substance-Paket mit einem bestimmten Namen gespeichert.</li><li data-preserve-html="true"><strong>Verknüpft</strong> (Standard) : Die gebackene Textur wird in dem definierten Ordner gespeichert und dann in das Substance-Paket aufgenommen.</li></ul> |
| **Ordner** | Speicherort der Texturen, die als Stapel vorliegen. Klicken Sie auf drei Punkte, um ein Dateidialogfeld zu öffnen, und wählen Sie den Exportordner aus. Rechts wird ein Häkchen angezeigt, das angibt, ob der Ordner tatsächlich existiert oder nicht. |
| **Name** | Namenskonvention der gebackenen Texturen. Klicken Sie auf die Schaltfläche mit den drei Punkten, um eine Dropdown-Liste zu öffnen und andere Platzhalter einzufügen (Backname, benutzerdefiniert, Material, Gitter). |
| **Beispiel** | Simulieren Sie einen Dateinamen, um die Namenskonvention zu testen. |
| **Ressource in einen netzspezifischen Ordner platzieren** | Wenn diese Option aktiviert ist, werden die Texturen in einem Ordner gespeichert, der als Gitterdatei bezeichnet wird. |

### HD-Meshes

Dieses Bedienfeld steuert die Liste der Gitter mit hohem Poly-Wert und die zugehörigen Einstellungen. Weitere Informationen finden Sie in den [allgemeinen Parametern](https://experienceleague.adobe.com/de/docs/substance-3d/bakers/bakers-settings/common-parameters).

![High-Definition-Meshes](../assets/sd-high.png "High-Definition-Meshes")

### Standardwerte

Weitere Informationen finden Sie in den [allgemeinen Parametern](https://experienceleague.adobe.com/de/docs/substance-3d/bakers/bakers-settings/common-parameters).

![Standardwerte](../assets/sd-default-values.png "Standardwerte")

### Renderliste und Einstellungen für Bäcker

In der Renderliste &quot;**Bäcker&quot; &quot;**&quot; können Sie auswählen, welche gebackene Textur Sie generieren möchten. Standardmäßig ist die Liste leer.

* **Neuen Bäcker hinzufügen:** Klicken Sie auf die Schaltfläche &quot;Bäcker hinzufügen&quot;.
* **Einen Bäcker entfernen:** Wählen Sie den Bäcker in der Liste aus und klicken Sie dann auf die Schaltfläche &quot;Bäcker löschen&quot;.
* **Einen Bäcker nach oben verschieben:** Wählen Sie den Bäcker in der Liste aus und klicken Sie dann auf die Schaltfläche &quot;Nach oben ziehen&quot;.
* **Einen Bäcker nach unten bewegen:** Wählen Sie den Bäcker in der Liste aus und klicken Sie dann auf die Schaltfläche &quot;Nach unten schieben&quot;.

Jeder Bäcker in der erbt standardmäßig die Standardwerte (siehe oben). Die Größe (Auflösung) kann z.B. überschrieben werden, indem man auf die Zelle in der Zeile des Bäckers klickt. Dies gilt auch für die anderen Einstellungen in der Zeile.

Wenn Sie auf einen Bäcker in der Liste klicken, wird die Ansicht &quot;Bäckerparameter&quot; mit den spezifischen Parametern aktualisiert.

Weitere Informationen zu den spezifischen Parametern finden Sie unter: [Baker-Einstellungen](https://experienceleague.adobe.com/de/docs/substance-3d/bakers/bakers-settings/bakers-settings).

![Baker-Renderliste](../assets/sd-baker-list.png "Baker-Renderliste")

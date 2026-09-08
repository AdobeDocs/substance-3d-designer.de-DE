---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/bakers.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---


# Baker

Baking bezieht sich auf die Aktion **Übertragen von Mesh-basierten Informationen in Texturen**. Diese Informationen werden dann von Shadern und/oder Substance-Filtern gelesen, um komplexere Effekte oder Texturen zu erzeugen.

>[!NOTE]
>
> Weitere Informationen zum Baking finden Sie in der [Dokumentation zum Baking](https://experienceleague.adobe.com/de/docs/substance-3d/bakers/home).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Auf das Fenster &quot;Baking&quot; kann über die Meshdatei im Fenster &quot;[Explorer](../interface/the-explorer-window/the-explorer-window.md)&quot; zugegriffen werden. Klicken Sie mit der rechten Maustaste auf den Namen des Meshs, und wählen Sie &quot;**Baking Model Information**&quot; aus, um das Fenster &quot;Baking&quot; zu öffnen.

</td>
<td width="33.33%" style="border: 0;" valign="top">

Option ![&#x200B; &#39;Baking-Modus-Informationen&#39; im Kontextmenü der 3D-Szene-Ressource](../assets/sd-mesh-right-click.png " &#39;Baking-Modus-Informationen&#39; im Kontextmenü der 3D-Szene-Ressource")

</td>
</tr>
</table>

![Fenster wird Baking geführt](../assets/sd-window-overview.png "Fenster wird Baking geführt")

## Überblick

Das Baking-Fenster von ist in mehrere Bedienfelder unterteilt, die im Folgenden beschrieben werden.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Zu Baking führend Elemente

Dieses Bedienfeld steuert, welcher Teil des Meshs mit wenig Poly für das Baking verwendet wird.

Es listet die Geometrie auf, die in der Meshdatei mit niedriger Poly zu finden ist. Standardmäßig basiert die Liste auf den einzelnen Materialien, die in der Datei gefunden wurden, kann jedoch bei Bedarf auf Unter-Mesh umgestellt werden. Sie können Elemente deaktivieren, die beim Baking ignoriert werden sollen.

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

Dieses Bedienfeld steuert, wo sich die Baking geführt Textur befindet.

</td>
<td style="border: 0;" valign="top">

![](../assets/sd-output.png)

</td>
</tr>
</table>

| *Parameter* | *Beschreibung* |
| --- | --- |
| **Methode** | Steuert, wie die Baking geführt Texturen mit dem Substance-Paket gespeichert werden.Mögliche Werte:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Eingebettet</strong> : Die Baking geführt Texturen werden in einem Unterordner neben dem Substance-Paket mit einem bestimmten Namen gespeichert.</li><li data-preserve-html="true"><strong>Verknüpft</strong> (Standard) : Die Baking geführt Texturen werden in dem definierten Ordner abgelegt und dann in das Substance-Paket aufgenommen.</li></ul> |
| **Ordner** | Speicherort der Baking geführt Texturen beim Speichern. Klicken Sie auf drei Punkte, um ein Dateidialogfeld zu öffnen, und wählen Sie den Exportordner aus. Rechts wird ein Häkchen angezeigt, das angibt, ob der Ordner tatsächlich existiert oder nicht. |
| **Name** | Namenskonvention der Baking geführt Texturen. Klicken Sie auf die Schaltfläche mit den drei Punkten, um eine Dropdown-Liste zu öffnen und andere Platzhalter einzufügen (Backname, benutzerdefiniert, Material, Mesh). |
| **Beispiel** | Simulieren Sie einen Dateinamen, um die Namenskonvention zu testen. |
| **Ressource in einen Ordner platzieren, der für einen bestimmten Mesh bestimmt ist** | Wenn diese Option aktiviert ist, werden die Baking geführt Texturen in einem Ordner gespeichert, der als Meshdatei bezeichnet wird. |

### High-Definition-Meshs

Dieses Bedienfeld steuert die Liste der Mesh mit hohen Poly-Raten und die zugehörigen Einstellungen. Weitere Informationen finden Sie in den [allgemeinen Parametern](https://experienceleague.adobe.com/de/docs/substance-3d/bakers/bakers-settings/common-parameters).

![High-Definition-Mesh](../assets/sd-high.png "High-Definition-Mesh")

### Standardwerte

Weitere Informationen finden Sie in den [allgemeinen Parametern](https://experienceleague.adobe.com/de/docs/substance-3d/bakers/bakers-settings/common-parameters).

![Standardwerte](../assets/sd-default-values.png "Standardwerte")

### Baker rendern Liste und Einstellungen

In der Renderliste &quot;**Baker&quot; &quot;**&quot; können Sie auswählen, welche Baking geführt Textur generiert werden soll. Standardmäßig ist die Liste leer.

* **Neuen Baker hinzufügen:** Klicken Sie auf die Schaltfläche &quot;Baker hinzufügen&quot;.
* **Entfernen eines Bakers:** Wählen Sie den Baker in der Liste aus, und klicken Sie dann auf die Schaltfläche &quot;Baker löschen&quot;.
* **Verschieben eines Bakers nach oben:** Wählen Sie den Baker in der Liste aus und klicken Sie dann auf die Schaltfläche &quot;Nach oben ziehen&quot;.
* **Einen Baker nach unten bewegen:** Wählen Sie den Baker in der Liste aus, und klicken Sie dann auf die Schaltfläche &quot;Nach unten schieben&quot;.

Jeder Baker in der erbt standardmäßig die Standardwerte (siehe oben). Die Größe (Auflösung) kann beispielsweise überschrieben werden, indem man auf die Zelle in der Zeile des Bakers klickt. Dies gilt auch für die anderen Einstellungen in der Zeile.

Wenn Sie auf einen Baker in der Liste klicken, wird die Parameteransicht des Bakers mit ihren spezifischen Parametern aktualisiert.

Weitere Informationen zu den spezifischen Parametern finden Sie unter: [Baker-Einstellungen](https://experienceleague.adobe.com/de/docs/substance-3d/bakers/bakers-settings/bakers-settings).

![Liste zum Rendern von Bakern](../assets/sd-baker-list.png "Liste zum Rendern von Bakern")

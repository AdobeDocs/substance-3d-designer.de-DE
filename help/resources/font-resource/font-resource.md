---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/font-resource.html"
breadcrumb-title: ''
description: Importiere und verwende Schriftenressourcen in Substance 3D Designer, um Text und Typografie zu deinen Materialien hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Resources > Font resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Schriftarten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Schriftarten

Schriftartenressourcen sollen zusammen mit dem [atomaren Textknoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) verwendet werden. Sie ermöglichen die Verwendung von Schriftarten, die nicht auf Ihrem System installiert sind, indem Sie auf eine Schriftartdatei an einer beliebigen Stelle auf der Festplatte verweisen.

>[!NOTE]
>
> **Schriftarten in SBSAR**
> 
> Schriften werden immer in eine SBSAR eingebettet, unabhängig davon, ob sie von einer verknüpften Ressource stammen oder eine vom System installierte Schrift verwenden. Der Vorteil dieser Methode ist, dass es nicht notwendig ist, zu installieren, und beim Exportieren einer SBS-Datei mit Abhängigkeiten können Sie sicher sein, dass die Schriftdateien mitkommen.

## Verwenden von Ressourcen für benutzerdefinierte Schriften

* Klicken Sie mit der rechten Maustaste auf ein Paket und wählen Sie <b>Link > Font</b>
* Wählen Sie eine OTF- oder TTF-Datei aus.
* Platzieren Sie einen [Textknoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) in Ihrem [Diagramm](../../compositing-graphs/substance-compositing-graphs.md).
* Unter der Eigenschaft <b>Schriftart </b> befinden sich alle Schriftartenressourcen ganz oben in der Liste.

Beachten Sie, dass die Schriftartenliste bei geöffneten Eigenschaften nicht automatisch aktualisiert wird. Sie müssen zu einem anderen Eigenschaftenfenster und zurück zu einem Knoten &quot;Text&quot; wechseln, um neu verknüpfte Schriftarten anzuzeigen.

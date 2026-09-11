---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/resources/3d-scene-resource.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie 3D-Szenenressourcen in Substance 3D Designer für die Materialvorschau und das Testen importieren und verwenden.
helpx_creative_field: ""
helpx_description: Designer > Resources > 3D scene resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Szenen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 1%

---


# 3D-Szenen

Auf dieser Seite wird der Ressourcentyp **3D scene** in Substance 3D Designer beschrieben, einschließlich der unterstützten Dateiformate und der Verwendung.

## Überblick

3D-Szenenressourcen können in verschiedenen Workflows verwendet werden:

* [Maschen-Backmaschen](../../bakers/bakers.md)
* Vorschau von *Texturen* aus [Substance-Graphen](../../compositing-graphs/substance-compositing-graphs.md) in der [3D-Ansicht](../../interface/3d-view/3d-view.md)

Die folgenden 3D-Szenendateiformate werden unterstützt:

* [USD](https://graphics.pixar.com/usd/release/index.html) (\*.usd)
* [USDA](https://graphics.pixar.com/usd/release/index.html) (\*.usda)
* [USDZ](https://graphics.pixar.com/usd/release/index.html) (\*.usdz)
* [Autodesk FBX](https://www.autodesk.com/products/fbx/overview) (\*.fbx)
* [Wavefront OBJ](https://www.fileformat.info/format/wavefrontobj/egff.htm) (\*.obj)
* [Autodesk 3D Studio Mesh](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2022/ENU/3DSMax-Data-Exchange/files/GUID-A16ECF7F-70E5-4F9F-8EAD-35F5CFB485A2-htm.html) (\*.3ds)
* [Collada](https://www.khronos.org/collada/) (\*.date)
* [Autodesk AutoCAD-Zeichnung](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/AutoCAD-Core/files/GUID-D4242737-58BB-47A5-9B0E-1E3DE7E7D647-htm.html) (\*.dxf)

## Gitterspeicher

3D-Szenen können *nur* verknüpft werden, d. h. sie bleiben an ihrem Speicherort auf dem Datenträger und werden nur in der Anwendung referenziert.

Wenn ein Paket mit einer 3D-Szenenressource als [Substance 3D](https://www.adobe.com/de/products/substance3d/3d-augmented-reality.html)-Asset (SBSAR) veröffentlicht wird, ist das Gitter *nicht eingebettet*, aber verworfen.

## Backen von Gitterkarten

Das Verknüpfen einer 3D-Szene mit Ihrem Paket ist die einzige Möglichkeit, [Gitterzuordnungen](../../bakers/bakers.md) aus dieser Szenengeometrie zu backen. Sie können die folgenden Schritte ausführen, um zu beginnen:

* Klicken Sie auf *RMB* in einem Paket und wählen Sie im Kontextmenü die Option <b>Link > 3D-Mesh</b> aus.
* Wählen Sie eine unterstützte 3D-Szenendatei
* Wenn die Dialogaufforderung <b>Als Udim-Gitter verknüpfen</b> angezeigt wird, klicken Sie auf *Nein*, es sei denn, Sie möchten UV-Kacheln backen.
* Wenn die Ressource in [Explorer](../../interface/the-explorer-window/the-explorer-window.md) geladen ist, klicken Sie auf *RMB*, und wählen Sie im Kontextmenü die Option <b>Modellinformationen für Backen</b> aus.
* Das Dialogfeld &quot;[Modellinformationen backen](../../bakers/bakers.md)&quot; wird angezeigt, in dem Sie alle Gitterzuordnungs-Backs einrichten und ausführen können.

![Gitterzuordnungen sichern](../../assets/bake-model-information.gif "Gitterzuordnungen sichern"){width="512px"}

## UDIM/UV-Kachelverwendung

Wenn eine Gitterressource verknüpft ist und die Anwendung erkennt, dass sie UVs außerhalb des 0-1-Bereichs enthält, werden Sie gefragt, ob dieses Gitter als UDIM-Gitter (auch als UV-Kacheln bezeichnet) behandelt werden soll. Diese Einstellung kann anschließend geändert werden. Sofern Sie nicht sicher sind, dass Sie UV-Kacheln verwenden, sollte sie als <b>Nein</b> beantwortet werden.

Wenn das Verhalten &quot;UV-Kachel&quot; aktiv ist, verhält sich das Backen anders und backt Texturen für jede erfasste UV-Kachel.

## Ressource/Szene im Vergleich zum Status

Die Anwendung unterteilt die Elemente, die Sie in der 3D-Ansicht sehen, in zwei verschiedene Dateien. Das eigentliche 3D-Modell oder -Mesh ist eine Ressource, die im Explorer angezeigt wird. Das Setup von Lichtern, Kameras und anderen Einstellungen wird als &quot;<b>Status</b>&quot; bezeichnet. Status können in externen .sbsscn-Dateien gespeichert und später erneut geladen werden. .sbsscn-Dateien sind keine Ressourcen, sondern zusätzliche Konfigurationsdateien, die nur über [das Szenenmenü in der 3D-Ansicht geladen werden können.](../../interface/3d-view/3d-view.md)

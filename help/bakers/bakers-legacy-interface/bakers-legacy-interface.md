---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über die ältere Benutzeroberfläche für Substance 3D Designer-Bäcker für Benutzer, die mit älteren Versionen vertraut sind.
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bakers Legacy-Schnittstelle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 3%

---


# Bakers Legacy-Schnittstelle

Hier ist die Beschreibung der Bäcker-Schnittstelle, die in [Adobe Substance 3D Designer](https://www.adobe.com/de/products/substance3d-designer.html)-Versionen vor 6.0.4 verfügbar ist.

## Überblick

![](../../assets/image2017-3-13-9-33-40.png)

Das Backblech ist in 4 Teile unterteilt:

### 1: Szene

![](../../assets/image2017-3-13-9-35-53.png)

Legen Sie fest, welcher Teil des Gitters am Backvorgang beteiligt ist.

Neu in Version 6, können Sie auch nach Material auswählen:

![](../../assets/image2017-3-13-9-45-26.png)

### 2: Bäcker

![](../../assets/image2017-3-13-9-46-26.png)

Durch Drücken der Schaltfläche ![](../../assets/image2017-3-13-9-47-47.png) können Sie die gewünschten Bäcker zur Verarbeitungsliste hinzufügen.

>[!NOTE]
>
> Backvorgänge werden nach der Listenreihenfolge verarbeitet (von oben nach unten): Dies kann wichtig sein, wenn Sie das Ergebnis eines Backvorgangs (wie die normale Karte) in einem anderen Backvorgang wiederverwenden möchten

Durch Klicken auf das Pluszeichen (+) im Baker-Layout können Sie die Baker in einem Stapel hinzufügen (Sie können beliebig viele Baker in einem Stapel ablegen).

.![](../../assets/image2017-3-13-9-52-8.png)

Sie können einen Backvorgang aus der Liste entfernen, indem Sie ![](../../assets/image2017-3-13-9-54-33.png) drücken.

Sie können die Backprozessliste neu anordnen, indem Sie einen Backvorgang auswählen und ![](../../assets/image2017-3-13-9-55-33.png) verwenden.

### 3: Parameter für Bäcker

![](../../assets/image2017-3-13-13-24-0.png)

In diesem Abschnitt werden die spezifischen Optionen für den aktuell ausgewählten Bäcker angezeigt.

### 4: Allgemeine Parameter

![](../../assets/image2017-3-13-13-28-12.png)

Zeigt die Parameter an, die von den Bäckern gemeinsam verwendet werden.

>[!NOTE]
>
> Ändern Sie standardmäßig einen dieser Parameter. wirkt sich auf alle Bäcker aus, außer wenn Sie die Option Parameter überschreiben aktivieren, die für alle Bäcker gelten: in diesem Fall werden die Änderungen lokal für den aktuellen Bäcker übernommen.

* **Im Feld Ressourcenname** können Sie den Namen der generierten Bitmap bei Bedarf ändern.
* **In der Dropdownliste &quot;Dateiformat**&quot; können Sie das Dateiformat vom Standard (Windows- oder OS/2-Bitmapformat &quot;BMP&quot;) ändern.
* Mit dem Kontrollkästchen **Die** **Ressource in einem netzspezifischen Ordner platzieren** können Sie auswählen, ob die generierte Bitmap auf derselben Ebene wie das Modell oder in einem neuen Unterordner mit dem Namen &quot;Resources&quot; gespeichert wird.
* **Mit der Methode** können Sie festlegen, ob die neue Bitmapressource mit dem Substance-Paket verknüpft oder eingebettet werden soll.
* **Im Ordner &quot;**&quot; können Sie festlegen, wo die Zuordnungen gespeichert werden sollen.

Durch Drücken der OK-Taste unten rechts im Fenster wird der Backvorgang gestartet.

Neu in Version 6: Sie können den Backvorgang jetzt mit der Schaltfläche &quot;Abbrechen&quot; abbrechen:

![](../../assets/image2017-3-13-13-50-4.png)

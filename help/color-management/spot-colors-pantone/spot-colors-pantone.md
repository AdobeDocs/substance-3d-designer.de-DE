---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/color-management/spot-colors-pantone.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Pantone-Volltonfarben in Substance 3D Designer verwenden, um die Farben in Druck- und Design-Arbeitsabläufen genau abzugleichen.
helpx_creative_field: ""
helpx_description: Designer > Color Management > Spot Colors (Pantone)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Volltonfarben (Pantone)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# Volltonfarben (Pantone)

Volltonfarben sind ein alternativer Modus zum Auswählen von Farben. Anstelle des standardmäßigen RGB- oder HSV-Farbwählers können Sie in Substance 3D Designer Farben aus Farbtafeln auswählen, die den bestehenden Farbmanagement- und Farbwiedergabesystemen entsprechen. Auf diese Weise können Sie sicherstellen, dass die in Designer verwendeten Digitalfarben denen der hergestellten Produkte sehr ähnlich sind.

Derzeit bietet Spot Colors siebzehn Pantone-Bücher an.

## Farbmanagement

Da Volltonfarben für die präzise Farbwiedergabe und den Farbabgleich vorgesehen sind, müssen Sie [Farbmanagement](../../color-management/color-management.md) für Designer einrichten, bevor Sie mit der Arbeit beginnen. Volltonfarben funktionieren am besten mit <b>Adobe Color Engine (ACE)</b>-Farbmanagement, nicht mit OCIO. Sie funktionieren im Legacy-Modus, aber Sie können nicht sicher sein, ob sie korrekt angezeigt werden, wenn Ihr Monitor nicht für sRGB kalibriert ist.

Kurz gesagt, umfasst die Einrichtung des Farbmanagements für Volltonfarben Folgendes:

* Kalibrieren Sie Ihren Monitor, indem Sie das richtige ICC-Profil generieren oder abrufen.
* Aktivieren Sie in den Voreinstellungen von Designer das Farbmanagement mit Adobe Color Engine (ACE).
* Legen Sie die 2D- und 3D-Ansicht fest, um das richtige Profil von Ihrem Monitor zu verwenden.
* Starten Sie neu, damit die Änderungen wirksam werden.
* Überprüfen der Farbübereinstimmung zwischen Designer und einer anderen Adobe-Anwendung wie Adobe Illustrator oder Photoshop Die Farbe &quot;<b>Pantone Rhodamine Red C</b>&quot; aus dem ersten Pantone-Buch &quot;Solid Coated&quot; ist ein guter Testfall, da sie erheblich variieren kann, wenn das Farbmanagement nicht korrekt ist.

>[!WARNING]
>
> **Miniaturansichtsfarben**
> 
> Knoten-Miniaturansichten sind standardmäßig *nicht farbverwaltet*. Stellen Sie daher sicher, dass die Farbanzeige in der 2D-Ansicht nur mit dem richtigen Profil angezeigt wird. Das Miniatur-Farbmanagement kann in den Voreinstellungen des Farbmanagements Ihres Projekts aktiviert werden, hat aber geringe Leistungskosten.

## Verwenden von Volltonfarben

### Wechseln von RGB zu Volltonfarbe

Auch wenn Sie das Farbmanagement einrichten, verwenden die Farbwähler standardmäßig weiterhin RGB- oder HSV-Farbwähler. Sie müssen sie manuell in Volltonfarben ändern. Diese Einstellung wird pro Parameter gespeichert und wird sogar bei der Belichtung eines Parameters übernommen.

1. Klicken Sie auf die Schaltfläche ![](../../assets/image2021-1-25-9-40-40.png) <b>Farbwählertyp</b> neben dem RGB-Farbfeld.
1. Wählen Sie anstelle von <b>RGB von Farben</b> ein <b>Farbbuch</b> aus der Dropdown-Liste aus.
1. Das Symbol des ![](../../assets/image2021-1-25-9-40-25.png) <b>Farbwählertyps</b> ändert sich, und die Benutzeroberfläche ändert sich in den Modus <b>Volltonfarbe</b>.

![Wechseln in den Volltonfarbmodus](../../assets/spot-switch.gif "Wechseln in den Volltonfarbmodus"){width="512px"}

### Auswählen und Suchen von Volltonfarben

Es gibt mehrere Möglichkeiten, Volltonfarben in einem Farbtafel zu suchen und auszuwählen.

* Sie können die ![](../../assets/image2021-1-25-10-40-28.png) ![](../../assets/image2021-1-25-10-40-53.png) <b>Nach-links- und Nach-rechts-Pfeile</b> auf beiden Seiten der Buchseiten verwenden, um zwischen den Seiten zu wechseln. Sie können auch auf die Seitenanzeige klicken und sie ziehen, um zwischen den Seiten zu scrollen.
* Sie können auf eine beliebige Farbe auf der aktuellen Seite klicken, um sie auszuwählen. Häufig sind mehr Farben verfügbar und erfordern einen Bildlauf nach unten.
* Sie können die Suchleiste verwenden, um Farben nach Name oder Nummer zu suchen. Diese Suche stimmt nur mit den Namen der Farben im Buch überein. Es gibt keine komplexe Logik. Wenn Sie &quot;grau&quot; suchen, erhalten Sie nur Ergebnisse mit dem Wort &quot;grau&quot; im Namen. Sie sehen keine grauen Farben, die nur Zahlen im Namen haben.
* Um eine größere, benutzerfreundlichere Oberfläche für das Farbbuch zu erhalten, klicken Sie auf das Farbvorschaufeld zwischen dem Symbol ![](../../assets/image2021-1-25-10-39-18.png) <b>Pipette</b> und dem ![](../../assets/image2021-1-25-10-40-28.png) <b>Linkspfeil</b>.

![Volltonfarben durchsuchen](../../assets/spot-choose.gif "Volltonfarben durchsuchen"){width="512px"}

### Volltonfarben aufnehmen und konvertieren

Volltonfarben können mit der ![](../../assets/image2021-1-25-10-39-18.png) <b>Pipette</b> ausgewählt werden. Im Volltonfarbmodus bedeutet dies, dass die aufgenommene RGB-Farbe in die Volltonfarbe umgewandelt wird, die der Volltonfarbe des aktuell ausgewählten Buchs am nächsten kommt.

Das <b>Eyedropper</b>-Tool von Designer kann überall auf Ihrem Bildschirm ohne Einschränkungen verwendet werden, d. h. Sie können Designer als Spot Color-Konvertierungstool verwenden.

Wenn Sie &quot;Books&quot; wechseln oder sogar von einem Spot Color-Buch zurück zum RGB wechseln, wird die aktuelle Farbe in die nächstliegende Farbe konvertiert. Das bedeutet, dass Sie Farben zwischen Büchern und wieder zurück auf RGB konvertieren können.

>[!WARNING]
>
> Das Konvertieren von Volltonfarben zwischen Büchern ist ein verlustbehafteter Vorgang. Ein Round-Trip-Konvertieren führt oft nicht zu der gleichen Farbe wie die, mit der du angefangen hast!

![Auswählen und Konvertieren von Volltonfarben](../../assets/spot-pick.gif "Auswählen und Konvertieren von Volltonfarben"){width="512px"}

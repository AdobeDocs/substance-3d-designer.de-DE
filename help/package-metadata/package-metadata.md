---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/package-metadata.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Paket-Metadaten in Substance 3D Designer für organisierte Elementbibliotheken erstellen und verwalten.
helpx_creative_field: ""
helpx_description: Designer > Package Metadata
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metadaten verpacken
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---


# Metadaten verpacken

Package Metadata ist ein Wörterbuch mit Textwerten (Zeichenfolgen), die auf Paketebene definiert sind. Es ist in der SBSAR enthalten, wenn es veröffentlicht wird, und es ist ein Allzweck-Speicher, der von Python-Skripten verwendet werden soll.

## Anzeigen und Bearbeiten von Metadaten über die Oberfläche von Designer

Wenn Sie ein Python-Plug-in entwickeln, sollten Sie Metadaten zum Testen und Debuggen manuell bearbeiten. Gehen Sie dazu folgendermaßen vor:

1. Wenn Sie im Explorer auf ein Paket doppelklicken, wird das Eigenschaftenfenster für dieses Paket geöffnet.

   ![Paketmetadaten](package-metadata.resources/package-metadata-01.png "Paketmetadaten")
1. Hier haben Sie einen eigenen Abschnitt &quot;Metadaten&quot;. Es ist in Ihrem Fall wahrscheinlich leer, wie in der Aufnahme oben.

   Sie können neue Metadaten hinzufügen, indem Sie auf die Schaltfläche &quot;Plus&quot; klicken.

   ![Schaltfläche zum Hinzufügen von Metadaten](package-metadata.resources/package-metadata-02.png "Schaltfläche zum Hinzufügen von Metadaten")
1. Im folgenden Abschnitt wird ein neues Element angezeigt:

   ![Neue Metadaten](package-metadata.resources/package-metadata-03.png "Neue Metadaten")
1. Es gibt ein Feld &quot;Schlüssel&quot; und ein Feld &quot;Wert&quot;. Beide Optionen sind beliebig wählbar. Das Feld &quot;Schlüssel&quot; muss in der Liste einen eindeutigen Wert aufweisen.

   ![Neuer Metadatenwert](package-metadata.resources/package-metadata-04.png "Neuer Metadatenwert")
1. Sie können auch den &quot;Typ&quot; des Elements auswählen. Im Moment kann es &quot;String&quot; oder &quot;URL&quot; sein:

   ![Metadatentyp ändern](package-metadata.resources/package-metadata-05.png "Metadatentyp ändern")
1. &quot;URL&quot; bedeutet hier einen Verweis auf eine Ressource, die im Paket enthalten ist. Wählen Sie dazu eine Datei auf Ihrer Festplatte aus und ziehen Sie sie per Drag &amp; Drop in das Paket im Explorer. Dabei kann es sich um eine normale Ressource wie ein Bild oder eine beliebige andere Datei wie eine Textdatei handeln.

   ![Generische Ressource im Paket](package-metadata.resources/package-metadata-06.png "Generische Ressource im Paket")
1. Die Datei wird als neue Ressource im Paket angezeigt.

   Kehren Sie nun zum Bedienfeld &quot;Paketeigenschaften&quot; zurück, erstellen Sie neue Metadaten, geben Sie einen passenden Schlüssel ein und wählen Sie &quot;URL&quot; als Typ. Wählen Sie dann &quot;...&quot; aus. im Feld &quot;Wert&quot; und wählen Sie &quot;Von Ressource&quot; aus. Wählen Sie die Datei aus, die Sie zuvor eingefügt haben, und überprüfen Sie:

   ![URL-Metadaten](package-metadata.resources/package-metadata-07.gif "URL-Metadaten")
1. Jetzt können Sie die &quot;URL&quot; der Ressource wird im Feld &quot;Wert&quot; gespeichert.

   Sie können Metadaten auch über die Schaltfläche &quot;X&quot; rechts neben dem Element löschen:

   ![Metadaten löschen](package-metadata.resources/package-metadata-08.png "Metadaten löschen")

>[!NOTE]
>
> Das Verschieben oder Neuanordnen von Metadateneinträgen ist deaktiviert: die Reihenfolge ist nicht aussagekräftig und wird bei der Veröffentlichung des Pakets nicht beibehalten.

## Metadaten in veröffentlichten SBSAR-Dateien

In einigen Fällen können Sie die Metadaten abrufen, die Sie für ein Paket in der entsprechenden veröffentlichten SBSAR definiert haben. Im Folgenden erfahren Sie, wie Metadaten transformiert und im Archiv gespeichert werden und wie Sie sie daraus richtig nutzen können.

Die Metadaten werden entsprechend dem JSON-Format in einer Datei mit dem Namen /assemblies/content/0000/metadata.json gespeichert (der Pfad ist relativ zum Stammordner des .sbsar-Archivs).

Reguläre (String-)Metadaten werden wie vorhanden gespeichert, z. B. &quot;key&quot;: &quot;stringValue&quot;, eine pro Zeile. Auch hier wird die ursprüngliche Reihenfolge der verschiedenen Schlüssel nicht beibehalten und die Implementierung ist definiert. Verlassen Sie sich bei Ihrem Prozess nie auf die Bestellung, wie bei regulären Python-Aufträgen!

Da das Ziel der URL-Metadaten darin besteht, Benutzern und Plug-ins die Aufnahme ausländischer Dateien in das .sbsar-Archiv zu ermöglichen, unterliegen sie einer bestimmten Transformation: Zunächst wird die Datei der Ressource, die mit der gespeicherten URL übereinstimmt, in das Archiv an einem implementierungsdefinierten Speicherort (normalerweise in einem nummerierten Unterordner, der nur diese Datei enthält) kopiert. Es geht darum, Namenskonflikte zu vermeiden.) Die Datei behält ihren ursprünglichen Namen bei (der Name der Ressource wird an dieser Stelle verworfen). Anstelle der ursprünglichen URL in der Datei &quot;metadata.json&quot; wird dann der Pfad zur kopierten Datei im Archiv relativ zur Datei &quot;metadata.json&quot; geschrieben.

Wenn wir das im vorherigen Abschnitt erstellte Beispielpaket exportieren (nachdem wir mindestens ein Diagramm mit einigen Ausgaben erstellt haben), erhalten wir diesen Archivinhalt:

```
myPackage.sbsar

|-- assemblies

        |-- content

            |-- 0000

                |-- New_Graph.sbsasm

                |-- New_Graph.xml

                |-- metadata.json

                |-- resources

                    |-- 0

                        |-- TEXT.txt
```


Der Inhalt metadata.json lautet:

```
{

    "myResource": "resources/0/TEXT.txt",

    "myText": "This is a text"

}
```


Derzeit wird kein spezielles Tool für den Zugriff auf die im Archiv gespeicherten Metadaten und Ressourcen bereitgestellt. Die empfohlene Methode ist, das Archiv mit dem LZMA-Decoder Ihrer Wahl zu öffnen und die Datei metadata.json mit einem regulären JSON-Parser zu analysieren (Wenn die Schlüssel oder Wertzeichenfolgen einige Sonderzeichen enthalten, werden sie auf die JSON-Art und Weise escaped).

>[!NOTE]
>
> Es sind keine Informationen übrig geblieben, ob es sich bei den einzelnen Metadaten um eine einfache Zeichenfolge oder eine URL handelt. Daher müssen Sie wissen, was jeder Schlüssel, den Sie lesen möchten, bedeuten soll.

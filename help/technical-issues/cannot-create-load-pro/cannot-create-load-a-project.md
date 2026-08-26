---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/cannot-create-load-a-project.html"
breadcrumb-title: ''
description: Beheben Sie Probleme beim Erstellen oder Laden von Projekten in Substance 3D Designer und suchen Sie nach Lösungen.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Cannot createload a project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Projekt kann nicht erstellt und geladen werden
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---


# Probleme beim Erstellen oder Laden eines Projekts

Auf dieser Seite werden häufige Ursachen für das Fehlschlagen beim Erstellen oder Laden von Projekten in Substance 3D Designer aufgeführt und für jeden dieser Fehler entsprechende Schritte zur Fehlerbehebung aufgeführt.

## Anwendung ist zu alt zum Öffnen einer URL

**![(Fehler)](../../assets/error.svg) Problem**

Die **Substance 3D-Datei (SBS)** wird von einer Substance 3D Designer-Version geladen, die das Format *nicht unterstützt*. Die Substance 3D-Datei wurde wahrscheinlich *in einer neueren Version* der Software gespeichert, die ein aktualisiertes Format für diese Dateien verwendet.

**![(tick)](../../assets/check.svg) Empfohlene Schritte**

Mit der Weiterentwicklung von Substance 3D Designer gilt dasselbe für das Substance 3D-Dateiformat (SBS). Oft muss eine neue Version der Software *Ihre Dateien* aktualisieren, damit sie die neuesten Funktionen unterstützen können.

Sie werden *aufgefordert*, diese Aktualisierung durchzuführen, wenn *die Datei zum ersten Mal* in einer neuen Version geladen wird.

>[!WARNING]
>
> Wenn die Datei &quot;*&quot; nach &quot;*&quot; gespeichert wurde, wurde die Aktualisierung angewendet, und auch die Formatversion ändert sich. Zu diesem Zeitpunkt kann &quot;*&quot; nicht mehr in vorherigen Substance 3D Designer-Versionen &quot;*&quot; geladen werden.
> 
> Diese Einschränkung gilt auch für die [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html).

Überprüfen Sie zunächst, ob Sie die neueste Version von Substance 3D Designer verwenden, die Ihre aktuelle Lizenz zulässt. Hier finden Sie die Punkte, an denen Sie auf die Updates für jede Edition zugreifen können:

* <b>Adobe Substance 3D-Abonnement:</b> Wechseln Sie zum Abschnitt Updates der Registerkarte Apps in der Anwendung [Adobe Creative Cloud Desktop](https://creativecloud.adobe.com/en/apps/download/creative-cloud)
* <b>[Substance3d.com](http://Substance3d.com)-Abonnement:</b> Aktualisieren Sie, wenn Sie in Substance 3D Designer dazu aufgefordert werden, oder laden Sie das neueste Installationsprogramm im Abschnitt [Meine Lizenzen](https://store.substance3d.com/user) der [Substance3d.com](http://substance3d.com)-Website herunter.
* <b>Steam:</b> Die Anwendung wird standardmäßig automatisch aktualisiert. Sie können die Aktualisierung manuell auslösen, indem Sie Substance 3D Designer starten oder den Bildschirm &quot;Downloads&quot; aufrufen

>[!WARNING]
>
> Vergewissern Sie sich, dass Sie Ihre Dateien nicht in eine vorherige Version von Substance 3D Designer *laden müssen, bevor Sie eine aktualisierte Datei speichern*.
> 
> Alternativ können Sie *eine Kopie* der Datei *erstellen, bevor Sie* in eine neue Substance 3D Designer-Version laden. Sie haben also immer eine Datei, zu der Sie zurückkehren können, wenn Sie eine frühere Softwareversion verwenden müssen.

## Absturz beim Erstellen oder Laden eines Projekts

<b>![(Fehler)](../../assets/error.svg) Problem </b>

Ein Absturz beim Erstellen oder Laden eines Projekts wird häufig durch einen Fehler bei der Initialisierung der [3D-Ansicht](../../interface/3d-view/3d-view.md) verursacht, der beim Einrichten des Arbeitsbereichs auftritt.

Wenn das System ein Laptop ist, erzwingt eine Drittanbieteranwendung möglicherweise einen *Energieverwaltungsplan*, der verhindert, dass die 3D-Ansicht die GPU des Systems verwendet. Dies kann zu einem Absturz führen, wenn kein anderes GPU-Gerät die Aufgabe an ihrer Stelle ausführen kann.

Ein Absturz kann auch auftreten, wenn die *Anzeigekonfiguration oder Skalierung* zwischen den Sitzungen geändert wurde, sodass der 3D-Ansicht-Renderframe an ungültigen Koordinaten erstellt wird.

<b>![(tick)](../../assets/check.svg) Empfohlene Schritte</b>

In Anbetracht der verschiedenen möglichen Ursachen für diesen Absturz empfehlen wir, die folgenden Schritte zur Fehlerbehebung in der angegebenen Reihenfolge auszuführen:

Grafiktreiber aktualisieren

Stellen Sie zunächst sicher, dass die Grafiktreiber auf dem neuesten Stand sind. Die neueste Version für Ihre GPU [finden Sie hier](https://www.nvidia.com/Download/index.aspx?lang=en-us) (NVIDIA), [hier](https://www.amd.com/en/support) (AMD) oder [hier](https://downloadcenter.intel.com/product/80939/Graphics-Drivers) (Intel).

Beste Leistung erzwingen

Suchen Sie nach Software, die den *Energieplan* Ihres Systems verwaltet (z. B. ASUS Armory Crate), insbesondere wenn das System ein Laptop ist.

Einige Power Management-Anwendungen können den Zugriff anderer Anwendungen auf die GPU des Systems einschränken oder die GPU-Leistung beeinträchtigen, was zu Abstürzen führen kann. Wenn eine Stromverwaltungsanwendung vorhanden und aktiv ist, wechseln Sie zu der Abo-Variante, die die beste Leistung bietet.

Erzwingen der Verwendung einer separaten GPU

Wenn Ihr System über *umschaltbare Grafiken* verfügt, sollten Sie die Verwendung der diskreten GPU (dGPU) für Substance 3D-Anwendungen erzwingen.

In den meisten Fällen wird dies in einer dedizierten Anwendung erreicht, die die GPU-Einstellungen steuert. Beispielsweise können Sie dies für NVIDIA-GPUs in der Anwendung &quot;NVIDIA-Systemsteuerung&quot; tun.

In der Registrierung gespeicherte Benutzeroberfläche zurücksetzen

Wenn der Absturz durch eine Änderung der Anzeigekonfiguration oder der Skalierung verursacht wird, können Sie versuchen, neben anderen Einstellungen die vorhandenen Registrierungseinträge für Designer zu löschen, um die Benutzeroberfläche vollständig zurückzusetzen.

Das Verfahren zum Ausführen dieses Zurücksetzens für jedes Betriebssystem wird im Folgenden beschrieben:

+++Windows
* Designer schließen

Designer schließen

* Öffnen Sie die Anwendung <b>Eingabeaufforderung</b>.

Öffnen Sie die Anwendung <b>Eingabeaufforderung</b>.

* Geben Sie den folgenden Befehl ein und drücken Sie <b>Enter</b>:

  <b>Creative Cloud-Desktop</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Designer" /f
  ```


  <b>Steam/Substance-Edition</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Allegorithmic\Substance Designer" /f
  ```


Geben Sie den folgenden Befehl ein und drücken Sie <b>Enter</b>:

<b>Creative Cloud-Desktop</b>

<b>Steam/Substance-Edition</b>

* Trennen Sie den zweiten Monitor von Ihrem System, und verbinden Sie ihn wieder (ignorieren Sie diesen Schritt, wenn *nicht* mehrere Bildschirme angeschlossen sind).

Trennen Sie den zweiten Monitor von Ihrem System, und verbinden Sie ihn wieder (ignorieren Sie diesen Schritt, wenn *nicht* mehrere Bildschirme angeschlossen sind).

* Starten Sie Designer, aber erstellen oder öffnen Sie *kein* Projekt.

Starten Sie Designer, aber erstellen oder öffnen Sie *kein* Projekt.

* Öffnen Sie in der oberen Leiste das Menü <b>Windows</b> und wählen Sie die Option <b>Neue 3D-Ansicht</b> aus.

Öffnen Sie in der oberen Leiste das Menü <b>Windows</b> und wählen Sie die Option <b>Neue 3D-Ansicht</b> aus.

* Überprüfen Sie, ob die <b>3D-Ansicht</b> korrekt initialisiert ist, und probieren Sie verschiedene Vorschaugitter im Menü <b>Szene</b> in der oberen Leiste des Bedienfelds aus.

Überprüfen Sie, ob die <b>3D-Ansicht</b> korrekt initialisiert ist, und probieren Sie verschiedene Vorschaugitter im Menü <b>Szene</b> in der oberen Leiste des Bedienfelds aus.

* Erstellen oder Öffnen von Materialien

Erstellen oder Öffnen von Materialien

+++

+++macOS
* Designer schließen

Designer schließen

* Öffnen Sie die Anwendung <b>Terminal</b>.

Öffnen Sie die Anwendung <b>Terminal</b>.

* Geben Sie den folgenden Befehl ein und drücken Sie <b>Enter</b>:

  <b>Creative Cloud-Desktop</b>

  ```
  rm ~/Library/Preferences/com.adobe.Adobe\ Substance\ 3D\ Designer.plist
  ```


  <b>Steam/Substance-Edition</b>

  ```
  rm ~/Library/Preferences/com.allegorithmic.Substance\ Designer.plist
  ```


Geben Sie den folgenden Befehl ein und drücken Sie <b>Enter</b>:

<b>Creative Cloud-Desktop</b>

<b>Steam/Substance-Edition</b>

* Trennen Sie den zweiten Monitor von Ihrem System, und verbinden Sie ihn wieder (ignorieren Sie diesen Schritt, wenn *nicht* mehrere Bildschirme angeschlossen sind).

Trennen Sie den zweiten Monitor von Ihrem System, und verbinden Sie ihn wieder (ignorieren Sie diesen Schritt, wenn *nicht* mehrere Bildschirme angeschlossen sind).

* Starten Sie Designer, aber erstellen oder öffnen Sie *kein* Projekt.

Starten Sie Designer, aber erstellen oder öffnen Sie *kein* Projekt.

* Öffnen Sie in der oberen Leiste das Menü <b>Windows</b> und wählen Sie die Option <b>Neue 3D-Ansicht</b> aus.

Öffnen Sie in der oberen Leiste das Menü <b>Windows</b> und wählen Sie die Option <b>Neue 3D-Ansicht</b> aus.

* Überprüfen Sie, ob die <b>3D-Ansicht</b> korrekt initialisiert ist, und probieren Sie verschiedene Vorschaugitter im Menü <b>Szene</b> in der oberen Leiste des Bedienfelds aus.

Überprüfen Sie, ob die <b>3D-Ansicht</b> korrekt initialisiert ist, und probieren Sie verschiedene Vorschaugitter im Menü <b>Szene</b> in der oberen Leiste des Bedienfelds aus.

* Erstellen oder Öffnen von Materialien

Erstellen oder Öffnen von Materialien

+++

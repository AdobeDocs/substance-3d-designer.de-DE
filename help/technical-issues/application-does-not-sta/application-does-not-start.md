---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/application-does-not-start.html"
breadcrumb-title: ''
description: Beheben Sie Probleme, die den Start von Substance 3D Designer verhindern, und finden Sie Lösungen zum Starten der Anwendung.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Application does not start
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Anwendung kann nicht gestartet werden
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 1%

---


# Anwendung kann nicht gestartet werden

Auf dieser Seite werden häufige Ursachen aufgeführt, warum Substance 3D Designer nicht ordnungsgemäß gestartet wurde, und es werden für jeden Benutzer Fehlerbehebungsschritte angezeigt, die nach Betriebssystem gruppiert sind:

[Designer 15.0 und höher](#version-15-0)

[Windows 10/11](#windows-10-11)

[Windows 7/8/8.1](#windows-7-8)

[Linux](#linux)

## Designer 15.0 und höher

<b>![(Fehler)](../../assets/error.svg) Problem </b>

Die Versionen 15.0 und höher von Designer können auf Systemen mit integrierter GPU (iGPU) und diskreter GPU (dGPU) nicht gestartet werden.

<b>![(tick)](../../assets/check.svg) Empfohlene Schritte</b>

Aktualisieren Sie die Grafiktreiber der iGPU. Die neuesten Treiber finden Sie hier:  [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)  | [AMD](https://www.amd.com/en/support/download/drivers.html)

## Windows 10/11

**![(Fehler)](../../assets/error.svg) Problem**

Substance 3D Designer kann auf Systemen mit Windows 10 oder Windows 11 nicht gestartet werden.

**![(tick)](../../assets/check.svg) Empfohlene Schritte**

Ältere Versionen von Designer können unter Windows 10 oder Windows 11 möglicherweise nicht gestartet werden, da im Lizenzvalidierungsprozess eine *veraltete* `libeay32.dll` Bibliothek verwendet wird.

Sie können versuchen, die Bibliothek durch eine *aktualisierte Version* zu ersetzen, z. B. durch die hier verteilte Version [hier](https://support.networkoptix.com/hc/en-us/articles/115015730007-Nx-Software-crashes-due-to-libeay32-dll-on-Windows) (wählen Sie die Datei für 32-Bit-Windows aus). Führen Sie dazu die folgenden Schritte aus:

1. Suchen Sie die Datei &quot;`libeay32.dll`&quot; im Installationsverzeichnis von Designer
1. Sichern Sie die Datei an einem sicheren Speicherort, wenn Sie sie in Zukunft wiederherstellen müssen
1. Datei durch die aktualisierte Version ersetzen
1. Designer starten

>[!WARNING]
>
> Nicht unterstützte Konfigurationen
> 
> Windows 10 wird nicht unterstützt. Weitere Informationen finden Sie auf der Seite [Systemanforderungen](../../getting-started/system-requirements/system-requirements.md).
> 
> Versionen von Designer, deren Wartungszeitraum bereits abgelaufen ist, werden nicht unterstützt. Diese Versionen werden möglicherweise nicht mehr zuverlässig ausgeführt, wenn wesentliche Änderungen am System vorgenommen werden, z. B. Betriebssystem-Upgrades.

## Windows 7/8/8.1

**![(Fehler)](../../assets/error.svg) Problem**

Substance 3D Designer kann auf Systemen mit Windows 7, Windows 8 oder Windows 8.1 nicht gestartet werden.

**![(tick)](../../assets/check.svg) Empfohlene Schritte**

Im Rahmen des Updates der Version **11.3.0** haben wir mehrere Bibliotheken, Tools und SDKs aktualisiert, die *die Kompatibilität* mit Versionen von Windows unter Windows 10 beschädigt haben.

Wir empfehlen *dringend*, ein Upgrade auf Windows 10 durchzuführen, da Microsoft selbst ältere Windows-Versionen nicht mehr für die normale Verwendung unterstützt (siehe [hier](https://www.microsoft.com/en-us/windows/windows-7-end-of-life-support-information) und [hier](https://docs.microsoft.com/en-us/lifecycle/faq/windows#windows-8.1)). Die weitere Verwendung dieser Versionen stellt daher ein *Sicherheitsproblem* dar.\
Wenn ein Upgrade auf Windows 10 nicht möglich ist, *aktualisieren Sie* Ihre Installation von Designer *Version* **11.2.2** nicht.

>[!WARNING]
>
> Nicht unterstützte Konfigurationen
> 
> Hinweis: Windows 7, Windows 8 und Windows 8.1 werden *nicht offiziell unterstützt*. Weitere Informationen finden Sie auf der Seite [Systemanforderungen](../../getting-started/system-requirements/system-requirements.md).

## Linux

<b>![(Fehler)](../../assets/error.svg) Problem </b>

Absturz beim Schließen des Startbildschirms und Anzeigen des Hauptfensters.

<b>![(tick)](../../assets/check.svg) Empfohlene Schritte</b>

Designer kann Python-Komponenten nicht laden, da die Systembibliothek <b>libffi.so</b> anstatt ihrer eigenen geladen wird.

Um sicherzustellen, dass Designer eine eigene Bibliothek lädt, verwenden Sie diesen Befehl im Designer-Installationsverzeichnis. Ersetzen Sie `%command%` durch Ihren Befehl, um Designer auszuführen:

```
LD_PRELOAD=./plugins/pythonsdk/lib/python3.11/lib-dynload/libffi.so.6 %command%
```


Beachten Sie, dass die Python-Versionsnummer von der ausgeführten Designer-Version abhängt:

* Unterhalb von 14.0.0: Python3.9
* kleiner als 12.1.0: Python3,7

+++Startoptionen für Dampf
Linux-Benutzer, die Designer von Steam aus starten, können den Befehl LD\_PRELOAD in den Startoptionen von Designer festlegen, wie unten gezeigt.

Anschließend kann Designer in allen zukünftigen Sitzungen normalerweise von Steam aus gestartet werden.

![Optionen für den Steam-Start](../../assets/steam_linux_launch_option.jpg "Optionen für den Steam-Start")



+++

**![(Fehler)](../../assets/error.svg) Problem**

Die Steam-Edition von Designer kann nicht gestartet werden und gibt keine Fehlermeldung aus.

**![(tick)](../../assets/check.svg) Empfohlene Schritte**

Sie können Fehlermeldungen erhalten, indem Sie stattdessen die Steam-Anwendung protokollieren.

Wie empfohlen [hier](https://github.com/ValveSoftware/steam-for-linux/issues/7114#issuecomment-629634260), schließen Sie Steam vollständig und führen Sie dann den folgenden Befehl von einem Terminal aus (oder erstellen Sie eine Verknüpfung für diesen Befehl):

```
steam 2>&1 | tee /path/to/logfile
```


<b>![(Fehler)](../../assets/error.svg) Problem</b><b>e</b>

Das `<b>xcb</b>`-Plug-In kann nicht geladen werden. Die folgende Meldung wird in der Befehlszeile angezeigt:

```
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found. 

This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem. 

 

Available platform plugins are: minimal, offscreen, xcb. 

 

Aborted (core dumped)
```


**![(tick)](../../assets/check.svg) Empfohlene Schritte**

Einige erforderliche Pakete fehlen. Führen Sie den folgenden Befehl aus dem Installationsverzeichnis von Designer aus:

```
ldd libQt5XcbQpa.so.5
```


Überprüfen Sie die gedruckte Liste auf Pakete, die als `not found` gemeldet wurden, und führen Sie dann den folgenden Befehl für jedes dieser fehlenden Pakete aus:

```
apt-get install <package-name>
```


E.g.

```
apt-get install libxcb-xinput0
```


<b>![(Fehler)](../../assets/error.svg) Problem </b>

Dieser Fehler wird beim Starten von Designer ausgelöst:

```
error while loading shared libraries: libcrypt.so.1: cannot open shared object file: No such file or directory
```


Eine von Designer geladene Systembibliothek ist mit der eigenen <b>libcrypto.so.1.1</b>-Bibliothek von Designer nicht kompatibel.

<b>![(tick)](../../assets/check.svg) Empfohlene Schritte</b>

Entfernen Sie die <b>`libcrypto.so.1.1`</b>-Bibliothek aus dem Installationsverzeichnis von Designer, sodass stattdessen die Systembibliothek verwendet wird.

>[!NOTE]
>
> Diese Problemumgehung funktioniert nur, wenn das System über eine eigene Bibliothek libcrypto.so.1 verfügt. In aktuellen Distributionen muss möglicherweise ein Kompatibilitätspaket wie <b>libxcrypt-compat</b> installiert werden.

<b>![(Fehler)](../../assets/error.svg) Problem </b>

Substance 3D Designer kann nicht auf Systemen gestartet werden, die *Arch-basierte* Linux-Distributionen verwenden.

**![(tick)](../../assets/check.svg) Empfohlene Schritte *(![(Warnung)](../../assets/warning.svg) Instable, nur AMD-GPUs!)***

Versuchen Sie, **program** (Teil der [AMDGPU-PRO](https://wiki.archlinux.org/title/AMDGPU_PRO) Treiber) zu installieren, und starten Sie Designer über diese Software. Sie können dies tun, indem Sie das Präfix &quot;`progl`&quot; im Befehl zum Starten der Anwendung verwenden:

```
progl <designer-application-path>
```


Beachten Sie, dass `progl` möglicherweise instabil ist. Dies sollte daher als *letztes Mittel* versucht werden.

>[!WARNING]
>
> Beachten Sie, dass archbasierte Distributionen von Linux *nicht unterstützt werden*. Weitere Informationen finden Sie auf der Seite [Systemanforderungen](../../getting-started/system-requirements/system-requirements.md).

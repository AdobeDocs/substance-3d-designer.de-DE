---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ''
description: Überprüfen Sie die Systemanforderungen für Substance 3D Designer , um sicherzustellen, dass Ihr Computer die erforderlichen Spezifikationen erfüllt.
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Systemanforderungen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# Unterstützte Systeme

Im Folgenden finden Sie eine Liste der von der Anwendung unterstützten Hardware und Systeme:

## Windows

|  | Minimum | Empfohlen | Optimal |
| --- | --- | --- | --- |
| <b>Betriebssystem</b> | Windows 11 64-Bit Version 23H2 | Windows 11 64-Bit Version 24H1 | Windows 11 64-Bit Version 24H2 |
| <b>CPU</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 ADA Generation AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 GB | 16 GB | 24 GB |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>Speicher</b> | SSD mit 30 GB verfügbarem Speicherplatz | SSD mit 50 GB verfügbarem Speicherplatz | SSD mit 70 GB verfügbarem Speicherplatz |

### MacOS

|  | Minimum | Empfohlen | Optimal |
| --- | --- | --- | --- |
| <b>Betriebssystem</b> | macOS 14 Sonoma | macOS 26 Tahoe | macOS 26 Tahoe |
| <b>CPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>GPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>Speicher</b> | SSD mit 30 GB verfügbarem Speicherplatz | SSD mit 50 GB verfügbarem Speicherplatz | SSD mit 70 GB verfügbarem Speicherplatz |

### Linux

| Unternehmen | dämpfen |
| --- | --- |
| RHEL 8 </br>RHEL 9 | Ubuntu 22,04 |

## Allgemeine Empfehlungen

* Für die Arbeit unter angenehmen Bedingungen empfehlen wir einen Monitor mit einer Auflösung größer als 1 Megapixel und breiter als 1280 Pixel.
* Viele Substance-Apps sind für RHEL8/9-Kompatibilität auf OpenSSL 1.1.1 angewiesen. Bei Systemen mit neueren OpenSSL-Versionen müssen Sie diese manuell bereitstellen.
* *Es wurden nur* Versionen <b>2019.x</b> und höher beglaubigt, um auf <b>MacOS 10.15</b> (Catalina) ausgeführt zu werden.
* <b>Remotedesktop</b> ist möglich, wenn ein OpenGL 3.3-Kontext verfügbar ist. Es funktioniert auf <b>Nvidia Quadro</b>, aber *nicht* auf Nvidia GeForce, da es nur einen OpenGL 1.4-Kontext bereitstellt. Wenn dies ein Problem ist, empfehlen wir die Verwendung alternativer Lösungen wie <b>VNC</b>/<b>Teamviewer</b>.
* Benutzer der <b>Steam</b>-Version sollten *die <b>Steam-Überlagerung</b> für Designer deaktivieren*, da sie Leistungsprobleme verursachen kann, wenn sie aktiv sind.

## Unterstützte GPUs

Im Folgenden finden Sie eine Liste der mit der Anwendung kompatiblen GPU:

* NVIDIA GeForce GTX 1060 und höher
* NVIDIA Quadro P2200 und höher
* AMD Radeon RX 580 und höher
* AMD Radeon Pro 5300 M

>[!TIP]
>
> **TDR (nur Windows)**
> 
> Für die beste Gesamtstabilität bei der Durchführung umfangreicher Berechnungen auf der GPU - z. B. Rendern komplexer Diagramme, Rendern in der 3D-Ansicht, Exportieren einer Szene aus der 3D-Ansicht usw. - wird dringend empfohlen, sicherzustellen, dass die <b>Timeout Detection and Recovery (TDR)</b>-Werte mit den Empfehlungen in [dieser Seite](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) unserer Dokumentation übereinstimmen.

## Nicht unterstützte Konfigurationen

<b>Windows</b>

* Virtuelle Computer werden nicht unterstützt.
* Windows Server wird nicht unterstützt.

<b>macOS</b>

* Intel-basierte macOS-Systeme werden nicht unterstützt.
* Es werden nur offizielle Apple-Konfigurationen unterstützt.
* eGPUs werden derzeit nicht unterstützt und haben möglicherweise Stabilitätsprobleme.

<b>Linux</b>

* Mesa-Treiber unter Linux werden nicht unterstützt.

<b>Beliebige Plattform</b>

* Integrierte GPUs werden auf x86-64-CPUs (Intel, AMD) nicht unterstützt.
* Die Verwendung von Designer in Kombination mit Software von Drittanbietern, die Designer-Aufrufe an die Grafiktreiber abfängt, wird nicht unterstützt. Diese Software umfasst:
  * Nachbearbeitungs-Injectors wie Schattierer, die Farbkorrektur anwenden, Kameraeffekte, ...
  * On-Screen-Overlays, z. B. benutzerdefinierte Fadenkreuze, GPU-Leistungsmetriken, Skins für Video-Streaming ...

## Mindestversionen von GPU-Treibern

Im Folgenden finden Sie eine Liste der erforderlichen Mindestversionen von GPU-Treibern, damit die Anwendung problemlos ausgeführt werden kann. Diese Liste kann mit der Veröffentlichung neuer Versionen geändert werden.

Informationen zum Herunterladen neuer Treiber finden Sie unter: [GPU hat veraltete Treiber](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers).

| Betriebssystem | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| <b>Windows</b> | GeForce 451,48 Quadro 451,48 | Radeon 19.7.1 Radeon Pro/FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.129.03 | Radeon 23.20 Pro 23.Q3 | Nicht unterstützt |

>[!NOTE]
>
> Unter **Mac OS** wird der GPU-Treiber vom Betriebssystem selbst bereitgestellt. Aktualisieren Sie auf die neueste Version Ihres Betriebssystems, um auf den neuesten Treiber zuzugreifen.

## GPU-Raytracing zum Backen

Um GPU-Raytracing über Optix oder DXR zu aktivieren, müssen die oben empfohlenen Treiber installiert sein.

<b>DXR</b> erfordert die folgende Mindestkonfiguration:

* <b>Windows 10</b> Version 1809. Weitere Informationen finden Sie auf [dieser Seite](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing).
* <b>GPU mit Pascal-Architektur</b> (Nvidia GeForce 10XX)

>[!TIP]
>
> GPU-Raytracing läuft optimal auf dedizierter Raytracing-Hardware wie NVIDIA GeForce RTX oder NVIDIA Quadro RTX GPUs.

## Tablets verwenden

Tablet-Benutzer unter <b>Windows</b> sollten die auf der folgenden Seite beschriebenen Einstellungen anwenden, um die zuverlässigste Erfahrung zu erzielen: [Konfigurieren von Stiften und Tablets](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets).

## Sprachen

Die Software-Benutzeroberfläche ist in den folgenden Sprachen verfügbar:

* Deutschland
* Englisch (Vereinigte Staaten)
* Español (Spanien)
* Français (Frankreich)
* Italiano (Italia)
* Portugiesisch (Brasilien)
* 日本語(日本)
* 한국어(한국)
* 简体中文(中国)

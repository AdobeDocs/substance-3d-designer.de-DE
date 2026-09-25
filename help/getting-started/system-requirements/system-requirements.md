---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ""
description: Überprüfen Sie die Systemanforderungen für Substance 3D Designer , um sicherzustellen, dass Ihr Computer die erforderlichen Spezifikationen erfüllt.
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Systemanforderungen
user-guide-description: ""
user-guide-title: ""
source-git-commit: aeb517a0def4b5bc2de723633f8932dfc03f052c
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%
---

# Systemanforderungen

Im Folgenden finden Sie eine Liste der von der Anwendung unterstützten Hardware und Systeme:

## Systemkonfiguration nach Plattform

### Windows

|             | Minimum | Empfohlen | Optimal |
|:------------|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| **Betriebssystem** | Windows 11 64-Bit Version 23H2 | Windows 11 64-Bit Version 24H1 | Windows 11 64-Bit Version 24H2 |
| **CPU** | Intel Core i5<br>AMD Ryzen 5 | Intel Core i7<br>AMD Ryzen 7 | Intel Core i9<br>AMD Ryzen 9 |
| **GPU** | NVIDIA GeForce RTX 2060 Super<br>NVIDIA Quadro RTX 4000<br>AMD Radeon RX 5700 XT<br>AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080<br>NVIDIA Quadro RTX A4000<br>AMD Radeon RX 6800 XT<br>AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090<br>NVIDIA Quadro RTX 5000 ADA Generation<br>AMD Radeon RX 7900 XTX<br>AMD Radeon Pro W7800 |
| **VRAM** | 8 GB | 16 GB | 24 GB |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **Speicher** | SSD mit 30 GB verfügbarem Speicherplatz | SSD mit 50 GB verfügbarem Speicherplatz | SSD mit 70 GB verfügbarem Speicherplatz |

### macOS

|             | Minimum | Empfohlen | Optimal |
|:------------|:----------------------------------|:----------------------------------|:----------------------------------|
| **Betriebssystem** | macOS 14 Sonoma | macOS 26 Tahoe | macOS 26 Tahoe |
| **CPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **GPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **Speicher** | SSD mit 30 GB verfügbarem Speicherplatz | SSD mit 50 GB verfügbarem Speicherplatz | SSD mit 70 GB verfügbarem Speicherplatz |

### Linux

| Unternehmen | dämpfen |
|:------------------|:-------------|
| RHEL 8</br>RHEL 9 | Ubuntu 22,04 |

## Allgemeine Empfehlungen

* Für die Arbeit unter angenehmen Bedingungen empfehlen wir einen Monitor mit einer Auflösung größer als 1 Megapixel und breiter als 1280 Pixel.
* Viele Substance-Apps sind für RHEL8/9-Kompatibilität auf OpenSSL 1.1.1 angewiesen. Bei Systemen mit neueren OpenSSL-Versionen müssen Sie diese manuell bereitstellen.
* *Nur* Versionen **2019.x** und höher wurden zur Ausführung auf **macOS 10.15 Catalina** notariell beglaubigt.
* **Remotedesktop** ist möglich, wenn ein OpenGL 3.3-Kontext verfügbar ist. Es funktioniert auf **Nvidia Quadro**, aber *nicht* auf Nvidia GeForce, da es nur einen OpenGL 1.4-Kontext bereitstellt. Wenn dies ein Problem ist, empfehlen wir die Verwendung alternativer Lösungen wie **VNC/Teamviewer**.
* Benutzer der **Steam**-Version sollten *die **Steam-Überlagerung**&#x200B;für Designer deaktivieren*, da sie Leistungsprobleme verursachen kann, wenn sie aktiv sind.

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
> Für eine optimale Gesamtstabilität bei der Durchführung umfangreicher Berechnungen an der GPU - z. B. beim Rendern komplexer Graf, beim Rendern in der 3D-Ansicht, beim Exportieren einer Szene aus der 3D-Ansicht usw. - wird dringend empfohlen, sicherzustellen, dass die **Timeout Detection and Recovery (TDR)**-Werte mit den Empfehlungen in [dieser &#x200B;](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) unserer Dokumentation übereinstimmen.

## Nicht unterstützte Konfigurationen

**Windows**

* Virtuelle Computer werden nicht unterstützt.
* Windows Server wird nicht unterstützt.

**macOS**

* Intel-basierte macOS-Systeme werden nicht unterstützt.
* Es werden nur offizielle Apple-Konfigurationen unterstützt.
* eGPUs werden derzeit nicht unterstützt und haben möglicherweise Stabilitätsprobleme.

**Linux**

* Mesa-Treiber unter Linux werden nicht unterstützt.

**Beliebige Plattform**

* Integrierte GPUs werden auf x86-64-CPUs (Intel, AMD) nicht unterstützt.
* Die Verwendung von Designer in Kombination mit Software von Drittanbietern, die Designer-Aufrufe an die Grafiktreiber abfängt, wird nicht unterstützt. Diese Software umfasst:
  * Nachbearbeitungs-Injectors wie Re-Shader, die Farbkorrektur anwenden, Kamera-Effekte, ...
  * On-Screen-Overlays, z. B. benutzerdefinierte Fadenkreuze, GPU-Leistungsmetriken, Skins für Video-Streaming ...

## Mindestversionen von GPU-Treibern

Im Folgenden finden Sie eine Liste der erforderlichen Mindestversionen von GPU-Treibern, damit die Anwendung problemlos ausgeführt werden kann. Diese Liste kann mit der Veröffentlichung neuer Versionen geändert werden.

Informationen zum Herunterladen neuer Treiber finden Sie unter: [GPU hat veraltete Treiber](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers).

| Betriebssystem | NVIDIA | AMD | Intel |
|:------------|:-----------------------------|:-----------------------------------------|:------------|
| **Windows** | GeForce 451,48 Quadro 451,48 | Radeon 19.7.1 Radeon Pro/FirePro 18.Q4 | 15.33 |
| **Linux** | 535.129.03 | Radeon 23.20 Pro 23.Q3 | Nicht unterstützt |

>[!NOTE]
>
> Auf **macOS** wird der GPU-Treiber vom Betriebssystem selbst bereitgestellt. Aktualisieren Sie auf die neueste Version Ihres Betriebssystems, um auf den neuesten Treiber zuzugreifen.

## GPU-Raytracing zum Baking

Um GPU-Raytracing über Optix oder DXR zu aktivieren, müssen die oben empfohlenen Treiber installiert sein.

**DXR** erfordert die folgende Mindestkonfiguration:

* **Windows 10** Version 1809. Weitere Informationen finden Sie auf [dieser Seite](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing).
* **GPU mit Pascal-Architektur** (Nvidia GeForce 10XX)

>[!TIP]
>
> GPU-Raytracing läuft optimal auf dedizierter Raytracing-Hardware wie NVIDIA GeForce RTX oder NVIDIA Quadro RTX GPUs.

## Tablets verwenden

Tablet-Benutzer unter **Windows** sollten die auf der folgenden Seite beschriebenen Einstellungen anwenden, um die zuverlässigste Erfahrung zu erzielen: [Konfigurieren von Stiften und Tablets](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets).

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

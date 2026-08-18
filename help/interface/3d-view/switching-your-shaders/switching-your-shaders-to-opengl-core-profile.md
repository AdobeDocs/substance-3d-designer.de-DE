---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/interface/3d-view/switching-your-shaders-to-opengl-core-profile.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Shader in der Substance 3D Designer 3D-Ansicht auf das OpenGL-Kernprofil umstellen, um Kompatibilität und Leistung zu gewährleisten.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Switching your shaders to OpenGL Core Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Schattierungen auf OpenGL-Kernprofil umstellen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# Schattierungen auf OpenGL-Kernprofil umstellen

Seit Version 2018.2.0 verwendet der 3D-Viewport das OpenGL-Kernprofil.\
Bei dieser Gelegenheit haben wir einige Shader aktualisiert, die wir mit der Anwendung von GLSL-Version 120 auf GLSL-Version 330 zur Verfügung stellen.

Sie können Ihre eigenen Shader aktualisieren, um entweder die neuen verfügbaren GLSL-Funktionen zu nutzen oder Ihren GLSL-Code moderner zu gestalten. Beachten Sie, dass unter MacOS alte Shader möglicherweise nicht mehr funktionieren.\
Um einen vollständigen Überblick über die neuen Funktionen zu erhalten, empfehlen wir Ihnen dringend, die offizielle OpenGL-Dokumentation durchzusehen. Sie können sich beispielsweise die [OpenGL Schattierung Language Specification 3.30](https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.3.30.pdf) ansehen.\
Andernfalls finden Sie hier eine Kurzanleitung, die Ihnen helfen wird, Ihre GLSL 1.20-Shader in GLSL 3.30 zu konvertieren:

## Versionsnummer aktualisieren

Ersetzen Sie zunächst Ihre vorherige `#version`-Direktive durch `#version 330` (oder fügen Sie sie oben in Ihrer Datei hinzu, falls Sie sie noch nicht haben).

### Ersetzen Sie &quot;Attribut&quot; und &quot;abweichend&quot; durch &quot;ein&quot; oder &quot;aus&quot;.

Jetzt werden `attribute` und `varying` Variablen explizit als `in` oder `out` deklariert, abhängig von der Shader-Phase:

Im Vertexshader werden `attribute`s der Scheitelpunkte als `in` deklariert, während `varying`s, die an den Fragmentshader übergeben werden sollen, als `out` deklariert werden.\
Beispiel:

```
## version 120



attribute vec3 vertexPosition;

attribute vec3 vertexNormal;

attribute vec2 vertexUV;



varying vec3 fragmentNormal;

varying vec2 fragmentUV;
```


wird zu:

```
## version 330



in vec3 vertexPosition;

in vec3 vertexNormal;

in vec2 vertexUV;



out vec3 fragmentNormal;

out vec2 fragmentUV;
```


Genauso wird im Fragment-Shader das Variieren berücksichtigt. Sie sollten auch eine out-Variable deklarieren, die gl\_FracColor ersetzt (die nicht mehr integriert ist):

```
## version 120



varying vec3 fragmentNormal;

varying vec2 fragmentUV;



void main() {

...

gl_FragColor = vec4(myColor.rgb, 1.0);

}
```


wird zu:

```
## version 330



in vec3 fragmentNormal;

in vec2 fragmentUV;



out vec4 outColor; //you could choose any name you want here



void main() {

...

outColor = vec4(myColor.rgb, 1.0);

}
```


### Neue Textursuchfunktionen verwenden

Mit der neuen Version von Schattierung wurde die Texture-Lookup-API vereinfacht und erweitert.

Die Funktionen `texture1D()`, `texture2D()`, `texture3D()` und `textureCube()` werden alle zu Überladungen von `texture()`.\
Ebenso wird `texture2DLod()` zu `textureLod()`, `texture2DGrad()` zu `textureGrad()` usw.

Sie haben jetzt auch Zugriff auf nützliche Funktionen wie `textureSize()` (zum Abfragen der Größe des Samplers in Texel), `textureOffset()` (zum Aufnehmen von Nachbarn des Zielspeicherorts), `textureFetch()` (zum Bereitstellen eines Beispielspeicherorts in Pixel) und vieles mehr.

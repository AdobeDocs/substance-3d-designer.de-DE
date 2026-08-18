---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/glslfx-shaders.html"
breadcrumb-title: ''
description: Verwenden Sie die GLSLFX-Shader in der Substance 3D Designer-3D-Ansicht, um das Rendern von Material anzupassen und Vorschaueffekte anzupassen.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > GLSLFX Shaders
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GLSLFX Shader
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '3098'
ht-degree: 1%

---


# GLSLFX Shader

GLSLFX-Dateien stellen die Brücke zwischen der Anwendung und den glsl shader-Dateien dar.\
Es ermöglicht die Verwendung eines beliebigen glsl-Shaders, ohne den Code ändern zu müssen.

## Dateiformat

Das GLSLFX-Dateiformat ist eine XML-Datei. Kommentare werden unterstützt.

### Kopf- und Stammknoten

Das XML-Stammknotenelement hat den Namen <b>glslfx</b>.

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->

</glslfx>
```


### Body

#### Technik

XML-Element, das eine Technik beschreibt. Eine Technik ist eine Variante des aktuellen FX. Ein GLSLFX kann mehrere Techniken enthalten, aber mindestens eine Technik muss definiert werden.

Die Geometrie wird mit einer der in der Anwendung definierten Techniken gerendert.

+++XML-Elementdefinition
<b>Name:</b> Technik

<b>Attribute:</b>

* Name: Beliebige Zeichenfolge, die zum Benennen der Technik verwendet wird

+++

Das XML-Element kann mehrere untergeordnete Elemente haben. Die in einer Technik definierten Elemente überschreiben die global definierten Elemente.

Sie wird beispielsweise verwendet, um bestimmte Uniformwerte zu überschreiben und FX-Variationen für diese Technik zu erhalten.

#### Renderdurchgang

XML-Element, das eine Renderdurchlauf beschreibt. Ein Renderdurchgang beschreibt das Rendern der Geometrie.

Eine Technik kann mehrere Renderdurchläufe enthalten, die nacheinander ausgeführt werden. Eine Technik, die keinen Renderdurchgang enthält, entspricht einer Technik, die einen &quot;On-Screen&quot;-Renderdurchgang enthält.

Die in einem Renderdurchlauf definierten Elemente überschreiben die in der übergeordneten Technik definierten Elemente.

+++XML-Elementdefinition
<b>Name:</b> übergeben

<b>Attribute:</b>

* Ausgabe

* offscreen: Das Rendering erfolgt in benutzerdefinierten Renderzielen.

* auf dem Bildschirm: Das Rendering erfolgt im Standard-Renderziel

+++

#### Shader

Legen Sie die GLSL-Shader-Dateien für jeden Typ fest.

XML-Elementdefinition:

+++XML-Elementdefinition
<b>Name:</b> Shader

<b>Attribute:</b>

* Typ: Der GLSL-Shader-Typ.

* Dateiname: Der Pfad der GLS-Shader-Datei. Kann absolut oder relativ zur GLSLFX-Datei sein;

* primitiveType: Die Methode zum Rendern der Grundform.


| &#39;type&#39;-Wert | Beschreibung |
| --- | --- |
| Scheitelpunkt | Vertex-Shader |
| Geometrie | Geometry Shader |
| tess\_control | Tesselierungssteuerungs-Shader |
| tess\_eval | Tesselierung Evaluation Shader |
| Fragment | Fragment-Shader |



| primitiveType-Wert | Beschreibung |
| --- | --- |
| Punkt | Als Punkte rendern |
| Linienführung | Als Zeilenschleife rendern |
| Patch[1.N] | Als Patches mit [1.N] Scheitelpunkten rendern |


+++

#### Eigenschaften

Erlauben Sie, einen Teil des OpenGL-Status einzurichten.

+++XML-Elementdefinition
<b>Name:</b>, Eigenschaft

<b>Attribute:</b>

* name: Der Name der festzulegenden Eigenschaft. Der Name basiert auf der OpenGL-Funktion oder dem glEnum-Namen:
  * Enumerationssyntax: Ohne das Präfix &quot;GL\_&quot;, in Kleinbuchstaben. Beispiele: glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;&quot;
  * Funktionssyntax: ohne das Präfix &quot;gl&quot;, in Kleinbuchstaben und mit allen Wörtern getrennt durch das Zeichen &quot;\_&quot;. Beispiel: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* Enumerationssyntax: Ohne das Präfix &quot;GL\_&quot;, in Kleinbuchstaben. Beispiele: glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;&quot;

* Funktionssyntax: ohne das Präfix &quot;gl&quot;, in Kleinbuchstaben und mit allen Wörtern getrennt durch das Zeichen &quot;\_&quot;. Beispiel: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* Wert: Der Wert der Eigenschaft.


| Namenswerte | &#39;value&#39; Werte | Beschreibung |
| --- | --- | --- |
| blend\_enabled | boolesch | Mischmodus aktivieren/deaktivieren |
|  | true |  |
|  | false |  |
| blend\_func | Zeichenfolge, Zeichenfolge | Festlegen der Funktionen für Quellen und Ziel-Überblendung |
|  | Null | für OpenGL enum GL\_ZERO |
|  | eins | für OpenGL enum GL\_ONE |
|  | src\_color | für OpenGL enum GL\_SRC\_COLOR |
|  | one\_minus\_src\_color | für OpenGL-Enumeration GL\_ONE\_MINUS\_SRC\_COLOR |
|  | dst\_color | für OpenGL enum GL\_DST\_COLOR |
|  | one\_minus\_dst\_color | für OpenGL-Enumeration GL\_ONE\_MINUS\_DST\_COLOR |
|  | src\_alpha | für OpenGL enum GL\_SRC\_ALPHA |
|  | one\_minus\_src\_alpha | für OpenGL-Enumeration GL\_ONE\_MINUS\_SRC\_ALPHA |
|  | dst\_alpha | für OpenGL enum GL\_DST\_ALPHA |
|  | one\_minus\_dst\_alpha | für OpenGL-Enumeration GL\_ONE\_MINUS\_DST\_ALPHA |
|  | Konstante\_Farbe | für OpenGL enum GL\_CONSTANT\_COLOR |
|  | one\_minus\_constant\_color | für OpenGL-Enumeration GL\_ONE\_MINUS\_CONSTANT\_COLOR |
|  | Konstante\_Alpha | für OpenGL enum GL\_CONSTANT\_ALPHA |
|  | one\_minus\_constant\_alpha | für OpenGL-Enumeration GL\_ONE\_MINUS\_CONSTANT\_ALPHA |
|  | src\_alpha\_saturate | für OpenGL-Enumeration GL\_SRC\_ALPHA\_SATURATE |
|  | src1\_color | für OpenGL enum GL\_SRC1\_COLOR |
|  | one\_minus\_src1\_color | für OpenGL-Enumeration GL\_ONE\_MINUS\_SRC1\_COLOR |
|  | src1\_alpha | für OpenGL enum GL\_SRC1\_ALPHA |
|  | one\_minus\_src1\_alpha | für OpenGL-Enumeration GL\_ONE\_MINUS\_SRC1\_ALPHA |
| cull\_face\_enabled | boolesch | Aktivieren/Deaktivieren der Gesichtskeulung |
|  | true |  |
|  | false |  |
| cull\_face\_mode | String | Legen Sie den Gesichtsauswaschmodus fest. |
|  | Front | für OpenGL enum GL\_FRONT |
|  | Rückseite | für OpenGL enum GL\_BACK |
|  | front\_and\_back | für OpenGL-Enumeration GL\_FRONT\_AND\_BACK |
| Tiefe\_Funktion | String | Tiefe-Vergleichsfunktion einstellen |
|  | nie | für OpenGL enum GL\_NEVER |
|  | weniger | für OpenGL enum GL\_LESS |
|  | legal | für OpenGL enum GL\_LEQUAL |
|  | Gleichgestellter | für OpenGL enum GL\_EQUAL |
|  | ungleich | für OpenGL enum GL\_NOTEQUAL |
|  | Gequal | für OpenGL enum GL\_GEQUAL |
|  | größer | für OpenGL enum GL\_GREATER |
|  | Immer | für OpenGL enum GL\_ALWAYS |


+++

#### Uniformen

Erlaubt das Überschreiben einiger Uniformen, die global oder in der übergeordneten Technik definiert sind. Dies ermöglicht es, das Shader-Verhalten für diese Technik oder diesen Render-Pass zu ändern.

Weitere Informationen zu ihrer Definition finden Sie im Abschnitt <b>Uniforms</b> weiter unten.

+++Beispiel


+++

## Renderziele

Bei &quot;Offscreen&quot;-Renderdurchläufen müssen Renderziele im Renderdurchlauf definiert werden.

+++XML-Elementdefinition
<b>Name:</b> Ausgabe

<b>Attribute:</b>

* Anlage: Der OpenGL-Anfügepunkt, inspiriert von den OpenGL-Namen:\
  GL\_COLOR\_ATTACHMENT[0.3] => &#39;color[0.3]&#39;\
  GL\_TIEFE\_ANLAGE => &#39;Tiefe&#39;

Anlage: Der OpenGL-Anfügepunkt, inspiriert von den OpenGL-Namen:\
GL\_COLOR\_ATTACHMENT[0.3] => &#39;color[0.3]&#39;\
GL\_TIEFE\_ANLAGE => &#39;Tiefe&#39;

* Name: den Namen des Renderziels.\
  Sie kann in einem späteren Renderdurchgang verwendet werden, um dieses Renderziel als Sampler zu binden.

Name: den Namen des Renderziels.\
Sie kann in einem späteren Renderdurchgang verwendet werden, um dieses Renderziel als Sampler zu binden.

* Format: das interne Format des Renderziels.

Format: das interne Format des Renderziels.

* klar: optionales Attribut, das einen Clear-Wert definiert.\
  Wenn vorhanden, wird das Renderziel zu Beginn des Renderdurchgangs auf diesen Wert gelöscht.\
  Wenn das Renderziel fehlt, bleibt der vorherige Inhalt erhalten.

+++

>[!NOTE]
>
> Farb-Renderziele sind in einem &quot;On-Screen&quot;-Renderdurchgang verboten, aber ein Tiefe-Renderziel kann mit jedem Renderdurchgang gemeinsam genutzt werden (das Rendering wird jedoch wahrscheinlich unterbrochen, wenn mehrere Materialien in der Szene gemischt werden).

<b>Formate</b>

Bei Tiefe-Formaten werden alle OpenGL-Formate nur für Tiefe (keine Schablone) unterstützt:

* GL\_TIEFE\_COMPONENT16 => &#39;Tiefe26&#39;
* GL\_TIEFE\_COMPONENT24 => &#39;Tiefe34&#39;
* GL\_TIEFE\_COMPONENT32 => &#39;Tiefe42&#39;
* GL\_TIEFE\_COMPONENT32F => &#39;Tiefe42f&#39;

Bei Farbformaten basiert der Name auf OpenGL-Enumerationsnamen, in Kleinbuchstaben ohne das Präfix &quot;GL\_&quot;.\
Drei Kanalformate (RGB) werden nicht unterstützt. Verwenden Sie stattdessen ein RGBA-Format.\
Unterstützte Bittiefe pro Kanal:

* Normalisierte Ganzzahl ohne Vorzeichen: 8, 16
* Gleitkomma: 16, 32

Eine Ausnahme von diesen Regeln ist das GL\_R11F\_G11F\_B10F, das unterstützt wird:

* GL\_RGBA8 =>&#39;rgba8&#39;
* GL\_RGBA16F =>&#39;rgba16f&#39;
* GL\_SRGB8\_ALPHA8 => &#39;srgb8\_alpha8&#39;
* GL\_R11F\_G11F\_B10F => &#39;r11f\_g11f\_b10f&#39;
* GL\_RG16 => &quot;rg16&quot;

### Sampler

Erlaubt das Überschreiben einiger global definierter Sampler. Diese können nicht in einer Technik definiert werden. Dies ermöglicht es, eine Samplerverwendung für diesen Renderdurchgang zu definieren oder von einem Renderziel eines vorherigen Renderdurchgangs zu lesen.

Weitere Informationen zu ihrer Definition finden Sie im Abschnitt <b>Samplers</b>.

+++Beispiel


+++

## Eingabescheitelpunktformat

Dadurch können Sie die Semantik der einzelnen Attribute definieren, die im Vertexshader definiert werden.

<b>XML-Elementdefinition:</b>

Name: vertexformat

Attribute:

* &#39;name&#39;: Der Name des Attributs, wie im Vertexshader definiert.
* &quot;semantisch&quot;: Die Semantik des Attributs.

| semantischer Wert | Beschreibung |
| --- | --- |
| Position | Scheitelpunktposition (float3) |
| normal | Scheitelpunkt Normal (float3) |
| texcoord[0..N] | Scheitelpunkt-Textur-Koordinatenpuffer N (float2) |
| Tangente[0..N] | Scheitelpunkt-Tangentenpuffer N (float4) |
| binormal[0..N] | Scheitelpunkt-Binormalpuffer N (float4) |

Beispiel:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- INPUT VERTEX FORMAT -->

     <vertexformat name="iVS_Position" semantic="position"/>

     <vertexformat name="iVS_Normal" semantic="normal"/>

     <vertexformat name="iVS_UV" semantic="texcoord0"/>

     <vertexformat name="iVS_Tangent" semantic="tangent0"/>

     <vertexformat name="iVS_Binormal" semantic="binormal0"/>

</glslfx>
```


## Sampler

Dadurch kann die Verwendung der einzelnen Sampler definiert werden.\
Es wird von der Anwendung verwendet, um zu wissen, welche Textur in den angegebenen Samplern eingestellt werden soll.

<b>XML-Elementdefinition:</b>

Name: &quot;Probenehmer&quot;

Attribute:

* &#39;name&#39;: Der Name der Samplervariable in der Shader-Datei.
* &#39;Nutzung&#39;: Die Verwendung des Samplers. Es entspricht der Verwendung, die im Ausgabeknoten des Diagramms angegeben ist.

| Wert &quot;usage&quot; | Beschreibung |
| --- | --- |
| diffus | Diffuse Karte |
| Deckkraft | Deckkraftmap |
| Ausstrahlend | Emissionskarten |
| Ambientokklusion | Umgebungskarte Verdeckung |
| umgebend | Umgebungskarte |
| maskieren | Maskenübersicht |
| detailnormal | Detail Normalmap |
| normal | Normalen-Map |
| Stoß | Bumpmap |
| Höhe | Height Map |
| Versatz | Versatz Map |
| Spiegelebene | Specular level Map |
| Glanzfarbe | Specular-Farbkarte |
| Glanz | Specular Map |
| Glanzintensität | Glossiness Map |
| Rauheit | Rauigkeitskarte |
| Anisotropiegrad | Anisotropiestufe |
| Anisotropiewinkel | Anisothropiekarte |
| durchscheinend | Transmissive Karte |
| Nachdenken | Reflexionskarte |
| Brechung | Refraktionskarte |
| Umgebung | Umgebungskarte (Cubemap) |
| Panorama | Die Panoramakarte (Längen-/Breitenkarte) |
| Bluenoisemask | Eine 256 x 256-Dithering-Textur |

* Es werden mehrere Verwendungen unterstützt.
  * Beispiel:

```
   <!-- SAMPLERS -->

    <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <!-- ... -->
```


&#39;isHidden&#39;: Boolescher Wert, der angibt, ob der Sampler in der GUI angezeigt werden soll

* Beispiel:

```
     <!-- SAMPLERS -->

    <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <!-- ... -->
```


Umbruchmodus:

<table data-preserve-html="true"><tbody><tr><th>Name</th><th>Wert</th></tr><tr><td rowspan="4">texture_wrap_s, texture_wrap_t, texture_wrap_r<br/><br/><br/></td><td>clip_to_edge</td></tr><tr><td>clip_to_border</td></tr><tr><td colspan="1">mirrored_repeat</td></tr><tr><td colspan="1">wiederholen<br/><br/></td></tr></tbody></table>

Texturfilter

<table data-preserve-html="true"><tbody><tr><th>Name</th><th>Wert</th></tr><tr><td rowspan="6">texture_min_filter, texture_mag_filter<br/><br/><br/></td><td>nächste</td></tr><tr><td>linear</td></tr><tr><td colspan="1">nearest_mipmap_nearest</td></tr><tr><td colspan="1">linear_mipmap_nearest</td></tr><tr><td colspan="1">nearest_mipmap_linear</td></tr><tr><td colspan="1">linear_mipmap_linear</td></tr></tbody></table>

Beispiel:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- SAMPLERS -->

     <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <sampler name="heightMap" usage="height"/>

     <sampler name="normalMap" usage="normal"/>

     <sampler name="detailNormalMap" usage="detailNormal"/>

     <sampler name="environmentMap" usage="environment"/>

     <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <sampler name="sssDiffuseMap" usage="sssDiffuse"/>

</glslfx>
```


## Uniformen

Auf diese Weise können Sie zusätzliche Informationen zu jeder Shader-Uniform hinzufügen.

<b>XML-Elementdefinition:</b>

Name: &quot;Uniform&quot;

Attribute:

&#39;name&#39;: Der Name der Uniform in der Shader-Datei.

| semantischer Wert | Beschreibung |
| --- | --- |
| Welt | World Matrix (float16) |
| worldinversetranspose | World Inverse Transpose Matrix (float16) |
| WeltbildProjektion | World View Projection Matrix (float16) |
| Ansichtsverse | World Inverse Matrix (float16) |
| Weltsicht | World View Matrix (float16) |
| Modellansicht | Modellansichtsmatrix (float16) |
| projection | Projektionsmatrix (float16) |
| umgebend | Umgebungsfarbe der Szene (float3) |
| lightposition[0..N] | Position des N-ten Lichts der Szene (float3) |
| lightcolor[0..N] | Farbe des N-ten Lichts der Szene (float3) |
| Lichtintensität[0..N] | Intensität des N-ten Lichts der Szene (float) |
| GlobalTime | Aktuelle Zeit in Sekunden (Gleitkomma) |
| Beschluss | Viewport-Auflösung (int2) |
| Maus | Mausposition (int2) |
| Beispielpostablesize | Anzahl der Samples, die zur Berechnung der Umgebungsbeleuchtung verwendet werden sollen (int) |
| Bestrahlungsköche | Das Array der sphärischen Oberwellenvektoren (float3[10]) |
| panoramamipmapheight | Anzahl der Mipmap-Stufen in der Panoramakarte (float) |
| Panoramarotation | Winkel Drehwinkel der Panoramakarte (float) |
| Panoramaintensität | Intensität der Panoramakarte (float) |
| ComputerBinormalinfragmentshader | Wird das binormale Fragment pro Fragment berechnet? (wenn nicht dann pro Scheitelpunkt) (bool) |
| isdirectxnormal | Ist die Normalen-Map-Format DirectX ? bool) |
| uvwscale | Skalierungswerte von u, v, w (float3) |
| renderuvtil | Nur 1 UV-Kachel rendern ? bool) |
| uvtilecoords | Zu rendernde UV-Kachelkoordinate (int2) |

&quot;semantisch&quot;: Die Semantik der Uniform. (Alle Matrizen sind float16).

Beispiel:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- MATRICES -->

     <uniform name="worldMatrix" semantic="world"/>

     <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

     <uniform name="worldViewMatrix" semantic="worldview"/>

     <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

     <uniform name="viewInverseMatrix" semantic="viewinverse"/>

     <uniform name="modelViewMatrix" semantic="modelview"/>

     <uniform name="projectionMatrix" semantic="projection"/>

</glslfx>
```


Beispiel:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>

</glslfx>
```


### Andere Parameter

Weitere zusätzliche Informationen können zu jeder Uniform hinzugefügt werden:

* den Standardwert definieren
* Spannwerte
* steuert, wie die Uniform in der Anwendung angezeigt wird:
* Aufkleber festlegen
* Festlegen der Widget-Informationen, die zum Bearbeiten des Werts in der Anwendung verwendet werden:
* Widget-Name, min, max, Schritt zum Erhöhen/Verringern
* Gruppenuniformen in Gruppen-Widgets

Da die Uniformen für jede Technik überschrieben werden können, kann für jede Technik eine bestimmte GUI-Einrichtung angezeigt werden.

<b>XML-Elementdefinition:</b>

Name: &quot;Uniform&quot;

Attribute:

* &#39;name&#39;: Der Name der Uniform in der Shader-Datei.
* &#39;default&#39;: Der einheitliche Standardwert
* &#39;min&#39;: Der Minimalwert des Gültigkeitsbereichs
* &#39;max&#39;: Der Höchstwert des Gültigkeitsbereichs
* &#39;guiName&#39;: Der Name der Uniform in der GUI der Anwendung
* &#39;guiGroup&#39;: Der Name der Gruppe, die die Uniform in die GUI der Anwendung einfügen soll
* &#39;guiWidget&#39;: Der Name des Widgets, das zum Bearbeiten des einheitlichen Werts in der Benutzeroberfläche der Anwendung verwendet wird

| guiWidget-Wert | Beschreibung |
| --- | --- |
| Regler | Regler-Widget für floatN |
| Winkel | Winkel-Widget für Gleitkommawerte |
| Farbe | Farb-Widget für &quot;float3&quot;, &quot;float4&quot; |
| Kontrollkästchen | CheckBox-Widget für bool |

* &#39;guiMin&#39;: Der Mindestwert des Widgets
* &#39;guiMax&#39;: Der Höchstwert des Widgets

## Beispiel: Tesselierung/Parallaxe

### Parallax Scheitelpunkt-Schattierungs-Datei

In .\tessellation\_parallax\parallax\vs.glsl

Inhalt:

> #version 120

Attribut vec4 iVS\_Position;\
Attribut vec4 iVS\_Normal;\
Attribut vec2 iVS\_UV;\
Attribut vec4 iVS\_Tangent;\
Attribut vec4 iVS\_Binormal;

variierendes vec3 iFS\_Normal;\
variierendes vec2 iFS\_UV;\
variierendes vec3 iFS\_Tangent;\
variierendes vec3 iFS\_Binormal;\
variierendes vec3 iFS\_PointWS;

Uniform Mat4 WorldMatrix;\
uniform mat4 worldViewProjMatrix;

void main()\
{\
gl\_Position = worldViewProjMatrix \&#42; iVS\_Position;\
iFS\_Normal = iVS\_Normal.xyz;\
iFS\_UV = iVS\_UV;\
iFS\_Tangent = iVS\_Tangent.xyz;\
iFS\_Binormal = iVS\_Binormal.xyz;\
iFS\_PointWS = (worldMatrix \&#42; iVS\_Position).xyz;\
}

### Tesselation Vertex Shader-Datei

In .\tessellation\_parallax\tessellation\vs.glsl

Inhalt:

>> 

#version 120

Attribut vec4 iVS\_Position;\
Attribut vec4 iVS\_Normal;\
Attribut vec2 iVS\_UV;\
Attribut vec4 iVS\_Tangent;\
Attribut vec4 iVS\_Binormal;

variierendes vec4 oVS\_Normal;\
variierendes vec2 oVS\_UV;\
variierendes vec4 oVS\_Tangent;\
variierendes vec4 oVS\_Binormal;

void main()\
{\
gl\_Position = iVS\_Position;\
oVS\_Normal = iVS\_Normal;\
oVS\_UV = iVS\_UV;\
oVS\_Tangent = iVS\_Tangent;\
oVS\_Binormal = iVS\_Binormal;\
}

### Tesselierungssteuerungsschattierungsdatei

In .\tessellation\_parallax\tessellation\tcs.glsl

Inhalt:

>> 

#version 400 Core\
#extension GL\_ARB\_tessellation\_shader : befähigen

layout(vertices = 3) out;

in vec4 oVS\_Normal[];\
in vec2 oVS\_UV[];\
in vec4 oVS\_Tangent[];\
in vec4 oVS\_Binormal[];

out vec4 oTCS\_Normal[];\
out vec2 oTCS\_UV[];\
out vec4 oTCS\_Tangent[];\
out vec4 oTCS\_Binormal[];

uniform float tesselationFactor;

void main()\
{\
gl\_TessLevelOuter[0] = tesselationFactor;\
gl\_TessLevelOuter[1] = tesselationFactor;\
gl\_TessLevelOuter[2] = tesselationFactor;\
gl\_TessLevelInner[0] = tesselationFactor;\
gl\_out[gl\_InvocationID].gl\_Position = gl\_in[gl\_InvocationID].gl\_Position;

oTCS\_Normal[gl\_InvocationID] = oVS\_Normal[gl\_InvocationID];\
oTCS\_UV[gl\_InvocationID] = oVS\_UV[gl\_InvocationID];\
oTCS\_Tangent[gl\_InvocationID] = oVS\_Tangent[gl\_InvocationID];\
oTCS\_Binormal[gl\_InvocationID] = oVS\_Binormal[gl\_InvocationID];\
}

### Tesselierungsauswertung Shader-Datei

In .\tessellation\_parallax\tessellation\tcs.glsl

Inhalt:

>> 

#version 400 Core

layout(triangles, equal\_spacing, ccw) in;

in vec4 TCS\_Normal[];\
in vec2 oTCS\_UV[];\
in vec4 TCS\_Tangent[];\
in vec4 TCS\_Binormal[];

Uniform Mat4 WorldMatrix;\
uniform mat4 worldViewProjMatrix;

Uniform Sampler2D heightMap;

Kacheln mit gleichmäßigem Schwimmer = 1,0f;\
uniform float heightMapScale = 1.0f;

out vec3 iFS\_Normal;\
out vec2 iFS\_UV;\
out vec3 iFS\_Tangent;\
out vec3 iFS\_Binormal;\
out vec3 iFS\_PointWS;

vec3 interpolieren3D(vec3 v0, vec3 v1, vec3 v2, vec3 uvw)\
{\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
}

vec2 interpolate2D(vec2 v0, vec2 v1, vec2 v2, vec3 uvw)\
{\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
}

void main()\
{\
vec3 uvw = gl\_TessCoord.xyz;

vec3 newPos = interpolate3D(gl\_in[0].gl\_Position.xyz, gl\_in[1].gl\_Position.xyz, gl\_in[2].gl\_Position.xyz, uvw);\
vec3 newNormal = normalize(interpolate3D(oTCS\_Normal[0].xyz, oTCS\_Normal[1].xyz, oTCS\_Normal[2].xyz, uvw));\
vec3 newTangent = normalize(interpolate3D(oTCS\_Tangent[0].xyz, oTCS\_Tangent[1].xyz, oTCS\_Tangent[2].xyz, uvw));\
vec3 newBinormal = normalize(interpolate3D(oTCS\_Binormal[0].xyz, oTCS\_Binormal[1].xyz, oTCS\_Binormal[2].xyz, uvw));\
vec2 newUV = interpolate2D(oTCS\_UV[0], oTCS\_UV[1], oTCS\_UV[2], uvw);

float heightTextSample = texture(heightMap, newUV \&#42; tiling).x \&#42; 2.0 - 1.0;\
newPos += newNormal \&#42; heightTextSample \&#42; heightMapScale;

vec4 obj\_pos = vec4(newPos, 1);\
gl\_Position = worldViewProjMatrix \&#42; obj\_pos;

iFS\_UV = newUV \&#42; Tiling;\
iFS\_Tangent = newTangent;\
iFS\_Binormal = newBinormal;\
iFS\_Normal = newNormal;\
iFS\_PointWS = (worldMatrix \&#42; obj\_pos).xyz;\
}

### Fragment Shader File

In .\tessellation\_parallax\fs.glsl

Inhalt:

>> 

#version 120

// #define ALG\_NORMAL\_DIRECTX\
#define ALG\_NORMAL\_OPENGL

#ifdef ALG\_NORMAL\_DIRECTX\
// #define FLIP\_NORMAL\_X\
#define FLIP\_NORMAL\_Y\
// #define FLIP\_NORMAL\_Z\
#endif //#ifdef ALG\_NORMAL\_DIRECTX

#ifdef ALG\_NORMAL\_OPENGL\
// #define FLIP\_NORMAL\_X\
#define FLIP\_NORMAL\_Y\
// #define FLIP\_NORMAL\_Z\
#endif //#ifdef ALG\_NORMAL\_OPENGL

variierendes vec3 iFS\_Normal;\
variierendes vec2 iFS\_UV;\
variierendes vec3 iFS\_Tangent;\
variierendes vec3 iFS\_Binormal;\
variierendes vec3 iFS\_PointWS;

uniform vec3 Lamp0Pos = vec3(0.0f,0.0f,70.0f);\
uniform vec3 Lamp0Color = vec3(1.0f,1.0f,1.0f);\
uniform vec3 Lamp1Pos = vec3(70.0f,0.0f,0.0f);\
uniform vec3 Lamp1Color = vec3(0,198f,0,198f,0,198f);\
Normal = true;\
Uniform Float TilingDetail = 3.0f;\
Specexpon = 50,0;\
Gleichmäßiger Schwimmer Ks = 1,0;\
uniform int parallax\_mode = 0;\
uniform float tesselationFactor = 4.0;\
uniform float heightMapScale = 1.0f;\
uniform float Tiefe\_detail = 0,5f;\
einheitlicher Schwimmer Kr = 0,5f;\
uniform int KF\_on = 1;\
KFs = 1,0f;\
uniform vec3 AmbiColor = vec3(0,07f,0,07f,0,07f);\
Kacheln mit gleichmäßigem Schwimmer = 1,0f;\
uniform int enableTilingInFS = 0;

Uniform Sampler2D heightMap;\
Uniform Sampler2D normalMap;\
uniform sampler2D detailNormalMap;\
Uniform Sampler2D emissiveMap;\
Uniform Sampler2D DiffuseMap;\
uniform sampler2D specularMap;\
uniform sampler2D opacityMap;\
uniform samplerCube environmentMap;

Uniform Mat4 WorldMatrix;\
Uniform mat4 worldInverseTransposeMatrix;\
uniform mat4 viewInverseMatrix;

vec4 litFct(float NdotL, float NdotH, float specExp)\
{\
float ambient = 1,0;\
float diffuse = max(NdotL, 0,0);\
float Specular = step(0.0, NdotL) \&#42; pow(max(0.0, NdotH), specExp);\
return vec4(ambient, diffuse, Specular, 1.0);\
}

vec3 lerpFct(vec3 v0, vec3 v1, float percent)\
{\
return v0 + (v1-v0) \&#42; percent;\
}

// Phong-Schattierung\
void phong\_Schattierung(\
in vec3 LightColor,\
in vec3 normalWS,\
in vec3 pointToLightDirWS,\
in vec3 pointToCameraDirWS,\
inout vec3 DiffuseContrib,\
inout vec3 SpecularContrib)\
{\
vec3 Hn = normalize(pointToCameraDirWS + pointToLightDirWS);\
vec4 litV = litFct(dot(normalWS, pointToLightDirWS), dot(normalWS, Hn), SpecExpon);\
DiffuseContrib = litV.y \&#42; LightColor;\
SpecularContrib = litV.y \&#42; litV.z \&#42; Ks \&#42; LightColor;\
}

vec3 fixNormalSample(vec3 v)\
{\
vec3 result = v - vec3(0,5,0,5,0,5);

#ifdef FLIP\_NORMAL\_X\
result.x = -result.x;\
#endif // ifdef FLIP\_NORMAL\_X\
#ifdef FLIP\_NORMAL\_Y\
result.y = -result.y;\
#endif // ifdef FLIP\_NORMAL\_Y\
#ifdef FLIP\_NORMAL\_Z\
result.z = -result.z;\
#endif // ifdef FLIP\_NORMAL\_Z

Rückgabeergebnis;\
}

vec3 normalVecOSToWS(vec3 normal)\
{\
normale Rückkehr;\
}

void main()\
{\
vec3 cameraPosWS = viewInverseMatrix[3].xyz;\
vec3 pointToLight0DirWS = normalize(Lamp0Pos - iFS\_PointWS);\
vec3 pointToLight1DirWS = normalize(Lamp1Pos - iFS\_PointWS);\
vec3 pointToCameraDirWS = normalize(cameraPosWS);\
vec3 normalOS = normalize(iFS\_Normal);\
vec3 tangentOS = normalize(iFS\_Tangent);\
vec3 binormalOS = normalize(iFS\_Binormal);

// ------------------------------------------\
// Vergewissern Sie sich, dass die TBN orthonormalisiert ist\
binormalOS = normalize(cross(normalOS, tangentOS));\
tangentOS = normalize(cross(binormalOS, normalOS));

vec3 cumulatedNormalOS = normalOS;

// ------------------------------------------\
// Update UV\
float a = dot(normalOS,-pointToCameraDirWS);\
vec3 s = vec3(dot(pointToCameraDirWS,tangentOS), dot(pointToCameraDirWS,binormalOS), a);\
vec2 uv = enableTilingInFS == 0 ? iFS\_UV : (iFS\_UV \&#42; Tiling);\
float Height = texture2D(heightMap,uv).x \&#42; 2.0 - 1.0 ;\
float parallax = parallax\_mode == 0 ? (tesselationFactor / 100000.f + heightMapScale / 500.f) : (heightMapScale / 50.f);\
uv += (Height \&#42; s.xy \&#42; Parallaxe);

// ------------------------------------------\
// Add Normal from normalMap\
vec3 normalTS = texture2D(normalMap,uv).xyz;\
normalTS = fixNormalSample(normalTS);\
vec3 normalMapOS = normalTS.x\&#42;tangentOS + normalTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalMapOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

// ------------------------------------------\
// Details zur Normalmap hinzufügen\
vec3 normalDetailTS = texture2D(detailNormalMap,uv\&#42;TilingDetail).xyz;\
normalDetailTS = fixNormalSample(normalDetailTS);\
vec3 variableNormalDetailTS = lerpFct(vec3(0.0,0.0,0.5),normalDetailTS,Tiefe\_detail);\
vec3 normalDetailOS = variableNormalDetailTS.x\&#42;tangentOS + variableNormalDetailTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalDetailOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

if (length(normalTS)&lt;0.0001)\
cumulatedNormalOS = normalOS;

vec3 cumulatedNormalWS = normalVecOSToWS(cumulatedNormalOS);

// ------------------------------------------\
// Compute Diffuse &amp; Specular

// Lichtspende 0\
vec3 diffContrib = vec3(0, 0, 0);\
vec3 specContrib = vec3(0, 0, 0);\
phong\_Schattierung(Lamp0Color, cumulatedNormalWS, pointToLight0DirWS, pointToCameraDirWS, diffContrib, specContrib);

// Lichtbeitrag 1\
vec3 diffContrib2 = vec3(0, 0, 0);\
vec3 specContrib2 = vec3(0, 0, 0);\
phong\_Schattierung(Lamp1Color, cumulatedNormalWS, pointToLight1DirWS, pointToCameraDirWS, diffContrib2, specContrib2);

diffContrib += diffContrib2;\
specContrib += specContrib2;

vec4 diffuseColor = texture2D(diffuseMap,uv);

vec3 specularColor = texture2D(specularMap,uv).rgb;\
vec3 R = reflect(pointToCameraDirWS,cumulatedNormalWS);\
vec3 reflColor = Kr \&#42; textureCube(environmentMap,R.xyz).bgr;

float FallofRefl;

if (KFs >= 0,0)\
FallofRefl = max(1-dot(pointToCameraDirWS/(KFs),cumulatedNormalWS)),0)\&#42;KF\_on;\
sonst\
FallofRefl = (1-max((1-dot(pointToCameraDirWS/(-KFs),cumulatedNormalWS))),0))\&#42;KF\_on;

if (KF\_on == 0)\
FallofRefl=1.0;

vec3 Ambiant\_final = diffuseColor.rgb\&#42;AmbiColor;

// ------------------------------------------\
vec3 emissive = texture2D(emissiveMap,uv).xyz;

vec3 finalcolor = Ambiant\_final\
+ specularColor\&#42;specContrib\
+ diffuseColor.rgb\&#42;diffContrib\
+ (reflColor\&#42;specularColor\&#42;FallofRefl)\
+ emissiv;

// Final Color\
vec4 finalColor4 = vec4(finalcolor, texture2D(opacityMap,uv));

gl\_FragColor = finalColor4;\
}

### GLSLFX Datei

Die glslfx-Datei definiert zwei Techniken zum Rendern der Geometrie:

* Man verwendet die Hardware-Tesselierungstechnik
* Die andere basiert auf einem Parallaxeffekt, der als Fallback verwendet wird, wenn die Benutzer-Hardware die Tessellation nicht unterstützt.

In .\tessellation\_parallax\fs.glsl

Inhalt:

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE sbsbatchnode SYSTEM "glslfx.dtd">

<glslfx version="1.0.0" author="allegorithmic.com">



    <!-- TECHNIQUES -->

    <technique name="Tesselation">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/tessellation/vs.glsl" primitiveType="patch4"/>

        <shader type="tess_control" filename="tessellation_parallax/tessellation/tcs.glsl"/>

        <shader type="tess_eval" filename="tessellation_parallax/tessellation/tes.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="0" max="0" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="0" max="0" />

        <uniform name="tessellationFactor" guiName="Tessellation Factor" default="4" min="1" max="64" guiStep="1" guiWidget="slider"/>

    </technique>



    <technique name="Parallax">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/parallax/vs.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="1" max="1" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="1" max="1" />



    </technique>



    <!-- INPUT VERTEX FORMAT -->

    <vertexformat name="iVS_Position" semantic="position"/>

    <vertexformat name="iVS_Normal" semantic="normal"/>

    <vertexformat name="iVS_UV" semantic="texcoord0"/>

    <vertexformat name="iVS_Tangent" semantic="tangent0"/>

    <vertexformat name="iVS_Binormal" semantic="binormal0"/>



    <!-- SAMPLERS -->

    <sampler name="diffuseMap" usage="diffuse"/>

    <sampler name="heightMap" usage="height"/>

    <sampler name="normalMap" usage="normal"/>

    <sampler name="detailNormalMap" usage="detailNormal"/>

    <sampler name="emissiveMap" usage="emissive"/>

    <sampler name="specularMap" usage="specular"/>

    <sampler name="opacityMap" usage="opacity"/>

    <sampler name="environmentMap" usage="environment"/>



    <!-- MATRICES -->

    <uniform name="worldMatrix" semantic="world"/>

    <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

    <uniform name="worldViewMatrix" semantic="worldview"/>

    <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

    <uniform name="viewInverseMatrix" semantic="viewinverse"/>

    <uniform name="modelViewMatrix" semantic="modelview"/>

    <uniform name="projectionMatrix" semantic="projection"/>



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>



    <!-- UNIFORMS -->

    <uniform name="tiling" guiName="Tiling" default="1" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="heightMapScale" guiGroup="Height" guiName="Scale" default="1" min="0" guiWidget="slider" guiMin="-50" guiMax="50" />

    <uniform name="TilingDetail" guiGroup="Detail Normal" guiName="Tiling" default="3" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="Depth_detail" guiGroup="Detail Normal" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.05" guiWidget="slider"/>

    <uniform name="SpecExpon" guiGroup="Specular" guiName="Power" default="50" min="1" guiWidget="slider" guiMax="128"/>

    <uniform name="Ks" guiGroup="Specular" guiName="Intensity" default="1" min="0" guiWidget="slider" guiMax="3"/>

    <uniform name="Kr" guiGroup="Reflection" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.01" guiWidget="slider"/>

    <uniform name="KF_on" guiGroup="Reflection" guiName="Falloff" default="1" min="0" max="1" guiStep="1" guiWidget="slider"/>

    <uniform name="KFs" guiGroup="Reflection" guiName="Falloff Size" default="1" min="-1" max="1" guiStep="0.05" guiWidget="slider"/>



</glslfx>
```

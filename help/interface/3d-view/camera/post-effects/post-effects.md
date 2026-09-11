---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/camera/post-effects.html"
breadcrumb-title: ''
description: Wenden Sie Nachbearbeitungseffekte auf die Kamera der 3D-Ansicht an, um eine verbesserte Materialvorschau und Visualisierung zu ermöglichen.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Camera > Post effects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Post-Effekte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# Post-Effekte

![Effekte nach &#x200B;](../../../../assets/postEffects.png "Effekte nach "){zoomable="yes"}

In den Kameraeigenschaften können Sie Nachbearbeitungseffekte aktivieren, um das Rendering zu verbessern, oder bestimmte Materialeigenschaften überprüfen.

Diese Effekte werden intern entwickelt und sind nur für die Rasterizer- und GPU-Pathtracer [renderers](../../../../interface/3d-view/3d-renderers/3d-renderers.md) verfügbar.

Jeder Post-Effekt, der zum Zeitpunkt des Speicherns von [3D-Szenenressourcen](../../../../resources/3d-scene-resource/3d-scene-resource.md) oder [Szenenstatusdateien](../../../../working-with-3d-scenes/working-with-3d-scenes.md) aktiviert ist, wird als Teil des Szenenstatus gespeichert.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Ton-Mapping

</td>
<td style="border: 0;" valign="top">

### Bloom

</td>
<td style="border: 0;" valign="top">

### Feldtiefe

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Ton-Mapping

Ordnet die Farben des Renderings gemäß bestimmten Algorithmen und/oder Nachschlagetabellen (LUT) neu zu.

So können Sie die Farbkonsistenz zwischen Anwendungen verbessern. Zum Beispiel ist der AgX-Farbtonzuweiser auch in Blender verfügbar.

+++Reinhard


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXReinhard.jpg" alt="PostFXReinhard">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXReinhard](../../../../assets/PostFXReinhard.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAtan.jpg" alt="PostFXAtan">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAtan](../../../../assets/PostFXAtan.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXExp.jpg" alt="PostFXExp">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXExp](../../../../assets/PostFXExp.jpg "PostFXExp")

+++

+++Protokoll


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXLog.jpg" alt="PostFXLog">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXLog](../../../../assets/PostFXLog.jpg "PostFXLog")

+++

+++Asse


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAces.jpg" alt="PostFXAces">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAces](../../../../assets/PostFXAces.jpg "PostFXAces")

+++

+++Hejl


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXHejl.jpg" alt="PostFXHejl">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXHejl](../../../../assets/PostFXHejl.jpg "PostFXHejl")

+++

+++Neutral


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXNeutral.jpg" alt="PostFXNeutral">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXNeutral](../../../../assets/PostFXNeutral.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAgx.jpg" alt="PostFXAgx">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAgx](../../../../assets/PostFXAgx.jpg "PostFXAgx")

+++

+++Pbr neutral


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXPbrNeutral.jpg" alt="PostFXPbrNeutral">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXPbrNeutral](../../../../assets/PostFXPbrNeutral.jpg "PostFXPbrNeutral")

+++

## Bloom

Simuliert den Effekt in der Kamera, wenn Lichtstreifen von sehr hellen Bereichen nach außen auf Bereiche mit geringerem Lichteinfall treffen.

Die Wirkung wird durch die Beleuchtung, die Belichtung der Kamera und die emissive-Materials der Szene beeinflusst.

+++Schwellenwert
Die Luminanz, über der die Blüte sichtbar sein soll.

*Links: 1.0 / Rechts: 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![bloomThreshold1](../../../../assets/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](../../../../assets/bloomThreshold4.jpg "bloomThreshold4")

+++

+++Abnahme
Die Blütendämpfungsrampe, bei der ein niedrigerer Wert zu einem kürzeren Blütenradius führt.

*Links: 1.0 / Rechts: 0.6*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![bloomFalloff1](../../../../assets/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](../../../../assets/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++Tonwertkorrektur
Die Intensität der Blüte. Ein höherer Wert führt zu helleren, ausgeprägteren Lichträndern.

*Links: 8.0 / Rechts: 2.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![bloomLevel8](../../../../assets/bloomLevel8.jpg "bloomLevel8")

![bloomLevel2](../../../../assets/bloomLevel2.jpg "bloomLevel2")

+++

+++Farbverschiebung
Verschiebt den Farbton der von der Blüte betroffenen Bereiche in Richtung wärmerer Farben.

*Links: 0.0 / Rechts: 0,8*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![bloomColorShift0](../../../../assets/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](../../../../assets/bloomColorShift0-8.jpg "bloomColorShift0-8")

+++

## Feldtiefe

Simuliert ein optisches Phänomen, das durch Kameras verursacht wird, bei denen Objekte, die näher und weiter als die Fokusentfernung sind, unscharf werden.

Der Effekt wird sowohl von den Parametern &quot;F-Stopp&quot; als auch &quot;Fokusabstand&quot; der Kamera beeinflusst.

>[!TIP]
>
> Um den Fokus auf die Kamera schnell anzupassen, platzieren Sie den Cursor an der Stelle, an der sich die Szene im Fokus befinden soll, und drücken Sie Strg+LMB (Windows) bzw. Befehl+LMB (macOS), um den Fokusabstand automatisch auf diese Stelle einzustellen.

+++Max. Radius
Der maximale Radius des Weichzeichnungseffekts.

*Links: 32.0 / Rechts: 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius32.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius4.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](../../../../assets/depthOfFieldMaxRadius32.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](../../../../assets/depthOfFieldMaxRadius4.jpg "depthOfFieldMaxRadius4")

+++

+++Stärke der Komposition
Die Stärke des Weichzeichnungseffekts von der Fokusentfernung nach außen.

*Links: 0.2 / Rechts: 0,05*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-2.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-05.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](../../../../assets/depthOfFieldCompositeStrength0-2.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](../../../../assets/depthOfFieldCompositeStrength0-05.jpg "depthOfFieldCompositeStrength0-05")

+++

+++Longitudinale Aberration
Die Intensität der Aberration, die außerhalb des Fokusabstands auftritt.

Die Aberration simuliert, wie unterschiedliche Wellenlängen eine leicht unterschiedliche Brennweite haben. Die Farben scheinen versetzt zu sein und weisen subtile Fokusunterschiede auf.

*Links: 0,0 / RIght: 1.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration0.jpg" alt="depthOfFieldLongitudinalAberration0">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration1.jpg" alt="depthOfFieldLongitudinalAberration1">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![depthOfFieldLongitudinalAberration0](../../../../assets/depthOfFieldLongitudinalAberration0.jpg "depthOfFieldLongitudinalAberration0")

![depthOfFieldLongitudinalAberration1](../../../../assets/depthOfFieldLongitudinalAberration1.jpg "depthOfFieldLongitudinalAberration1")

+++

+++Achromatische Aberration
Gibt an, ob die Aberration achromatisch sein soll, d. h., dass einige oder alle Farben die gleiche Brennweite haben.

Dadurch wirkt der Weichzeichnungseffekt gleichmäßiger verteilt.

*Links: Wahr/Rechts: False*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationYes.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationNo.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](../../../../assets/depthOfFieldAchromaticAberrationYes.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](../../../../assets/depthOfFieldAchromaticAberrationNo.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++Katzenaugeneffekt
Aktiviert den Augeneffekt der Katze in der Szene. Damit wird simuliert, wie schräg einfallendes Licht nicht auf die Scheibe einfällt, sondern in ein unebenes Oval, was zu Verzerrung führt.

Dieser Effekt ist bei höheren Blendenwerten, d. h. bei niedrigeren Blendenwerten, ausgeprägter.

*Links: Wahr/Rechts: False*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>Nach</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg "depthOfFieldAchromaticCatsEyeNo")

+++

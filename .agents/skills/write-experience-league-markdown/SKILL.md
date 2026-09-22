---
name: write-experience-league-markdown
description: |
  Syntaxregeln, benutzerdefinierte Erweiterungen und Gotchas zum Schreiben von auf Adobe Experience League veröffentlichten Markdown-Inhalten. Verwenden Sie diese Fähigkeit beim Erstellen oder Bearbeiten einer Seite unter "help" oder in diesem Repo (oder in einem anderen Experience League-Inhalts-Repo) - Überschriften, Verknüpfungen, Bilder, Tabellen, Hinweis-/Warnblöcke, UICONTROL/DNL-Tags, Videoeinbettungen, Anker und bekannte Rendering-Fehler. Quelle: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 4%
---

# Experience League Markdown wird geschrieben

Experience League rendert Markdown mit GitHub-Geschmack durch eine benutzerdefinierte Pipeline
mit eigenen Erweiterungen und Rendering-Schwachstellen. Standard-GFM funktioniert meistens, aber
Die folgenden Elemente sind Experience League-spezifisch. Irren Sie sich, und geben Sie den Inhalt an.
Lint-/Link-Check-CI schlägt fehl oder wird auf der Live-Site falsch gerendert.

## Überschriften

* `#` bis `#####` (Stufen 1-5). Das `title`-Titelblatt der Seite ist
tatsächlich Stufe 0; Die erste Markdown-Überschrift im Textkörper sollte ein
Einzelne `# Level 1`-Überschrift, die mit dem Seitentitel übereinstimmt (oder diesem sehr ähnlich ist).
* Überspringen Sie Ebenen nicht willkürlich; Das mini-TOC wird aus Überschriften generiert.

## Textformatierung

* `**bold**`, `*italic*`, `***bold and italic***`.
* Escapezeichen mit Sonderzeichen mit umgekehrtem Schrägstrich (`\*`, `\_` usw.).
* **Und-Zeichen** in Überschriften/Titeln müssen ausgeschrieben (`and`) oder codiert sein als
  `&amp;` - ein RAW `&` in einem Titel kann die Analyse unterbrechen.
* **Als Literaltext verwendete Winkelklammern** (nicht echte HTML) müssen codiert sein:
  `<placeholder>` → `&lt;placeholder&gt;`.
* **Aus Textverarbeitungsprogrammen eingefügte typografische Anführungszeichen** müssen codiert sein und dürfen nicht als
Literale geschweifte Zeichen: linkes Doppelzeichen `&#8220;`, rechtes Doppelzeichen `&#8221;`,
Apostroph/rechte einzelne `&#8217;`.

## Listen

* Nummerierte Listen: Jedes Element mit `1.` (oder `1)`) starten — GitHub/Experience
Automatische Nummerierung der Liga unabhängig von den eingegebenen Literalziffern.
* Aufzählungslisten: `*`, `-` oder `+` verwenden, aber **Aufzählungszeichen nicht mischen
in derselben Liste/demselben Dokument**.
* Die Verschachtelung der Liste &quot;`TOC.md`&quot; verwendet `+` durchgehend. Folgen Sie der Verschachtelung der vorhandenen Datei
Auszeichnungsstil, anstatt einen anderen einzufügen.

## Verknüpfungen

* Interne Querverweise müssen **relative** Markdown-Links zu den
Zieldatei `.md`: `[Overview](../../overview.md)`
* Externe Verweise müssen **absolute** URLs sein.
* Anker in Überschriften/Bereiche einer anderen Seite: &quot;`#anchor-id`&quot; anfügen, z. B.
  `[Mesh](../../glossary/glossary.md#mesh)`.
* Seitenanker werden entweder als Überschrift (mit automatischem Schrägstrich) oder als
explizit `<span id="anchor-id"></span>` (HTML) / `{: #anchor-id}` (Markdown) unmittelbar vor dem Begriff —
Das im gesamten Repo verwendete Muster finden Sie unter `help/glossary/glossary.md`.
* `TOC.md`-Abschnittsanker verwenden `{#section-id}`-Syntax nach einer Überschrift/Liste.
Bezeichnung, z. B. `Getting started{#getting-started}`

## Bilder

Markdown-Bildsyntax verwenden, wann immer möglich:

```markdown
![Alt text](path/to/image.png "Optional hover text")
```

* Der `![...]`-Text ist ein barrierefreier Alternativtext erforderlich. Fassen Sie es kurz und tun Sie es
keine Unterstriche verwenden; Verwenden Sie stattdessen Leerzeichen oder Bindestriche.
* Der Bildpfad kann relativ zur Markdown-Datei oder stammrelativ sein, z. B.
als `/help/assets/shared-image.png`. Seitenspezifische Bilder gehören in der
Geschwisterordner &quot;`<page-name>.resources/`&quot; (zum Beispiel
  `<page-name>.resources/image.png`). `help/assets/` ist ein älterer freigegebener Ordner.
  Fügen Sie dort keine neuen seitenspezifischen Bilder hinzu.
* Optionale Parameter für die Bildabfrage können die CDN-Verarbeitung steuern:
  `?width=750&format=png&optimize=medium`. Diese Parameter im Bild beibehalten
  URL, vor jedem Eigenschaftsblock.
* Fügen Sie unmittelbar nach dem schließenden `)` Bildeigenschaften hinzu:
  `![Alt text](image.png "Hover text"){width="300" align="center"}`.
  `width` ist ein Pixelwert oder ein Prozentwert des Ansichtsbereichs. Abbildungsmaßstab
proportional ändern. Unterstützte Ausrichtungswerte sind `center` und `right`.
  `valign` wird nicht unterstützt.
* Verwenden Sie &quot;`modal="regular"`&quot; oder &quot;`zoomable="yes"`&quot;, um ein Bild durch Klicken zum Zoomen zu erstellen:
  `![Alt text](image.png){width="100" zoomable="yes"}`. Nicht kombinieren
  Klicken zum Zoomen mit einem Bildlink; hat der Hyperlink Vorrang.
* Um ein Bild mit einer anderen Seite zu verknüpfen, gliedern Sie das Bild in einen Markdown-Link ein:
  `[![Alt text](image.png)](../target/target.md)`.
* Geben Sie bei großen Bildern mindestens 640 Pixel der Quellbreite an, wenn dies praktisch ist.
Verwenden Sie nicht mehr als etwa 2000 Pixel, wenn es nicht erforderlich ist, und lassen Sie Bilddateien unter
5 MB, wo möglich. Die Pipeline akzeptiert Dateien mit bis zu 100 MB, Dateien werden jedoch über
20 MB Fehlervalidierung und Artikel sollten in der Regel nicht mehr als
100 Bilder (laut einiger älterer Richtlinien 200; die strengeren Grenzwerte verwenden).

Verwenden Sie HTML nur, wenn Markdown das erforderliche Layout nicht ausdrücken kann, z. B. ein
eine spezielle Tabelle oder eine spezielle Inline-Präsentation. Das unterstützte HTML-Bildformular
ist:

```html
<img src="image.png" alt="Alt text" />
```

* Geben Sie immer ein aussagekräftiges `alt`-Attribut an und verwenden Sie ein relatives oder
Root-relative `src`, die mit Markdown-Bildern konsistent ist.
* Für das HTML von Bildern innerhalb eines beibehaltenen Inline-HTML fügen Sie
  `data-preserve-html="true"` zu den enthaltenen Tags hinzufügen, wenn dies vom
  umgebender Markup. Beispiel:

  ```html
  <div data-preserve-html="true" align="center">
    <img src="my-page.resources/preview.gif" alt="Preview" />
  </div>
  ```

* Um das Klicken zum Zoomen für ein HTML-Bild zu aktivieren, verwenden Sie
  `class="modal-image"` im `<img>`-Tag.
* Verwenden Sie keine nicht unterstützten HTML-Attribute, oder verlassen Sie sich auf `valign`. Markdown bevorzugen
-Eigenschaften für Breite und Ausrichtung fest.

## Tabellen

Bevorzugen Sie native Markdown-Tabellen für gewöhnlichen Tabelleninhalt:

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

* Lege eine Leerzeile vor die Tabelle. Markdown-Tabellen erfordern mindestens eine
Kopfzeile und eine Standardzeile; Verwenden einer HTML-Tabelle für eine einzeilige oder ohne Überschrift
-Tabelle.
* Verwenden Sie mindestens drei Bindestriche in jeder Kopftrennzelle, und behalten Sie die gleiche
Anzahl der Pipe-Zeichen in jeder Zeile. Escapezeichen für eine literale Pipe als `\|` oder
  `&vert;`.
* Verwenden Sie bei Bedarf Ausrichtungsmarken in der Trennlinie:
  `|---|:---:|---:|` für linke, mittlere und rechte Ausrichtung.
* Inline-HTML wird in Markdown-Tabellenzellen für Absatzumbrüche und
einfachen Listen. Verwenden Sie `<p>` für separate Absätze, `<br>` für Zeilenumbrüche und
  `<ul>`/`<ol>` mit `<li>` Elementen für Listen. Addieren
  `data-preserve-html="true"` zum Inline-HTML von Elementen, wenn dies vom
  umgebendes Repository-Markup.

  ```markdown
  | Header | Details |
  |---|---|
  | Text | First paragraph.<p>Second paragraph.<br>New line.<ul><li>Item</li></ul> |
  ```

* Vermeiden von sehr breiten und sehr hohen Tischen; die Navigation ist schwierig.
Seien Sie bei Inline-Code in Tabellen vorsichtig, da langer Code
unverhältnismäßige Spaltenbreiten.
* Um das Tabellenlayout für eine Markdown-Tabelle auszuwählen, fügen Sie die Eigenschaft nach dem &quot;
Tabelle, getrennt durch eine Leerzeile:

  ```markdown
  {style="table-layout:fixed"}
  ```

  Verwenden Sie `table-layout:auto` (Standard), wenn langer Text oder Code flexibel sein muss.
  Spaltenbreiten. `fixed` für ausgeglichene Spalten verwenden, z. B. Tabellen, die
  Bilder ähnlicher Größe.

Verwenden einer HTML-Tabelle, wenn Markdown die erforderliche Struktur nicht ausdrücken kann, z. B.
Auslassen von Kopfzeilen, Kombinieren von Zellen mit Bereichen, Ausgleichen von Spalten oder Ausrichten
Inhalt in Zellen:

```html
<table style="table-layout:fixed">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td align="center">Example</td>
    <td>Details</td>
  </tr>
</table>
```

* Zu den unterstützten Tabellenelementen gehören `<table>`, `<tbody>`, `<thead>`, `<tfoot>`,
  `<tr>`, `<th>`, `<td>`, `<col>` und `<colgroup>`, zusammen mit unterstützten
Inline-Elemente wie `<p>`, `<br>`, `<b>`, `<i>`, `<ul>`, `<ol>` und
  `<li>`.
* Verwenden Sie keine Markdown-Syntax in einer HTML-Tabelle. Beispiel: Markdown
Notizen, Bilder und Links können wörtlich gerendert werden; Verwenden Sie stattdessen die HTML-Syntax.
  `UICONTROL` und `DNL` Lokalisierungstags sind Ausnahmen.
* `align="left"`, `align="center"` oder `align="right"` in einer Zelle verwenden, wenn
erforderlich ist. HTML Tabellen können keine verschachtelten Tabellen enthalten.
* Legen Sie das HTML-Tabellenlayout auf das öffnende Tag fest:
  `<table style="table-layout:auto">` oder
  `<table style="table-layout:fixed">`.
* Bei einer einzeiligen HTML ohne Rahmen verwenden Sie
  `<tr style="border: 0;">`.

## Code

* Inline-Code: einzelne Backticks.
* Umzäunte Blöcke: Triple Backticks, mit einer optionalen Syntaxsprache
Markierung (` ```python `, ` ```javascript ` usw.).

## Hinweis/Warnblöcke

Benutzerdefinierte Blockquote-Syntax, ein Typ pro Block, leere Blockquote-Zeile zwischen
Tag und Haupttext:

```markdown
>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard TIP.

>[!IMPORTANT]
>
>This is an IMPORTANT note.
```

Unterstützte Typen: `NOTE`, `TIP`, `IMPORTANT`, `CAUTION`, `WARNING`
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## Video-Einbettungen

Experience League unterstützt keine direkten MP4- oder YouTube-Videoeinbettungen in `[!VIDEO]`-Blöcke. Wenn Sie eine animierte Vorschau benötigen, verwenden Sie stattdessen eine GIF im gleichrangigen Ordner &quot;`.resources`&quot; der Seite und zentrieren Sie sie bei Bedarf mit der Inline-HTML.

```markdown
<div data-preserve-html="true" align="center">
  <img src="my-page.resources/my-preview.gif" alt="My preview" />
</div>
```

Verwenden Sie `[!VIDEO]` nicht für lokale MP4-Dateien, Remote-MP4-Dateien oder YouTube-URLs - die Veröffentlichungspipeline weist sie zurück, und CI schlägt fehl.

## UICONTROL-Tag

Eingliedert Namen von Benutzeroberflächenelementen (Schaltflächenbeschriftungen, Menüelemente, Feldnamen) inline, sodass
die Lokalisierungspipeline weiß, dass sie nach einer Kamera bewogen Zeichenfolge sucht, und fällt
Zurück zur englischen Bezeichnung, wenn keine vorhanden ist:

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

Verwenden Sie sie für jede literale UI-Beschriftung, auf die im Anweisungstext (Menü
Elemente, Schaltflächennamen, Dialogtitel, Fensternamen).

## DNL-Tag (&quot;Nicht lokalisieren&quot;)

Eingliedert Produktnamen, Funktionsnamen von Drittanbietern oder Phrasen, die
niemals maschinell Kamera bewogen werden:

```markdown
Use [!DNL Adobe Analytics] to track metrics.
The [!DNL Target] implementation requires configuration.
```

Verwenden Sie es in diesem Repo für Produktnamen wie `[!DNL Substance 3D Designer]`,
`[!DNL Substance 3D Sampler]` usw. auf ersten/markanten Erwähnungen pro Seite,
mit vorhandenen Seiten konsistent ist.

## Inline-HTML

Raw-HTML ist zulässig (MD033 wird durch die `markdownlint_custom.json`-Version dieses Repos deaktiviert).
aus diesem Grund), sondern nur zuverlässig durch die
Pipeline, wenn Tags `data-preserve-html="true"` enthalten. Inline-HTML reservieren
für Fälle, in denen einfaches Markdown nicht ausgedrückt werden kann (Bilder/Listen in Tabellenzellen,
`<span id="...">` Anker), anstatt als allgemeinen Ersatz für Markdown.

## Titelblatt

Den genauen Block, der von AGENTS verwendet wird, finden Sie im Abschnitt &quot;Seitenvordergrund&quot; von AGENTS.md.
reguläre Inhaltsseiten in diesem Repo und `metadata.md` für die Repo-Ebene
geerbte Felder.
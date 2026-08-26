---
name: write-experience-league-markdown
description: ""
Source: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ec58342925d3e608b0180b67a1e20ffaeb1f306a
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 5%

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
explizit `<span id="anchor-id"></span>` unmittelbar vor dem Begriff —
Das im gesamten Repo verwendete Muster finden Sie unter `help/glossary/glossary.md`.
* `TOC.md`-Abschnittsanker verwenden `{#section-id}`-Syntax nach einer Überschrift/Liste.
Bezeichnung, z. B. `Getting started{#getting-started}`

## Bilder

* `![Alt text](path/to/image.png "Optional hover title")`.
* Optionale Parameter für die Größen-/Optimierungsabfrage werden unterstützt:
  `![Adobe logo](assets/logo.png?width=750&format=png&optimize=medium)`.
* **Alt-Text darf keine Unterstriche enthalten** - sie werden nicht korrekt gerendert;
Verwenden Sie stattdessen Bindestriche oder Leerzeichen.
* Seitenspezifische Bilder sind in `<page-name>.resources/` live; gemeinsame/App-Symbole
live in `help/assets/` (siehe CLAUDE.md).

## Tabellen

* Durch Pipe getrennt, mit Header-Separator-Zeile für einen Bindestrich:

  ```markdown
  | Header | Another header | Yet another header |
  |--- |--- |--- |
  | row 1 | column 2 | column 3 |
  | row 2 | row 2 column 2 | row 2 column 3 |
  ```

* Der Tabelle muss eine leere Zeile vorangehen, da sie sonst nicht als Tabelle gerendert wird.
* Tabellen können nicht sauber Inhalte mit mehreren Absätzen oder komplexen Blöcken in einem
Zelle - wenn dieses Repo Bilder/Listen in einer Tabellenzelle benötigt (z. B.
Vergleichstabellen in `overview.md`), wird auf die Inline-HTML zurückgegriffen
(`<div>`, `<b>`, `<ul>`/`<li>`) mit jeweils `data-preserve-html="true"`
-Tag hinzu, damit die Pipeline sie nicht entfernt. Diesem Muster folgen.
als die neue Inline-HTML zu erfinden, sofern nicht erforderlich.

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

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

## UICONTROL-Tag

Eingliedert Namen von Benutzeroberflächenelementen (Schaltflächenbeschriftungen, Menüelemente, Feldnamen) inline, sodass
die Lokalisierungspipeline weiß, dass sie nach einer übersetzten Zeichenfolge sucht, und fällt
Zurück zur englischen Bezeichnung, wenn keine vorhanden ist:

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

Verwenden Sie sie für jede literale UI-Beschriftung, auf die im Anweisungstext (Menü
Elemente, Schaltflächennamen, Dialogtitel, Fensternamen).

## DNL-Tag (&quot;Nicht lokalisieren&quot;)

Eingliedert Produktnamen, Funktionsnamen von Drittanbietern oder Phrasen, die
niemals maschinell übersetzt werden:

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

Den genauen Block, der von CLAUDE.md verwendet wird, finden Sie im Abschnitt &quot;Titelblatt&quot; von CLAUDE.md
reguläre Inhaltsseiten in diesem Repo und `metadata.md` für die Repo-Ebene
geerbte Felder.
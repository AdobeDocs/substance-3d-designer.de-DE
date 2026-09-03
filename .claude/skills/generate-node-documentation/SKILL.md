---
name: generate-node-documentation
description: ""
source-git-commit: 69f546a26d2e09127b1c79ef4003e235536289da
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 4%

---


# Generieren der Knotendokumentation

Jede Blattknoten-Referenzseite in diesem Repo folgt einer konsistenten Struktur. Dieses
Geschicklichkeit ist die Spezifikation für diese Struktur. Das kanonische, voll bearbeitete Beispiel ist
`.../node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` —
im Zweifelsfall öffnen und spiegeln.

Diese Kenntnis deckt nur die Knotenseite *Struktur* ab. Für Basis-Experience League-Markdown
(Hinweis-/Warnblöcke, relative-vs-absolute Links, UICONTROL/DNL, Bildabfrageparameter,
lint gotchas) folgen Sie den `write-experience-league-markdown`-Kenntnissen.

## Wo sich eine Knotenseite befindet (Ordner/Inhaltsverzeichniskonvention)

* Ein Ordner pro Knoten unter dem entsprechenden Kategorie-/Unterkategoriepfad, z. B.
  `.../node-library/<category>/<subcategory>/<node-name>/<node-name>.md`.
* Der Ordner wird als Kebab-case-Knotentitel benannt. Es enthält **eine** `.md` Datei.
identisch benannt.
* Alle eingebetteten Medien für die Seite (Symbol, Beispielbilder, GIF) befinden sich in einem **-gleichrangigen Element.
  `<node-name>.resources/`-Ordner &quot;**&quot; neben &quot;`.md`&quot; und werden mit einem
  relativer Pfad (z. B. `<node-name>.resources/<file>.png`). Knotenseiten nicht auf
  Der freigegebene Ordner &quot;`help/assets/`&quot; - dies ist ein veraltetes Muster, das allmählich ausläuft; neue und
  Die bearbeiteten Seiten verwenden einen eigenen `.resources`-Ordner.
* Jede Seite hat einen entsprechenden Eintrag in `help/guide/TOC.md`. Beim Hinzufügen oder Verschieben eines
&quot;`TOC.md`&quot; und das Ordnerlayout gemeinsam aktualisieren (siehe Ordner/Inhaltsverzeichnis von CLAUDE.md
Konvention).

## Titelblatt

Knotenseiten verwenden den **minimal**-Block - nur `title` und einen Breadcrumb-Stil
`description`. (Dies unterscheidet sich von dem 11-Feld-Legacy-Block CLAUDE.md-Dokumenten für
Seiten mit regulären Inhalten.)

```yaml
---
title: "Shape splatter v2"
description: "Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Generator > Pattern > Shape splatter v2"
---
```

## Körperstruktur

Von oben nach unten, alles unter dem Vordergrund zählt:

### &#x200B;1. H1-Titel

Eine einzelne `# <Node title>` - genau ein H1 pro Seite.

### &#x200B;2. Symbol-/Beschreibungstabelle

Eine HTML, eine Zeile, zwei Zellen. Linke Zelle (`33.33%`) enthält das Symbol und dann die
`In:` Breadcrumb; Die rechte Zelle (`100.00%`) enthält `## Description` und die Prosa.

```html
<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![<Node title> icon](<node-name>.resources/<node-name>.png "<Node title>")

<b>In:</b> <Category> &gt; <Subcategory>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

<Description prose.>

</td>
</tr>
</table>
```

Beschreibungszellenprosa-Konventionen:
* Separate Absätze mit `<br><br>` (leere Zeilen innerhalb der Zelle sind unzuverlässig).
* Der Inline-Schwerpunkt ist `<b>…</b>` / `<i>…</i>`.
* Lead-In-Seiten verwenden `<i>Note:</i>` / `<i>Tip:</i>` am Anfang des Satzes.
* Verwenden Sie `&gt;` für `>` in der Zeile `In:` (innerhalb der HTML). Übernehmen Sie die Kategorie /
Unterkategorienamen vom Knoten selbst; Du musst sie nicht erfinden.

### &#x200B;3. Optionale Beschriftungen

`>[!INFO]`, `>[!TIP]`, `>[!NOTE]` usw. gehen **nach** in die Symbol-/Beschreibungstabelle (nicht
in der Zelle). Syntax gemäß der `write-experience-league-markdown`-Qualifikation.

### &#x200B;4. Eingaben

Nur einbeziehen, wenn der Knoten über Eingabe-Nadeln verfügt. Setzen Sie der Überschrift einen Anker voran.

```markdown
<a name="inputs"></a>

## Inputs

|  |  |
|:---|:---|
| <b>Background height</b> <i>Grayscale</i> | The base height map in which shapes are scattered.<br><br>The contribution is controlled by the <b>Background input opacity</b> parameter. |
```

* Zwei Spalten, leere Kopfzeile, `|:---|:---|` Ausrichtung.
* Eine Zeile pro Eingabe: linke Zelle `<b>Name</b> <i>Type</i>`, rechte Zelle die Beschreibung.
* Die Typmarke wird kursiv HTML — `<i>Type</i>` — nicht Markdown `*Type*`.

### &#x200B;5. Ausgaben

Die gleiche Form wie &quot;Eingaben&quot; mit `<a name="outputs"></a>` + `## Outputs`. Nur einbeziehen, wenn das
Knoten dokumentiert verschiedene Ausgaben (viele Knoten haben eine einzelne implizite Ausgabe und lassen diese
Abschnitt - erfinden Sie keinen).

Bei gepackten Mehrkanalausgaben brechen Sie die Kanäle mit `<br>` und Einzug auf.
Unterpunkte mit `&nbsp;` (siehe die Zeilen &quot;Splatter UVW&quot; / &quot;Splatter-Daten&quot; im
Referenz):

```markdown
| <b>Splatter UVW</b> | <b>R</b> - U component of the shapes' UVs.<br><b>G</b> - V component of the shapes' UVs.<br><b>B</b> - The shapes' height. (W)<br><b>A</b> - Packed data:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- <i>Integer part:</i> The shapes' unique identifier. |
```

### &#x200B;6. Parameter

Dieselbe Tabellenform mit `<a name="parameters"></a>` + `## Parameters`. Alles auslassen.
-Abschnitt, wenn der Knoten keine Parameter hat (keine leere Tabelle oder &quot;Keine Parameter&quot; ausgeben).
-Zeile).

* **Gruppierte Parameter**: eine übergreifende Labelzeile mit einer leeren rechten Zelle vor dem
Zeilen der Gruppe:

  ```markdown
  | <b>Positioning</b> |  |
  | <b>Project Input</b> <i>UV Position, World Space Position</i> | Choose whether the projection position is set in 2D/UV or in 3D/World space. |
  ```

* **Enum / Multi-Option-Werte**: Listen Sie die Optionen in der Beschreibungszelle als
  `<br>`-getrennte Strichliste:

  ```markdown
  | <b>Position distribution mode</b> <i>Integer</i> | The method of distributing the shapes:<br><br>- <b>2D grid:</b> A simple uniform grid.<br>- <b>Poisson disc:</b> Randomly offsets grid cells to prevent overlaps.<br>- <b>Uniform:</b> An even distribution of a set number of shapes. |
  ```

### &#x200B;7. Beispiele

Nur bei Beispielbildern/GIF einschließen. Verwenden einer HTML-Galerietabelle Eins `<td>`
pro Bild mit einer optionalen Beschriftung; wird nach 3 Bildern in ein neues `<tr>`-Element umgebrochen. Medienpfade
in den Ordner &quot;`.resources`&quot; der Seite zeigen.

```html
## Examples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file>.gif" /><br><i>Caption</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file2>.jpg" /><br><i>Another caption</i>
        </td>
    </tr>
</table>
```

Nachfolgende Zellen in einer teilweise gefüllten letzten Zeile leer lassen (`<td …></td>`), anstatt
umfließen. Lassen Sie Beschriftungen aus, wenn die Quelle keine enthält.

## Kanonische Typwerte

Verwenden Sie die Typenbezeichnung des Knotens erneut. typische Werte: `Grayscale`, `Color`, `Integer`
`Float`, `Float2`, `Float3`, `Float4`, `Integer2`, `Boolean`, `Grayscale Input`,
`Color Input`, `(Color value)`, `(Grayscale value)`. Erfinden oder &quot;normalisieren&quot; Sie keinen Typ
der Knoten nicht verwendet wird.

## Tabellenzellenregeln

* Keine unformatierten Zeilenumbrüche in einer Tabellenzelle - Verbinden Sie Zeilen mit `<br>` (und `<br><br>` zwischen
Absätze).
* Die Hervorhebung in Zellen ist `<b>`/`<i>` und die Typmarke ist immer `<i>Type</i>`.
* Verschachtelte Unterpunkte mit `&nbsp;` Sequenzen einrücken.

## Regeln/Don&#39;ts

* **keine** Eingaben, Ausgaben oder Parameter anfertigen, die der Knoten nicht hat; weglassen
-Abschnitt stattdessen. Versucht, vorhandene technische Inhalte nicht umzuformulieren, zusammenzufassen oder zu löschen - nur
formatieren.
* **Relative Links** zu anderen `.md` Seiten beibehalten; Externe Links absolut.
* **Löschen Sie die alte Seite**, wenn Sie eine alte Seite in dieses Format bearbeiten: Schwierigkeitsgrad
(`**Simple**` / `**Intermediate**` / `**Complex**`), die redundante `## <Title>`
Unterüberschrift in der Symbolzelle, Stub-Sätze wie &quot;Es sind keine Bilder angehängt
dieser Seite.&quot; sowie alle verbleibenden leeren Navigations-/Wrapper-Tabellen aus früheren Migrationen.
* **Ein H1** pro Seite; -Abschnitte verwenden `##`, und die Eingabe-/Ausgabe-/Parameter-Anker
(`inputs` / `outputs` / `parameters`) muss den Überschriften vorausgehen, damit sie die Seite überschreiten.
  `#inputs` Links werden aufgelöst.
* **`TOC.md` synchron halten** beim Hinzufügen, Umbenennen oder Verschieben einer Seite.

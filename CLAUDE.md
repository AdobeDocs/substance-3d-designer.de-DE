---
source-git-commit: e44437dcecf30714ffe5274c91135d84a0360aa7
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---
# CLAUDE.md

Diese Datei bietet Anweisungen für Claude Code (claude.ai/code) beim Arbeiten mit Code in diesem Repository.

# Substance 3D Designer - Dokumentation

Dieses Repository enthält die Dokumentation für Substance 3D Designer. Es ist kein Anwendungscode, kein Buildschritt oder keine Testsuite vorhanden - das Repository *ist* der Inhalt, der in Markdown geschrieben und auf [Adobe Experience League](https://experienceleague.adobe.com/docs/substance3d-designer.html?lang=en) veröffentlicht wurde.

# Repository-Struktur

* `help/` — der gesamte Dokumentationsinhalt, der so organisiert ist, dass er das Inhaltsverzeichnis spiegelt.
* `help/guide/TOC.md` - das Inhaltsverzeichnis. Jeder Eintrag ist ein relativer Link (der auf `/help/...` verwurzelt ist) zur Markdown-Datei einer Seite. `TOC.md` enthält auch Seitenstruktur-Metadaten (`user-guide-title`, `breadcrumb-title`, `nudge`, Abschnittsanker wie `{#section-id}`).
* `help/assets/` - Legacy-Ordner für freigegebene Bilder. Seitenspezifische Medien befinden sich jetzt in einem gleichrangigen Ordner für jede Seite `<md-file-name>.resources/` (siehe Ordner-/Inhaltsverzeichniskonvention unten). Nur eine Handvoll übriger Bilder, die von keiner Seite referenziert werden, sind noch hier zu finden. Legen Sie neue Bilder im Ordner &quot;`.resources`&quot; der Seite &quot;Verwenden&quot; ab, nicht hier.
* `help/glossary/glossary.md` - eine einzelne große Glossarseite, alphabetisch geordnet mit Ankerbereichen (`<span id="term"></span>`), die für die Vernetzung über `#term` Fragmente verwendet werden.
* `metadata.md` - Titelblatt auf Repo-Ebene (Cloud/Lösung/Produkt-IDs, `git-repo` usw.) die von jedem `TOC.md` geerbt wird. Nur für repo-weite Metadatenänderungen bearbeiten; seitenspezifische Metadaten gehören zum eigenen Titelblatt der Seite.
* `redirects.csv`, `linkcheckexclude.json`, `markdownlint_custom.json`, `pipeline.opts` — Konfiguration der Publishing-Pipeline (Umleitungen, Ausnahmen bei der Linkprüfung, Überschreibungen der Lint-Regel, Pipelineoptionen).
* `fix-image-names.py` - Einmaliges Dienstprogramm, das `help/assets` Bilder mit in Klammern gesetzten Suffixen umbenennt (z. B. `foo(1).png` → `foo_1.png`) und schreibt jeden Markdown-Verweis entsprechend neu. Nicht Teil eines regulären Workflows; nur dann manuell ausgeführt werden, wenn diese Dateinamen wieder angezeigt werden.

## Ordner-/Inhaltsverzeichniskonvention

Für jeden Eintrag in `help/guide/TOC.md`:
* Unter &quot;`help/`&quot; befindet sich ein entsprechender Ordner, der auf dieselbe Verschachtelung wie das Inhaltsverzeichnis folgt.
* Dieser Ordner enthält eine Markdown-Datei, die als Groß-/Kleinschreibung für den Seitentitel bezeichnet wird.
* Wenn die Seite über individuelle Medien (Bilder, GIF, Videos) verfügt, befindet sie sich in einem gleichgeordneten Unterordner mit dem Namen `<md-file-name>.resources`.

Wenn Sie eine Seite hinzufügen oder verschieben, aktualisieren Sie `TOC.md` und das Ordnerlayout gemeinsam - sie müssen synchron bleiben.

## Knotenreferenzseiten

Die Knotenbibliotheksbäume (z. B. `help/compositing-graphs/nodes-reference-for-com/node-library/<category>/<node>/<node>.md`) sind ein eigenständiger Seitentyp mit einem eigenen, konsistenten Layout: eine Symbol-/Beschreibungstabelle, gefolgt von verankerten `## Inputs` / `## Outputs` / `## Parameters` HTML (`#inputs`/`#outputs`/`#parameters`) und einer `## Examples`-Galerie. Sie verwenden das **minimal**-Titelblatt (nur `title` + `description`), nicht den unten stehenden regulären Inhaltsseitenblock, der `.../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` nachempfunden ist. Eingebettete Medien (Symbol, Beispielbilder/GIF) befinden sich in einem gleichrangigen Ordner &quot;`<node-name>.resources/`&quot; neben der Seite, auf den relativ verwiesen wird. Verwenden Sie die `generate-node-documentation`-Kenntnisse (sofern vorhanden) für die vollständige Authoring-Vorlage.

## Titelblatt der Seite

Normale Inhaltsseiten verwenden einen Titelblatt-Block wie:

```yaml
---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/<section>/<page>.html"
breadcrumb-title: ""
description: <one/two sentence SEO description>
helpx_creative_field: ""
helpx_description: Designer > <Section> > <Page>
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: <Page title>
user-guide-description: ""
user-guide-title: ""
---
```

`description` ist präzise und prägnant - wird für SEO-/Such-Snippets verwendet.

# Regeln für Content-Authoring

* Englisch ist die Quelle der Wahrheit; alle anderen Sprachen sind davon Kamera bewogen.
* Alle Links zu anderen Dokumentationsseiten müssen **relative** Links sein. Alle Verknüpfungen zu externen Ressourcen müssen **absolute** Verknüpfungen sein.
* Der Inhalt ist in Markdown mit GitHub-Geschmack mit benutzerdefinierten Erweiterungen/Gotchas von Experience League geschrieben und [hier](https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown) dokumentiert. Verwenden Sie die `write-experience-league-markdown`-Kenntnisse (sofern vorhanden) für die Details.
* Jede übermittelte Änderung durchläuft automatisierte Lint-Prüfungen und Link-Validierung in CI (siehe unten). Überprüfen Sie `markdownlint_custom.json` und `linkcheckexclude.json`, bevor Sie davon ausgehen, dass eine Regel gilt oder ein Link repariert werden muss.

# Validierung/CI

* `.github/workflows/validate-articles.yml` wird auf PRs ausgeführt und an `main` gesendet (und über einen `retest` PR-Kommentar). Der freigegebene `Adobe-Enterprise-Docs/workflows` wiederverwendbare Workflow wird aufgerufen, um Markdown zu linten und Links zu validieren. In diesem Repo gibt es kein lokales entsprechendes Skript — CI ist die Quelle der Wahrheit für &quot;pass/fail&quot;.
* `.github/workflows/mirror.yml` spiegelt `main` auf Push in den öffentlichen Repo. Es ist Infrastruktur, nicht etwas, das Content-Änderungen berühren müssen.
* `markdownlint_custom.json` erweitert den freigegebenen `markdownlint.json`-Regelsatz und deaktiviert mehrere Regeln (MD005, MD007, MD018, MD032, MD033, MD034, MD037, MD040), die mit den benutzerdefinierten Markdown-Erweiterungen von Experience League in Konflikt stehen (z. B. Inline-HTML, nicht standardmäßige Hervorhebung). Beheben Sie keine Inhalte, um diese deaktivierten Regeln zu erfüllen.
* `linkcheckexclude.json` Whitelists für Linkmuster (derzeit `example.com`/`example-end.com`), die von der Linkprüfung übersprungen werden sollten.

# Arbeitskonventionen

* Dies ist eine Dokumentation mit vielen Versionshinweisen — Versionshinweise befinden sich unter `help/release-notes/`, einem Ordner pro Version (z. B. `version-16-0`) plus `all-changes` und `old-versions` Aggregationsseiten. Befolgen Sie beim Hinzufügen einer neuen Version den vorhandenen Versionsordner als Vorlage.

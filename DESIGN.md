---
name: h,x-Trainer Pro
description: Interaktives Mollier-h,x-Diagramm für feuchte Luft, gezeichnet als Konstruktion auf Millimeterpapier.
colors:
  paper: "#fcfdfb"
  paper-tint: "#f3f8f5"
  rule: "#d9e7df"
  rule-strong: "#b7d3c4"
  grid-1: "#dcece4"
  grid-5: "#a9d2bd"
  grid-10: "#6fb495"
  print-ink: "#1f6b4f"
  graphite: "#202226"
  graphite-2: "#55595f"
  graphite-3: "#6b7077"
  red: "#d92d20"
  blue: "#1d6fd1"
  violet: "#8e3bd6"
  ochre: "#c7771a"
  ochre-ink: "#8a5310"
  ice: "#8fb8e6"
typography:
  title:
    fontFamily: "Barlow, ui-sans-serif, system-ui, sans-serif"
    fontSize: "26px"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "Barlow, ui-sans-serif, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 600
  value:
    fontFamily: "Barlow, ui-sans-serif, system-ui, sans-serif"
    fontSize: "22px"
    fontWeight: 600
    lineHeight: 1
    fontFeature: "\"tnum\" 1, \"lnum\" 1"
  body:
    fontFamily: "Barlow, ui-sans-serif, system-ui, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.25
    fontFeature: "\"tnum\" 1, \"lnum\" 1"
  label:
    fontFamily: "Barlow, ui-sans-serif, system-ui, sans-serif"
    fontSize: "13px"
    fontWeight: 400
  chart-label:
    fontFamily: "Barlow Semi Condensed, Barlow, sans-serif"
    fontSize: "12px"
    fontWeight: 600
    fontFeature: "\"tnum\" 1"
rounded:
  none: "0px"
  sm: "2px"
  thumb: "4px"
spacing:
  row-y: "12px"
  gutter-mobile: "16px"
  gutter-tablet: "24px"
  section-gap: "32px"
  touch-min: "48px"
components:
  protocol-row:
    textColor: "{colors.graphite}"
    typography: "{typography.body}"
    padding: "12px 4px"
  protocol-row-hover:
    backgroundColor: "{colors.paper-tint}"
  layer-toggle:
    textColor: "{colors.graphite}"
    typography: "{typography.body}"
    rounded: "{rounded.sm}"
    height: "48px"
    padding: "0 4px"
  number-field:
    textColor: "{colors.graphite}"
    typography: "{typography.value}"
    rounded: "{rounded.none}"
    width: "5.2ch"
  select-underline:
    textColor: "{colors.graphite}"
    rounded: "{rounded.none}"
    padding: "6px 28px 6px 0"
  ruler-thumb:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.red}"
    rounded: "{rounded.thumb}"
    width: "22px"
    height: "34px"
---

# Design System: h,x-Trainer Pro

## Overview

**Creative North Star: "Das gezeichnete Protokollblatt"**

Die Oberfläche ist ein Blatt, kein Dashboard. Weißes Papier trägt ein grün gedrucktes Raster in drei Stärken (1 / 5 / 10), Graphit zeichnet Achsen, Kurven und Text, und jede Ablesung erscheint als Buntstiftstrich in einer fest vergebenen Farbe. Daneben (Desktop) bzw. darunter (Hochformat) liegt ein liniertes Protokoll mit festen Spalten: Markierung, Größe mit Formelzeichen, Wert, Einheit.

Die Dichte ist die eines technischen Formblatts: viele Werte, wenig Dekor, keine Flächen, die nicht etwas bedeuten. Hierarchie entsteht durch Linienstärke, Graphitstufen und Ziffern in tabellarischer Schrift, nicht durch Kästen, Karten oder Schatten. Die Farbe einer Größe ist im Diagramm, in der Protokollzeile und in der Legende dieselbe; so lässt sich jede Zahl ihrer Konstruktion zuordnen.

Bewegung gibt es genau einmal im System: Beim Loslassen des Zustandspunkts zeichnen sich die Konstruktionslinien wie Bleistiftstriche nach.

**Key Characteristics:**
- Papierweiß mit grünem Druckraster, Graphit für alles Gezeichnete.
- Feste Buntstift-Rollen: Rot = Zustand, Blau = Taupunkt, Violett = Feuchtkugel, Ocker = Enthalpie, Druckgrün = Randmaßstab.
- Liniierte Protokollzeilen statt Karten; Trennung nur durch Haarlinien.
- Tabellarische, lining Ziffern überall; Formelzeichen kursiv.
- Flach; Tiefe nur am Regler-Daumen, der physisch gegriffen wird.

## Colors

Ein neutrales Papier-und-Graphit-System mit einem grünen Vordruck und fünf semantisch fest gebundenen Stiftfarben.

### Primary
- **Zustandsrot** (red): Die einzige Signalfarbe. Zustandspunkt, seine Hilfslinien zu den Achsen, Achsmarken für t und x, Regler-Daumen, Fokusstrich des Zahlenfelds, Text-Caret, Auswahlfarbe (16 % Deckung).

### Secondary
- **Taupunktblau** (blue): Taupunkt-/Reifpunkt-Konstruktion (senkrecht, x = const), ihr Achswert und ihr Protokollwert.
- **Feuchtkugelviolett** (violet): Feuchtkugel-Konstruktion (entlang h = const), Achswert und Protokollwert.

### Tertiary
- **Isenthalpen-Ocker** (ochre): Nur als Linie: Isenthalpen im Diagramm (Hauptlinien 62 %, Zwischenlinien 30 % Deckung), Legendenstrich.
- **Ocker-Tinte** (ochre-ink): Die lesbare Textfassung von Ocker: Isenthalpen-Beschriftung, Achstitel „Enthalpie h“, Enthalpiewert im Protokoll.
- **Druckgrün-Tinte** (print-ink): Randmaßstab Δh/Δx (Striche, Pol, Beschriftung) und dessen Legende.
- **Eisblau** (ice): Nur für die gestrichelten Nebelisothermen unter 0 °C.

### Neutral
- **Papier** (paper): Seiten- und Diagrammgrund, Halo hinter Diagrammtext, Konturring um Punkte.
- **Papier getönt** (paper-tint): Hover-Fläche der Protokoll- und Ebenenzeilen; sonst nirgends.
- **Linie** (rule): Haarlinien zwischen Protokollzeilen, Spaltentrenner der mobilen Ablesezeile, Fußzeile.
- **Linie kräftig** (rule-strong): Strukturkanten (Kopfzeile unten, Diagrammblatt-Kante), Hover-Unterstrich des Zahlenfelds, Scrollbar.
- **Raster 1 / 5 / 10** (grid-1, grid-5, grid-10): Die Millimeterpapier-Hierarchie für Wassergehalt-Senkrechte und Isothermen; grid-5 auch für Nebelisothermen über 0 °C, grid-10 als Legendenstrich.
- **Graphit** (graphite): Text, Achsen, Rahmen, φ = 100 %-Kurve, Checkbox, Select-Unterstrich, Fokusring.
- **Graphit 2** (graphite-2): Sekundärtext (Größenname, Einheit, Untertitel), φ-Kurven 10–90 %.
- **Graphit 3** (graphite-3): Tertiärtext (Konstruktionshinweise, Fußzeile, „Nebelgebiet“), Lineal-Nebenstriche, ausgeschaltete Konstruktionsmarker.

### Named Rules
**The Eine-Größe-eine-Farbe Rule.** Eine Stiftfarbe gehört genau einer physikalischen Größe und erscheint für diese Größe überall gleich: Linie im Diagramm, Achswert, Protokollwert, Legendenstrich. Eine neue Größe bekommt eine neue Farbe oder Graphit, nie eine bereits vergebene.

**The Rot-ist-der-Zustand Rule.** Rot markiert ausschließlich den gesetzten Zustand und die Eingabe dafür. Keine Warnungen, Buttons oder Hervorhebungen in Rot.

**The Linie-und-Tinte Rule.** Ocker ist eine Linienfarbe; Text in Ocker wird immer in ochre-ink gesetzt. Grüne Druckfarbe folgt demselben Paar (grid-Töne für Linien, print-ink für Schrift).

## Typography

**Body Font:** Barlow (mit ui-sans-serif, system-ui, sans-serif)
**Label/Chart Font:** Barlow Semi Condensed (mit Barlow, sans-serif)

**Character:** Eine nüchterne, normschriftnahe Grotesk für Protokoll und Bedienung; die schmalere Semi Condensed für alles, was im Diagramm und auf der Linealskala steht. Beide durchgehend mit tabellarischen, linienbündigen Ziffern (`tnum`, `lnum`).

### Hierarchy
- **Title** (700, 22px mobil / 26px ab lg, line-height 1, −0.01em): Nur der Produktname in der Kopfzeile.
- **Headline** (600, 17px): Abschnittsköpfe des Protokolls (Zustand, Ablesung, Ebenen).
- **Value** (600, 22px, line-height 1, tabellarisch): Die abgelesenen Zahlen in der rechten Wertspalte. In der mobilen Ablesezeile dieselbe Rolle in 16px.
- **Body** (400, 15px, leading-tight): Größennamen, Einheiten, Ebenen-Beschriftungen, Select (15px mobil / 16px ab lg, 600).
- **Label** (400, 13px; 12.5px für Hinweise und Fußzeile; 12px für das Feldlabel „Klimazone“; 11px Linealskala): Sekundärtext in graphite-2 bzw. graphite-3.
- **Chart Label** (Semi Condensed 600, 12px Achsen / 12.5px Achstitel / 10.5px Kurven- und Isenthalpenwerte / 11.5–13px 700 für Ablesemarken, alle mit Faktor fs auf schmalen Bildschirmen vergrößert): Diagrammbeschriftung, stets mit Papier-Halo (Stroke 3.5px × fs, paint-order stroke).

### Named Rules
**The Formelzeichen Rule.** Physikalische Größen (t, φ, x, h, p) stehen kursiv, Einheiten und Ziffern aufrecht, Indizes als echte Tiefstellung (t_τ, t_F). Dezimalkomma, echtes Minuszeichen (−).

**The Feste-Ziffern Rule.** Jede Zahl in der Oberfläche läuft tabellarisch, damit Werte beim Ziehen nicht springen und in der Wertspalte rechtsbündig fluchten.

## Layout

Hochformat (unter lg): schmale Kopfzeile (Titel links, Klimazone rechts, 46 % Breite, max. 300px), darunter das Diagrammblatt randlos in voller Breite und `sticky` am oberen Rand, begrenzt auf eine Breite von 56vh × 8/7, damit darunter Platz bleibt. Direkt unter dem Diagramm eine sechsspaltige Ablesezeile (t | φ | x | h | t_τ | t_F) mit Haarlinien-Trennern. Darunter das Protokoll, max. 2xl breit, zentriert.

Desktop (ab lg): Zweispaltiges Raster, Diagramm links (flexibel, Höhe an den Viewport gebunden: (100vh − 9rem) × 800/700), Protokoll als Journal-Spalte rechts (380px, ab xl 420px), getrennt durch eine rule-strong-Kante. Die mobile Ablesezeile entfällt.

Rhythmus: Seitenränder 16 / 24 / 28–32px (mobil / sm / lg); Abschnittsabstand 32px; Protokollzeilen 12px vertikal; interaktive Zeilen mindestens 48px hoch. Das Protokoll ist ein vierspaltiges Raster (Markierung 24px | Name | Wert rechtsbündig | Einheit), dessen Spalten über Subgrid in allen Zeilen fluchten.

## Elevation & Depth

Das System ist flach. Ebenen werden durch Haarlinien und Strichstärke getrennt, nicht durch Schatten oder Flächen. Die einzige Ausnahme ist der Regler-Daumen: Er ist das eine Objekt, das man greift, und trägt deshalb einen weichen Schatten. Im Diagramm ersetzt der Papier-Halo hinter Beschriftungen jede Hinterlegung.

### Shadow Vocabulary
- **Daumen** (`box-shadow: 0 2px 6px rgb(32 34 38 / 0.18)`): Ruhezustand des Lineal-Daumens.
- **Daumen-Fokus** (`box-shadow: 0 0 0 3px rgb(217 45 32 / 0.25), 0 2px 6px rgb(32 34 38 / 0.18)`): Tastaturfokus auf dem Regler.

### Named Rules
**The Blatt-bleibt-flach Rule.** Keine Karten, keine Schatten auf Flächen. Getrennt wird mit Linie (rule) oder Kante (rule-strong).

## Shapes

Rechtwinklig wie ein Formblatt. Felder und Select haben keine Ecken und keinen Rahmen, nur einen Unterstrich. Zeilen-Buttons tragen einen kaum sichtbaren Radius (2px), der nur beim Hover-Grund auffällt; Checkboxen 2px; der Regler-Daumen 4px. Runde Formen sind den Messpunkten im Diagramm vorbehalten (Zustandspunkt r 6.5, Taupunkt/Feuchtkugel r 4.5, jeweils mit Papier-Konturring), dazu kleine gefüllte Dreiecke als Achsmarken. Konstruktionsstriche haben runde Enden.

## Components

### Lineal-Regler (Signatur)
Ein Maßstab statt eines Schiebereglers.
- **Skala:** Graphit-Grundlinie, Nebenstriche 6px (graphite-3, 55 %), Mittelstriche 10px, Hauptstriche 14px in Graphit mit Semi-Condensed-Beschriftung 11px darunter. Höhe 46px.
- **Daumen:** 22 × 34px, 4px Radius, Papier mit 90 % Deckung, 1.5px roter Rahmen und roter 2px-Ablesestrich in der Mitte; Schatten siehe Elevation.
- **Fokus:** zusätzlicher roter 3px-Ring (25 %).

### Zahlenfeld
- **Style:** Transparent, rahmenlos, rechtsbündig, 5.2ch breit, erbt die Value-Typografie; unsichtbarer 1.5px-Strichel-Unterstrich.
- **Hover:** Unterstrich gestrichelt in rule-strong. **Fokus:** Unterstrich durchgezogen rot. Übergang 160ms ease-out.
- Eingabe mit Dezimalkomma; übernommen bei Enter oder Verlassen, Escape verwirft.

### Select (Klimazone)
- **Style:** Rahmenlos, 1.5px Graphit-Unterstrich, 600, Chevron als Graphit-SVG rechts. Kleines Label darüber (12px, graphite-2).
- **Fokus:** Unterstrich wird rot.

### Protokollzeile
- **Aufbau:** Markierung | Name mit kursivem Formelzeichen | Wert (Value) | Einheit, getrennt durch rule-Haarlinien oben.
- **Markierung:** Linienmuster 22 × 12px in der Farbe der Größe (durchgezogen, gestrichelt, mit Punkt), exakt wie die Linie im Diagramm.
- **Umschaltbar (Taupunkt, Feuchtkugel):** Die ganze Zeile ist ein Button (aria-pressed). An: Wert und Marker in Stiftfarbe, Hinweis „Konstruktion sichtbar: …“. Aus: Marker graphite-3, Wert Graphit, Hinweis „Konstruktion ausgeblendet“. Hover paper-tint.

### Ebenen-Schalter
- **Aufbau:** Zeile mit mindestens 48px Höhe: gezeichnete Checkbox (18px, 2px Radius, Graphit gefüllt mit Papier-Haken bzw. nur Kontur) | Beschriftung 15px | Status „sichtbar“/„aus“ 13px | Linienmuster der Ebene.
- **Hover:** paper-tint.

### Mobile Ablesezeile
Sechs gleich breite Spalten unter dem Diagramm: kursives Formelzeichen 13px, Wert 16px 600 in der Farbe der Größe (t, φ, x in Graphit), Einheit 11px; Haarlinien zwischen den Spalten.

### Diagrammblatt
- Raster in grid-1/5/10 (0.8px bzw. 1px, non-scaling), φ-Kurven gestrichelt `5 3` in graphite-2 (70 %), φ = 100 % durchgezogen 2.4px Graphit, Rahmen 1.4px Graphit.
- Konstruktionsstriche 2.6px × fs mit runden Enden; Hilfslinien zu den Achsen 1px gepunktet `2 3`.
- **Bewegung:** Nach dem Loslassen zeichnen sich die Konstruktionsstriche in 560ms `cubic-bezier(.16, 1, .3, 1)` nach (Feuchtkugel 120ms versetzt), Endpunkte und Achsmarken blenden 380ms nach 360ms ein. Während des Ziehens keine Animation; bei `prefers-reduced-motion` sofort vollständig.

## Do's and Don'ts

### Do:
- **Do** jede neue Ablesung als Konstruktion im Diagramm zeichnen und im Protokoll in derselben Stiftfarbe wiederholen.
- **Do** Werte mit Dezimalkomma, tabellarischen Ziffern und kursivem Formelzeichen setzen (z. B. „t_τ 12,9 °C“).
- **Do** Beschriftungen im Diagramm mit Papier-Halo schreiben statt sie zu hinterlegen.
- **Do** interaktive Zeilen mindestens 48px hoch halten; der Hover ist paper-tint, nicht mehr.
- **Do** Eingaben als unterstrichene Felder bauen: Hover rule-strong, Fokus rot.

### Don't:
- **Don't** weiße Karten, Seitenleisten-Panels oder Pillen-Schalter einführen; Gliederung geschieht mit Haarlinien auf dem Blatt.
- **Don't** Rot für etwas anderes als den Zustandspunkt und seine Eingabe verwenden.
- **Don't** eine Stiftfarbe für eine zweite Größe wiederverwenden oder Ocker als Textfarbe setzen (dafür ochre-ink).
- **Don't** Schatten auf Flächen legen; der Regler-Daumen ist die einzige gegriffene, schattierte Form.
- **Don't** Emoji oder Glyphen-Icons als Bedeutungsträger einsetzen; Legenden sind gezeichnete Linienmuster.

# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users
Studierende einer Hochschul-Vorlesung Lüftungstechnik. Sie nutzen die App hauptsächlich auf **Tablet und Smartphone** (bestätigt), um das h,x-Diagramm (Mollier) für feuchte Luft zu verstehen und Kennwerte abzulesen. Der Dozent (Markus) stellt die App bereit und nutzt sie in der Lehre.

## Product Purpose
Interaktives h,x-Diagramm zum Lernen: Zustandspunkt über Temperatur/relative Feuchte, per Klick oder Ziehen im Diagramm setzen und Taupunkt/Reifpunkt, Feuchtkugeltemperatur, Wassergehalt x und Enthalpie h grafisch nachvollziehen. Erfolg heißt: Die Studierenden verstehen die Konstruktion im Diagramm, nicht nur die Zahl.

## Positioning
Die Werte werden exakt so berechnet, wie man sie im Diagramm konstruiert (Taupunkt als Umkehr der Sättigungskurve, Feuchtkugel über h = const). Rechnung und Grafik stimmen daher immer überein. Das Diagramm ist ein echtes schiefwinkliges Mollier-Diagramm mit Isenthalpen, Nebelgebiet, Eis unter 0 °C und Randmaßstab Δh/Δx.

## Operating Context
- Einsatz in Vorlesung und Übung sowie zum Selbststudium; Hauptgeräte Tablet und Smartphone (Touch).
- Öffentlich über GitHub Pages: https://markuspfeil4-glitch.github.io/hx-diagramm/
- Entwicklung vollständig über GitHub (Issues, Branches, Pull Requests).

## Capabilities and Constraints
- Eine einzige `index.html`, React 18 + Tailwind + Babel per CDN, keine Build-Kette.
- Physik (Magnus Wasser/Eis, p = 1013,25 hPa, h = 1,006·t + x·(2501 + 1,86·t)) ist geprüft und bleibt unverändert.
- Diagrammbereich −20 … 45 °C, x = 0 … 35 g/kg.
- Klimazonen-Auswahl: nur Sommer-Referenztage (Winter-Presets bewusst verworfen).
- Sprache: Deutsch, Dezimalkomma.
- Zurückgestellt: Zustandsänderungen, zweiter Zustandspunkt, variabler Luftdruck, Übungsmodus.

## Brand Commitments
- Name „h,x-Trainer Pro“ bleibt (bestätigt).
- Kein Hochschul-Corporate-Design vorgegeben.

## Evidence on Hand
Keine Nutzerzitate, Kennzahlen oder Logos. Nichts davon erfinden.

## Product Principles
1. Das Diagramm ist das Produkt; alles andere dient dem Ablesen.
2. Rechnung und Konstruktion müssen sichtbar übereinstimmen.
3. Fachlich korrekt vor dekorativ: Einheiten, Formelzeichen und Bezeichnungen wie im Lehrbuch.
4. Touch zuerst: Auf dem Smartphone muss man den Punkt bequem setzen und die Werte sehen können.

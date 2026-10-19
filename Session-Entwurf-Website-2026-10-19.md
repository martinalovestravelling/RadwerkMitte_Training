# Chat-Zusammenfassung – Erster Website-Entwurf (2026-10-19)

Protokoll dieser Session: Auftrag, Vorgehen, Ergebnis und offene Punkte.

## Auftrag

„Bau mir bitte einen ersten Entwurf für eine Webseite mit allen Informationen die du hast, frag mich gerne wenn du weitere Informationen benötigst.“

## Vorgehen

1. Grundlage waren [CLAUDE.md](CLAUDE.md) und [DESIGN.md](DESIGN.md) (PRD, Kurzfassung, Firmensteckbrief, Kundengespräch-Protokoll).
2. Beim Start eines Design-Artifacts zeigte sich, dass in der Organisation bereits ein **Design-System „Radwerk Mitte – Designvorgaben Website“** existiert (als Claude-Artifact geteilt). Dieses wurde gelesen und als Grundlage verwendet, statt Farben/Typografie neu zu erfinden.
3. Aus dem Design-System übernommen:
   - **Farben**: Radblau `#1f5fbf` (Hausfarbe), Koralle `#ff6b4a` (Akzent, nur als Fläche mit dunklem Text), Cyan `#5cc8ff` (nur in dunklen „Glow“-Flächen), Nachtblau `#0a1424` (Text/Footer).
   - **Typografie**: Plus Jakarta Sans (Fließtext/Überschriften), JetBrains Mono (Kennzahlen in Glow-Flächen).
   - **Konzept „JobRad-Muster, Radwerk-Ausprägung“**: Orientierung an der Struktur von jobrad.org (Zielgruppen-Weiche, Rechner, Schritte, Vertrauenszahlen), aber mit eigenen Farben/Inhalten, keine fremde Marke.
   - **Seitenaufbau** (11 Abschnitte, dokumentiert im Design-System unter „Seitenaufbau.md“) wurde 1:1 für die Startseite übernommen.
4. Daraus wurde ein interaktiver Startseiten-Entwurf als Claude-Artifact gebaut (Design-Canvas-Format).

## Ergebnis

**Artifact:** [Radwerk Mitte – Website Entwurf](https://claude.ai/artifact/HaGjnC56Gtv4CoJqkBzKnB)

Enthaltene Abschnitte der Startseite:

- Sticky Header: Logo, Navigation (Für Arbeitgeber / Für Beschäftigte / Werkstatt / E-Bikes & Shop), Telefonnummer, CTA „Angebot anfragen“.
- Hero mit Zielgruppen-Schalter (Arbeitgeber / Beschäftigte / Privatkunden) – Arbeitgeber vorausgewählt, damit B2B-Leasing mit einem Klick erreichbar ist.
- Vertrauensleiste: „seit 1989“, 2 Filialen, fiktive Referenzkunden.
- **Leasing-Rechner**: Eingabe Radpreis + Bruttogehalt, live berechnete Monatsrate in einer Glow-Fläche, klar als unverbindliche Beispielrechnung mit Platzhalter-Formel gekennzeichnet.
- „So funktioniert's“ in 4 Schritten.
- 3 Zielgruppen-Kacheln (Arbeitgeber, Beschäftigte, Werkstatt).
- B2B-Referenzzitat (fiktiver Kunde).
- Werkstatt-Bereich: Terminablauf in 3 Schritten + interaktive Status-Abfrage.
- FAQ-Akkordeon mit 6 Fragen.
- Anfrageformular mit Pflicht-Kategorie (B2B-Angebot, Werkstatt, Bestellung, Sonstiges); bei B2B erscheinen zusätzliche Felder (Firmengröße, Bedarf).
- Footer mit beiden Standorten (Kassel, Göttingen), Öffnungszeiten, Telefon, Hinweis auf datenschutzkonforme Reichweitenmessung.

Barrierefreiheit: Skip-Link, sichtbare Fokusringe, Tastaturbedienbarkeit, Kontrastwerte aus dem Design-System, keine reinen Farbsignale, `prefers-reduced-motion` berücksichtigt.

## Offene Punkte / bewusst markiert statt erfunden

1. **Werkstatt-Terminbuchung & Status-Abfrage** stammen nur aus der Kurzfassung, nicht aus dem ausführlichen PRD (siehe CLAUDE.md „Abweichung Kurzfassung ↔ PRD“). Im Entwurf mit Badge „Konzept – Umfang laut Kurzfassung, mit Radwerk abzustimmen“ markiert. **Klärung nötig**, welche PRD-Version für den Build gilt.
2. **Leasing-Konditionen/Berechnungsformel**: laut PRD noch offen, liefert Radwerk. Der Rechner nutzt eine klar sichtbare Platzhalter-Pauschale, keine echten Werte.
3. **Link zum externen Onlineshop**: Platzhalter, da keine echte URL vorliegt.
4. **Logo**: Design-System enthält noch keine Logo-Datei; aktuell nur Schriftzug „radwerk mitte“.
5. Bisher nur die **Startseite** umgesetzt; Unterseiten (B2B-Detail, Werkstatt, Privatkunden, Impressum/Datenschutz) fehlen noch.
6. Exakte Markenfarben/Logo-Dateien sind im Design-System zwar schon als Arbeitswerte gesetzt, aber laut DESIGN.md noch nicht final mit Radwerk abgestimmt.

Diese Punkte decken sich mit den bereits in [TECHSPEC.md](TECHSPEC.md) unter „Offene Entscheidungen“ festgehaltenen Fragen.

## Nächste Schritte (Vorschlag)

- Rückmeldung zum Entwurf einholen (Layout, Tonalität, Umfang Kurzfassung vs. PRD).
- Bei Bedarf weitere Unterseiten entwerfen.
- Offene Punkte aus TECHSPEC.md mit Radwerk/Projektteam klären, sobald möglich.

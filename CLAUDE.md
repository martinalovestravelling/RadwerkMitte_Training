# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Projektstand

Noch kein Code, kein Build, keine Tests. Der Ordner enthält nur die Projektunterlagen (PDFs). Der Tech-Stack ist **bewusst noch offen**: Die bestehende WordPress-Seite wird erst per Fragebogen analysiert, WordPress ist nicht gesetzt. Sobald ein Stack gewählt ist, Build-/Test-Befehle hier ergänzen.

Kontext: Übungsprojekt im Kurs „Vibe Engineering“ (BTA). Radwerk Mitte GmbH ist eine **fiktive** Firma, alle Personen und Zahlen sind erfunden.

## Quelldokumente

- `PRD – Neue Website Radwerk Mitte.pdf` – ausführliches PRD (Stand 19.10.2026, @Martina). **Maßgebliche Quelle für Umfang und Akzeptanzkriterien.**
- `Radwerk_PRD_Kurzfassung.pdf` – einseitige Kurzfassung „Stufe 1“. Weicht vom ausführlichen PRD ab (siehe unten).
- `Firmensteckbrief-Radwerk-Mitte-BTA.pdf` – Firma, Personen, Haltung.
- `Übung_Kundengespräch_Protokoll.pdf` – Protokoll des Kundengesprächs mit Merle Vogelsang; Herkunft aller Ziele.

## Kunde in Kürze

Fahrradhändler mit Werkstatt, Standorte **Kassel und Göttingen**, ~120 Beschäftigte, ~28 Mio. € Umsatz, externer Onlineshop, Zentrallager. Wachstumsziel ~15 % im nächsten Jahr, vor allem über **Dienstrad-Leasing für Unternehmen (B2B)**. Budget zunächst ca. 150.000 €.

Ansprechpersonen: Merle Vogelsang (Geschäftsführung, gibt frei), Dilan Aydın (B2B-Vertrieb), Amara Osei (Kundenservice – einzige Person im Support), Svenja Kowalczyk (E-Commerce/Marketing, pflegt Inhalte), Heiner Vogelsang (Werkstatt).

## Umfang Version 1 (laut ausführlichem PRD)

Website mit B2B-Bereich, Leasing-Rechner, FAQ und Anfrageformular.

Akzeptanzkriterien:
- Dienstrad-Leasing für Unternehmen von der Startseite mit **einem Klick** erreichbar.
- Leasing-Rechner: Eingabe Radpreis + Bruttogehalt → monatliche Belastung, mit Hinweis „unverbindlich“. Konditionen liefert Radwerk (noch offen).
- Anfrageformular mit Pflicht-Kategorie (z. B. B2B-Angebot, Werkstatt, Bestellung, Sonstiges), leitet per Mail an die zuständige Person weiter; B2B-Anfragen mit Firmengröße und Bedarf.
- FAQ zu den häufigsten Standardfragen.
- Mindestens eine Referenz eines Geschäftskunden.
- Telefonnummer und beide Standorte auf **jeder** Seite.
- Funktionierender Link zum externen Onlineshop.
- Blau und Orange, modernes Design; voll smartphone-tauglich, barrierefrei.
- Absprungrate und Anzahl Anfragen ab Launch messbar (datenschutzkonform).
- Inhalte durch das Team ohne Programmierer pflegbar (CMS).

## Nicht-Ziele (nicht bauen)

Kein eigener Onlineshop (externer Shop wird nur verlinkt), kein Partnerportal/Kunden-Login (nur Schnittstellen vorbereiten), kein Konfigurator für Custom-Räder, kein Rebranding, keine neue Support-Software. Die Lösung muss ohne zusätzliche Stellen funktionieren.

## Abweichung Kurzfassung ↔ PRD

Die Kurzfassung nennt zusätzlich Online-Werkstatttermine (≤ 3 Schritte, Bestätigung, Erinnerung, proaktive Nachricht bei Verzögerung), Statusabfrage per Auftragsnummer, Filialverfügbarkeit im Shop und einen FAQ-Chat mit Übergabe ans Team, sowie Livegang vor Frühjahr 2027. Das ausführliche PRD enthält diese Punkte nicht. Vor dem Umsetzen solcher Features nachfragen, welche Version gilt.

## Ton & Gestaltung

Ausführliche Design-Vorgaben (Farben, Navigation, Barrierefreiheit, offene Punkte): [DESIGN.md](DESIGN.md) – vor jeder Gestaltungsarbeit lesen.

@DESIGN.md

Kurzfassung:

- Sprache Deutsch, Ton **sachlich, hilfsbereit, per Sie**.
- Haltung des Hauses: „Erst anschauen, dann sagen.“ – Zusagen werden gehalten; Texte versprechen nichts, was nicht eingelöst wird.
- Farben Blau und Orange sind gesetzt (wie auf den Firmenfahrzeugen).
- Klare Navigation: B2B, Privatkunden und Werkstatt auf den ersten Blick unterscheidbar.

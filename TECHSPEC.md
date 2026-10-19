# Techspec – Website Radwerk Mitte

Stand: 2026-10-19. Technische Spezifikation auf Basis der Quelldokumente (siehe [CLAUDE.md](CLAUDE.md)). Noch kein Code, kein Build, keine Tests. **Tech-Stack ist bewusst noch offen** – siehe Abschnitt „Offene Entscheidungen".

## Zweck

Grundlage für die technische Umsetzung von Version 1 der Website (lt. ausführlichem PRD). Wird ergänzt/konkretisiert, sobald Stack, Hosting und CMS feststehen.

## Funktionaler Scope (V1)

Abgeleitet aus den Akzeptanzkriterien in [CLAUDE.md](CLAUDE.md):

1. **Startseite** mit Ein-Klick-Zugang zu „Dienstrad-Leasing für Unternehmen" (B2B).
2. **Leasing-Rechner**
   - Eingabe: Radpreis, Bruttogehalt.
   - Ausgabe: monatliche Belastung, mit sichtbarem Hinweis „unverbindlich".
   - Berechnungslogik/Konditionen: noch offen, liefert Radwerk.
3. **Anfrageformular**
   - Pflichtfeld Kategorie (z. B. B2B-Angebot, Werkstatt, Bestellung, Sonstiges).
   - Routing per E-Mail an zuständige Person je Kategorie (Zuordnung: siehe Ansprechpersonen in CLAUDE.md).
   - B2B-Formular zusätzlich mit Firmengröße und Bedarf.
4. **FAQ-Bereich** zu häufigen Standardfragen (Inhalte liefert Radwerk/Amara Osei).
5. **Referenzen**: mindestens ein B2B-Referenzkunde darstellbar.
6. **Globale Elemente auf jeder Seite**: Telefonnummer, Standorte Kassel und Göttingen (z. B. Header/Footer).
7. **Link zum externen Onlineshop**, gut sichtbar, funktionsfähig (kein eigener Checkout).
8. **Navigation**: B2B, Privatkunden, Werkstatt klar unterscheidbar (siehe [DESIGN.md](DESIGN.md)).
9. **Messung**: Absprungrate und Anzahl Anfragen ab Launch erfassbar, datenschutzkonform (siehe Abschnitt Analytics).
10. **CMS-Pflegbarkeit**: Texte/Bilder durch Team (Svenja Kowalczyk) ohne Programmierkenntnisse änderbar.

## Nicht-Ziele (explizit nicht bauen)

- Eigener Onlineshop/Checkout (nur Verlinkung).
- Partnerportal oder Kunden-Login (nur Schnittstellen technisch vorbereiten, nicht umsetzen).
- Konfigurator für Custom-Räder.
- Rebranding (Farben Blau/Orange bleiben, siehe DESIGN.md).
- Neue Support-Software.
- Lösung muss ohne zusätzliche Personalstellen betreibbar sein (Pflegeaufwand gering halten).

## Nicht-funktionale Anforderungen

- **Responsive / Mobile First**: alle Seiten voll smartphone-tauglich.
- **Barrierefreiheit**: Arbeitsmaßstab WCAG 2.1 AA (Kontrast, Tastaturbedienung, Alternativtexte, sichtbarer Fokus, Überschriftenstruktur). Details: [DESIGN.md](DESIGN.md).
- **Datenschutz**: Analytics/Tracking datenschutzkonform (DSGVO) – Tool noch offen, keine personenbezogene Auswertung ohne Rechtsgrundlage/Einwilligung.
- **E-Mail-Zustellung**: Formular-Routing muss zuverlässig zustellen (SPF/DKIM/DMARC je nach gewähltem Versandweg – bei Stack-Entscheidung berücksichtigen).
- **Wartbarkeit**: Content-Pflege ohne Entwickler:in; Redaktionssystem muss unterschiedliche Textlängen/Bildformate vertragen (siehe DESIGN.md „Pflegbarkeit").
- **Performance**: keine harten Vorgaben in den Quelldokumenten – Standard-Erwartung „modern, nicht altbacken", daher übliche Web-Vitals-Praxis anstreben.

## Schnittstellen

- **Externer Onlineshop**: ausgehender Link, kein API-Zugriff gefordert.
- **E-Mail-Versand**: Formulardaten → Weiterleitung an zuständige Person je Kategorie.
- **Zukünftige Schnittstellen (nur vorbereiten, nicht bauen)**: Partnerportal/Kunden-Login – technisch so anlegen, dass eine spätere Anbindung möglich ist, ohne sie in V1 zu implementieren.

## Datenmodell (grob, vorläufig)

- **Anfrage** (aus Formular): Kategorie (Pflicht), Kontaktdaten, Nachricht, bei B2B zusätzlich Firmengröße + Bedarf, Zeitstempel, Status (z. B. „neu/weitergeleitet").
- **FAQ-Eintrag**: Frage, Antwort, Kategorie/Thema.
- **Referenz**: Kundenname (B2B), Kurzbeschreibung, ggf. Bild/Logo (Freigabe durch Kunde nötig – mit Radwerk klären).
- **Leasing-Rechner-Parameter**: Radpreis (Eingabe), Bruttogehalt (Eingabe), Berechnungsformel/Konditionen (TBD von Radwerk).

Konkrete Felder/Typen werden erst mit CMS-/Stack-Wahl spezifiziert.

## Offene Entscheidungen (mit Radwerk/Projektteam klären)

- **Tech-Stack**: Framework, Hosting, CMS – noch nicht gewählt. Bestehende WordPress-Seite wird erst per Fragebogen analysiert; WordPress ist **nicht** gesetzt.
- **Leasing-Konditionen/Berechnungsformel**: liefert Radwerk.
- **Analytics-Tool**: datenschutzkonforme Lösung noch zu wählen (z. B. serverseitig, ohne Cookies/Consent-Pflicht wo möglich).
- **Markenfarben (exakte HEX/RGB-Werte)**: bei Radwerk anfragen, keine Werte erfinden (siehe DESIGN.md).
- **E-Mail-Routing-Zuordnung**: genaue Kategorie→Person-Zuordnung final mit Radwerk abstimmen.
- **Umfang Kurzfassung vs. PRD**: Online-Werkstatttermine, Statusabfrage, Filialverfügbarkeit, FAQ-Chat stehen nur in der Kurzfassung, nicht im ausführlichen PRD – vor Umsetzung Rückfrage, welche Version gilt (siehe CLAUDE.md „Abweichung Kurzfassung ↔ PRD").
- **Freigabeprozess**: Anzahl Entwurfsrunden, Entscheider:in für Design (Merle Vogelsang gibt frei, lt. DESIGN.md).

## Nächste Schritte

1. Fragebogen zur bestehenden WordPress-Seite auswerten → Stack-Entscheidung.
2. Sobald Stack gewählt: dieses Dokument um konkrete Architektur, Build-/Test-Befehle und Ordnerstruktur ergänzen; CLAUDE.md entsprechend aktualisieren.

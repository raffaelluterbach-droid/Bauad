# BauAdmin

Bauadministration nach BKP (Schweizer Baukostenplan) — Kostenkontrolle, Verträge & Nachträge, Rechnungen, Leistungsverzeichnisse (SIA 451 / CRBX), Angebotsvergleich mit Nutzwertanalyse, Rapporte, Erwartungen und Bauabrechnung.

## Nutzung

**`bauadmin.html`** — die fertige App. Herunterladen und per Doppelklick im Browser öffnen (Chrome/Edge/Firefox). Komplett offline-fähig: React, Tailwind und der App-Code sind eingebettet, kein Internet nötig. Daten werden lokal im Browser gespeichert (localStorage).

**`bauadmin-quellcode.html`** — Entwicklungsversion mit lesbarem JSX-Quellcode (lädt React/Tailwind/Babel per CDN, braucht Internet).

## Funktionen

- **Kostenübersicht**: KV revidiert, beauftragt, Prognose, bezahlt — nach BKP-Gruppen
- **KV / BKP-Positionen**: CSV-Import, Hierarchie (Haupt-/Unterpositionen)
- **Mutationen & Umbuchungen**: Budgetänderungen und -verschiebungen
- **Verträge & Nachträge**: nach BKP geordnet, Konditionen-Kaskade (Rabatt → Pauschal → Skonto → Bauabzüge → Rundung), Regiebudget, Teuerung
- **Rechnungen**: Akonto/Rechnung/Regie, Status-Workflow, fakturiert/soll-Kontrolle
- **Leistungsverzeichnisse**: SIA-451/CRBX-Import (echtes Messerli-Format inkl. Einheitspreise), Preis-Matrix Positionen × Unternehmer, Offerten-Import je Unternehmer (CRBX/CSV), Vergabe an neue oder bestehende Verträge
- **Angebote & Vergleich**: Nutzwertanalyse (Preis/Referenzen/Lehrlinge, gewichtet)
- **Rapporte**: auf Verträge, netto nach Konditionen, Regie-Überschuss → Erwartung
- **Bauabrechnung**: Detailzeilen, Netto/Brutto, Doppelklick-Bearbeitung, CSV/PDF-Export

## Entwicklung

Der Quellcode liegt als JSX in `bauadmin-quellcode.html`. Die Offline-Datei `bauadmin.html` wird daraus gebaut (Babel-Kompilierung + statisches Tailwind-CSS + React UMD inline).

# NIS2 Incident Reporting Playbook

## Dokumentinformationen

- Dokument-ID: PB-NIS2-REPORT-001
- Version: 1.0
- Klassifizierung: Vertraulich / Intern
- Referenzstandards:
  - NIS2 (Directive (EU) 2022/2555)
  - Nationale NIS2-Umsetzung
  - BSI-Meldeverfahren
  - ISO 27035
  - IEC 62443
- Geltungsbereich:
  - Wesentliche Einrichtungen
  - Wichtige Einrichtungen
  - KRITIS-Betreiber
  - OT-/ICS-Umgebungen
  - IT-Systeme mit NIS2-Relevanz

---

# Zweck

Dieses Playbook definiert den standardisierten Prozess zur Bewertung, Vorbereitung, Erstellung und Einreichung von Meldungen im Rahmen der NIS2-Meldepflichten.

Ziele:

- Fristgerechte Meldungen
- Nachvollziehbare Dokumentation
- Einheitliche Kommunikation
- Minimierung regulatorischer Risiken
- Nachweis der Compliance

---

# Management Summary

## NIS2-Meldekette

### Innerhalb von 24 Stunden

Frühwarnung (Early Warning)

### Innerhalb von 72 Stunden

Incident-Meldung (Incident Notification)

### Innerhalb von 1 Monat

Abschlussbericht (Final Report)

### Optional

Zwischenbericht (Progress Report)

---

# Rollen und Verantwortlichkeiten

## Incident Commander

Verantwortlich für:

- Lagebewertung
- Eskalation
- Genehmigung technischer Informationen

---

## Compliance

Verantwortlich für:

- Meldepflichtprüfung
- Fristenkontrolle
- Dokumentation

---

## Legal

Verantwortlich für:

- Rechtliche Bewertung
- Haftungsprüfung
- Behördenabstimmung

---

## Kommunikation

Verantwortlich für:

- Interne Kommunikation
- Externe Kommunikation
- Medienkommunikation

---

## Executive Crisis Team

Verantwortlich für:

- Managemententscheidungen
- Freigaben
- Governance

---

# Phase 1: Meldepflicht prüfen

## Ziel

Feststellen, ob ein Vorfall unter die NIS2-Meldepflicht fällt.

---

## Prüfkriterien

### Auswirkungen auf Dienstleistungen

- Schwerwiegende Betriebsstörung
- Beeinträchtigung kritischer Dienste
- Produktionsstillstand

### Finanzielle Auswirkungen

- Wesentliche finanzielle Schäden
- Erhebliche Betriebsunterbrechungen

### Auswirkungen auf Dritte

- Kunden betroffen
- Lieferanten betroffen
- Partner betroffen

### Sicherheitsrelevanz

- Vertraulichkeitsverletzung
- Integritätsverletzung
- Verfügbarkeitsverlust

---

## Checkliste

- [ ] Betroffene Dienstleistung identifiziert
- [ ] Schweregrad bewertet
- [ ] Auswirkungen bewertet
- [ ] Meldepflicht festgestellt
- [ ] Dokumentation gestartet

---

# Phase 2: 24-Stunden-Frühwarnung

## Ziel

Frühzeitige Information der zuständigen Behörde.

---

## Frist

```text
Innerhalb von 24 Stunden nach Kenntnisnahme
```

---

## Minimalinhalt

### Basisinformationen

- Organisation
- Ansprechpartner
- Datum und Uhrzeit der Entdeckung

### Vorläufige Bewertung

- Vermuteter Vorfall
- Betroffene Systeme
- Erste Auswirkungen

### Pflichtangaben

- Verdacht auf vorsätzliches oder kriminelles Handeln
- Mögliche grenzüberschreitende Auswirkungen

---

## Frühwarnungs-Checkliste

- [ ] Incident dokumentiert
- [ ] Ansprechpartner benannt
- [ ] Auswirkungen beschrieben
- [ ] Vorläufige Bewertung erstellt
- [ ] Frühwarnung freigegeben
- [ ] Frühwarnung versendet

---

## Frühwarnungs-Vorlage

### Zusammenfassung

```text
Am [DATUM/UHRZEIT] wurde ein Cyber-Sicherheitsvorfall festgestellt.

Der Vorfall betrifft derzeit [SYSTEME/DIENSTE].

Eine Untersuchung läuft.

Zum Zeitpunkt der Meldung besteht:
[ ] Verdacht auf kriminelle Handlung
[ ] Verdacht auf grenzüberschreitende Auswirkungen

Weitere Informationen folgen im Rahmen der Incident-Meldung.
```

---

# Phase 3: 72-Stunden-Incident-Meldung

## Ziel

Bereitstellung strukturierter Informationen zum Vorfall.

---

## Frist

```text
Innerhalb von 72 Stunden nach Kenntnisnahme
```

---

## Inhalte

### Vorfallbeschreibung

- Was ist passiert?
- Wann wurde der Vorfall entdeckt?
- Wie wurde er entdeckt?

### Auswirkungen

- Betroffene Systeme
- Betroffene Dienste
- Betroffene Standorte
- Produktionsauswirkungen

### Schweregrad

- Niedrig
- Hoch
- Kritisch

### Indicators of Compromise (IoCs)

Beispiele:

- Schadsoftware
- Hashwerte
- Domains
- IP-Adressen
- Benutzerkonten

### Gegenmaßnahmen

- Isolation
- Segmentierung
- Eindämmung
- Forensik

---

## Incident-Meldungs-Checkliste

- [ ] Vorfall beschrieben
- [ ] Betroffene Systeme dokumentiert
- [ ] Auswirkungen bewertet
- [ ] IoCs dokumentiert
- [ ] Gegenmaßnahmen dokumentiert
- [ ] Freigabe erfolgt
- [ ] Meldung eingereicht

---

## Incident-Meldungs-Vorlage

### Zusammenfassung

```text
Der Vorfall wurde am [DATUM/UHRZEIT] entdeckt.

Betroffen sind:

- [SYSTEM]
- [SYSTEM]
- [SYSTEM]

Bekannte Auswirkungen:

- [AUSWIRKUNG]

Aktuelle Gegenmaßnahmen:

- [MASSNAHME]

Bekannte IoCs:

- [IOC]
```

---

# Phase 4: Zwischenbericht

## Ziel

Behörden über neue Erkenntnisse informieren.

---

## Wann erforderlich?

- Vorfall dauert länger an
- Behörde fordert zusätzliche Informationen an
- Wesentliche Änderungen ergeben sich

---

## Inhalte

### Status

- Aktueller Bearbeitungsstand
- Neue Erkenntnisse
- Neue Risiken

### Fortschritt

- Eindämmungsmaßnahmen
- Wiederherstellung
- Forensik

---

## Checkliste

- [ ] Neue Erkenntnisse dokumentiert
- [ ] Fortschritt beschrieben
- [ ] Bericht freigegeben
- [ ] Bericht eingereicht

---

# Phase 5: Abschlussbericht

## Ziel

Abschluss der Meldepflicht.

---

## Frist

```text
Innerhalb eines Monats
```

oder

```text
Nach Abschluss des Vorfalls
```

---

## Pflichtinhalte

### Root Cause Analysis

- Ursache
- Angriffsvektor
- Ausbreitung

### Auswirkungen

- Systeme
- Produktion
- Kunden
- Geschäftsbetrieb

### Maßnahmen

- Eindämmung
- Wiederherstellung
- Verbesserungen

### Erkenntnisse

- Lessons Learned
- Kontrollversagen
- Verbesserungsmaßnahmen

---

## Abschlussbericht-Checkliste

- [ ] Root Cause Analysis abgeschlossen
- [ ] Auswirkungen dokumentiert
- [ ] Gegenmaßnahmen dokumentiert
- [ ] Verbesserungen festgelegt
- [ ] Bericht freigegeben
- [ ] Bericht eingereicht

---

## Abschlussbericht-Vorlage

### Zusammenfassung

```text
Der Vorfall begann am [DATUM].

Ursache:

[URSACHE]

Betroffene Bereiche:

- [BEREICH]
- [BEREICH]

Auswirkungen:

[AUSWIRKUNGEN]

Ergriffene Maßnahmen:

[MASSNAHMEN]

Geplante Verbesserungen:

[VERBESSERUNGEN]
```

---

# Kommunikationsfreigabe

## Verpflichtende Freigaben

Vor jeder Meldung:

- [ ] Incident Commander
- [ ] Compliance
- [ ] Legal
- [ ] Executive Crisis Team

---

# Dokumentationspflichten

## Zu archivieren

### Meldungen

- Frühwarnungen
- Incident-Meldungen
- Zwischenberichte
- Abschlussberichte

### Nachweise

- Forensische Berichte
- IoC-Listen
- Kommunikationsprotokolle
- Entscheidungsprotokolle

### Aufbewahrung

- Gemäß internen Compliance-Vorgaben
- Gemäß regulatorischen Anforderungen

---

# Management Dashboard

## Kritische Kennzahlen

### Compliance

- Anzahl meldepflichtiger Vorfälle
- Fristgerechte Meldungen
- Offene Meldeverfahren

### Incident Management

- Time to Detect
- Time to Report
- Time to Contain
- Time to Recover

---

# Quick Reference

## NIS2 Reporting Timeline

### 24 Stunden

- [ ] Frühwarnung

### 72 Stunden

- [ ] Incident-Meldung

### 1 Monat

- [ ] Abschlussbericht

### Optional

- [ ] Zwischenbericht

---

# Executive Statement

NIS2-Meldungen sind keine rein regulatorische Pflicht.

Sie sind ein zentraler Bestandteil moderner Cyber-Resilienz und ermöglichen eine koordinierte Reaktion auf sicherheitsrelevante Vorfälle mit potenziellen Auswirkungen auf Gesellschaft, Wirtschaft und kritische Dienstleistungen.

Fristgerechte, vollständige und nachvollziehbare Meldungen sind ein wesentlicher Bestandteil eines professionellen Incident- und Krisenmanagements.

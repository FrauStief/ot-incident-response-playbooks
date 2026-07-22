# OT Ransomware Response Playbook

## Dokumentinformationen

- Dokument-ID: PB-OT-RANSOM-001
- Version: 1.0
- Klassifizierung: Vertraulich / Intern
- Referenzstandards:
  - NIST SP 800-82
  - IEC 62443
  - BSI ICS Security Guidance
  - NIS2
- Geltungsbereich:
  - Produktionsstandorte
  - SCADA-Umgebungen
  - HMI-Systeme
  - Historian-Systeme
  - Engineering Workstations
  - OT Active Directory
  - OT-Netzwerke

---

# Zweck

Dieses Playbook beschreibt die standardisierte Reaktion auf einen bestätigten oder vermuteten Ransomware-Vorfall in einer Operational-Technology-(OT)-Umgebung.

Ziel ist der Schutz von:

- Menschen
- Umwelt
- Anlagen
- Produktionsprozessen
- Unternehmenswerten

---

# Leitprinzip

## Safety First

```text
SAFETY > AVAILABILITY > CONFIDENTIALITY
```

Menschen und Anlagen haben Vorrang vor allen technischen Wiederherstellungsmaßnahmen.

Keine Reaktion darf:

- Safety-Systeme gefährden
- Not-Aus-Funktionen beeinträchtigen
- Prozesssicherheit reduzieren
- Unkontrollierte Anlagenzustände erzeugen

---

# Typische OT-Ransomware-Ziele

## Produktionsnahe Systeme

- Engineering Workstations
- SCADA-Server
- HMI-Systeme
- Historian-Systeme
- APC-Systeme
- Manufacturing Execution Systems (MES)

## Infrastruktur

- OT Active Directory
- Dateiserver
- Backup-Systeme
- Jump Hosts
- Remote-Access-Plattformen

## Kritische Warnzeichen

- Lösegeldforderung
- Verschlüsselte Dateien
- Ausfall mehrerer HMIs
- Historian nicht erreichbar
- Unbekannte Benutzerkonten
- Deaktivierte Sicherheitssoftware
- Ungewöhnliche Netzwerkaktivität
- Massiver Dateiumsatz

---

# Incident-Klassifizierung

## Standard-Einstufung

Ein bestätigter OT-Ransomware-Vorfall wird mindestens als:

```text
STUFE 2 – HOCH
```

eingestuft.

---

## Automatische Einstufung als STUFE 3 – KRITISCH

Wenn mindestens eines der folgenden Kriterien erfüllt ist:

- SCADA betroffen
- SPS-/PLC-nahe Systeme betroffen
- Safety-Systeme betroffen
- Produktionsunterbrechung eingetreten
- Active Directory betroffen
- Historian betroffen
- Mehrere Anlagen betroffen
- Physische Auswirkungen möglich

---

# Phase 1: Erste 15 Minuten

## Ziel

Schutz von Menschen und Anlagen sowie Eindämmung des Vorfalls.

---

## 1.1 Safety prüfen

### Checkliste

- [ ] SIS überprüft
- [ ] Not-Aus-Systeme funktionsfähig
- [ ] Kühlsysteme stabil
- [ ] Keine unmittelbare Gefährdung
- [ ] Produktionsstatus bekannt

---

## 1.2 Incident bestätigen

### Prüfen

- Lösegeldforderung vorhanden
- Verschlüsselung aktiv
- Bekannte Ransomware-Indikatoren
- Auffällige Dateiveränderungen
- Active Directory betroffen

### Checkliste

- [ ] Incident bestätigt
- [ ] Zeit der Entdeckung dokumentiert
- [ ] Betroffene Systeme erfasst

---

## 1.3 OT Incident Response Team aktivieren

### Rollen

- OT Incident Commander
- OT Engineering
- OT Security
- IT Security
- Krisenstab
- Legal
- Compliance

### Checkliste

- [ ] OT-IRT aktiviert
- [ ] Kommunikationswege aktiviert
- [ ] Dokumentation begonnen

---

# Phase 2: Sofortige Eindämmung

## Ziel

Verhinderung weiterer Ausbreitung.

---

## 2.1 Air-Gap-on-Demand

### Maßnahmen

- IT-OT-Kommunikation unterbrechen
- IDMZ absichern
- Kritische Segmente isolieren

### Checkliste

- [ ] IT-Verbindungen getrennt
- [ ] IDMZ geschützt
- [ ] Segmentierung aktiv

---

## 2.2 Remote Access stoppen

### Maßnahmen

- VPN deaktivieren
- Jump Hosts deaktivieren
- Drittanbieterzugänge sperren
- Wartungszugänge blockieren

### Checkliste

- [ ] VPN deaktiviert
- [ ] Jump Hosts deaktiviert
- [ ] Remote Access beendet

---

## 2.3 Keine Neustarts

### Verbotene Maßnahmen

- Keine Server neu starten
- Keine HMIs neu starten
- Keine Engineering Workstations ausschalten
- Keine unkontrollierte Recovery starten

### Ziel

Erhalt forensischer Beweise.

### Checkliste

- [ ] Neustartverbot kommuniziert
- [ ] Systeme stabil gehalten

---

# Phase 3: Executive Escalation

## Ziel

Strategische Entscheidungen auf Management-Ebene.

---

## Executive Crisis Team aktivieren

### Beteiligte Rollen

- Geschäftsführung
- CIO
- CISO
- Werksleitung
- Legal
- Kommunikation

### Entscheidungen

- Produktionsstopp
- Notbetrieb
- Regulatorische Meldungen
- Kundenkommunikation
- Versicherungsaktivierung

### Checkliste

- [ ] Executive Team informiert
- [ ] Krisenstab aktiv
- [ ] Verantwortlichkeiten geklärt

---

# Phase 4: Forensik und Analyse

## Ziel

Art und Umfang des Angriffs feststellen.

---

## 4.1 Beweissicherung

### Sicherung

- Logs
- Speicherabbilder
- PCAP-Dateien
- Firewall-Logs
- Authentifizierungsdaten

### Checkliste

- [ ] Logs gesichert
- [ ] Speicherabbilder erstellt
- [ ] Netzwerkdaten gesichert

---

## 4.2 Scope Analysis

### Identifizieren

- Erstinfektion
- Ausbreitungspfad
- Betroffene Systeme
- Betroffene Benutzer
- Kompromittierte Konten

### Checkliste

- [ ] Scope definiert
- [ ] Patient Zero identifiziert
- [ ] Ausbreitung verstanden

---

# Phase 5: Backup- und Recovery-Bewertung

## Ziel

Ermitteln, ob eine Wiederherstellung möglich ist.

---

## Backup-Prüfung

### Kontrollieren

- Offline-Backups verfügbar
- Immutable Backups verfügbar
- Letzter erfolgreicher Backup-Lauf
- Backup-Integrität

### Checkliste

- [ ] Offline-Backup geprüft
- [ ] Immutable Backup geprüft
- [ ] Test-Restore erfolgreich

---

## Gold Master Validierung

### Prüfen

- SPS-Konfigurationen
- SCADA-Images
- Historian-Backups
- Engineering-Projekte

### Checkliste

- [ ] Gold Master verfügbar
- [ ] Integrität bestätigt

---

# Phase 6: Entscheidungspunkt

## Lösegeldzahlung

### Grundsatz

Das Werk trifft keine Lösegeldentscheidung.

### Verantwortlich

- Executive Crisis Team
- Geschäftsführung
- Legal
- Versicherer

### Checkliste

- [ ] Legal eingebunden
- [ ] Versicherer informiert
- [ ] Managemententscheidung dokumentiert

---

# Phase 7: Wiederherstellung

## Reihenfolge

### Schritt 1

- Safety-Systeme

### Schritt 2

- SPS-/PLC-Ebene

### Schritt 3

- SCADA und HMI

### Schritt 4

- Historian

### Schritt 5

- IDMZ

### Schritt 6

- Enterprise-Anbindung

---

## Recovery Checklist

- [ ] Firmware geprüft
- [ ] SPS-Logik geprüft
- [ ] Zertifikate erneuert
- [ ] Service Accounts erneuert
- [ ] SCADA validiert
- [ ] Historian validiert
- [ ] Active Directory validiert
- [ ] Recovery Gate bestanden

---

# Phase 8: Regulatorische Meldungen

## 24 Stunden

- [ ] Frühwarnung erstellt
- [ ] Behörde informiert

---

## 72 Stunden

- [ ] Incident-Meldung erstellt
- [ ] IoCs dokumentiert
- [ ] Auswirkungen beschrieben

---

## 1 Monat

- [ ] Abschlussbericht erstellt
- [ ] Root Cause Analysis abgeschlossen
- [ ] Verbesserungsmaßnahmen definiert

---

# Phase 9: Lessons Learned

## Root Cause Analysis

- [ ] Angriffsvektor identifiziert
- [ ] Schwachstellen identifiziert
- [ ] Timeline erstellt

---

## Verbesserungen

- [ ] Detection verbessert
- [ ] Playbooks angepasst
- [ ] Übungen geplant
- [ ] Recovery-Prozesse verbessert

---

# Incident Closure

Der Vorfall kann geschlossen werden, wenn:

- [ ] Produktion stabil läuft
- [ ] Safety-Systeme verifiziert sind
- [ ] Keine aktiven IoCs vorliegen
- [ ] Regulatorische Pflichten erfüllt wurden
- [ ] Management-Freigabe vorliegt
- [ ] Lessons Learned dokumentiert wurden

---

# Executive Statement

OT-Ransomware ist kein klassischer IT-Sicherheitsvorfall.

Sie ist ein potenzieller Betriebs-, Produktions- und Safety-Notfall, der eine koordinierte Reaktion von OT, IT, Management, Legal und Compliance erfordert.

Der Erfolg der Reaktion wird nicht daran gemessen, wie schnell Systeme neu gestartet werden, sondern daran, wie sicher Menschen geschützt, Anlagen stabilisiert und Produktionsprozesse wiederhergestellt werden.

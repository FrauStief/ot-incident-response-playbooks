# Management Summary

## Zweck des Playbooks

Dieses OT Incident Response Playbook definiert die verbindlichen Prozesse zur Erkennung, Eindämmung, Wiederherstellung und Nachbereitung von Cybervorfällen in Produktions- und OT-Umgebungen.

Ziel ist der Schutz von:

- Menschen
- Umwelt
- Produktionsanlagen
- Produktionsverfügbarkeit
- Unternehmenswerten
- Unternehmensreputation

---

# Management-Leitprinzip

## Prioritäten im Ernstfall

1. Safety (Mensch und Anlage)
2. Verfügbarkeit der Produktion
3. Vertraulichkeit von Daten

Produktionssicherheit hat stets Vorrang vor IT-Maßnahmen.

Keine Incident-Response-Maßnahme darf Safety-Systeme, Not-Aus-Ketten oder kritische Schutzmechanismen gefährden.

---

# Governance

## Verantwortlichkeiten

### OT Incident Commander

Verantwortlich für:

- Einsatzleitung
- Eskalationsentscheidungen
- Produktionsstopp
- Recovery-Freigabe

### Executive Crisis Team

Verantwortlich für:

- Strategische Entscheidungen
- Krisenmanagement
- Behördenkommunikation
- Externe Kommunikation
- Freigabe kritischer Maßnahmen

---

# Incident-Schweregrade

## Stufe 1 – Niedrig

Beispiele:

- Geblockte Angriffsversuche
- Isolierte Malware ohne Produktionsbezug

Auswirkung:

- Keine Produktionsbeeinträchtigung

---

## Stufe 2 – Hoch

Beispiele:

- Kompromittierte Engineering Workstations
- Befall einzelner HMI-Systeme
- Verdächtige Aktivitäten im OT-Netz

Auswirkung:

- Erhöhtes Betriebsrisiko
- Sofortige Incident Response erforderlich

---

## Stufe 3 – Kritisch

Beispiele:

- Manipulation von SPS-/PLC-Logik
- Ransomware im OT-Bereich
- Beeinträchtigung von SCADA-Systemen
- Gefährdung von Mensch oder Anlage

Auswirkung:

- Produktionsausfall möglich
- Notfallverfahren aktivieren
- Management-Eskalation

---

# Management-Kritische Entscheidungen

Im Vorfall müssen folgende Entscheidungen durch Management oder Executive Crisis Team getroffen werden:

- Produktionsstopp oder Weiterbetrieb
- Aktivierung des Krisenstabs
- Freigabe regulatorischer Meldungen
- Freigabe externer Kommunikation
- Einbindung externer Forensik-Partner
- Priorisierung von Wiederherstellungsmaßnahmen

---

# OT-Ransomware-Sonderfall

Bei Befall von:

- SCADA-Systemen
- Historian-Systemen
- Engineering Workstations
- APC-Systemen

werden sofort umgesetzt:

- Trennung von OT und IT
- Stopp aller Fernzugriffe
- Aktivierung des Executive Crisis Teams
- Forensische Beweissicherung
- Prüfung regulatorischer Meldepflichten

Lösegeldentscheidungen dürfen ausschließlich auf Unternehmensleitungsebene getroffen werden.

---

# Regulatorische Anforderungen

## NIS2- und BSIG-Meldepflichten

### Innerhalb von 24 Stunden

Frühwarnung an zuständige Behörden.

### Innerhalb von 72 Stunden

Vorläufige Incident-Meldung mit:

- Schweregrad
- Auswirkungen
- IoCs
- Gegenmaßnahmen

### Innerhalb von 1 Monat

Abschlussbericht mit:

- Root Cause Analysis
- Auswirkungen
- Maßnahmen
- Verbesserungsplan

---

# Recovery-Prinzip

Die Wiederherstellung erfolgt kontrolliert in vier Stufen:

1. Safety- und Hilfssysteme
2. SPS-/PLC-Ebene
3. HMI- und SCADA-Systeme
4. Re-Integration der IDMZ

Eine Produktionsfreigabe erfolgt erst nach erfolgreichem Recovery Gate Review.

---

# Erwarteter Nutzen für das Unternehmen

Durch die Umsetzung dieses Playbooks werden:

- Sicherheitsrisiken reduziert
- Ausfallzeiten verkürzt
- Regulatorische Anforderungen erfüllt
- Recovery-Prozesse standardisiert
- Unternehmenswerte geschützt
- Produktionsresilienz erhöht

---

# Management-Kennzahlen (KPIs)

Das Management sollte mindestens folgende Kennzahlen regelmäßig überwachen:

- Anzahl sicherheitsrelevanter OT-Incidents
- Mean Time to Detect (MTTD)
- Mean Time to Respond (MTTR)
- Mean Time to Recover (MTTRec)
- Anzahl erfolgreicher Recovery-Tests
- Anzahl OT-Tabletop-Übungen pro Jahr
- Status kritischer Backups
- Status kritischer Sicherheitsmaßnahmen

---

# Executive Statement

Cybervorfälle in der OT sind keine reinen IT-Ereignisse.

Sie sind potenzielle Betriebs- und Sicherheitsnotfälle mit Auswirkungen auf Menschen, Anlagen, Produktion, Lieferfähigkeit und Unternehmenswert.

Dieses Playbook stellt sicher, dass das Unternehmen solche Vorfälle strukturiert, sicher, regulatorisch konform und mit minimalen Auswirkungen auf den Geschäftsbetrieb bewältigen kann.
# Operational Technology Incident Response Plan (OT-IRP)

## Dokumentinformationen

- Dokument-ID: PB-OT-SEC-001
- Version: 3.0
- Klassifizierung: Vertraulich / Intern
- Referenzstandards:
  - NIST SP 800-82 Rev. 3
  - IEC 62443
  - BSI ICS-Security-Kompendium
  - NIS2
- Geltungsbereich:
  - Produktionsstandorte
  - SCADA-Systeme
  - HMI-Systeme
  - SPS-/PLC-Umgebungen
  - Gebäudeautomation
  - Industrial Demilitarized Zone (IDMZ)
  - OT-zu-IT-Schnittstellen

---

# Safety First

## Oberstes Leitprinzip

**SAFETY > AVAILABILITY > CONFIDENTIALITY**

Arbeitsschutz und physische Sicherheit haben bei allen Incident-Response-Maßnahmen absolute Priorität.

Folgende Systeme dürfen durch Incident-Response-Maßnahmen niemals unbeabsichtigt beeinträchtigt werden:

- Safety Instrumented Systems (SIS)
- Not-Aus-Ketten
- Druckentlastungssysteme
- Kühlkreisläufe
- Brandmelde- und Löschsysteme
- Physische Schutzmechanismen

Jede Isolierungs-, Eradikations- oder Recovery-Maßnahme ist vor Umsetzung auf mögliche Auswirkungen auf Menschen, Umwelt und Anlagen zu bewerten.

---

# Phase 0: Vorbereitung und Readiness

## Ziel

Ziel dieser Phase ist die organisatorische, technische und personelle Vorbereitung auf Cyber-Sicherheitsvorfälle in OT-Umgebungen.

Eine erfolgreiche Incident Response beginnt vor der Erkennung eines Vorfalls.

---

## 0.1 Asset Readiness

### Anforderungen

- Vollständiges OT-Asset-Inventar
- Inventar aller SPS-/PLC-Systeme
- Inventar aller HMI-Systeme
- Inventar aller SCADA-Systeme
- Inventar aller Historian-Systeme
- Dokumentation aller Firmware-Versionen
- Dokumentation aller Software-Versionen
- Aktuelle Netzwerkpläne
- Purdue-Modell-Dokumentation
- Kommunikationsmatrix aller OT-Segmente
- Kritikalitätsbewertung aller Systeme

### Nachweis

- [ ] Asset-Inventar aktuell
- [ ] Netzwerkdokumentation aktuell
- [ ] Kritikalitätsbewertung vorhanden

---

## 0.2 Backup Readiness

### Anforderungen

- Offline-Backups aller SPS-/PLC-Konfigurationen
- Offline-Backups aller HMI-Systeme
- Offline-Backups aller SCADA-Systeme
- Offline-Backups aller Historian-Systeme
- Immutable Backups kritischer Systeme
- Gold-Master-Konfigurationen verfügbar
- Regelmäßige Wiederherstellungstests
- Dokumentierte Restore-Prozesse

### Nachweis

- [ ] Offline-Backups vorhanden
- [ ] Recovery-Test erfolgreich durchgeführt
- [ ] Backup-Integrität geprüft

---

## 0.3 Incident Readiness

### Anforderungen

- Mindestens eine OT-IR-Übung pro Jahr
- Regelmäßige Tabletop-Exercises
- Krisenstabsübungen
- Dokumentierte Eskalationswege
- Dokumentierte Alarmierungswege
- Dokumentierte Kommunikationspläne
- Out-of-Band-Kommunikationskanäle verfügbar

### Nachweis

- [ ] Letzte Übung dokumentiert
- [ ] Alarmierungsprozess getestet
- [ ] Krisenstab geschult

---

## 0.4 Third-Party Readiness

### Anforderungen

- Lieferantenkontakte aktuell
- Herstellerkontakte aktuell
- Hersteller-Eskalationspfade dokumentiert
- OT-Forensik-Partner verfügbar
- Incident-Response-Retainer aktiv
- CERT- und Behördenkontakte gepflegt

### Nachweis

- [ ] Kontaktlisten aktuell
- [ ] Retainer-Verträge gültig
- [ ] Eskalationspfade dokumentiert

---

## Exit-Kriterien Phase 0

Die Organisation gilt als vorbereitet, wenn:

- [ ] Asset-Inventar vollständig ist
- [ ] Kritische Systeme gesichert sind
- [ ] Wiederherstellungstests erfolgreich waren
- [ ] Alarmierungsketten funktionieren
- [ ] Third-Party-Partner verfügbar sind
- [ ] Übungen regelmäßig durchgeführt werden

---

# Phase 1: Rollen und Verantwortlichkeiten

## 1.1 OT Incident Commander (OT-IC)

### Rolle

Accountable

### Verantwortlichkeiten

- Gesamteinsatzleitung im Werk
- Incident-Klassifizierung freigeben
- Produktionsstopp anordnen
- Notbetrieb anordnen
- Recovery freigeben
- Kommunikation mit Management koordinieren

---

## 1.2 Lead OT Engineer (OT-ENG)

### Rolle

Responsible

### Verantwortlichkeiten

- Bewertung der Anlagensicherheit
- Steuerung des operativen Anlagenbetriebs
- Durchführung manueller Bedienverfahren
- Freigabe lokaler Eingriffe
- Unterstützung bei Recovery und Inbetriebnahme

---

## 1.3 OT Security Specialist (OT-SEC)

### Rolle

Responsible

### Verantwortlichkeiten

- Forensische Analyse
- Log-Analyse
- Netzwerkforensik
- IoC-Hunting
- Threat Hunting
- Integritätsprüfung von SPS-Programmen
- Dokumentation technischer Erkenntnisse

---

## 1.4 IT Security Lead (IT-SEC)

### Rolle

Consulted

### Verantwortlichkeiten

- Schutz der Enterprise-IT
- Isolation der IDMZ
- Unterstützung bei Netzwerksegmentierung
- Kontrolle von Remote-Zugängen
- Unterstützung bei forensischen Untersuchungen

---

## 1.5 Compliance, Legal und Kommunikation

### Rolle

Informed

### Verantwortlichkeiten

- Regulatorische Bewertung
- BSI- und NIS2-Meldungen
- Juristische Bewertung
- Externe Kommunikation
- Medienkommunikation
- Dokumentationspflichten

---

# Phase 2: Triage und Incident-Klassifizierung

## Ziel

Jeder erkannte Vorfall ist innerhalb von 15 Minuten zu klassifizieren.

Die Einstufung bestimmt die weiteren Maßnahmen und Eskalationspfade.

---

## 2.1 Entscheidungslogik

### Frage 1

Ist der physische Prozess sicher und stabil?

#### Ja

Bewertung als Stufe 1 oder Stufe 2.

#### Nein

Sofortige Einstufung als Stufe 3.

---

### Frage 2

Sind produktionskritische Systeme betroffen?

Beispiele:

- SPS-/PLC-Systeme
- SCADA-Systeme
- Safety Instrumented Systems (SIS)
- HMI-Systeme
- Historian-Systeme

#### Ja

Mindestens Stufe 2.

#### Nein

Bewertung nach Risiko und Auswirkung.

---

## 2.2 Stufe 1 – Niedrig

### Kriterien

- Geblockter Portscan
- Einzelne Firewall-Anomalien
- Isolierte Malware auf Nicht-Produktionssystemen
- Keine OT-Auswirkungen
- Keine Ausbreitung erkennbar

### Maßnahmen

- Vorfall dokumentieren
- Monitoring erhöhen
- Ursachenanalyse durchführen
- Incident beobachten

---

## 2.3 Stufe 2 – Hoch

### Kriterien

- Infektion einzelner HMI-Systeme
- Infektion von Engineering Workstations
- Ungewöhnliche OT-Protokollaktivitäten
- Verdächtige Netzwerkkommunikation
- Produktion läuft weiterhin stabil

### Maßnahmen

- Incident Response Team aktivieren
- Segmentierung prüfen
- Forensik einleiten
- Management informieren

---

## 2.4 Stufe 3 – Kritisch

### Kriterien

- Manipulation von SPS-/PLC-Logik
- Manipulation von SIS-Systemen
- Kontrollverlust über Produktionsprozesse
- Ransomware im OT-Segment
- Physische Gefährdung von Menschen
- Physische Gefährdung von Anlagen
- Andauernde Produktionsstörung

### Maßnahmen

- Sofortige Aktivierung des OT-IRTs
- Management-Eskalation
- Einleitung von Notfallverfahren
- Vorbereitung regulatorischer Meldungen
- Air-Gap-on-Demand prüfen

---

## 2.5 OT-Ransomware-Sonderfall

### Betroffene Systeme

- Engineering Workstations
- Historian-Systeme
- SCADA-Systeme
- Advanced Process Control Systeme (APC)
- OT-Dateiserver
- OT-Domänencontroller

### Sofortmaßnahmen

#### Maßnahme 1: OT von IT trennen

- Air-Gap-on-Demand aktivieren
- Nicht benötigte Verbindungen unterbrechen
- IDMZ absichern

#### Maßnahme 2: Keine Neustarts

- Systeme nicht neu starten
- Systeme nicht ausschalten
- Flüchtige Daten erhalten

#### Maßnahme 3: Keine Lösegeldentscheidung auf Werksebene

- Entscheidungen ausschließlich durch Executive Crisis Team
- Einbindung von Geschäftsführung und Legal

#### Maßnahme 4: Executive Crisis Team aktivieren

- Management
- Legal
- Compliance
- Kommunikation
- Cyber-Krisenstab

#### Maßnahme 5: Meldepflichten prüfen

- BSI
- Aufsichtsbehörden
- NIS2-relevante Stellen

### Zusätzliche Maßnahmen

- [ ] Ausbreitungsanalyse durchführen
- [ ] Remote-Zugänge deaktivieren
- [ ] Backups prüfen
- [ ] Forensik aktivieren
- [ ] SPS-/PLC-Integrität prüfen
- [ ] SCADA-Integrität prüfen
- [ ] Historian-Integrität prüfen

### Hinweis

Safety und Anlagenstabilität haben bei OT-Ransomware-Vorfällen stets Vorrang vor Wiederherstellungs- oder Bereinigungsmaßnahmen.

---

## Exit-Kriterien Phase 2

- [ ] Incident-Klassifizierung durchgeführt
- [ ] Verantwortlichkeiten zugewiesen
- [ ] Eskalationslevel festgelegt
- [ ] Kommunikationswege aktiviert
- [ ] Entscheidung über weitere Maßnahmen getroffen

---

# Phase 3: Detektion und Erstevaluation

## Ziel

Ziel dieser Phase ist die schnelle Bewertung des Vorfalls, die Sicherstellung der Anlagensicherheit und die Aktivierung der Incident-Response-Prozesse.

---

## 3.1 Prozesssicherheit prüfen

### Aufgaben

- Status der Safety Instrumented Systems (SIS) prüfen
- Status von Not-Aus-Systemen prüfen
- Status von Kühlkreisläufen prüfen
- Status von Druckentlastungssystemen prüfen
- Status physischer Schutzsysteme prüfen
- Prüfung auf Anzeichen physischer Gefährdungen

### Checkliste

- [ ] SIS betriebsbereit
- [ ] Not-Aus-Systeme funktionsfähig
- [ ] Kühlkreisläufe funktionsfähig
- [ ] Druckentlastungssysteme funktionsfähig
- [ ] Keine unmittelbare Personen- oder Anlagengefährdung

---

## 3.2 Incident klassifizieren

### Aufgaben

- Klassifizierung bestätigen
- Auswirkungen bewerten
- Kritikalität überprüfen
- Eskalationsstufe bestätigen

### Checkliste

- [ ] Incident-Stufe bestätigt
- [ ] Auswirkungen dokumentiert
- [ ] Verantwortlichkeiten bestätigt
- [ ] Eskalationsstufe aktiviert

---

## 3.3 OT Incident Response Team aktivieren

### Aufgaben

- OT Incident Commander informieren
- OT Incident Response Team alarmieren
- Out-of-Band-Kommunikation aktivieren
- Dokumentation starten

### Zulässige Kommunikationswege

- Notfalltelefonie
- Satellitentelefon
- Funk
- Separierte Notfallsysteme

### Checkliste

- [ ] OT-IC informiert
- [ ] OT-IRT aktiviert
- [ ] Kommunikationswege verfügbar
- [ ] Incident-Dokumentation gestartet

---

## 3.4 Beweissicherung und Log Preservation

### Aufgaben

- Relevante Logs sichern
- Flüchtige Daten sichern
- Netzwerkverkehr dokumentieren
- Zeitleiste starten

### Voraussetzungen

Systeme dürfen nicht ohne Bewertung ausgeschaltet werden.

Ausnahmen sind nur zulässig, wenn:

- Safety gefährdet ist
- Anlagen beschädigt werden könnten
- Gefahr für Personen besteht

### Checkliste

- [ ] Logdaten gesichert
- [ ] Netzwerkdaten gesichert
- [ ] Forensische Beweissicherung gestartet
- [ ] Incident-Timeline erstellt

---

## Exit-Kriterien Phase 3

- [ ] Anlagenzustand bewertet
- [ ] Incident klassifiziert
- [ ] Incident Team aktiviert
- [ ] Beweissicherung gestartet
- [ ] Eskalationspfade aktiviert

---

# Phase 4: Eindämmung (Containment)

## Ziel

Ziel der Eindämmung ist die Verhinderung einer weiteren Ausbreitung des Angreifers bei gleichzeitigem Erhalt eines sicheren Anlagenbetriebs.

---

## 4.1 Air-Gap-on-Demand aktivieren

### Ziel

Logische Trennung von Enterprise-IT und OT-Umgebung.

### Maßnahmen

- Trennung aller nicht erforderlichen Verbindungen
- Isolation kritischer Segmente
- Aktivierung definierter Incident-Regeln
- Schutz der IDMZ

### Checkliste

- [ ] IT-OT-Verbindungen bewertet
- [ ] Nicht erforderliche Verbindungen getrennt
- [ ] IDMZ abgesichert
- [ ] Segmentierung aktiv

---

## 4.2 IDMZ-Trennung

### Maßnahmen

- In-Band-Verbindungen trennen
- Out-of-Band-Verbindungen prüfen
- Firewall-Notfallregeln aktivieren
- Kommunikationspfade dokumentieren

### Checkliste

- [ ] Firewall-Regeln aktiviert
- [ ] IDMZ isoliert
- [ ] Verbindungen dokumentiert
- [ ] Ausnahmezugriffe geprüft

---

## 4.3 Remote Access stoppen

### Maßnahmen

- VPN-Zugänge deaktivieren
- Jump Hosts sperren
- Drittanbieterzugänge deaktivieren
- Wartungsverbindungen beenden

### Checkliste

- [ ] VPN deaktiviert
- [ ] Jump Hosts gesperrt
- [ ] Drittanbieterzugänge deaktiviert
- [ ] Aktive Sitzungen beendet

---

## 4.4 Manuelle Betriebsführung aktivieren

### Ziel

Aufrechterhaltung der Produktion bei Ausfall von HMI- oder SCADA-Systemen.

### Maßnahmen

- Umschaltung auf lokale Bedienung
- Aktivierung manueller Verfahren
- Unterstützung durch OT-ENG

### Voraussetzungen

Nur nach Freigabe durch den Lead OT Engineer.

### Checkliste

- [ ] Lokale Bedienung möglich
- [ ] Bedienpersonal verfügbar
- [ ] Verfahren dokumentiert
- [ ] Freigabe erteilt

---

## 4.5 Passives Netzwerkmonitoring aktivieren

### Ziel

Analyse des Vorfalls ohne Beeinflussung der Produktionsumgebung.

### Maßnahmen

- Aktivierung vorhandener TAPs
- Aktivierung von SPAN-Ports
- Aufzeichnung relevanter Protokolle
- Erstellung von PCAP-Dateien

### Beobachtete Protokolle

- S7
- Modbus
- CIP
- DNP3
- OPC UA
- Weitere herstellerspezifische ICS-Protokolle

### Checkliste

- [ ] Monitoring aktiviert
- [ ] Netzwerkverkehr aufgezeichnet
- [ ] PCAP-Sammlung gestartet
- [ ] Daten sicher gespeichert

---

## Exit-Kriterien Phase 4

- [ ] Ausbreitung gestoppt
- [ ] Netzwerk segmentiert
- [ ] Remote Access deaktiviert
- [ ] Netzwerküberwachung aktiv
- [ ] Produktionsbetrieb stabil

---

# Phase 5: Eradikation und Integritätsprüfung

## Ziel

Entfernung kompromittierter Komponenten sowie Nachweis der Integrität aller produktionsrelevanten Systeme.

---

## 5.1 SPS-/PLC-Code-Verifikation

### Aufgaben

- Vergleich produktiver Programme mit Gold-Master-Versionen
- Hash-Prüfung
- Checksummen-Vergleich
- Freigabe durch OT-Engineering

### Checkliste

- [ ] SPS-Logik verifiziert
- [ ] Referenzstände geprüft
- [ ] Abweichungen dokumentiert
- [ ] Engineering-Freigabe erfolgt

---

## 5.2 HMI- und SCADA-Wiederherstellung

### Grundsatz

Kompromittierte Systeme werden nicht bereinigt.

Kompromittierte Systeme werden vollständig neu aufgebaut.

### Aufgaben

- Neuinstallation aus Gold Images
- Wiederherstellung aus vertrauenswürdigen Backups
- Integritätsprüfung

### Checkliste

- [ ] Neuinstallation abgeschlossen
- [ ] Integrität geprüft
- [ ] Betrieb getestet
- [ ] Freigabe erfolgt

---

## 5.3 Credential Rotation

### Aufgaben

- Service Accounts zurücksetzen
- Administrator-Konten zurücksetzen
- Zertifikate erneuern
- Pre-Shared Keys ersetzen

### Checkliste

- [ ] Service Accounts erneuert
- [ ] Administrative Konten erneuert
- [ ] Zertifikate erneuert
- [ ] Schlüssel erneuert

---

## 5.4 OT Threat Hunting und IoC-Analyse

### Ziel

Identifikation weiterer kompromittierter Systeme und Persistenzmechanismen.

### Prüfbereiche

- ICS-Malware-Artefakte
- SPS-/PLC-Manipulationen
- Unautorisierte Programmänderungen
- Neue Benutzerkonten
- Neue Service Accounts
- Laterale Bewegungen
- Verdächtige Netzwerkpfade
- Verdächtige Engineering-Aktivitäten

### Checkliste

- [ ] IoCs identifiziert
- [ ] IoCs bewertet
- [ ] IoCs beseitigt
- [ ] Ergebnisse dokumentiert

---

## 5.5 Firmware Integrity Verification

### Aufgaben

- Firmware-Versionen prüfen
- Hersteller-Checksummen prüfen
- Digitale Signaturen prüfen
- Secure-Boot-Konfiguration prüfen

### Checkliste

- [ ] Firmware validiert
- [ ] Signaturen geprüft
- [ ] Checksummen geprüft
- [ ] Secure Boot bewertet

---

## 5.6 Recovery Gate Review

## Ziel

Formelle Freigabe vor Wiederaufnahme des Normalbetriebs.

### Recovery Gate Checklist

- [ ] SPS-/PLC-Logik verifiziert
- [ ] Firmware verifiziert
- [ ] HMI-Systeme validiert
- [ ] SCADA-Systeme validiert
- [ ] Keine aktiven IoCs vorhanden
- [ ] Keine aktive Kompromittierung erkennbar
- [ ] Netzwerkverkehr normalisiert
- [ ] Safety-Freigabe erteilt
- [ ] OT-IC-Freigabe erteilt

### Entscheidung

Erst nach erfolgreichem Recovery Gate Review darf die Recovery-Phase gestartet werden.

---

## Exit-Kriterien Phase 5

- [ ] Kompromittierte Systeme ersetzt oder bereinigt
- [ ] SPS-/PLC-Integrität nachgewiesen
- [ ] Firmware-Integrität nachgewiesen
- [ ] Threat Hunting abgeschlossen
- [ ] Recovery Gate erfolgreich bestanden

---

# Phase 6: Kontrollierter Wiederanlauf (Recovery)

## Ziel

Ziel der Recovery-Phase ist die sichere und kontrollierte Wiederaufnahme des Produktionsbetriebs.

Der Wiederanlauf erfolgt schrittweise und ausschließlich nach erfolgreichem Abschluss des Recovery Gate Reviews.

Die Reihenfolge der Wiederinbetriebnahme darf nicht verändert werden.

---

## Recovery-Prinzipien

### Grundsatz 1

Safety hat Vorrang vor Produktion.

### Grundsatz 2

Jede Ebene wird vollständig validiert, bevor die nächste Ebene aktiviert wird.

### Grundsatz 3

Fehler während des Wiederanlaufs führen zu einem sofortigen Stopp des Recovery-Prozesses.

### Grundsatz 4

Alle Recovery-Schritte werden dokumentiert.

---

## 6.1 Sicherheits- und Hilfssysteme

### Ziel

Sicherstellung der Betriebsfähigkeit aller sicherheitskritischen Komponenten.

### Betroffene Systeme

- Safety Instrumented Systems (SIS)
- Not-Aus-Systeme
- Brandmeldeanlagen
- Löschanlagen
- Kühlsysteme
- Lüftungssysteme
- Druckentlastungssysteme
- Stromversorgungssysteme
- USV-Systeme

### Aktivitäten

- Funktionstests durchführen
- Alarmfunktionen prüfen
- Redundanzen prüfen
- Sensorik prüfen
- Kommunikationspfade prüfen

### Checkliste

- [ ] SIS funktionsfähig
- [ ] Not-Aus-Systeme geprüft
- [ ] Brandmeldeanlage geprüft
- [ ] Löschsysteme geprüft
- [ ] Kühlung verfügbar
- [ ] Lüftung verfügbar
- [ ] Energieversorgung stabil
- [ ] Alle Tests erfolgreich

### Freigabe

Freigabe durch:

- Lead OT Engineer
- Safety-Verantwortliche

---

## 6.2 Feldebene (Level 0 bis Level 2)

### Ziel

Wiederanlauf der Steuerungs- und Automatisierungsebene.

### Betroffene Systeme

- SPS-/PLC-Systeme
- Feldcontroller
- Sensoren
- Aktoren
- Remote I/O Systeme
- Prozessnetzwerke

### Aktivitäten

- Systeme im Inselbetrieb starten
- Kommunikationspfade prüfen
- Input-Signale prüfen
- Output-Signale prüfen
- Steuerungslogik verifizieren

### Checkliste

- [ ] SPS-/PLC-Systeme gestartet
- [ ] Kommunikationspfade verfügbar
- [ ] Eingänge geprüft
- [ ] Ausgänge geprüft
- [ ] Steuerungslogik validiert
- [ ] Keine Fehler festgestellt

### Freigabe

Freigabe durch:

- OT-Engineering
- OT Incident Commander

---

## 6.3 Leit- und Visualisierungsebene (Level 3)

### Ziel

Wiederherstellung der betrieblichen Steuerungs- und Überwachungsfunktionen.

### Betroffene Systeme

- HMI-Systeme
- SCADA-Systeme
- Historian-Systeme
- Alarmserver
- Engineering Workstations

### Aktivitäten

- Systeme starten
- Verbindungen prüfen
- Alarmierungen testen
- Datenhistorisierung prüfen
- Benutzerzugriffe prüfen

### Checkliste

- [ ] HMI-Systeme verfügbar
- [ ] SCADA-Systeme verfügbar
- [ ] Historian-Systeme verfügbar
- [ ] Alarmfunktionen getestet
- [ ] Benutzerzugriffe geprüft
- [ ] Betriebsdaten korrekt

### Freigabe

Freigabe durch:

- OT Engineering
- OT Security

---

## 6.4 Kontrollierte IDMZ-Reintegration (Level 3.5)

### Ziel

Wiederaufnahme kontrollierter Datenflüsse zwischen OT und Enterprise-IT.

### Voraussetzungen

- Recovery Gate erfolgreich abgeschlossen
- Keine aktiven IoCs vorhanden
- Produktionsbetrieb stabil

### Aktivitäten

- Freigegebene Datenflüsse aktivieren
- Firewall-Regeln schrittweise freigeben
- Monitoring verstärken
- Datenverkehr überwachen

### Zulässige Datenflüsse

Beispiele:

- Historian-Replikation
- Produktionsreports
- Monitoringdaten
- Patch-Management-Verbindungen
- Backup-Replikation

### Checkliste

- [ ] Firewall-Regeln aktiviert
- [ ] Datenflüsse überwacht
- [ ] Keine Anomalien festgestellt
- [ ] Monitoring aktiv
- [ ] IT-OT-Kommunikation validiert

### Freigabe

Freigabe durch:

- OT Incident Commander
- IT Security Lead

---

## 6.5 Hypercare-Phase

### Dauer

Empfohlen: 72 Stunden bis 14 Tage

### Ziel

Früherkennung verbliebener Probleme nach Wiederanlauf.

### Aktivitäten

- Erhöhtes Monitoring
- Tägliche Lagebesprechungen
- Zusätzliche Threat-Hunting-Aktivitäten
- Überprüfung von Alarmen
- Review aller Security Events

### Checkliste

- [ ] Monitoring erhöht
- [ ] Daily Reviews etabliert
- [ ] Keine Anomalien festgestellt
- [ ] Produktionsbetrieb stabil

---

## Exit-Kriterien Phase 6

- [ ] Produktion wiederhergestellt
- [ ] Safety-Systeme stabil
- [ ] OT-Systeme stabil
- [ ] IDMZ-Verbindungen kontrolliert aktiviert
- [ ] Hypercare erfolgreich abgeschlossen
- [ ] Übergabe in Regelbetrieb erfolgt

---

# Phase 7: Regulatorische Meldungen und Krisenkommunikation

## Ziel

Einhaltung aller regulatorischen Meldepflichten sowie Sicherstellung einer konsistenten internen und externen Kommunikation.

---

## 7.1 Erstbewertung der Meldepflicht

### Verantwortlich

- Compliance
- Legal
- OT Incident Commander

### Prüfkriterien

- Kritische Infrastruktur betroffen
- Wesentliche Einrichtung nach NIS2 betroffen
- Produktionsausfall
- Gefährdung von Personen
- Grenzüberschreitende Auswirkungen
- Verdacht auf vorsätzliches Handeln
- Datenschutzrelevante Auswirkungen

### Checkliste

- [ ] Meldepflicht bewertet
- [ ] Rechtsabteilung eingebunden
- [ ] Dokumentation gestartet

---

## 7.2 Frühwarnung innerhalb von 24 Stunden

### Ziel

Erfüllung der gesetzlichen Frühwarnpflicht.

### Inhalte

- Zeitpunkt der Feststellung
- Erste Einschätzung des Vorfalls
- Verdacht auf vorsätzliches Handeln
- Mögliche grenzüberschreitende Auswirkungen
- Betroffene Geschäftsprozesse

### Checkliste

- [ ] Frühwarnung erstellt
- [ ] Freigabe erfolgt
- [ ] Meldung versendet
- [ ] Nachweis archiviert

---

## 7.3 Incident-Meldung innerhalb von 72 Stunden

### Ziel

Bereitstellung einer ersten qualifizierten Bewertung.

### Inhalte

- Schweregrad des Vorfalls
- Betroffene Systeme
- Vorläufige Ursachenanalyse
- Indikatoren einer Kompromittierung (IoCs)
- Eingeleitete Gegenmaßnahmen
- Erste Bewertung möglicher Auswirkungen

### Checkliste

- [ ] Incident-Meldung erstellt
- [ ] IoCs dokumentiert
- [ ] Maßnahmen dokumentiert
- [ ] Meldung übermittelt

---

## 7.4 Fortschrittsbericht

### Voraussetzung

Der Vorfall ist nach Ablauf der Erstmeldungsphase noch nicht abgeschlossen.

### Inhalte

- Aktueller Bearbeitungsstand
- Zusätzliche Erkenntnisse
- Aktualisierte Risikobewertung
- Weitere Maßnahmen

### Checkliste

- [ ] Bericht erstellt
- [ ] Bericht freigegeben
- [ ] Bericht übermittelt

---

## 7.5 Abschlussbericht innerhalb eines Monats

### Ziel

Formeller Abschluss der regulatorischen Meldepflichten.

### Inhalte

- Root Cause Analysis
- Angriffspfad
- Betroffene Systeme
- Eingetretene Auswirkungen
- Ergriffene Gegenmaßnahmen
- Geplante Verbesserungsmaßnahmen
- Finale Risikobewertung

### Checkliste

- [ ] Root Cause Analysis abgeschlossen
- [ ] Abschlussbericht erstellt
- [ ] Bericht freigegeben
- [ ] Bericht versendet
- [ ] Nachweis archiviert

---

## 7.6 Interne Krisenkommunikation

### Ziel

Vermeidung widersprüchlicher Informationen während des Vorfalls.

### Anforderungen

- Ein zentraler Kommunikationskanal
- Einheitliche Lageberichte
- Definierte Freigabeprozesse
- Dokumentierte Kommunikationshistorie

### Checkliste

- [ ] Kommunikationsverantwortliche benannt
- [ ] Lageberichte etabliert
- [ ] Kommunikationsprotokoll vorhanden

---

## 7.7 Externe Kommunikation

### Ziel

Konsistente Kommunikation gegenüber Öffentlichkeit, Kunden, Partnern und Behörden.

### Verantwortlich

- Unternehmenskommunikation
- Pressestelle
- Legal
- Executive Crisis Team

### Anforderungen

- Nur freigegebene Informationen kommunizieren
- Spekulationen vermeiden
- Rechtskonforme Kommunikation sicherstellen
- Einheitliche Botschaften verwenden

### Checkliste

- [ ] Freigabeprozess definiert
- [ ] Kommunikationsverantwortliche benannt
- [ ] Externe Statements geprüft

---

## Exit-Kriterien Phase 7

- [ ] Meldepflichten erfüllt
- [ ] Nachweise archiviert
- [ ] Behördenkommunikation abgeschlossen
- [ ] Interne Kommunikation abgeschlossen
- [ ] Externe Kommunikation abgeschlossen

---

# Phase 8: Post-Incident Review und Continuous Improvement

## Ziel

Ziel dieser Phase ist die nachhaltige Verbesserung der OT-Cyber-Resilienz durch strukturierte Nachbereitung des Vorfalls.

Jeder OT-Sicherheitsvorfall wird als Lernereignis behandelt.

---

## 8.1 Root Cause Analysis

### Ziel

Ermittlung der tatsächlichen Ursache des Vorfalls.

### Untersuchungsbereiche

- Initialer Angriffsvektor
- Betroffene Systeme
- Ausgenutzte Schwachstellen
- Angreiferaktivitäten
- Auswirkungen auf Produktion und Betrieb
- Auswirkungen auf Safety-Systeme

### Checkliste

- [ ] Initialer Angriffsvektor identifiziert
- [ ] Ursache dokumentiert
- [ ] Auswirkungen erfasst
- [ ] Abschlussbewertung erstellt

---

## 8.2 Incident Timeline

### Ziel

Vollständige Rekonstruktion des Vorfalls.

### Dokumentation

- Zeitpunkt der ersten Erkennung
- Zeitpunkt der Eskalation
- Zeitpunkt der Eindämmung
- Zeitpunkt der Recovery-Maßnahmen
- Zeitpunkt der Wiederherstellung
- Zeitpunkt der Meldungen

### Checkliste

- [ ] Vollständige Timeline erstellt
- [ ] Ereignisse validiert
- [ ] Zeitleiste archiviert

---

## 8.3 Control Gap Assessment

### Ziel

Identifikation von Sicherheitslücken und organisatorischen Schwächen.

### Untersuchungsbereiche

- Netzwerksegmentierung
- Zugriffskontrollen
- Monitoring
- Asset Management
- Backup und Recovery
- Logging
- Alarmierung
- Lieferantenmanagement

### Checkliste

- [ ] Sicherheitslücken identifiziert
- [ ] Risiken bewertet
- [ ] Prioritäten festgelegt

---

## 8.4 Verbesserungsmaßnahmen

### Ziel

Definition und Umsetzung konkreter Verbesserungen.

### Maßnahmenbeispiele

- Zusätzliche Netzwerksegmentierung
- Verbesserte Zugriffskontrollen
- Erweiterte Überwachung
- Härtung kritischer Systeme
- Optimierung von Backup-Prozessen
- Verbesserung der Recovery-Verfahren

### Checkliste

- [ ] Maßnahmen definiert
- [ ] Verantwortliche benannt
- [ ] Umsetzungsfristen 

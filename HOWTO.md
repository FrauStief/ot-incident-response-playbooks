# Industrial Cyber Blueprints

> Offene Sammlung von Sicherheitshandbüchern für die Betriebstechnik (OT), Plänen zur Reaktion auf Vorfälle, Runbooks zur Wiederherstellung, Verfahren zur Reaktion auf Ransomware, Checklisten und Governance-Vorlagen für industrielle Umgebungen.

Basierend auf etablierten Branchenpraktiken und Leitlinien aus:

- NIST SP 800-82
- IEC 62443
- Purdue Enterprise Reference Architecture
- BSI-Leitfaden zur ICS-Sicherheit
- NIS2-Anforderungen zur Meldung von Vorfällen

---

## Überblick

Industrielle Umgebungen erfordern einen anderen Ansatz in Bezug auf Sicherheit und Vorfallreaktion als herkömmliche IT-Umgebungen.

In der Betriebstechnik (OT) ist das vorrangige Ziel nicht der Schutz von Daten, sondern der Schutz von Menschen, industriellen Prozessen und physischen Anlagen.

Dieses Repository bietet praktische, praxisorientierte Dokumentation für:

- Fertigung
- Industrielle Steuerungssysteme (ICS)
- Kritische Infrastruktur (KRITIS)
- Energie
- Versorgungsunternehmen
- Wasser- und Abwasserwirtschaft
- Chemiewerke
- Pharmazeutische Produktion
- Gebäudeautomation
- Industrieller Betrieb

---

## Kernprinzip

```text
SICHERHEIT > VERFÜGBARKEIT > VERTRAULICHKEIT
```

Die Sicherheit von Menschen und die physische Prozessintegrität haben Vorrang vor allen Maßnahmen zur Reaktion auf Cybervorfälle.

---

# Struktur des Repositorys

```text
industrial-cyber-blueprints
│
├── ot-incident-response-plan-v3.md
├── ot-incident-response-runbook.md
├── ot-management-summary.md
│
├── HOWTO.md
│
├── LICENSE
└── README.md

```

---

# Enthaltene Dokumente

## 1. OT-Incident-Response-Plan (OT-IRP)

**Datei**

```text
ot-incident-response-plan-v3.md
```

Umfassendes OT-Handbuch zur Reaktion auf Vorfälle, einschließlich:

- Vorbereitung und Bereitschaft
- Anlagenmanagement
- Bereitschaft der Datensicherung
- Klassifizierung von Vorfällen
- Reaktion auf OT-Ransomware
- Eindämmungsmaßnahmen
- Bedrohungssuche
- Wiederherstellungsschritte
- Kontrollierte Wiederherstellung
- Meldungen an Aufsichtsbehörden
- Gewonnene Erkenntnisse
- Checklisten und Anhänge

Zielgruppe:

- OT-Sicherheitsteams
- Werksleiter
- OT-Ingenieure
- Incident-Responder
- Betreiber kritischer Infrastrukturen

---

## 2. OT-Runbook für die Reaktion auf Vorfälle

**Datei**

```text
ot-incident-response-runbook.md
```

Checkliste für Betriebsvorfälle, die für den Einsatz während aktiver Vorfälle konzipiert ist.

Enthält:

- Maßnahmen in den ersten 15 Minuten
- Eindämmungsaufgaben
- Wiederherstellungsaufgaben
- Aufgaben zur behördlichen Berichterstattung
- Aufgaben zum Abschluss des Vorfalls

Zielgruppe:

- OT-Einsatzleiter
- Schichtleiter
- Krisenmanagementteams
- SOC-Analysten
- Einsatzkräfte bei Vorfällen

---

## 3. Zusammenfassung für die Geschäftsleitung

**Datei**

```text
ot-management-summary.md
```

Überblick auf Führungsebene über das OT-Rahmenwerk zur Reaktion auf Vorfälle.

Enthält:

- Überblick über die Governance
- Eskalationsstufen
- Verantwortlichkeiten der Führungskräfte
- Überblick über die NIS2-Berichterstattung
- Eskalationspfad bei Ransomware
- Wiederherstellungsstrategie
- Management-KPIs

Zielgruppe:

- CIOs
- CISOs
- CTOs
- Werksleiter
- Vorstandsmitglieder
- Krisenmanagement-Teams

---

# Verwendungszweck

Diese Dokumente sind als Referenzvorlagen konzipiert.

Unternehmen sollten sie anpassen an:

- Lokale Vorschriften
- Interne Governance-Anforderungen
- Industrielle Prozesse
- OT-Architekturen
- Sicherheitsanforderungen
- Bestehende Verfahren zur Reaktion auf Vorfälle

---

# Empfohlene Anpassung an Standards

Das Repository soll die Anpassung an folgende Standards unterstützen:

- NIST SP 800-82
- IEC 62443
- NIS2
- BSI-Leitfaden für ICS
- Purdue-Modell
- Best Practices für industrielle Cybersicherheit

---

# Beiträge

Beiträge, Korrekturen, Verbesserungen und branchenspezifische Anpassungen sind willkommen.

Vorgeschlagene Bereiche für Beiträge:

- Zusätzliche OT-Playbooks
- Branchenspezifische Runbooks
- Vorlagen für die Meldung von Vorfällen
- Wiederherstellungsverfahren
- Leitlinien für sicherheitsrelevante Reaktionen
- Inhalte zur Erkennungstechnik
- Verfahren zur OT-Bedrohungssuche

---

# Lizenz

Dieses Projekt wird unter der BSD Zero Clause License (0BSD) veröffentlicht.

Sie dürfen:

- das Material nutzen
- es ändern
- verbreiten
- veröffentlichen
- kommerziell verwerten

das Material ohne Einschränkungen.

Einzelheiten finden Sie in der Datei `LICENSE`.

---

# Sicherheitshinweis

Das Material in diesem Repository wird als Referenzdokumentation bereitgestellt.

Organisationen sind weiterhin dafür verantwortlich, Folgendes zu überprüfen:

- Betriebsanforderungen
- behördliche Anforderungen
- Sicherheitsanforderungen
- Rechtliche Verpflichtungen

, bevor Sie Verfahren in Produktionsumgebungen anwenden.

Legen Sie stets größten Wert auf den Schutz von:

1. Menschen
2. Umwelt
3. Physischen Vermögenswerten
4. Produktionsabläufen
5. Informationsressourcen

---

# Haftungsausschluss

DAS MATERIAL WIRD „WIE BESEHEN“ OHNE JEGLICHE GEWÄHRLEISTUNG BEREITGESTELLT.

Die Autoren übernehmen keine Haftung für Schäden, Verluste, Vorfälle, Ausfälle, Auswirkungen auf den Produktionsbetrieb oder regulatorische Konsequenzen, die sich aus der Nutzung dieses Repositorys ergeben.

Die Nutzung erfolgt auf eigene Gefahr.

---

# Betreuer

Industrial Cyber Blueprints Community

Version: 1.0

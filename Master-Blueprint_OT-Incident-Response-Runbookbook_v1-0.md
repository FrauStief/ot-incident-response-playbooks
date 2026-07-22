# Anhang 0: OT Incident Response Master Runlist

## Incident-Erkennung

### Erste 15 Minuten

- [ ] Vorfall erkannt und dokumentiert
- [ ] OT Incident Commander informiert
- [ ] Physische Prozesssicherheit bewertet
- [ ] SIS-Systeme geprüft
- [ ] Incident-Stufe festgelegt
- [ ] Incident-Ticket eröffnet
- [ ] OT-IRT aktiviert
- [ ] Out-of-Band-Kommunikation aktiviert

---

## Incident-Klassifizierung

### Stufe 1

- [ ] Dokumentieren
- [ ] Monitoring erhöhen
- [ ] Ursachenanalyse durchführen

### Stufe 2

- [ ] OT-IRT aktivieren
- [ ] Management informieren
- [ ] Forensik starten
- [ ] Segmentierung prüfen

### Stufe 3

- [ ] Krisenmodus aktivieren
- [ ] Executive Crisis Team informieren
- [ ] Notfallverfahren aktivieren
- [ ] Regulatorische Bewertung starten

---

## OT-Ransomware-Sonderfall

Wenn betroffen:

- [ ] Engineering Workstations
- [ ] Historian
- [ ] SCADA
- [ ] APC-Systeme
- [ ] OT-Dateiserver
- [ ] OT-Domänencontroller

Sofortmaßnahmen:

- [ ] OT von IT trennen
- [ ] Keine Neustarts durchführen
- [ ] Remote Access deaktivieren
- [ ] Beweissicherung starten
- [ ] Executive Crisis Team aktivieren
- [ ] BSI-/NIS2-Meldepflicht prüfen

---

## Eindämmung (Containment)

### Netzwerk

- [ ] Air-Gap-on-Demand aktiviert
- [ ] IDMZ isoliert
- [ ] Firewall-Notfallregeln aktiviert
- [ ] Netzwerksegmentierung überprüft

### Zugriffe

- [ ] VPN deaktiviert
- [ ] Jump Hosts deaktiviert
- [ ] Drittanbieterzugänge entfernt
- [ ] Administrative Konten geprüft

### Monitoring

- [ ] TAP-Monitoring aktiviert
- [ ] SPAN-Monitoring aktiviert
- [ ] PCAP-Aufzeichnung gestartet
- [ ] Log-Sicherung gestartet

---

## Forensik & Analyse

### Beweissicherung

- [ ] Logs gesichert
- [ ] Speicherabbilder gesichert
- [ ] PCAP-Dateien gesichert
- [ ] Timeline gestartet

### Threat Hunting

- [ ] IoCs gesammelt
- [ ] Laterale Bewegungen untersucht
- [ ] Neue Benutzerkonten geprüft
- [ ] Verdächtige Engineering-Aktivitäten geprüft
- [ ] Persistenzmechanismen gesucht

---

## Integritätsprüfung

### SPS / PLC

- [ ] SPS-Programme exportiert
- [ ] Vergleich mit Gold-Master durchgeführt
- [ ] Hashwerte geprüft
- [ ] Abweichungen dokumentiert

### Firmware

- [ ] Firmware-Versionen geprüft
- [ ] Signaturen geprüft
- [ ] Checksummen geprüft
- [ ] Secure Boot geprüft

### HMI / SCADA

- [ ] Systeme neu installiert
- [ ] Gold Images verwendet
- [ ] Integrität geprüft

---

## Credential Rotation

- [ ] Service Accounts zurückgesetzt
- [ ] Administrator-Konten zurückgesetzt
- [ ] Zertifikate erneuert
- [ ] Pre-Shared Keys ersetzt

---

## Recovery Gate

Vor Wiederanlauf:

- [ ] SPS-/PLC-Logik verifiziert
- [ ] Firmware verifiziert
- [ ] HMI-Systeme geprüft
- [ ] SCADA-Systeme geprüft
- [ ] Keine aktiven IoCs vorhanden
- [ ] Netzwerkverkehr normalisiert
- [ ] Safety-Freigabe erfolgt
- [ ] OT-IC-Freigabe erfolgt

---

## Recovery

### Schritt 1

- [ ] Safety-Systeme gestartet
- [ ] Kühlung geprüft
- [ ] Lüftung geprüft
- [ ] Not-Aus getestet

### Schritt 2

- [ ] SPS-/PLC-Ebene gestartet
- [ ] Sensoren getestet
- [ ] Aktoren getestet

### Schritt 3

- [ ] HMI gestartet
- [ ] SCADA gestartet
- [ ] Historian gestartet

### Schritt 4

- [ ] IDMZ-Verbindungen aktiviert
- [ ] Datenflüsse überwacht
- [ ] Anomalien ausgeschlossen

---

## Regulatorische Anforderungen

### Innerhalb 24 Stunden

- [ ] Frühwarnung erstellt
- [ ] Rechtsabteilung eingebunden
- [ ] Meldung versendet

### Innerhalb 72 Stunden

- [ ] Incident-Bericht erstellt
- [ ] IoCs dokumentiert
- [ ] Maßnahmen dokumentiert

### Innerhalb 1 Monat

- [ ] Root Cause Analysis abgeschlossen
- [ ] Abschlussbericht erstellt
- [ ] Bericht eingereicht

---

## Post Incident Review

- [ ] Root Cause Analysis abgeschlossen
- [ ] Incident Timeline erstellt
- [ ] Lessons Learned dokumentiert
- [ ] Control Gap Assessment durchgeführt
- [ ] Verbesserungsmaßnahmen definiert
- [ ] Detection Rules aktualisiert
- [ ] Playbook aktualisiert

---

## Incident Closure

Vor formeller Schließung:

- [ ] Produktion stabil
- [ ] Safety-Systeme stabil
- [ ] Management informiert
- [ ] Dokumentation abgeschlossen
- [ ] Regulatorische Vorgaben erfüllt
- [ ] Maßnahmenplan verabschiedet
- [ ] Incident offiziell geschlossen
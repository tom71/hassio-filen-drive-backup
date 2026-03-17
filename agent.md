Hier ist ein Vorschlag für eine `Agent.md`-Datei, welche die Kernpunkte und Pläne für dein Projekt zusammenfasst. Diese Datei dient als erste Orientierung und lässt sich bei Bedarf erweitern.

```markdown
# Home Assistant Encrypted Backup Add-on

## Projektbeschreibung

Dieses Add-on soll automatisierte, verschlüsselte Backups für Home Assistant ermöglichen, die sicher auf einem externen Speicheranbieter (z. B. Filen.io) abgelegt werden. Es bietet Funktionen zur Verwaltung der Backups, einschließlich regelmäßiger Löschvorgänge und Warnungen bei Erreichen von Speicherlimits. Zusätzlich sollen Wiederherstellungen (Restore) nahtlos über das Add-on durchgeführt werden können.

---

## Features

- **Verschlüsselte Backups:**
  - Alle Backups werden vor dem Hochladen verschlüsselt gespeichert.
- **Integration mit Filen.io SDK:**
  - Nutzung des Filen.io SDK für die Speicher- und Datenverwaltung.
- **Regelmäßiges Backup:**
  - Automatisierte Erstellung von Backups basierend auf einstellbaren Zeitplänen.
- **Aufbewahrungsfristen:**
  - Definierte Regeln, um alte Backups automatisch zu löschen.
- **Wiederherstellungen:**
  - Intuitive Wiederherstellung der Daten direkt über das Add-on.
- **Speicherverwaltung:**
  - Warnungen bei Annäherung an das verfügbare Speicherlimit.
- **Einfache Konfiguration:**
  - Alle Optionen über die Benutzeroberfläche von Home Assistant konfigurierbar.

---

## Technischer Stack

- **Programmiersprache:** TypeScript
- **Plattform:** Home Assistant Add-on
- **Speicheranbieter:** Filen.io (SDK-Integration)
- **Verschlüsselung:** AES-256 oder vergleichbar
- **Task-Management:** Cron oder Node-Scheduler für geplante Tasks
- **Dateiformat:** `.tar.gz` Kombination für Kompression + Verschlüsselung

---

## Ziele

### MVP (Minimum Viable Product)

1. Einrichtung des Add-ons als Home Assistant-Erweiterung.
2. Anbindung von Filen.io SDK für Datei-Uploads und -Downloads.
3. Manuelles Erstellen eines verschlüsselten Backups und Hochladen auf Filen.io.
4. Dokumentation für Benutzer zur einfachen Einrichtung.

### Erweiterte Funktionen

1. Automatisierung:
   - Zeitplan für regelmäßige Backups.
2. Speicherverwaltung:
   - Automatisches Löschen älterer Backups basierend auf Aufbewahrungsrichtlinien.
   - Warnungen bei Speicherüberschreitung.
3. Benutzeroberfläche:
   - Einstellungsmöglichkeiten direkt in der Home Assistant GUI.
   - Auswahl von Ordnern oder Komponenten für Backups.
4. Restore-Prozess:
   - Zum Downloaden und Wiederherstellen in Home Assistant.

---

## Projektstruktur

```
homeassistant-backup-addon/
├── src/
│   ├── services/                # Dienste für Filen.io Kommunikation und Verschlüsselung
│   └── schedulers/              # Backup- und Lösch-Zeitpläne
├── config/
│   └── config.json              # Benutzerkonfigurations-Template
├── docs/
│   └── Agent.md                 # Projektbeschreibung und Ziele
├── Dockerfile                   # Basis für Home Assistant Add-on
└── README.md                    # Hauptdokumentation für das GitHub-Repo
```

---

## Anforderungen

- **Home Assistant Entwicklungsumgebung:**
  - Add-on Erstellung muss Home Assistant Add-on Standards und Testing-Frameworks erfüllen.
- **Installation der Abhängigkeiten:**
  - Filen.io SDK
  - Verschlüsselungsbibliothek (z. B. `crypto` in Node.js)
- **Speicherplatzverwaltung:**
  - API-Call zur Überprüfung des belegten und verbleibenden Speicherplatzes.

---

## Erste Schritte: Roadmap

### Phase 1: Projektsetup
- [ ] Repository erstellen.
- [ ] Grundstruktur des Add-ons entwickeln (Docker-Setup, TypeScript-Projekt starten).
- [ ] Filen.io SDK integrieren.

### Phase 2: Backup-Logik
- [ ] Verschlüsseln und Hochladen eines Test-Backups.
- [ ] Wiederherstellungsprozess implementieren.

### Phase 3: Automation Feature
- [ ] Backup-Zeitplan hinzufügen.
- [ ] Automatische Speicher- und Aufbewahrungsverwaltung.

### Phase 4: GUI und Benutzerfreundlichkeit
- [ ] GUI-Integration in Home Assistant.
- [ ] Benutzerfreundliches Warnsystem (z. B. bei vollem Speicher).

---

## Lizenz

Dieses Projekt wird unter der MIT-Lizenz veröffentlicht. Drittanbieter-Bibliotheken (wie das Filen.io SDK) unterliegen ihren eigenen Lizenzbedingungen.

---

## Ansprechpartner

- **Projektleitung:** [GitHub Profil von tom71](https://github.com/tom71)
- **Feedback und Beiträge:** Contributions via Pull Request sind willkommen!

```

Mit dieser Datei hast du einen soliden Plan und kannst mit der Umsetzung des Projekts beginnen. Diese Datei könnte in ein GitHub-Repository mit dem Projekt aufgenommen werden. Soll ich dir bei einem bestimmten Teil wie dem Einrichten der Projektstruktur oder Docker-Konfiguration helfen?
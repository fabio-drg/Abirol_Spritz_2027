# 📄 Einfache PDF-Verwaltung - Anleitung

## ✅ So einfach geht's - OHNE Code-Änderung!

Sie müssen **NIE WIEDER** die `index.html` bearbeiten! Alle PDFs werden jetzt automatisch aus der Datei `pdfs/documents.json` geladen.

---

## 🚀 Neues PDF hinzufügen (3 Schritte):

### Schritt 1: PDF hochladen
Legen Sie Ihre PDF-Datei in den Ordner `pdfs/`

**Beispiel:** `pdfs/mein-neues-dokument.pdf`

### Schritt 2: JSON-Datei öffnen
Öffnen Sie die Datei: `pdfs/documents.json`

### Schritt 3: Eintrag hinzufügen
Fügen Sie Ihr PDF zum JSON-Array hinzu:

```json
[
    {
        "title": "Protokoll 28.01.26 Erste Austauschversammlung mit Eltern",
        "description": "Wichtige Informationen für Eltern",
        "file": "Protokoll 28.01.26.pdf",
        "date": "2026-02-03",
        "size": "137 KB",
        "icon": "📋"
    },
    
    // IHR NEUES PDF HIER HINZUFÜGEN:
    {
        "title": "Mein neues Dokument",
        "description": "Kurze Beschreibung des Inhalts",
        "file": "pdfs/mein-neues-dokument.pdf",
        "date": "2026-02-15",
        "size": "1.5 MB",
        "icon": "📄"
    }
]
```

**WICHTIG:** 
- Vergessen Sie nicht das **Komma** nach dem vorherigen Eintrag!
- Das letzte Element im Array braucht **kein** Komma

---

## 📝 Felder Erklärung:

| Feld | Beschreibung | Beispiel |
|------|--------------|----------|
| `title` | Titel des Dokuments | `"Protokoll 28.01.26 Erste Austauschversammlung mit Eltern"` |
| `description` | Kurze Beschreibung | `"Wichtige Informationen für Eltern"` |
| `file` | Pfad zur PDF-Datei | `"Protokoll 28.01.26.pdf"` |
| `date` | Datum (YYYY-MM-DD) | `"2026-02-03"` |
| `size` | Dateigröße | `"137 KB"` |
| `icon` | Emoji-Symbol | `"📋"` |

---

## 🎨 Verfügbare Icons (Emojis):

Wählen Sie ein passendes Icon:

- 📋 Standard Dokument
- 📄 Formular  
- 💰 Finanzen
- 👕 Abipulli
- 📸 Fotos
- 📅 Termine
- ✉️ Brief/Info
- 🎓 Abitur
- 🎉 Events
- 📊 Berichte
- 🎟️ Tickets
- 🍰 Kuchenverkauf

---

## ✏️ Vollständiges Beispiel:

```json
[
    {
        "title": "Protokoll 28.01.26 Erste Austauschversammlung mit Eltern",
        "description": "Wichtige Informationen für Eltern",
        "file": "Protokoll 28.01.26.pdf",
        "date": "2026-02-03",
        "size": "137 KB",
        "icon": "📋"
    },
    {
        "title": "Ihr zweites Dokument",
        "description": "Beschreibung hinzufügen",
        "file": "pdfs/dokument-2.pdf",
        "date": "2026-02-10",
        "size": "200 KB",
        "icon": "📄"
    }
]
```

---

## 🗑️ PDF löschen:

1. Öffnen Sie `pdfs/documents.json`
2. Löschen Sie den kompletten Eintrag (inkl. `{ ... }`)
3. Achten Sie auf korrekte Kommas!
4. Speichern

---

## ⚠️ Häufige Fehler vermeiden:

### ❌ FALSCH - Fehlendes Komma:
```json
[
    {
        "title": "Dokument 1",
        ...
    }  // ← FEHLT KOMMA
    {
        "title": "Dokument 2",
        ...
    }
]
```

### ✅ RICHTIG:
```json
[
    {
        "title": "Dokument 1",
        ...
    },  // ← MIT KOMMA
    {
        "title": "Dokument 2",
        ...
    }
]
```

---

## 🔍 Tipps:

- **Dateinamen:** Verwenden Sie klare, beschreibende Namen
  - ✅ `Protokoll 28.01.26.pdf`
  - ❌ `Dokument1.pdf`

- **Datum:** Neueste Dokumente werden oben angezeigt

- **Größe:** Dateigröße können Sie mit Rechtsklick → Eigenschaften sehen

- **JSON-Syntax prüfen:** Falls etwas nicht funktioniert, prüfen Sie auf [jsonlint.com](https://jsonlint.com/)

---

## 🆘 Probleme?

**PDFs werden nicht angezeigt?**
1. Prüfen Sie die Browser-Konsole (F12)
2. Kontrollieren Sie die JSON-Syntax
3. Stellen Sie sicher, dass die PDF im `pdfs/` Ordner liegt

**Bei Fragen:** f.dragano@emagym.de

---

## 🎉 Fertig!

Jetzt einfach:
1. `pdfs/documents.json` bearbeiten
2. Speichern
3. Hochladen/Pushen
4. **Fertig!** Die Website aktualisiert sich automatisch

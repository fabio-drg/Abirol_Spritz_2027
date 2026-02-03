# 📄 PDF-Upload Anleitung für Abirol Spritz 2027

## So fügen Sie neue PDFs zur Website hinzu:

### Schritt 1: PDF vorbereiten
1. Benennen Sie Ihre PDF-Datei sinnvoll (z.B. `elternbrief-februar.pdf`)
2. Verwenden Sie **keine Leerzeichen** im Dateinamen (nutzen Sie stattdessen `-` oder `_`)
3. Beispiele für gute Dateinamen:
   - ✅ `abipulli-bestellung-2026.pdf`
   - ✅ `finanzuebersicht-januar.pdf`
   - ✅ `elterninfo-abiball.pdf`
   - ❌ `Dokument mit Leerzeichen.pdf`

### Schritt 2: PDF hochladen
1. Öffnen Sie den Ordner `pdfs/` in Ihrem Projekt
2. Kopieren Sie Ihre PDF-Datei in diesen Ordner
3. Achten Sie darauf, dass die Datei im richtigen Verzeichnis liegt

### Schritt 3: PDF zur Website hinzufügen
1. Öffnen Sie die Datei `index.html`
2. Suchen Sie nach dem Abschnitt mit `newsDocuments` (ca. Zeile 1420)
3. Fügen Sie Ihr PDF zum Array hinzu:

```javascript
const newsDocuments = [
    // Bestehende PDFs...
    
    // IHR NEUES PDF:
    {
        title: 'Elternbrief Februar',              // Titel (wird angezeigt)
        description: 'Infos zum Abiball',          // Kurzbeschreibung
        file: 'pdfs/elternbrief-februar.pdf',      // Pfad zur Datei
        date: '2026-02-15',                         // Datum (YYYY-MM-DD)
        size: '1.5 MB',                             // Dateigröße
        icon: '✉️'                                  // Emoji Icon
    },
];
```

### Schritt 4: Speichern und veröffentlichen
1. Speichern Sie die `index.html`
2. Committen Sie die Änderungen:
   ```bash
   git add .
   git commit -m "PDF hinzugefügt: Elternbrief Februar"
   git push
   ```
3. Die Website aktualisiert sich automatisch (bei GitHub Pages)

## 📋 Verfügbare Icons (Emoji)
Wählen Sie ein passendes Icon für Ihr Dokument:

- 📋 Standard Dokument
- 📄 Formular
- 💰 Finanzen
- 👕 Abipulli
- 📸 Fotos/Bilder
- 📅 Termine/Events
- ✉️ Brief/Info
- 🎓 Abitur-bezogen
- 🎉 Events/Feiern
- 📊 Berichte/Statistiken

## ⚠️ Wichtige Hinweise

### Dateigröße
- Versuchen Sie PDFs unter 5 MB zu halten
- Große Dateien können langsam laden
- Bei Bedarf PDFs komprimieren: https://www.ilovepdf.com/compress_pdf

### Dateinamen
- Keine Umlaute (ä, ö, ü) → verwenden Sie ae, oe, ue
- Keine Sonderzeichen außer `-` und `_`
- Kleinbuchstaben bevorzugt
- Beschreibend benennen

### Datum
- Format: `YYYY-MM-DD` (z.B. `2026-02-15`)
- Neueste Dokumente werden oben angezeigt
- Das Datum wird automatisch formatiert angezeigt

## 📝 Beispiel: Vollständiger Ablauf

Sie möchten einen Elternbrief hochladen:

1. **PDF erstellen:** `elternbrief-februar-2026.pdf`
2. **Hochladen:** Datei in den `pdfs/` Ordner kopieren
3. **Eintrag erstellen in index.html:**
   ```javascript
   {
       title: 'Elternbrief Februar 2026',
       description: 'Wichtige Informationen zum Abiball und Ablauf',
       file: 'pdfs/elternbrief-februar-2026.pdf',
       date: '2026-02-15',
       size: '1.2 MB',
       icon: '✉️'
   },
   ```
4. **Speichern, committen, pushen**
5. **Fertig!** Das PDF erscheint automatisch auf der News-Seite

## 🆘 Probleme?

**PDF wird nicht angezeigt?**
- Prüfen Sie den Dateipfad (muss exakt stimmen)
- Kontrollieren Sie die Kommasetzung im Array
- Schauen Sie in die Browser-Konsole (F12) nach Fehlern

**Download funktioniert nicht?**
- Stellen Sie sicher, dass die PDF im `pdfs/` Ordner liegt
- Überprüfen Sie die Schreibweise des Dateinamens

Bei weiteren Fragen: f.dragano@emagym.de

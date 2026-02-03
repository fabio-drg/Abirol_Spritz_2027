# PDF Dokumente

## Wie man neue PDFs hinzufügt:

1. **PDF in diesen Ordner hochladen**
   - Legen Sie Ihre PDF-Datei in den Ordner `pdfs/`

2. **index.html aktualisieren**
   - Öffnen Sie `index.html`
   - Suchen Sie nach dem Array `newsDocuments`
   - Fügen Sie Ihr PDF hinzu:

```javascript
const newsDocuments = [
    {
        title: 'Ihr Dokumentname',
        description: 'Kurze Beschreibung',
        file: 'pdfs/IhreDatei.pdf',
        date: '2026-02-03',  // Format: YYYY-MM-DD
        size: '1.5 MB',
        icon: '📋'  // Emoji Icon
    },
    // Weitere Dokumente...
];
```

3. **Speichern und hochladen**
   - Speichern Sie die Änderungen
   - Pushen Sie zu GitHub

Die Website zeigt das PDF dann automatisch an!

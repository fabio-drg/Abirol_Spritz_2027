# 📱 Social Media Posts - Anleitung

## ✅ So fügen Sie neue Posts hinzu (in 30 Sekunden!)

### Wann Sie dies tun:
**Immer wenn Sie etwas auf Instagram/TikTok posten!**

### Schritt 1: Post auf Instagram/TikTok veröffentlichen
Posten Sie wie gewohnt auf Ihren Accounts

### Schritt 2: Link zum Post kopieren
- **Instagram:** Öffnen Sie den Post → Drei Punkte → "Link kopieren"
- **TikTok:** Öffnen Sie das Video → "Teilen" → "Link kopieren"

### Schritt 3: `social-posts.json` öffnen
Öffnen Sie die Datei im Repository

### Schritt 4: Neuen Eintrag OBEN hinzufügen
Fügen Sie den neuen Post **ganz oben** im Array ein:

```json
[
    {
        "platform": "instagram",
        "title": "Titel des Posts",
        "description": "Kurze Beschreibung was im Post zu sehen ist",
        "link": "https://www.instagram.com/p/HIER-POST-ID",
        "timestamp": "2026-02-03T14:30:00",
        "icon": "📸"
    },
    
    // Ältere Posts bleiben darunter...
]
```

---

## 📝 Felder erklärt:

| Feld | Wert | Beispiel |
|------|------|----------|
| `platform` | `"instagram"` oder `"tiktok"` | `"instagram"` |
| `title` | Titel/Überschrift (optional) | `"Mottowoche Tag 1"` |
| `description` | Was ist zu sehen? | `"Die besten Momente vom Pyjama-Tag!"` |
| `link` | Kopierter Link vom Post | `"https://www.instagram.com/p/ABC123"` |
| `timestamp` | Aktuelles Datum/Zeit | `"2026-02-03T14:30:00"` |
| `icon` | Emoji (optional) | `"📸"` für Instagram, `"🎵"` für TikTok |

---

## ⏰ Zeitformat (timestamp):

Format: `YYYY-MM-DDTHH:MM:SS`

**Beispiele:**
- `"2026-02-03T14:30:00"` = 3. Februar 2026, 14:30 Uhr
- `"2026-02-05T09:15:00"` = 5. Februar 2026, 09:15 Uhr
- `"2026-03-10T18:00:00"` = 10. März 2026, 18:00 Uhr

**Tipp:** Die Website zeigt automatisch "vor X Stunden/Tagen" an!

---

## 🎯 Komplettes Beispiel:

```json
[
    {
        "platform": "instagram",
        "title": "Mottowoche Tag 1 - Pyjama Party",
        "description": "Die besten Outfits vom Pyjama-Tag! 🛏️",
        "link": "https://www.instagram.com/p/C3aBc123DeF",
        "timestamp": "2026-02-03T14:30:00",
        "icon": "📸"
    },
    {
        "platform": "tiktok",
        "title": "Lustiger Moment aus der Pause",
        "description": "Das müsst ihr sehen! 😂",
        "link": "https://www.tiktok.com/@abirolspritz27/video/1234567890",
        "timestamp": "2026-02-02T18:00:00",
        "icon": "🎵"
    },
    {
        "platform": "instagram",
        "title": "Kuchenverkauf Erfolg",
        "description": "Danke für eure Unterstützung! Wir haben 250€ eingenommen 🎉",
        "link": "https://www.instagram.com/p/XyZ789aBc",
        "timestamp": "2026-02-01T16:45:00",
        "icon": "🍰"
    }
]
```

---

## 🔄 Workflow:

1. **Post veröffentlichen** auf Instagram/TikTok
2. **Link kopieren** vom Post
3. **`social-posts.json` öffnen**
4. **Neuen Eintrag oben hinzufügen**
5. **Speichern & Pushen**
6. **Fertig!** Website zeigt automatisch den neuen Post mit "vor X Min/Stunden"

---

## 💡 Tipps:

### Alte Posts löschen
Nach ein paar Wochen können Sie alte Posts aus der Liste entfernen, um die Übersicht zu behalten. Behalten Sie nur die **letzten 5-10 Posts**.

### Icons
Sie können kreative Emojis verwenden:
- 🎉 Events
- 🍰 Kuchenverkauf
- 📸 Fotos
- 🎥 Videos
- 🎓 Abi-bezogen
- 🎊 Feiern
- 📅 Termine

### Zeitgenauigkeit
Die Uhrzeit muss nicht sekundengenau sein - wichtig ist nur das Datum und ungefähr die Tageszeit (morgens/mittags/abends).

---

## ⚠️ Häufige Fehler:

### ❌ Vergessenes Komma
```json
[
    {
        "platform": "instagram",
        ...
    }  // ← KOMMA FEHLT!
    {
        "platform": "tiktok",
        ...
    }
]
```

### ✅ Richtig
```json
[
    {
        "platform": "instagram",
        ...
    },  // ← MIT KOMMA
    {
        "platform": "tiktok",
        ...
    }
]
```

---

## 🎉 Das war's!

Jetzt müssen Sie nur noch nach jedem Instagram/TikTok-Post kurz die `social-posts.json` aktualisieren - dauert 30 Sekunden! 🚀

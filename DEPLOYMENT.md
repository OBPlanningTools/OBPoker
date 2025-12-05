# PlanITPoker Online - Deployment Guide 🚀

## Einfachste Option: GitHub Pages (KOSTENLOS, 2 Minuten)

### Schritt 1: GitHub Account erstellen
- Gehen Sie zu https://github.com
- Klicken Sie auf "Sign up" (falls noch kein Account)

### Schritt 2: Neues Repository erstellen
1. Klicken Sie auf das "+" Symbol → "New repository"
2. Name: `planitpoker` (oder beliebiger Name)
3. ✅ Public
4. ✅ Add a README file
5. Klicken Sie auf "Create repository"

### Schritt 3: Datei hochladen
1. Klicken Sie auf "Add file" → "Upload files"
2. Ziehen Sie die Datei `index.html` in den Browser
3. Klicken Sie auf "Commit changes"

### Schritt 4: GitHub Pages aktivieren
1. Gehen Sie zu "Settings" (oben rechts)
2. Klicken Sie links auf "Pages"
3. Bei "Source": Wählen Sie "main" Branch
4. Klicken Sie auf "Save"
5. Nach 1-2 Minuten erscheint Ihre URL!

**Ihre URL wird sein:**
```
https://IHR-USERNAME.github.io/planitpoker/
```

---

## Alternative 1: Netlify Drop (KOSTENLOS, 30 Sekunden)

1. Gehen Sie zu https://app.netlify.com/drop
2. Ziehen Sie die `index.html` direkt in den Browser
3. **FERTIG!** Sie bekommen sofort eine URL wie:
   ```
   https://random-name-123456.netlify.app
   ```

---

## Alternative 2: Vercel (KOSTENLOS)

1. Gehen Sie zu https://vercel.com
2. Klicken Sie auf "Sign Up" (mit GitHub)
3. Klicken Sie auf "Add New..." → "Project"
4. Importieren Sie Ihr GitHub Repository
5. Klicken Sie auf "Deploy"
6. **FERTIG!** URL wird automatisch generiert

---

## Alternative 3: Firebase Hosting (KOSTENLOS + Echtzeit-Datenbank)

### Vorteile:
- ✅ Kostenlos
- ✅ Echtzeit-Synchronisation zwischen Benutzern
- ✅ Professionelle Lösung

### Setup:
1. Gehen Sie zu https://console.firebase.google.com
2. Klicken Sie auf "Add project" → Name eingeben → "Continue"
3. Google Analytics: Kann deaktiviert werden → "Create project"
4. Warten Sie 30 Sekunden → "Continue"

### Realtime Database aktivieren:
1. Links im Menü: "Build" → "Realtime Database"
2. Klicken Sie auf "Create Database"
3. Location: Europe
4. Security rules: "Start in test mode" → "Enable"

### Ihre Firebase Config:
1. Links im Menü: "Project Overview" → Zahnrad-Symbol → "Project settings"
2. Scrollen Sie nach unten zu "Your apps"
3. Klicken Sie auf das Web-Icon `</>`
4. Nickname: planitpoker → "Register app"
5. **KOPIEREN Sie die firebaseConfig** Daten

### Config in index.html einfügen:
Öffnen Sie `index.html` und ersetzen Sie die Zeilen 459-466:
```javascript
const firebaseConfig = {
    apiKey: "IHRE_API_KEY",
    authDomain: "ihr-projekt.firebaseapp.com",
    databaseURL: "https://ihr-projekt-default-rtdb.firebaseio.com",
    projectId: "ihr-projekt-id",
    storageBucket: "ihr-projekt.appspot.com",
    messagingSenderId: "123456789",
    appId: "1:123456789:web:abcdef"
};
```

### Firebase Hosting aktivieren:
```powershell
# Firebase CLI installieren
npm install -g firebase-tools

# Login
firebase login

# Projekt initialisieren
firebase init hosting

# Datei deployen
firebase deploy
```

Oder einfach die Datei über GitHub Pages hosten und nur die Realtime Database von Firebase nutzen!

---

## Empfehlung für Sie:

### Option A: **Nur zum Testen** (1 Minute)
→ **Netlify Drop**: https://app.netlify.com/drop
- Einfach `index.html` rein ziehen
- Sofort online!

### Option B: **Für echte Nutzung** (5 Minuten)
→ **GitHub Pages**
- Permanente URL
- Kostenlos
- Einfach zu aktualisieren

### Option C: **Professionell mit Echtzeit** (15 Minuten)
→ **Firebase (Database) + GitHub Pages (Hosting)**
- Beste Lösung
- Echte Echtzeit-Synchronisation
- Kostenlos bis 10.000 Nutzer/Monat

---

## Was funktioniert wie?

| Lösung | Kosten | Setup-Zeit | Echtzeit? | Empfohlen für |
|--------|--------|------------|-----------|---------------|
| **Netlify Drop** | Kostenlos | 30 Sek | Nein | Schnelltest |
| **GitHub Pages** | Kostenlos | 2 Min | Nein | Permanente URL |
| **Firebase** | Kostenlos | 15 Min | ✅ Ja | Professionell |

Welche Option möchten Sie nutzen? Ich helfe Ihnen beim Setup! 🚀

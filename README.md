# ☕ Koffein Entwöhnungstracker

Schlafoptimierter Koffein-Tracker als installierbare PWA.

## Features

- **Getränke-Logging** — Kaffee, Club-Mate, Mate Tee, Grüner Tee mit korrekten Portionsgrößen
- **Schlafoptimierung** — Cutoffs basierend auf Halbwertszeit und Schlafenszeit 21 Uhr
- **Blut-Koffein-Schätzung** — Aktuell + Projektion zur Schlafenszeit (<50mg Ziel)
- **Zeitkorrektur** — Tap auf Uhrzeit zum nachträglichen Korrigieren
- **7-Tage-Statistik** — Balkendiagramm mit Cutoff-Verletzungen
- **Offline-fähig** — Service Worker, funktioniert ohne Netz
- **Installierbar** — PWA, zum Homescreen hinzufügbar

## Regeln

| Getränk | mg | Cutoff |
|---------|-----|--------|
| Kaffee · Becher | 95mg | 12 Uhr |
| Club-Mate · Flasche | 100mg | 12 Uhr |
| Mate · Kalebasse | 78mg | 12 Uhr |
| Grüner Tee · Tasse | 35mg | 14 Uhr |
| **Alles** | — | **Ab 14 Uhr STOPP** |

Ziel: <50mg Restkoffein um 21 Uhr (Schlafenszeit)

## Deployment

### GitHub Pages (automatisch)

1. Neues GitHub Repo erstellen
2. Diesen Ordner pushen:
   ```bash
   cd koffein-tracker
   git init
   git add .
   git commit -m "init"
   git branch -M main
   git remote add origin git@github.com:DEIN-USER/koffein-tracker.git
   git push -u origin main
   ```
3. In Repo → Settings → Pages → Source: **GitHub Actions**
4. Push triggert automatisches Deployment
5. URL: `https://DEIN-USER.github.io/koffein-tracker/`

### Manuell

Einfach den `public/` Ordner auf einen beliebigen Webserver legen — keine Build-Tools nötig.

## Installieren als App

- **iOS**: Safari → Teilen → "Zum Home-Bildschirm"
- **Android**: Chrome → Menü → "App installieren"
- **Desktop**: Chrome Adressleiste → Install-Icon

## Tech

Vanilla JS, kein Framework, kein Build-Step. Daten in `localStorage`.

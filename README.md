# Wurfbild – Handball-Wurferfassung fürs iPhone

Erfasst im Spiel pro Wurf **Position**, **Team**, **Tor / kein Tor** und **Spielzug** und wertet sie aus (Wurfbild, Spielzüge pro Position, Bild-Export).

Die App ist eine einzelne Web-Seite. Sie läuft über **GitHub Pages**, lässt sich am iPhone auf den Home-Bildschirm legen und funktioniert nach dem ersten Öffnen auch **ohne Internet** in der Halle.

## Inhalt des Repositorys

| Datei | Zweck |
|---|---|
| `index.html` | Die komplette App |
| `sw.js` | Offline-Speicher (Service Worker) |
| `manifest.webmanifest` | Name, Farben und Symbol für den Home-Bildschirm |
| `icons/` | App-Symbole |

## Einrichten (einmalig)

1. **GitHub-Konto anlegen** auf <https://github.com> (falls noch keines vorhanden).
2. **Neues Repository erstellen:** oben rechts **+** → **New repository**.
   - Name: `wurfbild`
   - Sichtbarkeit: **Public** (GitHub Pages ist im kostenlosen Konto nur für öffentliche Repositorys verfügbar. Öffentlich ist nur der Programmcode – deine Spieldaten bleiben auf deinem iPhone.)
   - **Create repository** antippen.
3. **Dateien hochladen:** im neuen Repository auf **uploading an existing file** klicken (oder **Add file → Upload files**).
   - Den Inhalt des entpackten Ordners hineinziehen: `index.html`, `sw.js`, `manifest.webmanifest`, `README.md` und den Ordner `icons`.
   - Wichtig: die Dateien selbst hochladen, nicht den übergeordneten Ordner. `index.html` muss ganz oben im Repository liegen.
   - Unten **Commit changes** klicken.
4. **GitHub Pages einschalten:** **Settings → Pages**.
   - Bei **Source**: **Deploy from a branch**
   - Bei **Branch**: `main` und `/ (root)` → **Save**
5. **1–2 Minuten warten.** Oben auf derselben Seite erscheint die Adresse, z. B.
   `https://DEIN-NAME.github.io/wurfbild/`

## Auf dem iPhone installieren

1. Die Adresse in **Safari** öffnen (nicht in Chrome, sonst fehlt „Zum Home-Bildschirm“).
2. Unten auf **Teilen** (Quadrat mit Pfeil) tippen → **Zum Home-Bildschirm** → **Hinzufügen**.
3. Die App ab jetzt immer über das **Wurfbild-Symbol** auf dem Home-Bildschirm öffnen.
4. Einmal mit Internet öffnen – danach funktioniert sie auch offline.

> Die App auf dem Home-Bildschirm hat ihren **eigenen Speicher**, getrennt von Safari. Daten, die du in Safari erfasst, siehst du nicht in der Home-Bildschirm-App und umgekehrt. Erfasse deshalb immer über das Symbol.

## Daten aus der Claude-Version übernehmen

1. In der bisherigen Version (in Claude): **Menü ☰ → Daten speichern → Sicherung aller Spiele** → in der Dateien-App sichern.
2. In der neuen App (Home-Bildschirm): **Menü ☰ → Daten speichern → Sicherung laden** → die Datei auswählen.

## Daten sichern

Alle Daten liegen nur auf dem iPhone. Nach jedem Spiel: **Menü ☰ → Daten speichern → Sicherung aller Spiele** → **In Dateien sichern** (z. B. in iCloud Drive). Wird die App gelöscht, sind die Daten sonst weg.

## Bild in Fotos speichern

**Auswertung** → Spielzug wählen → **Als Bild exportieren** → **In Fotos speichern** → im Teilen-Menü **Bild sichern**.

## App aktualisieren

1. Im Repository auf `index.html` klicken → Stift-Symbol (Bearbeiten) oder neue Datei über **Add file → Upload files** hochladen und **Commit changes**.
2. In `sw.js` die Zeile `const CACHE = 'wurfbild-v1';` auf die nächste Nummer ändern (`v2`, `v3` …) und ebenfalls speichern.
3. Nach 1–2 Minuten die App am iPhone mit Internet öffnen, einmal schließen und wieder öffnen – dann ist die neue Version aktiv. Die Spieldaten bleiben erhalten.

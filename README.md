# Mathematikdidaktik-Webseite

Diese Webseite ist als statische One-Page aufgebaut (`index.html` + `styles.css`) und kann sehr einfach über **GitHub Pages** veröffentlicht werden.

## Schnellstart: Seite lokal testen

```bash
python3 -m http.server 4173
```

Dann im Browser öffnen: `http://localhost:4173`

---

## Veröffentlichung ins Internet (GitHub Pages)

In diesem Repository ist bereits ein GitHub-Workflow für die Veröffentlichung enthalten (`.github/workflows/deploy-pages.yml`).

### 1) Repository zu GitHub pushen

Falls noch kein Remote gesetzt ist:

```bash
git remote add origin https://github.com/<DEIN-USERNAME>/<DEIN-REPO>.git
git push -u origin work
```

> Falls dein Haupt-Branch anders heißt (z. B. `main`), passe den Push entsprechend an.

### 2) GitHub Pages aktivieren

1. Öffne auf GitHub dein Repository.
2. Gehe zu **Settings → Pages**.
3. Unter **Build and deployment** wähle bei **Source**: `GitHub Actions`.

### 3) Deployment abwarten

- Nach jedem Push auf den Branch `work` startet der Workflow automatisch.
- Nach erfolgreichem Lauf ist die Seite online unter:
  - `https://<DEIN-USERNAME>.github.io/<DEIN-REPO>/`

---

## Eigene Domain (optional)

Wenn du später eine eigene Domain (z. B. `www.deine-domain.de`) verwenden willst:

1. Lege im Repo eine Datei `CNAME` mit deiner Domain an.
2. Setze bei deinem Domainanbieter einen CNAME-Record auf `<DEIN-USERNAME>.github.io`.
3. Aktiviere in GitHub Pages HTTPS.

---

## Inhalte ändern

- Texte/Struktur: `index.html`
- Design/Farben/Layout: `styles.css`

Nach Änderungen einfach committen und pushen — GitHub Pages aktualisiert die Live-Seite automatisch.

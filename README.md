# wazuh.cyqore.de

Technische Wazuh-Übersicht für Administratoren. Eine einzelne statische Seite,
kein Build, keine Abhängigkeiten.

## Inhalt

| Datei | Zweck |
|-------|-------|
| `index.html` | Die komplette Seite. Wortmarke als Data-URI eingebettet. |
| `CNAME` | Zieldomain für GitHub Pages. |

## Gestaltung

Die Seite nutzt die CYQORE-Tokens aus `cyqore_daily/web/style.css`:
Akzent `#E7095B`, Grund `#000` mit Bordeaux-Verlauf `#2F0012`, Flächen `#141416`,
Text `#F5F5F7`, Sekundärtext `#9CA0A8`.

**Keine externen Aufrufe.** Schriften kommen aus dem System, die Wortmarke steckt
als Data-URI in der Datei. Damit geht beim Aufruf kein Request an Dritte — relevant,
weil die CYQORE-Datenschutzerklärung Google nur für den Mailversand nennt.

## Veröffentlichen

GitHub Pages, Quelle `main` / Wurzelverzeichnis. Passender DNS-Eintrag:

    wazuh   CNAME   cyqore.github.io

Danach unter *Settings → Pages* "Enforce HTTPS" aktivieren, sobald das Zertifikat
ausgestellt ist (dauert nach dem DNS-Eintrag einige Minuten).

## Pflege

Die Versionsangaben (Versionslinie, Installationsbefehl, Hardwarebedarf) stehen im
Fußbereich und in Abschnitt 06. Bei einem Wazuh-Hauptversionswechsel beide prüfen.

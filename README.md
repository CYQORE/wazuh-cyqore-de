# wazuh.cyqore.de

Technische Wazuh-Übersicht für Administratoren. Eine einzelne statische Seite,
kein Build, keine Abhängigkeiten.

## Inhalt

| Datei | Zweck |
|-------|-------|
| `index.html` | Die komplette Seite. Wortmarke als Data-URI eingebettet. |
| `CNAME` | Zieldomain für GitHub Pages. |

## Gestaltung

Die Seite bildet die **Wazuh-Oberfläche** nach — helles Dashboard in EUI-/
OpenSearch-Optik mit dunkler Kopfleiste, Seitenleiste und Modulkacheln.
Bewusst *nicht* im CYQORE-Design: Administratoren sollen wiedererkennen, was
sie später vor sich haben.

Das Modul **Live-Betrieb** animiert den Weg eines Ereignisses durch die
Pipeline — Endpunkt, Agent, Decoder, Regeln, Indexer, Dashboard, Reaktion —
in vier Szenarien (SSH-Brute-Force, Webshell, verwundbares Paket, getrennter
Agent), mit Schritt-für-Schritt-Erklärung und einem laufenden Ereignisstrom.
Bei `prefers-reduced-motion` startet die Animation erst per Klick.

Abgebildet sind alle Modulgruppen von Wazuh 4.14 — Endpoint Security, Threat
Intelligence, Security Operations, Cloud Security und Verwaltung — dazu ein
Abschnitt Grundlagen mit Architektur, Ports, Regeln und Betrieb. Jeder Eintrag
in Seitenleiste und Kachelraster trägt einen Tooltip, der erklärt, was das
Modul zeigt und tut.

Ein dauerhaft sichtbares Band oben stellt klar: Nachbau zu Schulungszwecken,
keine laufende Installation, keine Seite der Wazuh Inc. Kennzahlen sind
erfunden, Modulnamen, Regel-IDs, Feldnamen und Konfigurationsblöcke nicht.

**Keine externen Aufrufe.** Schriften kommen aus dem System, das gesamte
Markup, CSS und JavaScript steht in der einen Datei.

## Veröffentlichen

GitHub Pages, Quelle `main` / Wurzelverzeichnis. Passender DNS-Eintrag:

    wazuh   CNAME   cyqore.github.io

Danach unter *Settings → Pages* "Enforce HTTPS" aktivieren, sobald das Zertifikat
ausgestellt ist (dauert nach dem DNS-Eintrag einige Minuten).

## Pflege

Die Versionsangaben (Versionslinie, Installationsbefehl, Hardwarebedarf) stehen im
Fußbereich und in Abschnitt 07. Bei einem Wazuh-Hauptversionswechsel beide prüfen.

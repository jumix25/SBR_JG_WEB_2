# Schubert Reisen – neue Website

Neue responsive Landingpage im hellen Liquid-Glass-Stil für Schubert Reisen GmbH.

## Hosting mit GitHub Pages
1. Repository öffnen: https://github.com/jumix25/SBR_JG_WEB_2
2. **Settings → Pages** öffnen.
3. Unter **Build and deployment** die Quelle **Deploy from a branch** wählen.
4. Branch `main`, Ordner `/(root)`, speichern.
5. Nach dem Deployment ist die Seite normalerweise unter https://jumix25.github.io/SBR_JG_WEB_2/ erreichbar.

## Wichtig: statische Demo
GitHub Pages hostet nur statische Dateien. Die Seite enthält UI-Prototypen für Extranet/JuAcc, Bewertung, Problemmeldung und Chat. Diese sind **noch nicht produktiv angebunden**:
- JuAcc-Login authentifiziert keine Nutzer und sendet keine Zugangsdaten.
- Chat ist ein geführter Demo-Assistent, keine echte KI und keine Live-Übergabe.
- Formulare öffnen das lokale E-Mail-Programm; sie speichern oder versenden keine Daten selbst.
- Bewertungen werden nicht gesammelt oder öffentlich angezeigt.

Für einen produktiven Betrieb müssen JuAcc, ein sicheres Backend, KI-/Chat-Service, Support-Übergabe und Formularverarbeitung integriert und datenschutzrechtlich geprüft werden. Keine Zugangsdaten oder sensiblen Daten in statische JavaScript-Dateien schreiben.

## Rechtliche Seiten
Die Links zu AGB, Impressum und Agenturanmeldung führen vorerst auf die entsprechenden offiziellen Seiten von schubert-reisen.de. Die Datenschutzerklärung ist ebenfalls mit der offiziellen Website verlinkt. Vor dem Livegang sollte SBR die rechtlichen Texte und die Verwendung des Firmenlogos freigeben.

## Design
Responsive HTML/CSS/JavaScript, ohne Build-Schritt. Die Website verwendet Google Fonts und externe Unsplash-Bilder; für vollständig lokale/offline Nutzung diese Assets lokal einbinden.

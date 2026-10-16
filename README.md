# Schubert Reisen – neue Website

Neue responsive Landingpage im hellen Liquid-Glass-Stil für Schubert Reisen GmbH.

## Hosting mit GitHub Pages
1. Repository öffnen: https://github.com/jumix25/SBR_JG_WEB_2
2. **Settings → Pages** öffnen.
3. Unter **Build and deployment** die Quelle **Deploy from a branch** wählen.
4. Branch `main`, Ordner `/(root)`, speichern.
5. Nach dem Deployment ist die Seite normalerweise unter https://jumix25.github.io/SBR_JG_WEB_2/ erreichbar.

## JuAcc / Firebase – einfacher Verbindungstest
Der Extranet-Link öffnet einen JuAcc-Testdialog. Er schreibt beim Klick ausschließlich `status: "juacc geht"` mit Zeitstempel nach Firestore unter `juacc/status`. Es gibt **noch keinen Benutzer-Login** und keine Nutzerpasswörter.

Vor dem Test in der Firebase Console für das Projekt `jugroup-kundenportal`:
1. **Build → Authentication → Sign-in method** öffnen und **Anonymous** aktivieren.
2. **Build → Firestore Database** öffnen und eine Datenbank erstellen, falls noch keine existiert.
3. Unter **Firestore → Rules** den Inhalt der Datei `firestore.rules` veröffentlichen.
4. Unter **Authentication → Settings → Authorized domains** sicherstellen, dass `jumix25.github.io` zugelassen ist.
5. GitHub Pages öffnen, Extranet / JuAcc anklicken und auf **„juacc geht“ in Firebase schreiben** klicken.
6. In Firestore unter `juacc/status` prüfen, ob `status` den Wert `juacc geht` enthält.

Die Regeln erlauben angemeldeten (auch anonymen) Firebase-Sitzungen nur das Schreiben dieses einen festgelegten Statusdokuments; Lesen und Löschen sind gesperrt. Weil anonyme Anmeldung öffentlich erreichbar ist, ist dies nur ein Verbindungstest, kein belastbares Produktions-Authentifizierungssystem.

## Weitere Demo-Funktionen
GitHub Pages hostet nur statische Dateien:
- Chat ist ein geführter Demo-Assistent, keine echte KI und keine Live-Übergabe.
- Chat ist ein geführter Demo-Assistent, keine echte KI und keine Live-Übergabe.
- Formulare öffnen das lokale E-Mail-Programm; sie speichern oder versenden keine Daten selbst.
- Bewertungen werden nicht gesammelt oder öffentlich angezeigt.

Für einen produktiven Betrieb müssen JuAcc, ein sicheres Backend, KI-/Chat-Service, Support-Übergabe und Formularverarbeitung integriert und datenschutzrechtlich geprüft werden. Keine Zugangsdaten oder sensiblen Daten in statische JavaScript-Dateien schreiben.

## Rechtliche Seiten
Die Links zu AGB, Impressum und Agenturanmeldung führen vorerst auf die entsprechenden offiziellen Seiten von schubert-reisen.de. Die Datenschutzerklärung ist ebenfalls mit der offiziellen Website verlinkt. Vor dem Livegang sollte SBR die rechtlichen Texte und die Verwendung des Firmenlogos freigeben.

## Design
Responsive HTML/CSS/JavaScript, ohne Build-Schritt. Die Website verwendet Google Fonts und externe Unsplash-Bilder; für vollständig lokale/offline Nutzung diese Assets lokal einbinden.

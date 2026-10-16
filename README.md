# Schubert Reisen – neue Website

Neue responsive Landingpage im hellen Liquid-Glass-Stil für Schubert Reisen GmbH.

## Hosting mit GitHub Pages
1. Repository öffnen: https://github.com/jumix25/SBR_JG_WEB_2
2. **Settings → Pages** öffnen.
3. Unter **Build and deployment** die Quelle **Deploy from a branch** wählen.
4. Branch `main`, Ordner `/(root)`, speichern.
5. Nach dem Deployment ist die Seite normalerweise unter https://jumix25.github.io/SBR_JG_WEB_2/ erreichbar.

## JuAcc / Firebase – E-Mail-Login
Der JuAcc-Button öffnet ein Anmeldefenster mit E-Mail-Adresse und Passwort. Die Erfolgsmeldung **„JuAcc geht — du bist erfolgreich eingeloggt“** erscheint erst nach erfolgreicher Firebase-Anmeldung und erfolgreichem Schreiben des Teststatus nach Firestore. Dies ist noch kein vollständiges Agenturportal mit Rollen oder geschützten Inhalten.

Vor der Nutzung in der Firebase Console für das Projekt `jugroup-kundenportal`:
1. Unter **Build → Authentication → Sign-in method** die Methode **E-Mail/Passwort** aktivieren.
2. Unter **Authentication → Users** das gewünschte JuAcc-Konto mit E-Mail und Passwort anlegen. Ein Konto kann nicht einfach auf der Website selbst registriert werden.
3. Unter **Build → Firestore Database** eine Datenbank erstellen, falls noch keine existiert.
4. Unter **Firestore → Rules** den Inhalt der Datei `firestore.rules` veröffentlichen.
5. Unter **Authentication → Settings → Authorized domains** sicherstellen, dass `jumix25.github.io` zugelassen ist.
6. GitHub Pages öffnen, auf **JuAcc** klicken und mit dem zuvor angelegten Konto anmelden.

Nach erfolgreicher Anmeldung sollte Firestore unter `juacc/status` den Wert `status: "juacc geht"` enthalten. Die Regeln erlauben nur Konten, die sich mit E-Mail und Passwort angemeldet haben, dieses eine Statusdokument zu schreiben; Lesen und Löschen sind gesperrt. Die Erfolgsmeldung kommt nicht bei falschen Zugangsdaten.

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

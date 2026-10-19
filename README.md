# Paketdienst-Planspiel

Eine rundenbasierte Unternehmenssimulation für den Wirtschaftskunde-Unterricht. Schülerinnen und Schüler führen einen kleinen Paketdienst in Wien ein Geschäftsjahr lang. Jede Runde ist ein Geschäftsmonat. Sie nehmen Aufträge an, setzen Preise, leasen oder kaufen Fahrzeuge, stellen Personal ein und lesen danach ihren Monatsbericht.

Das ganze Spiel steckt in einer einzigen Datei: `index.html`.

## Stufen

- **Einsteiger** (Unterstufe): Einnahmen, Ausgaben, Gewinn, Löhne, Lohnnebenkosten, 13./14. Gehalt, Leasing, Kontoüberziehung
- **Fortgeschritten** (Oberstufe, HAK, HAS): zusätzlich Kauf mit Abschreibung, Kredit, Erfolgsrechnung, Bilanz, Deckungsbeitrag, Break-even, Bonität, Maut, Kennzahlen

Dazu gibt es Ereigniskarten, Arbeitsaufträge nach jedem Monat, ein Begriffslexikon und einen Abschlussbericht zum Abgeben.

## Auf GitHub Pages veröffentlichen

1. Neues Repository auf GitHub anlegen, zum Beispiel `paketdienst-planspiel`. Es kann öffentlich sein.
2. Die Dateien `index.html`, `README.md` und `.nojekyll` in das Repository hochladen (auf GitHub: **Add file → Upload files**).
3. Im Repository **Settings → Pages** öffnen.
4. Bei **Source** „Deploy from a branch“ wählen, dann Branch `main` und Ordner `/ (root)`, und speichern.
5. Nach ein bis zwei Minuten läuft das Spiel unter
   `https://<dein-github-name>.github.io/paketdienst-planspiel/`

Diesen Link gibst du an deine Klasse weiter. Eine Anmeldung ist für die Schülerinnen und Schüler nicht nötig.

## Ohne Internet verwenden

`index.html` lässt sich auch direkt öffnen, etwa per Doppelklick, von einem USB-Stick oder aus einem Schul-Netzlaufwerk. Das Spiel braucht keine Internetverbindung.

## Datenschutz

- Das Spiel lädt **keine** externen Dateien: keine Schriften, keine Bibliotheken, kein Tracking, keine Cookies.
- Alle Spielstände werden **nur lokal im Browser** des jeweiligen Geräts gespeichert (`localStorage`). Es werden keine Daten an einen Server geschickt, auch nicht an GitHub.
- Name, Klasse und Firmenname, die beim Start eingegeben werden, bleiben ebenfalls nur auf dem Gerät. Sie erscheinen im Abschlussbericht, den die Schülerin oder der Schüler selbst kopiert oder als Datei speichert und bei dir abgibt.

## Speichern und Weiterspielen

- Der Spielstand wird automatisch im Browser gespeichert. Wer die Seite später wieder öffnet, spielt dort weiter, wo er aufgehört hat.
- Löscht ein Browser seine Daten, ist der Spielstand weg. Das passiert etwa im privaten Modus oder auf verwalteten Schulgeräten. Unter **Speichern** gibt es deshalb einen **Sicherungscode** zum Kopieren und eine **Sicherungsdatei**. Damit kann man auch auf einem anderen Gerät weiterspielen.
- **Neu starten** (oben rechts) löscht den Spielstand nach einer Bestätigung. Name, Klasse, Firma und Stufe bleiben vorausgefüllt.

## Ergebnisse einsammeln

Am Ende des Jahres, oder jederzeit über **Speichern → Abschlussbericht**, erzeugt das Spiel einen Textbericht mit allen Monatszahlen und den Antworten auf die Arbeitsaufträge. Die Schülerinnen und Schüler kopieren ihn oder speichern ihn als `.txt`-Datei und geben ihn ab, zum Beispiel über Teams, Moodle oder per E-Mail.

## Zahlen anpassen

Alle Annahmen stehen am Anfang des Skripts in `index.html` im Abschnitt `Annahmen`, unter anderem:

| Konstante | Bedeutung |
|---|---|
| `PRICE` | Diesel- und Strompreis (netto) |
| `LNK` | Lohnnebenkosten des Arbeitgebers (Anteil vom Bruttolohn) |
| `KOEST` | Körperschaftsteuer |
| `START_CAPITAL` | Startkapital |
| `OD_LIMIT`, `OD_RATE`, `LOAN_RATE` | Überziehungsrahmen und Zinssätze |
| `WAGE` | Bruttolöhne nach Führerscheinklasse |
| `VEH` | Fahrzeuge: Kaufpreis, Leasingrate, Versicherung, Wartung, Verbrauch, Kapazität |

Die Werte sind vereinfachte Annahmen, angelehnt an österreichische Verhältnisse 2026. Sie eignen sich für den Unterricht, nicht als Planungsgrundlage. Alle Firmen- und Kundennamen sind frei erfunden.

## Technisches

- Eine Datei, reines HTML, CSS und JavaScript, ohne Build-Schritt und ohne Abhängigkeiten
- Läuft in aktuellen Versionen von Chrome, Edge, Firefox und Safari, auch auf Tablets und Handys
- Hell- und Dunkelmodus folgen der Geräteeinstellung
- `.nojekyll` sorgt dafür, dass GitHub Pages die Datei unverändert ausliefert

# Sitzungscockpit Landrat Nidwalden

Das Sitzungscockpit ist eine inoffizielle Arbeitshilfe für Mitglieder des Nidwaldner Landrats. Es begleitet die Arbeit von der Vorbereitung bis zur Nachbereitung einer Sitzung. Massgebend sind die amtlichen Unterlagen und Beschlüsse.

## Ziele und Vorteile

| Ziel | Was das im Alltag bringt |
| --- | --- |
| Unterlagen schnell finden | Die Traktandenliste und die Links zu den amtlichen Dokumenten stehen beim jeweiligen Geschäft. Die Suche findet Einträge nach Nummer, Titel, Verfahrensschritt oder Bezeichnung einer Unterlage. |
| Die Beratung gezielt vorbereiten | Pro Geschäft lassen sich offene Fragen, eigene Notizen und der Entwurf eines Votums festhalten. |
| Während der Sitzung den Überblick behalten | Mit «Erledigt» lässt sich der Bearbeitungsstand sichtbar machen. Beschlüsse, Rückfragen und Pendenzen bleiben beim passenden Geschäft. |
| Gehaltene Voten weitergeben | Die bestätigten Wortmeldungen lassen sich in einer gemeinsamen Word-Datei für das Landratssekretariat zusammenstellen. |

## Starten

1. Auf GitHub **Code → Download ZIP** wählen und das Archiv entpacken.
2. Die Datei `index.html` im Browser öffnen. Als Beispiel ist die Sitzung vom **25. November 2026** eingetragen.
3. Ein Traktandum auswählen. In der Detailansicht stehen die Unterlagen, das Votumsfeld und die persönliche Sitzungsnotiz.

Das Cockpit selbst funktioniert offline. Für Links zu nw.ch und für die Arbeit mit ChatGPT ist eine Internetverbindung erforderlich.

## Arbeitsweise

### Vor der Sitzung

- Die amtliche Traktandenliste öffnen und den Stand der eigenen Unterlagen prüfen.
- Die relevanten Geschäfte nach Nummer oder Stichwort suchen. Offene Punkte im Feld «Meine Sitzungsnotiz» sammeln.
- Für geplante Wortmeldungen im Feld «Votum · Entwurf» den Text vorbereiten. Das Feld passt seine Höhe automatisch an.
- Bei Bedarf «Votum mit KI überarbeiten» wählen. Das Cockpit erstellt einen Auftrag mit Geschäft, Verfahrensstand, amtlichen Links und aktuellem Text. Den Auftrag prüfen, vertrauliche Inhalte entfernen und ihn in ChatGPT einfügen. Das Ergebnis fachlich prüfen und in das Votumsfeld zurückkopieren.

### Während der Sitzung

- Beim passenden Geschäft Beschlüsse, Rückfragen und Pendenzen notieren. Für eine Pendenz empfiehlt sich eine Zeile mit der zuständigen Person und dem Termin, falls beides bekannt ist.
- «Erledigt» setzen, sobald die eigene Bearbeitung abgeschlossen ist.
- Nach einer Wortmeldung den Entwurf mit dem tatsächlich vorgetragenen Text abgleichen und «Votum gehalten» markieren. Die Sprecherrolle bei Bedarf ergänzen.

### Nach der Sitzung

1. Namen im Feld «Name für den Word-Export» erfassen.
2. «Gehaltene Voten als Word exportieren» wählen. Die Datei enthält die markierten Voten in Traktandenreihenfolge, jeweils mit Sitzungsdatum, Geschäft und erfasster Sprecherrolle. Sitzungsnotizen gehören nicht zum Word-Export.
3. Die Word-Datei vor dem Versand öffnen und Auswahl, Wortlaut und Rollen prüfen. Den Versand ans Landratssekretariat separat auslösen.
4. Mit «Notizen exportieren» bei Bedarf eine Textdatei für die Nachbereitung erstellen. Für das Weiterarbeiten oder einen Gerätewechsel zusätzlich eine JSON-Sicherung erstellen.

## Tipps und Tricks

- **Ähnliche Geschäfte unterscheiden.** Über die Unterziffer direkt zum richtigen Teilgeschäft springen, etwa `6.2`. Eine Suche wie `Stans West` zeigt die zusammengehörenden Traktanden.
- **Direkt zum Geschäft zurückkehren.** Nach der Auswahl enthält die Browseradresse die Traktandennummer als Anker, etwa `#t-6.2`. Ein Lesezeichen hilft beim nächsten Öffnen derselben Datei.
- **Für einen WLAN-Ausfall vorbereiten.** Die HTML-Datei und die wichtigsten amtlichen Dokumente vorab lokal ablegen. Die Dokumente lassen sich dann über die gespeicherten Kopien öffnen.
- **Die beiden Häkchen gezielt nutzen.** «Erledigt» zeigt den Bearbeitungsstand. «Votum gehalten» bestimmt die Auswahl für den Word-Export.
- **Wenn der Word-Button inaktiv bleibt.** Prüfen, ob mindestens ein Votum als gehalten markiert ist, alle markierten Voten Text enthalten und der Name eingetragen ist.
- **Gerät oder Browser wechseln.** Vorher unter «Speichern und wiederherstellen» eine Sicherung herunterladen. Im Zielbrowser die HTML-Datei derselben Sitzung öffnen, «Sicherung laden» wählen und den Namen für den Word-Export bei Bedarf neu eingeben.

## Eingaben sichern

Notizen, Voten und Markierungen speichert das Cockpit lokal im Browser. Je nach Browser, Profil oder privatem Modus kann die Speicherung eingeschränkt sein. Eine JSON-Sicherung enthält die persönlichen Eingaben. Sie gehört in einen geschützten Ordner und wird im Cockpit derselben Sitzung geladen. Der Text- und der Word-Export dienen der Weitergabe.

## Weitere Sitzungen

Für eine neue Sitzung eine eigene Kopie von `index.html` anlegen. Das angezeigte Sitzungsdatum, das Datum im Speicherschlüssel, in den Exportnamen, im Word-Manuskriptkopf und im KI-Auftrag sowie den Link zur Traktandenliste anpassen. Der Datenblock `<script id="data" type="application/json">` enthält je Geschäft vier Felder.

| Feld | Inhalt |
| --- | --- |
| `id` | Traktandennummer als Text, zum Beispiel `"6.2"` |
| `title` | Öffentlicher Titel des Geschäfts |
| `stage` | Verfahrensschritt |
| `links` | Liste aus Linktext und URL zur öffentlichen Unterlage |

Für dieselbe Sitzung Traktandennummern stabil halten, damit vorhandene Notizen zugeordnet bleiben. Sitzungsdaten und amtliche Unterlagen werden von Hand gepflegt.

## Erklärung zur Bereitstellung

> Ich stelle das Sitzungscockpit als freiwillige Arbeitshilfe für Kolleginnen und Kollegen im Nidwaldner Landrat zur Verfügung. Die Nutzung und Pflege erfolgen in eigener Verantwortung. Ich übernehme keinen Support und sage weder Wartung noch Aktualisierungen zu.
>
> Dominik Steiner

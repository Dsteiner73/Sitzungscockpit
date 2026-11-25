# Sitzungscockpit Landrat Nidwalden

Eine inoffizielle Arbeitshilfe für Mitglieder des Nidwaldner Landrats. Das Cockpit bündelt die Traktanden und die auf nw.ch verlinkten Unterlagen. Es bietet eine Suche, persönliche Notizen, Erledigt-Markierungen und einen Word-Export für gehaltene Voten.

## Starten

1. Dieses Repository als ZIP herunterladen und entpacken.
2. `index.html` im Browser öffnen. Die Beispielsitzung vom 25. November 2026 ist bereits eingetragen.
3. Mit Nummer oder Stichwort suchen. Bei einem Geschäft stehen die Links zu den Unterlagen und das persönliche Notizfeld.

Das Cockpit selbst lässt sich offline öffnen. Die verlinkten amtlichen Unterlagen auf nw.ch benötigen eine Verbindung. Massgebend sind die Unterlagen und Beschlüsse der zuständigen Stellen.

## Voten bearbeiten und exportieren

1. Im jeweiligen Traktandum das Feld «Votum · Entwurf» bearbeiten. Es wächst und schrumpft mit dem Text.
2. Bei Bedarf «Votum mit KI überarbeiten» wählen. Den erzeugten Auftrag prüfen, vertrauliche Inhalte entfernen und den Auftrag in ChatGPT einfügen. Das Ergebnis anschliessend in den Entwurf zurückkopieren.
3. Den tatsächlich gehaltenen Wortlaut prüfen, «Votum gehalten» markieren und bei Bedarf die Sprecherrolle eintragen.
4. Den Namen für den Word-Export erfassen und «Gehaltene Voten als Word exportieren» wählen. Die Datei enthält die markierten Voten in Traktandenreihenfolge mit einem Manuskriptkopf pro Votum.

## Eingaben sichern

Notizen, Voten und Markierungen speichert der Browser lokal. Je nach Browser oder privatem Modus kann die lokale Speicherung eingeschränkt sein. Unter «Speichern und wiederherstellen» lässt sich eine JSON-Sicherung herunterladen und wieder laden. Die Sicherung enthält die persönlichen Eingaben. Bewahre sie geschützt auf und lade sie nur im Cockpit derselben Sitzung.

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

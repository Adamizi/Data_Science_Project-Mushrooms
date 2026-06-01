# Abschlussbericht: Pilzklassifikation

## Ziel

Ziel war es, mit dem Pilz-Datensatz vorherzusagen, ob ein Pilz essbar oder giftig ist. Die Zielvariable heißt `poison`, mit `e` für essbar und `p` für giftig.

## Vorgehen

Wir haben uns an der Struktur aus dem Unterrichtsnotebook zur supervised classification orientiert:

- Daten laden
- Daten kurz explorieren
- einfache Diagramme zur Zielvariable, zu fehlenden Werten und zu `odor` erstellen
- Input und Output trennen
- Train/Test-Split erstellen
- Daten vorverarbeiten
- Entscheidungsbaum und KNN trainieren
- Ergebnisse mit F1, Recall, Precision und Accuracy bewerten

## Datenprobleme

Die Datei war mit `~` getrennt und nicht mit Komma. Außerdem gab es drei Zeilen mit leeren Zusatzfeldern am Ende. Diese wurden beim Laden entfernt. Auffällige Werte wie `d**`, `0.34`, `0.3` und `0.4` wurden als unbekannte Werte behandelt.

## Ergebnis

Der Entscheidungsbaum und KNN erreichen sehr gute Ergebnisse. Das liegt vermutlich daran, dass manche Merkmale, zum Beispiel `odor`, sehr stark mit der Zielvariable zusammenhängen. Im Notebook sieht man das auch in einem einfachen Balkendiagramm.

## Fazit

Der Entscheidungsbaum ist für unser Projekt die passendste Lösung, weil er gute Ergebnisse liefert und noch relativ einfach erklärbar ist. Bei Pilzen ist besonders der Recall für giftige Pilze wichtig, weil ein giftiger Pilz nicht als essbar vorhergesagt werden sollte.

## LLM-Nutzung

Wir haben ein LLM zur Unterstützung bei Struktur, Formulierungen und Datenprüfung genutzt. Die Lösung wurde bewusst am Kursnotebook orientiert und einfach gehalten.

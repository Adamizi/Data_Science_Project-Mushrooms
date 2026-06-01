# Abschlussbericht: Mushroom Classification

## Ziel

Ziel war es, mit dem Mushroom-Datensatz vorherzusagen, ob ein Pilz essbar oder giftig ist. Die Zielvariable heißt `poison`, mit `e` für essbar und `p` für giftig.

## Daten

Der Datensatz enthält 8.124 Zeilen und fast nur kategoriale Merkmale. Beim Laden gab es ein paar kleine Probleme: Der Trenner ist `~` und nicht Komma, außerdem hatten drei Zeilen leere Zusatzfelder am Ende. Diese wurden beim Laden entfernt. Einige auffällige Werte wie `d**`, `0.34`, `0.3` und `0.4` wurden als unbekannt (`?`) behandelt.

## Vorgehen

Wir haben zuerst die Daten angeschaut, die Zielvariable geprüft und fehlende bzw. auffällige Werte untersucht. Danach haben wir die Daten für Machine Learning vorbereitet:

- `veil-type` entfernt, weil diese Spalte nur einen Wert hat
- `?` als fehlende Werte behandelt
- kategoriale Features mit One-Hot-Encoding umgewandelt
- Decision Tree als Modell verwendet

## Ergebnis

Die einfache Baseline liegt bei ungefähr 52% Accuracy. Das Decision-Tree-Modell erreicht auf dem Testset fast perfekte Ergebnisse. Das liegt daran, dass manche Merkmale, besonders `odor`, sehr stark mit der Klasse zusammenhängen.

## Fazit

Das Projekt zeigt, wie man ein kategoriales Dataset lädt, einfache Datenprobleme bereinigt und ein Klassifikationsmodell mit scikit-learn trainiert. Für unser Projekt ist der Decision Tree eine gute Wahl, weil er gute Ergebnisse liefert und noch relativ leicht erklärbar ist.

## LLM-Nutzung

Wir haben ein LLM zur Unterstützung bei Struktur, Datenprüfung und Formulierungen genutzt. Die Gruppe ist verantwortlich dafür, den Code und die Ergebnisse erklären zu können.

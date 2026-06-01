# Abschlussbericht: Mushroom Classification

## Problemstellung

Ziel des Projekts ist die Vorhersage, ob ein Pilz essbar (`e`) oder giftig (`p`) ist. Dafür werden 22 kategoriale Merkmale genutzt, zum Beispiel Geruch, Lamellenfarbe, Sporenabdruckfarbe, Population und Habitat.

## Datenqualität

Die Rohdatei nutzt `~` als Separator. Beim Laden wurden drei Zeilen mit zusätzlichen leeren Feldern am Zeilenende gefunden und konservativ auf die erwarteten 23 Felder gekürzt. Zusätzlich wurden einzelne ungültige Kategorien gefunden, darunter `d**` im Habitat und numerische Werte wie `0.34`, `0.3` und `0.4` in kategorialen Spalten. Diese Werte wurden als unbekannt (`?`) behandelt.

Der Datensatz enthält 8.124 Zeilen. Die Zielklassen sind nahezu ausgeglichen: 4.208 essbare und 3.916 giftige Pilze. Die Spalte `veil-type` ist konstant und wurde für das Modell entfernt. `stalk-root` enthält viele `?`-Werte, die in der Pipeline imputiert werden.

## Machine-Learning-Strategie

Das Projekt wurde als überwachtes binäres Klassifikationsproblem umgesetzt. Alle Input-Features sind kategorial. Die Preprocessing-Pipeline ersetzt unbekannte Werte, imputiert kategoriale Werte mit der häufigsten Ausprägung und nutzt One-Hot-Encoding.

Verglichen wurden eine Dummy-Baseline, ein Decision Tree, Logistic Regression und Random Forest. Der Decision Tree eignet sich besonders gut als Hauptmodell, weil er sehr gut erklärbar ist und regelartige Entscheidungen sichtbar macht.

## Ergebnis

Die Dummy-Baseline erreicht nur ca. 51,8% Accuracy. Der Decision Tree erreicht in der 5-fachen Cross-Validation ca. 99,95% Accuracy und ca. 99,90% Recall für die giftige Klasse. Random Forest erreicht im Testlauf 100% auf allen Metriken.

Für diese Aufgabe ist Recall der giftigen Klasse besonders wichtig, weil ein giftiger Pilz, der als essbar klassifiziert wird, der gefährlichste Fehler wäre.

## Fazit

Nach Bereinigung und Preprocessing ist der Datensatz sehr gut klassifizierbar. Das finale empfohlene Modell ist der Decision Tree, da er nahezu perfekte Leistung mit hoher Interpretierbarkeit verbindet.

## Dokumentation der LLM-Nutzung

Large Language Models wurden zur Strukturierung des Projekts, zur Unterstützung bei der Datenprüfung, zur Entwicklung der ML-Strategie und zum Formulieren erklärender Texte genutzt. Die Gruppe bleibt verantwortlich dafür, den Code, die Datenbereinigung und die Modellierung vollständig zu verstehen und erklären zu können.

<!--
author: Thomas Stabla
version: 1.4.1
language: de
comment: Zusammenfassung und interaktive Übungen zu Feldern und Listen in Python für den Informatik-Grundkurs 11.
tags: Informatik, Python, Grundkurs 11, Feld, Liste
import: https://raw.githubusercontent.com/LiaScript/CodeRunner/master/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
-->

# Python 02: Felder in Python

## 1. Felder und Indizes

### Merkteil: Felder und Python-Listen

Ein **Feld (Array)** fasst mehrere Werte unter einem gemeinsamen Namen zusammen. Auf jedes Element kann über seine **Position (Index)** zugegriffen werden.

In Python verwenden wir dafür **Listen** (`list`). Die Indizes beginnen bei **0**.

**Beispiel:**

```python
x = 6 * [0]   # Liste mit sechs Nullen erzeugen
x[1] = 2     # Zweites Element verändern
x[4] = 4     # Fünftes Element verändern
print(x)     # [0, 2, 0, 0, 4, 0]
```

| Index | 0 | 1 | 2 | 3 | 4 | 5 |
|:-----:|:-:|:-:|:-:|:-:|:-:|:-:|
| Wert  | 0 | 2 | 0 | 0 | 4 | 0 |

- Mit `x[i]` liest man das Element mit dem Index `i`.
- Mit `x[i] = ...` verändert man dieses Element.
- `len(x)` gibt die **Anzahl der Elemente** an. Hier ist das Ergebnis `6`.
- Der letzte gültige Index ist deshalb `len(x) - 1`, also `5`. Der Zugriff auf `x[6]` würde einen Fehler (`IndexError`) auslösen.

**Unterschied:** Ein klassisches Feld hat normalerweise eine feste Anzahl von Elementen desselben Datentyps. Eine **Python-Liste** kann dagegen länger oder kürzer werden und auch Werte verschiedener Datentypen enthalten. In den folgenden Aufgaben nutzen wir Python-Listen wie Felder.

### Verständnisfragen

**1.** Bestimme den Wert von `len(x)` für `x = [3, 7, 2, 9]`.

[[4]]

**2.** Bestimme den Wert von `x[2]` für `x = [3, 7, 2, 9]`.

- [( )] `3`
- [( )] `7`
- [(X)] `2`
- [( )] `9`

**3.** Gib an, was bei `x[4]` passiert, wenn `x = [3, 7, 2, 9]` ist.

- [( )] Der Wert `9` wird ausgegeben.
- [(X)] Es tritt ein Fehler auf, weil der Index nicht vorhanden ist.
- [( )] Es wird automatisch ein fünftes Element angelegt.

**4.** Bestimme die Ausgabe des Programms.

```python
x = [3, 7, 2, 9]
x[1] = x[1] + 3
print(x)
```

- [( )] `[6, 7, 2, 9]`
- [(X)] `[3, 10, 2, 9]`
- [( )] `[3, 3, 2, 9]`
- [( )] `[6, 10, 5, 12]`

## 2. Felder mit Schleifen durchlaufen

### Merkteil: Index und Schleife

Mit einer **`for`-Schleife** lassen sich die Elemente einer Liste nacheinander lesen oder verändern. Dazu kann die Schleifenvariable die Indizes durchlaufen.

**Beispiel:**

```python
x = [1, 5, 2, 3, 4]
n = len(x)

for i in range(n):
    print(i, x[i])
```

**Ausgabe:**

```text
0 1
1 5
2 2
3 3
4 4
```

- `len(x)` liefert die Anzahl der Elemente (`5`).
- `range(n)` liefert die Indizes von `0` bis `n - 1`.
- `i` bezeichnet den aktuellen **Index**, `x[i]` den **Wert** an dieser Stelle.
- Mit `x[i] = ...` kann man Werte auch innerhalb der Schleife verändern.

### Verständnisfragen

**5.** Gib an, welche Indizes das Programm ausgibt.

```python
x = [4, 8, 12]
for i in range(len(x)):
    print(i)
```

- [(X)] `0`, `1`, `2`
- [( )] `1`, `2`, `3`
- [( )] `0`, `1`, `2`, `3`

**6.** Bestimme die Ausgabe des Programms.

```python
x = [4, 8, 12]
for i in range(len(x)):
    print(x[i])
```

- [( )] `0`, `1`, `2` (jeweils in einer neuen Zeile)
- [(X)] `4`, `8`, `12` (jeweils in einer neuen Zeile)
- [( )] `[4, 8, 12]` in einer Zeile

## 3. Programmierübungen

Bearbeite die Aufgaben, führe deine Programme aus und prüfe die Ergebnisse. Die Aufgaben 1–3 sind Pflichtaufgaben; die Aufgaben 4 und 5 sind Zusatzaufgaben. Falls du nicht weiterkommst, öffne die **Hilfen nacheinander**.

### Aufgabe 1: Summe berechnen

Gegeben ist die Liste `x = [3, 7, 2, 8, 5]`.

**Schreibe** ein Programm, das mit einer `for`-Schleife und einem Index die Summe aller Listenelemente berechnet und ausgibt. Verwende nicht `sum()`.

**Kontrolle:** Das Ergebnis ist `25`.

**Teste** dein fertiges Programm anschließend mit `x = [4, -1, 2]`. Ändere nur die Liste am Programmanfang. Das Ergebnis muss `5` sein.

```python
x = [3, 7, 2, 8, 5]

# Ergänze dein Programm.

```
@LIA.python3

<details>
<summary>Hilfe 1 – Anfangswert</summary>

Verwende eine Variable `summe`, in der du das bisherige Ergebnis speicherst. Mit welchem Anfangswert muss sie beginnen?

</details>

<details>
<summary>Hilfe 2 – Alle Elemente erreichen</summary>

Mit `for i in range(len(x)):` erreichst du nacheinander alle gültigen Indizes.

</details>

<details>
<summary>Hilfe 3 – Summe aktualisieren</summary>

Innerhalb der Schleife kannst du `summe = summe + x[i]` verwenden. Gib die Summe erst **nach** der Schleife aus.

</details>

<details>
<summary>Musterlösung – erst nach dem eigenen Versuch öffnen</summary>

```python
x = [3, 7, 2, 8, 5]
summe = 0

for i in range(len(x)):
    summe = summe + x[i]

print(summe)
```

Vor der Schleife ist die Summe noch 0. In jedem Durchlauf kommt ein Element hinzu. Die Ausgabe erfolgt erst nach dem letzten Durchlauf.

</details>

### Aufgabe 2: Alle Elemente verdoppeln

Gegeben ist die Liste `x = [2, 4, 6, 8, 10]`.

**Schreibe** ein Programm, das jedes Listenelement an seiner bisherigen Position verdoppelt. Gib anschließend die gesamte veränderte Liste aus.

**Kontrolle:** Die Ausgabe ist `[4, 8, 12, 16, 20]`.

**Teste** dein fertiges Programm anschließend mit `x = [-3, 0, 5]`. Ändere nur die Liste am Programmanfang. Die Ausgabe muss `[-6, 0, 10]` sein.

```python
x = [2, 4, 6, 8, 10]

# Ergänze dein Programm.

```
@LIA.python3

<details>
<summary>Hilfe 1 – Elemente verändern</summary>

Mit `print(x[i])` wird ein Wert nur angezeigt. Stattdessen muss der veränderte Wert wieder an derselben Position gespeichert werden.

</details>

<details>
<summary>Hilfe 2 – Alle Indizes verwenden</summary>

Nutze eine Schleife mit `for i in range(len(x)):`.

</details>

<details>
<summary>Hilfe 3 – Verdoppeln</summary>

Die Zuweisung `x[i] = 2 * x[i]` gehört **in** die Schleife. `print(x)` steht **nach** der Schleife.

</details>

<details>
<summary>Musterlösung – erst nach dem eigenen Versuch öffnen</summary>

```python
x = [2, 4, 6, 8, 10]

for i in range(len(x)):
    x[i] = 2 * x[i]

print(x)
```

Die Zuweisung ersetzt jedes Element durch seinen doppelten Wert. Die Länge der Liste bleibt dabei gleich.

</details>

### Aufgabe 3: Elemente zählen

Gegeben ist die Liste `x = [4, 12, 10, 18, 7, 11]`.

**Schreibe** ein Programm, das mit einer `for`-Schleife und einem Index zählt, wie viele Elemente größer als 10 sind. Gib die Anzahl aus. Der Wert 10 wird nicht mitgezählt.

**Kontrolle:** Das Ergebnis ist `3`.

**Teste** dein Programm anschließend mit `x = [10, -2, 8]`. Ändere nur die Liste am Programmanfang. Das Ergebnis muss `0` sein.

```python
x = [4, 12, 10, 18, 7, 11]

# Ergänze dein Programm.
```
@LIA.python3

<details>
<summary>Hilfe 1 – Zählen statt addieren</summary>

Speichere die Anzahl in einer Variablen `anzahl`. Zu Beginn ist noch kein passendes Element gefunden. Addiere später nicht den Elementwert, sondern zähle jeden Treffer einmal.

</details>

<details>
<summary>Hilfe 2 – Bedingung prüfen</summary>

Durchlaufe alle Indizes mit `for i in range(len(x)):`. Prüfe innerhalb der Schleife mit `if x[i] > 10:`, ob das aktuelle Element mitgezählt werden muss.

</details>

<details>
<summary>Hilfe 3 – Zähler erhöhen</summary>

Setze vor der Schleife `anzahl = 0`. Die Anweisung `anzahl = anzahl + 1` gehört in den eingerückten Block der Bedingung. Gib die Anzahl nach der Schleife aus.

</details>

<details>
<summary>Musterlösung – erst nach dem eigenen Versuch öffnen</summary>

```python
x = [4, 12, 10, 18, 7, 11]
anzahl = 0

for i in range(len(x)):
    if x[i] > 10:
        anzahl = anzahl + 1

print(anzahl)
```

Die Werte 12, 18 und 11 erfüllen die Bedingung. Für jeden Treffer steigt die Anzahl um 1. Die Elementwerte selbst werden nicht addiert.

</details>

### Aufgabe 4: Größtes Element bestimmen (Zusatzaufgabe)

Gegeben ist die Liste `x = [12, 5, 19, 7, 14]`.

**Schreibe** ein Programm, das mit einer Schleife das größte Element bestimmt und ausgibt. Verwende nicht `max()`.

**Kontrolle:** Das Ergebnis ist `19`.

**Teste** dein fertiges Programm anschließend mit `x = [-12, -5, -19, -7]`. Ändere nur die Liste am Programmanfang. Das Ergebnis muss `-5` sein.

```python
x = [12, 5, 19, 7, 14]

# Ergänze dein Programm.

```
@LIA.python3

<details>
<summary>Hilfe 1 – Startwert festlegen</summary>

Nimm zunächst an, dass das erste Element das größte ist. Speichere seinen Wert in einer Variablen `groesstes`.

</details>

<details>
<summary>Hilfe 2 – Werte vergleichen</summary>

Vergleiche jedes Listenelement mit `groesstes`. Falls ein Element größer ist, muss der bisher gespeicherte Wert ersetzt werden.

</details>

<details>
<summary>Hilfe 3 – Bedingungen und Schleifen kombinieren</summary>

Beginne mit `groesstes = x[0]`. Durchlaufe die Indizes mit einer `for`-Schleife und prüfe `if x[i] > groesstes:`. Speichere in diesem Fall den neuen größten Wert. Gib das Ergebnis nach der Schleife aus.

</details>

<details>
<summary>Musterlösung – erst nach dem eigenen Versuch öffnen</summary>

```python
x = [12, 5, 19, 7, 14]
groesstes = x[0]

for i in range(len(x)):
    if x[i] > groesstes:
        groesstes = x[i]

print(groesstes)
```

Als Startwert wird das erste Element verwendet. So funktioniert das Programm auch bei ausschließlich negativen Werten. Ein Startwert von 0 wäre dafür ungeeignet. Die Liste muss mindestens ein Element enthalten. Der erneute Vergleich des ersten Elements mit sich selbst ist unschädlich.

</details>

### Aufgabe 5: Sortierung prüfen (Zusatzaufgabe)

Gegeben ist die Liste `x = [2, 4, 4, 7, 10]`.

**Schreibe** ein Programm, das mit einer Schleife und Indizes prüft, ob die Liste aufsteigend sortiert ist. Gleiche benachbarte Werte sind erlaubt. Gib `"sortiert"` oder `"nicht sortiert"` aus. Verändere die Liste nicht und verwende weder `sort()` noch `sorted()`.

**Kontrolle:** Die Ausgabe ist `sortiert`.

**Teste** dein Programm anschließend mit `x = [2, 6, 4, 7]`. Die Ausgabe muss `nicht sortiert` sein. Prüfe außerdem `x = [3, 3]` und `x = [5]`: Beide gelten als sortiert.

```python
x = [2, 4, 4, 7, 10]

# Ergänze dein Programm.
```
@LIA.python3

<details>
<summary>Hilfe 1 – Benachbarte Werte vergleichen</summary>

Vergleiche jedes Element mit seinem direkten Nachfolger. Sobald der linke Wert größer als der rechte ist, steht fest: Die Liste ist nicht aufsteigend sortiert.

</details>

<details>
<summary>Hilfe 2 – Schleifengrenze wählen</summary>

Die Nachbarn sind `x[i]` und `x[i + 1]`. Der letzte mögliche linke Index ist `len(x) - 2`. Verwende deshalb `range(len(x) - 1)`, damit der Zugriff auf den Nachfolger gültig bleibt.

</details>

<details>
<summary>Hilfe 3 – Ergebnis merken</summary>

Beginne mit `ist_sortiert = True`. Setze die Variable bei `if x[i] > x[i + 1]:` auf `False`. Setze sie bei einem späteren passenden Paar nicht wieder auf `True`. Entscheide nach der Schleife mit `if/else`, welchen Text du ausgibst.

</details>

<details>
<summary>Musterlösung – erst nach dem eigenen Versuch öffnen</summary>

```python
x = [2, 4, 4, 7, 10]
ist_sortiert = True

for i in range(len(x) - 1):
    if x[i] > x[i + 1]:
        ist_sortiert = False

if ist_sortiert:
    print("sortiert")
else:
    print("nicht sortiert")
```

`ist_sortiert` speichert einen Wahrheitswert: `True` bedeutet wahr, `False` bedeutet falsch. Ein einziges absteigendes Nachbarpaar reicht aus, um die Sortierung zu widerlegen. Gleiche Werte sind erlaubt, deshalb wird mit `>` geprüft. Bei einem einzelnen Element gibt es kein Nachbarpaar; die Liste gilt als sortiert.

</details>

### Abschlusscheck

**7.** Unterscheide die Bedeutung von `i` und `x[i]`.

- [(X)] `i` ist der Index; `x[i]` ist der Wert an dieser Position.
- [( )] `i` ist der Wert; `x[i]` ist der Index.
- [( )] Beide bezeichnen immer denselben Wert.

**8. Erkläre**, warum die Schleife `for i in range(len(x)):` auch dann alle Elemente erreicht, wenn du vor einem erneuten Programmstart eine längere oder kürzere Liste einträgst.

<details>
<summary>Erklärung anzeigen</summary>

`len(x)` bestimmt bei jedem Programmstart die Anzahl der Elemente der eingetragenen Liste. `range(len(x))` umfasst dann genau die Indizes von `0` bis `len(x) - 1`. Eine fest eingetragene Anzahl würde sich nicht an die neue Listenlänge anpassen: Elemente könnten ausgelassen werden oder es könnte ein `IndexError` auftreten.

Dabei bleibt die Listenlänge während der Schleife unverändert. Das Verändern von Elementwerten wie in Aufgabe 2 verändert die Länge nicht.

</details>

**9.** Wähle die passende Erklärung: Warum steht `summe = 0` in Aufgabe 1 vor der Schleife?

- [( )] Weil Variablen innerhalb einer Schleife nicht verändert werden dürfen.
- [(X)] Weil die Summe einmal mit 0 beginnen und anschließend über alle Durchläufe erhalten bleiben muss.
- [( )] Weil eine Schleife nur funktioniert, wenn vorher eine Variable auf 0 gesetzt wurde.

<details>
<summary>Erklärung anzeigen</summary>

Würde `summe = 0` am Anfang jedes Schleifendurchlaufs stehen, ginge die bisher berechnete Summe jedes Mal verloren. Nach dem Addieren bliebe dann nur der Wert des aktuellen Elements übrig. Bei der Liste aus Aufgabe 1 wäre die abschließende Ausgabe 5 statt 25.

</details>

## 4. Bearbeitungsstand sichern

**Sichere** zum Abschluss deinen Bearbeitungsstand:

1. Trage unten deinen Namen ein und erstelle einen Abgabelink.
2. Kopiere den vollständigen Link und bewahre ihn auf, zum Beispiel in deinen persönlichen Notizen.
3. Öffne den Link zur Kontrolle in einem neuen Tab. Prüfe, ob deine Antworten angezeigt werden.

Der Link zeigt einen **eingefrorenen Stand zur Ansicht**, keine bearbeitbare Fortsetzung des Kurses. Für weiteres Arbeiten verwende den ursprünglichen Kurs.

**Speichere deine Python-Programme zusätzlich als eigene Dateien**, zum Beispiel durch Kopieren nach Thonny und Speichern als `.py`. Verlasse dich für die Sicherung der Codefelder nicht allein auf den Abgabelink.

@Abgabe

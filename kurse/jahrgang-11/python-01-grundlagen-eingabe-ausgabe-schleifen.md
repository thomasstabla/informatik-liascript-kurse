<!--
author: Thomas Stabla
version: 1.1.0
language: de
comment: Interaktiver Einstieg in Python-Grundlagen für eine 90-minütige Unterrichtseinheit in Klasse 11.
tags: Informatik, Python, Klasse 11, Grundlagen, Kurs
import: https://raw.githubusercontent.com/LiaScript/CodeRunner/master/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-navigation/0.0.2/README.md
import: https://raw.githubusercontent.com/liaTemplates/Random/master/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
-->

# Python 01: Grundlagen – Eingabe, Ausgabe und Schleifen

<article>

In dieser Kursaufgabe wiederholst und übst du grundlegende Python-Bausteine. Bearbeite die fünf Unterkapitel der Reihe nach. Lies den Beispielcode, überlege zuerst selbst, was passiert, und probiere ihn anschließend aus.

Die Codefelder lassen sich im Browser bearbeiten und ausführen. Dafür ist eine Internetverbindung erforderlich. Die Ausführung wird von einem externen CodeRunner-Dienst bereitgestellt.

**Ziel:** Du kannst einfache Programme mit `print`, `input`, Variablen, `if/else`, `for` und `while` lesen und schreiben.

**So arbeitest du:** Die Aufgaben mit **Basis** bearbeitest du zuerst. **Zusatz** ist freiwillig und für dich gedacht, wenn du schneller fertig bist oder eine größere Herausforderung suchst. Nutze Hilfestellungen erst, wenn du selbst einen Lösungsweg versucht hast.

**Sichere deine Programme:** Lege eine Textdatei mit dem Namen `Python_Grundlagen_Nachname.txt` an. Kopiere nach jeder Programmieraufgabe deinen getesteten Code hinein und versehe ihn mit einer Überschrift, zum Beispiel `1. Speisekarte` oder `2. Getränkeautomat`. Speichere die Datei in deinem persönlichen Schulordner oder bei LernSax.

### Einstiegscheck: Was kannst du schon?

Löse die drei kurzen Aufgaben zunächst ohne Hilfe. Der Check ist keine Note. Er zeigt dir, bei welchen Grundlagen du besonders aufmerksam arbeiten solltest.

Was gibt dieses Programm aus?

```python
print(2 + 3)
print("2 + 3")
```

- [( )] Zweimal die Zahl 5
- [(X)] Erst 5, darunter der Text 2 + 3
- [( )] Erst 2 + 3, darunter 5

Welche Zahl wird ausgegeben?

```python
punkte = 4
punkte = punkte + 3
print(punkte)
```

[[7]]

Wie oft wird `Runde` ausgegeben?

```python
for nummer in range(1, 4):
    print("Runde")
```

- [( )] Einmal
- [( )] Viermal
- [(X)] Dreimal

Wenn du bei einer Aufgabe unsicher warst, ist das völlig in Ordnung: Bearbeite die Beispiele im passenden Kapitel besonders sorgfältig.

</article>

## Ausgabe

<article>

Mit `print(...)` gibt ein Programm Text oder berechnete Werte aus. Mehrere `print`-Anweisungen erzeugen mehrere Zeilen.

```python
print("Fahrplan")
print(4 + 3)
```
@LIA.python3

### Basis-Check: Was ist die Ausgabe?

Was gibt dieses Programm aus?

```python
print("Bus")
print(6 * 2)
```

- [(X)] Bus und darunter 12
- [( )] Bus12 in einer Zeile
- [( )] Bus und darunter 6 * 2

### Basis-Check: Was ist die Ausgabe?

Welche Zahl wird ausgegeben?

```python
print(18 - 7)
```

[[11]]

### Basisaufgabe: Speisekarte

Ein Imbiss möchte auf einem Bildschirm drei Angebote anzeigen. Ergänze die beiden fehlenden Angebote. Die Ausgabe soll genau drei Zeilen enthalten:

- Suppe: 4 Euro
- Sandwich: 5 Euro
- Tee: 2 Euro

```python
print("Suppe: 4 Euro")

```
@LIA.python3

<details>
<summary>Hilfestellung öffnen</summary>

Ergänze für jedes fehlende Angebot eine eigene `print(...)`-Anweisung. Achte darauf, den Text in Anführungszeichen zu setzen.

</details>

### Prüfe deine Speisekarte

Führe dein Programm aus und vergleiche die Ausgabe mit der Sollausgabe. Achte auf die drei Zeilen, die Namen und die Preise.

```text
Suppe: 4 Euro
Sandwich: 5 Euro
Tee: 2 Euro
```

### Zusatz: Preisübersicht erweitern

Ergänze die Speisekarte um ein viertes Angebot deiner Wahl. Gib zusätzlich eine Zeile aus, die den Gesamtpreis aller vier Angebote berechnet. Du darfst die Preise direkt in einer Rechnung verwenden.

```python
print("Suppe: 4 Euro")
print("Sandwich: 5 Euro")
print("Tee: 2 Euro")
# Ergänze ein viertes Angebot und berechne die Summe.
```
@LIA.python3

<details>
<summary>Hilfestellung öffnen</summary>

Lege den Preis deines vierten Angebots fest. Addiere diesen Preis zu 4, 5 und 2 und gib die Summe mit `print` aus.

</details>

</article>

## Eingabe und Variablen

<article>

Eine Variable speichert einen Wert unter einem Namen. `input(...)` fragt eine Eingabe ab. Die Eingabe ist zunächst Text. Für eine Rechnung mit einer ganzen Zahl verwendest du `int(...)`.

```python
name = input("Wie heißt du? ")
print("Willkommen,", name)
```
@LIA.python3_withShell

### Werte zuweisen und verändern

Bei einer Zuweisung wird zuerst die rechte Seite ausgewertet. Danach ersetzt das Ergebnis den bisherigen Wert der Variablen. `=` bedeutet hier also eine Zuweisung, keine mathematische Gleichung.

```python
punkte = 5
punkte = punkte + 2
print(punkte)
```
@LIA.python3

| Anweisung | Wert von `punkte` danach |
| --- | --- |
| `punkte = 5` | 5 |
| `punkte = punkte + 2` | 7 |

### Zahlen eingeben

`int(...)` wandelt einen passenden Text in eine ganze Zahl um. Gib bei den Zahlenabfragen dieses Kurses ganze Zahlen ein; Texte wie `drei` oder `2.5` führen bei `int(...)` zu einem `ValueError`.

Bei Zahlen:

```python
anzahl = int(input("Wie viele Brötchen? "))
preis = anzahl * 2
print("Preis in Euro:", preis)
```
@LIA.python3_withShell

### Basis-Check: Was ist die Ausgabe?

Du gibst `Mia` ein. Welche Ausgabe erzeugt anschließend die `print`-Anweisung?

```python
name = input("Name: ")
print("Hallo", name)
```

- [( )] HalloName: Mia
- [(X)] Hallo Mia
- [( )] name Mia

### Basis-Check: Was ist die Ausgabe?

Welcher Gesamtpreis wird ausgegeben?

```python
anzahl = 3
preis_pro_heft = 2
print(anzahl * preis_pro_heft)
```

[[6]]

### Basisaufgabe: Getränkeautomat

Ein Getränkeautomat verkauft Wasserflaschen für 2 Euro. Frage nach der gewünschten Anzahl und gib den Gesamtpreis aus. Verwende eine Variable für die Anzahl und eine für den Gesamtpreis.

Versuche zuerst, das Programm selbst zu ergänzen. Nutze die Hilfestellungen bei Bedarf der Reihe nach.

```python
anzahl = int(input("Wie viele Flaschen möchtest du? "))

```
@LIA.python3_withShell

<details>
<summary>Hilfestellung 1 öffnen</summary>

Wie hängt der Preis von der Anzahl der Flaschen ab? Überlege zunächst für drei Flaschen.

</details>

<details>
<summary>Hilfestellung 2 öffnen</summary>

Multipliziere die eingegebene Anzahl mit dem Preis einer Flasche. Eine zusätzliche Variable für den Einzelpreis ist möglich, aber nicht nötig.

</details>

<details>
<summary>Hilfestellung 3 öffnen</summary>

Speichere das Rechenergebnis in einer Variablen für den Gesamtpreis. Gib diese mit einer Beschriftung durch `print(...)` aus.

</details>

**Teste:** 0 Flaschen → 0 Euro; 1 Flasche → 2 Euro; 3 Flaschen → 6 Euro.

### Zusatz: Pfand berechnen

Erweitere deinen Getränkeautomaten: Eine Wasserflasche kostet 2 Euro. Frage zusätzlich, wie viele leere Flaschen zurückgegeben werden. Für jede zurückgegebene Flasche werden 25 Cent gutgeschrieben. Die 2 Euro enthalten bereits das Pfand. Berechne den Gesamtpreis in Cent und gib ihn aus. Ein negativer Betrag bedeutet, dass du Geld zurückbekommst.

**Teste:** Kauf von 2 Flaschen und Rückgabe von 3 Flaschen → 325 Cent; Kauf von 0 Flaschen und Rückgabe von 1 Flasche → −25 Cent.

```python
anzahl = int(input("Wie viele Wasserflaschen möchtest du kaufen? "))
zurueck = int(input("Wie viele leere Flaschen gibst du zurück? "))

```
@LIA.python3_withShell

<details>
<summary>Hilfestellung öffnen</summary>

Berechne den Flaschenpreis in Cent (`anzahl * 200`). Ziehe davon die Pfandgutschrift (`zurueck * 25`) ab.

</details>

</article>

## If/else

<article>

Mit `if` prüft ein Programm eine Bedingung. Ist sie wahr, wird der eingerückte Block ausgeführt. Andernfalls wird der eingerückte Block nach `else` ausgeführt.

Mit Vergleichsoperatoren formulierst du Bedingungen:

| Operator | Bedeutung |
| --- | --- |
| `==` | gleich |
| `!=` | ungleich |
| `<` / `>` | kleiner / größer |
| `<=` / `>=` | kleiner oder gleich / größer oder gleich |

**Merke:** `=` weist einen Wert zu, `==` vergleicht zwei Werte. Nach `if` und `else` steht ein Doppelpunkt. Die zugehörigen Anweisungen werden gleich weit eingerückt, üblicherweise um vier Leerzeichen.

Ändere im Beispiel den Wert von `temperatur` zuerst auf `12` und führe das Programm aus. Ändere ihn danach auf `3`. Überlege vorher, welche Ausgabe jeweils erscheint und welcher Zweig ausgeführt wird.

```python
temperatur = 8

if temperatur < 10:
    print("Jacke anziehen")
else:
    print("Leichte Kleidung reicht")
```
@LIA.python3

### Basis-Check: Was ist die Ausgabe?

```python
punkte = 12

if punkte >= 10:
    print("Ziel erreicht")
else:
    print("Noch üben")
```

- [(X)] Ziel erreicht
- [( )] Noch üben
- [( )] Das Programm gibt beide Texte aus.

### Basis-Check: Was ist die Ausgabe?

Welche einzelne Zahl wird ausgegeben?

```python
temperatur = 3

if temperatur < 0:
    print(0)
else:
    print(1)
```

[[1]]

### Basis-Check: Fehler finden – Einrückung

Das Programm soll abhängig von der Temperatur einen passenden Hinweis ausgeben. Es enthält einen Fehler. Korrigiere den Code im Editor und führe ihn aus.

```python
temperatur = 8

if temperatur < 10:
print("Jacke anziehen")
else:
print("Leichte Kleidung reicht")
```
@LIA.python3

### Basisaufgabe: Regen oder Sonne?

Frage nach dem Wetter (`regen` oder `sonne`). Wenn `regen` eingegeben wird, soll das Programm `Regenschirm mitnehmen` ausgeben; sonst `Sonnenbrille einpacken`.

```python
wetter = input("Wie ist das Wetter? ")

pass  # Ersetze pass durch if und else.

```
@LIA.python3_withShell

<details>
<summary>Hilfestellung 1 öffnen</summary>

Vergleiche `wetter` mit dem Text `"regen"`. Achte auf `==` für einen Vergleich und `=` zum Zuweisen eines Wertes.

</details>

<details>
<summary>Hilfestellung 2 öffnen</summary>

Der `if`-Zweig gibt den Regenschirm-Hinweis aus. Der `else`-Zweig gibt den Hinweis für die Sonnenbrille aus. Beide `print`-Zeilen müssen eingerückt sein.

</details>

### Zusatz: Versandkosten

**Testfälle:** Warenwert 39 Euro → 44 Euro Gesamtbetrag; 40 Euro → 40 Euro; 41 Euro → 41 Euro.

Frage nach dem Warenwert in ganzen Euro. Ab 40 Euro ist der Versand kostenlos. Bei einem niedrigeren Warenwert kommen 5 Euro Versandkosten hinzu. Gib den Gesamtbetrag aus.

```python
warenwert = int(input("Warenwert in Euro? "))

```
@LIA.python3_withShell

<details>
<summary>Hilfestellung öffnen</summary>

Speichere den Warenwert als ganze Zahl. Verwende `if warenwert >= 40` und berechne in den beiden Zweigen jeweils den Gesamtbetrag.

</details>

</article>

## For-Schleife

<article>

Eine `for`-Schleife wiederholt einen Anweisungsblock für die Werte einer Folge. `range(1, 4)` liefert die Zahlen 1, 2 und 3. Die obere Grenze 4 gehört nicht mehr dazu.

```python
for nummer in range(1, 4):
    print(nummer)
```
@LIA.python3

Mit nur einer Grenze beginnt `range` bei 0:

| Ausdruck | Werte | Anzahl |
| --- | --- | --- |
| `range(4)` | 0, 1, 2, 3 | 4 |
| `range(1, 4)` | 1, 2, 3 | 3 |

`range(n)` ermöglicht bei einer nichtnegativen ganzen Zahl `n` genau `n` Durchläufe. Bei `n = 0` wird der Schleifenblock nicht ausgeführt.

### Basis-Check: Was ist die Ausgabe?

```python
for runde in range(1, 4):
    print("Runde", runde)
```

- [( )] Runde 1, Runde 2, Runde 3 und Runde 4
- [(X)] Drei Zeilen: Runde 1, Runde 2 und Runde 3
- [( )] Eine Zeile: Runde 123

### Eine Summe schrittweise aufbauen

```python
summe = 0
for zahl in range(1, 4):
    summe = summe + zahl
print(summe)
```
@LIA.python3

| Durchlauf | `zahl` | `summe` vorher | `summe` danach |
| --- | --- | --- | --- |
| 1 | 1 | 0 | 1 |
| 2 | 2 | 1 | 3 |
| 3 | 3 | 3 | 6 |

Die Startzuweisung steht vor der Schleife, damit die bisherige Summe erhalten bleibt. Die Ausgabe steht nach der Schleife und zeigt das Endergebnis.

### Basis-Check: Eine andere Summe

Welche Zahl wird nach der Schleife ausgegeben?

```python
summe = 0

for zahl in range(2, 5):
    summe = summe + zahl

print(summe)
```

[[9]]

### Basisaufgabe: Garderobenmarken nummerieren

Für eine Veranstaltung sollen die Garderobenmarken 101 bis 104 ausgegeben werden. Schreibe eine `for`-Schleife, die diese vier Zeilen erzeugt: `Marke 101`, `Marke 102`, `Marke 103` und `Marke 104`.

```python
pass  # Ersetze pass durch eine for-Schleife.

```
@LIA.python3

### Ausgabe prüfen

Führe dein Programm aus und vergleiche die tatsächliche Ausgabe mit der Sollausgabe oben. Achte darauf, dass genau vier Zeilen mit den Nummern 101 bis 104 erscheinen.

<details>
<summary>Hilfestellung 1 öffnen</summary>

Welche Nummer soll zuerst erscheinen, welche zuletzt?

</details>

<details>
<summary>Hilfestellung 2 öffnen</summary>

Die obere Grenze von `range` gehört nicht mehr zu den ausgegebenen Werten.

</details>

<details>
<summary>Hilfestellung 3 öffnen</summary>

Wähle 101 als Start und eine Grenze unmittelbar nach 104. Gib im Schleifenblock den Text `Marke` und die Schleifenvariable mit `print(...)` aus.

</details>

### Zusatz: Summe von 100 bis 200

Berechne mit einer `for`-Schleife die Summe aller ganzen Zahlen von 100 bis einschließlich 200 und gib das Ergebnis aus.

```python
summe = 0

```
@LIA.python3_withShell

<details>
<summary>Hilfestellung 1 öffnen</summary>

Beginne mit einer Variablen `summe = 0`. In jedem Schleifendurchlauf wird eine Zahl zu dieser Summe addiert.

</details>

<details>
<summary>Hilfestellung 2 öffnen</summary>

Die Schleifenvariable soll nacheinander die Werte 100 bis einschließlich 200 annehmen. Beachte, dass `range` die obere Grenze nicht mitzählt.

</details>

</article>

## While-Schleife

<article>

Eine `while`-Schleife prüft ihre Bedingung vor jedem Durchlauf. Solange sie wahr ist, wird der Schleifenblock ausgeführt. Ist sie schon am Anfang falsch, gibt es keinen Durchlauf. Damit die Schleife endet, muss die Bedingung irgendwann falsch werden. Im folgenden Beispiel geschieht das durch das Verringern von `sekunden`.

```python
import time

sekunden = 3

while sekunden > 0:
    print(sekunden)
    time.sleep(1)
    sekunden = sekunden - 1

print("Start!")
```
@LIA.python3

`time.sleep(1)` pausiert das Programm für eine Sekunde. Dafür wird das Modul `time` am Programmanfang importiert.

### Basis-Check: Was ist die Ausgabe?

Bei jedem Aufruf wird eine der folgenden Varianten ausgewählt. Berechne die Ausgabe und trage die Zahl in das Eingabefeld ein.

@Random.random(1, false)

<div class="random">

```python
stand = 1

while stand < 1:
    stand = stand + 1

print(stand)
```

Welche Zahl wird ausgegeben?

[[1]]

</div>

<div class="random">

```python
stand = 1

while stand < 3:
    stand = stand + 1

print(stand)
```

Welche Zahl wird ausgegeben?

[[3]]

</div>

<div class="random">

```python
stand = 1

while stand < 4:
    stand = stand + 2

print(stand)
```

Welche Zahl wird ausgegeben?

[[5]]

</div>

<div class="random">

```python
stand = 1

while stand < 5:
    stand = stand + 3

print(stand)
```

Welche Zahl wird ausgegeben?

[[7]]

</div>

### Basis-Check: Was ist die letzte ausgegebene Zahl?

```python
schritte = 0

while schritte < 5:
    schritte = schritte + 2
    print(schritte)
```

[[6]]

### Basis-Check: Kein Durchlauf?

Wie oft wird `Los` ausgegeben?

```python
rest = 0
while rest > 0:
    print("Los")
    rest = rest - 1
```

[[0]]

### Basisaufgabe: Sparziel

Du legst jeden Monat 5 Euro zurück. Schreibe ein Programm mit einer `while`-Schleife, das den Kontostand nach jedem Monat ausgibt, bis mindestens 20 Euro erreicht sind.

```python
kontostand = 0

pass  # Ersetze pass durch eine while-Schleife.

```
@LIA.python3

<details>
<summary>Hilfestellung öffnen</summary>

Solange der Kontostand kleiner als 20 ist, addierst du 5 Euro. Gib den neuen Kontostand innerhalb der Schleife aus.

</details>

**Prüfe dein Sparziel:** Die Ausgabe muss nacheinander 5, 10, 15 und 20 zeigen. Ändere zum Test das Ziel auf 22 Euro: Dann muss der letzte Kontostand 25 Euro sein.

### Zusatz: Passwortversuche zählen

Mit `and` verknüpfst du zwei Bedingungen: Beide müssen wahr sein. Beispiel: `alter >= 12 and alter < 18` trifft auf ein Alter von 12 bis 17 Jahren zu. `!=` bedeutet „ungleich“.

Ein Programm erlaubt drei Versuche, ein Passwort einzugeben. Lege das richtige Passwort in einer Variablen fest. Wiederhole die Eingabe mit einer `while`-Schleife, solange das Passwort falsch ist und noch Versuche übrig sind. Gib anschließend aus, ob der Zugang erlaubt ist.

```python
richtiges_passwort = "python11"
versuche = 0

```
@LIA.python3_withShell

<details>
<summary>Hilfestellung 1 öffnen</summary>

Lege vor der Schleife eine Eingabevariable mit dem leeren Text `""` an. Die Schleife läuft, solange die Eingabe falsch ist **und** der Zähler kleiner als 3 ist.

</details>

<details>
<summary>Hilfestellung 2 öffnen</summary>

Frage innerhalb der Schleife das Passwort ab und erhöhe danach den Zähler um 1. Nach der Schleife prüfst du mit `if/else`, ob das Passwort richtig war.

</details>

### Zusatz / Transfer: Kinokasse

Diese freiwillige Challenge verbindet die bisherigen Bausteine. Entwickle dein Programm in drei Schritten und teste nach jedem Schritt:

1. **Ticketpreis:** Frage zunächst das Alter einer einzelnen Person ab und gib ihren Ticketpreis aus. Teste 17 Jahre → 6 Euro und 18 Jahre → 10 Euro.
2. **Gesamtsumme:** Frage nach der Personenzahl, wiederhole die Altersabfrage und sammle die Ticketpreise in einer Summe.
3. **Erweiterung:** Ergänze die erneute Abfrage bei ungültiger Personenzahl und den Gruppenrabatt.

Das fertige Programm soll diese Anforderungen erfüllen:

1. Frage nach der Anzahl der Personen. Frage bei 0 und negativen Zahlen erneut. Du darfst voraussetzen, dass ganze Zahlen eingegeben werden.
2. Frage für jede Person nach dem Alter.
3. Ein Ticket kostet für Personen unter 18 Jahren 6 Euro, sonst 10 Euro.
4. Addiere alle Ticketpreise und gib die Gesamtsumme aus.
5. Ab 50 Euro Gesamtpreis gibt es 5 Euro Gruppenrabatt. Gib dann den rabattierten Preis aus.

**Testfälle für das fertige Programm:**

| Personen und Alter | Summe vor Rabatt | Endpreis |
| --- | --- | --- |
| 2 Personen: 17, 18 | 16 Euro | 16 Euro |
| 5 Personen: jeweils 18 | 50 Euro | 45 Euro |
| 6 Personen: jeweils 18 | 60 Euro | 55 Euro |

Teste zusätzlich die Eingabefolge 0, −2, 1 bei der Personenzahl: Erst 1 darf akzeptiert werden.

Verwende dafür `input`, Variablen, `if/else`, eine `for`-Schleife und eine `while`-Schleife. Die Lösung steht nicht im Kursfeld: Entwickle sie selbst und teste sie mit verschiedenen Eingaben.

```python
anzahl = int(input("Wie viele Personen? "))

```
@LIA.python3_withShell

<details>
<summary>Hilfestellung 1 öffnen</summary>

Setze vor der Eingabeschleife die Gesamtsumme auf 0. Verwende `while anzahl <= 0`, um eine ungültige Anzahl erneut abzufragen.

</details>

<details>
<summary>Hilfestellung 2 öffnen</summary>

Verwende danach `for person in range(anzahl)`. In jedem Durchlauf fragst du ein Alter ab und entscheidest mit `if/else` über den Ticketpreis.

</details>

<details>
<summary>Hilfestellung 3 öffnen</summary>

Addiere den Preis jeder Person sofort zur Gesamtsumme. Prüfe nach der Schleife, ob die Summe mindestens 50 Euro beträgt.

</details>

### Rückblick

Ordne jedem Problem den passenden Baustein zu. Wähle in jeder Zeile genau eine Möglichkeit aus.

[[print] [input] [if/else] [for] [while]]
[ ( ) ( ) ( ) (X) ( ) ] Eine feste Anzahl von Wiederholungen ausführen
[ (X) ( ) ( ) ( ) ( ) ] Einen Text auf dem Bildschirm anzeigen
[ ( ) (X) ( ) ( ) ( ) ] Einen Wert von einer Person abfragen
[ ( ) ( ) ( ) ( ) (X) ] Wiederholen, solange eine Bedingung gilt
[ ( ) ( ) (X) ( ) ( ) ] Zwischen zwei Möglichkeiten entscheiden


**Prüfe dich:** Kannst du bei einem kurzen Programm zuerst die Ausgabe vorhersagen und es danach im Browser ausführen? Kannst du erklären, wann eine `for`- und wann eine `while`-Schleife sinnvoll ist?

**Erkläre mit eigenen Worten:** Warum muss sich in einer `while`-Schleife häufig der Wert einer Variablen ändern? Notiere deine Erklärung oder tausche dich mit einer Partnerin oder einem Partner aus.

Wenn bei einer Codeausführung eine Verbindungsmeldung erscheint oder der Start lange dauert, sichere zuerst deinen bearbeiteten Code. Lade danach die Kursseite neu und probiere es erneut. Der CodeRunner führt Python auf einem externen Server aus; ohne Verbindung zu diesem Dienst funktionieren die Codefelder nicht.

</article>

## Arbeitsstand sichern und abgeben

Erzeuge mit dem folgenden Feld einen Abgabelink und kopiere ihn in deinen Schulordner oder deine Abgabe bei LernSax. Öffne den Link zur Kontrolle und prüfe deinen gespeicherten Arbeitsstand. Bewahre deine Programme zusätzlich in der Textdatei auf, damit du sie unabhängig vom Kurs weiterverwenden kannst.

@Abgabe

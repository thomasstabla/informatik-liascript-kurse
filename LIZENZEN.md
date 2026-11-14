# Lizenzprüfung

Geprüft am 14.11.2026 anhand der beiden Kursdateien und der jeweils eingebundenen Upstream-Dateien. Diese Übersicht dokumentiert den gefundenen Stand; sie ist keine Rechtsberatung.

## Eigene Kursmaterialien

Die beiden Markdown-Dateien enthalten Unterrichtserklärungen, Aufgaben und kurze Python-Beispiele. Ich habe keine eingebetteten Bilder, längeren Zitate oder erkennbar übernommenen fremden Unterrichtstexte gefunden. Die Beispiele behandeln übliche Python-Grundlagen; eine Websuche nach markanten Formulierungen ergab keine passende 1:1-Quelle.

Im Repository liegt keine `LICENSE`-Datei. Damit wird für die eigenen Kursmaterialien keine ausdrückliche freie Weiterverwendungslizenz erteilt. Eine repoweite Lizenz sollte erst ergänzt werden, wenn die Rechte an allen enthaltenen Bestandteilen geklärt sind.

## Direkt eingebundene Erweiterungen

| Erweiterung | Verwendet in | Gefundener Lizenzstand |
|---|---|---|
| [LiaScript CodeRunner](https://github.com/LiaScript/CodeRunner) | Python 01 und 02 | Die Upstream-Datei `LICENSE` enthält CC0 1.0 Universal. |
| [LiaTemplates Random](https://github.com/liaTemplates/Random) | Python 01 | Die Upstream-Datei `LICENSE` enthält CC0 1.0 Universal. Das Upstream-README setzt außerdem ein Wikimedia-Bild als Logo. Dieses Bild ist nicht in diesem Repo gespeichert; seine konkrete Lizenz habe ich nicht bestätigt. |
| [MINT-the-GAP lia-navigation](https://github.com/MINT-the-GAP/lia-navigation/tree/0.0.2) | Python 01 | Der verwendete Tag 0.0.2 enthält keine auffindbare `LICENSE`-Datei und nennt im README keine Lizenz. Weiterverwendungslizenz daher ungeklärt. |
| [MINT-the-GAP lia-board-mode](https://github.com/MINT-the-GAP/lia-board-mode) | Python 02 | Die LiaScript-Projektseite nennt MIT. Im geprüften Upstream-Repo fand ich keine Root-`LICENSE`-Datei. Der Kurs importiert den veränderlichen Branch `main`. |
| [MINT-the-GAP lia-freeze-v2](https://github.com/MINT-the-GAP/lia-freeze-v2) | Python 02 | Die LiaScript-Projektseite nennt MIT. Im geprüften Upstream-Repo fand ich keine Root-`LICENSE`-Datei. Der Kurs importiert den veränderlichen Branch `main`. |

CodeRunner, Random und die MINT-Erweiterungen werden über `import:` von ihren jeweiligen Upstream-Adressen geladen; ihre Implementierungen sind nicht in dieses Repository kopiert.

## Zusätzliche Importe durch lia-freeze-v2

Das aktuelle README von `lia-freeze-v2/main`, das die Abgabe-Funktion bereitstellt, bindet selbst weitere Erweiterungen ein: LiaTemplates JSXGraph sowie MINT-the-GAP lia-DynFlex, lia-annotation, lia-canvas-ocr, lia-coordinate, lia-Mathe, lia-orthography und lia-marker. Für mehrere dieser Repositories war im geprüften Stand keine Lizenzdatei oder klare Lizenzangabe auffindbar. Einzelne Erweiterungen nennen zudem Inhalte mit eigenen Bedingungen (beispielsweise Wörterbuchinhalte aus Wiktionary oder FormulaNet).

Deshalb ist die Lizenzlage der gesamten Laufzeit-Abhängigkeitskette noch nicht vollständig geklärt. Die Import-URLs von `main` und `master` können sich ändern; ein Lizenzcheck sollte sich auf konkrete Versionen oder Commit-Hashes beziehen.

## Empfohlene Klärung

- Für `lia-navigation` die Lizenz beim Projektteam erfragen oder den Import entfernen.
- Für `lia-freeze-v2` und seine zusätzlichen Importe die Lizenzlage anhand einer festgelegten Version bestätigen lassen.
- Das Wikimedia-Logo der Random-Erweiterung prüfen oder den Logo-Eintrag der Erweiterung vor Verwendung überschreiben.
- Erst danach entscheiden, ob und unter welcher Lizenz die eigenen Kursmaterialien freigegeben werden sollen.

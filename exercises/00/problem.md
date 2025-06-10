# Du hast es zu Aufgabe 1 geschafft! ✨

Du kannst die Übungen, die du abschließen musst, links aufgelistet sehen.

## Was ist dein Ziel?

In dieser Aufgabe führen wir clientseitige Angriffe durch. Dein Ziel ist es, "Angriffseingaben" zu entwickeln, die, wenn sie in anfällige Websites eingegeben werden, es dir ermöglichen, Code im Browser des Ziels auszuführen.

Bei Reflected XSS möchtest du einen Weg finden, die Angriffseingabe in eine URL zu kodieren, die an ein Ziel gesendet werden kann. Wenn die URL besucht wird, wird deine Angriffseingabe vom serverseitigen (oder möglicherweise clientseitigen) Code extrahiert und im Browser des Ziels ausgeführt.

Bei Stored XSS möchtest du einen Weg finden, deine Angriffseingabe dauerhaft zu speichern, z.B. in der Datenbank des Servers, sodass, wenn dein Ziel zu einem späteren Zeitpunkt eine Seite besucht, die mit diesen Daten erstellt wurde, dein Angriffscode in ihrem Browser ausgeführt wird.

Normalerweise kannst du deine "Angriffseingaben" testen, indem du sie in ein Formulareingabefeld eingibst oder in einen URL-Parameter kodierst. Sobald du Code im Browser des Opfers ausführen kannst, kannst du dies beweisen, indem du die `success()`-Funktion aufrufst, die wir für dich erstellt haben. Denke daran, die Angriffseingaben, die du erzeugst, im Opal-Kurs abzugeben. Dies ist das, was du zur Bewertung einreichen wirst.

## Lass uns loslegen!

<a href='#' onclick="window.postMessage('success', '*')">Klicke auf diesen Link, um success() aufzurufen</a> und deine erste Übung abzuschließen.

Dein Konkurrent hält erneut eine Notfallsitzung ab, um seine Antwort auf deinen letzten Hack zu planen. An diesem Punkt sollten sie ihre Notfallsitzung einfach in eine regelmäßig geplante Sitzung umwandeln.

Sie erkennen ihren Fehler und beschließen, dich daran zu hindern, aus dem Skriptkontext auszubrechen, indem sie die Zeichenfolge entfernen, die du dafür verwenden musst. Nämlich `</`. Sie verwenden dazu einen regulären Ausdruck, aber wie üblich gibt es einen Fehler darin.

Aber du weißt, dass ihre schwachen Verteidigungen keine Chance gegen deine Fähigkeiten haben werden, da du schon einmal [den Gibson gehackt](https://www.youtube.com/watch?v=vYNnPx8fZBs) hast!!!!11

## Ziel

Finde die XSS-Schwachstelle im Suchfeld. Du kannst jedes HTML-Tag verwenden, um die `success()`-Funktion auszuführen.

<iframe src='http://hackme.ifflaender-family.de:4160'></iframe>

**Hinweis**: Eventuell blockiert Firefox den Port 4160. In diesem Fall kannst du Chrome oder einen anderen Browser verwenden oder den Port 4160 in Firefox freigeben. Dazu musst du `about:config` in die Adressleiste eingeben und `network.security.ports.banned.override` auf `4160` setzen. Existierte die Einstellung nicht, musst du sie erstellen (als String).

Bevor du zur nächsten Übung übergehst, denke daran, deine "Angriffseingabe" im Opal-Kurs abzugeben.

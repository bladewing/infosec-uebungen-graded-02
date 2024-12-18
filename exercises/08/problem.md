Der Sicherheitsberater hat genug von diesen Katz-und-Maus-Spielen. Er erkennt, dass alle deine Angriffe nicht mehr funktionieren würden, wenn er dich daran hindert, bestimmte "kritische" Zeichen zu verwenden.

Er erkennt auch, dass du seinen Quellcode gestohlen hast, was es dir viel einfacher gemacht hat, die Schwachstellen in seinem System zu finden. Also hat er diesen Angriffsvektor geschlossen. Du musst dich auf deine Einfallsreichtum verlassen, um herauszufinden, was sein Code tut, indem du verschiedene Eingaben ausprobierst und siehst, was am Ende im HTML der resultierenden Seite landet.

```js
router.get('/search', async (req, res) => {
  // TOP SECRET –– REDACTED
})
```

Hinweis: Versuche nicht, den **serverseitigen Quellcode** des Servers anzusehen, um herauszufinden, was der `/search` Routen-Handler tut. Dies entspricht nicht dem Geist dieser Übung. Du kannst natürlich weiterhin den HTML-Quellcode der Seiten ansehen, die der Server an den Client zurücksendet.

## Ziele

1. Finde die XSS-Schwachstelle im Such-Eingabefeld. Du kannst jeden HTML-Tag verwenden, den du möchtest.

1. Schreibe den Code auf, von dem du glaubst, dass der Server ihn ausführt, um die Eingabe zu verarbeiten.

## Tipp

Versuche verschiedene Eingaben zu übermitteln und sieh dir dann den HTML-Quellcode des `<iframe>` an, um herauszufinden, was der Bereinigungscode tun muss.

<iframe src='http://hackme.ifflaender-family.de:4080'></iframe>

Bevor du zur nächsten Übung übergehst, denke daran, deine "Angriffseingabe" sowie deinen Servercode in die `SOLUTIONS.md` Datei zu kopieren.

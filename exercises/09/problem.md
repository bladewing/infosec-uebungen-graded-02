Dein Konkurrent hat genug von den enttäuschenden Ergebnissen des TU Dresden Absolventen und beschließt, stattdessen einen HTWD-Studenten einzustellen, der Informationssicherheit und Datenschutz abgeschlossen hat. Dieser kann schnell eine narrensichere `htmlElementEscape()`-Funktion implementieren, die deine Spielereien ein für alle Mal vereitelt.

Bitte lies den Code für `htmlElementEscape()` und stelle sicher, dass du im Detail verstehst, wie er funktioniert.

```js
function htmlElementEscape (str) {
  return str
    // Dies ist nicht für die Sicherheit, sondern weil '&' das HTML-Escape-Zeichen ist
    // und wir nicht wollen, dass die Benutzereingabe als Escape-Sequenz behandelt wird.
    .replace(/&/g, '&amp;')

    // Ohne das Zeichen '<' können keine HTML-Tags erstellt werden.
    .replace(/</g, '&lt;')
}
```

Jetzt muss dein Konkurrent nur noch diese Funktion aufrufen, wann immer er unzuverlässige Daten direkt in den HTML-Body einfügt, also in Tags wie `div`, `p`, `b`, `td`, etc.

Ihr aktualisierter Routen-Handler-Code sieht jetzt so aus:

```js
router.get('/search', async (req, res) => {
  let q = req.query.q
  if (q == null) q = ''

  q = htmlElementEscape(q)

  const results = await getResults(q)
  res.render('caloogle-search-page', { q, results })
})
```

Es scheint, als hätten wir vorerst kein Glück...

<a href='#' onclick="window.postMessage('success', '*')">Klicke auf diesen Link, um success() aufzurufen</a> und diese Übung abzuschließen.

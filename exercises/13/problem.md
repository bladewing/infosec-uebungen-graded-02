Genervt von den enttäuschenden Ergebnissen bei der Abwehr deiner Angriffe, stellt dein Konkurrent einen HTWD-Studenten ein, der Informationssicherheit und Datenschutz abgeschlossen hat. Später musst du mit diesen Studenten darüber sprechen, für deine Feinde zu arbeiten.

In der Zwischenzeit ist dein Konkurrent in der Lage, eine narrensichere `htmlAttributeEscape()`-Funktion zu implementieren, die dich vorerst besiegt... 😔

Bitte lies den Code für `htmlAttributeEscape()` und stelle sicher, dass du im Detail verstehst, wie er funktioniert.

```js
function htmlAttributeEscape (str) {
  return str
    // Dies ist nicht für die Sicherheit, sondern weil '&' das HTML-Escape-Zeichen ist
    // und wir nicht wollen, dass die Benutzereingabe als Escape-Sequenz behandelt wird.
    .replace(/&/g, '&amp;')

    // Ohne das einfache Anführungszeichen kann der Angreifer nicht aus
    // einem einfach-quotierten HTML-Attribut entkommen.
    .replace(/'/g, '&apos;')

    // Ohne das doppelte Anführungszeichen kann der Angreifer nicht aus
    // einem doppelt-quotierten HTML-Attribut entkommen.
    .replace(/"/g, '&quot;')
}
```

Jetzt muss dein Konkurrent nur noch diese Funktion aufrufen, wann immer er unzuverlässige Daten direkt in HTML-Attribute einfügt, z.B. `<div class='UNTRUSTED INPUT HERE'>`.

Ihr aktualisierter Routen-Handler-Code sieht jetzt so aus:

```js
router.get('/search', async (req, res) => {
  let q = req.query.q
  if (q == null) q = ''

  q = htmlAttributeEscape(q)

  const results = await getResults(q)
  res.render('caloogle-search-page', { q, results })
})
```

Es scheint, als hätten wir vorerst kein Glück...

<a href='#' onclick="window.postMessage('success', '*')">Klicke auf diesen Link, um success() aufzurufen</a> und diese Übung abzuschließen.

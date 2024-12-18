Dein Konkurrent kann nicht glauben, wie erfolgreich deine Angriffe waren. Sie sind begierig darauf, diesem Katz-und-Maus-Spiel ein Ende zu setzen. Daher beschließen sie, einen Sicherheitsberater zu engagieren, um das Problem mit ihrem Ansatz ein für alle Mal zu beheben.

Du beschließt, Ihre [Social Engineering](https://de.wikipedia.org/wiki/Social_Engineering_(Sicherheit)) Fähigkeiten einzusetzen und zu sehen, was du über ihren neu eingestellten Berater herausfinden können. Nach einem kurzen Telefonat kannst du eine entscheidende Tatsache über den Berater herausfinden: Er hat einen Abschluss der TU Dresden. Deine Ängste sind unbegründet. Mit neuem Selbstvertrauen wirfst du einen weiteren Blick auf ihren Code, um den unvermeidlichen Fehler zu finden, von dem du weißt, dass er existieren muss.

```js
router.get('/search', async (req, res) => {
  let q = req.query.q
  if (q == null) q = ''

  let oldQ
  while (q !== oldQ) {
    oldQ = q
    q = q.replace(/script/gi, '')
  }

  const results = await getResults(q)
  res.render('caloogle-search-page', { q, results })
})
```

## Ziel

Finde die XSS-Schwachstelle im Suchfeld. Verwende **keinen** `<script>`-Tag in diesem Angriff.

<iframe src='http://hackme.ifflaender-family.de:4060'></iframe>

Bevor Du zur nächsten Übung übergehst, denke daran, deine "Angriffseingabe" in die Datei `SOLUTIONS.md` zu kopieren.

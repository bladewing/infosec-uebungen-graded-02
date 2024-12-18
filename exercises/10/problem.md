Die `htmlElementEscape()`-Funktion deines Konkurrenten funktioniert ziemlich gut und du konntest ihre Benutzer nicht mehr angreifen, seit sie diese Funktion implementiert haben. Es ist viel schwieriger, den Status quo wie ein weltveränderndes Startup zu disruptieren, wenn du deine Konkurrenten nicht mit XSS angreifen kannst. Jetzt machst du dir Sorgen, dass du die nächste Finanzierungsrunde nicht bekommen könntest. Das ist ein großer Dämpfer.

Glücklicherweise hat dein Konkurrent gerade eine neue Version seiner Website veröffentlicht, die eine brandneue Funktion enthält. Vielleicht gibt es darin eine neue XSS-Schwachstelle?

Die Funktion heißt "Konkurrentenvergleich" und enthält Links zu Suchmaschinen von Konkurrenten, damit Benutzer Suchergebnisse vergleichen und entscheiden können, welche Suchmaschine die beste ist. Offensichtlich sind sie ziemlich zuversichtlich, dass ihre Ergebnisse die besten sind.

Sie scheinen die narrensichere `htmlElementEscape()`-Funktion zu verwenden, die von einem HTWD-Studenten für sie geschrieben wurde, um das HTML für diese Links zu generieren, sodass du denkst, dass sie garantiert sicher sind:

```js
router.get('/search', async (req, res) => {
  let q = req.query.q
  if (q == null) q = ''

  q = htmlElementEscape(q)

  const results = await getResults(q)
  res.render('caloogle-search-page', { q, results })
})
```

Aber bei näherer Betrachtung scheint es, dass sie die Funktion nicht richtig verwenden. Zeit, ihnen eine weitere Lektion zu erteilen!

## Ziel

Finde die XSS-Schwachstelle im Suchfeld. Du kannst beliebiges HTML verwenden, um die `success()`-Funktion auszuführen.

## Tipp

Versuche, verschiedene Eingaben zu übermitteln und dann den HTML-Quellcode des `<iframe>` zu betrachten, um herauszufinden, wie die "bereinigte" Benutzereingabe mit dem Kontext des HTML-Quellcodes interagiert.

<iframe src='http://hackme.ifflaender-family.de:4100'></iframe>

Bevor du zur nächsten Übung übergehst, denke daran, deine "Angriffseingabe" in die `SOLUTIONS.md`-Datei zu kopieren.

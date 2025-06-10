Sie sind dir auf die Schliche gekommen! Sie haben deinen letzten Angriff in ihren Serverprotokollen gesehen und ihren Code zur Eingabesäuberung erneut aktualisiert.

```js
router.get("/search", async (req, res) => {
  let q = req.query.q;
  if (q == null) q = "";

  let oldQ;
  while (q !== oldQ) {
    oldQ = q;
    q = q.replace(/script|SCRIPT/g, "");
  }

  const results = await getResults(q);
  res.render("caloogle-search-page", { q, results });
});
```

## Ziel

Kannst du dir eine Möglichkeit überlegen, ihren verbesserten Säuberungscode zu umgehen und dein `<script>`-Tag über das Suchfeld in die Seite einzufügen?

<iframe src='http://hackme.ifflaender-family.de:4050'></iframe>

Bevor du zur nächsten Übung übergehst, denke daran, deine "Angriffseingabe" im Opal-Kurs abzugeben.

## Hinweis

Deine Lösung muss ein `<script>`-Tag enthalten.

Nach ihrer letzten Niederlage sind sie wirklich frustriert über deine Angriffe.

Sie beschließen, einfach wiederholt zu iterieren, bis all deine Hackereien aus der Eingabe entfernt sind. Aber es gibt ein Problem mit ihrem Ansatz.

```js
router.get("/search", async (req, res) => {
  let q = req.query.q;
  if (q == null) q = "";

  let oldQ;
  while (q !== oldQ) {
    oldQ = q;
    q = q.replace(/script/g, "");
  }

  const results = await getResults(q);
  res.render("caloogle-search-page", { q, results });
});
```

## Ziel

Kannst du dir eine Möglichkeit überlegen, ihren verbesserten Bereinigungscode zu umgehen und dein `<script>`-Tag über das Suchfeld in die Seite einzufügen?

<iframe src='http://hackme.ifflaender-family.de:4040'></iframe>

Bevor du zur nächsten Übung übergehst, denke daran, deine "Angriffseingabe" (die bösartige Eingabezeichenfolge, nicht die URL) im Opal-Kurs abzugeben.

## Hinweis

Deine Lösung muss ein `<script>`-Tag enthalten.

Dein Konkurrent merkt, dass du einen Weg gefunden hast, ihren Hotfix zu umgehen. Sie reagieren schnell und machen eine weitere Änderung, um sich gegen deinen letzten Angriff zu verteidigen.

Sie haben keine guten Ingenieurpraktiken, also setzen sie ihren Fix direkt in die Produktion ein, ohne eine Code-Überprüfung. Du solltest ihnen eine Lektion erteilen, die sie nicht so schnell vergessen werden. Hacke sie so gründlich, dass sie in die Vorgründungsphase zurückversetzt werden!

```js
router.get("/search", async (req, res) => {
  let q = req.query.q;
  if (q == null) q = "";

  q = q.replace(/script/gi, "");

  const results = await getResults(q);
  res.render("caloogle-search-page", { q, results });
});
```

## Ziel

Kannst du dir eine Möglichkeit überlegen, ihren verbesserten Bereinigungscode zu umgehen und dein `<script>`-Tag über das Suchfeld in die Seite einzufügen?

<iframe src='http://hackme.ifflaender-family.de:4030'></iframe>

Bevor du zur nächsten Übung übergehst, denke daran, deinen "Angriffseingang" (die bösartige Eingabezeichenfolge, nicht die URL) im Opal-Kurs abzugeben.

## Hinweis

Deine Lösung muss ein `<script>`-Tag enthalten.

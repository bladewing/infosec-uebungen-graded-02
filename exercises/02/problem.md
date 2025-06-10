Dein Konkurrent ist dir auf die Schliche gekommen! Sie haben herausgefunden, was du vorhast, und ihren besten Engineering-"Rockstar" auf den Fall angesetzt.

Zum Glück für dich ist ihr bester Ingenieur nicht sehr gut.

Sie versuchen, die Suchanfrage mit einem Aufruf von [`String.prototype.replace`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace) zu bereinigen. Dies ist der endgültige Code, den sie in die Produktion einführen:

```js
router.get("/search", async (req, res) => {
  let q = req.query.q;
  if (q == null) q = "";

  q = q.replace(/script/i, "");

  const results = await getResults(q);
  res.render("caloogle-search-page", { q, results });
});
```

## Ziel

Du solltest in der Lage sein, eine kleine Änderung an deinem "Angriffs-Input" aus der letzten Übung vorzunehmen, und dein Reflected XSS-Angriff sollte weiterhin gegen ihre Benutzer funktionieren. Entfessle mehr `<script>`-Schaden!

<iframe src='http://hackme.ifflaender-family.de:4020'></iframe>

Bevor du zur nächsten Übung übergehst, denke daran, deinen "Angriffs-Input" (die bösartige Eingabezeichenfolge, nicht die URL) im Opal-Kurs abzugeben.

## Hinweis

Deine Lösung muss ein `<script>`-Tag enthalten.

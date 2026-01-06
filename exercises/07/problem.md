Der Berater ist cleverer als du erwartet hast und hat die Server-Logs genau beobachtet, als du den letzten Angriff durchgeführt hast. Sie haben deine Arbeit entdeckt und konnten schnell mit einem Fix reagieren.

Du weißt jedoch, dass ihr Fix wahrscheinlich immer noch in irgendeiner Weise fehlerhaft ist. Du tauchst in den Code ein, um den Fehler zu finden, von dem du weißt, dass er existieren muss. 😆

```js
router.get("/search", async (req, res) => {
  let q = req.query.q;
  if (q == null) q = "";

  let oldQ;
  while (q !== oldQ) {
    oldQ = q;
    q = q.replace(/script|onerror=|onload=/gi, "");
  }

  const results = await getResults(q);
  res.render("caloogle-search-page", { q, results });
});
```

## Ziel

Finde die XSS-Schwachstelle im Suchfeld. Du solltest **keinen** `<script>`-Tag in diesem Angriff verwenden.

<iframe src='https://hackme.security-prof.de/ex/07/'></iframe>

Bevor du zur nächsten Übung übergehst, denke daran, deinen "Angriffseingang" im Opal-Kurs abzugeben.

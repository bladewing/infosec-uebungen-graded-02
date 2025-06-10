Dein Konkurrent hat sich entschieden, ein Gästebuch auf seiner Website hinzuzufügen.

Gästebücher waren auf Websites, die in den späten 90er und frühen 00er Jahren gebaut wurden, sehr beliebt. Falls du mit dem Konzept nicht vertraut bist, hier ist eine Definition:

> Im Web ist ein Gästebuch ein Protokollsystem, das es Besuchern einer Website ermöglicht, einen öffentlichen Kommentar zu hinterlassen. In einigen Gästebüchern ist es möglich, dass Besucher ihre Gedanken über die Website oder ihr Thema äußern. Im Allgemeinen erfordert es nicht, dass der Verfasser ein Benutzerkonto erstellt, da es eine informelle Methode ist, eine kurze Nachricht zu hinterlassen. Der Zweck eines Website-Gästebuchs besteht darin, die Art der Besucher anzuzeigen, die die Seite erhält, einschließlich des Teils der Welt, in dem sie sich befinden, und Feedback von ihnen zu erhalten. Dies ermöglicht es dem Webmaster, seine Seite zu bewerten und zu verbessern. Ein Gästebuch ist im Allgemeinen ein Skript, das normalerweise extern gehostet wird... – [Wikipedia](https://de.wikipedia.org/wiki/Gästebuch)

Als du es dir ansiehst, bemerkst du, dass sie Kommentare serverseitig speichern, sodass spätere Besucher des Gästebuchs die Kommentare früherer Poster sehen können. Du erkennst, dass dies eine perfekte Gelegenheit für einen Stored XSS-Angriff sein könnte!

Dein Konkurrent verwendet ein Open-Source-Gästebuch-Paket, und du konntest durch etwas Nachforschung herausfinden, welches und welche Version. Du lädst den Code herunter, um zu sehen, womit du es zu tun hast:

```js
router.get("/", async (req, res) => {
  const comments = await getCommentsFromDatabase();
  res.render("caloogle-guestbook-page", { comments });
});

router.post("/comment", async (req, res) => {
  const comment = req.body;

  if (comment == null) throw new Error("comment cannot be empty");
  if (comment.text == null) throw new Error("comment.text cannot be empty");

  // if client specifies no id, then use the next id
  if (comment.id == null) comment.id = await getNextAvailableIdFromDatabase();

  await addCommentToDatabase(comment);

  res.send({ error: null, comment });
});
```

Wenn du einen Stored XSS-Angriff durchführen kannst, werden alle zukünftigen Besucher ihres Gästebuchs deinen Angriffscode ausführen! Im Gegensatz zu den Reflected XSS-Angriffen, die du bisher durchgeführt hast, erfordert dieser nicht, dass das Opfer deine speziell gestaltete Angriffs-URL besucht, um ausgenutzt zu werden. Das Opfer muss lediglich das Gästebuch besuchen, und dein Angriffscode wird ausgeführt.

Zeit, deinem Konkurrenten die Macht von Stored XSS zu zeigen!

## Ziele

1. Finde die XSS-Schwachstelle in ihrem Code. Du kannst beliebiges HTML verwenden.

1. Deine Lösung sollte ein Code-Snippet sein, das, wenn es in die DevTools des Browsers eingefügt wird, einen Kommentar in der Datenbank des Servers hinzufügt.

## Tipps

- Das allgemeine Konzept von Stored XSS ist dasselbe wie bei Reflected XSS. Deine bisherigen Übungen sollten dir hier also nützlich sein!

- Du solltest die [`fetch`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) API verwenden, um eine HTTP-Anfrage zu erstellen, die dein XSS-Payload im Datenspeicher des Servers speichert.

- Es ist in Ordnung, wenn dein Angriffscode nicht sofort beim Laden der Seite ausgeführt wird. Es ist akzeptabel, wenn er später als Reaktion auf die Interaktion des Benutzers mit der Seite ausgeführt wird.

<iframe src='http://hackme.ifflaender-family.de:4170'></iframe>

Bevor du zur nächsten Übung übergehst, denke daran, deinen "Angriffscode" im Opal-Kurs abzugeben.

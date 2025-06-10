Du bist der Gründer eines innovativen [weltverändernden Startups](https://tiffzhang.com/startup/)! Es hat etwas mit Blockchain in der Cloud zu tun. Es ist wie Uber, aber für Katzen. Oder vielleicht ist es wie Airbnb, aber für Gamification. Es ist sozial, mobil und lokal. Die Tech-Presse sagt, dass es disruptiv und revolutionär ist. Wirklich, es hat alles, was ein Benutzer wollen könnte. Aber du iterierst immer noch im Stealth-Modus mit der Lean Startup™️-Methode, bis du das Produkt-Markt-Fit findest und ein Einhorn wirst! 🦄

Aber... eines Tages, aus dem Nichts, schlägt das Unglück zu! Du siehst, dass dein größter Konkurrent ein Produkt veröffentlicht hat, das genau wie das ist, was du gebaut hast. Aber sie waren schneller auf dem Markt!

Du vermutest, dass sie möglicherweise einige Ecken bei der Sicherheit geschnitten haben, um ihr Produkt so schnell zu veröffentlichen. Keine gute Idee. Du entscheidest dich, den "Hacker" in "Growth Hacker" zu stecken und ihnen eine Lektion darüber zu erteilen, Web-Sicherheit ernst zu nehmen.

Vielleicht kannst du deinen Konkurrenten überzeugen, ihre Website zurückzuziehen, wenn sie sehen, dass ihre Benutzer in freier Wildbahn angegriffen werden. Dies würde deinem Team die dringend benötigte Zeit geben, um dein überlegenes Produkt zu starten! 😈

Du entscheidest dich, ihre Website zu überprüfen und nach einer Reflected XSS-Schwachstelle zu suchen.

## Ziel

Finde einen Weg, ein `<script>`-Tag in die Website deines Konkurrenten einzufügen. Sobald du einen Weg gefunden hast, Code auf ihrer Website auszuführen, solltest du die `success()`-Funktion aufrufen. Wenn du es richtig gemacht hast, solltest du eine Browser-Benachrichtigung sehen, die dir sagt, dass du erfolgreich warst.

<iframe src='http://hackme.ifflaender-family.de:4010'></iframe>

Da dies ein Reflected XSS-Angriff ist, beachte, dass die URL der Opferseite eine URL-codierte Version deiner "Angriffseingabe" enthält.

Wenn du wirklich böse wärst, könntest du diese URL in sozialen Medien teilen und wenn unschuldige Benutzer auf den Link klicken, sollte dein Angriffscode in ihren Browsern ausgeführt werden und Chaos anrichten. Du könntest ihre Cookies exfiltrieren und dich als sie einloggen oder Aktionen auf ihrem Konto ausführen, einschließlich des Löschens. Dein Konkurrent wird Schwierigkeiten haben, seine nächste Finanzierungsrunde von Investoren zu bekommen, wenn ihre Benutzerzahlen sinken! 🤣📉🤣 Anfänger!

Du solltest versuchen, diese URL zu kopieren und in einem neuen Tab zu öffnen und bestätigen, dass dein Angriffscode sofort ausgeführt wird, wenn die Seite geladen wird. Dies ist die Macht von Reflected XSS!

Bevor du zur nächsten Übung übergehst, denke daran, deine "Angriffseingabe" (die bösartige Eingabezeichenfolge, nicht die URL) im Opal-Kurs abzugeben, damit du sie einreichen und Kredit erhalten kannst.

## Hinweis

Deine Lösung muss ein `<script>`-Tag beinhalten.

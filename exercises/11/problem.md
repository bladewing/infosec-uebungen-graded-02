Dein letzter Angriff hat deinem Konkurrenten die Augen geöffnet. Sie erkennen jetzt, warum sie `htmlElementEscape()` falsch verwendet haben.

Dank dir haben sie gelernt, dass die Funktion `htmlElementEscape()` nicht für die Werte von HTML-Attributen funktioniert. Sie entkommt nicht dem richtigen Zeichensatz für diesen Kontext.

Die besten Ingenieure deines Konkurrenten berufen eine Notfallsitzung ein, um herauszufinden, was zu tun ist. Sie entscheiden, dass der beste Weg, das Problem zu lösen, darin besteht, doppelte Anführungszeichen (`"`) durch das entsprechende HTML-Entity (`&quot;`) zu ersetzen, damit es nicht möglich ist, aus dem Attributwertbereich "auszubrechen".

Aber in ihrer Eile scheinen sie vergessen zu haben, an alle Fälle zu denken... Pech für sie. Es gibt nur einen Weg, wie sie es lernen werden. Zeig es ihnen! 😈

## Ziele

1. Finde die XSS-Schwachstelle im Suchfeld. Du kannst beliebiges HTML verwenden, um die Funktion `success()` auszuführen.

1. Schreibe den Code auf, von dem du glaubst, dass der Server ihn zur Verarbeitung der Eingabe ausführt.

<iframe src='http://hackme.ifflaender-family.de:4110'></iframe>

Bevor du zur nächsten Übung übergehst, denke daran, deine "Angriffseingabe" sowie deinen Servercode im Opal-Kurs abzugeben.

# Graded Assignment 2 – Journey to the Dark Side 🌘

# Informationssicherheit - Bewertete Übung 02

**Abgabefrist:** siehe Opal-Kurs

## Vorbereitung

- Auf Ihrem System muss NodeJS -- vorzugsweise in Version 18 -- installiert sein.
- Variante 1: Nutzen Sie das beiliegende Vagrant-File.
- Variante 2: Folgen Sie den Anweisungen unter [https://nodejs.org/en/download/package-manager](https://nodejs.org/en/download/package-manager)

## Aufgabenstellung

Checken Sie die Aufgabenstellung aus dem Git-Repository aus.

```console
$ git clone https://github.com/bladewing/infosec-uebungen-graded-02.git graded02
```

Wechseln Sie in das Verzeichnis `graded02` und installieren Sie die Abhängigkeiten.

```console
$ cd graded02
[graded02]$ npm install
```

Starten Sie den Webserver.

```console
[graded02]$ npm start
```

**Variante 1 (lokal):** Unter [http://127.0.0.1:4000/](http://127.0.0.1:4000/) bzw. [http://localhost:4000/](http://localhost:4000/) finden Sie die Webseite mit der Aufgabenstellung.

**Variante 2 (remote zum Laborrechner):** Unter [http://xxx.xxx.xxx.xxx:4000/](http://xxx.xxx.xxx.xxx:4000/) finden Sie die Webseite mit der Aufgabenstellung. Ersetzen Sie xxx.xxx.xxx.xxx durch die IP-Adresse des Laborrechners.

**Variante 3 (gehostete Version):** Die Übung ist auch unter [https://hackme.security-prof.de/](https://hackme.security-prof.de/) verfügbar. Diese Version läuft über HTTPS und erfordert keine lokale Installation.

Arbeiten Sie sich durch die Aufgabenstellung und lösen Sie die Aufgaben. Geben Sie Ihre Antworten in der Datei `src/SOLUTION.md` an.

## Abgabe

Geben Sie die Lösungen im OPAL-Kurs ab. Beachten Sie, dass es nach jeder Aufgaben-Abgabe ein paar Sekunden dauert, bis die Funktionalität Ihrer Lösung belegt wird.

## Bekannte Probleme

Kommt es bei der Erstellung der Vagrant-VM zur Meldung, dass der Port 4000 bereits belegt ist, führt bereits jemand anders die Aufgabe auf dem Laborrechner aus. Ersetzen Sie `host:4000` in der Vagrantfile durch einen anderen Wert. Ändern Sie entsprechend auch den Port in Ihrem Browser (also z.B. statt [http://localhost:4000/](http://localhost:4000/) verwenden Sie [http://localhost:4001/](http://localhost:4000/))

## Danksagung

Credits to Feross Aboukhadijeh

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

Wechseln Sie in das Verzeichnis `assign1` und installieren Sie die Abhängigkeiten.

```console
$ cd assign1
[assign1]$ npm install
```

Starten Sie den Webserver.

```console
[assign1]$ npm start
```

Variante 1 (eigener Rechner oder im Labor): Unter [http://127.0.0.1:4000/](http://127.0.0.1:4000/) finden Sie die Webseite mit der Aufgabenstellung.

Variante 1 (remote zum Laborrechner): Unter [http://xxx.xxx.xxx.xxx:4000/](http://xxx.xxx.xxx.xxx:4000/) finden Sie die Webseite mit der Aufgabenstellung. Ersetzen Sie xxx.xxx.xxx.xxx durch die IP-Adresse des Laborrechners.

Variante 2: Unter [http://localhost:4000/](http://localhost:4000/) finden Sie die Webseite mit der Aufgabenstellung.

Arbeiten Sie sich durch die Aufgabenstellung und lösen Sie die Aufgaben. Geben Sie Ihre Antworten in der Datei `src/SOLUTION.md` an.

## Abgabe

Laden Sie die Datei `src/SOLUTION.md` in Opal hoch.

## Bekannte Probleme

Kommt es bei der Erstellung der Vagrant-VM zur Meldung, dass der Port 4000 bereits belegt ist, führt bereits jemand anders die Aufgabe auf dem Laborrechner aus. Ersetzen Sie ```host:4000``` in der Vagrantfile durch einen anderen Wert. Ändern Sie entsprechend auch den Port in Ihrem Browser (also z.B. statt [http://localhost:4000/](http://localhost:4000/) verwenden Sie [http://localhost:4001/](http://localhost:4000/))

## Danksagung

Credits to Feross Aboukhadijeh

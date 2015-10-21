# Wie kann ich an diesem Buch mitarbeiten ?

## Mitarbeiten über GitBook

Eröffne ein Konto bei [Gitbook](http://www.gitbook.com/login) und [sende eine Anfrage zur Mitarbeit](https://www.gitbook.com/book/neomatrix369/adoptopenjdk-getting-started-kit/contact) beim [Adopt OpenJDK Git Buch](http://neomatrix369.gitbooks.io/adoptopenjdk-getting-started-kit/)

Die [Dokumentation](http://help.gitbook.com/) und die [Anleitung zur lokalen Installation von GitBook](https://github.com/GitbookIO/gitbook) sind ebenfalls hilfreich.

## Mitarbeiten über GitHub

1. Forke das Projekt auf der folgenden Webseite: <br/> **https://github.com/neomatrix369/adoptopenjdk-getting-started-kit#fork-destination-box** 

2. Klone deine Version in deinen lokalen Workspace <br/>
```git clone git@github.com:{YOUR_GITHUB_ACCOUNT}/adoptopenjdk-getting-started-kit.git```

3. Konfiguriere das Original Repository als Upstream <br/>
```git remote add --track master upstream git://github.com/neomatrix369/adoptopenjdk-getting-started-kit.git```

So kannst du deinen Fork auf den Stand des originalen Repositories bringen <br/>
```git fetch upstream``` <br/>
und dann <br/>
```git merge upstream/master```

Während des Arbeitens helfen dir die folgenden Befehle:
1. Commit geänderter Dateien <br/>
```git add <changed files / wild-card pattern>```<br/>
```git commit -am "sinnvolle Beschreibung deiner Änderungen"```

2. Push <br/>
```git push```

3. Erstellen eines Pull Requests <br/>
Gehe zu deinem Repository auf GitHub <br/> https://github.com/{YOUR_GITHUB_ACCOUNT}/adoptopenjdk-getting-started-kit/pulls und klicke auf den 'New Pull Request' Knopf

## Wie finde ich heraus was geändert hat ?

Es gibt zwei [Scripts](https://github.com/neomatrix369/adoptopenjdk-getting-started-kit) im Hauptordner des Repositories. Diese erzeugen eine <b>What's changed</b> Markdown Seite. Sie ist immer Englisch und sieht [so](http://neomatrix369.gitbooks.io/adoptopenjdk-getting-started-kit/content/en/whatsChanged.html) aus.

Die beiden Scripts heissen  [whatsChanged.sh](https://github.com/neomatrix369/adoptopenjdk-getting-started-kit/blob/master/whatsChangedFor.sh) und [whatsChangedForAllLanguages.sh](https://github.com/neomatrix369/adoptopenjdk-getting-started-kit/blob/master/whatsChangedFor.sh).

Bitte zögere nicht, Verbesserungen oder Verbesserungsvorschläge einzubringen. Achte aber bitte darauf dass bestehende Funktionalität erhalten bleibt.
# Splash-Docker
> Docker-Compose-Datei für die Installation des JavaScript-Rendering-Dienstes Splash in einem Docker-Container

Dieses Repository enthält eine Docker-Compose-Datei, um die Installation des JavaScript-Rendering-Dienstes Splash in einem Docker-Container realisieren zu können. Hierfür wird das von Scrapinghub zur Verfügung gestellte Docker-Image verwendet.

Das Repository dient als persönliches Backup für den Einsatz in einem privaten LAN.

Die Lauffähigkeit der Docker-Container wurde auf einem Ubuntu 23.04 ("Lunar Lobster") getestet.

## Download des Repositorys und Starten der Docker-Container

```shell
# Klonen des Repositorys und Wechsel in das Verzeichnis
git clone https://github.com/steffen-roesemann/splash-docker
cd splash-docker

# Starten des Splash-Docker-Containers
docker-compose up -d
```

Mit dem Starten des Docker-Containers wird im aktuellen Verzeichnis ein Ordner "splash" angelegt, in dem die Unterordner "filters", "proxy-profiles", "js-profiles" und "lua_modules" angelegt werden. In diese Ordner kann man entsprechende Dateien lokal ablegen und über den Docker-Container auf diese zugreifen.

Über einen Webbrowser kann der Docker-Container dann wie folgt aufgerufen werden:

- http://localhost:8050 oder http://{ip-adresse-des-hosts}:8050


## Hinweise zum Arbeiten mit dem Docker-Container

```shell
# Stoppen des laufenden Container-Dienstes
docker-compose down

# Updaten des verwendeten Images
docker-compose pull

# Neustarten des Containers als Dienst
docker-compose up -d

# Laufenden Docker-Container anzeigen lassen
docker ps

# Alle Docker-Container, Images und Netzwerke löschen (ACHTUNG! Löscht auch alles andere!)
docker system prune -a
```

## Nutzungsbedingungen

Die folgenden Bedingungen regeln die Nutzung dieser Software. Durch die Verwendung erklären 
ihr euch mit den nachstehenden Bedingungen einverstanden:

Die Software wird "wie sie ist" zur Verfügung gestellt, ohne jegliche ausdrückliche oder stillschweigende Gewährleistung. Dies schließt, aber ist nicht beschränkt auf, Gewährleistungen hinsichtlich der Eignung für einen bestimmten Zweck, der Marktgängigkeit und der Nichtverletzung von Rechten Dritter ein.

Ich übernehme keine Verantwortung oder Haftung für die Richtigkeit, Vollständigkeit, Zuverlässigkeit oder Aktualität der Software oder der damit erzielten Ergebnisse.

In keinem Fall hafte ich für direkte, indirekte, zufällige, besondere oder Folgeschäden, die sich aus der Nutzung oder Unmöglichkeit der Nutzung der Software ergeben, einschließlich, aber nicht beschränkt auf entgangenen Gewinn, Datenverlust, Geschäftsunterbrechung oder jegliche andere kommerzielle Schäden oder Verluste.

Ihr stimmt zu, die Software nur in Übereinstimmung mit den geltenden Gesetzen und Vorschriften zu nutzen. Ich übernehme keine Verantwortung für rechtliche Konsequenzen, die sich aus einer rechtswidrigen Nutzung der Software ergeben.

Ihr erkennt an, dass die Software möglicherweise Fehler, Unvollkommenheiten oder technische Probleme aufweisen kann. Ich übernehme keine Verantwortung für etwaige Schäden oder Datenverluste, die durch solche Probleme verursacht werden.

Jegliche Kommunikation, die über die Software erfolgt, liegt in eurer Verantwortung. Ich hafte nicht für den Inhalt solcher Kommunikation oder die Verwendung, die ihr davon macht.

Durch die Verwendung dieser Software erklärt ihr euch damit einverstanden, auf jegliche Ansprüche, Klagen oder Forderungen gegenüber mir zu verzichten, die sich aus der Nutzung der Software ergeben könnte.
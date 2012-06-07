# Analyse

In diesem Kapitel erfolgt die Analyse zur Entwicklung der mobilen Anwendung. 

<q>Plan your work and work your plan.</q>
<div style="text-align: right; margin-right: 2em; margin-top: -2em;">
    Vince Lombardi
</div>

Die ersten Abschnitte beziehen sich auf die Projektplanung, wie die Definition der Zielgruppe und Ist-Zustandsanalyse. In den darauffolgenden Abschnitten wird die Konzeption und Identität anhand von Navigationskonzepte, Design eines Logos und Apple Design verdeutlicht. Gefolgt werden diese von der Strukturierung der Anwendung durch ein Story-Board und Usability-Tests anhand einiger Vorlagen.

## Zielgruppe

Die Definition der Zielgruppe und die Abfragen der Interessen der Anwender ist entscheidet für die Realisierung einer guten Anwendung.

### Brainstorming

Um die Zielgruppe und deren Anforderungen besser spezifizieren zu können, wurde in einem Meeting aller Mitglieder der Abteilung, ein Brainstorming abgehalten. Durch dieses Verfahren war es einfacher möglich eine genaue Definition zu erstellen.

Mit der in <a href="#zielgruppe-brainstorming">Abbildung 7</a> erstellten Mindmap konnte eine Definition abgeleitet werden. Für eine bessere kreative Arbeit wurde das Brainstorming aber mit Papier und Stift erstellt. Das Original befindet sich in der Anlage.

<div class="figure" id="zielgruppe-brainstorming">
	<img src="http://up.frubar.net/1756/zielgruppe-brainstorming.svg" alt="Zielgruppe Brainstorming" width="90%" />
	<p>Brainstorming mit und über die Zielgruppe</p>
</div>


### Definition

Die Zielgruppe für das Projekt umfasst Mitarbeiter einer IT Abteilung. Diese Mitarbeiter sind erfahrene IT Administratoren für die Betriebssysteme Linux und Windows. Sie sind vertraut mit der Handhabung eines Smartphones, insbesondere iPhones.

Den Benutzern ist die Verwendung von virtuellen Servern in einer Cloud-Landschaft bekannt. Die Technologie libvirt und Linux KVM im Zusammenhang mit Hardware-Virtualisierung ist ein Begriff.

## Ist-Zustandsanalyse

Zum jetzigen Zeitpunkt existiert noch keine mobile Anwendung (iPhone Anwendung) zur Verwaltung der Cloud Infrastruktur.

Zum Einsatz im Unternehmen kommt Citrix CloudStack <span class="fn"><a href="http://www.citrix.de/produkte/cloudstack/">Citrix CloudStack</a></span>. Hierbei handelt es sich um eine OpenSource Webanwendung zur Verwaltung einer Infrastruktur Cloud. Zwischen der Weboberfläche und der Virtualisierungstechnologie befindet sich die libvirt-Schnittstelle. Nach <a href="#libvirt-schnittstelle">Abbildung 3 Einbindung libvirt Schnittstelle</a>, befindet sich CloudStack in der Anwenderschicht. Durch diese Schnittstelle ist es möglich verschiedene Virtualisierungstechnologien zu nutzen. 

Eine zufriedenstellende Verwendung von CloudStack ist nur in einem Browser mit ausreichend großem Bildschirm möglich. Auf einem Smartphone ist die Vielzahl an Funktionen unübersichtlich und im Notfall nicht verwendbar.

<div class="figure" id="cloudstack-dashboard">
	<img src="http://up.frubar.net/1773/cloudstack-dashboard.jpg" alt="cloudstack-dashboard" width="90%" />
	<p>CloudStack Dashboard <cite><a href="cstack12">cstack12</a></cite></p>
</div>

Da durch CloudStack auf die libvirt-Schnittstelle aufgesetzt wird, ist es sinnvoll diese auch für die Entwicklung der mobilen Anwendung zu verwenden.

## Alternative Anwendungen

Da aktuell noch keine Anwendungen für die Verwaltung von virtuellen Rechnerinstanzen existieren werden alternative IT-relevante Anwendungen betrachtet. Ein Teil der Erfahrungen mit diesen Anwendungen wird in der Realisierungsphase nützlich sein.

Die Anwendungen werden kurz Beschrieben und die grafischen Benutzeroberflächen bewertet.

### iSSH

Die Anwendung „iSSH - SSH / VNC Console“ bietet IT Administratoren die Möglichkeit sich mit einer Remote Verbindung auf einen Server zu verbinden und diesen zu verwalten. Unterstützt werden viele verschiedenste Protokolle, wie SSH<span class="fn"><a href="http://openssh.org">SSH</a></span> und Windows Remote Desktop<span class="fn"><a href="http://support.microsoft.com/?scid=kb%3Ben-us%3B186607&x=13&y=11">Windows Remote Desktop</a></span>.

<div class="figure" id="issh-overview">
	<img src="http://up.frubar.net/1768/issh-overview.png" alt="issh-overview" width="35%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1770/issh-overview-server.png" alt="issh-overview-server" width="35%" />
	<p>iSSH Kategorisierung und Übersicht der Server</p>
</div>

Das sortieren von Servern in verschiedene Kategorien bzw. Ordner bietet eine hohe Übersichtlichkeit. Durch grüne oder rote Punkte wird Angezeigt ob ein Server erreichbar ist. Somit hat der Benutzer eine direkte Rückmeldung ob er sich zum Server verbinden kann.

Einige Nachteile bieten die vielen Einstellungsmöglichkeiten auf der Übersichtsseite (Abbildung 8, linkes Bild). Die „General Settings“, „Add Configuration“ und „Add Grouping“ wären an der Unterseite des Bildschirms oder in den iPhone Einstellungen besser aufgehoben.

### IPMI Touch

Bei „IPMI Touch“ handelt es sich um ein weiteres IT Verwaltungswerkzeug von Servern. Es liest Hardwareinformationen eines Servers über das IPMI Protokoll<span class="fn"><a href="http://www.intel.com/design/servers/ipmi/">IPMI</a></span> aus. Für diese Informationen werden Temperatursensoren des Gehäuses ausgelesen, die Geschwindigkeit der Lüfter und der aktuelle Stromverbrauch. Über die Anwendung ist es dem Administrator auch möglich den Server auszuschalten.

<div class="figure" id="ipmi-overview">
	<img src="http://up.frubar.net/1771/ipmi-overview.png" alt="ipmi-overview" width="35%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1772/ipmi-server.png" alt="ipmi-server" width="35%" />
	<p>IPMI Touch Übersicht und Hardwareinformationen</p>
</div>
	
Auf der Übersichtsseite der Anwendung ist durch die farblichen Unterschiede und Symbole sofort erkennbar bei welchem Server Probleme vorhanden sind. Klickt der Benutzer auf einen Menüpunkt erhält er eine detaillierte Anzeige der Hardware, in der ebenso farblich Probleme gekennzeichnet sind. Hinzufügen neuer Server erfolgt über das Plus („+“) in der oberen rechten Ecke des Bildschirms und braucht somit keinen Platz in der Anzeige.

Server lassen sich bei dieser Anwendung nicht in Kategorien oder Ordner einsortieren, dies erschwert bei einer großen Anzahl an System die Übersichtlichkeit.

## Situationen für mobile Anwendungen

Es gibt viele verschiedene Situationen in denen eine iPhone Anwendung Verwendung findet. Laut Josh Clark, iPhone Designer und Entwickler, können diese in drei Situationen zusammengefasst werden. <cite><a href="#tapworthy11">tapworthy11</a></cite>

### „Meine minimale Aufgabenverwaltung“

Ein Großteil der Anwendungen in dieser Kategorie sind zur Terminplanung, Aufgabenverwaltung oder Administration. Sie dienen der Produktivitätssteigerung und somit zum effektiven lösen von Problemen.

Die Anwendungen „Kalender“ oder „Things“, die zur Verwaltung von Terminen und Aufgaben dient, sind zum Anlegen von neuen Terminen oder Aufgaben optimiert. Hierfür befindet sich auf jeden Bildschirm ein Plus („+“), wie in der <a href="#microtasking">Abbildung 12</a> zu sehen.

<div class="figure" id="microtasking">
	<img src="http://up.frubar.net/1780/microtasking-cal.png" alt="microtasking-cal" width="35%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1781/microtasking-things.png" alt="microtasking-things" width="35%" />
	<p>Screenshot des Kalender und Things „App“</p>
</div>

Die mobile Anwendung zur Verwaltung der Cloud Infrastruktur fällt in diese Kategorie.

### „Was ist meiner Umgebung?“

Hierbei handelt es sich Hauptsächlich um Anwendungen die auf Kartenmaterial, beziehungsweise auf Sensoren des iPhones, zugreifen. Im Vordergrund der Anwendungen steht die Navigation und das Mitteilungsbedürfnis des Benutzers. 

<div class="figure" id="local">
	<img src="http://up.frubar.net/1787/local-map.png" alt="local-map" width="35%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1788/local-foursquare.png" alt="local-foursquare" width="35%" />
	<p>Screenshot der Karten und der Foursquare Anwendung</p>
</div>

### „Mir ist Langweilig“

In diese Kategorie fallen sowohl Spiele als auch Tools wie das Wetter „App“ oder der Wecker. Diese sind auch die beliebteste Kategorie<span class="fn"><a href="http://de.statista.com/statistik/daten/studie/166976/umfrage/beliebteste-kategorien-im-app-store/">Statista, Top 15 Kategorien im App Store (2012)</a></span> im App Store. Die Beliebtheit wird nach den Anteil aller verfügbaren „Apps“ im App Store gemessen.

Wie auf dem darauffolgenden Screenshot zu erkennen ist, hat das Spiel „Angry Birds“ keine iPhone Navigationselemente. Spiele nehmen meist den gesamten Bildschirm ein und verwenden ihre eigenen Symbole für die Navigation. Sogar die Statusbar mit der Empfangsanzeige, Uhrzeit und der Batterieanzeige werden ausgeblendet.

<div class="figure" id="bored">
	<img src="http://up.frubar.net/1786/bored-angrybirds.png" alt="bored-angrybirds" width="60%" />
	<p>Screenshot des Spiels Angry Birds</p>
</div>


# Konzeption

Für die Entwicklung einer iPhone Anwendung sollten grundlegende Punkte, wie die Struktur und die Benutzerinteraktion, beschrieben werden. Dies erfolgt in diesem Kapitel.


## Navigationsmodel

Der Aufbau der Navigation hängt von der Aufgabe der Anwendung ab, wie der vorherige Abschnitt <b>Situation für mobile Anwendungen</b> zeigt. Apple bietet hierzu drei verschiedene Navigationsmodelle an. Diese können sich innerhalb einer Anwendung nicht ändern, daher sollte man sich, vor der Entwicklung, für eines der folgenden Modelle entscheiden. 

<div class="figure" id="navigation-mode">
	<img src="http://up.frubar.net/1789/navigation-models.png" alt="navigation-model" width="80%" />
	<p>Navigationsmodelle (von links) - Ebenen, Tab-Navigation, Baum-Struktur</p>
</div>

### Ebenen

Die einzelnen Ebenen lassen sich am besten mit Spielkarten, die sich auf einem Stapel befinden, vergleichen. Auf allen Ebenen ist der Inhalt meist im selben Stil aufbereitet, somit findet dieses Navigationsmodel meist bei Tools und kleinen Anwendungen Verwendung.

<div class="figure" id="nav-flat">
	<img src="http://up.frubar.net/1792/nav-flat-first.png" alt="nav-flat-first" width="35%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1790/nav-flat.png" alt="nav-flat" width="35%" />
	<p>Screenshot der Wetter „App“</p>
</div>

Für die Navigation befindet sich ein „Punkt“ am unteren Bildschirmrand. Über diesen ist ersichtlich auf welcher Ebene man sich gerade befindet. Die Navigation erfolgt durch das verschieben der Ebenen von links nach rechts mit einem Finger.

<table>
	<thead>
		<tr><th style="width: 50%;">Vorteile</th><th>Nachteile</th></tr>
	</thead>
	<tbody>
		<tr>
			<td valign="top"><ul>
					<li>Ideal für zielgerichtet Inhalt; geeignet für gelegentliches verwenden der „App“</li>
					<li>Einfache Navigation; Gestengesteuert</li>
					<li>Viel Platz für den Inhalt; Navigation nimmt wenig Platz im Bildschirm ein</li>
				</ul>
			</td>
			<td valign="top"><ul>
					<li>Man muss durch alle Ebenen durchblättern; der Sprung zu einer speziellen Ebene ist nicht möglich</li>
					<li>Mehr als 20 Ebenen können nicht angezeigt bzw. erstellt werden</li>
					<li>Kein Scrollen möglich; somit keine langen Inhalte darstellbar</li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>

### Tab-Navigation

Am unteren Rand des Bildschirms befindet sich eine Tab-Navigation, ähnlich die eines Browsers. Im Gegensatz zu den „Tabs“ im Browser sind diese fest in der Anwendung verankert. Sie bietet auch maximal Platz für fünf Symbole.

<div class="figure" id="nav-flat">
	<img src="http://up.frubar.net/1791/nav-tap.png" alt="nav-tap" width="35%" style="padding-right: 1.5em;" />
	<img src="http://up.frubar.net/1793/nav-tap-instagram.png" alt="nav-flat-first" width="35%" />
	<p>Screenshot des App Stores und der Instagram „App“</p>
</div>

In der Tab-Navigation befinden sich meist Menüpunkte auf die der Anwender sehr schnell oder häufig zugreifen muss. So bietet sie bei der Anwendung „App Store“ die Suchfunktion, Kategorien oder verfügbare Updates an.

<table>
	<thead>
		<tr><th style="width: 50%;">Vorteile</th><th>Nachteile</th></tr>
	</thead>
	<tbody>
		<tr>
			<td valign="top"><ul>
					<li>Sofortigen Zugriff auf die Hauptfunktionen der Anwendung</li>
					<li>Klar erkennbare Menüpunkte anhand Symbol und Beschreibung</li>
				</ul>
			</td>
			<td valign="top"><ul>
					<li>Nur fünf Menüpunkte können gleichzeitig angezeigt werden</li>
					<li>Navigation verbraucht sehr viel Platz</li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>

### Baum-Struktur



## Formulare

## Tabellen


## Identität
Introducing your app, Logo, Aussehen

## Strukturierung
Story Board

## Usability-Tests
Planung, Ergebnis von Usability Tests
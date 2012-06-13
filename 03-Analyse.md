# Analyse

In diesem Kapitel erfolgt die Analyse zur Entwicklung der mobilen Anwendung. 

<q>Plan your work and work your plan.</q>
<div style="text-align: right; margin-right: 2em; margin-top: -2em;">
    Vince Lombardi
</div>

Die ersten Abschnitte beziehen sich auf die Projektplanung, wie die Definition der Zielgruppe und Ist-Zustandsanalyse. In den darauffolgenden Abschnitten wird die Konzeption und Identität anhand von Navigationskonzepte, Design eines Logos und Apple Design verdeutlicht. Gefolgt werden diese von der Strukturierung der Anwendung durch ein Story-Board und Usability-Tests anhand einiger Vorlagen.

## Zielgruppe

Die Definition der Zielgruppe und die Abfragen der Interessen der Anwender ist entscheidend für die Realisierung einer guten Anwendung.

### Brainstorming

Um die Zielgruppe und deren Anforderungen besser spezifizieren zu können, wurde in einem Meeting allen Mitglieder der Abteilung, ein Brainstorming abgehalten. Durch dieses Verfahren war es einfacher möglich eine genaue Ziel-Definition zu erstellen.

Mit der in <a href="#zielgruppe-brainstorming"><i>Abbildung 8</i></a> erstellten Mindmap konnte eine Definition abgeleitet werden. Für eine bessere kreative Arbeit wurde das Brainstorming aber mit Papier und Stift erstellt. Das Original befindet sich in der Anlage.

<div class="figure" id="zielgruppe-brainstorming">
	<img src="http://up.frubar.net/1756/zielgruppe-brainstorming.svg" alt="Zielgruppe Brainstorming" width="90%" />
	<p>Brainstorming mit und über die Zielgruppe</p>
</div>


### Definition

Die Zielgruppe für das Projekt umfasst Mitarbeiter einer IT Abteilung. Diese Mitarbeiter sind erfahrene IT Administratoren für die Betriebssysteme Linux und Windows. Sie sind vertraut mit der Handhabung eines Smartphones, insbesondere iPhones.

Den Benutzern ist die Verwendung von virtuellen Servern in einer Cloud-Landschaft bekannt. Die Technologie libvirt und Linux KVM im Zusammenhang mit Hardware-Virtualisierung ist ein Begriff.

---

## Ist-Zustandsanalyse

Zum jetzigen Zeitpunkt existiert noch keine mobile Anwendung (iPhone Anwendung) zur Verwaltung der Cloud Infrastruktur.

Zum Einsatz im Unternehmen kommt Citrix CloudStack <span class="fn"><a href="http://www.citrix.de/produkte/cloudstack/">Citrix CloudStack</a></span>. Hierbei handelt es sich um eine OpenSource Webanwendung zur Verwaltung einer Infrastruktur Cloud. Zwischen der Weboberfläche und der Virtualisierungstechnologie befindet sich die libvirt-Schnittstelle. Nach <a href="#libvirt-schnittstelle"><i>Abbildung 3 Einbindung libvirt Schnittstelle</i></a>, befindet sich CloudStack in der Anwenderschicht. Durch diese Schnittstelle ist es möglich verschiedene Virtualisierungstechnologien zu nutzen. 

Eine zufriedenstellende Verwendung von CloudStack ist nur in einem Browser mit ausreichend großem Bildschirm möglich. Auf einem Smartphone ist die Vielzahl an Funktionen unübersichtlich und im Notfall nicht verwendbar.

<div class="figure" id="cloudstack-dashboard">
	<img src="http://up.frubar.net/1773/cloudstack-dashboard.jpg" alt="cloudstack-dashboard" width="90%" />
	<p>CloudStack Dashboard <cite><a href="cstack12">cstack12</a></cite></p>
</div>

Da durch CloudStack auf die libvirt-Schnittstelle aufgesetzt wird, ist es sinnvoll diese auch für die Entwicklung der mobilen Anwendung zu verwenden.

## Anwendungsfunktionen

Um die Aufgabe der Anwendung besser definieren zu können folgt ein Aufstellung der Funktionen die geboten werden sollen. Die genauen Schritte für den Benutzer werden in der Konzeptionsphase und im Story-Board beschrieben.

<ul>
	<li><strong>Cloud Server</strong><br />
		Beim Cloud Server handelt es sich um das Host-System der virtuellen Server. Der Cloud Server stellt dem virtuellen Server Rechnerressourcen zur Verfügung.
		<ul>
			<li>Hinzufügen (Anzeigename, Hostname, Port, Benutzername, Kennwort)</li>
			<li>Bearbeiten</li>
			<li>Löschen</li>
		</ul>
	</li>
	<li><strong>Virtueller Server</strong><br />
		Virtuelle Server sind Gast-Systeme auf einem Cloud Server. Der virtuelle Server erhält Rechnerressourcen vom Cloud Server.
		<ul>
			<li>Hinzufügen (Anzeigename, Rechnerressourcen)</li>
			<li>Bearbeiten</li>
			<li>Löschen</li>
			<li>Anzeige Rechnerressourcen</li>
			<li>Bearbeiten der Rechnerressourcen</li>
			<li>Starten</li>
			<li>Stoppen</li>
			<li>Neustarten</li>
		</ul>		
	</li>
</ul>

Die veränderbaren Rechnerressourcen werden wie folgt definiert:

<ul>
	<li>Anzahl der CPUs</li>
	<li>Verwendbarer Arbeitsspeicher</li>
	<li>Angebotener Festplattenspeicher</li>
	<li>Aktivierung oder Deaktivierung von Remote Verbindungen</li>
</ul>

Beispielsweise, befindet sich der Administrator gerade nicht an seinem Arbeitsplatz, hat aber sein iPhone dabei. Durch die weitere Anwendung „Nagios“, für das Überwachen der virtuellen Server, erhält er den Hinweis, dass kein Arbeitsspeicher auf einem Server verfügbar ist. Mit der zu entwickelnden Anwendung kann der Administrator zum Beispiel per Schieberegler den Arbeitsspeicher eines virtuellen Server erhöhen.

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

Das sortieren von Servern in verschiedene Kategorien bzw. Ordner bietet eine hohe Übersichtlichkeit. Durch grüne oder rote Punkte wird Angezeigt ob ein Server erreichbar ist. Somit hat der Benutzer eine direkte Rückmeldung, ob er sich zum Server verbinden kann.

Einige Nachteile bieten die vielen Einstellungsmöglichkeiten auf der Übersichtsseite (<a href="#issh-overview"><i>Abbildung 10</i></a>, linkes Bild). Die „General Settings“, „Add Configuration“ und „Add Grouping“ wären an der Unterseite des Bildschirms oder in den iPhone Einstellungen besser aufgehoben.

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

<div class="figure" id="microtasking">
	<img src="http://up.frubar.net/1780/microtasking-cal.png" alt="microtasking-cal" width="35%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1781/microtasking-things.png" alt="microtasking-things" width="35%" />
	<p>Screenshot des Kalender und Things „App“</p>
</div>

Die Anwendungen „Kalender“ oder „Things“, die zur Verwaltung von Terminen und Aufgaben dienen, sind zum Anlegen von neuen Terminen oder Aufgaben optimiert. Hierfür befindet sich auf jedem Bildschirm ein Plus („+“), wie in der <a href="#microtasking"><i>Abbildung 12</i></a> zu sehen.

Die mobile Anwendung zur Verwaltung der Cloud Infrastruktur fällt in diese Kategorie.

### „Was ist in meiner Umgebung?“

Hierbei handelt es sich hauptsächlich um Anwendungen die auf Kartenmaterial, beziehungsweise auf Sensoren des iPhones, zugreifen. Im Vordergrund der Anwendungen steht die Navigation und das Mitteilungsbedürfnis des Benutzers. 

<div class="figure" id="local">
	<img src="http://up.frubar.net/1787/local-map.png" alt="local-map" width="35%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1788/local-foursquare.png" alt="local-foursquare" width="35%" />
	<p>Screenshot der Karten und der Foursquare Anwendung</p>
</div>

### „Mir ist Langweilig“

In diese Kategorie fallen sowohl Spiele als auch Tools wie das „Musik App“. Diese sind auch die beliebteste Kategorie<span class="fn"><a href="http://de.statista.com/statistik/daten/studie/166976/umfrage/beliebteste-kategorien-im-app-store/">Statista, Top 15 Kategorien im App Store (2012)</a></span> im App Store. Die Beliebtheit wird nach dem Anteil aller verfügbaren „Apps“ im App Store gemessen.

Wie auf dem Screenshot <a href="#bored"><i>Abbildung 14</i></a> zu erkennen ist, hat das Spiel „Angry Birds“ keine iPhone Navigationselemente. Spiele nehmen meist den gesamten Bildschirm ein und verwenden ihre eigenen Symbole für die Navigation. Sogar die Statusbar mit der Empfangsanzeige, Uhrzeit und der Batterieanzeige werden ausgeblendet.

<div class="figure" id="bored">
	<img src="http://up.frubar.net/1786/bored-angrybirds.png" alt="bored-angrybirds" width="60%" />
	<p>Screenshot des Spiels Angry Birds</p>
</div>


# Konzeption

<q>Structuring your app the Apple way.</q>
<div style="text-align: right; margin-right: 2em; margin-top: -2em;">
    Josh Clark
</div>

Für die Entwicklung einer iPhone Anwendung sollten grundlegende Punkte, wie die Struktur und die Benutzerinteraktion, beschrieben werden. Dies erfolgt in diesem Kapitel.

## Navigationsmodelle

Der Aufbau der Navigation hängt von der Aufgabe der Anwendung ab, wie der vorherige Abschnitt <a href="#situation-fur-mobile-anwendungen"><i>Situation für mobile Anwendungen</i></a> zeigt. Apple bietet hierzu drei verschiedene Navigationsmodelle an. Diese können sich innerhalb einer Anwendung nicht ändern, daher sollte man sich, vor der Entwicklung, für eines der folgenden Modelle entscheiden. 

<div class="figure" id="navigation-mode">
	<img src="http://up.frubar.net/1789/navigation-models.png" alt="navigation-model" width="80%" />
	<p>Navigationsmodelle (von links) - Ebenen, Tab-Navigation, Baum-Struktur</p>
</div>

---

### Ebenen

Die einzelnen Ebenen lassen sich am besten mit Spielkarten, die sich auf einem Stapel befinden, vergleichen. Auf allen Ebenen ist der Inhalt meist im selben Stil aufbereitet, somit findet dieses Navigationsmodel meist bei Tools und kleinen Anwendungen Verwendung.

<div class="figure" id="nav-flat">
	<img src="http://up.frubar.net/1792/nav-flat-first.png" alt="nav-flat-first" width="33%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1790/nav-flat.png" alt="nav-flat" width="33%" />
	<p>Screenshot der Wetter „App“</p>
</div>

Für die Navigation befindet sich ein „Punkt“ am unteren Bildschirmrand. Über diesen ist ersichtlich auf welcher Ebene man sich gerade befindet. Die Navigation erfolgt durch das verschieben der Ebenen von links nach rechts mit einem Finger.

<div class="table" id="nav-flat-table">
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
					<li>Nur geringes Scrollen möglich; somit nur teilweise langen Inhalte darstellbar</li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>
<p>Vorteile und Nachteile für das Navigationsmodell Ebenen</p>
</div>

### Tab-Navigation

Am unteren Rand des Bildschirms befindet sich eine Tab-Navigation, ähnlich die eines Browsers. Im Gegensatz zu den „Tabs“ im Browser sind diese fest in der Anwendung verankert. Sie bietet auch maximal Platz für fünf Symbole.

<div class="figure" id="nav-tab">
	<img src="http://up.frubar.net/1791/nav-tap.png" alt="nav-tap" width="33%" style="padding-right: 1.5em;" />
	<img src="http://up.frubar.net/1793/nav-tap-instagram.png" alt="nav-flat-first" width="33%" />
	<p>Screenshot des App Stores und der Instagram „App“</p>
</div>

In der Tab-Navigation befinden sich meist Menüpunkte auf die der Anwender sehr schnell oder häufig zugreifen muss. So bietet sie bei der Anwendung „App Store“ die Suchfunktion, Kategorien oder verfügbare Updates an.

<div class="table" id="nav-tab-table">
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
<p>Vorteile und Nachteile für die Tab-Navigation</p>
</div>

### Baum-Struktur

Die Baum-Struktur ist eines der häufig benutzten Navigationsmodelle. Gerade wenn viele Menüpunkte oder Ebenen benötigt werden kommt diese Struktur zum Einsatz. Eine sorgfältige Planung, welche Ebene nach welchem Menüpunkt kommt, ist zwingend erforderlich. Andernfalls kann es schnell sein, dass sich ein Benutzer nicht mehr in der Struktur zurecht findet.

<div class="figure" id="nav-tree">
	<img src="http://up.frubar.net/1794/nav-tree.png" alt="nav-tree" width="100%" />
	<p>Screenshot Baum-Struktur von Apple Mail</p>
</div>

Bei diesen Anwendungen ist meist die erste Ebene eine Übersichtsebene in Tabellenform, wodurch dann zu weiteren Ebenen navigiert werden kann. Im obersten Teil des Bildschirms befindet sich die Navigation um zur vorherigen Ebene zurückzukehren. 

<div class="table" id="nav-tree-table">
<table>
	<thead>
		<tr><th style="width: 50%;">Vorteile</th><th>Nachteile</th></tr>
	</thead>
	<tbody>
		<tr>
			<td valign="top"><ul>
					<li>Übersichtlich bei vielen Kategorien, Ebenen oder Menüpunkten</li>
					<li>Organisationsstruktur ist gut verständlich</li>
					<li>Direkte Interaktion mit dem Inhalt</li>
				</ul>
			</td>
			<td valign="top"><ul>
					<li>Übersichtsebene befindet sich nur am Anfang der Ebenen</li>
					<li>Ineffiziente Navigation bei vielen Ebenen</li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>
<p>Vorteile und Nachteile für das Baum-Struktur Navigationsmodell</p>
</div>

### Kombination der Navigationsmodelle

Meist findet eine Kombination aus zwei Navigationsmodellen statt, wie die Abbildung 18 von Apple Mail zeigt. Durch dies können mehrere Vorteile der unterschiedlichen Modelle genutzt werden.

Bei der Apple Mail Anwendung wird die „Tab-Navigation“ verkleinert, so das nur Symbole angezeigt werden. Hierbei handelt es sich um eine abgewandelte Form der Navigation und kann als Aktions-Buttons verstanden werden. Dem Benutzer ist es dadurch möglich schnell auf seine wichtigsten Funktionen zuzugreifen ohne einen Großteil seines Bildschirms einzuschränken.

## Darstellung des Inhalts

Ein klar strukturierter Inhalt erlaubt dem Benutzer auf die benötigten Informationen zuzugreifen. Ist die Darstellung unübersichtlich oder überladen beendet der Anwender die „App“ im schlimmsten Fall. Es sollte daher immer ein Kompromiss zwischen der Masse an Informationen und der Bildschirmgröße gefunden werden.

In vielen Fällen findet eine Kombination aus der Tabellendarstellung und der Benutzereingabe durch Formulare statt.

### Tabellen

Die Tabellen Darstellung beim iPhone kann nicht zu 100% mit klassischen Tabellen verglichen werden. Die Informationen werden meist zeilenweise gruppiert und es wird nur eine Spalte angezeigt. 

Aus folgenden Gründen kommt die Darstellung in Tabellenform zum Einsatz:
<ul>
	<li>Navigation durch die Baum-Struktur</li>
	<li>Liste an Optionen oder Einstellungen</li>
	<li>Lange Listen durch die schnell navigiert werden soll</li>
	<li>Detaillierter oder gruppierter Inhalt</li>
</ul>

<div class="figure" id="content-table">
	<img src="http://up.frubar.net/1802/view-table.png" alt="content-table" width="100%" />
	<p>Screenshot verschiedener Anwendungen mit Tabellen Darstellung</p>
</div>

Durch bestimmte Symbole an der rechten Seite ist erkennbar ob es sich um ein Navigationselement handelt. Die Schriftfarbe blau zeigt an, ob sich der Inhalt des Elements ändern lässt oder ggf. dynamisch ändert.

Drei der Standart Symbole sind wie folgt erklärt:
<div class="table" id="table-symbols">
<table>
	<tr>
		<td valign="middle" align="center"><img src="http://up.frubar.net/1803/view-table-icon_disclosure.png" /></td>
		<td>Weitere Informationen Symbol; durch das Tippen auf das Element wird eine neuer Bildschirm mit weiteren Informationen für den Benutzer sichtbar.</td>
	</tr>
	<tr>
		<td valign="middle" align="center"><img src="http://up.frubar.net/1804/view-table-icon_detail.png" /></td>
		<td>Details Symbol; ähnlich dem „Weitere Informationen Symbol“, beim direkten Tippen auf das Symbol sollen weitere Details zu diesem Element angezeigt werden.</td>
	</tr>
	<tr>
		<td valign="middle" align="center"><img src="http://up.frubar.net/1805/view-table-icon_check.png" /></td>
		<td>Check-Box Symbol; durch Tippen auf das Element wird die Check-Box aktiviert oder deaktiviert.</td>
	</tr>
</table>
<p>iPhone Standart Symbole</p>
</div>

Die Gruppierung der Elemente geschieht entweder durch ein Register (wie bei <a href="#content-table"><i>Abbildung 19</i></a>, links) oder durch farblich, zum Hintergrund abgehobene, Boxen (<a href="#content-table"><i>Abbildung 19</i></a>, mitte und rechts).

### Formulare

Die Formulare dienen dem Benutzer zur Eingabe von neuem Inhalt in die Anwendung. In dem meisten Fällen wir die Benutzereingabe durch die Auto-Korrektur unterstützt. 

Es ist Abhängig vom Eingabefeld welches Tastaturlayout für den Benutzer angezeigt wird. So wird bei üblicher Texteingabe die QWERTY-Tastatur angezeigt, beim Wählvorgang in der „Telefon-App“ jedoch nur der Nummernblock.

<div class="figure" id="form">
	<img src="http://up.frubar.net/1806/form-input-ipmi.png" alt="form-ipmi" width="35%" style="padding-right: 1.5em;" />
	<img src="http://up.frubar.net/1807/form-input-twitter.png" alt="form-twitter" width="35%" />
	<p>Screenshot von IPMI Touch und Twitter „App“ mit Eingabeformular</p>
</div>

## Identität

Die Identität einer Anwendung ist enorm wichtig für den Benutzer und dessen Wiedererkennungswert. Diese werden durch den Namen, eine klare Beschreibung, das Logo und Aussehen bewirkt.

Dieser Abschnitt bezieht sich explizit auf die Umsetzung der mobilen Anwendung zur Verwaltung der Cloud Infrastruktur.

### Name

Bei der Wahl des Namens ist zu beachten, dass nur begrenzt Platz auf dem Bildschirm und unterhalb des Logos ist. Da Apple zwischen dem Namen auf dem iPhone und dem im App Store unterscheidet, können zwei unterschiedliche Namen gewählt werden. So sollte der Name für das iPhone kurz und prägnant sein, der Name für den App Store mehr Beschreiben.

Namen die auf dem iPhone zu lang sind, werden automatisch in der Mitte gekürzt. Dadurch wird aus „Cloud infrastructure control via libvirt“,  „Cloud...bvirt“, was für den Benutzer nicht aussagekräftig ist. Von vielen Anwendungen wird daher ein allgemeiner Name auf dem iPhone verwendet, so wird aus „Dragon Dictation“ nur „Dictation“ oder aus „Al Jazeera English“, „AJE Live“.

Folgende Kurznamen standen während der Identitätsbildung zur Auswahl:
<ul>
	<li>**Cloud Control**<br />Aussagekräftiger Namen für die Verwaltung der Cloud. Die verwendete Technologie ist aber nicht erkennbar.</li>
	<li>**libvirt Control**<br />Verwaltung der verwendeten Technologie ist erkennbar.</li>
	<li>**libvirt Cloud**<br />Verwaltung der verwendeten Technologie ist erkennbar. Aber nicht das es sich um eine Anwendung zur Verwaltung dieser handelt.</li>
	<li>**InfraCloud**<br />Durch „Infra“ ist teilweise die Infrastruktur Cloud ersichtlich.</li>
	<li>**virtCloud**<br />Die Worte „Cloud“ und „virt“ für Virtuell können fast gleich gesetzt werden. Daher ist die Beschreibung redundant.</li>
</ul>

Nach Absprache und Analyse mit den Mitarbeitern der IT Abteilung wurde der Name „Cloud Control“ als aussagekräftigster Name ausgewählt. Die verwendete Technologie kann in der Beschreibung oder im Namen für den App Store angezeigt werden. Als Name für den App Store wird daher „Cloud Control &ndash; manage your libvirt infrastructure“ verwendet.

---

### Logo

Das Logo ist ein weiteres Identitätsmerkmal für die Anwendung, wenn nicht sogar das wichtigste. Der erste Blick des Benutzers fällt meist auf das Logo anstatt auf den Namen. Es sollte entweder die Funktion oder den Namen im Logo wiedererkennbar sein. Bekannte Anwendungen oder Unternehmen greifen meist auf ihr Logo in abgeänderter Form oder ihren Initialen zurück. 

<div class="figure" id="ident-logo">
	<img src="http://up.frubar.net/1808/ident-logo-things.tiff" alt="ident-logo-things" width="15%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1809/ident-logo-insta.tiff" alt="ident-logo-instagram" width="15%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1810/ident-logo-cellarrat.tiff" alt="ident-logo-cellarrat" width="15%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1811/ident-logo-twitter.tiff" alt="ident-logo-twitter" width="15%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1812/ident-logo-facebook.tiff" alt="ident-logo-facebook" width="15%" />
	<p>„App“-Logos (von links). Things, Instagram, Cellar Rat, Twitter, Facebook</p>
</div>

Wie gut ein Logo erkennbar ist, hängt meist von der Auflösung und der Detailgenauigkeit ab. Ein „App“-Logo muss mindestens für drei verschiedene Auflösungen erstellt werden. So verwendet das iPhone für kleine Logos eine Auflösung von 29x29 Pixel und für mittlere Logos 57x57 Pixel. Ein großes Logo mit 512x512 Pixel wird für den App Store benötigt.

Für die eigene Anwendung soll das Logo die Funktion widerspiegeln und Begriffe wie „Cloud“, „Computer“, „Netzwerk“ und „libvirt“ sollen erkennbar sein. Nach Skizzen, die sich im Anhang befinden, wurde ein Logo entworfen. Im größten Logo wird sich der Begriff „libvirt“ als Zusatz befinden. In den kleineren ist dies nicht mehr lesbar, daher wurde er entfernt.

<div class="figure" id="cloud-control">
	<img src="http://up.frubar.net/1814/logo-cc-libvirt.png" alt="logo-cc-libvirt" width="20%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1813/logo-cc.png" alt="logo-cc" width="20%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1813/logo-cc.png" alt="logo-cc" width="12%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1813/logo-cc.png" alt="logo-cc" width="5%" style="padding-right: 1.5em;"/>
	<p>Erster Entwurf. Logos des Cloud Control „Apps“</p>
</div>

Nach einigen Befragungen der Mitarbeiter wurde festgestellt, dass das Logo zwar die Begriffe darstellt aber gegenüber anderen Logos langweilig und zu technisch wirkt. Es wurde daher ein modernes Logo entworfen, dass die Begriffe „Cloud“ und „Control“ darstellt.

<div class="figure" id="cloud-control-more-cloud">
	<img src="http://up.frubar.net/1821/logo-cc-more-cloud.png" alt="cloud-control-more-cloud" width="20%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1821/logo-cc-more-cloud.png" alt="cloud-control-more-cloud" width="12%" style="padding-right: 1.5em;"/>
	<img src="http://up.frubar.net/1821/logo-cc-more-cloud.png" alt="cloud-control-more-cloud" width="5%" style="padding-right: 1.5em;"/>
	<p>Zweiter Entwurf. Logos des Cloud Control „Apps“</p>
</div>


### Design

Design und äußerliche Erscheinung sind meistens Geschmacksfragen, doch spielt der Erkennungswert und die Benutzerfreundlichkeit auch eine Rolle. Die Navigation und die Anordnung bzw. Strukturierung von Inhalt kann nur teilweise bei iPhone „Apps“ verändert werden. 

Einige Anbieter von „Apps“ setzen daher auf das Standart iPhone Design und passen lediglich Farbgebung und Symbole an. Um die Benutzer der „Cloud Control App“ nicht zu verunsichern, sowie Übersichtlichkeit und Einfachheit zu gewährleisten wird ebenfalls das Standart iPhone Design verwendet.

## Strukturierung

Eine gute Struktur der Anwendung ist vergleichbar mit dem „roten Faden“ in einem Manuskript. Ohne diesen ist es dem Benutzer nicht möglich zu erkennen welches Ergebnis auf ein Navigationselement erfolgt.

Abhängig vom verwendeten Navigationsmodel muss die Anwendung anders strukturiert werden. So bietet die Baum-Struktur mehr Möglichkeiten der „Verzweigung“ im Gegensatz zu den flachen Ebenen. Eine Strukturierung erfolgt am besten durch die Skizzen auf Papier oder durch Mockups mit einer Anwendung am Computer. 

<div class="figure" id="storyboard">
	<img src="http://up.frubar.net/1815/storyboard-part.jpg" alt="storyboard" width="100%" />
	<p>Ausschnitt Cloud Control Story-Board</p>
</div>

Für diesen Zweck wurde ein „Story-Board“ auf Papier entworfen, dieses befindet sich im Anhang. Mit diesem war es möglich erste Prototypen zu entwerfen und in den Usability-Tests anzuwenden. Das Story-Board wurde während den Tests verändert und erweitert.

## Usability-Tests

Die Usability-Tests dienen dem Entwickler seine Anwendung mehr aus der Sicht des Nutzers zu betrachten. Die Sichtweisen sind meist Unterschiedlich, da der Entwickler seine Anwendung entworfen hat und das Navigationskonzept kennt.

Ziel des Tests ist es Unstimmigkeiten in der Navigation und Handhabung der Anwendung aufzudecken um diese im Anschluss optimieren zu können.

### Durchführung

Für den Zweck des Usability-Tests wurde mit drei Mitarbeitern (männlich, Alter 20-30) ein Thinking-Aloud Test<span class="fn"><a href="http://www.useit.com/alertbox/thinking-aloud-tests.html">Thinking Aloud Test</a></span> durchgeführt. Die Mitarbeiter haben Vorkenntnisse über Smartphones, mobile Anwendungen und kennen das Bedienkonzept des iPhones.

---

Jeder Mitarbeiter wird einzeln befragt und erhält während der Testphase Aufgaben die er an Prototypen durchführen soll. Es werden zwei Prototypen betrachtet:
<ul>
	<li>**Prototyp 1**: Mock-up auf Papier</ul>
	<li>**Prototyp 2**: Anwendung auf dem iPhone</ul>
</ul>

Die Ergebnisse werden schriftlich fixiert um daraus eine Optimierung ableiten zu können. Es wird expliziert gebeten Ideen und Veränderungsvorschläge einzubringen. Der Test dauert pro Person zwischen 20-40 Minuten.

### Szenarien

In diesem Abschnitt werden die Aufgaben der Mitarbeiter beschrieben. Zwischen den Prototypen sind die Aufgaben ähnlich, beim Prototyp 1 können einige Aufgaben nicht vorgenommen werden.

<ul>
	<li><strong>Start der Anwendung</strong> <br/>Betrachten Sie die Anwendung und die Navigationselemente. Was ist Ihr erster Eindruck? Ist Ihnen das Ziel der Anwendung klar?</li>
	<li><strong>Cloud Server hinzufügen</strong> <br />Fügen Sie einen neuen Cloud Server hinzu. Wie gehen Sie vor?</li>
	<li><strong>Cloud Server bearbeiten</strong> <br />Ändern Sie den Namen oder ein anderes Attribut des Cloud Servers. Wie gehen Sie vor?</li>
	<li><strong>Status Abfrage</strong> <br />Wie erkennen Sie den aktuellen Status Ihrer Server? Wo würden Sie nachsehen?</li>
	<li><strong>Virtual Server hinzufügen</strong> <br />Fügen Sie einen virtuellen Server zu einem bestehenden Cloud Server hinzu. Wie gehen Sie vor?</li>
	<li><strong>Virtual Server Details</strong> <br />Lassen Sie sich Details zu einem virtuellen Server anzeigen. Wie viel Speicherplatz wird verwendet?</li>
	<li><strong>Virtual Server bearbeiten</strong> <br />Ändern Sie ein Attribut eines virtuellen Servers. Fügen Sie z.B. mehr Arbeitsspeicher hinzu. Wo würden Sie dies tun?</li>
	<li><strong>Virtual Server Neustarten</strong> <br />Starten Sie einen virtuellen Server neu. Wie gehen Sie vor?</li>
	<li><strong>Virtual Server löschen</strong> <br />Löschen Sie einen virtuellen Server von einem Cloud Server. Wie würden Sie vorgehen?</li>
</ul>

### Ergebnisse

Es wurde festgestellt, dass der Prototyp 1, das Mock-up auf Papier, für den Test ungeeignet war. Somit wurde lediglich Prototyp 2, die iPhone Anwendung, bewertet. Zur Konzeptionsphase und für Erweiterungen wird aber weiterhin das Mock-up verwendet.

#### Erster Start

Die Anwendung wirkt beim ersten Start leer, da noch keine Cloud Server vorhanden sind. Der Benutzer findet sich daher nur schwer zu recht und fühlt sich mit der neuen Anwendung „allein gelassen“.

Es wurden Tooltips hinzugefügt die beim erster Start und falls noch keine Server vorhanden sind, angezeigt werden.

<div class="figure" id="cc-intro">
	<img src="http://up.frubar.net/1831/cloud-control-intro.png" alt="cc-intro" width="50%" />
	<p>Erster Start der Anwendung, Erweiterung durch Tooltips</p>
</div>

#### Navigation

Die Navigation wurde von den Benutzern gut angenommen, sie fanden sich in der Baum-Struktur gut zu recht.

Es stellte sich aber heraus, dass für das Löschen eines virtuellen Servers keine Funktion im Story-Board vorgesehen war. Somit war es dem Benutzer nicht möglich einen virtuellen Server zu löschen. Dies wurde mit einen Editieren-Button bei der Übersichtsseite der virtuellen Server gelöst.

Des Weiteren fiel auf, dass virtuelle Server die Ausgeschalten sind nicht auf der Übersichtsseite erkennbar waren. Nach einer Änderung werden diese nun grau in der Liste angezeigt und an die unterster Stelle sortiert.

#### Status Abfrage

In der ersten Version wurde der Cloud Status nur an der unteren rechten Seite angezeigt. Somit war es für den Benutzer nicht zu erkennen welcher Server ein Problem aufweist. Es wird daher bei jedem Cloud und virtuellen Server der Status an der rechten Seite angezeigt.

<div class="figure" id="cc-status">
	<img src="http://up.frubar.net/1832/cloud-control-status.png" alt="cc-status" width="50%" />
	<p>Cloud Status, rechts bei jedem Cloud Server</p>
</div>

#### Sonstige Anmerkungen

Beim Neustart des virtuellen Servers erfolgte keine Abfrage ob der Benutzer wirklich den Server Neustarten möchte. Hierzu erscheint nun eine Dialogbox die vom Benutzer bestätigt oder abgebrochen werden kann.
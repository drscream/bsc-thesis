# Analyse

In diesem Kapitel erfolgt die Analyse zur Entwicklung der mobilen Anwendung. 

<q>Plan your work and work your plan.</q>
<div style="text-align: right; margin-right: 2em; margin-top: -2em;">
    Vince Lombardi
</div>

Die ersten Abschnitte beziehen sich auf die Projektplanung, wie die Definition der Zielgruppe und Ist-Zustandsanalyse. In den darauffolgenden Abschnitten wird die Konzeption und Identität anhand Navigationskonzepte, Design eines Logos und Apple Design verdeutlicht. Gefolgt werden diese von der Strukturierung der Anwendung durch ein Story-Board und Usability-Tests Anhand einiger Vorlagen.

## Zielgruppe

Die Definition der Zielgruppe und die Abfragen der Interessen der Anwender ist entscheiden für die Realisierung einer guten Anwendung.

### Brainstorming

Um die Zielgruppe und deren Anforderungen besser spezifizieren zu können, wurde in einem Meeting aller Mitglieder der Abteilung, ein Brainstorming abgehalten. Durch dieses Verfahren war es einfacher möglich eine genaue Definition zu erstellen.

Mit der in <a href="#zielgruppe-brainstorming">Abbildung 7</a> erstellte Mindmap konnte eine Definition abgeleitet werden. Für eine bessere kreative Arbeit wurde das Brainstorming aber mit Papier und Stift erstellt. Das Original befindet sich in der Anlage.

<div class="figure" id="zielgruppe-brainstorming">
	<img src="http://up.frubar.net/1756/zielgruppe-brainstorming.svg" alt="Zielgruppe Brainstorming" width="90%" />
	<p>Brainstorming mit und über die Zielgruppe</p>
</div>


### Definition

Die Zielgruppe für das Projekt umfasst Mitarbeiter einer IT Abteilung. Diese Mitarbeiter sind erfahrene IT Administratoren für die Betriebssysteme Linux und Windows. Sie sind vertraut mit der Handhabung eines Smartphones, insbesondere iPhones.

Den Benutzern ist die Verwendung von virtuellen Servern in einer Cloud-Landschaft bekannt. Die Technologie libvirt und Linux KVM im Zusammenhang mit Hardware-Virtualisierung ist ein Begriff.

## Ist-Zustandsanalyse



## Alternative Anwendungen

Da aktuell noch keine Anwendungen für die Verwaltung von virtuellen Rechnerinstanzen existieren werden alternative IT-relevante Anwendungen betrachtet. Ein Teil der Erfahrungen mit diesen Anwendungen wird in der Realisierungsphase nützlich sein.

Die Anwendungen werden kurz Beschrieben und die grafischen Benutzeroberflächen bewertet.

### iSSH

Die Anwendung „iSSH - SSH / VNC Console“ bietet IT Administratoren die Möglichkeit sich mit einer Remote Verbindung auf einen Server zu verbinden und diesen zu verwalten. Unterstützt werden viele verschiedenste Protokolle, wie SSH<span class="fn"><a href="http://openssh.org">SSH</a></span> und Windows Remote Desktop<span class="fn"><a href="http://support.microsoft.com/?scid=kb%3Ben-us%3B186607&x=13&y=11">Windows Remote Desktop</a></span>.

<div class="figure" id="issh-overview">
	<img src="http://up.frubar.net/1768/issh-overview.png" alt="issh-overview" width="35%" />
	<img src="http://up.frubar.net/1770/issh-overview-server.png" alt="issh-overview-server" width="35%" />
	<p>iSSH Kategorisierung und Übersicht der Server</p>
</div>

Das sortieren von Servern in verschiedene Kategorien bzw. Ordner bietet eine hohe Übersichtlichkeit. Durch grüne oder rote Punkte wird Angezeigt ob ein Server erreichbar ist. Somit hat der Benutzer eine direkte Rückmeldung ob er sich zum Server verbinden kann.

Einige Nachteile bieten die vielen Einstellungsmöglichkeiten auf der Übersichtsseite (Abbildung 8, linkes Bild). Die „General Settings“, „Add Configuration“ und „Add Grouping“ wären an der Unterseite des Bildschirms oder in den iPhone Einstellungen besser aufgehoben.

### IPMI Touch

Bei „IPMI Touch“ handelt es sich um ein weiteres IT Verwaltungswerkzeug von Servern. Es liest Hardwareinformationen eines Servers über das IPMI Protokoll<span class="fn"><a href="http://www.intel.com/design/servers/ipmi/">IPMI</a></span> aus. Für diese Informationen werden Temperatursensoren des Gehäuses ausgelesen, die Geschwindigkeit der Lüfter und der aktuelle Stromverbrauch. Über die Anwendung ist es dem Administrator auch möglich den Server auszuschalten.

<div class="figure" id="ipmi-overview">
	<img src="http://up.frubar.net/1771/ipmi-overview.png" alt="ipmi-overview" width="35%" />
	<img src="http://up.frubar.net/1772/ipmi-server.png" alt="ipmi-server" width="35%" />
	<p>IPMI Touch Übersicht und Hardwareinformationen</p>
</div>
	
Auf der Übersichtsseite der Anwendung ist durch die farblichen Unterschiede und Symbole sofort erkennbar bei welchem Server Probleme vorhanden sind. Klickt der Benutzer auf einen Menüpunkt erhält er eine detaillierte Anzeige der Hardware, in der ebenso farblich Probleme gekennzeichnet sind. Hinzufügen neuer Server erfolgt über das Plus („+“) in der oberen rechten Ecke des Bildschirms und braucht somit keinen Platz in der Anzeige.

Server lassen sich bei dieser Anwendung nicht in Kategorien oder Ordner einsortieren, dies erschwert bei einer großen Anzahl an System die Übersichtlichkeit.

## Konzeption
Design, Bildschirmgröße, Apple iOS, iPhone
Navigation innerhalb einer Anwendung

## Identität
Introducing your app, Logo, Aussehen

## Strukturierung
Story Board

## Usability-Tests
Planung, Ergebnis von Usability Tests
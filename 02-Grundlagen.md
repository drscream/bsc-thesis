# Grundlagen

In diesem Kapitel werden einige Grundlagen und Grundbegriffe näher erläutert. Die Erklärung erfolgt auf Basis der benötigten Informationen für die Bachelorarbeit.

## Mobile Endgeräte

Der Begriff mobile Endgeräte wird umgangssprachlich mit Mobiltelefone, Smartphones und PDAs gleichgesetzt. Unter diesen Begriff fallen aber alle Geräte die ohne größere körperliche Anstrengung transportiert und mobil eingesetzt werden können. Somit auch MP3-Player, Notebooks oder Tablet-PCs.

In der Bachelorarbeit wird der Fokus auf Smartphones und die mobilen Anwendungen gelegt.

### Smartphones

Smartphones stellen die Computerfunktionalität auf einem Mobiltelefon zur Verfügung. Sie sind durch ihre Konstruktion und Bedienung nicht zum Telefonieren optimiert, stattdessen ermöglichen Sie die Verwendung von einer großen Anzahl an Anwendungen. Daher sind typische Merkmale ein großer Touchscreen und eine alphanumerische Tastatur.

### mobile Anwendungen

Eine mobile Anwendung, im allgemeinen Sprachgebraucht „App“ genannt, ist eine Software die für ein Smartphone entwickelt wurde und meist über einen integrierten Onlineshop bezogen werden kann.

Die ersten Mobiltelefone enthielten schon Anwendungen wie Kalender, Taschenrechner oder Spiele. Durch die Entwicklung von Java ME<span class="fn"><a href="http://www.oracle.com/technetwork/java/javame">Java ME</a></span> war es auch Entwicklern möglich weitere mobile Anwendungen zu programmieren und zur Verfügung zu stellen. Aber erst mit der Erscheinung von Apples iPhone und Googles Android Smartphones, wurden die „App“ populär. Dies ist nicht allein dem Marketingkonzept zuzuschreiben, auch wenn dies einen großen Einfluss auf die Popularität hatte. Die vereinfachte Installation und Bereitstellung über integrierte Onlineshops konnte die breite Bevölkerung ansprechen. 

Im Oktober 2011 befanden sich über 400.000 Anwendungen<span class="fn"><a href="http://de.statista.com/statistik/daten/studie/208599/umfrage/anzahl-der-apps-in-den-top-app-stores/">Statista, Anzahl der Apps in den Top App-Stores im Oktober 2011</a></span> im App Store von Apple. Hinzu kommt im März 2012 würden über 20 Millionen Downloads<span class="fn"><a href="http://de.statista.com/statistik/daten/studie/20149/umfrage/anzahl-der-getaetigten-downloads-aus-dem-apple-app-store/">Statista, Anzahl der heruntergeladenen Anwendungen im Apple App Store</a></span> im gemessen. Diese Zahlen zeigen den wachsenden Markt für mobile Anwendungen.

## Cloud-Computing

Die Cloud beschreibt die Abstraktion von IT Infrastruktur wie z.B. Rechenkapazität, Speicherbedarf oder auch Software. Diese können bei Bedarf und zur Verfügung gestellt werden.

<div class="figure" id="cloud-computing-diagram">
	<img src="http://up.frubar.net/1747/cloud_computing_diagram.jpg" alt="Cloud Computing Diagram" width="80%" />
	<p>Elemente des Cloud-Computing</p>
</div>

### Technische Realisierungen

Cloud-Computing wird in drei technische Schichten, in einen so genannten Cloud-Stack, aufgeteilt. Jeder Schicht stellt einen Grad der Abstraktion dar. <a href="#bartonb08"><cite>bartonb08</cite></a>

#### Infrastruktur

„Infrastructure as a Service“ befindet sich an der untersten Schicht im Cloud-Stack. Der Benutzer verwaltet seine virtuellen Server (Rechnerinstanzen) selbst. Der Cloud-Dienst selbst ist skalierbar ausgelegt, jedoch nicht zwingend die Programme die der Benutzer auf den Rechnerinstanzen installiert. 

Je nach Anforderung kann der Cloud-Dienst um Rechnerinstanzen erweitert oder verkleinert werden. Der Benutzer ist hierbei ab der Betriebssystemebene für seine Instanz selbst verantwortlich.

#### Plattform

Bei „Platform as a Service“ steht die Anwendung des Entwicklers im Vordergrund. Der Entwickler stellt seine Anwendung über die Cloud zur Verfügung, diese kümmert sich um die Aufteilung auf die Rechnungsinstanzen.

Da der Benutzer nur seine Anwendung liefert, kann die Cloud die Anzahl der tatsächlichen Instanzen jederzeit erhöhen oder reduzieren. In der Cloud werden vom Benutzer gelieferte Daten verarbeitet, das umliegende System ist für ihn nicht einsehbar.

#### Anwendung

Der Benutzer verwenden bei „Software as a Service“ eine bereits bestehende Anwendung in der Cloud. Für Ihn sind die Platform und die Infrastruktur nicht sichtbar. 

Beispiele für eine Cloud-Anwendung sind unter anderem Google Drive<span class="fn"><a href="http://drive.google.com">Google Drive</a></span>, DropBox<span class="fn"><a href="http://www.dropbox.com">DropBox</a></span> und Microsoft Office Communications Online<span class="fn"><a href="http://www.microsoft.com/online/de-de/prodComm.aspx">Microsoft Office Communications Online</a></span>.

### Organisatorische Arten

Die Cloud wird meist, abhängig vom Anwendungsfall, in drei Organisationsformen eingeordnet. <cite><a href="#cloudadop10">cloudadop10</a></cite>

#### Private Cloud

Die Anbieter und Nutzer der „Private Cloud“ stammen aus der selben Organisation oder dem selben Unternehmen. Daten innerhalb dieser Cloud sind nur der Organisation zugänglich und nicht außerhalb erreichbar, dies bietet einen großen Sicherheitsaspekt.

#### Public Cloud

Die „Public Cloud“ ist nicht für eine Organisation beschränkt, sie ist öffentlich erreichbar und jeden zugänglich. Eine wichtige Rolle spielt hierbei die Datensicherheit. Jeder Benutzer muss hierbei selbst Entscheiden welche und wie viele Daten er in der Cloud speichert.

#### Hybrid Cloud

Hierbei handelt es sich um eine Mischung aus „Private und Public Cloud“. Eine Organisation verwendet eine „Private Cloud“ und wechselt im Fehlerfall oder bei hoher Belastung zur „Public Cloud“.

##  Virtualisierung

Für die Virtualisierung gibt es viele verschiedene Methoden, abhängig ob eine Anwendung oder ein gesamtes Betriebssystem virtualisiert werden soll. Die Virtualisierung spielt eine wichtige Rolle für die Cloud Infrastruktur. Für die Bachelorarbeit hat die Hardware Virtualisierung bzw. Paravirtualisierung, somit die Bereitstellung von Rechnerinstanzen, Relevanz.

### Hardware Virtualisierung

Die virtuelle Maschine stellt dem Gastbetriebssystem Teilbereiche der Hardware in Form von virtueller Hardware zur Verfügung. Somit kann ein unverändertes Betriebssystem darauf in einer isolierten Umgebung laufen. Das Gastsystem muss hierbei für den gleichen CPU-Typ ausgelegt sein.

### Paravirtualisierung

Bei Paravirtualisierung wird zwar ein Betriebssystem virtuell gestartet, jedoch wird keine Hardware virtualisiert, sondern die Betriebssysteme verwenden eine abstrakte Verwaltungsschicht, um auf gemeinsame Ressourcen (Netzanbindung, Festplattenspeicher) zuzugreifen. Damit das Betriebssystem auf der virtuellen Maschine ausgeführt werden kann muss es teilweise portiert werden. Durch diese Portierung kann sich die Leistung der virtuellen Maschine erhöhen. <cite><a href="#degelas08">degelas08</a></cite>

### Schnittstelle zur Virtualisierung

Durch die verschiedenen Virtualisierungstechnologien und Verfahren wird es den Entwickler nicht einfach gemacht Anwendungen zu entwerfen die mit allen Schnittstellen umgehen können. Libvirt bietet eine einheitliche Schnittstelle (API) um verschiedene Technologien wie Linux KVM<span class="fn"><a href="http://www.linux-kvm.org">Linux KVM</a></span>, Xen<span class="fn"><a href="http://www.xen.org">Xen</a></span> und VMware ESX<span class="fn"><a href="http://www.vmware.com">VMWare ESX</a></span> zu verwalten.

<div class="figure" id="libvirt-schnittstelle">
	<img src="http://up.frubar.net/1748/libvirtd.svg" alt="libvirt Schnittstelle" width="80%" />
	<p>Einbindung libvirt Schnittstelle</p>
</div>
	
## Usability und User friendlyness

<q>People don't want dump from your app; they want simplicity and ease.</q>
<div style="text-align: right; margin-right: 2em; margin-top: -2em;">
    Josh Clark - iPhone Designer und Entwickler
</div>

Usability (Gebrauchstauglichkeit) und User friendlyness (Benutzerfreundlichkeit) sind eng verwandte Begriffe und sollen die Nutzbarkeit und Zufriedenheit für den Kunden erhöhen. So kann durch <cite><a href="#ISO9126">ISO 9126</a></cite> (Benutzbarkeit) und <cite><a href="#ISO9241">ISO 9241</a></cite> (Gebrauchstauglichkeit) folgende Formel abgeleitet werden:
<pre>
Benutzbarkeit = Effektivität + Effizienz
Gebrauchstauglichkeit = Benutzbarkeit + Zufriedenstellung
Benutzerfreundlichkeit = Gebrauchstauglichkeit + Zufriedenheit + Nützlichkeit
</pre>

Zudem lassen sich folgende fünf Attribute für den Begriff Usability definieren <cite><a href="nie93">nie93</a></cite>:
<ul>
	<li>**Effektivität**: Das System sollte leicht zu erlernen sein, damit der Benutzer möglichst schnell seine Arbeit erledigen kann.</li>
	<li>**Effizienz**: Das System sollte effizient genutzt werden können, damit der Benutzer produktiv damit arbeiten kann, nachdem er es erlernt hat.</li>
	<li>**Einprägsamkeit**: Das System sollte sich dem Benutzer leicht einprägen, damit er auch nach einer längeren Pause, in der der Benutzer das System nicht verwendet hat, es wieder verwenden kann ohne es neu lernen zu müssen.
	<li>**Fehler**: Das System sollte wenige Fehler vom Benutzer zulassen, Fehler sollten sich leicht beheben lassen und schwerwiegende Fehler sollten gar nicht erscheinen.
	<li>**Zufriedenheit**: Das System sollte angenehm bei der Verwendung sein, damit der Benutzer mit dem System zufrieden ist und es mag.</li>
</ul>

In dieser Arbeit bezieht sich der Begriff Usability nur auf die Gebrauchstauglichkeit von mobilen Anwendungen, nicht auf die Usability des Gerätes oder anderer Software.

In diesem Abschnitt werden die bekanntesten Usability Regeln aufgeführt und die Relevanz für mobile Anwendungen dargestellt. Die eigentliche Anwendung der Regeln und Usability Konzepte erfolgt in Kapitel <a href="#analyse"><b>3. Analyse</b></a>.

### Usability Regeln



### Relevanz für mobile Anwendungen



#### Bildschirmgröße

#### Touchscreen


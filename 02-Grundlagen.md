# Grundlagen

In diesem Kapitel werden einige Grundlagen und Grundbegriffe näher erläutert. Die Erklärung erfolgt auf Basis der benötigten Informationen für die Bachelorarbeit.

## Mobile Endgeräte

Der Begriff mobile Endgeräte wird umgangssprachlich mit Mobiltelefone, Smartphones und PDAs gleichgesetzt. Unter diesen Begriff fallen aber alle Geräte, die ohne größere körperliche Anstrengung transportiert und mobil eingesetzt werden können. Somit auch MP3-Player, Notebooks oder Tablet-PCs. <cite><a href="#wiki11a">wiki11a</a></cite>

In der Bachelorarbeit wird der Fokus auf Smartphones und die mobilen Anwendungen gelegt.

### Klassische Mobiltelefone

Die klassischen Mobiltelefone sind meist mit einem Nummernblock und integriertem T9 Ziffernblock<span class="fn"><a href="http://worldwide.espacenet.com/publicationDetails/biblio?CC=EP&NR=1256871A2&KC=A2&FT=D&ND=3">T9 Ziffernblock Patent</a></span> ausgestattet. Die Größe und Farbtiefe des Bildschirms ist deutlich geringer als bei einem Smartphone.

Bei neueren Modellen besteht zum Teil die Möglichkeiten Anwendungen in der Programmiersprache Java zu entwickeln. Die Schnittstellen zum Betriebssystem des Mobiltelefons erlauben aber nur einen Bruchteil der möglichen Funktionen.

### PDAs

Die persönlich digitalen Assistenten, kurz PDAs, sind eine Kombination aus den klassischen Mobiltelefonen und Computern. Sie bieten zur Telefonfunktion auch persönliche Kalender-, Adress- und Aufgabenverwaltung an. PDAs können zusätzlich Office-Dateien verarbeiten. Sie werden durch die Smartphones langsam vom Markt verdrängt. 

### Smartphones

Smartphones stellen die Computerfunktionalität auf einem Mobiltelefon zur Verfügung. Diese Geräte sind über die verschiedensten Telekommunikationsdienste, wie UMTS<span class="fn">Universal Mobile Telecommunications System</span>, HSDPA<span class="fn">High Speed Downlink Packet Access</span> oder Wireless-LAN, internetfähig.

Sie sind durch ihre Konstruktion und Bedienung nicht zum Telefonieren optimiert, stattdessen ermöglichen Sie die Verwendung von einer großen Anzahl an Anwendungen. Daher sind typische Merkmale ein großer Touchscreen und eine alphanumerische Tastatur. Die Tastatur befindet sich im Touchscreen, was die Eingabe erschweren kann.

### mobile Anwendungen

Eine mobile Anwendung, im allgemeinen Sprachgebraucht „App“ genannt, ist eine Software die für ein Smartphone entwickelt wurde und meist über einen integrierten Onlineshop bezogen werden kann.

Die ersten Mobiltelefone enthielten schon Anwendungen wie Kalender, Taschenrechner oder Spiele. Durch die Entwicklung von Java ME<span class="fn"><a href="http://www.oracle.com/technetwork/java/javame">Java ME</a></span> war es auch Entwicklern möglich weitere mobile Anwendungen zu programmieren und zur Verfügung zu stellen. Aber erst mit dem Erscheinen von Apples iPhone und Googles Android Smartphones, wurden die „App“ populär. Dies ist nicht allein dem Marketingkonzept zuzuschreiben, auch wenn dies einen großen Einfluss auf die Popularität hatte. Die vereinfachte Installation und Bereitstellung über integrierte Onlineshops konnte die breite Bevölkerung ansprechen. 

Im Oktober 2011 befanden sich über 400.000 Anwendungen<span class="fn"><a href="http://de.statista.com/statistik/daten/studie/208599/umfrage/anzahl-der-apps-in-den-top-app-stores/">Statista, Anzahl der Apps in den Top App-Stores im Oktober 2011</a></span> im App Store von Apple. Dazu wurden im März 2012 über 20 Millionen Downloads<span class="fn"><a href="http://de.statista.com/statistik/daten/studie/20149/umfrage/anzahl-der-getaetigten-downloads-aus-dem-apple-app-store/">Statista, Anzahl der heruntergeladenen Anwendungen im Apple App Store</a></span> App Store im gemessen. Durch diese Zahlen ist der Trend für steigende Entwicklung von mobilen Anwendungen klar erkennbar.

## Cloud-Computing

Die Cloud ist ein umschreibender Begriff für den Ansatz IT Infrastruktur, wie zum Beispiel Rechenkapazität, Speicherbedarf oder auch Software über ein Netzwerk zur Verfügung zu stellen. Durch die Aufteilung der einzelnen IT Ressourcen können diese dynamisch und an den Bedarf angepasst, angeboten werden.

Vereinfach kann man sich die Cloud wie folgt vorstellen: Man besitzt ein Online-Kleidergeschäft, mit zwei Mitarbeitern. Diese Mitarbeiter pflegen die Seite, verpacken und versenden die Ware. Während dem Jahr können die zwei Mitarbeiter alle Kunden jederzeit bedienen und es kommt zu keinen Engpässen. Über die Weihnachtszeit ist der Andrang aber so hoch, dass Kunden ihre Kleidung nicht rechtzeitig erhalten, da dass verpacken viel zu lange dauert. <br />
Nun gibt es für den Besitzer drei Möglichkeiten. Er stellt einen weiteren Mitarbeiter ein, den er aber ein ganzes Jahr beschäftigen müsste und zum Teil nicht ausgelastet ist. Die zweite Möglichkeit wäre, dass der Besitzer auf den Mehrumsatz verzichtet. Oder der Besitzer wendet sich für diese Zeit an einen Dienstleister der das verpacken und versenden für Ihn übernimmt.

Aus der Sicht der Informatik, hat der Besitzer einen Online-Shop, dieser läuft auf einem Server. Für die üblichen Benutzerzahlen im Jahr ist dieser Server völlig ausreichend, jedoch steigt die Zugriffszahlen über die Weihnachtszeit. Statt einen weiteren Server zu kaufen, der jährlich Geld kostet, mietet sich der Besitzer für eine geringe Zeitspanne weitere Rechnerressourcen in der Cloud.

<div class="figure" id="cloud-computing-diagram">
	<img src="http://up.frubar.net/1758/cloud_computing_diagram.jpg" alt="Cloud Computing Diagram" width="80%" />
	<p>Elemente des Cloud-Computing</p>
</div>

### Technische Realisierungen

Cloud-Computing wird in drei technische Schichten, in einen so genannten Cloud-Stack, aufgeteilt. Jeder Schicht stellt einen Grad der Abstraktion dar und werden in diesem Abschnitt näher erläutert. <a href="#bartonb08"><cite>bartonb08</cite></a>

<div class="figure" id="cloud-technische-realisierungen">
	<img src="http://up.frubar.net/1776/cloud-services-zielgruppen.svg" alt="cloud-technische-realisierungen" width="100%" />
	<p>Cloud-Stack, die drei technischen Schichten</p>
</div>

#### Infrastruktur (IaaS)

„Infrastructure as a Service“ befindet sich an der untersten Schicht im Cloud-Stack. Die Cloud-Provider bieten dem Benutzer Rechnerinstanzen, meist in Form von virtuellen Servern, an. Diese kann der Benutzer selbst verwalten. Der Cloud-Dienst ist skalierbar ausgelegt, jedoch nicht zwingend die Programme die der Benutzer auf den Rechnerinstanzen installiert. 

Je nach Anforderung kann der Cloud-Dienst um Rechnerinstanzen erweitert oder verkleinert werden. Der Benutzer ist hierbei ab der Betriebssystemebene für seine Instanz verantwortlich.

#### Plattform (PaaS)

Bei „Platform as a Service“ steht die Anwendung des Entwicklers im Vordergrund. Der Entwickler stellt seine Anwendung über die Cloud zur Verfügung. Die Cloud selbst kümmert sich um die Aufteilung auf die Rechnungsinstanzen.

Da der Entwickler nur seine Anwendung liefert, kann die Cloud die Anzahl der tatsächlichen Instanzen jederzeit erhöhen oder reduzieren. In der Cloud werden vom Entwickler gelieferte Daten verarbeitet, das umliegende System ist für ihn nicht einsehbar.

#### Anwendung (SaaS)

Der Benutzer verwendet bei „Software as a Service“ eine bereits bestehende Anwendung in der Cloud. Für ihn sind die Platform und die Infrastruktur nicht sichtbar. 

Beispiele für Cloud-Anwendung sind unter anderem Google Drive<span class="fn"><a href="http://drive.google.com">Google Drive</a></span>, DropBox<span class="fn"><a href="http://www.dropbox.com">DropBox</a></span> und Microsoft Office Communications Online<span class="fn"><a href="http://www.microsoft.com/online/de-de/prodComm.aspx">Microsoft Office Communications Online</a></span>.

### Organisatorische Arten

Die Cloud wird meist, abhängig vom Anwendungsfall, in drei Organisationsformen eingeordnet. Eine Beschreibung der Organisationsformen erfolgt in diesem Abschnitt. <cite><a href="#cloudadop10">cloudadop10</a></cite>

#### Private Cloud

Die Anbieter und Nutzer der „Private Cloud“ stammen aus der selben Organisation oder dem selben Unternehmen. Daten innerhalb dieser Cloud sind nur der Organisation zugänglich und nicht außerhalb erreichbar, dies bietet einen großen Sicherheitsaspekt.

#### Public Cloud

Die „Public Cloud“ ist nicht für eine Organisation beschränkt, sie ist öffentlich erreichbar und jeden zugänglich. Eine wichtige Rolle spielt hierbei die Datensicherheit. Jeder Benutzer muss hierbei selbst Entscheiden welche und wie viele Daten er in der Cloud speichert.

#### Hybrid Cloud

Hierbei handelt es sich um eine Mischung aus „Private und Public Cloud“. Eine Organisation verwendet eine „Private Cloud“ und wechselt im Fehlerfall oder bei hoher Belastung zur „Public Cloud“. 

##  Virtualisierung

Für die Virtualisierung gibt es viele verschiedene Methoden, abhängig davon eine Anwendung oder ein gesamtes Betriebssystem virtualisiert werden soll. Die Virtualisierung spielt eine wichtige Rolle für die Cloud Infrastruktur. Für die Bachelorarbeit ist die Bereitstellung ganzer Rechnerinstanzen relevant. Die beste Leistung wird mit der Paravirtualisierung erreicht. <cite><a href="#yaovt10">yaovt10</a></cite> <cite><a href="#yaocpu10">yaocpu10</a></cite> <cite><a href="#yaodisk10">yaodisk10</a></cite>


### Hardware Virtualisierung

Die virtuelle Maschine stellt dem Gastbetriebssystem Teilbereiche der Hardware in Form von virtueller Hardware zur Verfügung. Somit kann ein unverändertes Betriebssystem darauf in einer isolierten Umgebung laufen. Das Gastsystem muss hierbei für den gleichen CPU-Typ ausgelegt sein.

### Paravirtualisierung

Bei Paravirtualisierung wird zwar ein Betriebssystem virtuell gestartet, jedoch wird keine Hardware virtualisiert, sondern die Betriebssysteme verwenden eine abstrakte Verwaltungsschicht, um auf gemeinsame Ressourcen, wie Netzanbindung oder Festplattenspeicher, zuzugreifen. Damit das Betriebssystem auf der virtuellen Maschine ausgeführt werden kann muss es teilweise portiert werden. Durch diese Portierung kann sich die Leistung der virtuellen Maschine erhöhen. <cite><a href="#degelas08">degelas08</a></cite>

### Schnittstelle zur Virtualisierung

Durch die verschiedenen Virtualisierungstechnologien und Verfahren ist es schwierig für den Entwickler, eine Anwendung zu entwerfen, die mit allen Schnittstellen umgehen kann. Libvirt bietet eine einheitliche Schnittstelle (API) um verschiedene Technologien wie Linux KVM<span class="fn"><a href="http://www.linux-kvm.org">Linux KVM</a></span>, Xen<span class="fn"><a href="http://www.xen.org">Xen</a></span> und VMware ESX<span class="fn"><a href="http://www.vmware.com">VMWare ESX</a></span> zu verwalten.

<div class="figure" id="libvirt-schnittstelle">
	<img src="http://up.frubar.net/1757/libvirtd.svg" alt="libvirt Schnittstelle" width="80%" />
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
	<li>**Effektivität**<br />Das System sollte leicht zu erlernen sein, damit der Benutzer möglichst schnell seine Arbeit erledigen kann.</li>
	<li>**Effizienz**<br />Das System sollte effizient genutzt werden können, damit der Benutzer produktiv damit arbeiten kann, nachdem er es erlernt hat.</li>
	<li>**Einprägsamkeit**<br />Das System sollte sich dem Benutzer leicht einprägen, damit er auch nach einer längeren Pause, in der der Benutzer das System nicht verwendet hat, es wieder verwenden kann ohne es neu lernen zu müssen.
	<li>**Fehler**<br />Das System sollte wenige Fehler vom Benutzer zulassen, Fehler sollten sich leicht beheben lassen und schwerwiegende Fehler sollten gar nicht erscheinen.
	<li>**Zufriedenheit**<br />Das System sollte angenehm bei der Verwendung sein, damit der Benutzer mit dem System zufrieden ist und es mag.</li>
</ul>

In dieser Arbeit bezieht sich der Begriff Usability nur auf die Gebrauchstauglichkeit von mobilen Anwendungen, nicht auf die Usability des Gerätes oder anderer Software.

In diesem Abschnitt werden die bekanntesten Usability Regeln aufgeführt und die Relevanz für mobile Anwendungen dargestellt. Die eigentliche Anwendung der Regeln und Usability Konzepte erfolgt in Kapitel <a href="#analyse"><b>3. Analyse</b></a>.

### Usability-Regeln

Die große Anzahl an verschiedensten Usability-Regeln erschwert es die relevanten Regeln zu erkennen. Einige der seit Jahren anerkannten Regeln werden kurz erklärt und bewertet.

#### Handlungsschritte nach Norman

Schon 1988 veröffentlichte Donald Norman sein Buch „The Design of Everyday Things“ <cite><a href="#norman88">norman88</a></cite> welches sieben Handlungsschritte zum Erreichen eines Ziels beschreibt.

<div class="figure" id="sieben-handlungss-norman">
	<img src="http://up.frubar.net/1762/sieben-handlungss-norman.svg" alt="Die sieben Handlungsschritte von Norman" width="70%" />
	<p>Die sieben Handlungsschritte von Norman <cite><a href="dah06">dahm06</a></cite></p>
</div>

Aus den Handlungsschritten lassen sich zwei Handlungsphasen ableiten, die auftreten, wenn es für den Benutzer zu Problemen kommt das Ziel zu erreichen:
<ul>
	<li>Der **Gulf of Execution** beinhaltet Probleme, die während der Formulierung, Planung oder Ausführung auftreten. Diese treten auf, wenn der Benutzer nicht weiß, wie er zu der Lösung seines Problems kommt. Zu diesen Problemen gehört ein unverständliches Bedienkonzept oder eine mangelhafte Navigation.</li>
	<li>Der **Gulf of Evaluation** stellt die Probleme zwischen Anzeige und Interpretation dar. Diese entsteht durch Fehlinterpretation, mangelhafte Darstellung oder Rückmeldung.</li>
</ul>

Die sieben Handlungsschritte nach Norman sind durchaus wichtig für die Entwicklung einer mobilen Anwendung. So ist zu beachten das der Benutzer stets eine Rückmeldung auf seine Aktion erhält. Ebenso soll ein, in sich stimmiges, Bedienkonzept existieren, da sonst die Unzufriedenheit des Benutzers erhöht wird. Im schlimmsten Fall würde der Benutzer die Anwendung nicht mehr verwenden.

#### Usability-Heuristik von Nielsen

Der Software-Ergonom Jakob Nielsen verfasste 1990 unter dem Titel „Improving a Human-Computer Dialogue“ zehn Prinzipen, welche als Kategorien für die Usability-Probleme dienten. Heutzutage findet diese Heuristik Anwendung in der Gestaltung von neuen Benutzerschnittstellen. <cite><a href="#nie93">nie93</a></cite> <cite><a href="#niemo90">niemo90</a></cite> 

<ul>
	<li><strong>Einfache und natürliche Dialoge</strong><br />Dialoge sollen nur die nötigsten Informationen beinhalten. Alle weiteren Informationen, die nicht relevant sind, verringern die Wichtigkeit der nötigen Informationen. Die Darstellung soll natürlich und logisch sein.</li>
	<li><strong>Ausdrucksweisen des Anwenders</strong><br />Die Dialoge sollen in einer, dem Benutzer vertrauten, Sprache geschrieben sein. Fachausdrücke sollten, falls möglich, vermieden werden.</li>
	<li><strong>Minimale mentale Belastung des Benutzers</strong><br />Der Benutzer soll sich keine Informationen über mehrere Dialoge hinweg merken müssen.</li>
	<li><strong>Konsistenz</strong><br />Die Dialoge sollen immer auf die gleiche Art und Weise dargestellt werden. Der Benutzer soll sich während der Verwendung nicht umgewöhnen müssen.</li>
	<li><strong>Rückmeldung</strong><br />Die Anwendung sollte dem Benutzer immer, in einer vernünftigen Zeit, informatives Feedback liefern. Siehe auch <a href="#handlungsschritte-nach-norman">Handlungsschritte nach Norman</a>.</li>
	<li><strong>Kontrolle über die Funktionen</strong><br />Sollte der Benutzer eine falsche Funktion ausgeführt haben, muss er diesen Vorgang jederzeit abbrechen oder einen Schritt zurückgehen können.</li>
	<li><strong>Abkürzungen</strong><br />Das System soll dem erfahrenen Benutzer Abkürzungen, z.B. durch Tastenkürzel oder Funktionstasten, bieten können. Somit ist gewährleistet, dass erfahrene und unerfahrene Benutzer das System effizient nutzen können.</li>
	<li><strong>Gute Fehlermeldungen</strong><br />Eine Fehlermeldung soll nie den Benutzer kritisieren, sie sollte defensiv, präzise und konstruktiv sein.</li>
	<li><strong>Fehlervermeidung</strong><br />Fehler sollten durch das Design und die Benutzereingabe weitestgehend vermieden werden.</li>
	<li><strong>Hilfe und Dokumentation</strong><br />Auch wenn das System ohne Hilfe und Dokumentation benutzbar ist, sollte eine Dokumentation und Hilfe immer zur Verfügung stehen.</li>
</ul>

Wie für jede Gestaltung von neuen Benutzerschnittstellen bieten die Usability-Heuristik von Nielsen auch eine gute Grundlage für die Entwicklung und das Design einer mobilen Anwendung.

#### KISS - Keep it Simple and Straightforward

Bei dem KISS-Prinzip soll immer eine einfache Lösung für das Problem gewählt werden. Dabei ist KISS ein Akronym, welches auch unter „Keep It Simple and Stupid“ oder „Keep It Short and Simple“ bekannt ist.

<div class="figure" id="kiss-iphone">
	<img src="http://up.frubar.net/1779/kiss-iphone.png" alt="kiss-iphone" width="50%" />
	<p>KISS Prinzip anhand einer iPhone Anwendung <cite><a href="#tapworthy11">tapworthy11</a></cite></p>
</div>

Abgeleitet auf die mobile Anwendung bedeutet dies, dass die Benutzerinteraktion und Oberfläche so einfach wie möglich gestaltet werden muss, um das Ziel zu erreichen. Ein Auswahlmenü sollte somit nicht 20 Funktionen anzeigen, sondern nur diese die er zur Lösung seiner Aufgabe benötigt.

### Relevanz für mobile Anwendungen

Durch die Besonderheit des mobilen Geräts gegenüber herkömmlichen Computern müssen spezielle Usability-Regeln bei der Entwicklung beachtet werden. So bietet ein kleinerer Bildschirm und Touchscreen andere Eingabemöglichkeiten für den Benutzer. Die Umgebung in welcher die Anwendung eingesetzt wird spielt auch eine tragende Rolle für die Usability.

#### Umgebung

Es sollte immer bedacht werden, dass eine mobile Anwendung gerade Unterwegs zum Einsatz kommt. iPhones werden meist mit einer Hand verwendet und es wird nur mit einem kurzen Blick auf den Bildschirm geschaut. Wie die Abbildung 4 zeigt, ist eine Anwendung überladen und werden zu viele Informationen dargestellt kann ein Benutzer diese nicht aufnehmen.

<div class="figure" id="iphone-umgebung">
	<img src="http://up.frubar.net/1753/iphone-umgebung.png" alt="iPhone Umgebung" width="70%" />
	<p>iPhone Anwendung, Nutzung Unterwegs <cite><a href="#tapworthy11">tapworthy11</a></cite></p>
</div>

Durch die unterschiedlichen Lichtverhältnisse in der Umgebung muss auf ein starkes Kontrastverhältnis geachtet werden. Die Anwendung kannst sonst bei starken Spiegelungen oder Lichteinfall nicht erkennbar sein.

#### Bildschirmgröße

Der Bildschirm bei einem iPhone oder einem anderen Smartphone ist deutlich kleiner gegenüber einem Computer. Es ist daher kein Platz für unnötige Informationen die den Benutzer auf dem aktuellen Bildschirm nur irritieren könnten.

Durch den kleineren Bildschirm können weniger Informationen auf einem Ausschnitt platziert werden, dadurch muss mit einer guten Navigation gearbeitet werden. Diese sollte nicht zu Tief in „verwinkelt“ sondern für den Benutzer intuitiv nutzbar sein.

#### Touchscreen

Da ein Touchscreen meist mit den Fingern und nicht mit der Maus bedient wird, sind einige Designaspekte zu beachten. 

Die Finger oder der Handrücken überdecken, wie Abbildung 5 zeigt, bei der Navigation zum Teil die Anwendung. Die Hauptnavigation innerhalb einer Anwendung sollte daher am unteren linken Rand des Bildschirms angezeigt werden.

<div class="figure" id="iphone-daumen">
	<img src="http://up.frubar.net/1754/iphone-daumen.png" alt="iPhone Daumen" width="30%" />
	<p>Der Daumen bedeckt einen Großteil des Bildschirms <cite><a href="#tapworthy11">tapworthy11</a></cite></p>
</div>

Mit der vollwertigen QWERTZ-Tastatur, gegenüber der T9-Tastatur, ist es zwar einfacher Eingaben vorzunehmen aber es ist dennoch mühsam. Für den Benutzer sollte man daher die Eingaben so gering wie möglich halten.



# Einleitung
## Projektträger

Der Auftraggeber und Träger dieses Projekts ist die IT Abteilung der Avira Operations GmbH & Co. KG<span class="fn"><a href="http://www.avira.com">Avira Operations GmbH & Co. KG</a></span>. (im Folgenden Avira genannt). Die IT Abteilung versteht sich als serviceorientierter Dienstleister für Avira, der Kunde und die Verfügbarkeit der Dienste liegen somit im Mittelpunkt.

Die Avira ist mit rund 100 Millionen Kunden und 500 Mitarbeitern ein weltweit führender Anbieter selbst entwickelter Sicherheitslösungen für den kommerziellen und privaten Einsatz. Das Unternehmen gehört mit mehr als 25-jähriger Erfahrung zu den Pionieren in diesem Bereich.

Als führender deutscher Sicherheitsspezialist verfügt Avira über fundierte Erfahrung im Entwickeln und Unterstützung ihrer Lösungen. Neben Programmen direkt für den Einzelplatzbetrieb bietet sie, hauptsächlich professionelle, Lösungen für systemübergreifenden Schutz von Netzwerken auf verschiedenen Ebenen an. Hierzu zählen unter anderem Produkte für Workstations, File-, Mail- und Web-Server. Auch Gateway-Rechner können, wie Arbeitsplatzrechner, über eine zentrale Verwaltungskonsole betriebssystemübergreifend verwaltet werden. Zu den Verwaltungsprodukten der einzelnen Lösungen kommen noch Sicherheitsprogramme für PDAs, Smartphones und Embedded Devices hinzu. Ein signifikanter Sicherheitsbeitrag ist Avira AntiVir Personal, das millionenfach bei Privatanwendern im Einsatz ist.

Avira ist in Tettnang am Bodensee einer der größten regionalen Arbeitgeber. Sie unterhält mehrere Unternehmensstandorte in Deutschland und pflegt Partnerschaften in Europa, Asien und Amerika. Mehrere Dutzend Virus-Researcher in verteilten Virenlabors kümmern sich, rund um die Uhr, um die lokalen und globalen Bedrohungen der Virenfront. Bestätigt wird diese Arbeit etwa durch mehrfache Testauszeichnungen mit dem VB 100% des Virus Bulletin<span class="fn"><a href="http://www.virusbtn.com">Virus Bulletin</a></span> oder der wiederholten TÜV-Zertifizierung.

Zu den nationalen und internationalen Kunden zählen namhafte, börsennotierte Unternehmen aber auch Bildungseinrichtungen und öffentliche Auftraggeber. Neben dem Schutz der virtuellen Umgebung kümmert sich Avira, durch Fördern der Auerbach Stiftung<span class="fn"><a href="http://www.auerbach-stiftung.de">Auerbach Stiftung</a></span>, um mehr Schutz und Sicherheit in der realen Welt.

## Motivation

„Alles muss in die Cloud“, wie oft liest man dies in IT Magazinen oder hört die Aussage von Managern? Doch diese Infrastruktur muss auch gepflegt und administriert werden. Gerade im Notfall müssen IT Mitarbeiter, auch von unterwegs, schnell Probleme beheben. Eine Bereitschaft der IT Administratoren von 24 Stunden, 7 Tage die Woche können sich viele kleine Firmen nicht leisten und setzen auf das Engagement der Mitarbeiter. Einige der Probleme könnten bequem per Smartphone gelöst werden.

Der Marktanteil für Smartphones mit Google Android oder Apple iOS<span class="fn"><a href="http://developer.apple.com/library/ios/documentation/Miscellaneous/Conceptual/iPhoneOSTechOverview/iPhoneOSTechOverview.pdf">iOS Technology Overview</a></span> steigt jedes Jahr um mehrere Prozent. So sind diese Betriebssysteme schon auf mehr als 50% der Geräte im Umlauf.<span class="fn"><a href="http://www.gartner.com/it/page.jsp?id=1622614">Marktanteile laut Gartner Inc. (April 2011)</a></span>

Durch den immer weiter steigenden Verkauf von Smartphones wächst auch die Verwendung mobiler Anwendungen. Diese Anwendungen haben jedoch völlig andere Anforderungen als Programme für Desktop Computer oder Laptops. Herausstechendstes Merkmal ist der kleinere Bildschirm sowie die Bedienung mittels Touchscreen, hierauf muss beim Aufbau der Benutzeroberfläche besonders geachtet werden.

## Problemstellung

<q>Als Admin eines Online-Shops fahre ich mit meinem Sportwagen Richtung Süden. Dank meines iPhone bemerke ich, dass meine Internetseite auf Facebook angekündigt wird. Durch die vielen Zugriffe auf den Webserver wäre meine Seite nicht mehr erreichbar und ich würde Umsatz verlieren.</q>

<div style="text-align: right; margin-right: 2em; margin-top: -2em;">
    User-Story eines IT Mitarbeiters
</div>

Jeder IT Mitarbeiter der Avira besitzt ein iPhone und soll, falls möglich, schnell auf Probleme reagieren können. Da viele Dienste auf virtuellen Servern in der Cloud Infrastruktur zur Verfügung stehen, müssen diese schnell und einfach verwaltet werden können.

Erfahrungen der Mitarbeiter zeigen, dass nicht die Dienste selbst das Problem sind, sondern oftmals eine Störung am virtuellen Server vorliegt. So muss, unter anderem, bei hoher Last des Servers mehr Arbeitsspeicher oder mehrere CPUs hinzugeschaltet werden. Da ein Smartphone leichter zu transportieren ist als ein Notebook, bietet sich eine mobile Anwendung für die Steuerung der Cloud Systeme an.

Zum aktuellen Zeitpunkt steht noch keine mobile Anwendung zur Verfügung, welche die Verwaltung der Server ermöglicht.

## Zielsetzung

Durch dieses Projekt soll ein Konzept für eine iOS Anwendung erstellt werden, mit der die Möglichkeit besteht virtuelle Server innerhalb einer Cloud Infrastruktur zu steuern. Die Zielgruppe für die Anwendung sind IT Mitarbeiter und Administratoren. Die Anwendung kommt häufig im Problemfall zum Einsatz, somit ist auf eine einfache und intuitive Bedienung zu achten. Bei der Anwendung steht die Benutzerfreundlichkeit im Vordergrund.

Als Schnittstelle zwischen iOS Anwendung und den virtuellen Servern soll libvirt<span class="fn"><a href="http://www.libvirt.org">libvirt</a></span>, eine API zur Verwaltung von verschiedenen Virtualisierungstechnologien, zum Einsatz kommen.

## Abgrenzung

In der Bachelor-Thesis wird keine vollwertige iOS Anwendung entwickelt. Durch ein Konzept und die Erstellung eines Prototyps soll ein gutes Gleichgewicht zwischen Benutzerfreundlichkeit und Anwendungsumfang erreicht werden.

## Zielgruppe der Thesis

Die Leserzielgruppe der Arbeit umfasst Entwickler von mobilen Anwendungen für iPhone Geräte sowie technisch versierte Systemadministratoren. Bei der Entwicklung der Anwendung werden Usability-Regeln und Design berücksichtigt, daher ist die Thesis auch für Usability-Forscher interessant.

## Struktur und Aufbau der Arbeit

Die Bachelorarbeit ist in vier Teilbereiche gegliedert. Sie spiegelt dadurch den ungefähren Verlauf des Projekts wieder.

In der <a href="#einleitung"><i>Einleitung</i> wird der Projektträger vorgestellt und die Ziele des Projekts beschrieben. Die für die Arbeit relevanten Begriffe werden in den <a href="#grundlagen"><i>Grundlagen</i> erklärt. Es erfolgt eine Vorstellung des verwendeten Mobilen Endgeräts und der Cloud Schnittstelle. Außerdem werden die Kriterien für die Usability-Tests beschrieben.

In den Kapiteln <a href="#analyse"><i>Analyse</i></a> und <a href="#konzeption"><i>Konzeption</i></a> erfolgt eine Darstellung der aktuellen Situation. Ein erster Prototyp wird erstellt und beschrieben um Usability-Tests anwenden zu können. Anschließend wird die Zielgruppe zum Prototypen befragt. In der <a href="#realisierung"><i>Realisierung</i></a> werden die technischen Aspekte zur Entwicklung der Anwendung angesprochen. Es werden Quelltexte zur grafischen Benutzeroberfläche und Schnittstellen näher erläutert.

Den Abschluss der Thesis bildet das <a href="#fazit"><i>Fazit</i></a> über das gesamte Projekt und die Arbeit. Es folgt ein Ausblick auf den Verlauf des Projekts außerhalb der Bachelor-Thesis.

## Formale Hinweise

Unbekannte Begriffe oder weitere Hinweise zu einem Wort werden per Fußnote erklärt. Meist erfolgt ein weiterführender Link zu einer Internetseite. Zitate oder Quellenverweise sind per Eckiger-Klammer gekennzeichnet und im Quellenverzeichnis beschrieben. Verweise auf Kapitel oder wichtige Textstellen sind <i>kursiv</i> geschrieben.
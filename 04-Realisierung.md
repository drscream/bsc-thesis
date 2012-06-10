# Realisierung

<q>Let us think the unthinkable, let us do the undoable, let us prepare to grapple <br />with the ineffable itself, and see if we may not eff it after all.</q>
<div style="text-align: right; margin-right: 2em; margin-top: -2em;">
    Douglas Adams
</div>

In diesem Kapitel werden technische Details zur Realisierung erklärt und einige Quelltext und API Beispiele aufgeführt. Ein weiterer Abschnitt beschreibt die Entwicklungsarbeit an Prototypen.

## libvirt Schnittstelle

Wie in Kapitel 2.3 beschrieben handelt es sich bei libvirt um eine Schnittstelle zwischen Anwendungen und verschiedenen Virtualisierungstechnologien. Bei libvirt handelt es sich um eine C-Bibliothek, auf diese kann aber durch eine weitere Abstraktionsschichten auch mit anderen Programmiersprachen<span class="fn"><a href="http://libvirt.org/bindings.html">libvirt Bibliothek und weitere Programmiersprachen</a></span> zugegriffen werden. Dadurch werden Programmiersprachen wie Python, Perl, Ruby, Java und PHP unterstützt.

<div class="figure" id="build-api-interfaces">
	<img src="http://up.frubar.net/1824/build-api-interfaces.svg" alt="build-api-interfaces" width="80%" />
	<p>Schnittstellenaufbau mit Node.js und libvirt</p>
</div>

Der Softwareentwickler Camilo Aguilar<span class="fn"><a href="http://github.com/c4milo">GitHub Profil von Camilo Aguilar</a></span> hat eine weitere Bibliothek<span class="fn"><a href="http://github.com/c4milo/node-libvirt">libvirt-node.js Bibliothek</a></span> für libvirt und Node.js entwickelt. Dieses bietet für Node.js viele Schnittstellenimplementationen von libvirt an und kommt für den Prototyp zum Einsatz.

### Node.js

Bei Node.js handelt es sich um ein JavaScript Framework zur Erstellung von Server- und Konsolenanwendungen. Der JavaScript Quelltext wird mit der JavaScript-Engine V8<span class="fn"><a href="http://code.google.com/p/v8/">JavaScript-Engine V8</a></span> von Google in Maschinencode übersetzt und ausgeführt.

Durch die von Camilo Aguilar entwickelte Bibliothek ist es möglich direkt über die Programmiersprache JavaScript mit Node.js auf libvirt zuzugreifen. 

<div class="listing" id="node-js-example">
	<code><pre>var hypervisor = new Hypervisor(conf.uri);
var domain;
	
app.get('/domain/:uuid', function(req, res) {
	domain = hypervisor.lookupDomainByUUID(req.params.uuid);
	domainInfo = domain.getInfo();
	domainInfo.name = domain.getName();
	
	if (domainInfo != null)
		res.send(domainInfo);
});</pre></code>
	<p>Quelltext Auszug der REST Node.js Schnittstelle</p>
</div>

Mit dem Node.js Web-Framework express<span class="fn"><a href="http://expressjs.com/">Node.js Web-Framework express</a></span> kann mir wenigen Codezeilen eine REST (Representational State Transfer) API<span class="fn"><a href="http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm">Dissertation von Roy Fielding, zu REST</a></span> entwickelt werden. REST vereinfacht die Schnittstelle zwischen Systemen auf eine standardisierte Menge an Aktionen. Für die Umsetzung wird in diesem Fall das HTTP-Protokoll verwendet.

<div class="listing" id="url-example">
	<code><pre>http://example.com/domain/b84f1d60-cbc4-4cff-704e-96fc768f0922</pre></code>	
	<p>Beispiel URL</p>
</div>

Wie im Quelltext Auszug zu erkennen ist wird die HTTP-Funktion GET aufgerufen, dieser wird die eindeutige ID (UUID) der virtuellen Maschine übergeben. Über die libvirt-Funktionen werden zusätzliche Informationen abgefragt und an den Benutzer zurückgeliefert. Die Rückgabe erfolgt in JSON<span class="fn"><a href="http://json.org/">JSON</a></span>, einer JavaScript-Objekt Notation.

### JSON

Bei JSON handelt es sich um eine JavaScript-Objekt Notation, die zum kompakten Datenaustausch zwischen Anwendungen dient. Ein großer Vorteil ist die kompakte aber dennoch für den Menschen lesbare Struktur. Jedes JSON-Dokument ist auch ein gültiges JavaScript und kann daher von dieses Programmiersprache einfach interpretiert werden. Es existieren aber auch Parser für andere Programmiersprachen.

<div class="listing" id="return-example">
	<code><pre>{
	"state":1,
	"max_memory":524288,
	"memory":524288,
	"vcpus_number":1,
	"cpu_time":3434280000000,
	"name":"example"
}</pre></code>	
	<p>Beispiel Rückgabeinformationen</p>
</div>

Alle Daten die über die REST Node.js API angefragt werden, sollen als JSON zurückgeliefert werden. Der Prototyp für die iPhone Anwendung muss somit JSON interpretieren und anzeigen.

## Prototyp

Das Ziel eines Prototyps ist in erster Linie einen Teil der Funktionsfähigkeit der Anwendung dem Benutzer bereitzustellen. Da der Fokus auf der Benutzerfreundlichkeit liegt, wurde ein erster Prototyp ohne Verbindung zur API entworfen. Die angezeigten Daten sind daher fest im Programm verankert. Die erste Erstellung des Prototyps erfolgte nach Fertigstellung des Story-Boards. 

In diesem Abschnitt erfolgt eine Beschreibung zur Realisierung der verschiedenen Prototypen.

### Mock-up

Nach der Konzeptionsphase durch das Story-Board wird ein erstes Mock-up mit der Anwendung Balsamiq Mockups<span class="fn"><a href="http://www.balsamiq.com/products/mockups">Balsamiq Mockups</a></span> erstellt. Dies soll dem Benutzer einen ersten Eindruck der Cloud Control „Apps“ vermitteln.
	
<div class="figure" id="mockup">
	<img src="http://up.frubar.net/1825/mockup-cloud-control.png" alt="mockup" width="80%" />
	<p>Erstes Mock-up von Cloud Control</p>
</div>

Balsamiq Mockups bietet zwar viele gestalterische Möglichkeiten eine iPhone Anwendung darzustellen, jedoch ist es für den Benutzer nicht einfach sich dies vorzustellen. 

### XCode und PhoneGap

Die Entwicklung einer iPhone Anwendung erfolgt mit XCode und in der Programmiersprache Objective-C<span class="fn"><a href="http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/ObjectiveC/Introduction/introObjectiveC.html">Objective-C</a></span>. Bei XCode handelt es sich um die Entwicklungsumgebung von Apple und bietet auch Simulatoren für iPhone oder iPad an. Bei Objective-C handelt es sich um eine Erweiterung der Programmiersprache C um Sprachmittel zur objektorientierten Programmierung.




# CODEBUCH Datensatz Filmmusik
Stand: 2.10.26 (Blocktag 2)
Erstellt von: Sarah Tepel

## Inhalt des Codebuchs
- Ursprung und Datenerhebung
- Nodes.csv (Nodelist)
- Edges.csv (Edgelist)


## Ursprung und Datenerhebung
Die Daten wurden von der Gruppe Filmmusik im Sommer 2026 erhoben. Die Datenerhebung wurde im Oktober 2026 fertiggestellt.
Das Netzwerk ist ein ungerichtetes multimode-mode Netzwerk mit Akteuren als Personen und Filmstudios.


## Die NODE-Attribute

**id** 
Die ID ist die eindeutige Identifikation jedes Knotens.
Die IDs der Nodelist stimmen komplett mit den IDs der Edgelist überein.
Ids werden mithilfe der ersten zwei Buchstaben von Vor-und Nachnamen (oder Teilnamen) eines Knotens + mit der richtigen Typisierungskategorie erstellt.

Die vier Knoten-Kategorien sind:

100 = film
200 = director
300 = composer
400 = studio

Beispiel ID: stsp200 für Steven Spielberg

**name**
Ausgeschriebener Name des Knotens, bei Personen Vor- und Nachname, bei Studios vollständiger Name usw.

**type**
Definiert den Typ des Knotens: es gibt die Typen film, director oder composer (werden auch durch die ID gekennzeichnet)

**oscar**
Steht für gewonnene Oscars eines Films (nicht von Personen): entweder yes oder no

**oscar_nom**
Steht für Oscarnominierungen (ausschließlich von Filmen und nicht von Personen): entweder yes oder no

**imdb_rating**
IMDB ist eine Plattform, 
Rating von 1-10 Sternen, unterschiedliche Gewichtung der Stimmgaben

**year**
Erscheinungsjahr des Films.

**genre**
Das Film-Genre zB.: Thriller, Horror, Drama etc. Sind bei imdb mehrere Genres einem Film zugeordnet zählt nur das Erstgenannte

**studio**
Name des Produktionsstudios hinter dem jeweiligen Film zB.: 20th Century Fox, Universial oder Columbia

**sex**
m = male
f = female
d = diverse

**nationality**
Nationalität von composer oder director zB.: USA, Germany, bei 2 Nationalitäten wird der Geburtstort der Person nehmen

**birthyear**
Geburtsjahr von composer oder director zB.: 1975 oder 1940

**99 oder auch NA**
Definiert fehlende Werte bei der Datenerhebung, zB bei sex oder birthyear eines Films. 
Leere Zellen in der Daten-Tabelle in github werden durch RStudio mit NA (not available) gelabelt.
  
  

## Die EDGE-Attribute

**id**
Identische ID wie aus der Nodelist zur Identifikation der Knoten.


**from (mit ID)**
Verbindung von einem Knoten zu einem anderen.

**to ,zu ID**
Verbindung von einem Knoten zu einem anderen.

**relationship**
Es gibt verschiedene Beziehungsarten zwischen zwei Knoten, die relationship genannt werden.
1 = zwischen film und director oder composer
2 = zwischen composer und director
3 = zwischen studio und film

**year**
Erscheinungsjahr des Films, wie in der Nodelist.

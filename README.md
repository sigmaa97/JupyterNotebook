# Dokumentation: Custom Index Structure and Multithreaded Transaction Handling Group 11 

## Klassenstruktur:

    1. BTree
    2. IXServer.java
    3. IdxState.java
    4. Key.java
    5. Node.java
    6. Record.java
    7. RecordComperator.java
    8. Server.java
    9. TxnState.java

### BTree 

Die Klasse BTree ist die Indexstruktur zur Speicherung von Records. 
Auf BTrees werden alle Datenbankzugriffe durchgeführt.

#### Konstruktorübersicht

Konstruktoren
Konstruktor
Beschreibung
BTree(Types.KeyType type, String name)
Konstruktormethode, um eine Instanz eines BTree zu erstellen

#### Methodenübersicht

Modifizierer und Typ
Methode
Beschreibung
boolean
deleteFromInner(Node node, Record record, int search)
Löscht einen Key aus einem inneren Knoten
boolean
deleteFromLeaf(Node node, Record record, int search)
Löscht ein Key aus einem Blattknoten
boolean
delRecord(Record record)
Löscht ein Key aus dem BTree
void
drop()
Der BTree löscht seine Daten, indem alle Felder auf null gesetzt werden
Node
findLeafPredecessor(Node current)
Sucht in einem Subtree den Node, wo das größte Element drin ist
Node
findLeafSuccessor(Node current)
Sucht in einem Subtree den Node, wo das kleinste Element drin ist
Record
get(Record record)
Gibt ein Record zurück, falls dieser im BTree gespeichert wurde.
Node
getLeftSibling(Node node)
Gibt den linken Nachbar von einem Node zurück
Node
getLeftSibling(Record record)
Gibt den linken Nachbar von einem Node, wo ein Record drin ist, zurück
Record
getNext(Record key)
GetNext ruft die Methode recursiveSearch mit den Startparametern auf.
Node
getParentNode(Record record)
Die Methode findet die Parentnode von einem Record key.
Node
getRightSibling(Node node)
Gibt den rechten Nachbar von einem Node zurück
Node
getRightSibling(Record record)
Gibt den rechten Nachbar von einem Node, wo ein Record drin ist, zurück
boolean
insertRecord(Key<?> k, String payload)
Fügt einen Schlüssel assoziiert mit einem Datenpaket in den BTree ein.
boolean
recursiveDelete(Node node, Record record)
Sucht rekursiv nach einem Node, wo der Key drin ist, den man löschen möchte und ruft dann die entsprechende Methode auf um den Key zu löschen
Record
recursiveSearch(Node current, Record key, Record bestNext)
Die Methode geht rekursiv durch den Baum.
void
resolveMergeUnderflow(Node parent)
Sucht nach einem Key, der in einer Node eingefügt wird, wo ein underflow ist

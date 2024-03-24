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

#### Methodenübersicht -und Details

##### -drop

public void drop()
Der BTree löscht seine Daten, indem alle Felder auf null gesetzt werden

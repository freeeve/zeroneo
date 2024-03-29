zeroneo
=======
Zeromq + neo4j proof of concept. A zeromq service on top of a Neo4j database, supporting cypher.

## Protocol/Messaging

#### connect, set connection variables

* authentication
* encryption options
* compression options
* batch size (number of result rows to return before waiting to be asked for more)

#### connect acknowledgement

* connection id (assigned by server)

#### requests

* connection id
* transaction id (assigned by client)
* request id (assigned by client)
* request size in bytes
* request itself (cypher or index command)

#### responses

* connection id
* transaction id
* request id
* response size in bytes
* response itself (rows of data)
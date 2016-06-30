Graphviz Flow Diagram
---
![Flow Diagram](http://g.gravizo.com/g?
  digraph A {
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf}
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
)

Graphviz Sequence Diagram
---
![Seqence Diagram](http://g.gravizo.com/g?
  	@startuml;
    actor User;
	participant "First Class" as A;
	participant "Second Class" as B;
	participant "Last Class" as C;
    User -> A: DoWork;
	activate A;
	A -> B: Create Request;
	activate B;
	B -> C: DoWork;
	activate C;
	C --> B: WorkDone;
	destroy C;
	B --> A: Request Created;
	deactivate B;
	A --> User: Done;
	deactivate A;
  	@enduml
)


Mermaid Diagram
---
```mermaid
graph TD;
  A-->B;
  A-->D;
  B-->C;
  D-->C;
```

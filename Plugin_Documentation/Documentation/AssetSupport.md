# Asset Support

## Blueprint

Supportato: si.

Livello: buono per dati generici graph/node/pin/link.

Dati esportati:

- classi
- parent class
- generated class
- compile status
- interfacce
- variabili dichiarate
- graph
- nodi
- pin
- link
- dipendenze asset registry
- relazioni verso altri asset supportati

Dati mancanti/parziali:

- `memberName`, `functionName`, `variableName`, `targetClass` sono campi presenti ma vuoti nell'export base.
- traversal flow exec completo non implementato.
- data dependency precisa non implementata.

## Widget Blueprint

Supportato: si, come `UBlueprint`.

Livello: parziale per UMG specifico.

Dati esportati:

- graph e nodi Blueprint.
- indici AI-readable.
- widget tree file generato nel pack.

Limitazioni:

- designer tree UMG non viene letto tramite API UMG dedicate.
- widget/components sono inferiti da nomi/nodi.
- delegate binding reale e solo parzialmente deducibile.

## Actor Blueprint

Supportato: si, come `UBlueprint`.

Livello: generico.

Mancante:

- Simple Construction Script/component hierarchy dettagliata.
- transform/collision/mesh componenti non estratti in modo strutturato reale.

## Component Blueprint

Supportato: si, come `UBlueprint`.

Livello: generico.

Mancante:

- informazioni specifiche di componente oltre a graph/nodi/pin.

## Animation Blueprint

Supportato: si, come `UBlueprint`.

Livello: generico.

Mancante:

- state machine, anim graph e transition rules non hanno schema dedicato.

## Data Table

Supportato: si.

Dati esportati:

- row struct
- columns
- rows
- campi
- valori strutturati
- value text
- dipendenze

## User Defined Struct

Supportato: si.

Dati esportati:

- status
- guid
- size
- fields
- type
- default
- metadata utile

## User Defined Enum

Supportato: si.

Dati esportati:

- index
- numeric value
- name
- authoredName
- displayName
- hidden

## Altri asset

Supportato: no.

Il filtro AssetRegistry include solo:

```text
UBlueprint
UDataTable
UUserDefinedStruct
UUserDefinedEnum
```


# BP_AmmoPickUp

Path: /Game/ChuckContent/Systems/Weapons/Blueprints/BP_AmmoPickUp.BP_AmmoPickUp
Class: Blueprint
Parent: /Script/Engine.Actor
Generated: 2026-07-10T21:13:02.714Z

## Variables
- As ALS Chuck BP: object|/Game/ChuckContent/Blueprints/ALS_ChuckBP.ALS_ChuckBP_C
- AmmoAmount: int
- AmmoType: byte|/Game/ChuckContent/Systems/Weapons/Data/E_AmmoType.E_AmmoType
- As ALS Player Controller: object|/Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_Player_Controller.ALS_Player_Controller_C
- DisplayName: text

## Graphs
- GetInteractionPrompt (EdGraph): 4 nodes, 3 edges
- EventGraph (EventGraph): 32 nodes, 38 edges
- CollectAmmo (Function): 21 nodes, 24 edges
- UserConstructionScript (Function): 1 nodes, 0 edges

## Important References
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/UI/WIDGET_MENU/01_HUD/WBP_HUD
- /Game/ChuckContent/Blueprints/S_InteractionPrompt
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_Player_Controller
- /Game/ChuckContent/Blueprints/BPI_Interaction
- /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType
- /Game/ChuckContent/UI/files/MI_Outline

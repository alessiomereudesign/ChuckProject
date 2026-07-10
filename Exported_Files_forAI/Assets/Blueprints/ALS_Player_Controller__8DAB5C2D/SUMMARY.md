# ALS_Player_Controller

Path: /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_Player_Controller.ALS_Player_Controller
Class: Blueprint
Parent: /Script/Engine.PlayerController
Generated: 2026-07-10T21:13:02.714Z

## Variables
- DebugFocusCharacter: object|/Script/Engine.Character
- AvailableDebugCharacters: object|/Script/Engine.Character|container=Array
- ShowHUD: bool
- DebugView: bool
- ShowTraces: bool
- ShowDebugShapes: bool
- ShowLayerColors: bool
- ShowCharacterInfo: bool
- OverlaySwitcher: object|/Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/UI/OverlayStateSwitcher.OverlayStateSwitcher_C
- OverlayMenuOpen: bool
- Slomo: bool
- CustomRadialMenuRef: object|/Game/ChuckContent/UI/WIDGET_MENU/2_MENU_RAPIDO/WBP_CustomRadialMenu.WBP_CustomRadialMenu_C
- Chuck_HUD: object|/Game/ChuckContent/UI/WIDGET_MENU/01_HUD/WBP_HUD.WBP_HUD_C
- GenericPromptRef: object|/Game/ChuckContent/Blueprints/WBP_GenericPrompt.WBP_GenericPrompt_C
- CurrentInputDevice: name
- InputKeyMap: name|container=Map|value=text

## Graphs
- BPI_Get_DebugInfo (EdGraph): 13 nodes, 12 edges
- EventGraph (EventGraph): 151 nodes, 147 edges
- GetKeyTextForInputAction (Function): 13 nodes, 14 edges
- IsActiveInputDevice (Function): 3 nodes, 3 edges
- UserConstructionScript (Function): 1 nodes, 0 edges

## Important References
- /Game/ChuckContent/Blueprints/WBP_GenericPrompt
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/Interfaces/ALS_Controller_BPI
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CameraSystem/ALS_PlayerCameraManager
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/Libraries/ALS_MacroLibrary
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/UI/WIDGET_MENU/01_HUD/WBP_HUD
- /Game/ChuckContent/Blueprints/S_InteractionPrompt
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_BaseCharacterBP
- /Game/AdditionalContents/AdvancedLocomotionV4/Audio/UI/Click
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/UI/OverlayStateSwitcher
- /Game/ChuckContent/UI/WIDGET_MENU/2_MENU_RAPIDO/WBP_CustomRadialMenu
- /Engine/EditorBlueprintResources/StandardMacros

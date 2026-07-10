# ALS_PlayerCameraManager

Path: /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CameraSystem/ALS_PlayerCameraManager.ALS_PlayerCameraManager
Class: Blueprint
Parent: /Script/Engine.PlayerCameraManager
Generated: 2026-07-10T21:13:02.714Z

## Variables
- ControlledPawn: object|/Script/Engine.Pawn
- DebugViewOffset: struct|/Script/CoreUObject.Vector
- DebugViewRotation: struct|/Script/CoreUObject.Rotator
- RootLocation: struct|/Script/CoreUObject.Vector
- SmoothedPivotTarget: struct|/Script/CoreUObject.Transform
- PivotLocation: struct|/Script/CoreUObject.Vector
- TargetCameraLocation: struct|/Script/CoreUObject.Vector
- TargetCameraRotation: struct|/Script/CoreUObject.Rotator

## Graphs
- EventGraph (EventGraph): 11 nodes, 11 edges
- BlueprintUpdateCamera (Function): 12 nodes, 16 edges
- CalculateAxisIndependentLag (Function): 17 nodes, 25 edges
- CustomCameraBehavior (Function): 126 nodes, 134 edges
- Get_CameraBehaviorParam (Function): 9 nodes, 8 edges
- GetDebugTraceType (Function): 6 nodes, 7 edges
- UserConstructionScript (Function): 1 nodes, 0 edges

## Important References
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CameraSystem/ALS_PlayerCameraBehavior
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/Interfaces/ALS_Controller_BPI
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CameraSystem/Camera
- /Engine/EditorBlueprintResources/StandardMacros
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/Interfaces/ALS_Camera_BPI

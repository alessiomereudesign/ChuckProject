# ALS_PlayerCameraBehavior

Path: /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CameraSystem/ALS_PlayerCameraBehavior.ALS_PlayerCameraBehavior
Class: Blueprint
Parent: /Script/Engine.AnimInstance
Generated: 2026-07-10T21:13:02.714Z

## Variables
- PlayerController: object|/Script/Engine.PlayerController
- ControlledPawn: object|/Script/Engine.Pawn
- MovementState: byte|/Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_MovementState.ALS_MovementState
- MovementAction: byte|/Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_MovementAction.ALS_MovementAction
- RotationMode: byte|/Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_RotationMode.ALS_RotationMode
- Gait: byte|/Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_Gait.ALS_Gait
- Stance: byte|/Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_Stance.ALS_Stance
- ViewMode: byte|/Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_ViewMode.ALS_ViewMode
- RightShoulder: bool
- DebugView: bool

## Graphs
- Aiming (AnimationStateGraph): 16 nodes, 15 edges
- Looking Direction (AnimationStateGraph): 16 nodes, 15 edges
- Velocity Direction (AnimationStateGraph): 16 nodes, 15 edges
- Main Camera States (AnimationStateMachineGraph): 10 nodes, 13 edges
- Transition (AnimationTransitionGraph): 3 nodes, 2 edges
- Transition (AnimationTransitionGraph): 3 nodes, 2 edges
- Transition (AnimationTransitionGraph): 3 nodes, 2 edges
- EventGraph (EventGraph): 3 nodes, 1 edges
- AnimGraph (Function): 43 nodes, 31 edges
- UpdateCharacterInfo (Function): 16 nodes, 26 edges

## Important References
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_ViewMode
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_Stance
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_Gait
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CameraSystem/Camera_Skeleton
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Curves/CameraBlendCurves/CameraLerp_1
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Curves/CameraBlendCurves/CameraLerp_2
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_MovementState
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/Interfaces/ALS_Controller_BPI
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_OverlayState
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/Interfaces/ALS_Character_BPI
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_MovementAction
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/Interfaces/ALS_Camera_BPI
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_RotationMode

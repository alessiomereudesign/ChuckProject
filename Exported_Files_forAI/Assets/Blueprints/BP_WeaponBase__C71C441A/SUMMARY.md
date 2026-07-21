# BP_WeaponBase

Path: /Game/ChuckContent/Systems/Weapons/Blueprints/BP_WeaponBase.BP_WeaponBase
Class: Blueprint
Parent: /Script/Engine.Actor
Generated: 2026-07-21T14:07:27.544Z

## Variables
- WeaponData: struct|/Game/ChuckContent/Systems/Weapons/Data/S_WeaponData.S_WeaponData
- OwnerChuck: object|/Game/ChuckContent/Blueprints/ALS_ChuckBP.ALS_ChuckBP_C
- bIsEquipped: bool
- AttachLocationOffset: struct|/Script/CoreUObject.Vector
- AttachScaleOffset: struct|/Script/CoreUObject.Vector
- AttachRotationOffset: struct|/Script/CoreUObject.Rotator

## Graphs
- EventGraph (EventGraph): 26 nodes, 28 edges
- CanFire (Function): 5 nodes, 4 edges
- DoHitScan (Function): 27 nodes, 42 edges
- Equip (Function): 1 nodes, 0 edges
- GetFireMontage (Function): 4 nodes, 3 edges
- GetFireRate (Function): 4 nodes, 3 edges
- GetHitRange (Function): 4 nodes, 3 edges
- GetMuzzleTransform (Function): 4 nodes, 3 edges
- GetReloadMontage (Function): 4 nodes, 3 edges
- InitializeWeapon (Function): 19 nodes, 26 edges
- IsLoopingWeapon (Function): 4 nodes, 3 edges
- PlayFireEffects (Function): 1 nodes, 0 edges
- Reload (Function): 2 nodes, 1 edges
- SpawnMuzzleFX (Function): 7 nodes, 7 edges
- SpawnWeaponProjectile (Function): 5 nodes, 10 edges
- Unequip (Function): 1 nodes, 0 edges
- UpdateWeaponData (Function): 2 nodes, 2 edges
- UserConstructionScript (Function): 1 nodes, 0 edges

## Important References
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Blueprints/BP_WeaponProjectileData
- /Engine/EditorBlueprintResources/StandardMacros

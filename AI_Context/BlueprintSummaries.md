# Blueprint Summaries

## ALS_ChuckBP

- Probable System: ALS / Locomotion (heuristic)
- Parent Class: /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_BaseCharacterBP.ALS_BaseCharacterBP_C
- Main Class: /Game/ChuckContent/Blueprints/ALS_ChuckBP.ALS_ChuckBP_C
- Compile Status: UpToDate
- Graph Count: 27
- Node Count: 1290

### Important Variables

- OwnedWeapons
- Equipped_BigWeapon
- Equipped_Item
- CurrentWeaponSlot
- CurrentEquippedWeapon
- CurrentBigSmallWeaponBaseDamage
- CurrentMeleeBaseDamage
- CurrentBigSmalWeaponDamageRadius
- CurrentWeaponHitRange
- bIsCurrentWeaponExplosive?
- bIsCurrentWeaponLoopHit?
- bAreWeaponsVisible
- LoopedWeaponTimeHandle
- OwnedItems
- As ALS Player Controller
- CurrentMagazineAmmo
- InventoryAmmo
- Inventory
- CurrentWeaponData
- CurrentWeaponIndex

### Interfaces

- /Game/ChuckContent/Blueprints/BPI_Interaction.BPI_Interaction_C

### Events

- AddItemToInventory
- ClearArmorSlot
- ClearWeaponSlot
- CommitEquipItem
- EquipAccessory1
- EquipAccessory2
- EquipBigWeapon
- EquipChest
- EquipFeet
- EquipHead
- EquipLegs
- EquipMelee
- EquipSmallWeapon
- EventLoopHit
- Evento ActorBeginOverlap
- Evento ActorEndOverlap
- Evento Tick
- FistsState
- Flash
- ReloadCurrentWeapon
- ResetCombo
- ToggleArmorVisibility
- ToggleWeaponsVisibility
- TryAutoReloadCurrentWeapon
- UnarmedState
- UseConsumable

### Functions

- AddWeaponToInventory
- AttachToHand
- BPI_Get_3P_PivotTarget
- BPI_Get_3P_TraceParams
- BPI_Get_FP_CameraTarget
- ClearHeldObject
- GetCurrentWeaponFromInventory
- GetGetUpAnimation
- GetMantleAsset
- GetRollAnimation
- Has Weapon?
- MantleEnd
- MantleStart
- On Begin Play
- OnOverlayStateChanged
- RagdollEnd
- RagdollStart
- Set/ResetColors
- SetDynamicMaterials
- SpawnMuzzleFX
- UpdateColoringSystem
- UpdateHeldObject
- UpdateHeldObjectAnimations
- UpdateLayeringColors
- UserConstructionScript

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 391 nodes, 1397 pins, 439 links
- AttackGraph (EventGraph): 377 nodes, 1509 pins, 468 links
- Set/ResetColors (Function): 104 nodes, 277 pins, 103 links
- UpdateLayeringColors (Function): 80 nodes, 248 pins, 81 links
- SetDynamicMaterials (Function): 48 nodes, 210 pins, 61 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapDark/Sound/Knife/Wavs/Knife_ImpactBody01
- /Game/AdditionalContents/AdvancedLocomotionV4/Audio/Footsteps/Concrete_Pivot_03
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_BaseCharacterBP
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_Player_Controller
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/Interfaces/ALS_Camera_BPI
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/Interfaces/ALS_Controller_BPI
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/ALS_AnimBP
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_CLF_GetUp_Back_Montage_2H
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_CLF_GetUp_Back_Montage_Default
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_CLF_GetUp_Back_Montage_LH
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_CLF_GetUp_Back_Montage_RH
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_CLF_GetUp_Front_Montage_2H
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_CLF_GetUp_Front_Montage_Default
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_CLF_GetUp_Front_Montage_LH
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_CLF_GetUp_Front_Montage_RH
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_LandRoll_F_Montage_2H
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_LandRoll_F_Montage_Default
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_LandRoll_F_Montage_LH
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_LandRoll_F_Montage_RH
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_Mantle_1m_Montage_2H
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_Mantle_1m_Montage_Box
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_Mantle_1m_Montage_Default
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_Mantle_1m_Montage_LH
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_Mantle_1m_Montage_RH
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Actions/ALS_N_Mantle_2m_Montage_Default
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/Meshes/AnimMan
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/Meshes/Mannequin
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Curves/MantleCurves/Mantle_1m
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Curves/MantleCurves/Mantle_2m
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_OverlayState
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_RotationMode
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/MantleType
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/ALS_ComponentAndTransform
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/Mantle_Asset
- /Game/AdditionalContents/AdvancedLocomotionV4/Props/Meshes/Binoculars
- /Game/AdditionalContents/AdvancedLocomotionV4/Props/Meshes/Bow_AnimBP
- /Game/AdditionalContents/AdvancedLocomotionV4/Props/Meshes/Torch
- /Game/AdditionalContents/RamsterZ_FreeAnims_Volume1/AnimationSequence/H2H/AM_MM_H2H_LeftPunch
- /Game/AdditionalContents/RamsterZ_FreeAnims_Volume1/AnimationSequence/H2H/AM_MM_H2H_RightBigPunch
- /Game/AdditionalContents/RamsterZ_FreeAnims_Volume1/AnimationSequence/H2H/AM_MM_H2H_RightPunch
- /Game/ChuckContent/Blueprints/BPI_Interaction
- /Game/ChuckContent/Input/IA_Interact
- /Game/ChuckContent/Systems/Weapons/Blueprints/BP_WeaponProjectileData
- /Game/ChuckContent/Systems/Weapons/Data/DT_Weapon
- /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType
- /Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/UI/Interfaces/WBP_Tip
- /Game/ChuckContent/UI/WIDGET_MENU/01_HUD/MINIMAP/RT_Minimap
- /Game/ChuckContent/UI/WIDGET_MENU/01_HUD/WBP_HUD
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/DT_Armor
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/E_ArmorSlot
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/S_ArmorData
- /Game/ChuckContent/UI/WIDGET_MENU/WBP_MenuPausa

### Notes

Blueprint probabilmente collegato a 'ALS / Locomotion' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_Blueprints_ALS_ChuckBP.json)

## BPI_Interaction

- Probable System: Interaction (heuristic)
- Parent Class: /Script/CoreUObject.Interface
- Main Class: /Game/ChuckContent/Blueprints/BPI_Interaction.BPI_Interaction_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 1

### Important Variables

- Nessuno rilevato.

### Interfaces

- Nessuno rilevato.

### Events

- Nessuno rilevato.

### Functions

- Interact

### Macros

- Nessuno rilevato.

### Large Graphs

- Interact (Function): 1 nodes, 1 pins, 0 links

### Dependencies

- Nessuno rilevato.

### Notes

Blueprint probabilmente collegato a 'Interaction' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_Blueprints_BPI_Interaction.json)

## BP_WeaponProjectileData

- Probable System: Weapons / Combat (heuristic)
- Parent Class: /Script/Engine.Actor
- Main Class: /Game/ChuckContent/Systems/Weapons/Blueprints/BP_WeaponProjectileData.BP_WeaponProjectileData_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 28

### Important Variables

- Damage
- DamageRadius
- TrailFX
- ExplosionFX
- ProjectileMesh
- ProjectileSpeed

### Interfaces

- Nessuno rilevato.

### Events

- Evento BeginPlay
- On Component Hit (Sphere)

### Functions

- UserConstructionScript

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 27 nodes, 124 pins, 30 links
- UserConstructionScript (Function): 1 nodes, 1 pins, 0 links

### Dependencies

- Nessuno rilevato.

### Notes

Blueprint probabilmente collegato a 'Weapons / Combat' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_Systems_Weapons_Blueprints_BP_WeaponProjectileData.json)

## BP_CharacterPreview

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/Engine.Actor
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/CharacterPreview/BP_CharacterPreview.BP_CharacterPreview_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 17

### Important Variables

- Nessuno rilevato.

### Interfaces

- Nessuno rilevato.

### Events

- InitializeStudio

### Functions

- UserConstructionScript

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 16 nodes, 39 pins, 16 links
- UserConstructionScript (Function): 1 nodes, 1 pins, 0 links

### Dependencies

- /Engine/EditorResources/LightIcons/S_LightError
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/CharacterPreview/RT_CharacterPreview

### Notes

Blueprint probabilmente collegato a 'UI / Widgets' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_1_MENU_ARCHIVE_Equipment_CharacterPreview_BP_CharacterPreview.json)

## AIC_EnemyALS

- Probable System: ALS / Locomotion (heuristic)
- Parent Class: /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/AI/ALS_AI_Controller.ALS_AI_Controller_C
- Main Class: /Game/ChuckContent/Blueprints/Enemies/AIC_EnemyALS.AIC_EnemyALS_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 4

### Important Variables

- Nessuno rilevato.

### Interfaces

- Nessuno rilevato.

### Events

- Evento BeginPlay
- Evento Tick

### Functions

- UserConstructionScript

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 2 nodes, 5 pins, 0 links
- UserConstructionScript (Function): 2 nodes, 4 pins, 1 links

### Dependencies

- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/AI/ALS_AI_Controller

### Notes

Blueprint probabilmente collegato a 'ALS / Locomotion' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_Blueprints_Enemies_AIC_EnemyALS.json)

## BP_EnemyALS

- Probable System: ALS / Locomotion (heuristic)
- Parent Class: /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_BaseCharacterBP.ALS_BaseCharacterBP_C
- Main Class: /Game/ChuckContent/Blueprints/Enemies/BP_EnemyALS.BP_EnemyALS_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 21

### Important Variables

- Health

### Interfaces

- Nessuno rilevato.

### Events

- Evento AnyDamage

### Functions

- UserConstructionScript

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 19 nodes, 69 pins, 20 links
- UserConstructionScript (Function): 2 nodes, 4 pins, 1 links

### Dependencies

- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_BaseCharacterBP
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/ALS_AnimBP
- /Game/AdditionalContents/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/Meshes/AnimMan
- /Game/ChuckContent/Blueprints/Enemies/AIC_EnemyALS

### Notes

Blueprint probabilmente collegato a 'ALS / Locomotion' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_Blueprints_Enemies_BP_EnemyALS.json)

## BP_MasterPickUpSkeletalMesh

- Probable System: Weapons / Combat (heuristic)
- Parent Class: /Script/Engine.Actor
- Main Class: /Game/ChuckContent/Systems/Weapons/Blueprints/BP_MasterPickUpSkeletalMesh.BP_MasterPickUpSkeletalMesh_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 51

### Important Variables

- InstanceWeaponData

### Interfaces

- Nessuno rilevato.

### Events

- Evento BeginPlay
- On Component Begin Overlap (Sphere)
- On Component End Overlap (Sphere)

### Functions

- UserConstructionScript

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 47 nodes, 210 pins, 54 links
- UserConstructionScript (Function): 4 nodes, 14 pins, 4 links

### Dependencies

- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapDark/Sound/RocketLauncher/wavs/RocketLauncher_Reload02
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_OverlayState
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Blueprints/BP_WeaponProjectileData
- /Game/ChuckContent/Systems/Weapons/Blueprints/WBP_AssetName
- /Game/ChuckContent/Systems/Weapons/Data/DT_Weapon
- /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType
- /Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/UI/files/MI_Outline
- /Game/ChuckContent/UI/Interfaces/WBP_Tip

### Notes

Blueprint probabilmente collegato a 'Weapons / Combat' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_Systems_Weapons_Blueprints_BP_MasterPickUpSkeletalMesh.json)

## BP_MasterPickUpStaticMesh

- Probable System: Weapons / Combat (heuristic)
- Parent Class: /Script/Engine.Actor
- Main Class: /Game/ChuckContent/Systems/Weapons/Blueprints/BP_MasterPickUpStaticMesh.BP_MasterPickUpStaticMesh_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 40

### Important Variables

- AmmoAmount
- AmmoType
- As ALS Player Controller

### Interfaces

- Nessuno rilevato.

### Events

- Evento BeginPlay
- On Component Begin Overlap (Sphere)
- On Component End Overlap (Sphere)

### Functions

- UserConstructionScript

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 39 nodes, 152 pins, 45 links
- UserConstructionScript (Function): 1 nodes, 1 pins, 0 links

### Dependencies

- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_Player_Controller
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Blueprints/WBP_AssetName
- /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType
- /Game/ChuckContent/UI/files/MI_Outline
- /Game/ChuckContent/UI/Interfaces/WBP_Tip
- /Game/ChuckContent/UI/WIDGET_MENU/01_HUD/WBP_HUD

### Notes

Blueprint probabilmente collegato a 'Weapons / Combat' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_Systems_Weapons_Blueprints_BP_MasterPickUpStaticMesh.json)

## WBP_Tip

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/Interfaces/WBP_Tip.WBP_Tip_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 24

### Important Variables

- Txt_Translated

### Interfaces

- Nessuno rilevato.

### Events

- Evento Construct
- ShowTip

### Functions

- GetInputKeys

### Macros

- Nessuno rilevato.

### Large Graphs

- GetInputKeys (Function): 18 nodes, 51 pins, 15 links
- EventGraph (EventGraph): 6 nodes, 17 pins, 5 links

### Dependencies

- /Game/ChuckContent/Input/IA_Interact
- /Game/ChuckContent/UI/files/Text/Text

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_Interfaces_WBP_Tip.json)

## WBP_HUD

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/01_HUD/WBP_HUD.WBP_HUD_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 35

### Important Variables

- As ALS Chuck BP

### Interfaces

- Nessuno rilevato.

### Events

- Evento Construct
- UpdateWeaponDisplay

### Functions

- Nessuno rilevato.

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 35 nodes, 114 pins, 43 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType
- /Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/UI/files/ICONS/Fist
- /Game/ChuckContent/UI/files/img/pngtree-design-element-collimation-material-png-image_7185230
- /Game/ChuckContent/UI/files/Text/Text
- /Game/ChuckContent/UI/WIDGET_MENU/01_HUD/MINIMAP/M_Minimap_UI

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_01_HUD_WBP_HUD.json)

## WBP_MenuArchive

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/WBP_MenuArchive.WBP_MenuArchive_C
- Compile Status: UpToDate
- Graph Count: 9
- Node Count: 975

### Important Variables

- ActiveWeaponSelectorRef
- ActiveArmorSelectorRef
- LocalItemName
- LocalItemIcon
- CurrentSlot

### Interfaces

- Nessuno rilevato.

### Events

- Background Grey Dark/Light
- CharacterCard > CharacterSlotPage
- CharacterSlotPage > IntersectPage
- Content Whitee Dark/Light
- Evento Construct
- Evento Destruct
- Evento Tick
- FocusedTabColor
- On Clicked (Btn_AllInventory)
- On Clicked (Btn_ArmorInventory)
- On Clicked (Btn_Back)
- On Clicked (Btn_Personaggi)
- On Clicked (Btn_WeaponsInventory)
- On Clicked (BtnSlot_Accessory1Equip)
- On Clicked (BtnSlot_AccessoryEquip)
- On Clicked (BtnSlot_BigWeapon)
- On Clicked (BtnSlot_ChestEquip)
- On Clicked (BtnSlot_FeetEquip)
- On Clicked (BtnSlot_HeadEquip)
- On Clicked (BtnSlot_Inventory)
- On Clicked (BtnSlot_Item)
- On Clicked (BtnSlot_LegsEquip)
- On Clicked (BtnSlot_Melee)
- On Clicked (BtnSlot_SmallFirearm)
- On Clicked (ToggleVisibArmor)
- On Clicked (ToggleVisibWeapons)
- OpenCharacterSlot
- PopulateItemGrid
- RefreshMenuFocus
- ReturnBackManage
- ShowAllItems
- ShowArmorItems
- ShowWeapons Items
- UnfocusedTabColor

### Functions

- OnAnalogValueChanged
- OnArmorSlotClicked
- OnKeyDown
- OnWeaponSlotClicked
- UpdateEquipmentSlots
- UpdateWeaponSlots

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 259 nodes, 778 pins, 300 links
- OnKeyDown (Function): 245 nodes, 712 pins, 259 links
- InventoryGraph (EventGraph): 183 nodes, 739 pins, 198 links
- IntersectGraph (EventGraph): 95 nodes, 310 pins, 103 links
- UpdateEquipmentSlots (Function): 70 nodes, 244 pins, 80 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapDark/Sound/Pistol/Wavs/Pistol_Whip02
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapDark/Sound/Rifle/Wavs/Rifle_Reload01
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapSilver/Sound/Knife/Wavs/Knife_Raise
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapSilver/Sound/Knife/Wavs/KnifeA_Swing02
- /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_OverlayState
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Blueprints/BP_WeaponProjectileData
- /Game/ChuckContent/Systems/Weapons/Data/DT_Weapon
- /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType
- /Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/UI/files/ICONS/Antiprojectile_W
- /Game/ChuckContent/UI/files/ICONS/Backpack_W
- /Game/ChuckContent/UI/files/ICONS/medikit
- /Game/ChuckContent/UI/files/ICONS/pistol
- /Game/ChuckContent/UI/files/Text/ocr-a-bold_Font
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/DT_Armor
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/E_ArmorSlot
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/S_ArmorData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/CharacterPreview/BP_CharacterPreview
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/CharacterPreview/M_CharacterPreview_UI
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_SelectorButton
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_WeaponSelector
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/DT_CharacterData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/F_CharacterData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/WBP_TabIntersect_CharacterCard
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/WBP_TabIntersect_CharacterSlot
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/consum
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/feet
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/glasses
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/Hat
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/knife
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/medikit
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/pants
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/pistol
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/rifle
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/T-Shirt
- /Game/ChuckContent/UI/WIDGET_MENU/WBP_MenuPausa

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_1_MENU_ARCHIVE_WBP_MenuArchive.json)

## WBP_TabIntersect_CharacterSlot

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/WBP_TabIntersect_CharacterSlot.WBP_TabIntersect_CharacterSlot_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 34

### Important Variables

- CharacterData

### Interfaces

- Nessuno rilevato.

### Events

- Evento On Added to Focus Path
- Evento On Removed from Focus Path
- Evento Pre Construct
- InizializeCharacterSlot
- On Clicked (Btn_Slot)

### Functions

- OnSlotSelected

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 33 nodes, 117 pins, 33 links
- OnSlotSelected (DelegateSignature): 1 nodes, 2 pins, 0 links

### Dependencies

- /Game/ChuckContent/UI/files/Text/ocr-a-bold_Font
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/E_CharactersAffiliates
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/F_CharacterData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/Img/21-213224_unknown-person-icon-png-download
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/WBP_MenuArchive

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_1_MENU_ARCHIVE_Intersect_WBP_TabIntersect_CharacterSlot.json)

## WBP_SelectorButton

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_SelectorButton.WBP_SelectorButton_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 25

### Important Variables

- WeaponData
- RowName_Item
- Txt_ItemName
- Icon_Item
- WeaponSelectorRef
- ItemType
- WeaponIndex

### Interfaces

- Nessuno rilevato.

### Events

- Evento Construct
- Evento On Added to Focus Path
- Evento On Removed from Focus Path
- On Clicked (Btn_Selector)

### Functions

- Nessuno rilevato.

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 25 nodes, 83 pins, 22 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapDark/Sound/Rifle/Wavs/Rifle_Reload01
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/UI/files/Text/ocr-a-bold_Font
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_WeaponSelector
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/WBP_MenuArchive

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_1_MENU_ARCHIVE_Equipment_WBP_SelectorButton.json)

## WBP_WeaponSelector

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_WeaponSelector.WBP_WeaponSelector_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 108

### Important Variables

- IsWeapon?
- TargetWeaponSlot
- TargetArmorSlot
- ItemCount

### Interfaces

- Nessuno rilevato.

### Events

- EquipAndClose
- Evento Construct

### Functions

- Nessuno rilevato.

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 108 nodes, 389 pins, 161 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Blueprints/BP_WeaponProjectileData
- /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType
- /Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/DT_Armor
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/E_ArmorSlot
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/S_ArmorData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_SelectorButton
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/WBP_MenuArchive

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_1_MENU_ARCHIVE_Equipment_WBP_WeaponSelector.json)

## WBP_MenuPausa

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/WBP_MenuPausa.WBP_MenuPausa_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 88

### Important Variables

- MenuArchiveRef
- FocusedColor
- UnfocusedColor

### Interfaces

- Nessuno rilevato.

### Events

- ChangeColorOnFocus
- Evento Construct
- Evento Tick
- On Clicked (Btn_Archive)
- On Clicked (Btn_Quit)
- On Clicked (Btn_Resume)
- On Clicked (Btn_SaveGame)
- OpenAndInizializeMenu

### Functions

- OnKeyDown

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 73 nodes, 250 pins, 71 links
- OnKeyDown (Function): 15 nodes, 49 pins, 16 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/ChuckContent/UI/files/Text/OCRAEXT_Font
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/WBP_MenuArchive

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_WBP_MenuPausa.json)

## WBP_TabIntersect_CharacterCard

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/WBP_TabIntersect_CharacterCard.WBP_TabIntersect_CharacterCard_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 44

### Important Variables

- CharacterData

### Interfaces

- Nessuno rilevato.

### Events

- Evento Construct
- Evento Pre Construct
- Evento Tick
- FadeInEvent
- FadeOutEvent
- InizializeCharacterCard

### Functions

- Nessuno rilevato.

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 44 nodes, 172 pins, 56 links

### Dependencies

- /Game/ChuckContent/UI/files/img/ChatGPT_Image_9_giu_2026__23_43_50
- /Game/ChuckContent/UI/files/Text/ocr-a-bold_Font
- /Game/ChuckContent/UI/files/Text/OCRAEXT_Font
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/E_CharactersAffiliates
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/F_CharacterData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/Img/21-213224_unknown-person-icon-png-download

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_1_MENU_ARCHIVE_Intersect_WBP_TabIntersect_CharacterCard.json)

## WBP_CustomRadialMenu

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/2_MENU_RAPIDO/WBP_CustomRadialMenu.WBP_CustomRadialMenu_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 137

### Important Variables

- TargetIndex
- CurrentSelectedSlot
- As ALS Player Controller

### Interfaces

- Nessuno rilevato.

### Events

- CloseRadialMenu
- Evento Construct
- Evento Tick

### Functions

- Nessuno rilevato.

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 137 nodes, 451 pins, 169 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapDark/Sound/Pistol/Wavs/Pistol_Reload01
- /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/CharacterLogic/ALS_Player_Controller
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/UI/files/ICONS/Fist
- /Game/ChuckContent/UI/files/ICONS/glasses
- /Game/ChuckContent/UI/files/ICONS/knife
- /Game/ChuckContent/UI/files/ICONS/medikit
- /Game/ChuckContent/UI/files/ICONS/pistol
- /Game/ChuckContent/UI/files/ICONS/rifle
- /Game/ChuckContent/UI/files/ICONS/sandwitch
- /Game/ChuckContent/UI/WIDGET_MENU/01_HUD/WBP_HUD
- /Game/ChuckContent/UI/WIDGET_MENU/2_MENU_RAPIDO/tast

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_2_MENU_RAPIDO_WBP_CustomRadialMenu.json)

## WBP_MenuPrincipale

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/0_MAIN_MENU/WBP_MenuPrincipale.WBP_MenuPrincipale_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 66

### Important Variables

- MenuArchiveRef
- FocusedColor
- UnfocusedColor

### Interfaces

- Nessuno rilevato.

### Events

- ChangeColorOnFocus
- Evento Construct
- On Clicked (Btn_EsciDalGioco)
- On Clicked (Btn_Inizia)
- On Clicked (Btn_Load)
- VerifyFocusGamepad

### Functions

- Nessuno rilevato.

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 66 nodes, 311 pins, 69 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapDark/Sound/Pistol/Wavs/Pistol_Whip02
- /Game/ChuckContent/UI/files/img/ChatGPT_Image_10_giu_2026__11_15_33
- /Game/ChuckContent/UI/files/Text/ocr-a-bold_Font
- /Game/ChuckContent/UI/files/Text/OCRAEXT_Font
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/WBP_MenuArchive

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_0_MAIN_MENU_WBP_MenuPrincipale.json)

## WBP_AssetName

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/Systems/Weapons/Blueprints/WBP_AssetName.WBP_AssetName_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 9

### Important Variables

- Nessuno rilevato.

### Interfaces

- Nessuno rilevato.

### Events

- Evento Construct
- Evento Pre Construct
- Evento Tick

### Functions

- SetAssetName

### Macros

- Nessuno rilevato.

### Large Graphs

- SetAssetName (Function): 5 nodes, 11 pins, 5 links
- EventGraph (EventGraph): 4 nodes, 11 pins, 0 links

### Dependencies

- /Game/ChuckContent/UI/files/Text/ocr-a-bold_Font

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_Systems_Weapons_Blueprints_WBP_AssetName.json)

## WBP_GenericPrompt

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/Blueprints/WBP_GenericPrompt.WBP_GenericPrompt_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 0

### Important Variables

- Nessuno rilevato.

### Interfaces

- Nessuno rilevato.

### Events

- Nessuno rilevato.

### Functions

- Nessuno rilevato.

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 0 nodes, 0 pins, 0 links

### Dependencies

- /Game/ChuckContent/UI/files/Text/ocr-a-bold_Font

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_Blueprints_WBP_GenericPrompt.json)

## WBP_ArmorSelector

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/UMG.UserWidget
- Main Class: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_ArmorSelector.WBP_ArmorSelector_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 108

### Important Variables

- IsWeapon?
- TargetWeaponSlot
- TargetArmorSlot
- ItemCount

### Interfaces

- Nessuno rilevato.

### Events

- EquipAndClose
- Evento Construct

### Functions

- Nessuno rilevato.

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 108 nodes, 389 pins, 161 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Blueprints/BP_WeaponProjectileData
- /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType
- /Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/DT_Armor
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/E_ArmorSlot
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/S_ArmorData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_SelectorButton
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_WeaponSelector
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/WBP_MenuArchive

### Notes

Widget Blueprint dedotto da prefisso o parent class; il comportamento va verificato tramite grafi e links.

[JSON completo](../Game_ChuckContent_UI_WIDGET_MENU_1_MENU_ARCHIVE_Equipment_WBP_ArmorSelector.json)

## BP_TestTrigger

- Probable System: Misc / Unknown (heuristic)
- Parent Class: /Script/Engine.Actor
- Main Class: /Game/ChuckContent/Blueprints/BP_TestTrigger.BP_TestTrigger_C
- Compile Status: UpToDateWithWarnings
- Graph Count: 2
- Node Count: 8

### Important Variables

- Nessuno rilevato.

### Interfaces

- Nessuno rilevato.

### Events

- Evento ActorBeginOverlap
- Evento BeginPlay
- Evento Tick
- On Component Begin Overlap (Box)

### Functions

- UserConstructionScript

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 7 nodes, 31 pins, 5 links
- UserConstructionScript (Function): 1 nodes, 1 pins, 0 links

### Dependencies

- /Engine/BasicShapes/BasicShapeMaterial
- /Engine/BasicShapes/Cube
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData

### Notes

Blueprint probabilmente collegato a 'Misc / Unknown' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_Blueprints_BP_TestTrigger.json)

## Chuck_HUD

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/Engine.HUD
- Main Class: /Game/ChuckContent/UI/Interfaces/Chuck_HUD.Chuck_HUD_C
- Compile Status: UpToDate
- Graph Count: 2
- Node Count: 18

### Important Variables

- Wdg Tip

### Interfaces

- /Game/ChuckContent/UI/Interfaces/BPI_ChuckHUD.BPI_ChuckHUD_C

### Events

- ShowTip_1

### Functions

- UserConstructionScript

### Macros

- Nessuno rilevato.

### Large Graphs

- EventGraph (EventGraph): 17 nodes, 55 pins, 23 links
- UserConstructionScript (Function): 1 nodes, 1 pins, 0 links

### Dependencies

- /Engine/EditorBlueprintResources/StandardMacros
- /Game/ChuckContent/UI/Interfaces/BPI_ChuckHUD
- /Game/ChuckContent/UI/Interfaces/WBP_Tip

### Notes

Blueprint probabilmente collegato a 'UI / Widgets' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_UI_Interfaces_Chuck_HUD.json)

## BPI_ChuckHUD

- Probable System: UI / Widgets (heuristic)
- Parent Class: /Script/CoreUObject.Interface
- Main Class: /Game/ChuckContent/UI/Interfaces/BPI_ChuckHUD.BPI_ChuckHUD_C
- Compile Status: UpToDate
- Graph Count: 1
- Node Count: 1

### Important Variables

- Nessuno rilevato.

### Interfaces

- Nessuno rilevato.

### Events

- Nessuno rilevato.

### Functions

- ShowTip

### Macros

- Nessuno rilevato.

### Large Graphs

- ShowTip (Function): 1 nodes, 3 pins, 0 links

### Dependencies

- Nessuno rilevato.

### Notes

Blueprint probabilmente collegato a 'UI / Widgets' in base a nome e path; riepilogo statico da metadati e struttura dei grafi.

[JSON completo](../Game_ChuckContent_UI_Interfaces_BPI_ChuckHUD.json)

# WBP_MenuArchive

Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/WBP_MenuArchive.WBP_MenuArchive
Class: Blueprint
Parent: /Script/UMG.UserWidget
Generated: 2026-07-21T14:07:27.544Z

## Variables
- MenuPausaRef: object|/Game/ChuckContent/UI/WIDGET_MENU/WBP_MenuPausa.WBP_MenuPausa_C
- As ChuckRef: object|/Game/ChuckContent/Blueprints/ALS_ChuckBP.ALS_ChuckBP_C
- SpawnedStudioRef: object|/Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/CharacterPreview/BP_CharacterPreview.BP_CharacterPreview_C
- LastClickedButton: object|/Script/UMG.Button
- ActiveWeaponSelectorRef: object|/Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_WeaponSelector.WBP_WeaponSelector_C
- ActiveArmorSelectorRef: object|/Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_WeaponSelector.WBP_WeaponSelector_C
- ColorFocused: struct|/Script/CoreUObject.LinearColor
- ColorUnfocused: struct|/Script/CoreUObject.LinearColor
- ZainoCompleto: name|container=Array
- LocalItemName: text
- LocalItemIcon: object|/Script/Engine.Texture2D
- CurrentSlot: byte|/Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot.E_WeaponSlot

## Graphs
- EventGraph (EventGraph): 262 nodes, 302 edges
- IntersectGraph (EventGraph): 95 nodes, 103 edges
- InventoryGraph (EventGraph): 194 nodes, 211 edges
- OnAnalogValueChanged (Function): 26 nodes, 28 edges
- OnArmorSlotClicked (Function): 18 nodes, 23 edges
- OnKeyDown (Function): 245 nodes, 258 edges
- OnWeaponSlotClicked (Function): 17 nodes, 22 edges
- UpdateEquipmentSlots (Function): 70 nodes, 80 edges
- UpdateWeaponSlots (Function): 86 nodes, 111 edges

## Important References
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/feet
- /Game/ChuckContent/UI/files/ICONS/medikit
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapDark/Sound/Pistol/Wavs/Pistol_Whip02
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapSilver/Sound/Knife/Wavs/Knife_Raise
- /Game/ChuckContent/UI/WIDGET_MENU/WBP_MenuPausa
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/CharacterPreview/M_CharacterPreview_UI
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapDark/Sound/Rifle/Wavs/Rifle_Reload01
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/T-Shirt
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/medikit
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/glasses
- /Game/AdditionalContents/_WeaponsPacks/MilitaryWeapSilver/Sound/Knife/Wavs/KnifeA_Swing02
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/pistol
- /Game/ChuckContent/Systems/Weapons/Data/DT_Weapon
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/WBP_TabIntersect_CharacterSlot
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/CharacterPreview/BP_CharacterPreview
- /Game/ChuckContent/UI/files/ICONS/Backpack_W
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/rifle
- /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/DT_Armor
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/knife
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/WBP_TabIntersect_CharacterCard
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/Hat
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/E_ArmorSlot
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/consum
- /Game/ChuckContent/Blueprints/ALS_ChuckBP
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_WeaponSelector
- /Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot
- /Game/ChuckContent/UI/WIDGET_MENU/ICONS/ICONS_EMPTY/pants
- /Game/ChuckContent/UI/files/ICONS/Antiprojectile_W
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/DT_CharacterData
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/WBP_SelectorButton
- /Game/ChuckContent/Systems/Weapons/Blueprints/BP_WeaponProjectileData
- /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType
- /Game/ChuckContent/UI/files/ICONS/pistol
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/F_CharacterData
- /Game/ChuckContent/UI/files/Text/ocr-a-bold_Font
- /Engine/EditorBlueprintResources/StandardMacros
- /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/S_ArmorData

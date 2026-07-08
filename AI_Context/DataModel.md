# Data Model

## Structs

### S_WeaponData

- Path: /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData.S_WeaponData

Fields:
- RowName_80_90C885E245FEA60369938EAC6E1FCB25: FName = None
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Weapon_Icon_67_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D* = None
- Weapon_Image_68_E0882141471F7B74AF02C2B8D100E2BB: UTexture2D* = None
- Technical_Info_55_96E6AFB44DBF5A6518FAD09002832322: FText
- SlotType_5_6A80ABC24B17EFCD8135D98F80F1052A: TEnumAsByte<E_WeaponSlot> = NewEnumerator0
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh* = None
- ALS_OverlayState_16_84ACF4C94D2D7CFCD490FEA5E94AF136: TEnumAsByte<ALS_OverlayState> = NewEnumerator0
- AttackMontage_41_1AC39D4A4FCDB6A8A8C8B5AD841AEDB9: UAnimMontage* = None
- ReloadMontage_42_70E4B0D745DD79FC954BD8BA6A7CFB18: UAnimMontage* = None
- HolsterSocket_22_F328E5D44A0493E4582BAC8E4D2C1D4B: FName = None
- HandSocket_24_89A03DC24973F91DA8FD2990B14E6F5E: FName = None
- BaseDamage_45_F289CC934ED7259D6122668BE2919E95: double = 0.000000
- DamageRadius_50_C83F28B2469DEBCA28C054A5B7E9388F: double = 0.000000
- TraceRadius_118_B0D837064F49FEDF1DD885AF55D54B84: double = 0.000000
- HitRange_58_53C8DCE547CE983F554D118DC7343869: double = 0.000000
- FireRate_85_D4AF7CD849600FE131B142B9432BB57A: double = 0.000000
- MaxMagazineCapacity_72_D0C5AAE44C4A57660DC71B8A4310666D: int32 = 0
- CurrentAmmoInMagazine_75_6C0D0FC744AA581F3583A7AD569F10A8: int32 = 0
- CurrentReservedAmmo_77_63C0F0BC400C091CCA9E73B44C19DA22: int32 = 0
- IsExplosive?_47_96E770804A49F8E44F6A818192D7A8BA: bool = False
- IsLoopHit?_60_4D6D7C754FE89BCD1232E1834B3976D1: bool = False
- IsEquipped?_82_B4C251E048F3C287DAC918BA8E28F5BC: bool = False
- MuzzleFX_88_427443474634B234F9B526A88FA4E232: UParticleSystem* = None
- TrailFX_94_7630F88044032394DFE85B8471864128: UParticleSystem* = None
- ImpactFX_97_3AF5DF2E4B6DB5A236B80096D754596A: UParticleSystem* = None
- ExplosionFX_98_C2595F5940DECE86B2E3EBB60841AE77: UParticleSystem* = None
- ProjectileClass_110_7D027F1643A36111E2428D94852EFD7D: UClass* = None
- bUsesProjectile_102_79A168584A8CB2ACF8A3B9A5AE4962E0: bool = False
- ProjectileMesh_105_746AFA884B46AC4393B21CB5A81561E8: UStaticMesh* = None
- ProjectileSpeed_108_AF0BF6D24C5C79648E94E8A1524BC6D5: double = 0.000000
- AmmoType_115_D22F449C48769E5D871EEC991DAEE4F4: TEnumAsByte<E_AmmoType> = NewEnumerator0

Used by:

- [[ALS_ChuckBP]]
- [[BP_MasterPickUpSkeletalMesh]]
- [[BP_TestTrigger]]
- [[DT_Weapon]]
- [[WBP_ArmorSelector]]
- [[WBP_CustomRadialMenu]]
- [[WBP_HUD]]
- [[WBP_MenuArchive]]
- [[WBP_SelectorButton]]
- [[WBP_WeaponSelector]]

### S_ArmorData

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/S_ArmorData.S_ArmorData

Fields:
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Icon_36_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D* = None
- SlotType_37_6A80ABC24B17EFCD8135D98F80F1052A: TEnumAsByte<E_ArmorSlot> = NewEnumerator0
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh* = None

Used by:

- [[ALS_ChuckBP]]
- [[DT_Armor]]
- [[WBP_ArmorSelector]]
- [[WBP_MenuArchive]]
- [[WBP_WeaponSelector]]

### F_CharacterData

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/F_CharacterData.F_CharacterData

Fields:
- Subject_57_F26DCFA444362EC15F334C85DAEA606B: FText
- IsSubjectNameDiscovered?_72_371D046546FB4F151B82D68168F2F5D5: bool = False
- Icon_29_865610B04845107E08744FBEB7FC7FD1: UTexture2D* = None
- IsIconDiscovered?_32_209FFF6B4CD855BA7C6A10894DEA7A21: bool = False
- Aka_58_11C4F9654352996678422B9E4D637A62: FText
- IsAkaDiscovered?_73_4E6DBC3649A1AD2E07DEB6AE588F77AE: bool = False
- Nationality_59_D0C389D540DE4A29510B19AD186CEF6C: FText
- IsNationalityDiscovered?_80_61BF9CCF4A21C5B9CC328F8EE970DC62: bool = False
- PlaceOfBirth_60_C9F21F254055CCC9FC647190AFFBE29D: FText
- IsPlaceOfBirthDiscovered?_81_DE78335044A487316282FE9904C3B960: bool = False
- History_1_91_C9E22C80474D28C95371D7B98582444E: FText
- IsHistory_1Discovered?_82_063176C54D16E294CA28CBB3040D074B: bool = False
- History_2_93_66FAE1144ABD799E7AA9DE98739A621F: FText
- IsHistory_2Discovered?_96_CD7D83144FE95F9637C81793FCE6FB1A: bool = False
- History_3_101_C99699D14AA79209FB7902A2A7E96B70: FText
- IsHistory_3Discovered?_105_27A292884C51681A228FBFB161E3A2E7: bool = False
- History_4_102_6060F5E6460A81258273B4953E920724: FText
- IsHistory_4Discovered?_107_E4D8ABF749358EE19D24C18440F6B981: bool = False
- Affiliation_87_BFA5AACE4B04B0E4E281B39CAF247058: TArray<TEnumAsByte<E_CharactersAffiliates> >
- IsAffiliationDiscovered?_39_F8777F234098BF43FB42ADB9667E704C: bool = False
- Summary_71_F6C2334047FBE1B20E67D1B73C9FC9E8: FText
- IsSummaryDiscovered?_88_390CEFB9434AB82E648006BC83172F19: bool = False

Used by:

- [[DT_CharacterData]]
- [[WBP_MenuArchive]]
- [[WBP_TabIntersect_CharacterCard]]
- [[WBP_TabIntersect_CharacterSlot]]

### S_InteractionPrompt

- Path: /Game/ChuckContent/Blueprints/S_InteractionPrompt.S_InteractionPrompt

Fields:
- ActionText_2_3AC59B3E46A172564FA79D99159C6C36: FText
- ObjectName_4_D1DBE99F499FC8276645848688617E8A: FText
- InputAction_7_6279F1D24A27BA475D50FFA2303C8A12: FName = None

Used by:

- Nessuno rilevato.

### S_WheelSlotData

- Path: /Game/ChuckContent/UI/WIDGET_MENU/2_MENU_RAPIDO/S_WheelSlotData.S_WheelSlotData

Fields:
- Name_10_5ECDED464DF78BBE17C45C815763285C: FName = None
- Icon_11_ED13788447B6D5334FD6579404706199: UTexture2D* = None
- ActionType_12_13E522704AF2F96E9AADB6BC1D7DA7A8: TEnumAsByte<E_WheelActionType> = NewEnumerator0
- ALS_State_13_1AEF93D142EC712287FFE9821D69EDCC: TEnumAsByte<ALS_OverlayState> = NewEnumerator0
- ConsumableEventName_14_6D386EDC4E85F7054D94958C84881186: FName = None

Used by:

- Nessuno rilevato.

### F_ObjectData

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/F_ObjectData.F_ObjectData

Fields:
- Name_27_F26DCFA444362EC15F334C85DAEA606B: FText
- Category_38_BFA5AACE4B04B0E4E281B39CAF247058: TArray<TEnumAsByte<E_ObjectsCategory> >
- Description_37_F6C2334047FBE1B20E67D1B73C9FC9E8: FText
- Icon_29_865610B04845107E08744FBEB7FC7FD1: UTexture2D* = None
- IsNameDiscovered?_18_371D046546FB4F151B82D68168F2F5D5: bool = False
- IsAliasDiscovered?_20_4E6DBC3649A1AD2E07DEB6AE588F77AE: bool = False
- IsCategoryDiscovered?_30_F8777F234098BF43FB42ADB9667E704C: bool = False
- IsDescriptionDiscovered?_25_390CEFB9434AB82E648006BC83172F19: bool = False
- IsIconDiscovered?_32_209FFF6B4CD855BA7C6A10894DEA7A21: bool = False

Used by:

- [[DT_ObjectsData]]

### S_ItemsData

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Inventory/S_ItemsData.S_ItemsData

Fields:
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Icon_36_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D* = None
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh* = None
- Description_40_D1E175F4454CD0D995978B97126F49C4: FText

Used by:

- [[DT_Items]]

### S_ConsumableData

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Inventory/S_ConsumableData.S_ConsumableData

Fields:
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Icon_36_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D* = None
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh* = None
- Description_40_2423C9824F4F4F44EF95D78C53E0E886: FText

Used by:

- [[DT_Consumable]]

## Enums

### E_WeaponSlot

- Path: /Game/ChuckContent/Systems/Weapons/Data/E_WeaponSlot.E_WeaponSlot

Values:
- NewEnumerator0 / Fists (index 0, value 0)
- NewEnumerator1 / SmallFirearm (index 1, value 1)
- NewEnumerator2 / Melee (index 2, value 2)
- NewEnumerator3 / BigWeapon (index 3, value 3)
- NewEnumerator5 / Item (index 4, value 4)
- E_MAX / E MAX (index 5, value 5)

Used by:

- [[ALS_ChuckBP]]
- [[BP_MasterPickUpSkeletalMesh]]
- [[S_WeaponData]]
- [[WBP_ArmorSelector]]
- [[WBP_CustomRadialMenu]]
- [[WBP_HUD]]
- [[WBP_MenuArchive]]
- [[WBP_WeaponSelector]]

### E_AmmoType

- Path: /Game/ChuckContent/Systems/Weapons/Data/E_AmmoType.E_AmmoType

Values:
- NewEnumerator0 / None (index 0, value 0)
- NewEnumerator1 / Pistol (index 1, value 1)
- NewEnumerator2 / ShotGun (index 2, value 2)
- NewEnumerator3 / AssaultRifle (index 3, value 3)
- NewEnumerator4 / SniperRifle (index 4, value 4)
- NewEnumerator5 / GrenadeLauncher (index 5, value 5)
- NewEnumerator6 / RocketLauncher (index 6, value 6)
- E_MAX / E MAX (index 7, value 7)

Used by:

- [[ALS_ChuckBP]]
- [[BP_MasterPickUpSkeletalMesh]]
- [[BP_MasterPickUpStaticMesh]]
- [[S_WeaponData]]
- [[WBP_ArmorSelector]]
- [[WBP_HUD]]
- [[WBP_MenuArchive]]
- [[WBP_WeaponSelector]]

### E_ArmorSlot

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/E_ArmorSlot.E_ArmorSlot

Values:
- NewEnumerator0 / Head (index 0, value 0)
- NewEnumerator2 / Chest (index 1, value 1)
- NewEnumerator3 / Legs (index 2, value 2)
- NewEnumerator5 / Feet (index 3, value 3)
- NewEnumerator6 / Acessory (index 4, value 4)
- NewEnumerator1 / Accessory_1 (index 5, value 5)
- E_MAX / E MAX (index 6, value 6)

Used by:

- [[ALS_ChuckBP]]
- [[S_ArmorData]]
- [[WBP_ArmorSelector]]
- [[WBP_MenuArchive]]
- [[WBP_WeaponSelector]]

### E_CharactersAffiliates

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/E_CharactersAffiliates.E_CharactersAffiliates

Values:
- NewEnumerator0 / FAMILY (index 0, value 0)
- NewEnumerator3 / FRIENDS (index 1, value 1)
- NewEnumerator4 / BUY MORE (index 2, value 2)
- NewEnumerator1 / CIA (index 3, value 3)
- NewEnumerator5 / NSA (index 4, value 4)
- NewEnumerator2 / UNKNOWN (index 5, value 5)
- NewEnumerator6 / EX-CIA (index 6, value 6)
- NewEnumerator7 / RUSSIAN UNION (index 7, value 7)
- NewEnumerator8 / CHINA UNION (index 8, value 8)
- E_MAX / E MAX (index 9, value 9)

Used by:

- [[F_CharacterData]]
- [[WBP_TabIntersect_CharacterCard]]
- [[WBP_TabIntersect_CharacterSlot]]

### E_WheelActionType

- Path: /Game/ChuckContent/UI/WIDGET_MENU/2_MENU_RAPIDO/E_WheelActionType.E_WheelActionType

Values:
- NewEnumerator0 / ALS_Overlay (index 0, value 0)
- NewEnumerator1 / Consumable (index 1, value 1)
- E_MAX / E MAX (index 2, value 2)

Used by:

- [[S_WheelSlotData]]

### E_ObjectsCategory

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/E_ObjectsCategory.E_ObjectsCategory

Values:
- NewEnumerator8 / KEYS (index 0, value 0)
- NewEnumerator9 / CARDS (index 1, value 1)
- NewEnumerator10 / GADGET (index 2, value 2)
- NewEnumerator11 / DOCUMENTS (index 3, value 3)
- NewEnumerator12 / WEAPONS (index 4, value 4)
- NewEnumerator13 / INTERSECT (index 5, value 5)
- E_MAX / E MAX (index 6, value 6)

Used by:

- [[F_ObjectData]]

## Data Tables

### Text

- Row Struct: /Script/UMG.RichTextStyleRow
- Row Count: 2
- Path: /Game/ChuckContent/UI/files/Text/Text.Text

Fields:
- TextStyle: FTextBlockStyle

Rows:

- Default
- input

Referenced by:

- [[WBP_HUD]]
- [[WBP_Tip]]

### DT_Armor

- Row Struct: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/S_ArmorData.S_ArmorData
- Row Count: 19
- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Armor/DT_Armor.DT_Armor

Fields:
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Icon_36_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D*
- SlotType_37_6A80ABC24B17EFCD8135D98F80F1052A: TEnumAsByte<E_ArmorSlot>
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh*

Rows:

- A_AntiMunition_Jacket
- A_Glasses
- A_Mustache
- C_Informal_Suit_Jacket
- C_Shirt_NH
- C_Shirt_White
- C_Suit_Jacket
- C_T-Shirt_Tron
- F_Converse
- F_FlipFlop
- F_Suit_Shoes
- H_Hat_Mexican
- H_Hat_Military
- H_Hat_Simple
- H_Hat_Tactical
- L_Chino
- L_Jeans
- L_NH_Pants
- L_Suit_Pants

Referenced by:

- [[ALS_ChuckBP]]
- [[WBP_ArmorSelector]]
- [[WBP_MenuArchive]]
- [[WBP_WeaponSelector]]

### DT_Weapon

- Row Struct: /Game/ChuckContent/Systems/Weapons/Data/S_WeaponData.S_WeaponData
- Row Count: 14
- Path: /Game/ChuckContent/Systems/Weapons/Data/DT_Weapon.DT_Weapon

Fields:
- RowName_80_90C885E245FEA60369938EAC6E1FCB25: FName
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Weapon_Icon_67_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D*
- Weapon_Image_68_E0882141471F7B74AF02C2B8D100E2BB: UTexture2D*
- Technical_Info_55_96E6AFB44DBF5A6518FAD09002832322: FText
- SlotType_5_6A80ABC24B17EFCD8135D98F80F1052A: TEnumAsByte<E_WeaponSlot>
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh*
- ALS_OverlayState_16_84ACF4C94D2D7CFCD490FEA5E94AF136: TEnumAsByte<ALS_OverlayState>
- AttackMontage_41_1AC39D4A4FCDB6A8A8C8B5AD841AEDB9: UAnimMontage*
- ReloadMontage_42_70E4B0D745DD79FC954BD8BA6A7CFB18: UAnimMontage*
- HolsterSocket_22_F328E5D44A0493E4582BAC8E4D2C1D4B: FName
- HandSocket_24_89A03DC24973F91DA8FD2990B14E6F5E: FName
- BaseDamage_45_F289CC934ED7259D6122668BE2919E95: double
- DamageRadius_50_C83F28B2469DEBCA28C054A5B7E9388F: double
- TraceRadius_118_B0D837064F49FEDF1DD885AF55D54B84: double
- HitRange_58_53C8DCE547CE983F554D118DC7343869: double
- FireRate_85_D4AF7CD849600FE131B142B9432BB57A: double
- MaxMagazineCapacity_72_D0C5AAE44C4A57660DC71B8A4310666D: int32
- CurrentAmmoInMagazine_75_6C0D0FC744AA581F3583A7AD569F10A8: int32
- CurrentReservedAmmo_77_63C0F0BC400C091CCA9E73B44C19DA22: int32
- IsExplosive?_47_96E770804A49F8E44F6A818192D7A8BA: bool
- IsLoopHit?_60_4D6D7C754FE89BCD1232E1834B3976D1: bool
- IsEquipped?_82_B4C251E048F3C287DAC918BA8E28F5BC: bool
- MuzzleFX_88_427443474634B234F9B526A88FA4E232: UParticleSystem*
- TrailFX_94_7630F88044032394DFE85B8471864128: UParticleSystem*
- ImpactFX_97_3AF5DF2E4B6DB5A236B80096D754596A: UParticleSystem*
- ExplosionFX_98_C2595F5940DECE86B2E3EBB60841AE77: UParticleSystem*
- ProjectileClass_110_7D027F1643A36111E2428D94852EFD7D: UClass*
- bUsesProjectile_102_79A168584A8CB2ACF8A3B9A5AE4962E0: bool
- ProjectileMesh_105_746AFA884B46AC4393B21CB5A81561E8: UStaticMesh*
- ProjectileSpeed_108_AF0BF6D24C5C79648E94E8A1524BC6D5: double
- AmmoType_115_D22F449C48769E5D871EEC991DAEE4F4: TEnumAsByte<E_AmmoType>

Rows:

- AssaultRifleA
- AssaultRifleB
- GrenadeLauncherA
- GrenadeLauncherB
- KnifeA
- KnifeB
- PistolA
- PistolB
- RocketLauncherA
- RocketLauncherB
- ShotGunA
- ShotGunB
- SniperRifleA
- SniperRifleB

Referenced by:

- [[ALS_ChuckBP]]
- [[BP_MasterPickUpSkeletalMesh]]
- [[WBP_MenuArchive]]

### DT_CharacterData

- Row Struct: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/F_CharacterData.F_CharacterData
- Row Count: 20
- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/DT_CharacterData.DT_CharacterData

Fields:
- Subject_57_F26DCFA444362EC15F334C85DAEA606B: FText
- IsSubjectNameDiscovered?_72_371D046546FB4F151B82D68168F2F5D5: bool
- Icon_29_865610B04845107E08744FBEB7FC7FD1: UTexture2D*
- IsIconDiscovered?_32_209FFF6B4CD855BA7C6A10894DEA7A21: bool
- Aka_58_11C4F9654352996678422B9E4D637A62: FText
- IsAkaDiscovered?_73_4E6DBC3649A1AD2E07DEB6AE588F77AE: bool
- Nationality_59_D0C389D540DE4A29510B19AD186CEF6C: FText
- IsNationalityDiscovered?_80_61BF9CCF4A21C5B9CC328F8EE970DC62: bool
- PlaceOfBirth_60_C9F21F254055CCC9FC647190AFFBE29D: FText
- IsPlaceOfBirthDiscovered?_81_DE78335044A487316282FE9904C3B960: bool
- History_1_91_C9E22C80474D28C95371D7B98582444E: FText
- IsHistory_1Discovered?_82_063176C54D16E294CA28CBB3040D074B: bool
- History_2_93_66FAE1144ABD799E7AA9DE98739A621F: FText
- IsHistory_2Discovered?_96_CD7D83144FE95F9637C81793FCE6FB1A: bool
- History_3_101_C99699D14AA79209FB7902A2A7E96B70: FText
- IsHistory_3Discovered?_105_27A292884C51681A228FBFB161E3A2E7: bool
- History_4_102_6060F5E6460A81258273B4953E920724: FText
- IsHistory_4Discovered?_107_E4D8ABF749358EE19D24C18440F6B981: bool
- Affiliation_87_BFA5AACE4B04B0E4E281B39CAF247058: TArray<TEnumAsByte<E_CharactersAffiliates> >
- IsAffiliationDiscovered?_39_F8777F234098BF43FB42ADB9667E704C: bool
- Summary_71_F6C2334047FBE1B20E67D1B73C9FC9E8: FText
- IsSummaryDiscovered?_88_390CEFB9434AB82E648006BC83172F19: bool

Rows:

- BartowskiEllie
- BartowskiMary
- BartowskiStephen
- BeckmannDiane
- CaseyJohn
- GrimesMorgan
- NewRow
- NewRow_0
- NewRow_1
- NewRow_2
- NewRow_3
- NewRow_4
- NewRow_5
- NewRow_6
- NewRow_7
- NewRow_8
- NewRow_9
- TuckerMichael
- WalkerSarah
- WoodcombDevon

Referenced by:

- [[WBP_MenuArchive]]

### DT_ObjectsData

- Row Struct: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/F_ObjectData.F_ObjectData
- Row Count: 6
- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Intersect/Data/DT_ObjectsData.DT_ObjectsData

Fields:
- Name_27_F26DCFA444362EC15F334C85DAEA606B: FText
- Category_38_BFA5AACE4B04B0E4E281B39CAF247058: TArray<TEnumAsByte<E_ObjectsCategory> >
- Description_37_F6C2334047FBE1B20E67D1B73C9FC9E8: FText
- Icon_29_865610B04845107E08744FBEB7FC7FD1: UTexture2D*
- IsNameDiscovered?_18_371D046546FB4F151B82D68168F2F5D5: bool
- IsAliasDiscovered?_20_4E6DBC3649A1AD2E07DEB6AE588F77AE: bool
- IsCategoryDiscovered?_30_F8777F234098BF43FB42ADB9667E704C: bool
- IsDescriptionDiscovered?_25_390CEFB9434AB82E648006BC83172F19: bool
- IsIconDiscovered?_32_209FFF6B4CD855BA7C6A10894DEA7A21: bool

Rows:

- Governor
- IntersectCube1.0
- IntersectCube2.0
- IntersectCube3.0
- IntersectGlasses
- KeyCard

Referenced by:

- Nessuno rilevato.

### DT_Items

- Row Struct: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Inventory/S_ItemsData.S_ItemsData
- Row Count: 1
- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Inventory/DT_Items.DT_Items

Fields:
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Icon_36_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D*
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh*
- Description_40_D1E175F4454CD0D995978B97126F49C4: FText

Rows:

- Torch

Referenced by:

- Nessuno rilevato.

### DT_Consumable

- Row Struct: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Inventory/S_ConsumableData.S_ConsumableData
- Row Count: 2
- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Inventory/DT_Consumable.DT_Consumable

Fields:
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Icon_36_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D*
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh*
- Description_40_2423C9824F4F4F44EF95D78C53E0E886: FText

Rows:

- Bandages
- Sandwich

Referenced by:

- Nessuno rilevato.

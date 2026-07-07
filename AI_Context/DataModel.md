# Data Model

## Structs

### ALS_ComponentAndTransform

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/ALS_ComponentAndTransform.ALS_ComponentAndTransform

Fields:
- Transform_8_5A922B8141278287C6E895A0DBC17B89: FTransform = (Rotation=(X=0.000000,Y=-0.000000,Z=0.000000,W=1.000000),Translation=(X=0.000000,Y=0.000000,Z=0.000000),Scale3D=(X=1.000000,Y=1.000000,Z=1.000000))
- Component_11_74DA46FC4578E87978977783DBA2F302: UPrimitiveComponent* = None

Used by:

- [[ALS_BaseCharacterBP]]
- [[ALS_ChuckBP]]
- [[ALS_MacroLibrary]]

### MovementSettings

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/MovementSettings.MovementSettings

Fields:
- WalkSpeed_40_9AD737B14B8BC378F924E890E018B5B0: float = 0.000000
- RunSpeed_39_7397773A4A46B563F765429BD6A2DDE8: float = 0.000000
- SprintSpeed_38_6123675A40931BD70D4CF18D9A2A1C4C: float = 0.000000
- MovementCurve_51_FDDCE64149CA0F8A553745BEA0FEE53E: UCurveVector* = None
- RotationRateCurve_52_73FA146B4B31FF205DE8E1BBFA8800F6: UCurveFloat* = None

Used by:

- [[ALS_BaseCharacterBP]]
- [[MovementModelTable]]
- [[MovementSettings_Stance]]
- [[MovementSettings_State]]

### MovementSettings_Stance

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/MovementSettings_Stance.MovementSettings_Stance

Fields:
- Standing_12_291919F34C61D6D2C253D3B80934D9D2: FMovementSettings = (WalkSpeed_40_9AD737B14B8BC378F924E890E018B5B0=0.000000,RunSpeed_39_7397773A4A46B563F765429BD6A2DDE8=0.000000,SprintSpeed_38_6123675A40931BD70D4CF18D9A2A1C4C=0.000000,MovementCurve_51_FDDCE64149CA0F8A553745BEA0FEE53E=None,RotationRateCurve_52_73FA146B4B31FF205DE8E1BBFA8800F6=None)
- Crouching_14_DEF8FDDA4324E7EF87C9DE8D07831456: FMovementSettings = (WalkSpeed_40_9AD737B14B8BC378F924E890E018B5B0=0.000000,RunSpeed_39_7397773A4A46B563F765429BD6A2DDE8=0.000000,SprintSpeed_38_6123675A40931BD70D4CF18D9A2A1C4C=0.000000,MovementCurve_51_FDDCE64149CA0F8A553745BEA0FEE53E=None,RotationRateCurve_52_73FA146B4B31FF205DE8E1BBFA8800F6=None)

Used by:

- [[ALS_BaseCharacterBP]]
- [[MovementSettings_State]]

### MovementSettings_State

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/MovementSettings_State.MovementSettings_State

Fields:
- VelocityDirection_17_291919F34C61D6D2C253D3B80934D9D2: FMovementSettings_Stance = (Standing_12_291919F34C61D6D2C253D3B80934D9D2=(WalkSpeed_40_9AD737B14B8BC378F924E890E018B5B0=0.000000,RunSpeed_39_7397773A4A46B563F765429BD6A2DDE8=0.000000,SprintSpeed_38_6123675A40931BD70D4CF18D9A2A1C4C=0.000000,MovementCurve_51_FDDCE64149CA0F8A553745BEA0FEE53E=None,RotationRateCurve_52_73FA146B4B31FF205DE8E1BBFA8800F6=None),Crouching_14_DEF8FDDA4324E7EF87C9DE8D07831456=(WalkSpeed_40_9AD737B14B8BC378F924E890E018B5B0=0.000000,RunSpeed_39_7397773A4A46B563F765429BD6A2DDE8=0.000000,SprintSpeed_38_6123675A40931BD70D4CF18D9A2A1C4C=0.000000,MovementCurve_51_FDDCE64149CA0F8A553745BEA0FEE53E=None,RotationRateCurve_52_73FA146B4B31FF205DE8E1BBFA8800F6=None))
- LookingDirection_18_DEF8FDDA4324E7EF87C9DE8D07831456: FMovementSettings_Stance = (Standing_12_291919F34C61D6D2C253D3B80934D9D2=(WalkSpeed_40_9AD737B14B8BC378F924E890E018B5B0=0.000000,RunSpeed_39_7397773A4A46B563F765429BD6A2DDE8=0.000000,SprintSpeed_38_6123675A40931BD70D4CF18D9A2A1C4C=0.000000,MovementCurve_51_FDDCE64149CA0F8A553745BEA0FEE53E=None,RotationRateCurve_52_73FA146B4B31FF205DE8E1BBFA8800F6=None),Crouching_14_DEF8FDDA4324E7EF87C9DE8D07831456=(WalkSpeed_40_9AD737B14B8BC378F924E890E018B5B0=0.000000,RunSpeed_39_7397773A4A46B563F765429BD6A2DDE8=0.000000,SprintSpeed_38_6123675A40931BD70D4CF18D9A2A1C4C=0.000000,MovementCurve_51_FDDCE64149CA0F8A553745BEA0FEE53E=None,RotationRateCurve_52_73FA146B4B31FF205DE8E1BBFA8800F6=None))
- Aiming_21_D7B17FD043E721735EF6CCA049CD9E66: FMovementSettings_Stance = (Standing_12_291919F34C61D6D2C253D3B80934D9D2=(WalkSpeed_40_9AD737B14B8BC378F924E890E018B5B0=0.000000,RunSpeed_39_7397773A4A46B563F765429BD6A2DDE8=0.000000,SprintSpeed_38_6123675A40931BD70D4CF18D9A2A1C4C=0.000000,MovementCurve_51_FDDCE64149CA0F8A553745BEA0FEE53E=None,RotationRateCurve_52_73FA146B4B31FF205DE8E1BBFA8800F6=None),Crouching_14_DEF8FDDA4324E7EF87C9DE8D07831456=(WalkSpeed_40_9AD737B14B8BC378F924E890E018B5B0=0.000000,RunSpeed_39_7397773A4A46B563F765429BD6A2DDE8=0.000000,SprintSpeed_38_6123675A40931BD70D4CF18D9A2A1C4C=0.000000,MovementCurve_51_FDDCE64149CA0F8A553745BEA0FEE53E=None,RotationRateCurve_52_73FA146B4B31FF205DE8E1BBFA8800F6=None))

Used by:

- [[ALS_BaseCharacterBP]]
- [[MovementModelTable]]

### Mantle_Asset

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/Mantle_Asset.Mantle_Asset

Fields:
- AnimMontage_42_63D6D9044A5DAB0EFBDC858CD9E37736: UAnimMontage* = None
- PositionCorrectionCurve_43_0A4924AE48051202994680A7CE2D2C3A: UCurveVector* = None
- StartingOffset_30_FA0FF9D34F3BA3C50CF7C3928E516172: FVector = (X=0.000000,Y=0.000000,Z=0.000000)
- LowHeight_21_5CC2462A4191A12ECA9BDE85FA26C424: float = 0.000000
- LowPlayRate_37_391A50444B0AD0F7DD66A9BE9C6C65CA: float = 0.000000
- LowStartPosition_22_17AF0D8346D9E966FE520FB93F149B66: float = 0.000000
- HighHeight_23_8A8982FC42C3B6CDF79429B8675C86D9: float = 0.000000
- HighPlayRate_39_7ABB38D5459C2FE20D6A24AB7820B2FD: float = 0.000000
- HighStartPosition_24_D005813041B0EAEEB90490A469911497: float = 0.000000

Used by:

- [[ALS_BaseCharacterBP]]
- [[ALS_ChuckBP]]

### Mantle_Params

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/Mantle_Params.Mantle_Params

Fields:
- AnimMontage_24_3C1AEF894F90C77357FC01B1216DD889: UAnimMontage* = None
- PositionCorrectionCurve_25_716DDA5E44F540C50DA005B54E95AB0F: UCurveVector* = None
- StartingPosition_15_6F68E2244B632497DCA448A29CBDA0C8: float = 0.000000
- PlayRate_13_BBABD3264A1E44D275287FAE4C6D5556: float = 0.000000
- StartingOffset_10_381585D949B08D9A56D088A73A78B31B: FVector = (X=0.000000,Y=0.000000,Z=0.000000)

Used by:

- [[ALS_BaseCharacterBP]]

### Mantle_TraceSettings

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/Mantle_TraceSettings.Mantle_TraceSettings

Fields:
- MaxLedgeHeight_15_DC0D8FBF4C01FDE39D0AFDB1B04955A8: float = 0.000000
- MinLedgeHeight_14_857E2CDE423BEE7929567D8802243370: float = 0.000000
- ReachDistance_2_B3C154AA46EBFD9C1E67EB8DFBB7010E: float = 0.000000
- ForwardTraceRadius_9_C1A792084D8AAADBD22D8F8DE31A3A1C: float = 0.000000
- DownwardTraceRadius_12_7FE8C297416A916F74A892B85131B1BC: float = 0.000000

Used by:

- [[ALS_BaseCharacterBP]]

### AnimCurveCreationData

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/AnimModifiers/AnimCurveCreationData.AnimCurveCreationData

Fields:
- FrameNumber_2_BD15521446ADA77ADFD3CE88F52494A7: int32 = 0
- CurveValue_5_993AE0BE448F0E6CAD79769196535161: float = 0.000000

Used by:

- [[AnimCurveCreationParams]]
- [[Create_Curves]]

### AnimCurveCreationParams

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/AnimModifiers/AnimCurveCreationParams.AnimCurveCreationParams

Fields:
- CurveName_2_2BF8697245BD9A3A0827EDA874ECC1EC: FName = None
- KeyEachFrame_14_33D77EF046856C9C56BD8285457F89C8: bool = False
- Keys_12_82CD3EEB4393EF861DB5BBB5CD020AD2: TArray<FAnimCurveCreationData>

Used by:

- [[Create_Curves]]

### DynamicMontageParams

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/DynamicMontageParams.DynamicMontageParams

Fields:
- Animation_2_5E5C122A46BA0311400556A423FC05D0: UAnimSequenceBase* = None
- BlendInTime_10_1C5E8446412E51FFA0B03AB8BD32E6E8: float = 0.000000
- BlendOutTime_12_79DFD9804491A7DF0813EFA923002F9C: float = 0.000000
- PlayRate_5_4724216C43D83EADF735F0AFEE9947EB: float = 0.000000
- StartTime_7_3C5D7A3849D194E10AB51CA0344EBC8D: float = 0.000000

Used by:

- [[ALS_AnimBP]]

### LeanAmount

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/LeanAmount.LeanAmount

Fields:
- LR_17_ADF99333493B27F5B49BA89100DC4C05: float = 0.000000
- FB_15_297866804FB14F4B81FB4A976A7F57D1: float = 0.000000

Used by:

- [[ALS_AnimBP]]

### RotateInPlace_Asset

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/RotateInPlace_Asset.RotateInPlace_Asset

Fields:
- Animation_2_7BA2980D4E85CC9E320EB98B57C73B3A: UAnimSequenceBase* = None
- SlotName_5_73864C9E40AE26D9F294038C7099722B: FName = None
- SlowTurnRate_9_47A596764C9AFE145D75C49448F776A8: float = 90.000000
- FastTurnRate_17_566E906643D9AD8B150F87B98BBF88BB: float = 90.000000
- SlowPlayRate_16_1F78888146721190E66721BAA545F229: float = 1.000000
- FastPlayRate_18_730EF8A04D92C6D5D014CFBF34A93F2A: float = 1.000000

Used by:

- [[ALS_AnimBP]]

### TurnInPlace_Asset

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/TurnInPlace_Asset.TurnInPlace_Asset

Fields:
- Animation_2_7BA2980D4E85CC9E320EB98B57C73B3A: UAnimSequenceBase* = None
- AnimatedAngle_11_0BE5A89E455AEBE851DAA49A1FCA81A5: float = 0.000000
- SlotName_5_73864C9E40AE26D9F294038C7099722B: FName = None
- PlayRate_8_47A596764C9AFE145D75C49448F776A8: float = 1.000000
- ScaleTurnAngle_14_ED8450744340CD92E19052A9E8766866: bool = True

Used by:

- [[ALS_AnimBP]]

### VelocityBlend

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/VelocityBlend.VelocityBlend

Fields:
- F_3_2154ABAD4BD15DAC904154B63D704219: float = 0.000000
- B_5_0A0855774CB13BB3E4B0A6847E7154F6: float = 0.000000
- L_8_DFEBB8584D28F158D2562CA60EB07B6D: float = 0.000000
- R_9_79E6E09B4A52B442B9FE6DB7192CFBEE: float = 0.000000

Used by:

- [[ALS_AnimBP]]

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
- [[BP_WeaponMaster]]
- [[DT_Weapon]]
- [[WBP_ArmorSelector]]
- [[WBP_CustomRadialMenu]]
- [[WBP_HUD]]
- [[WBP_MenuArchive]]
- [[WBP_SelectorButton]]
- [[WBP_WeaponSelector]]

### OverlayStateButtonParams

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Blueprints/UI/OverlayStateButtonParams.OverlayStateButtonParams

Fields:
- Widget_5_4F22C4EE49421E434A46FE9803893231: UOverlayStateButton_C* = None
- State_9_BAF3D4CC4EE0E7CCD650F3B4963A2A65: TEnumAsByte<ALS_OverlayState> = NewEnumerator0

Used by:

- [[OverlayStateSwitcher]]

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

### S_ConsumableData

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Inventory/S_ConsumableData.S_ConsumableData

Fields:
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Icon_36_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D* = None
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh* = None
- Description_40_2423C9824F4F4F44EF95D78C53E0E886: FText

Used by:

- [[DT_Consumable]]

### S_ItemsData

- Path: /Game/ChuckContent/UI/WIDGET_MENU/1_MENU_ARCHIVE/Equipment/Inventory/S_ItemsData.S_ItemsData

Fields:
- Name_2_E0EAA52E4A6C9440143913B681C970CA: FText
- Icon_36_A8272ED24A449CC6084C88B1C8FF3C5A: UTexture2D* = None
- SkeletalMesh_13_98296F844317640264908E9852ED5A07: USkeletalMesh* = None
- Description_40_D1E175F4454CD0D995978B97126F49C4: FText

Used by:

- [[DT_Items]]

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

### CameraSettings

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/CameraSettings.CameraSettings

Fields:
- TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5: float = 0.000000
- SocketOffset_5_34B1F2644290538776D422A028DE6B30: FVector = (X=0.000000,Y=0.000000,Z=0.000000)
- LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA: float = 0.000000
- RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9: float = 0.000000
- DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB: bool = True

Used by:

- [[CameraSettings_Gait]]
- [[CameraSettings_State]]

### CameraSettings_Gait

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/CameraSettings_Gait.CameraSettings_Gait

Fields:
- Walking_12_B01E68F849F391C65F3682BD9C3219B9: FCameraSettings = (TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True)
- Running_15_43F84DDD4051F13684E292BA8ED0A033: FCameraSettings = (TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True)
- Sprinting_16_57A65D1848C2431ECEF41CB8DD648DBB: FCameraSettings = (TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True)
- Crouching_19_E0B6E9C74E44EAD9D33C5E94C9BBBAB2: FCameraSettings = (TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True)

Used by:

- [[CameraSettings_State]]

### CameraSettings_State

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/CameraSettings_State.CameraSettings_State

Fields:
- VelocityDirection_27_B01E68F849F391C65F3682BD9C3219B9: FCameraSettings_Gait = (Walking_12_B01E68F849F391C65F3682BD9C3219B9=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True),Running_15_43F84DDD4051F13684E292BA8ED0A033=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True),Sprinting_16_57A65D1848C2431ECEF41CB8DD648DBB=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True),Crouching_19_E0B6E9C74E44EAD9D33C5E94C9BBBAB2=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True))
- LookingDirection_26_6FC3380844EEF685DB8BFAADFD94A1E0: FCameraSettings_Gait = (Walking_12_B01E68F849F391C65F3682BD9C3219B9=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True),Running_15_43F84DDD4051F13684E292BA8ED0A033=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True),Sprinting_16_57A65D1848C2431ECEF41CB8DD648DBB=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True),Crouching_19_E0B6E9C74E44EAD9D33C5E94C9BBBAB2=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True))
- Aiming_31_C883256643AA6F168F52EAAD547703EE: FCameraSettings_Gait = (Walking_12_B01E68F849F391C65F3682BD9C3219B9=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True),Running_15_43F84DDD4051F13684E292BA8ED0A033=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True),Sprinting_16_57A65D1848C2431ECEF41CB8DD648DBB=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True),Crouching_19_E0B6E9C74E44EAD9D33C5E94C9BBBAB2=(TargetArmLength_2_4CF495804C45F21B7F9C8589345B0FE5=0.000000,SocketOffset_5_34B1F2644290538776D422A028DE6B30=(X=0.000000,Y=0.000000,Z=0.000000),LagSpeed_8_BDB960A74493A95BEF9A90B3C8C577BA=0.000000,RotationLagSpeed_10_B01E68F849F391C65F3682BD9C3219B9=0.000000,DoCollisionTest_12_1EC75993495EA471473E328B8784A5DB=True))

Used by:

- Nessuno rilevato.

## Enums

### GroundedEntryState

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/GroundedEntryState.GroundedEntryState

Values:
- NewEnumerator0 / None (index 0, value 0)
- NewEnumerator2 / Roll (index 1, value 1)
- GroundedEntryState_MAX / Grounded Entry State MAX (index 2, value 2)

Used by:

- [[ALS_Animation_BPI]]
- [[ALS_AnimBP]]
- [[GroundedEntryState_AnimNotify]]

### ALS_Gait

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_Gait.ALS_Gait

Values:
- NewEnumerator0 / Walking (index 0, value 0)
- NewEnumerator1 / Running (index 1, value 1)
- NewEnumerator2 / Sprinting (index 2, value 2)
- ALS_MAX / ALS MAX (index 3, value 3)

Used by:

- [[ALS_AnimBP]]
- [[ALS_BaseCharacterBP]]
- [[ALS_Character_BPI]]
- [[ALS_HUD]]
- [[ALS_PlayerCameraBehavior]]
- [[EarlyBlendOut_NotifyState]]
- [[MovementAction_NotifyState]]
- [[OverlayStateSwitcher]]

### ALS_MovementAction

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_MovementAction.ALS_MovementAction

Values:
- NewEnumerator4 / None (index 0, value 0)
- NewEnumerator0 / LowMantle (index 1, value 1)
- NewEnumerator1 / HighMantle (index 2, value 2)
- NewEnumerator2 / Rolling (index 3, value 3)
- NewEnumerator3 / GettingUp (index 4, value 4)
- ALS_MAX / ALS MAX (index 5, value 5)

Used by:

- [[ALS_AnimBP]]
- [[ALS_BaseCharacterBP]]
- [[ALS_Character_BPI]]
- [[ALS_HUD]]
- [[ALS_PlayerCameraBehavior]]
- [[EarlyBlendOut_NotifyState]]
- [[MovementAction_NotifyState]]
- [[OverlayStateSwitcher]]

### ALS_MovementState

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_MovementState.ALS_MovementState

Values:
- NewEnumerator0 / None (index 0, value 0)
- NewEnumerator1 / Grounded (index 1, value 1)
- NewEnumerator2 / In Air (index 2, value 2)
- NewEnumerator4 / Mantling (index 3, value 3)
- NewEnumerator3 / Ragdoll (index 4, value 4)
- ALS_MAX / ALS MAX (index 5, value 5)

Used by:

- [[ALS_AnimBP]]
- [[ALS_BaseCharacterBP]]
- [[ALS_Character_BPI]]
- [[ALS_HUD]]
- [[ALS_PlayerCameraBehavior]]
- [[EarlyBlendOut_NotifyState]]
- [[MovementAction_NotifyState]]
- [[OverlayStateSwitcher]]

### ALS_OverlayState

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_OverlayState.ALS_OverlayState

Values:
- NewEnumerator0 / Default (index 0, value 0)
- NewEnumerator12 / Masculine (index 1, value 1)
- NewEnumerator13 / Feminine (index 2, value 2)
- NewEnumerator14 / Injured (index 3, value 3)
- NewEnumerator15 / HandsTied (index 4, value 4)
- NewEnumerator1 / Rifle (index 5, value 5)
- NewEnumerator5 / Pistol 1H (index 6, value 6)
- NewEnumerator10 / Pistol 2H (index 7, value 7)
- NewEnumerator6 / Bow (index 8, value 8)
- NewEnumerator7 / Torch (index 9, value 9)
- NewEnumerator8 / Binoculars (index 10, value 10)
- NewEnumerator9 / Box (index 11, value 11)
- NewEnumerator11 / Barrel (index 12, value 12)
- NewEnumerator17 / Knife (index 13, value 13)
- NewEnumerator18 / Fists (index 14, value 14)
- ALS_MAX / ALS MAX (index 15, value 15)

Used by:

- [[ALS_AnimBP]]
- [[ALS_BaseCharacterBP]]
- [[ALS_Character_BPI]]
- [[ALS_ChuckBP]]
- [[ALS_HUD]]
- [[ALS_PlayerCameraBehavior]]
- [[BP_MasterPickUpSkeletalMesh]]
- [[BP_WeaponMaster]]
- [[EarlyBlendOut_NotifyState]]
- [[MovementAction_NotifyState]]
- [[OverlayStateButtonParams]]
- [[OverlayStateSwitcher]]
- [[S_WeaponData]]
- [[S_WheelSlotData]]
- [[WBP_MenuArchive]]

### ALS_RotationMode

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_RotationMode.ALS_RotationMode

Values:
- NewEnumerator0 / VelocityDirection (index 0, value 0)
- NewEnumerator1 / LookingDirection (index 1, value 1)
- NewEnumerator3 / Aiming (index 2, value 2)
- ALS_MAX / ALS MAX (index 3, value 3)

Used by:

- [[ALS_AnimBP]]
- [[ALS_BaseCharacterBP]]
- [[ALS_Character_BPI]]
- [[ALS_ChuckBP]]
- [[ALS_HUD]]
- [[ALS_PlayerCameraBehavior]]
- [[EarlyBlendOut_NotifyState]]
- [[MovementAction_NotifyState]]
- [[OverlayStateSwitcher]]

### ALS_Stance

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_Stance.ALS_Stance

Values:
- NewEnumerator0 / Standing (index 0, value 0)
- NewEnumerator1 / Crouching (index 1, value 1)
- ALS_MAX / ALS MAX (index 2, value 2)

Used by:

- [[ALS_AnimBP]]
- [[ALS_BaseCharacterBP]]
- [[ALS_Character_BPI]]
- [[ALS_HUD]]
- [[ALS_PlayerCameraBehavior]]
- [[EarlyBlendOut_NotifyState]]
- [[MovementAction_NotifyState]]
- [[OverlayStateSwitcher]]

### ALS_ViewMode

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/ALS_ViewMode.ALS_ViewMode

Values:
- NewEnumerator0 / ThirdPerson (index 0, value 0)
- NewEnumerator1 / FirstPerson (index 1, value 1)
- ALS_MAX / ALS MAX (index 2, value 2)

Used by:

- [[ALS_AnimBP]]
- [[ALS_BaseCharacterBP]]
- [[ALS_Character_BPI]]
- [[ALS_HUD]]
- [[ALS_PlayerCameraBehavior]]
- [[EarlyBlendOut_NotifyState]]
- [[MovementAction_NotifyState]]
- [[OverlayStateSwitcher]]

### MantleType

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/MantleType.MantleType

Values:
- NewEnumerator1 / HighMantle (index 0, value 0)
- NewEnumerator0 / LowMantle (index 1, value 1)
- NewEnumerator2 / FallingCatch (index 2, value 2)
- MantleType_MAX / Mantle Type MAX (index 3, value 3)

Used by:

- [[ALS_BaseCharacterBP]]
- [[ALS_ChuckBP]]

### FootstepType

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/FootstepType.FootstepType

Values:
- NewEnumerator0 / Step (index 0, value 0)
- NewEnumerator4 / Walk/Run (index 1, value 1)
- NewEnumerator7 / Jump (index 2, value 2)
- NewEnumerator8 / Land (index 3, value 3)
- FootstepType_MAX / Footstep Type MAX (index 4, value 4)

Used by:

- [[Footstep_AnimNotify]]

### HipsDirection

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/HipsDirection.HipsDirection

Values:
- NewEnumerator0 / F (index 0, value 0)
- NewEnumerator1 / B (index 1, value 1)
- NewEnumerator2 / RF (index 2, value 2)
- NewEnumerator3 / RB (index 3, value 3)
- NewEnumerator4 / LF (index 4, value 4)
- NewEnumerator5 / LB (index 5, value 5)
- HipsDirection_MAX / Hips Direction MAX (index 6, value 6)

Used by:

- [[ALS_AnimBP]]

### MovementDirection

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/MovementDirection.MovementDirection

Values:
- NewEnumerator0 / Forward (index 0, value 0)
- NewEnumerator1 / Right (index 1, value 1)
- NewEnumerator2 / Left (index 2, value 2)
- NewEnumerator3 / Backward (index 3, value 3)
- MovementDirection_MAX / Movement Direction MAX (index 4, value 4)

Used by:

- [[ALS_AnimBP]]

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
- [[BP_WeaponMaster]]
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
- [[BP_WeaponMaster]]
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

### AnimFeatureExample

- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Enums/AnimFeatureExample.AnimFeatureExample

Values:
- NewEnumerator0 / Stride Blending (index 0, value 0)
- NewEnumerator1 / Additive Leaning (index 1, value 1)
- NewEnumerator2 / Sprint Impulse (index 2, value 2)
- AnimFeatureExample_MAX / Anim Feature Example MAX (index 3, value 3)

Used by:

- Nessuno rilevato.

## Data Tables

### MovementModelTable

- Row Struct: /Game/AdditionalContents/AdvancedLocomotionV4/Data/Structs/MovementSettings_State.MovementSettings_State
- Row Count: 3
- Path: /Game/AdditionalContents/AdvancedLocomotionV4/Data/DataTables/MovementModelTable.MovementModelTable

Fields:
- VelocityDirection_17_291919F34C61D6D2C253D3B80934D9D2: FMovementSettings_Stance
- LookingDirection_18_DEF8FDDA4324E7EF87C9DE8D07831456: FMovementSettings_Stance
- Aiming_21_D7B17FD043E721735EF6CCA049CD9E66: FMovementSettings_Stance

Rows:

- Normal
- Responsive
- Sluggish

Referenced by:

- [[ALS_BaseCharacterBP]]

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
- [[BP_WeaponMaster]]
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

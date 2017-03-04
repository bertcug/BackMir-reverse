## GamePlayer
- GamePlayer struc ; (sizeof=0xABC, align=0x4, copyof_2029)

| offset | member | size/type |
|--------|--------|-----------|
| 00000000 | baseclass_0 | GameOtherPlayer |
| 00000794 | m_equipAttrib | PlayerEquipAttrib |
| 000007C8 | m_pSprHum | dd |
| 000007CC | m_pSprHair | dd |
| 000007D0 | m_pSprWeapon | dd |
| 000007D4 | m_pSprState | dd |
| 000007D8 | m_pSprMgc | dd |
| 000007DC | m_bag | PlayerBag |
| 00000814 | m_indexs | PlayerTexIndexTable |
| 0000081A | - | db | undefined |
| 0000081B | - | db | undefined |
| 0000081C | m_atkTarget | dd |
| 00000820 | m_nMapID | dd |
| 00000824 | m_stMagicDetail | MagicDetail[25] |
| 000009B4 | m_xInputMap | `std::map<char,MagicDetail*,std::less<char>,std::allocator<std::pair<char const ,MagicDetail *> > >` |
| 000009D4 | m_xAccInputMap |` std::map<char,MagicDetail *,std::less<char>,std::allocator<std::pair<char const ,MagicDetail *> > > ` |
| 000009F4 | m_bIsLocked | db |
| 000009F5 |-|                db |undefined|
| 000009F6 |-|                db |undefined|
| 000009F7 |-|                db |undefined|
| 000009F8 | m_dwLockType | dd |
| 000009FC | m_dwLastLockedTime | dd |
| 00000A00 | m_bIsWalkLocked | db |
| 00000A01 |                | db |  undefined |
| 00000A02 |				| db | undefined |
| 00000A03 |                | db | undefined |
| 00000A04 | m_dwLastLockedWalkTime | dd | |
| 00000A08 | m_pMgcTarget |   dd | offset
| 00000A0C | m_dwLastUseMagicTime | dd |
| 00000A10 | m_nSaveIndex | dd |
| 00000A14 | m_szSaveName | char[20] |
| 00000A28 | m_xMgcHistory | `std::map<unsigned long,unsigned long,std::less<unsigned long>,std::allocator<std::pair<unsigned long const ,unsigned long> > >` |
| 00000A48 | m_xDrugCoolDown | CoolDownController |
| 00000A68 | m_xQuest | QuestContext |
| 00000A7C | m_szNameCopy | char[20] |
| 00000A90 | m_uUID | dd |
| 00000A94 | m_nAccMagicID | dd |
| 00000A98 | m_bUsingPreLock | db |
| 00000A99 |                | db | undefined |
| 00000A9A |                | db | undefined |
| 00000A9B |                | db | undefined |
| 00000A9C | m_xNormalAtkRand | RandGenerator |
| 00000AA0 | m_dwPreCalcNormalAttackEffMask | dd |
| 00000AA4 | m_bEnableLieHuo | db |
| 00000AA5 | m_bEnableSuperLieHuo | db |
| 00000AA6 | m_bEnableBanYue | db |
| 00000AA7 | m_bEnableCiSha |  db |
| 00000AA8 | m_bEnableKtSword | db |
| 00000AA9 |                | db | undefined |
| 00000AAA |                | db | undefined |
| 00000AAB |                | db | undefined |
| 00000AAC | m_nWaitServerRspType | dd |
| 00000AB0 | m_dwWaitServerRspTimeoutTime | dd |
| 00000AB4 | m_nDonateLeft |  dd |
| 00000AB8 | m_bRequestSmallQuit | db |
| 00000AB9 |               |  db | undefined |
| 00000ABA |               | db | undefined |
| 00000ABB |               |  db | undefined |

## GameOtherPlayer
- GameOtherPlayer struc (sizeof=0x794, align=0x4, copyof_1983)

| offset | member | size/type |
|--------|--------|-----------|
| 00000000 | baseclass_0 | GameObject |
| 000001E8 | m_equip | ItemAttrib[13] |
| 000006C8 | m_fDetect | dd |
| 000006CC | m_fMoveOffsetXTotal | dd |
| 000006D0 | m_fMoveOffsetYTotal | dd |
| 000006D4 | m_fLastUpdateSkill | dd |
| 000006D8 | m_fLastUpdateAttack |  dd |
| 000006DC | m_fLastUpdateDeath | dd |
| 000006E0 | m_fLastUpdateAttackNoWeapon | dd |
| 000006E4 | m_fLastUpdateAttackStop | dd |
| 000006E8 | m_fLastUpdateAttacked | dd |
| 000006EC | m_fLastUpdateMove dd |
| 000006F0 | m_eEffect | dd 4 dup |  enum MAGICEFFECT_TYPE |
| 00000700 | m_pMagicEffect  | dd |
| 00000704 | m_pEffectRender dd |
| 00000708 | m_bPlayOneStep |  db |
| 00000709 | m_bPlayTwoStep | db |
| 0000070A | m_bJob | db |
| 0000070B | db | undefined |
| 0000070C | m_dwLastAttackTime | dd |
| 00000710 | m_dwLastAttackStopTime | dd |
| 00000714 | m_dwLastAttackMode | dd |
| 00000718 | m_xHumStates | `std::list<MagicElement*,std::allocator<MagicElement *> >` |
| 00000734 | m_dwJinGangExpireTime | dd |
| 00000738 | m_nLieHuoSkillLevel | dd |
| 0000073C | m_nVipLevel | dd |
| 00000740 | m_dwLastNameColorChangeTime | dd |
| 00000744 | m_nLastNameColorIndex | dd |
| 00000748 | m_xSkillInfo | `std::map<unsigned long,unsigned long,std::less<unsigned long>,std::allocator<std::pair<unsigned long const ,unsigned long> > >` |
| 00000768 | m_stExtAttrib | ExtendHeroAttrib |
| 00000794 | GameOtherPlayer ends |

## GameObject
- GameObject struc (sizeof=0x1E8, align=0x4, copyof_1936)

| offset | member | size/type |
|--------|--------|-----------|
| 00000000 | baseclass_0 |     RenderObject |
| 00000028 | baseclass_28 |    PacketHandler |
| 00000030 | m_fPosx | dd |
| 00000034 | m_fPosy | dd |
| 00000038 | m_ptPos | tagPOINT |
| 00000040 | m_type  | dd | enum OBJECT_TYPE |
| 00000044 | m_drt   |        dd | enum PLAYER_DIRECTION |
| 00000048 | m_sex   |        dd | enum PLAYER_SEX |
| 0000004C | m_stat  |        dd | enum PLAYER_STATUS |
| 00000050 | m_preStat |      dd | enum PLAYER_STATUS |
| 00000054 | m_attrib  | ItemAttrib |
| 000000B4 | m_fLastStandTime | dd |
| 000000B8 | m_bRenderName | db |
| 000000B9 | m_bHurt |         db |
| 000000BA |          |      db | undefined |
| 000000BB |          |      db | undefined |
| 000000BC | m_nCurrentTextureIndex | dd |
| 000000C0 | m_nCurrentSelectIndex | dd |
| 000000C4 | m_rcSelectRect | tagRECT |
| 000000D4 | m_szSaying | dw[80] |
| 00000174 | m_fSayingTime |   dd |
| 00000178 | m_stSayingSize | tagSIZE |
| 00000180 | m_dwLineNumber | dd |
| 00000184 | m_dwSayingColor | dd |
| 00000188 | m_dwHumEffectFlag | dd |
| 0000018C | m_dwHumEffectTime | dd[7] |
| 000001A8 | m_pMaster | dd |
| 000001AC | m_szMasterName |  db[20] |
| 000001C0 | m_bTransparentMode | db |
| 000001C1 |              |  db | undefined |
| 000001C2 |             | db | undefined |
| 000001C3 |              |   db | undefined |
| 000001C4 | m_eRenderMode | dd | enum OBJECT_RENDER_MODE |
| 000001C8 | m_dwLastMoveTime | dd |
| 000001CC | m_xAttackNumberList | `std::list<EffectAttackNumber *,std::allocator<EffectAttackNumber *> >` |
| 000001E8 | GameObject | ends |

## ItemAttrib
- ItemAttrib      struc ; (sizeof=0x60, align=0x4, mappedto_958)

| member | offset | size|
|--------|--------|-----|
| 00000000 | id |  dd |
| 00000004 | name | char[20] |
| 00000018 | lucky | db |
| 00000019 | curse | db |
| 0000001A | hide  | db |
| 0000001B | accuracy | db |
| 0000001C | atkSpeed | db |
| 0000001D | atkPalsy | db |
| 0000001E | atkPois | db |
| 0000001F | moveSpeed | db |
| 00000020 | weight   | db |
| 00000021 | reqType | db |
| 00000022 | reqValue | db  |
| 00000023 | sex  | db |
| 00000024 | type | db |
| 00000025 |      | db | undefined |
| 00000026 | maxDC | dw |
| 00000028 | DC    | dw |
| 0000002A | maxAC | dw |
| 0000002C | AC    | dw |
| 0000002E | maxMAC | dw |
| 00000030 | MAC  | dw |
| 00000032 | maxSC | dw |
| 00000034 | SC    | dw |
| 00000036 | maxMC | dw |
| 00000038 | MC    | dw |
| 0000003A |       | db | undefined |
| 0000003B |       | db | undefined
| 0000003C | maxHP | dd |
| 00000040 | HP    | dd |
| 00000044 | maxMP | dd |
| 00000048 | MP    | dd |
| 0000004C | maxEXPR | dd |
| 00000050 | EXPR   | dd |
| 00000054 | level  | dw |
| 00000056 | extra  | dw |
| 00000058 | tex   |  dw |
| 0000005A | price | dw |
| 0000005C | tag | dd |
| 00000060 | ItemAttrib  ends |

## UserData
- UserData struc ; (sizeof=0x78, align=0x4, copyof_1460)

| offset | member | size/type |
|--------|--|------|----------|
| 00000000 | stAttrib | ItemAttrib  |
| 00000060 | wCoordX |  dw  |
| 00000062 | wCoordY |  dw  |
| 00000064 | wMapID  |  dw  |
| 00000066 | undefined | db |
| 00000067 | undefined | db |
| 00000068 | eServerState | dd  | enum USER_STATE |
| 0000006C | eGameState | dd | enum OBJECT_STATE |
| 00000070 | nDrt | dd |
| 00000074 | bJob | db |
| 00000075 | - | db | undefined |
| 00000076 |-| db |  undefined |
| 00000077 |-| db | undefined |

## PlayerEquipAttrib
- PlayerEquipAttrib struc ; (sizeof=0x34, align=0x4, copyof_1984)
| offset | member | size/type |
|--------|------|----------|
| 00000000 | nWeapon | dd |
| 00000004 | nCloth | dd |
| 00000008 | nNeck  | dd |
| 0000000C | nBrac  | dd[2] |
| 00000014 | nRing  | dd[2] |
| 0000001C | nHelm | dd |
| 00000020 | nMedal | dd |
| 00000024 | nGem   | dd |
| 00000028 | nShoe  | dd |
| 0000002C | nBelt  | dd |
| 00000030 | nHairStyle | dd |
| 00000034 | PlayerEquipAttrib ends |

## MagicDetail
- MagicDetail     struc ; (sizeof=0x10, align=0x4, copyof_1992)

| offset | member | size/type |
|--------|------|----------|
| 00000000 | cKey | db |
| 00000001 | cAccKey | db |
| 00000002 | db | undefined |
| 00000003 | db | undefined |
| 00000004 | szName | dd |
| 00000008 | dwTrain | dd |
| 0000000C | cLevel | db |
| 0000000D |        | db | undefined |
| 0000000E | wID | dw |
| 00000010 | MagicDetail ends |



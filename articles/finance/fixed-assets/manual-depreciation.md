---
title: Handvirkar afskriftir
description: Þessi grein veitir yfirlit yfir handvirka afskriftaraðferð.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3545b863f14ac9553563caa9b6e57443ea378536
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723196"
---
# <a name="manual-depreciation"></a>Handvirkar afskriftir

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir handvirka afskriftaraðferð.

Þegar afskriftarregla fyrir eignir er sett upp og valið er **handvirkt** í svæðinu **aðferð** í síðunni **afskriftarregla** ráðast afskriftir eignasem heyra undir þá afskriftarreglu af prósentunni sem færð er inn fyrir hvert bil í almanaksárinu. Bilin sem sett eru upp sem prósentur fyrir, eru bókuð samkvæmt gildinu sem valið er í á **tímabilstíðni** reit á **Almennt** flýtiflipa í **afskriftareglur** síðu. Hér er gildin sem hægt er að velja:

- Árlega
- Mánaðarlega
- Ársfjórðungslega
- Tvisvar á ári
- Daglega

Þegar bókunarbil eru valin, smellið á **handvirk röðun** og stillið prósentur fyrir hvert bókunarbil. Saman skilgreina handvirka röðunin og bókunarbilin afskriftarmagnið, eins og sýnt er í dæmunum hér að neðan. Handvirkar afskriftir eru alltaf reiknaðar sem prósenta af kaupverði. Handvirkar afskriftir fyrir prósentutölurnar sem færðar eru inn í bilin fyrir afskriftir þurfa ekki að vera samanlagt 100 prósent. Handvirkar afskriftir eru sveigjanlega afskriftaraðferð sem oft er notuð til að skilgreina óregluleg afskriftaregla í á **bækur** síða, eins og óreglubundnar afskriftir fyrir sérstakan tilgang (t.d. skattur).

## <a name="examples"></a>Dæmi
Kaupverð: 11.000,00 Væntanlegt rýrnunarvirði: 1.000,00 eftirfarandi tafla sýnir bilin og prósentutölurnar sem settar eru upp á í **Afskriftaregluáætlanir eigna** síðu.

| Númerabil | Prósenta |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

Afskriftirnar eftir tímabilum eru reiknaðar eins og sýnt er í eftirfarandi töflu.

|  Númerabil | Reiknuð upphæð árlegra afskrifta | Nettó bókfært verð við lok árs |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11.000 – 1.000) × 10% = 1.000                | 10.000 (11.000 – 1.000)                   |
| 2                | (11.000 – 1.000) × 50% = 5.000                | 5.000 (10.000 – 5.000)                    |
| 3                | (11.000 – 1.000) × 8% = 800                   | 4.200 (5.000 – 800)                       |

Ef valið er **mánaðarlega** í svæðinu **tímabilstíðni** seturðu upp 12 handvirk röðunarbil. Eftirfarandi tafla sýnir afskriftarupphæðir fyrir fyrstu tveggja tímabila.

| Bil | Afskriftarupphæð            |
|----------|--------------------------------|
| janúar  | (11.000 – 1.000) × 10% = 1.000 |
| febrúar | (11.000 – 1.000) × 50% = 5.000 |

Ef valið er <strong>Tvisvar á ári</strong> í *<strong><em>Tímabilstíðni</em>* reitnum</strong> eru tvö handvirk röðunarbil sett upp. Eftirfarandi tafla sýnir afskriftarupphæðir fyrir þessi tvö tímabila.

| Bil    | Afskriftarupphæð            |
|-------------|--------------------------------|
| 30. júní     | (11.000 – 1.000) × 10% = 1.000 |
| 31. desember | (11.000 – 1.000) × 50% = 5.000 |

Samtala fyrir prósentutölurnar fyrir öll bilin þurfa ekki að vera 100. Hins vegar munu berast skilaboð ef gildið í **heildarprósenta** á síðunni **Afskriftaregluáætlanir eigna** er ekki **100**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

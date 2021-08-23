---
title: (ER) Flytja inn skilgreiningar úr RCS
description: Þetta efni gefur upplýsingar um hvernig notandi getur flutt inn nýja útgáfu af ER-skilgreiningum úr RCS.
author: NickSelin
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5674c418baaac7817c27780e2f0137ce6e7137eb3f1665f768ad843cc5b3114
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720785"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Flytja inn skilgreiningar úr RCS

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Regulatory Configuration Services (RCS). Í þessu dæmi munt þú velja útgáfu af ER-skilgreiningum sem hafa verið skilgreindar í RCS-tilviki og flytja hana inn í núverandi tilvik fyrir sýnisfyrirtækið, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningunum er deilt milli fyrirtækja. Til að ljúka þessum skrefum verður fyrst að ljúka skrefunum í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md). Til að ljúka þessum skrefum verður þú einnig að hafa aðgang að RCS-tilviki sem inniheldur að minnsta kosti eina ER-skilgreiningu í annaðhvort stöðunni **Lokið** eða **Deilt**.

1. Farðu í **Fyrirtækisstjórnun** > **Vinnusvæði** > **Rafræn skýrslugerð**. 
2. Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**. Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md). 
3. Ef engu RCS-umhverfi er úthlutað fyrir fyrirtækið skaltu velja ytri tengilinn **Regulatory services – skilgreining** og fylgja svo leiðbeiningunum til að úthluta RCS-umhverfi. 
4. Veljið **Rafrænar skýrslugerðarfæribreytur**. 
5. Veljið flipann **RCS**. 
6. Ef RCS-umhverfinu hefur þegar verið úthlutað á fyrirtækið skaltu nota vefslóðirnar sem eru á síðunni til að fá aðgang að því. 
7. Lokið síðunni. 

## <a name="register-a-new-er-repository"></a>Skráðu nýja ER-gagnasafn. 
1. Í listanum skal merkja valda línu. 
2. Veldu veituna Litware, Inc. 
3. Veldu Geymslur. 
4. Veldu Bæta við til að opna felligluggann. 
5. Í reitnum gerð geymslu fyrir grunnstillingar, færðu inn "RCS". 
6. Veljið Stofna geymslu. 
7. Sláðu inn eða veldu gildi í heitareitnum RCS-umhverfisbirting. 
8. Veldu viðeigandi RCS-tilvik. Hægt er að hafa nokkra þeirra. 
9. Veljið Í lagi. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Flytja inn skilgreiningar rafrænnar skýrslugerðar úr RCS-gagnageymslu
1. Velja **Sýna síur**. 
2. Sláðu inn síugildið „RCS“ í reitinn **Heiti** með því að nota síuvirknitáknið **hefst á**. 
3. Þegar valin geymsla er opnuð á **Tengjast við Regulatory Configuration Services** skal velja tengilinn **Smelltu hér til að tengjast Regulatory Configuration Services**. 
4. Veljið **Opna**. 
5. Veljið **Loka**. 
6. Veljið æskilega útgáfu af skilgreiningu rafrænnar skýrslugerðar og veljið **Flytja inn** til að færa hana inn í núverandi tilvik.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
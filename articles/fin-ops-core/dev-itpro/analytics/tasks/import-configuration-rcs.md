---
title: (ER) Flytja inn skilgreiningar úr RCS
description: Þetta efni gefur upplýsingar um hvernig notandi getur flutt inn nýja útgáfu af ER-skilgreiningum úr RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea2bfd2514be666d05165410ca27041a86464715
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143224"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Flytja inn skilgreiningar úr RCS

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Regulatory Configuration Services (RCS). Í þessu dæmi munt þú velja útgáfu af ER-skilgreiningum sem hafa verið skilgreindar í RCS-tilviki og flytja hana inn í núverandi tilvik fyrir sýnisfyrirtækið, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningunum er deilt milli fyrirtækja. Til að ljúka þessum skrefum verður fyrst að ljúka skrefunum í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md). Til að ljúka þessum skrefum verður þú einnig að hafa aðgang að RCS-tilviki sem inniheldur að minnsta kosti eina ER-skilgreiningu í annaðhvort stöðunni **Lokið** eða **Deilt**.

1. Farðu í **Fyrirtækisstjórnun** > **Vinnusvæði** > **Rafræn skýrslugerð**. 
2. Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**. Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md). 
3. Ef þú ert ekki með neinu RCS-umhverfi sem úthlutað á fyrirtækið skaltu smella á ytri tengilinn **Regulatory Services – Skilgreiningar** og fylgja leiðbeiningunum til að úthluta RCS-umhverfi. 
4. Smelltu á **Rafrænar skýrslufæribreytur**. 
5. Smelltu á flipann **RCS**. 
6. Ef RCS-umhverfinu hefur þegar verið úthlutað á fyrirtækið skaltu nota vefslóðirnar sem eru á síðunni til að fá aðgang að því. 
7. Lokið síðunni. 

## <a name="register-a-new-er-repository"></a>Skráðu nýja ER-gagnasafn. 
1. Í listanum skal merkja valda línu. 
2. Veldu veituna Litware, Inc. 
3. Smella á Geymslur. 
4. Smelltu á Bæta við til að opna felligluggann. 
5. Í reitnum gerð geymslu fyrir grunnstillingar, færðu inn "RCS". 
6. Smellið á Stofna gagnasafn. 
7. Sláðu inn eða veldu gildi í heitareitnum RCS-umhverfisbirting. 
8. Veldu viðeigandi RCS-tilvik. Athugaðu að þú getur verið með nokkur slík. 
9. Smellt er á Í lagi. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Flyttu inn ER-skilgreiningar úr RCS-geymslu
1. Smelltu á **Sýna síur**. 
2. Sláðu inn síugildið „RCS“ í reitinn **Heiti** með því að nota síuvirknitáknið **hefst á**. 
3. Þegar þú opnar valda geymslu á síðunni **Tengjast við Regulatory Configuration Services** skaltu smella á tengilinn **Smella hér til að tengjast Regulatory Configuration Services**. 
4. Smelltu á **Opna**. 
5. Smellið á **Loka**. 
6. Veldu viðeigandi útgáfu af ER-skilgreiningum og smelltu á **Flytja inn** til að færa það inn í núverandi tilvik.


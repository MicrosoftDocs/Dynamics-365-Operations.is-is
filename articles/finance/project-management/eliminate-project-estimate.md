---
title: Útiloka verkmat
description: Í þessu efnisatriði er að finna upplýsingar um losun verkáætlunar eftir að henni er lokið.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410230"
---
# <a name="eliminate-a-project-estimate"></a>Útiloka verkmat

[!include [banner](../includes/banner.md)]

Verkáætlanir bjóða upp á fjárhagsyfirlit fyrir vinnu sem er áætluð og tímasett fyrir verk. Til að vinna með mat fyrir stigveldi verks, verður að  hengja verkið við matsverk. Matsverk er alltaf byggt á núverandi verki, en þó geta mörg verk átt við eitt matsverk. Aðeins er hægt að hengja föst verð og fjárfestingaverkefni við matsverk og þau verk verða að tilheyra sama verkflokknum sem matsverkið.

Til að eyða matsverki verður að ljúka því. Eftirfarandi skref útskýra hvernig á að eyða mati.

1. Opnið **Verkefnastjórnun og bókhald** > **Öll verk** og opnið verkið. 
2. Í flipanum **Stjórna** skal velja **Mat** og á síðunni **Mat** skal velja **Losa**.
3. Á síðunni **Losa mat** í flipanum **Almennt** skal stilla eftirfarandi valkosti:

   - **Tímabilskóði**: Veljið tímabilskóða til að velja viðeigandi matsverk. 
   - **Dagsetning mats**: Veljið réttu matsdagsetninguna fyrir losun.
   - **Eyða með VÍV-viðvörun**: Virkið þennan valkost til að bjóða upp á tilkynningu þegar mat sem tengist verki í vinnslu verður losað. Ef þessi valkostur er ekki virkjaður getur losunin ekki haldið áfram ef einhverjar ómetnar færslur eru til staðar. 
   > [!NOTE]
   > Þessi valkostur er aðeins í boði þegar losun er notuð í matsverki. Hann er ekki í boði ef notaðar eru reglubundnar bókanir. Þessi stilling virkar með stillingum í flipanum **Mat** á síðunni **Færibreytur verks**, í reitahópnum **Leyfa losun þegar ómetnar færslur eru til**.
   - **Setja stig á Lokið**: Virkið þennan valkost til að stilla stig matsverks á **Lokið** eftir að losunin er sett af stað.
   - **Prenta matslista**: Veljið upplýsingar sem eiga að fylgja með þegar matslistinn er prentaður.
   - **Sýna athugasemdakladda**: Virkið þennan valkost til að birta athugasemdakladdann.
   - **Bókunardagsetning**: Veljið fjárhagsbókunardagsetningu fyrir matið.

4.  Veljið **Í lagi**.
5. Þegar losunarferlinu er lokið verður losaða matsverkið sýnt með neikvæðu gildi. 

Ef ætlunin var ekki að losa mat er hægt að velja losaða matið og velja **Bakfæra losun**.   

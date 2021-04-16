---
title: Grunnstilla gerðir leyfis og fjarvista
description: Settu upp tegundir orlofs sem starfsmenn geta tekið í Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf868ad44e52b0ed7d0ca6e1f133efa030f3c4a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794566"
---
# <a name="configure-leave-and-absence-types"></a>Grunnstilla gerðir leyfis og fjarvista

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Gerðir leyfa í Dynamics 365 Human Resources skilgreina hinar ýmsu gerðir fjarvista sem starfsmaður getur gefið upp. Þú getur sérsniðið leyfi eftir tegundum fyrirtækisins. Dæmi um orlofsgerðir eru:

- Greitt frí (PTO)
- Ógreidd leyfi
- Frí á launum
- Veikindaleyfi
- Læknaleyfi
- Fjölskylduleyfi
- Örorkubætur til skamms tíma
- Sorgarleyfi

## <a name="add-a-leave-type"></a>Bættu við leyfisgerð

1. Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.

2. Undir **Skipulag**, veldu **Tegundir og leyfi**.

3. Veljið **Nýtt**.

4. Sláðu inn heiti fyrir leyfisgerðina undir **Gerð**, veldu verkflæði frá **Auðkenni vinnuflæðis** og sláðu inn lýsingu undir **Lýsing**.

5. Í **Almennt**, veldu **Enginn**, **Áætlað** eða **Óáætlað** fellilistanum **Flokkur**.

6. Veldu launakóða úr fellilistanum **Vinnukóða**.

7. Undir **Ástæðukóða krafist**, veldu hvort þú vilt þurfa ástæðukóða. Ef þú vilt þurfa ástæðukóða gætirðu þurft að bæta þeim við. Undir **Ástæða númer**, veldu **Bæta við**, veldu ástæðukóða og veldu síðan **Virkt** gátreitinn við hliðina.

8. Undir **Takmarka aðgang að völdum hlutverkum**, veldu hvort þú vilt takmarka aðgang. Veldu síðan öryggishlutverkin undir **Öryggishlutverk fyrir þessa leyfisgerð**. Öryggishlutverkin eru skilgreind í verkflæðinu sem þú valdir undir **Auðkenni vinnuflæðis** fyrr í þessu ferli.

9. Undir **Litur dagatals** skal velja hvaða lit á að sýna fyrir leyfis- og fjarvistadagatöl fyrir þessa leyfisgerð. 

10. Undir **Frestunartengsl** skal velja hvort eigi að fresta þessari leyfisgerð eða fresta annarri leyfisgerð eða láta fresta vegna annarrar leyfisgerðar. Þegar beiðni um fjarvist er send inn fyrir frestaða leyfisgerð verður frestun leyfis sjálfkrafa búin til fyrir frestaða leyfisgerð. 

10. Veljið **Vista**.

## <a name="configure-leave-type-rules"></a>Stilla reglur leyfisgerða

1. Setja valkosti til að námunda fyrir orlofstegundina. Valkostir fela í sér **Enginn**, **Upp**, **Niður** og **Næst**. Þú getur einnig stillt námundun námundunar fyrir orlofstegundina.

2. Stilltu **Leiðrétting á fríi** til að námunda fyrir orlofstegundina. Þegar þú velur þennan valkost notar Human Resources þann fjölda frídaga sem falla á virkum degi til að ákvarða hvernig á að safna fríi fyrir orlofstegundina. Til dæmis, ef jóladagur fellur á mánudag, dregur Human Resources einn dag frá orlofstegundinni þegar unnið er með uppsafnanir.

   Frí er stillt í vinnutímadagatalinu. Fyrir frekari upplýsingar, sjá [Búðu til vinnutímadagatal](hr-leave-and-absence-working-time-calendar.md)
   
 3. Stillið **Yfirfærð leyfisgerð** fyrir leyfisgerð. Þegar þessi valkostur er valinn verða allar yfirfærðar stöður fluttar í tilgreinda gerð leyfis. Yfirfærsluleyfisgerðin þarf einnig að vera með í áætlun um leyfi og fjarveru. 
 
 4. Skilgreinið **Gildistímareglur** fyrir leyfisgerðina. Þegar þessi valkostur er skilgreindur er hægt að velja einingu daga eða mánaða og stilla tímalengd gildistímans. Einnig er hægt að stilla gildisdagsetningu gildistímareglunnar. Gildisdagsetningin er notuð til að ákvarða hvenær á að hefja keyrslu runuvinnslunnar sem vinnur úr gildistíma leyfis eða dagsetninguna þegar reglan tekur gildi. Sjálfur gildistíminn gerist alltaf á upphafsdegi leyfisáætlunarinnar þegar runuvinnslan er stillt á vinnslu. Til dæmis getur upphafsdagur áætlunarinnar verið 1/1/2020, en reglan var ekki búin til fyrr en 1/6/2020. Með því að stilla gildisdagsetninguna á 1/6/2020 verður reglan afgreidd í upphafi næsta árs, þ.e. 1/1/2021. Allar leyfisstöður sem eru til staðar þegar gildistíminn rennur út verða dregnar frá leyfisgerðinni og teknar inn í leyfsstöðuna. 
 
## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)
- [Búa til leyfis- og fjarvistaáætlun](hr-leave-and-absence-plans.md)
- [Búa til dagatal fyrir vinnutíma](hr-leave-and-absence-working-time-calendar.md)
- [Fresta leyfi](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Grunnstilla gerðir leyfis og fjarvista
description: Settu upp tegundir orlofs sem starfsmenn geta tekið í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198051"
---
# <a name="configure-leave-and-absence-types"></a>Grunnstilla gerðir leyfis og fjarvista

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

9. Veljið **Vista**.

## <a name="configure-leave-type-rules"></a>Stilla reglur leyfisgerða

1. Setja valkosti til að námunda fyrir orlofstegundina. Valkostir fela í sér **Enginn**, **Upp**, **Niður** og **Næst**. Þú getur einnig stillt námundun námundunar fyrir orlofstegundina.

2. Stilltu **Leiðrétting á fríi** til að námunda fyrir orlofstegundina. Þegar þú velur þennan valkost notar Human Resources þann fjölda frídaga sem falla á virkum degi til að ákvarða hvernig á að safna fríi fyrir orlofstegundina. Til dæmis, ef jóladagur fellur á mánudag, dregur Human Resources einn dag frá orlofstegundinni þegar unnið er með uppsafnanir.

   Frí er stillt í vinnutímadagatalinu. Fyrir frekari upplýsingar, sjá [Búðu til vinnutímadagatal](hr-leave-and-absence-working-time-calendar.md)
   
## <a name="configure-preview-features"></a>Stilla forskoðunareiginleika

Ef þú hefur gert forskoðunareiginleika virka fyrir leyfi og fjarveru þarftu líka að stilla stillingar fyrir þá.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Veldu leyfisgerð fyrir yfirfærslustöður sem á að flytja til. Þú getur líka búið til nýja leyfisgerð til að yfirfæra. 

## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)
- [Búa til leyfis- og fjarvistaáætlun](hr-leave-and-absence-plans.md)
- [Búa til dagatal fyrir vinnutíma](hr-leave-and-absence-working-time-calendar.md)

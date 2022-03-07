---
title: Leiðrétta niðurstöður afurðartillagna sem byggjast á AI-ML
description: Þetta efni útskýrir hvernig á að sníða niðurstöður afurðatillagna byggt á námi gervigreindarvéla (AI-ML) að fyrirtæki þínu.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5374b2ce559134bd26036b06ac6d96a9f5510ab847544707fc9885506aaab547
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748523"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>Leiðrétta niðurstöður afurðartillagna sem byggjast á AI-ML


[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að leiðrétta niðurstöður afurðatillagna byggt á námi gervigreindarvéla (AI-ML) að fyrirtæki þínu. 

Eftir að hafa gert afurðatillögur virkar munu sjálfgefnar stillingar taka gildi; þessar færibreytur munu vinna fyrir geta unnið fyrir margar þarfir. Best er að skipuleggja að eyða tíma í að meta hvort árangurinn passi við söluhreyfingu afurða. Við mælum með að meta niðurstöður í nokkra daga áður en færibreytum er breytt eftir þörfum áður en prófað er aftur. 

## <a name="understanding-recommendation-list-parameters"></a>Að skilja færibreytur tillögulista

Áður en færibreytuum er breytt skaltu læra hvernig þær hafa áhrif á niðurstöðurnar hér að neðan.

### <a name="trending-product-list"></a>Afurðalistinn „Vinsælt”

Afurðalistinn „Vinsælt” er með tvær færibreytur sem hægt er að breyta:

![Dæmi um sjálfgefna færibreytu fyrir „Vinsælt”](./media/exampletrendingparameters.png)

1. **Láta fylgja með nýjar afurðir frá síðustu X dögum** - Vörur sem hefur verið bætt við innan tiltekins fjölda daga fyrir núverandi dagsetningu má nota til að velja afurðatillögur. Sjálfgefið gildi á myndinni bendir til þess að hægt sé að nota afurðir sem eru orðnar 180 daga gamlar í vinsælum afurðalistanum.
1. **Láta fylgja með nýjar sölu frá síðustu X dögum** - Sölufærslur sem hafa orðið innan tiltekins fjölda daga fyrir núverandi dagsetningu má nota til að panta afurðirnar. Sjálfgefið gildi hér að ofan bendir til þess að öll innkaup, sem gerð hafa verið á vöru síðustu 30 daga, verði notuð til að ákvarða staðsetningu vörunnar í lista yfir vinsælar afurðir. 

### <a name="best-selling-product-list"></a>Listi yfir „mest seldar” afurðir

Það fer eftir viðskiptum þínum, en „Mest selt” getur skilað öðrum árangri en stefna, jafnvel þó að þeir noti bæði viðskiptatilvik til að panta vörur. Þar sem Mest selt er ekki með nein lok miðað við dagsetningu úrvals getur Mest selt samt bent á mjög vinsælar, eldri vörur sem gætu hafa verið felldar af listanum Vinsælt. 

Afurðalistinn „Mest selt” er með eina færibreytu sem hægt er að breyta:

![Dæmi um sjálfgefna færibreytu fyrir söluhæstu vörurnar.](./media/examplebestsellingparameters.PNG)

1. **Láta fylgja með nýjar sölu frá síðustu X dögum** - Sölufærslur sem hafa orðið innan tiltekins fjölda daga fyrir núverandi dagsetningu má nota til að panta afurðirnar. Sjálfgefið gildi hér að ofan bendir til þess að öll innkaup, sem gerð hafa verið á vöru síðustu 30 daga, verði notuð til að ákvarða staðsetningu vörunnar í lista yfir mest seldar afurðir. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Bættu við eða fjarlægðu vörur handvirkt af tillagnalistum

### <a name="for-new-trending-or-best-selling-lists"></a>Fyrir listana „Nýtt”, „Vinsælt” eða „Mest selt”

1.  Farðu í **Retail og Commerce** > **Afurðatillögur** > **Færibreytur tillögulista**.
1.  Á listanum yfir sameiginlegar færibreytur velurðu **Tillögulistar**.
1.  Veldu listann sem á að bæta við eða fjarlægja afurðir af.
1.  Til að bæta afurðum við töfluna skaltu velja **Bæta við línu**. 
1.  Undir vöru dálki, leitaðu að vöru eftir **Nafn** eða **Vörunúmer.**

    ![Dæmi um leit að vöru á Nýja vörulistanum.](./media/examplenewlistconfiguration1.png)

1.  Veldu einn af tveimur valkostum undir dálknum Línugerð:
    -   **Hafa með** - þvingar afurð fremst á listanum
    -   **Útiloka** - fjarlægir afurð frá því að birtast á listanum
    
    ![Dæmi um að taka með eða útiloka vöru frá Nýja vörulistanum.](./media/examplenewlistconfiguration2.png)

1.  Ef **Sýna röð** er breytt breytir það röðinni sem afurðir merktar **hafa með** birtast í á listanum.
    - Ef tvær vörur hafa sama gildi **birta röð**, þá getur endanleg röð þessara tveggja niðurstaðna verið frábrugðin bakforritinu.
1.  Til að fjarlægja vörur af töflunni: veldu línuna sem á að fjarlægja og veldu **Fjarlægja**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Fyrir listana „Fólki líkar einnig” eða „Oft keypt saman”

Í samhengi listanna „Oft keypt saman” eða „Fólki líkar einnig” er vélanám notað til að greina kaupmynstur neytenda til að mæla með skyldum vörum sem oftast eru keyptar saman fyrir einstaka grunnvöru. 
 
*Grunnafurð* er afurðin sem þú vilt búa til niðurstöður fyrir. Í tengslum við að breyta tillagnalistum handvirkt ertu að bæta við eða fjarlægja niðurstöður fyrir þessa afurð. 

Fylgdu þessum skrefum til að bæta við eða fjarlægja niðurstöður fyrir grunnafurð handvirkt:
1.  Velja **Grunnafurð**. 
1.  Undir dálkinum **Afurð** leitarðu að afurð eftir **Heiti** eða **Vörunúmeri.**
![Dæmi um leit að afurð á listanum Oft keypt saman.](./media/exampleFBTlistconfiguration1.png)
1. Veldu einn af tveimur valkostum undir dálknum **Línugerð**:
    - **Hafa með** - þvingar afurð fremst á listanum
    - **Útiloka** - fjarlægir afurð frá því að birtast á listanum     
![Dæmi um að hafa með eða útiloka afurð á listanum Oft keypt saman.](./media/exampleFBTlistconfiguration2.png)
1.  Til að fjarlægja vörur af töflunni: veldu línuna sem á að fjarlægja og veldu Fjarlægja.


## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Bæta við afurðatillögum á sölustað](product.md)

[Bæta tillögum við færsluskjáinn](add-recommendations-control-pos-screen.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
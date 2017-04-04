---
title: "Bóka með afleiddum bækur"
description: "Þessi grein lýsir því hvernig nota afleiddar Bækur."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: ca077727910059878fb16a3f78c5b9133c6c741f
ms.lasthandoff: 03/31/2017


---

# <a name="post-with-derived-books"></a>Bóka með afleiddum bækur

Þessi grein lýsir því hvernig nota afleiddar Bækur.

Þegar bókaðar eru færslur fyrir bóka sem inniheldur afleidd bækur, eru afleiddar bókafærslur bókaðar sjálfvirkt í færslubókum, innkaupapöntunum, eða reikningur með frjálsum texta. Ef aðalbókafærslur eru hins vegar undirbúnar í eignabókinni er hægt að skoða og breyta upphæðum afleiddra færslna áður en þær eru bókaðar.
-   Ákveðnir lyklar, svo sem VSK- og viðskiptavina- eða lánardrottnalyklar, eru uppfærðir aðeins einu sinni með bókunum á aðalbók. Færslur afleidds bóka eru bókaðar á lyklana sem hafa verið skilgreindir fyrir afleitt bók á síðunni Bókunarreglur eigna.
-   Kaup eru oft notuð sem færslugerð fyrir afleidda bóka. Þetta er notað þegar nota á bóka og afleitt bók á eign frá þeim tíma sem eignin var fengin.
-   Önnur gildi fyrir færslugerð kunna einnig að gilda. Til dæmis, ef aðalbók og afleiddu bækurnar hafa sömu bilin að því er varðar sölu og losun, eru allar tegundir viðskipta með eignir tiltækar fyrir uppsetningu afleiddrar bókar.

> [!WARNING]
> Afskrift sem færð er í afleitt Bók verður sömu upphæðar og fært var fyrir aðalbók. Ef afskriftaraðferðirnar eru mismunandi á milli bóka, þá á ekki að nota afleiðuaðferðina við að útbúa afskriftarfærslur. |

## <a name="example"></a>Dæmi 
Eftirfarandi upplýsingar sýna hvernig setja skal upp kaupfærslur með virkni fyrir afleidd bók.

1.  Stofna bækurnar á síðunni Bókum.
    -   Bók fyrir bókhaldið: VM 1, Núgildandi bókunarlag
    -   Bóka fyrir skattamál: VM 2, Skattabókunarlag

2.  Á VM 1 skal smella á flipann Afleidd bækur. Veljið VM 2 í reitnum bók og Kaup í reitnum Færslugerð.

Þá er hægt að tengja bók við tilteknar eignir. 

Þegar kaup eru bókuð fyrir eignina með bók VL 1, eru kaupin ekki einungis færð á vl1, heldur einnig á afleidda bók VL 2. Staða bæði eignabækur er uppfærð til að Opna.

> [!NOTE]                                                                                                         
> Ef ekki eru notuð afleidd bækur skal bóka kaupin á eigninni fyrir bæði bækur VM 1 og bók VM 2.

Nánari upplýsingar, sjá [Afleiddar afskriftarbækur](derived-books.md)



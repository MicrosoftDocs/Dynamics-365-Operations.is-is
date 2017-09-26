---
title: "Bókað í afleiddar bækur"
description: "Þessi grein lýsir því hvernig nota afleiddar Bækur."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: aaacf596f2ea1107a53647d779e9d2b6c37ab530
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="post-with-derived-books"></a>Bókað í afleiddar bækur

[!include[banner](../includes/banner.md)]


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

Þegar kaup eru færð vegna eigna með bóka VL 1 eru kaupin ekki einungis færð á VM 1, heldur einnig á afleiddu bókina VM 2. Staða beggja bóka eigna er uppfærð í Opið.

> [!NOTE]                                                                                                         
> Ef ekki eru notuð afleidd bækur skal bóka kaupin á eigninni fyrir bæði bækur VM 1 og bók VM 2.

Nánari upplýsingar er að finna í [Afleiddar bækur](derived-books.md)




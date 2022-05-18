---
title: Bókað í afleiddar bækur
description: Þessi grein lýsir því hvernig nota afleiddar Bækur.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d4874642743ed8188e84052d94003051f2af7af
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722689"
---
# <a name="post-with-derived-books"></a>Bókað í afleiddar bækur

[!include [banner](../includes/banner.md)]

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

2.  Á VM 1 skal smella á flipann Afleiddar bækur. Veljið VM 2 í reitnum bók og Kaup í reitnum Færslugerð.

Þá er hægt að tengja bók við tilteknar eignir. 

Þegar kaup eru færð vegna eigna með bóka VL 1 eru kaupin ekki einungis færð á VM 1, heldur einnig á afleiddu bókina VM 2. Staða beggja bóka eigna er uppfærð í Opið.

> [!NOTE]                                                                                                         
> Ef ekki eru notuð afleidd bækur skal bóka kaupin á eigninni fyrir bæði bækur VM 1 og bók VM 2.

Nánari upplýsingar er að finna í [Afleiddar bækur](derived-books.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

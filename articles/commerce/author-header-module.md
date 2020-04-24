---
title: Fyrirsagnareining
description: Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261445"
---
# <a name="header-module"></a>Eining síðuhauss


[!include [banner](includes/banner.md)]

Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Í Dynamics 365 Commerce samanstendur síðuhaus af mörgum einingum, eins og haus, yfirlitsvalmynd, leit, auglýsingarborða og samþykkiseiningum fyrir smákökur. 

Hausseiningin inniheldur merki vefsvæða, tengla á leiðsöguveldi, tengla á aðrar síður á vefnum, körfitákn, óskalistatákn, innskráningarvalkosti og leitarstikuna. Fyrirsagnareining er sjálfkrafa fínstillt fyrir tækið sem vefurinn er skoðaður á (með öðrum orðum, fyrir skjáborðstæki eða fartæki). Til dæmis, í fartæki er leiðsagnarstikan smækkuð niður í hnappinn **Valmynd** (sem er stundum kallaður *hamborgaravalmynd*).

## <a name="properties-of-a-header-module"></a>Eiginleikar fyrirsagnareiningar

Hauseining styður eiginleikana **Fyrirtækismerki**, **Merkjatengil** og **Mínir reikningstenglar**. 

Eiginleikarnir **Fyrirtækismerki** og **Merkjatengill** eru notaðir til að skilgreina merki á síðunni. Frekari upplýsingar er að finna á [Bæta merki við](add-logo.md). 

Hægt er að nota eiginleikann **Mínir reikningstenglar** til að skilgreina reikningssíður sem eigandi vefsins vill sýna flýtitengla fyrir í hausnum.

## <a name="modules-that-are-available-in-a-header-module"></a>Einingar sem eru fáanlegar í fyrirsagnareiningunni

Eftirfarandi einingar er hægt að nota í fyrirsagnareiningu:

- **Leiðasagnarvalmynd** - Leiðsagnarvalmyndin táknar leiðsagnarstigveldi rásarinnar og fleiri fasta leiðsagnartengla. Hægt er að stilla leiðsagnarstigveldi rásar í Dynamics 365 Commerce. Yfirlitsvalmyndin er með eiginleikann **Uppruni yfirlits** sem er notaður til að tilgreina valmyndaratriðin í Retail Server og grunnvalmyndaratriði sem uppsprettu. Ef grunnvalmyndaratriði eru tilgreind sem uppspretta er hægt að veita tengda tengla við aðrar síður á vefsvæðinu. Stilltir hlutir birtast síðan sem fyrirsagnarleiðsögn. 
- **Leit** - Leitareiningin gerir notendum kleift að slá inn leitarskilyrði til að leita að vörum. Vefslóð sjálfgefnu leitarsíðunnar og færibreytur leitarfyrirspurna vera að vera gefnar upp í **Svæðisstillingar \> Viðbætur**. Leitareiningin hefur eiginleika sem gera þér kleift að fela leitarhnappinn eða merkimiðann eins og þú þarfnast. Leitareiningin styður einnig valkosti með sjálfvirkum tillögum, svo sem leitarniðurstöðum afurðar, leitarorða og flokka.
- **Körfutákn** - Körfutákneiningin táknar körfutáknið sem sýnir fjölda af vörum í körfunni á hverjum tíma. Fyrir frekari upplýsingar, sjá [Körfutáknseining](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Stofna hauseiningu fyrir síðu

Til að stofna fyrirsagnareiningu skal fylgja eftirfarandi skrefum.

1. Búðu til brot sem er nefnt **hausbrot** og bættu gámaeiningunni við það.
1. Í eiginleikaglugganum fyrir gámaeininguna stillirðu eiginleikann **Breidd** á **Fylla gám**.
1. Bættu auglýsingaborða og samþykkiseiningum fyrir smákökur við gámaeininguna.
1. Bættu annarri gámaeiningu við brotið og stilltu eiginleikann **Breidd** á **Fylla gám**.
1. Bættu hauseiningu við seinni gámaeininguna.
1. Í hólfi **Yfirlitsvalmyndar** í hausseiningunni bætiður við einingu yfirlitsvalmyndar. 
1. Stilltu eiginleika aðgerðar einingar yfirlitsvalmyndar í eiginleikaglugganum í yfirlitsvalmyndareiningunni.
1. Í hólfinu **Leita** í hausseiningunni skal bæta leitareiningu við. 
1. Í eiginleikaglugga fyrir leitareininguna stillirðu eiginleika leitareiningarinnar. 
1. Í raufinni **Körfutákn** í hauseiningunni bætirðu við körfutáknseiningunni. 
1. Í eiginleikaglugga fyrir körfutáknseininguna stillirðu eiginleika körfutáknseiningarinnar. Ef þú vilt að körfutáknið sýni smákörfu þegar músin sveimar yfir skaltu velja **Satt** fyrir **Sýna smákörfu**.
1. Vistaðu síðubrotið, ljúktu við að breyta því og birtu það. 


Til að tryggja að haus birtist á hverri síðu, fylgdu þessum skrefum á hverju síðusniðmáti sem er búið til fyrir svæðið.

1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við haussíðbrotinu sem inniheldur hauseiningunni við hausinn.
1. Vistaðu sniðmátið, ljúktu við að breyta því og birtu það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Eining pöntunarstaðfestingar](order-confirmation-module.md)

[Eining síðuhauss](author-header-module.md)

[Neðanmálseining](author-footer-module.md)

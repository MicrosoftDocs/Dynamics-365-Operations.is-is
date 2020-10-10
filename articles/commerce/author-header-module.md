---
title: Fyrirsagnareining
description: Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 99457b2c98eae0ddd898f852630d690140a5a4c5
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817011"
---
# <a name="header-module"></a>Eining síðuhauss

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Í Dynamics 365 Commerce er síðuhaus stilltur sem síðubrot sem inniheldur haus, tilboðsborða og kökusamþykkiseiningar. 

Hausaeiningin inniheldur svæðismerki, tengla á yfirlitsstigveldið, tengla á aðrar síður á svæðinu, tákneiningu körfu, tákn óskalista, innskráningarmöguleika og leitarslána. Fyrirsagnareining er sjálfkrafa fínstillt fyrir tækið sem vefurinn er skoðaður á (með öðrum orðum, fyrir skjáborðstæki eða fartæki). Til dæmis, í fartæki er leiðsagnarstikan smækkuð niður í hnappinn **Valmynd** (sem er stundum kallaður *hamborgaravalmynd*).

Eftirfarandi mynd sýnir dæmi um fyrirsagnareiningu á heimasíðu.

![Dæmi um fyrirsagnareiningu](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Eiginleikar fyrirsagnareiningar

Hauseining styður eiginleikana **Fyrirtækismerki**, **Merkjatengil** og **Mínir reikningstenglar**. 

Eiginleikarnir **Fyrirtækismerki** og **Merkjatengill** eru notaðir til að skilgreina merki á síðunni. Frekari upplýsingar er að finna á [Bæta merki við](add-logo.md). 

Hægt er að nota eiginleikann **Mínir reikningstenglar** til að skilgreina reikningssíður sem eigandi vefsins vill sýna flýtitengla fyrir í hausnum.

## <a name="modules-that-are-available-within-a-header-module"></a>Einingar sem eru í boði innan hauseiningar

Eftirfarandi einingar er hægt að nota í fyrirsagnareiningu:

- **Leiðasagnarvalmynd** - Leiðsagnarvalmyndin táknar leiðsagnarstigveldi rásarinnar og fleiri fasta leiðsagnartengla. Frekari upplýsingar má finna i [Eining yfirlitsvalmyndar](nav-menu-module.md).

- **Leit** - Leitareiningin gerir notendum kleift að slá inn leitarskilyrði til að leita að vörum. Vefslóð sjálfgefnu leitarsíðunnar og færibreytur leitarfyrirspurna vera að vera gefnar upp í **Svæðisstillingar \> Viðbætur**. Leitareiningin hefur eiginleika sem gera þér kleift að fela leitarhnappinn eða merkimiðann eins og þú þarfnast. Leitareiningin styður einnig valkosti með sjálfvirkum tillögum, svo sem leitarniðurstöðum afurðar, leitarorða og flokka.

- **Körfutákn** - Körfutákneiningin táknar körfutáknið sem sýnir fjölda af vörum í körfunni á hverjum tíma. Fyrir frekari upplýsingar, sjá [Körfutáknseining](cart-icon-module.md).

## <a name="create-a-header-fragment-for-a-page"></a>Búa til hausbrot fyrir síðu

Fylgdu þessum skrefum til að búa til hausbrot.

1. Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.
1. Í glugganum **Nýtt brot** skal velja eininguna **Hólf**, slá inn heiti fyrir brotið og síðan velja **Í lagi**.
1. Velja skal hólfið **Sjálfgefið hólf** og síðan, hægra megin á eiginleikasvæðinu, skal stilla eiginleikann **Breidd** á **Fylla skjáinn**.
1. Í hólfinu **Sjálfgefið hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja einingarnar **Kökusamþykki**, **Haus** og **Tilboðsborði** og velja síðan **Í lagi**.
1. Í eiginleikasvæði í **Tilboðsborðaeining** skal velja **Bæta við skilaboðum** og velja svo **Skilaboð**.
1. Í svarglugganum **Skilaboða** skal bæta við texta og tenglum fyrir kynningarefnið og velja síðan **Í lagi**.
1. Í einingunni **Samþykki köku** skaltu bæta við og grunnstilla texta og tengil á persónuverndarsíðu.
1. Í hólfinu **Yfirlitsvalmynd** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Yfirlitsvalmynd** og síðan velja **Í lagi**.
1. Á eiginleikasvæðinu fyrir einingu yfirlitsvalmyndar, undir **Uppruni yfirlitsvalmyndar** skal velja **Retail Server**.
1. Í eignasvæði fyrir einingu yfirlitsvalmyndar, undir **Föst valmyndaratriði** skal velja **Bæta við valmyndaratriði** og velja svo **Valmyndaratriði**. 
1. Í svarglugganum **Valmyndaratriði** undir **Texti valmyndaratriðis** skal slá inn „Tengiliður“.
1. Í svarglugganum **Valmyndaratriði**, undir **Tenglamarkmið valmyndaratriðis** skal velja **Bæta við tengli**.
1. Í svarglugganum **Bæta við tengli** skal velja tengil fyrir „Tengiliður“ síðuna og síðan velja **Í lagi**.  
1. Í svarglugganum **Valmyndaratriði** skal velja **Í lagi**.
1. Í hólfinu **Leita** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Leita** og síðan velja **Í lagi**.
1. Á eiginleikasvæðinu fyrir leitareininguna skal stilla eiginleikana eftir því sem þörf krefur.
1. Í hólfinu **Körfutákn** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Körfutákn** og síðan velja **Í lagi**.
1. Á eiginleikasvæðinu fyrir einingu körfutákns skal stilla eiginleikana eftir því sem þörf krefur. Ef óskað er eftir að körfutáknið sýni samantekt körfu (einnig þekkt sem smákarfa) þegar notendur fara með bendilinn yfir það, skal velja **Sýna smákörfu**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.

Til að hjálpa til við að tryggja að haus birtist á hverri síðu skal fylgja þessum skrefum á hverju síðusniðmáti sem er búið til fyrir vefsvæðið.

1. Í hólfinu **Fyrirsögn** í einingunni **Sjálfgefin síða** skal bæta við neðanmálsbrotinu sem var búið til.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Körfutáknseining](cart-icon-module.md)

[Tilboðsborðaeining](add-alert.md)

[Eining yfirlitsvalmyndar](nav-menu-module.md) 

[Samþykki köku](cookie-consent-module.md)

[Eining síðufótar](author-footer-module.md)

---
title: Ósamstilltur viðskiptahamur til að búa til
description: Þetta efnisatriði lýsir ósamstilltri stofnun viðskiptavinar í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 22bb4eaf3d4897904412120fa5580c42637b56e0
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913775"
---
# <a name="asynchronous-customer-creation-mode"></a>Ósamstilltur viðskiptahamur til að búa til

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir ósamstilltri stofnun viðskiptavinar í Microsoft Dynamics 365 Commerce.

Í Commerce eru tvær leiðir til að búa til viðskiptavina: samstilltur (eða samstilltur) og ósamstilltur (eða ósamstilltur). Viðskiptavinir eru stofnaðir samstilltir að sjálfgefnu. Þ.e.a.s. þeir eru stofnaðir í Commerce Headquarters á rauntíma. Samstillingarstillingin fyrir sköpun viðskiptavina er gagnleg vegna þess að það er strax hægt að leita að nýjum viðskiptavinum á milli rása. Hins vegar er einnig galli á henni. Þar sem hún myndar köll [Commerce Data Exchange: Rauntímaþjónustu](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) til Commerce Headquarters, þá getur það haft áhrif á afköst ef mörg köll vegna stofnunar viðskiptavina eru gerð á sama tíma.

Ef valkosturinn **Stofna viðskiptavin í Async-stillingu** er stilltur á **Já** í virknireglu verslunar (**Smásala og viðskipti \> Uppsetning rásar \> Uppsetning netverslunar \> Virknireglur**), þá eru köll rauntímaþjónustu ekki notuð til að stofna viðskiptavinafærslur í gagnagrunni rásarinnar. Ósamstilltur viðskiptahamur hefur ekki áhrif á frammistöðu höfuðstöðva Commerce. Tímabundið alþjóðlegt einstakt auðkenni (GUID) er úthlutað á hverja nýja ósamstillta viðskiptavinaskrá og notað sem auðkenni viðskiptavinareiknings. Þetta GUID er ekki sýnt notendum sölustaða (POS). Þess í stað munu þessir notendur sjá **Bíður samstillingar** sem auðkenni viðskiptavinareikningsins.

> [!IMPORTANT]
> Alltaf þegar POS fer án nettengingar, býr kerfið sjálfkrafa til viðskiptavini ósamstillt, jafnvel þótt ósamstilltur viðskiptahamur sé óvirkur. Þess vegna, óháð vali þínu á milli samstillingar og ósamstilltra viðskiptavina, verða stjórnendur Commerce höfuðstöðva að búa til og skipuleggja endurtekið runuverk fyrir **P-starf**, hinn **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** starf (áður nefnt **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu**), og **1010** starf, þannig að ósamstilltum viðskiptavinum er breytt í samstillta viðskiptavini í höfuðstöðvum Commerce.

## <a name="async-customer-limitations"></a>Takmarkanir ósamstilltra viðskiptavina

Ósamstilltur viðskiptavinur hefur eftirfarandi takmarkanir eins og er:

- Ekki er hægt að breyta ósamstilltum færslum viðskiptavina nema viðskiptavinurinn hafi verið stofnaður í Commerce Headquarters og nýtt auðkenni viðskiptavinareiknings hefur verið samstillt aftur við rásina.
- Ekki er hægt að gefa út vildarkort til að samstilla viðskiptavini nema nýja auðkenni viðskiptavinarreikningsins hafi verið samstillt aftur við rásina.

## <a name="async-customer-enhancements"></a>Ósamstilltur aukahlutir viðskiptavina

Frá og með útgáfu Commerce útgáfu 10.0.24 geturðu virkjað **Virkjaðu aukna ósamstillta sköpun viðskiptavina** eiginleiki í **Eiginleikastjórnun** vinnurými. Þessi eiginleiki brúar bilið á milli ósamstillingar og samstillingar til að búa til viðskiptavina í POS og rafrænum viðskiptum á eftirfarandi hátt:

- Hægt er að tengja tengsl við ósamstillta viðskiptavini.
- Hægt er að bæta titlum við ósamstillta viðskiptavini.
- Hægt er að fanga aukanetföng og símanúmer fyrir ósamstillta viðskiptavini.

Frá og með útgáfu Commerce útgáfu 10.0.22 geturðu virkjað **Virkjaðu ósamstillta stofnun fyrir heimilisföng viðskiptavina** eiginleiki í **Eiginleikastjórnun** vinnurými. Þessi eiginleiki gerir kleift að vista nýstofnað heimilisföng viðskiptavina ósamstillt fyrir bæði samstillta viðskiptavini og ósamstillta viðskiptavini.

Eftir að þú hefur virkjað áðurnefnda eiginleika verður þú að skipuleggja endurtekið runuverk fyrir **P-starf**, hinn **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** starf, og **1010** starf, þannig að ósamstilltum viðskiptavinum er breytt í samstillta viðskiptavini í höfuðstöðvum Commerce.

### <a name="customer-creation-in-pos-offline-mode"></a>Stofnun viðskiptavinar á sölustað án nettengingar

Eins og áður hefur komið fram, alltaf þegar POS fer án nettengingar, býr kerfið sjálfkrafa til viðskiptavini ósamstillt, jafnvel þótt ósamstilltur viðskiptahamur sé óvirkur. Þess vegna verða stjórnendur Commerce höfuðstöðva að búa til og skipuleggja endurtekið runuverk fyrir **P-starf**, hinn **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** starf, og **1010** starf, þannig að ósamstilltum viðskiptavinum er breytt í samstillta viðskiptavini í höfuðstöðvum Commerce.

> [!NOTE]
> Ef valkosturinn **Afmarka samnýttar gagnatöflur viðskiptavinar** er stilltur á **Já** á síðunni **Skema fyrir viðskiptarás** (**Smásala og viðskipti \> Uppsetning höfuðstöðva \> Viðskiptaverkraðari \> Gagnagrunnsflokkur rásar**), verða færslur viðskiptavina ekki stofnaðar á sölustað sem er án tengingar. Frekari upplýsingar er að finna í [Útilokun gagna án nettengingar](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórnun viðskiptavina í verslunum](customer-mgmt-stores.md)

[Umbreyttu ósamstilltum viðskiptavinum í samstillta viðskiptavini](convert-async-to-sync.md)

[Eigindir viðskiptavinar](dev-itpro/customer-attributes.md)

[Útilokun gagna án nettengingar](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)

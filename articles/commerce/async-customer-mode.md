---
title: Ósamstillt stilling til að stofna viðskiptavin
description: Þessi grein lýsir ósamstilltri stofnun viðskiptavinar í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 95102936871e15f8e525abca736fa75927569b34
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473707"
---
# <a name="asynchronous-customer-creation-mode"></a>Ósamstillt stilling til að stofna viðskiptavin

[!include [banner](includes/banner.md)]

Þessi grein lýsir ósamstilltri stofnun viðskiptavinar í Microsoft Dynamics 365 Commerce.

Í Commerce eru tvær leiðir til að búa til viðskiptavina: samstilltur (eða samstilltur) og ósamstilltur (eða ósamstilltur). Viðskiptavinir eru stofnaðir samstilltir að sjálfgefnu. Með öðrum orðum, þeir eru búnir til í höfuðstöðvum Commerce í rauntíma. Samstillingaraðferðin til að búa til viðskiptavina er gagnleg vegna þess að það er strax hægt að leita að nýjum viðskiptavinum á milli rása. Hins vegar er einnig galli á henni. Þar sem hún myndar köll [Commerce Data Exchange: Rauntímaþjónustu](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) til Commerce Headquarters, þá getur það haft áhrif á afköst ef mörg köll vegna stofnunar viðskiptavina eru gerð á sama tíma.

Ef valkosturinn **Stofna viðskiptavin í Async-stillingu** er stilltur á **Já** í virknireglu verslunar (**Smásala og viðskipti \> Uppsetning rásar \> Uppsetning netverslunar \> Virknireglur**), þá eru köll rauntímaþjónustu ekki notuð til að stofna viðskiptavinafærslur í gagnagrunni rásarinnar. Ósamstilltur viðskiptahamur hefur ekki áhrif á frammistöðu höfuðstöðva Commerce. Tímabundið alþjóðlegt einstakt auðkenni (GUID) er úthlutað á hverja nýja ósamstillta viðskiptavinaskrá og notað sem auðkenni viðskiptavinareiknings. Þetta GUID er ekki sýnt notendum sölustaða (POS). Þess í stað munu þessir notendur sjá **Bíður samstillingar** sem auðkenni viðskiptavinareikningsins.

> [!IMPORTANT]
> Alltaf þegar POS fer án nettengingar, býr kerfið sjálfkrafa til viðskiptavini ósamstillt, jafnvel þótt ósamstilltur viðskiptahamur sé óvirkur. Þess vegna, óháð vali þínu á milli samstillingar og ósamstillingar viðskiptavina, verða stjórnendur Commerce höfuðstöðva að búa til og skipuleggja endurtekið runuverk fyrir **P-starf**, hinn **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** starf, og **1010** starf, þannig að ósamstilltum viðskiptavinum er breytt í samstillingarviðskiptavini í höfuðstöðvum Commerce.

## <a name="async-customer-limitations"></a>Takmarkanir ósamstilltra viðskiptavina

Ósamstilltur viðskiptavinur hefur eftirfarandi takmörkun eins og er:

- Ekki er hægt að gefa út vildarkort til að samstilla viðskiptavini nema nýja auðkenni viðskiptavinarreikningsins hafi verið samstillt aftur við rásina.

## <a name="async-customer-enhancements"></a>Ósamstilltur aukahlutir viðskiptavina

Til að hjálpa fyrirtækjum að nota ósamstilltan viðskiptaham til að stjórna viðskiptavinum og til að draga úr rauntímasamskiptum við höfuðstöðvar Commerce, hafa eftirfarandi endurbætur verið settar á laggirnar til að koma á jöfnuði milli samstillingar og ósamstillingar á rásum. 

| Eiginleikaaukning | Viðskiptaútgáfa | Upplýsingar um eiginleika |
|---|---|---|
| Frammistöðubætir þegar upplýsingar um viðskiptavini eru sóttar úr gagnagrunni rásarinnar | 10.0.20 og síðar | Til að hjálpa til við að bæta árangur er viðskiptaeiningunni skipt í smærri einingar. Kerfið sækir þá aðeins nauðsynlegar upplýsingar úr rásargagnagrunninum. |
| Geta til að búa til heimilisfang ósamstillt við útskráningu | 10.0.22 og síðar | <p>Eiginleikarofi: **Virkjaðu ósamstillta stofnun fyrir heimilisföng viðskiptavina**</p><p>Upplýsingar um eiginleika:</p><ul><li>Geta til að bæta við heimilisföngum án þess að hringja í rauntíma þjónustu í höfuðstöðvar Commerce</li><li>Geta til að bera kennsl á heimilisföng í gagnagrunni rásarinnar án þess að nota skráningarauðkenni (**RecId** gildi)</li><li>Rekja tímastimplar til að búa til heimilisfang</li><li>Samstilling heimilisfönga í höfuðstöðvum Commerce</li></ul><p>Þessi eiginleiki hefur áhrif á bæði samstillta viðskiptavini og ósamstillta viðskiptavini. Til að breyta vistföngum ósamstillt auk þess að búa þau til ósamstillt verður þú að virkja **Breytir viðskiptavinum í ósamstilltum ham** eiginleiki.</p> |
| Virkja jafnræði milli samstilltar og ósamstilltra sköpunar viðskiptavina. | 10.0.24 og síðar | <p>Eiginleikarofi: **Virkjaðu aukna ósamstillta sköpun viðskiptavina**</p><p>Eiginleikaupplýsingar: Geta til að fanga viðbótarupplýsingar, svo sem titil, tengsl frá sjálfgefnum viðskiptavinum og auka tengiliðaupplýsingar (símanúmer og netfang), á meðan þú býrð til viðskiptavini ósamstillt</p> |
| Notendavæn villuboð | 10.0.28 og síðar | Þessar endurbætur hjálpa til við að bæta notendavænni villuboð ef notandi getur ekki strax breytt upplýsingum á meðan samstilling er í gangi. Þú virkjar þessar endurbætur með því að nota **Leyfa tilteknum notendaeiningum að vera óbreytanlegir af ósamstilltum viðskiptavinum** stilling kl **Vefstillingar \> Framlengingar** í viðskiptasíðugerð. |
| Geta til að breyta upplýsingum viðskiptavina ósamstilltur | 10.0.29 og síðar | <p>Eiginleikarofi: **Virkjaðu að breyta viðskiptavinum í ósamstilltum ham**</p><p>Upplýsingar um eiginleika: Geta til að breyta gögnum viðskiptavina ósamstillt</p><p>Sjá svör við algengum spurningum um vandamál sem tengjast ósamstilltri breytingu á viðskiptavinaupplýsingum [Algengar spurningar um ósamstilltur viðskiptahamur](async-customer-mode-faq.md).</p> |

### <a name="feature-switch-hierarchy"></a>Eiginleikarofa stigveldi

Vegna stigveldis eiginleikarofa, áður en þú virkjar **Virkjaðu að breyta viðskiptavinum í ósamstilltum ham** eiginleika, þú verður að virkja eftirfarandi eiginleika: 

- **Frammistöðubætir fyrir pantanir viðskiptavina og viðskipti viðskiptavina** – Þessi eiginleiki hefur verið nauðsynlegur frá útgáfu Commerce útgáfu 10.0.28. 
- **Virkjaðu aukna ósamstillta sköpun viðskiptavina**
- **Virkja ósamstillta stofnun fyrir aðsetur viðskiptavinar**

Fyrir svör við algengum spurningum um bilanaleit, sjá [Algengar spurningar um ósamstilltur viðskiptahamur](async-customer-mode-faq.md). 

Eftir að þú hefur virkjað áðurnefnda eiginleika verður þú að skipuleggja endurtekið runuverk fyrir **P-starf**, hinn **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** starf, og **1010** starf, þannig að ósamstilltum viðskiptavinum er breytt í samstillingarviðskiptavini í höfuðstöðvum Commerce.

### <a name="customer-creation-in-pos-offline-mode"></a>Stofnun viðskiptavinar á sölustað án nettengingar

Eins og áður hefur komið fram, alltaf þegar POS fer án nettengingar, býr kerfið sjálfkrafa til viðskiptavini ósamstillt, jafnvel þótt ósamstilltur viðskiptahamur sé óvirkur. Þess vegna verða stjórnendur Commerce höfuðstöðva að búa til og skipuleggja endurtekið runuverk fyrir **P-starf**, hinn **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** starf, og **1010** starf, þannig að ósamstilltum viðskiptavinum er breytt í samstillingarviðskiptavini í höfuðstöðvum Commerce.

> [!NOTE]
> Ef valkosturinn **Afmarka samnýttar gagnatöflur viðskiptavinar** er stilltur á **Já** á síðunni **Skema fyrir viðskiptarás** (**Smásala og viðskipti \> Uppsetning höfuðstöðva \> Viðskiptaverkraðari \> Gagnagrunnsflokkur rásar**), verða færslur viðskiptavina ekki stofnaðar á sölustað sem er án tengingar. Frekari upplýsingar er að finna í [Útilokun gagna án nettengingar](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórnun viðskiptavina í verslunum](customer-mgmt-stores.md)

[Umbreyta ósamsettum viðskiptavinum í samstillta viðskiptavini](convert-async-to-sync.md)

[Eigindir viðskiptavinar](dev-itpro/customer-attributes.md)

[Útilokun gagna án nettengingar](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)

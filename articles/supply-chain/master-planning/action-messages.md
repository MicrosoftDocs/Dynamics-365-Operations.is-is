---
title: Aðgerðaboð
description: Aðgerðaboð eru tillaga sem mynduð er í kerfinu til að breyta fyrirliggjandi áætlaðri eða staðfestri pöntun.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570255"
---
# <a name="action-messages"></a>Aðgerðaboð

[!include [banner](../includes/banner.md)]

Aðgerðarskilaboð eru kerfismynduð tillaga um að breyta fyrirliggjandi skipulagðri, samþykktri eða staðfestri pöntun.

Útreikningur aðalröðunar myndar aðgerðaboð sem viðbrögð við breyttum þörfum. Til dæmis er sendingardagsetningu eða magni breytt á sölupöntun eftir að þú hefur þegar búið til innkaupapöntun til að uppfylla eftirspurnina fyrir þá sölupöntun. Í þessu tilviki myndar aðalskipulagsútreikningurinn ein eða fleiri aðgerðaskilaboð sem benda til þess að þú uppfærir innkaupapöntunina. Þú ákveður hvort framkvæma eigi ráðlagðar breytingar.

Hægt er að skilgreina hvernig aðgerðaboðin eru reiknuð fyrir þekjuhóp sem hægt er að tengja við vöru.

## <a name="select-action-messages"></a>Skoða aðgerðarboð

Á síðunni **Þekjuflokkar** er hægt að velja aðgerðaboð sem óskað er eftir að kerfið myndi, aðgerðaboð og þekjuflokka eða vörur sem skilaboðin skulu notuð við. Eftirfarandi tafla sýnir aðgerðaskilaboðin sem þú getur valið.

| Skilaboð | Lýsing |
|---|---|
| Flýta | Kerfið mun búa til aðgerðaskilaboð, eftir því sem þörf er á, til að færa pantanir á fyrri dagsetningu. Í **Framlegð framlegð** reit, getur þú tilgreint hámarksfjölda daga sem geta liðið á milli kvittunar og útgáfu án fyrirframaðgerðar. |
| Fresta | Kerfið mun búa til aðgerðaskilaboð, eftir því sem þörf er á, til að færa pantanir til síðari tíma. Í **Fresta framlegð** reit, getur þú tilgreint hámarksfjölda daga sem getur liðið á milli móttöku og útgáfu án þess að fresta aðgerð. |
| Lækka | Kerfið mun búa til aðgerðaskilaboð þegar minnka ætti framleiðslupantanir, innkaupapantanir og aðrar innhreyfingarfærslur til að koma í veg fyrir umfram birgðastig. |
| Hækka | Kerfið mun búa til aðgerðaskilaboð þegar auka ætti framleiðslupantanir, innkaupapantanir og aðrar innhreyfingarfærslur til að koma í veg fyrir skort á birgðum. |
| Afleiddar aðgerðir | Aðgerðaskilaboð sem eru búin til fyrir kvittunarfærslur verða sendar til allra afleiddra krafna og nauðsynleg aðgerðaskilaboð verða búin til fyrir kvittunarfærslurnar sem uppfylla þessar kröfur. |

Eftirfarandi kaflar veita nokkrar ítarlegar aðstæður.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Auka og minnka aðgerðir með sjálfgefnu pöntunarmagni vöru

Á **Sjálfgefnar pöntunarstillingar** síðu fyrir vöru, getur þú sett upp lágmarks pöntunarmagn, hámarks pöntunarmagn og mörg gildi. Kerfið tekur síðan tillit til þessara stillinga þegar það stingur upp á aðgerðum, til að tryggja að tillögurnar valdi aldrei of miklu framboði.

Til dæmis ertu með hlut sem hefur eftirfarandi stillingar á sér **Sjálfgefnar pöntunarstillingar** síða:

- **Lágmarks magn pöntunar:** *0*
- **Hámarks pöntunarmagn:** *90*
- **Margfalt:** *20*

Ef eftirspurn er eftir magni upp á 60 af þessari vöru, mun aðalskipulag stofna áætlaða innkaupapöntun fyrir magn upp á 60. Ef eftirspurnin er aukin um 30 mun aðalskipulag stinga upp á hækkun um 40, því það mun virða margfeldið 20 og valda aldrei vanframboði.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Aðgerðarskilaboð fyrir pantanir sem tengjast öryggisbirgðum

Aðgerðarskilaboð fyrir pantanir sem leggja fram öryggisbirgðir munu aldrei benda til þess að minnka magnið undir því magni sem þarf fyrir öryggisbirgðirnar. Með öðrum orðum, ef það er pöntun sem veitir öryggisbirgðum og eftirspurn viðskiptavina, og eftirspurnin minnkar eða hætt er við, mun aðalskipulag stinga upp á að minnka áætlaða pöntun með minni eftirspurn. Hins vegar mun það aldrei gefa til kynna gildi sem er lægra en öryggisbirgðir sem þarf.

Kerfið mun ekki leggja til frestun aðgerða til að útvega öryggisbirgðir, vegna þess að gert er ráð fyrir að öryggisbirgðir verði afhentar á tilskildum tíma og á tilskildum degi.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Framfara og fresta aðgerðum sem tengjast uppskriftum

Beita verður aðgerðum sem tengjast íhlutum efnisyfirlita (BOMs) á undan aðgerðum yfirvöru þeirra, vegna þess að frekari pantanir sem tengjast hærra stigi uppskrifta gætu haft áhrif. Þú verður síðan að keyra aðalskipulagningu aftur til að endurreikna og leggja til viðeigandi aðgerðir.

Til dæmis hefur þú eftirfarandi aðstæður:

- Lokagott *FG* af gerðinni *framleiðslu* er með uppskrift sem inniheldur hráefni *RM*.
- Dagsetningin í dag er 21. janúar.
- Fyrirliggjandi, útgefin framleiðslupöntun fyrir *FG* er áætluð 25. janúar.
- Til að styðja fyrirliggjandi framleiðslupöntun hefur aðalskipulag stofnað áætlaða innkaupapöntun fyrir nauðsynlegt hráefni *RM*. Þessi pöntun hefur kröfudagsetningu 25. janúar.
- Ný sölupöntun fyrir *FG* er búið til í dag. Það hefur kröfudagsetningu í dag (21. janúar).
- Lokað er fyrir afhendingu þann 21. janúar *RM* dagatal, en 22. janúar er opið.

Þegar aðaláætlanagerð er keyrð myndar hún fyrirfram aðgerðaskilaboð sem benda til þess að færa upp áður áætlaða framleiðslu svo hægt sé að uppfylla pöntun dagsins.

- Til að mæta nýju eftirspurninni er lagt til að færa framleiðslupöntunina fyrir *FG* til 21. janúar. (Það gerir þessa tillögu án þess að taka tillit til lokadagsetningar fyrir *RM* .)
- Vegna þess að *RM* er enn krafist fyrir framleiðslupöntunina, bendir það til þess að færa upp fyrirhugaða innkaupapöntun líka. Hins vegar, að þessu sinni, athugar það *RM* dagatal. Þess vegna er lagt til að færa fyrirhugaða innkaupapöntun fyrir *RM* til 22. janúar (því 21. janúar er lokað).

Eins og þú sérð, nauðsynlegt hráefni *RM* mun nú koma of seint fyrir áætlaða framleiðslu á *FG*. Þess vegna verður þú fyrst að beita fyrirframaðgerðinni á fyrirhugaða innkaupapöntun fyrir *RM* og keyra svo aðalskipulag aftur. Á þeim tímapunkti mun aðalskipulag búa til ný aðgerðaskilaboð sem stinga upp á að færa framleiðslupöntunina fyrir *FG* til 22. janúar.

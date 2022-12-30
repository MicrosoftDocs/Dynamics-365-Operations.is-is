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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570255"
---
# <a name="action-messages"></a>Aðgerðaboð

[!include [banner](../includes/banner.md)]

Aðgerðaboð eru tillaga sem mynduð er í kerfinu til að breyta fyrirliggjandi áætlaðri, samþykktri eða staðfestri pöntun.

Útreikningur aðalröðunar myndar aðgerðaboð sem viðbrögð við breyttum þörfum. Til dæmis er sendingardagsetningu eða magni breytt í sölupöntun þegar búið er að stofna innkaupapöntun til að uppfylla eftirspurnina fyrir þá sölupöntun. Í þessu tilviki býr útreikningur aðaláætlanagerðar til eitt eða fleiri aðgerðaboð sem leggja til að þú uppfærir innkaupapöntunina. Þú ákveður hvort framkvæma eigi ráðlagðar breytingar.

Hægt er að skilgreina hvernig aðgerðaboðin eru reiknuð fyrir þekjuhóp sem hægt er að tengja við vöru.

## <a name="select-action-messages"></a>Skoða aðgerðarboð

Á síðunni **Þekjuflokkar** er hægt að velja aðgerðaboð sem óskað er eftir að kerfið myndi, aðgerðaboð og þekjuflokka eða vörur sem skilaboðin skulu notuð við. Í eftirfarandi töflu er listi yfir aðgerðarskilaboð sem hægt er að velja.

| Skilaboð | Lýsing |
|---|---|
| Flýta | Kerfið mun búa til aðgerðaboð, eftir því sem þörf krefur, til að færa pantanir til fyrri tíma. Í reitnum **Færslumörk** er einnig hægt að tilgreina hámarksfjölda daga sem mega líða á milli innhreyfingar og úthreyfingar án færsluaðgerðar. |
| Fresta | Kerfið mun búa til aðgerðaboð eftir þörfum til að flytja pantanir á seinni dagsetningu. Í reitnum **Frestunarmörk** er einnig hægt að tilgreina hámarksfjölda daga sem mega líða á milli innhreyfingar og úthreyfingar án frestunaraðgerðar. |
| Lækka | Ef kerfið býr til aðgerðaboð þegar minnka á framleiðslupantanir, innkaupapantanir og aðrar innhreyfingarfærslur til að forðast of mikla birgðastöðu. |
| Hækka | Ef kerfið býr til aðgerðaboð þegar auka á framleiðslupantanir, innkaupapantanir og aðrar innhreyfingarfærslur til að forðast of litla birgðastöðu. |
| Afleiddar aðgerðir | Aðgerðaboðin sem eru búin til fyrir innhreyfingarfærslur verða úthlutaðar á allar afleiddar kröfur og nauðsynleg aðgerðaboð verða búin til fyrir innhreyfingarfærslur sem uppfylla þessar kröfur. |

Eftirfarandi kaflar sýna nokkrar ítarlegar aðstæður.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Aukningar- og minnkunarfærslur með sjálfgefnu pöntunarmagni vöru

Á síðunni **Sjálfgefnar pöntunarstillingar** fyrir vöru er hægt að setja upp lágmarks pöntunarmagn, hámarks pöntunarmagn og mörg gildi. Kerfið tekur þá tillit til þessara stillinga þegar það leggur til aðgerðir, til að tryggja að tillögurnar valdi aldrei valda skorti.

Til dæmis ert með vöru sem er með eftirfarandi stillingar á síðuni **Sjálfgefnar pöntunarstillingar**:

- **Lágmarksmagn pöntunar:** *0*
- **Hámarksmagn pöntunar:** *90*
- **Margfalt:** *20*

Ef eftirspurn er eftir magni sem nemur 60 af þessum lið mun aðalskipulagið búa til fyrirhugaða innkaupapöntun fyrir magnið sem nemur 60. Ef eftirspurnin eykst um 30 mun aðalskipulagið leggja til aukininguna 40, því það mun virða margfeldi 20 og aldrei valda því að lager tæmist.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Aðgerðaskilaboð vegna pantana sem tengjast öryggisbirgðum

Aðgerðarskilaboð fyrir pantanir sem veita öryggisbirgðir munu aldrei leggja til magns sem er minna en magnið sem þarf fyrir öryggisbirgðirnar. Þ.e. ef til er pöntun sem útvegar öryggisbirgðir og eftirspurn viðskiptavinar, og eftirspurnin er minnkuð eða afturkölluð, mun aðaláætlanagerð leggja til minnkun á áætlaðri pöntun sem nemur minnkaðri eftirspurn. Hins vegar mun það aldrei gefa til kynna gildi sem er lægra en öryggisbirgðir sem þörf er á.

Kerfið mun ekki leggja til frestunaraðgerðir til að uppfylla öryggisbirgðir því að gert er ráð fyrir að útvega þurfi öryggisbirgðirnar á nauðsynlegum tíma og nauðsynlegum degi.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Koma á framfæri og fresta aðgerðum sem tengjast uppskriftum

Beita verður aðgerðum sem tengjast íhlutum uppskrifta (uppskrift) áður en gripið er til aðgerða vegna þess að frekari fyrirmæli sem tengjast uppskriftum á hærra stigi gætu orðið fyrir áhrifum. Síðan verður að keyra aðaláætlanagerðina aftur til að reikna út aftur og leggja til viðeigandi aðgerðir.

Þú hefur til dæmis eftirfarandi aðstæður:

- Lokavaran *FG* af gerðinni *framleiðsla* er með uppskrift sem inniheldur hráefni *RM*.
- Dagurinn í dag er 21. janúar.
- Fyrirliggjandi, losuð framleiðslupöntun fyrir *FG* er áætluð 25. janúar.
- Til að styðja við núverandi framleiðslupöntun hefur aðaláætlanagerð stofnað áætlaða innkaupapöntun fyrir nauðsynlegt hráefni *RM*. Þessi pöntun er með dagsetningu þarfa 25. janúar.
- Ný sölupöntun fyrir *FG* er stofnuð í dag. Dagsetning þarfa er í dag (21. janúar).
- 21. janúar er lokað fyrir afhendingu í *RM* dagatali en 22. janúar er opinn.

Þegar aðaláætlanagerð er keyrð býr hún til aðgerðaboð um tilfærslu sem leggur til að færa upp áður tímasetta afurð þannig að þú getir uppfyllt pöntun dagsins í dag.

- Til að mæta nýju eftirspurninni leggur það til að framleiðslupöntun *FG* færist til 21. janúar. (Það gerir þessa tillögu án þess að íhuga lokaða dagsetningu fyrir *RM*.)
- Vegna þess að *RM* er enn nauðsynlegt fyrir framleiðslupöntunina, leggur það til að færa upp fyrirhugaða innkaupatillögu líka. Að þessu sinni skoðar hún þó dagatal *RM*. Því leggur hún til að færa fyrirhugaða innkaupapöntun fyrir *RM* til 22. janúar (því 21. janúar er lokað).

Eins og sjá má mun nauðsynlegt hráefni frá *RM* nú koma of seint í áætlaða framleiðslu *FG*. Þess vegna verður þú fyrst að nota færsluaðgerðina á áætlaða innkaupapöntun fyrir *RM* og síðan keyra aðaláætlanagerðina aftur. Á þeim tímapunkti mun aðaláætlanagerðin búa til ný aðgerðaboð sem leggja til að færa framleiðslupöntunina fyrir *FG* til 22. janúar.

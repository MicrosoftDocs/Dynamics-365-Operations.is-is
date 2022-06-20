---
title: Stuðningur og endurnýjun
description: Þessi grein útskýrir hvernig á að setja upp og nota stuðnings- og endurnýjunarferlið á sölupöntunum til að búa til greiðsluáætlun fyrir endurnýjunarvörur.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b40e0136883d909755480a3ce101627297bd9ffb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896522"
---
# <a name="support-and-renewals"></a>Stuðningur og endurnýjun 

Þessi grein útskýrir hvernig á að færa inn stuðningsvörur eða endurnýjunarvörur þegar sölupantanir eru færðar inn. Þessir liðir eru notaðir til að reikna út gjaldupphæð fyrir upprunalega stuðningssamninginn og/eða endurnýjunarupphæðina sem er notuð þegar innheimtuáætlun er búin til í áskriftarreikningi. Til dæmis selur fyrirtækið þitt netþjón til viðskiptavinar og þú býður upp á gagnaafritunaráskrift fyrsta árið og möguleika á að endurnýja þá áskrift á hverju ári. The *stuðningslið* er áskrift fyrsta árið, og *endurnýjunaratriði* er endurnýjun fyrir hvert ár í röð.

Þú getur slegið inn upplýsingar fyrir stuðningssamninginn, endurnýjunarsamninginn eða hvort tveggja. Þegar þú slærð inn upplýsingar um stuðningssamninginn er aðeins stuðningsvörunum bætt við sölupöntunina. Þegar þú slærð inn upplýsingar um endurnýjunarsamning er endurnýjunarliðurinn notaður til að búa til innheimtuáætlun.

## <a name="support-and-renewal-setup"></a>Uppsetning stuðnings og endurnýjunar

Á **Stuðnings- og endurnýjunarstig** síðu geturðu sett upp mismunandi stuðningsstig fyrir stuðnings- og endurnýjunaratriði. Stuðningurinn eða endurnýjunin getur verið hlutfall af upphaflegri vöruupphæð, eða það getur verið staðlað upphæð.

Þú getur valið sjálfgefna stuðningsstig á **Endurteknar innheimtufæribreytur samnings** síðu.

Til dæmis gæti fyrirtæki boðið upp á eftirfarandi stuðnings- og endurnýjunarstig.

| Stuðningsstig | Þjónustuhlutfall | Prósenta endurnýjunar |
|---|---|---|
| Ótakmarkað | 40% | 30% |
| Gull | 25% | 18% |
| Silfurgrátt | 20% | 14% |
| Brons | 15% | 10% |

Til að búa til stuðnings- eða endurnýjunarstig skaltu fylgja þessum skrefum.

1. Á **Stuðnings- og endurnýjunarstig** síðu, veldu **Nýtt**.
2. Í **Stuðningsstig** reit, sláðu inn einstakt nafn.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í **Stuðningur við útreikningsaðferð** reit, veldu stuðningsútreikningsaðferðina. Ef þú velur **Prósenta**, sláðu inn stuðningsprósentu í **Stuðningshlutfall** sviði.
5. Í **Útreikningsaðferð endurnýjunar** reit skaltu velja endurnýjunarútreikningsaðferðina. Ef þú velur **Prósenta**, sláðu inn endurnýjunarprósentu í **Endurnýjunarprósenta** sviði.
6. Veldu **Vista**.

### <a name="fields"></a>Svæði

The **Stuðnings- og endurnýjunarstig** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|---|---|
| Stuðningsstig | Einstakt auðkenni fyrir stuðnings- eða endurnýjunarstigið (td, **Gull** eða **Silfur**). |
| Lýsing | Lýsing á stuðnings- eða endurnýjunarstigi. |
| Útreikningsaðferð þjónustu | Veldu stuðningsútreikningsaðferð fyrir stigið: **Prósenta** eða **Stöðluð upphæð**. |
| Þjónustuhlutfall | Ef þú valdir **Prósenta** sem stuðningsútreikningsaðferð, tilgreinið prósentuna sem er notuð til að reikna út verð stuðningshlutarins. Ef þú valdir **Stöðluð upphæð** sem útreikningsaðferð er upphæðin tilgreind þegar færslan er stofnuð. |
| Útreikningsaðferð endurnýjunar | Veldu endurnýjunarútreikningsaðferð fyrir stigið: **Prósenta** eða **Stöðluð upphæð**. |
| Prósenta endurnýjunar | Ef þú valdir **Prósenta** sem endurnýjunarútreikningsaðferð, tilgreinið prósentuna sem er notuð til að reikna út verð endurnýjunarhlutarins. Ef þú valdir **Stöðluð upphæð** sem útreikningsaðferð er upphæðin tilgreind þegar færslan er stofnuð. |

## <a name="support-and-renewal-process"></a>Þjónustu- og endurnýjunarferli

Stuðnings- og endurnýjunarvirknin getur beitt mismunandi stuðningsstigum á vörur og uppfært endurnýjunarupplýsingar í áskriftarreikningi.

Áður en þú notar stuðnings- og endurnýjunarvirknina verður að ljúka eftirfarandi verkefnum.

1. Á **Stuðnings- og endurnýjunarstig** síðu, búðu til að minnsta kosti eitt stuðnings- eða endurnýjunarstig.
2. Á **Uppsetning hlutar** síðu, tengja hlut við stuðnings- og endurnýjunaratriði. Þetta verkefni er aðeins nauðsynlegt ef þú vilt setja upp sjálfgefin gildi fyrir stuðnings- og/eða endurnýjunaratriði.
3. Á **Endurteknar innheimtufæribreytur samnings** síðu, tilgreindu sjálfgefna stuðnings- og endurnýjunarstillingar fyrir nýjar innheimtuáætlanir.

Fylgdu þessum skrefum til að beita mismunandi stuðningsstigum á vörur og uppfæra upplýsingar um endurnýjun.

1. Á **Allar sölupantanir** síðu, búðu til sölupöntun.
2. Á **Sölupöntunarlínur** Flýtiflipi, bættu við atriði.
3. Á **Reikningur** flipa, veldu **Stuðningur og endurnýjun \> Bættu við stuðningi og endurnýjun**.
4. Á **Stuðnings- og endurnýjunarferli** síðu, haushlutinn er uppfærður með stillingum frá **Endurteknar innheimtufæribreytur samnings** síðu. Þessi gildi eiga við um alla stuðnings- og endurnýjunarliði. (Til dæmis ef innheimtutíðni er stillt á **Árlega**, allar sölulínur sem eru búnar til sem hafa endurnýjunarvöru hafa árlega tíðni.) Til að tengja sölupöntunina við fyrirliggjandi innheimtuáætlun skaltu velja gildi í **Númer innheimtuáætlunar** sviði.
5. Til að breyta upphafsdegi stuðnings- eða endurnýjunar skaltu stilla **Hneka upphafsdagsetningu** valmöguleika til **Já**.
6. Til að bæta við eða breyta stuðningsatriðinu skaltu velja **Stuðningur** gátreitinn og sláðu síðan inn stuðningsatriði í **Stuðningsatriði** sviði. Vörunni er bætt við sölupöntunina.
7. Til að bæta við eða breyta endurnýjunaratriðinu skaltu velja **Endurnýjun** gátreitinn og sláðu síðan inn endurnýjunaratriði í **Endurnýjunaratriði** sviði. Þegar sölupöntunin er reikningsfærð verður innheimtuáætlun sem inniheldur vöruna búin til.
8. Veldu **Í lagi**.
9. Á **Mynda** flipa, veldu **Reikningur**. Þegar sölupöntunin er bókuð er innheimtuáætlun stofnuð. Tilkynning sem inniheldur upplýsingar um innheimtuáætlun birtist í skilaboðaupplýsingunum.
10. Á **Allar/virkar innheimtuáætlanir** listasíðu, veldu númer innheimtuáætlunar til að skoða upplýsingar um innheimtuáætlun á **Innheimtuáætlanir** síðu.
11. Á **Innheimtuáætlunarlínur** Flýtiflipi, veldu **Stuðningur og endurnýjun** til að fara yfir upplýsingar um línurnar sem voru búnar til.

> [!NOTE]
> Ef breyta þarf upphafsdegi endurnýjunar fyrir greiðsluáætlunarlínu geturðu breytt **Upphafsdagur** gildi fyrir línuna á **Innheimtuáætlanir** síðu. Þegar þú opnar **Skoða innheimtuupplýsingar** síða fyrir línuna, the **Upphafsdagur innheimtu** reiturinn er uppfærður með nýju dagsetningunni. The **Lokadagur innheimtu** gildi er endurreiknað miðað við innheimtutíðni. Aðeins er hægt að uppfæra upphafsdag endurnýjunar ef fyrsti reikningurinn fyrir endurnýjunarreikningsáætlun hefur ekki verið búinn til og bókaður. Eftir að fyrsti reikningurinn er búinn til og bókaður er ekki hægt að breyta upphafsdagsetningunni.

Stuðnings- og endurnýjunarferlið er aðeins í boði fyrir sölupöntunina. Þegar þú bætir stuðnings- og endurnýjunarvörum við sölupöntun geturðu búið til nýja innheimtuáætlun eða bætt endurnýjunaratriðinu við núverandi innheimtuáætlun.

## <a name="support-and-renewal-audit"></a>Eftirlit með þjónustu og endurnýjun

Á **Stuðnings- og endurnýjunarúttekt** síðu geturðu skoðað upplýsingarnar um innheimtuáætlunarlínur sem eru búnar til úr endurnýjunarvöru í sölupöntun. Þessi valkostur er tiltækur þegar innheimtuáætlunarlínan er endurnýjunaratriði.

Til að breyta stuðnings- og endurnýjunarupplýsingum fyrir greiðsluáætlunarlínu skaltu fylgja þessum skrefum.

1. Á **Allar innheimtuáætlanir** síðu, veldu númer innheimtuáætlunar.
2. Í **Innheimtuáætlunarlínur** kafla, veldu línu og veldu síðan **Stuðningur og endurnýjun**.
3. Skoðaðu allar upplýsingar um stuðnings- eða endurnýjunaratriðið.
4. Gerðu allar nauðsynlegar breytingar á stuðningsstigi, eða endurnýjunarprósentu eða upphæð, og sláðu síðan inn gildi í **Ástæða breytinga** sviði.
5. Veldu **Ferli**.

### <a name="fields"></a>Svæði

The **Stuðnings- og endurnýjunarúttekt** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|-------|-------------|
| Vörunúmer | Vörunúmerið fyrir innheimtuáætlunarlínuna. |
| Afurðarheiti | Vöruheitið. |
| Stig þjónustuáætlunar | Skoðaðu eða breyttu stuðningsstigi fyrir endurnýjunarhlutinn. |
| Prósenta endurnýjunar | Færið inn endurnýjunarprósentuna sem er notuð þegar einingarverð er reiknað fyrir endurnýjunarlið í innheimtuáætlun. |
| Upphæð endurnýjunar | Færið inn endurnýjunarupphæð sem er notuð þegar einingarverð er reiknað fyrir endurnýjunarlið í innheimtuáætlun. |
| Ástæða breytingar | Sláðu inn ástæðuna þína fyrir því að breyta stuðnings- og endurnýjunarupplýsingunum. Þú verður að slá inn ástæðu þegar þú breytir **Endurnýjunarprósenta**, **·**, eða **Stuðningsáætlunarstig** gildi. |
| Upphafleg söluvara | Upprunalega söluvörunúmerið úr sölupöntuninni. |
| Upphafleg nettóupphæð | Upprunalega nettóupphæð vörunnar. |
| Upphaflegt þjónustustig | Upprunalega stuðningsstigið fyrir hlutinn. |
| Upphafleg prósenta endurnýjunar | Upprunalega endurnýjunarprósentan fyrir hlutinn. |
| Upphafleg upphæð endurnýjunar | Upprunalega endurnýjunarupphæð vörunnar. |
| **Hnitanet** | |
| Upphaflegt þjónustustig | Fyrra stuðningsstig. |
| Upphafleg prósenta endurnýjunar | Fyrri endurnýjunarprósenta. |
| Upphafleg upphæð endurnýjunar | Fyrri endurnýjunarupphæð. |
| Breytt af | Notandanafn notandans sem gerði breytinguna. |
| Breytt dagsetning og tími | Dagsetningin þegar breytingin átti sér stað. |
| Ástæða | Ástæðan fyrir breytingunni. |

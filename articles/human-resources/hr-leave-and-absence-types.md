---
title: Grunnstilla gerðir leyfis og fjarvista
description: Settu upp tegundir orlofs sem starfsmenn geta tekið í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e35c5fed886ebf9a453c22b3e04ca9ffe50b6d70
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805205"
---
# <a name="configure-leave-and-absence-types"></a>Grunnstilla gerðir leyfis og fjarvista

[!include [preview banner](../includes/preview-banner.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Gerðir leyfa í Dynamics 365 Human Resources skilgreina hinar ýmsu gerðir fjarvista sem starfsmaður getur gefið upp. Þú getur sérsniðið leyfi eftir tegundum fyrirtækisins. Dæmi um orlofsgerðir eru:

- Greitt frí (PTO)
- Ógreidd leyfi
- Frí á launum
- Veikindaleyfi
- Læknaleyfi
- Fjölskylduleyfi
- Örorkubætur til skamms tíma
- Sorgarleyfi

## <a name="add-a-leave-type"></a>Bættu við leyfisgerð

1. Á  **Orlofs- og fjarveru** vinnusvæðinu velurðu  **Tenglar** flipann.
2. Undir **Skipulag**, veldu **Tegundir og leyfi**.
3. Veljið **Nýtt**.
4. Sláðu inn heiti fyrir leyfistegundina undir **Tegund**, sláðu inn lýsingu undir **Lýsing** og veldu verkflæði í  **Auðkenni verkflæðis** reitur. Byggt á leyfisgerðinni, veldu beiðnitegund reitinn **Tegund beiðni** . Veldu til dæmis **Frístund** eða **Fjarvistarleyfi**.
5. Í **Almennt**, veldu **Enginn**, **Áætlað** eða **Óáætlað** fellilistanum **Flokkur**.
6. Veldu launakóða úr fellilistanum **Vinnukóða**.
7. Undir **Ástæðukóða krafist** velurðu hvort þú vilt krefjast ástæðukóða. Ef þú vilt krefjast ástæðukóða gætirðu þurft að bæta þeim við. Undir **Ástæða númer**, veldu **Bæta við**, veldu ástæðukóða og veldu síðan **Virkt** gátreitinn við hliðina.
8. Ef tegund beiðninnar er **Fjarvistarleyfi** skaltu fylgja þessum skrefum:

      1. Undir **Opin ended** velurðu hvort notendur eigi að geta búið til opin blöð.
      2. Ef **Open ended** er virkt geturðu valið hvort starfsmenn þurfi að senda inn tilkynningu um endurkomu til vinnu þegar þeir koma úr leyfi frá störfum.
      3. Ef starfsmenn verða að senda inn tilkynningu um endurkomu til vinnu geturðu virkjað **Virkja tilkynningu um endurkomu til vinnu**. Ef kveikt er á **Enable return to work notice** er kveikt á **Viðhengi krafist** er sjálfkrafa virkt og ekki hægt að slökkva á því.

9. Ef notendur ættu að hlaða upp skjölum þegar þeir búa til eða uppfæra leyfisbeiðnir geturðu virkjað **Viðhengi krafist**.
10. Undir **Takmarka aðgang að völdum hlutverkum** velurðu hvort þú vilt takmarka aðgang. Síðan, undir **Öryggishlutverk fyrir þessa leyfistegund**, velurðu öryggishlutverkin. Öryggishlutverkin eru skilgreind í verkflæðinu sem þú valdir undir **Auðkenni verkflæðis** fyrr í þessu ferli.
11. Undir **Dagatalslitur** skaltu velja litinn sem á að sýna í orlofs- og fjarvistadagatölum fyrir þessa orlofstegund.
11. Undir **Svössunartengsl** skal velja hvort þessi orlofstegund eigi annaðhvort að fresta annarri orlofstegund eða vera frestað af annarri orlofstegund. Þegar beiðni um fjarvist er send inn fyrir frestaða leyfisgerð verður frestun leyfis sjálfkrafa búin til fyrir frestaða leyfisgerð.
12. Veldu **Vista**.

## <a name="configure-leave-type-rules"></a>Stilla reglur leyfisgerða

1. Stilltu námundunarvalkosti fyrir tegundina **Orlof og fjarveru** . Valkostir fela í sér **Enginn**, **Upp**, **Niður** og **Næst**. Þú getur einnig stillt námundun námundunar fyrir orlofstegundina.
2. Stilltu **Leiðrétting á fríi** til að námunda fyrir orlofstegundina. Þegar þú velur þennan valkost verður fjöldi frídaga sem dettur niður á vinnudegi notaður til að ákvarða hvernig á að safna fríi fyrir leyfisgerðina. Til dæmis, ef jóladagur fellur á mánudag, dregur Human Resources einn dag frá orlofstegundinni þegar unnið er með uppsafnanir.

   Frí er stillt í vinnutímadagatalinu. Nánari upplýsingar eru í [Búa til dagatal fyrir vinnutíma](hr-leave-and-absence-working-time-calendar.md).
   
 3. Stillið **Yfirfærð leyfisgerð** fyrir leyfisgerð. Þegar þessi valkostur er valinn verða allar yfirfærðar stöður fluttar í tilgreinda gerð leyfis. Yfirfærsluleyfisgerðin þarf einnig að vera með í áætlun um leyfi og fjarveru. 
 
4. Skilgreinið **Gildistímareglur** fyrir leyfisgerðina. Þegar þessi valkostur er skilgreindur er hægt að velja einingu daga eða mánaða og stilla tímalengd gildistímans. Gildisdagsetning gildistímareglu er notuð til að ákvarða hvenær á að hefja keyrslu runuvinnslunnar sem vinnur úr gildistíma leyfis eða dagsetninguna þegar reglan tekur gildi. Gildistíminn mun alltaf sjást í upphafsdagsetningu uppsafnaðs tímabils. Ef til dæmis upphafsdagur uppsöfnunartímabils er 3. ágúst 2021 og gildistímareglan var sett á 6 mánuði, verður reglan unnin með hliðsjón af lokadeginum frá upphafsdegi uppsöfnunartímabilsins, þannig að hún yrði framkvæmd 3. febrúar 2022. Allar leyfisstöður sem eru til staðar þegar gildistíminn rennur út verða dregnar frá leyfisgerðinni og teknar inn í leyfsstöðuna.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>Skilgreina nauðsynlegt viðhengi fyrir hverja gerð leyfis

> [!NOTE]
> Til að nota reitinn **Viðhengi er nauðsynlegt** þarf fyrst að kveikja á eiginleikanum **Skilgreina áskilið viðhengi fyrir leyfisbeiðnir** í eiginleikastjórnun. Frekari upplýsingar um hvernig á að kveikja á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

1. Á síðunni **Leyfi og fjarvistir**, í flipanum **Tenglar**, undir **Uppsetning**, skal velja **Leyfis- og fjarvistagerðir**.

2. Veldu a **Orlofs- og fjarvistartegund** á listanum. Í **Almennt** hlutanum skaltu nota reitinn **Viðhengi krafist** til að tilgreina hvort viðhengi verði að hlaða upp þegar starfsmaður sendir inn ný orlofsbeiðni fyrir valda orlofstegund. 

Starfsmenn þurfa að hlaða upp viðhengi þegar þeir senda inn nýja leyfisbeiðni sem er með leyfisgerðina þar sem reiturinn **Viðhengi er nauðsynlegt** er virkjaður. Til að skoða viðhengið sem var hlaðið upp sem hluta af leyfisbeiðni geta samþykktaraðilar leyfisbeiðni notað valkostinn **Viðhengi** fyrir vinnuliðina sem þeim er úthlutað. Ef farið er inn í leyfisbeiðni með því að nota forrit Human Resources í Microsoft Teams er hægt að nota valkostinn **Skoða upplýsingar** fyrir leyfisbeiðnina til að skoða upplýsingar um hana og öll viðhengi.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Stilla leyfiseiningar (klukkustundir/dagar) fyrir hverja leyfisgerð

> [!NOTE]
> Til að nota leyfiseiningar á hverja virkni leyfisgerðar þarf fyrst að kveikja á eiginleikanum **Stilla leyfiseiningar fyrir hverja leyfisgerð** í eiginleikastjórnun. Frekari upplýsingar um hvernig á að kveikja á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

> [!IMPORTANT]
> Sjálfgefið er að leyfisgerðir í lögaðila noti leyfiseiningar úr skilgreiningu leyfisfæribreytum á stigi lögaðila.
> 
> Leyfiseiningu af leyfis- og fjarvistagerð er hægt að breyta eingöngu ef engar leyfisfærslur eru til fyrir leyfisgerðina.
> 
> Ekki er hægt að slökkva á eiginleikanum eftir að kveikt hefur verið á honum.

1. Á síðunni **Leyfi og fjarvistir**, í flipanum **Tenglar**, undir **Uppsetning**, skal velja **Leyfis- og fjarvistagerðir**.

2. Veldu leyfis- og fjarvistagerð í listanum. Því næst, í hlutanum **Almennt**, í reitnum **Eining**, skal velja leyfiseininguna. Hægt er að velja **Klukkustundir** eða **Daga**.

3. Valfrjálst: Ef þú valdir **Klukkustundir** í reitnum **Eining** getur þú notað reitinn **Virkja skilgreiningu hálfs dags** til að tilgreina hvort starfsmenn geti valið fyrri hluta eða seinni hluta dags í frí ef þeir óska eftir hálfs dags leyfi.

Starfsmenn sem senda inn nýja leyfisbeiðni geta valið úr mismunandi leyfisgerðum til að setja saman leyfsbeiðnina. Allar leyfisgerðir sem eru valdar sem hluti af einni leyfisbeiðni eiga að vera með sömu leyfiseininguna. Starfsmenn geta skoðað leyfiseininguna fyrir hverja leyfisgerð í skjámyndinni **Beiðni um frí**.

## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)
- [Búa til leyfis- og fjarvistaáætlun](hr-leave-and-absence-plans.md)
- [Búa til dagatal fyrir vinnutíma](hr-leave-and-absence-working-time-calendar.md)
- [Fresta leyfi](hr-leave-and-absence-suspend-leave.md)
- [Búa til verkflæði fyrir beiðni um kaup og sölu á leyfisdögum](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

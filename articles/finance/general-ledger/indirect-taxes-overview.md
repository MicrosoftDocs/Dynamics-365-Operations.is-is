---
title: Yfirlit virðisaukaskatts
description: Þetta efnisatriði veitir yfirlit yfir kerfi virðisaukaskatts. Það útskýrir þættina í uppsetningu virðisaukaskatts og hvernig þeir vinna saman.
author: ShylaThompson
manager: AnnBe
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3dacc755b3d4d3b5c7f51f6bac7c2e9c62773ba
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444433"
---
# <a name="sales-tax-overview"></a>Yfirlit virðisaukaskatts

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir kerfi virðisaukaskatts. Það útskýrir þættina í uppsetningu virðisaukaskatts og hvernig þeir vinna saman.

<a name="overview"></a>Yfirlit
--------

Vsk-ramminn°styður margar gerðir óbeinna skatta, s.s. söluskatt, virðisaukaskatt (VAT), skatt á vörur og þjónustu (GST), einingagjöld, og staðgreiðsluskatt. Þessar skattar eru reiknaðir og skráðir við innkaup og sölu. Reglulega þarf að tilkynna vsk og greiða hann til skattayfirvalda. 

Eftirfarandi skýringarmynd sýnir einingar í skattauppsetningu og hvernig þær eru tengdar.

[![Skýringarmynd sem sýnir yfirlit yfir skattauppsetningareiningar](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Fyrir hvert vsk sem fyrirtæki verður að standa skil á þarf vsk-kóða að vera skilgreindur. Vsk-kóði geymir skatthlutfall og útreikningsreglur°fyrir vsk. 

Hver vsk-kóði verður að vera°tengdur við vsk-tímabil. VSK-uppgjörstímabil°skilgreina með hvaða millibili á að gefa upp vsk og greiða til skattayfirvalda. Hvert vsk-uppgjörstímabil þarf að tengja við skattayfirvöld. Skattayfirvöld standa fyrir lögaðilann sem vsk er gefinn upp og greiddur til. Hann skilgreinir einnig útlit vsk-skýrslunnar. Hægt er að tengja skattayfirvöld lánardrottnalyklum. Nánari upplýsingar, sjá [Setja upp VSK-uppgjörstímabil](tasks/set-up-sales-tax-settlement-periods.md).

Hvern vsk-kóða þarf einnig að°tengja við fjárhagsbókunarflokk. Fjárhagsbókunarflokkur tilgreinir aðallykla sem upphæðir vsk-kóða varða bókaðar fyrir. 

Einnig er hægt að skilgreina valfrjálsa skýrslugerðarkóða virðisaukaskatts. Hægt er að úthluta þeim á vsk-kóðum fyrir mismunandi gerðir°upphæða sem reiknaðar eru út fyrir vsk-kóða. Í skýrslunni **Vsk-greiðsla eftir kóða** sjást samtölur fyrir vsk-skýrslukóða fyrir ákveðið vsk-tímabil og millibil. 

VSK-flokkur og VSK-flokkur vöru verða að tengjast hverri færslu sem snertir virðisaukaskatt. Vsk-flokkar eru tengdir aðila (til dæmis,°viðskiptavinur eða lánardrottinn) færslunnar, á meðan vsk-flokkar vöru tengjast tilfangi (til dæmis,°vöru eða innkaupa tegund)°færslunnar. Vsk-flokkar inniheldur lista yfir vsk-kóða. Skattkóðar sem eru til staðar fyrir bæði vsk-flokk og vsk-flokk fyrir færslu vöru eru skattkóðar sem eiga við þá færslu. 

Eftirfarandi tafla lýsir einingar sem og röð fyrir uppsetningu skatti.

| Uppsetningarverkþáttur                                                  | Bundið/valfrjálst og lýsing                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stofna aðallykla.                                           | Áskilið. Áður en virðisaukaskatturinn er settur upp verður að stofna fjárhagslyklana sem fyrirtækið notar til að greiða og skrá skatta.                                                                                                                                                                             |
| Setja upp fjárhagsbókunarflokka fyrir virðisaukaskatt.                     | Áskilið. Fjárhagsbókunarflokkar skilgreina aðallykla til að skrá og greiða°virðisaukaskatt.   Nánari upplýsingar er að finna í [Setja upp bókunarflokka virðisaukaskatts](tasks/set-up-ledger-posting-groups-sales-tax.md).                                                                                 |
| Setja upp skattayfirvöld.                                   | Áskilið. Skattayfirvöld eru þeir lögaðilar sem skattur verður tilkynntur og greiddur til.    Nánari upplýsingar um það eru í [Setja upp VSK-yfirvöld](tasks/set-up-sales-tax-authorities.md).                                                                                                                                          |
| Setja upp virðisaukaskatttímabil.                            | Áskilið. Virðisaukaskattstímabil°innihalda upplýsingar um°hvenær og hve oft eigi að tilkynna og greiða vsk. Þær eru tengdar við vsk-yfirvöld.                                                                                                                                                       |
| Uppsetning skýrslugerðarkóða virðisaukaskatts.                               | Valfrjálst. Skýrslugerðarkóða virðisaukaskatts er hægt að úthluta til vsk-kóða til að gefa skýrslu um upphæðir fyrir marga vsk-kóða undir einum skýrslugerðarkóða virðisaukaskatts. Nánari upplýsingar um það eru í [Setja upp VSK-skýrslugerðarkóða](tasks/set-up-sales-tax-reporting-codes.md).                                         |
| Setja upp VSK-kóða.                                         | Áskilið. Vsk-kóðar geymir skatthlutfall og°útreikningsreglur fyrir vsk. VSK-kóðar eru tengdir virðisaukaskatttímabili, og fjárhagsbókunarflokki. Nánari upplýsingar um það eru í [Setja upp VSK-kóða](tasks/set-up-sales-tax-codes.md).                                |
| Setja upp VSK-flokka.                                        | Áskilið. Vsk-flokkar inniheldur lista yfir sölukóða sem eiga við um aðila (viðskiptavinur eða lánardrottinn) færslu. Fyrir tilgreinda færslu ákveða°skurðpunktar°vsk-kóða í°vsk-flokki og vsk-flokkur vöru þá vsk-kóða sem eiga við þá færslu.                  |
| Setja upp VSK-flokka vöru.                                   | Áskilið. Vsk-flokkar vöru innihalda lista yfir sölukóða°sem eiga við°um tilföng°(afurðir, þjónustu og svo framvegis) færslu. Fyrir tilgreinda færslu ákveða°skurðpunktar°vsk-kóða í°vsk-flokki og vsk-flokkur vöru þá vsk-kóða sem eiga við þá færslu. Frekari upplýsingar, sjá [Setja upp VSK-flokka og VSK-flokka fyrir vörur](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md). |
| Setja upp færibreytur fyrir vsk á síðum forrits færibreytu. | Áskilið. Fyrir mismunandi svæði, eins og Fjárhagur, Viðskiptakröfur og viðskiptaskuldir, verður að setja upp færibreytur fyrir réttan útreikning á óbeinum sköttum. Þótt þessar færibreytur hafi flestar sjálfgildi, verður að aðlaga þær til að mæta kröfum fyrir hvert fyrirtæki.                                          |

## <a name="sales-tax-on-transactions"></a>Virðisaukaskattsfærslur
Á hverja færslu (sölu-/ innkaupaskjalalínur,°færslubækur og svo framvegis), þarf að færa vsk-flokk og vsk-flokk vöru til að reikna út virðisaukaskatt. Sjálfgefnir flokkar eru tilgreindir í aðalgögnum (t.d.°viðskiptavinir, lánardrottinn, vara og innkaupategund) en handvirkt er hægt°að breyta flokkum°á færslu ef þarf. Báðir flokkar innihalda lista yfir vsk-kóða og skurðpunktur listanna tveggja yfir vsk-kóða ákvarðar lista yfir viðeigandi vsk-kóða fyrir færsluna. 

Á hverri færslu er hægt að fletta upp reiknuðum virðisaukaskatti eftir opnun á **Vsk-færslan** síðu. Hægt er að fletta upp virðisaukaskatti fyrir línu skjals eða allt skjalið. Fyrir ákveðin skjöl (t.d.°reikning lánardrottins og almennar°færslubækur), er hægt að leiðrétta reiknaðan virðisaukaskatt ef upphaflega skjalið sýnir afbrigðilegar upphæðir.

## <a name="sales-tax-settlement-and-reporting"></a>Virðisaukauppgjör og skýrslugjöf
Virðisaukaskatt verður að tilkynna og greiða til skattayfirvalda með ákvörðuðu millibili (mánaðarlega, ársfjórðungslega, og svo framvegis). Hægt er að jafna skattlykla fyrir tímabilið og mótfæra stöður við jöfnun skattlykils, eins og tilgreint er í flokkum fjárhagsbókunar. Þessi aðgerð er hægt að fara á **Jafna og bóka vsk** síðunni. Tilgreina verður vsk-uppgjörstímabil sem á að jafna vsk fyrir. 

Eftir°að búið er að greiða vsk ætti að jafna stöðu á reikningi virðisaukaskattsuppgjörs gagnvart bankareikningnum. Ef vsk-yfirvöld sem tilgreind eru í vsk-uppgjörstímabili eru tengd lánardrottnalykli er vsk-staða bókuð sem opinn lánardrottnareikningur og hægt að taka með í reglulegu greiðslutillögunni.

## <a name="conditional-sales-tax"></a>Skilyrtur VSK
Skilyrtur virðisaukaskattur er virðisaukaskattur sem er greiddur hlutfallslega miðað við raunupphæðina sem greiða á samkvæmt reikningi. Venjulegur söluskattur er hins vegar reiknaður út við reikningsfærslu. Skilyrtan virðisaukaskatt þarf að greiða til virðisaukaskattsyfirvalds þegar greiðsla er bókuð, ekki þegar reikningurinn er bókaður. Þegar reikningur er bókaður verður færslan að vera tilkynnt í skýrslu VSK-bókar. Færslan verður hins vegar að vera tekin út úr VSK-greiðsluskýrslu. 

Ef gátreiturinn Skilyrtur söluskattur er valinn í færibreytuskjámynd fyrir fjárhag er ekki hægt að draga frá neinn söluskatt fyrr en reikningurinn hefur verið greiddur. Þetta er áskilið samkvæmt lögum á sumum löndum/svæðum.

> [!NOTE]
> Ef gátreitur fyrir skilyrtan söluskatt er valinn verður að setja upp vsk-kóða og vsk-hópa og einnig stofna fjárhagsbókunarflokka til að styðja þá virkni. |

###  <a name="example"></a>Dæmi

Skattar eru gerðir upp mánaðarlega. Júní 15, er stofnaður reikningur viðskiptavinar sem nemur 10.000, auk VSK.
-   Virðisaukaskattur er 25 prósent, eða 2.500.
-   Upphæðin á reikningnum kemur til greiðslu 30. júlí.

Almennt yrðir þú að gera upp og greiða 2.500 til skattyfirvalds þegar reikningur er bókaður í júní, jafnvel þótt greiðsla frá viðskiptavinir hafi ekki enn borist. 

Ef þú notar hins vegar skilyrtan virðisaukaskatt er gert upp við skattyfirvöld þegar þú færð greiðslu frá viðskiptavini þann 30. júlí.

### <a name="postdated-check"></a>Fyrirframdagsett ávísun

Ef þú notar útreiknaða ávísun sem greiðslumáta, þegar greiðslan er stofnuð, er bankareikningurinn ekki hreinsaður. Í sumum löndum verður virðisaukaskatturinn „innleyst“ ábyrgð þegar greiðslan hreinsar bankann, sem þýðir að fyrirframgreidd ávísun er gerð upp. Þú getur gert það kleift með því að velja **Innleysa skilyrtan skatt þegar fyrirframgreiddar ávísanir eru gefnar út** í **Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar > Fyrirframdagsettar ávísanir**.

Nánari upplýsingar um það eru í [Setja upp staðgreiðsluskattur](tasks/set-up-withholding-tax.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
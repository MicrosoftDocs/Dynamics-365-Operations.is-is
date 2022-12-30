---
title: Áætlanir byggðar á verðtilboðum og beiðni um tilboð
description: Þessi grein lýsir því hvernig á að setja upp aðaláætlanagerð til að taka til greina tilboð og tilboðsbeiðni þegar hún býr til áætlaðar pantanir.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690167"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Áætlun byggð á verðtilboðum og beiðni um tilboð

[!include [banner](../../includes/banner.md)]

Tilboð og beiðnir um tilboð (RFQ) tákna mögulegar eða jafnvel líklegar pantanir í framtíðinni. Þess vegna er skynsamlegt að taka þær til greina við aðaláætlanagerð, svo hægt sé að skipuleggja aukaframboð miðað við fyrirliggjandi tilboðsbeiðnir og líkur á að hvert tilboð verði að raunverulegri pöntun. Þessi grein lýsir því hvernig á að setja upp aðaláætlanagerð til að taka til greina tilboð og tilboðsbeiðnir þegar hún býr til áætlaðar pantanir.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Setja upp aðalskipulag til að íhuga sölutilboð og/eða tilboðsbeiðni

Notaðu eftirfarandi ferli til að setja upp aðaláætlanagerð til að taka til greina verðtilboð og/eða tilboðsbeiðnir.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veldu núverandi aðaláætlun á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan.
1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Taka með sölutilboð** – Stilltu þennan valkost á *Já* til að taka til greina sölutilboð þegar núverandi áætlun er keyrð. Stilla það á *Nei* til að hunsa.
    - **Líkur %** – Stilltu lágmarksstig trausts sem þarf til að tilboð sé tekið með í aðalskipulagi. Útreikningur aðalskipulags mun innihalda öll verðtilboð sem voru búin til úr tækifærum sem hafa þetta líkindahlutfall eða hærra. Til að taka með öll tilboð, þ.m.t. tilboð sem eru með engar líkur úthlutaðar eða engin tækifæri tengd við þau skal stilla þenna reit á *0* (núll). Frekari upplýsingar um líkur fyrir verðtilboð er að finna í næsta kafla.
    - **Taka með tilboðsbeiðnir** – Stilltu þennan valkost á *Já* til að taka til greina tilboðsbeiðnir þegar núverandi áætlun er keyrð. Stilla það á *Nei* til að hunsa. Ef þú velur að taka til greina tilboðsbeiðnir mun kerfið stofna innkaupatillögur fyrir þær, en mun ekki tilgreina lánardrottin fyrr en tilboðsbeiðnin er afgreidd. Fyrirhugaðar innkaupapantanir sem eru stofnaðar fyrir beiðni um tilboð gætu haft áhrif á magn annarra áætlaðra pantana.

1. Haltu áfram að setja upp aðalskipulagið á venjulegan hátt.

## <a name="assign-and-view-probabilities-for-quotations"></a>Úthluta og skoða líkur fyrir tilboð

Eins og nefnt var í fyrri hlutanum mun aðalskipulag aðeins taka tilboð sem uppfylla eða fara yfir líkindamörk sem skilgreind eru fyrir áætlunina (ef þröskuldur er skilgreindur). Líkurnar eru þó ekki stilltar beint á hvert tilboð. Þess í stað er hún afleidd af tækifærin sem var notað til að búa til tilboðið. Þess vegna munu tilboð sem eru búin til beint á síðunni **Öll tilboð** ekki vera með líkur úthlutaðar eða tækifæri tengd við þau og þau verða aldrei tekin til greina af aðaláætlanagerð (nema reiturinn **Líkur %** sé stilltur á *0* \[núll\]). Til að fá líkur úthlutaðar verður að búa til tilboð úr tækifæri.

### <a name="create-a-quotation-from-an-opportunity"></a>Stofna tilboð úr tækifæri

Notaðu eftirfarandi ferli til að úthluta líkum á tækifæri og búa síðan til tilboð úr tækifærinu.

1. Faraðu í **Sala og markaðssetning \> Vensl \> Tækifæri \> Öll tækifæri**.
1. Veldu núverandi tækifæri eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýtt.
1. Fylltu út tækifærissíðuna til að auðkenna tækifærið eins og þú vilt. Gættu þess að stilla **Líkindi** reitinn á viðeigandi gildi. Aðeins aðaláætlanir sem eru settar upp til að leita að líkum á þessu gildi eða hærra mun taka til greina tilboð sem eru mynduð úr þessu tækifæri.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðasvæðinu, í flipanum **Tækifæri**, í hópnum **Nýtt**, skal velja **Sölutilboð** eða **Verktilboð** eftir því hvers konar tilboð á að búa til.
1. Í svarglugganum **Stofna tilboð** skal stilla reitina eftir þörfum og velja síðan **Í lagi**.
1. Nýtt verðtilboð er stofnað og opnað. Í flýtiflipanum **Línur** skal nota tækjastiku til að bæta við sölulínum eða verklínum eftir þörfum til að skilgreina efni tilboðsins.
1. Í aðgerðarúðunni skal velja **Vista**. Lokaðu síðan tilboðinu.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Skoða líkurnar á því að því sé úthlutað í verðtilboð

Eina leiðin til að skoða líkurnar sem úthlutað er á tilboð er að opna tækifærið sem var notað til að stofna tilboðið eins og lýst er í eftirfarandi ferli.

1. Opnið **Sala og markaðsstarf \> Sölutilboð \> Öll tilboð**.
1. Ef dálkurinn **Tækifæriskenni** er ekki sýndur (hann er falinn í sjálfgefinni uppsetningu) skal fylgja þessum skrefum til að sýna hann tímabundið. (Önnur leið til að halda dálknum **Tækifæriskenni** tiltækum er að búa til [vistað yfirlit](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json) sem inniheldur hann.)

    1. Veljið og haldið (eða hægrismellið) í töflunni og veljið svo **Setja inn dálka**.
    1. Í svarglugganum **Setja inn dálka** skal finna línuna þar sem reiturinn **Reitur** er stilltur á *Tækifæri* og velja gátreitinn **Velja** fyrir þá línu.
    1. Veldu **Uppfæra** til að bæta völdum dálki við síðuna **Öll tilboð**.

1. Í hnitanetinu skal finna línuna fyrir viðkomandi tilboð. Í dálknum **Tækifæriskenni** skal síðan velja gildið fyrir þá línu.

    > [!NOTE]
    > Ef þú ert að leita að verktilboði gætirðu þurft að velja dálkhausinn **Gerð tilboðs** og hreins síuna. Í sjálfgefinni uppsetningu er þessi sía stillt þannig að aðeins sölutilboð eru sýnd.

1. Tengt tækifæri er opnað. Þú getur nú skoðað og breytt gildinu **Líkindi** eins og þú þarft.

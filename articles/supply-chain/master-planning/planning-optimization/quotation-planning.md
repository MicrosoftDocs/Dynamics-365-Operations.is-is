---
title: Áætlanir byggðar á tilvitnunum og tilboðum
description: Þessi grein lýsir því hvernig á að setja upp aðalskipulagningu til að taka tillit til tilboða og tilboðsbeiðna (RFQs) þegar hún býr til áætlaðar pantanir.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690167"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Áætlun byggt á tilvitnunum og tilboðum

[!include [banner](../../includes/banner.md)]

Tilvitnanir og beiðnir um tilboð (RFQs) tákna mögulegar eða jafnvel líklegar framtíðarpantanir. Þess vegna er skynsamlegt að huga að þeim við aðalskipulagningu, svo að hægt sé að skipuleggja aukaframboð út frá núverandi tilboðum og líkum á því að hver tilboð verði raunveruleg pöntun. Þessi grein lýsir því hvernig á að setja upp aðaláætlanagerð til að taka tillit til tilboða og tilboða þegar hún býr til áætlaðar pantanir.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Settu upp aðalskipulagningu til að íhuga sölutilboð og/eða beiðnir

Notaðu eftirfarandi ferli til að setja upp aðalskipulagningu til að taka tillit til sölutilboða og/eða tilboða.

1. Fara til **Aðalskipulag \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veldu núverandi áætlun í listaglugganum eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýjan.
1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Láttu sölutilboð fylgja með** – Stilltu þennan valkost á *Já* að huga að sölutilboðum þegar núverandi áætlun er keyrð. Stilltu það á *Nei* að hunsa þá.
    - **Líkur %** – Stilltu lágmarksöryggi sem þarf til að tilboð sé innifalið í aðalskipulagi. Aðalskipulagsútreikningurinn mun innihalda allar tilvitnanir sem voru búnar til úr tækifærum sem hafa þessa líkindaprósentu eða hærri. Til að taka með allar tilvitnanir, þar með talið tilvitnanir sem engar líkur eru á þeim eða engin tækifæri tengd þeim, stilltu þennan reit á *0* (núll). Fyrir frekari upplýsingar um líkur á tilvitnunum, sjá næsta kafla.
    - **Látið fylgja beiðnir um tilboð** – Stilltu þennan valkost á *Já* að huga að tilboðum þegar núverandi áætlun er keyrð. Stilltu það á *Nei* að hunsa þá. Ef þú velur að íhuga beiðnir um beiðnir, mun kerfið búa til fyrirhugaðar innkaupapantanir fyrir þær, en það mun ekki tilgreina lánardrottinn fyrr en beiðni um beiðni er leyst. Áætlaðar innkaupapantanir sem eru búnar til fyrir tilboðsbeiðnirnar gætu haft áhrif á magn annarra fyrirhugaðra pantana.

1. Haltu áfram að setja upp aðalskipulagið þitt á venjulegan hátt.

## <a name="assign-and-view-probabilities-for-quotations"></a>Úthlutaðu og skoðaðu líkur fyrir tilvitnanir

Eins og fram kom í kaflanum hér á undan tekur aðalskipulag aðeins tilvitnanir sem standast eða fara yfir líkindamörkin sem skilgreind eru fyrir áætlunina (ef viðmiðunarmörk eru skilgreind). Hins vegar eru líkurnar ekki stilltar beint á hverja tilvitnun. Þess í stað er það erft frá tækifærinu sem var notað til að búa til tilvitnunina. Því tilvitnanir sem eru búnar til beint á **Allar tilvitnanir** síðu mun ekki hafa úthlutað líkum eða tækifæri tengt þeim og þær verða aldrei teknar til greina í aðalskipulagi (nema **Líkur %** reiturinn er stilltur á *0*\[ núll\]). Til að fá úthlutað líkum á það verður að búa til tilvitnun úr tækifæri.

### <a name="create-a-quotation-from-an-opportunity"></a>Búðu til tilvitnun úr tækifæri

Notaðu eftirfarandi aðferð til að úthluta líkum á tækifæri og búðu síðan til tilvitnun úr því tækifæri.

1. Fara til **Sala og markaðssetning \> Sambönd \> Tækifæri \> Öll tækifæri**.
1. Veldu núverandi tækifæri, eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýjan.
1. Fylltu út tækifærissíðuna til að auðkenna tækifærið eins og þú vilt. Vertu viss um að stilla **Líkur** reit í viðeigandi gildi. Aðeins aðaláætlanir sem eru settar upp til að leita að líkum af þessu gildi eða hærra munu taka tilvitnanir sem eru búnar til frá þessu tækifæri.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðarrúðunni, á **Tækifæri** flipa, í **Nýtt** hópur, veldu **Sölutilboð** eða **Verktilvitnun**, allt eftir tegund tilboðsins sem þú vilt búa til.
1. Í **Búðu til tilvitnun** valmynd, stilltu reitina eins og þú vilt og veldu síðan **Allt í lagi**.
1. Ný tilvitnun er búin til og opnuð. Á **Línur** Flýtiflipi, notaðu tækjastikuna til að bæta við sölulínum eða verklínum eftir þörfum til að skilgreina innihald tilboðsins.
1. Í aðgerðarúðunni skal velja **Vista**. Lokaðu síðan tilvitnuninni.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Skoðaðu líkurnar á tilvitnun

Eina leiðin til að skoða líkurnar sem eru úthlutaðar á tilboð er að opna tækifærið sem var notað til að búa til tilboðið, eins og lýst er í eftirfarandi ferli.

1. Fara til **Sala og markaðssetning \> Sölutilboð \> Allar tilvitnanir**.
1. Ef **Tækifæri auðkenni** dálkurinn er ekki sýndur (hann er falinn í sjálfgefna uppsetningu), fylgdu þessum skrefum til að sýna hann tímabundið. (Að öðrum kosti, til að halda **Tækifæri auðkenni** dálkur í boði, búa til a [vistað útsýni](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json) það felur í sér.)

    1. Veldu og haltu inni (eða hægrismelltu) í hnitanetinu og veldu síðan **Settu inn dálka**.
    1. Í **Settu inn dálka** valmynd, finndu röðina þar sem **Field** reiturinn er stilltur á *Tækifæri*, og veldu **Veldu** gátreit fyrir þá línu.
    1. Veldu **Uppfærsla** til að bæta völdum dálki við **Allar tilvitnanir** síðu.

1. Finndu línuna fyrir viðeigandi tilvitnun í hnitanetinu. Síðan, í **Tækifæri auðkenni** dálki, veldu gildið fyrir þá línu.

    > [!NOTE]
    > Ef þú ert að leita að verktilboði gætirðu þurft að velja **Tilvitnunartegund** dálkhaus og hreinsaðu síuna hans. Í sjálfgefna uppsetningu er þessi sía stillt þannig að aðeins sölutilboð eru sýnd.

1. Tengd tækifæri opnast. Þú getur nú skoðað og breytt **Líkur** gildi eins og þú þarfnast.

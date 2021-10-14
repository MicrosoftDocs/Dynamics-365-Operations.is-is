---
title: Kostnaðarverð skilavöru og lotukenni skila
description: Þú gætir viljað að kostnaður skilavaranna jafngildi kostnaði varanna á þeim tíma þegar þú seldir vörurnar til viðskiptavinarins. Þú getur gert þetta með því að nota **Lotukenni skila**.
author: kamaybac
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c5ad2f7e46ecefd490936b950d2b579faed60b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580337"
---
# <a name="return-cost-price-and-return-lot-id"></a>Kostnaðarverð skilavöru og lotukenni skila        

[!include [banner](../includes/banner.md)]



Kostnaður við vörur sem er skilað til birgða er reiknaður með því að nota núverandi kostnað vörunnar. Hins vegar gætir þú viljað að kostnaður skilavaranna jafngildi kostnaði varanna á þeim tíma þegar þú seldir vörurnar til viðskiptavinarins. Þú getur gert þetta með því að nota reitinn **Lotukenni skila** á flýtiflipanum **Línuupplýsingar** í skjámyndinni **Sölupöntun**.

Íhugaðu til dæmis eftirfarandi atburðarás. Þú sendir viðskiptavini reikning. Síðan skilar viðskiptavinurinn afgreiddum vörum til þín. Þú skilar vörunum á lager. Í þessu tilviki, þegar þú kreditfærir viðskiptavininn vegna skilavaranna, er kostnaður þessara vara reiknaður út með því að nota núverandi kostnað varanna. Hins vegar, ef þú notar reitinn **Lotukenni skila**, er kostnaðurinn á skilavörunum reiknaður út með því að nota kostnað á reikningi upprunalegu sölunnar til viðskiptavinar.

Til að nota annan kostnað en núverandi kostnað vegna skila viðskiptavinar skaltu nota eina af eftirfarandi aðferðum.

## <a name="method-1-manually-enter-the-return-cost-price"></a>Aðferð 1: Sláðu inn handvirkt kostnaðarverð skila

Að sjálfgefnu, þegar þú bætir vörum við skilapöntun, er vörunum skilað til birgða á núverandi kostnaðarverði. Til að tilgreina annað kostnaðarverð skila skaltu fylgja þessum skrefum.

1.  Smelltu á **Sala og markaðssetning** \> **Almennt** \> **Skilapantanir** \> **Allar skilapantanir**.

2.  Í **Aðgerðarsvæði**, í flokknum **Nýtt**, skaltu smella á **Skilapöntun**.

3.  Í skjámyndinni **Stofna skilapöntun** skaltu velja viðskiptavinalykil og smella síðan á **Í lagi**.

4.  Í skjámyndinni **Skilapöntun - RMA-númer: %1, %2** velurðu vöru og slærð síðan inn neikvætt magn í reitinn **Magn**.

5.  Smellið á flýtiflipa **Upplýsingar um línur**.

6.  Á flipanum **Almennt** skaltu færa inn gildi í reitinn **Kostnaðarverð skila**. Þetta gildi er notað þegar vörunum er skilað til birgða. Ef þú færir ekki inn gildi er núverandi kostnaðarverð notað þegar vörunum er skilað til birgða.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>Aðferð 2: Búa til kostnaðarverð sjálfkrafa byggt á reikningslínu viðskiptavinar

Þetta er æskilega aðferðin til að búa til skilalínur. Til að nota kostnað vörunnar á þeim tíma sem þú seldir vörurnar til viðskiptavinarins skaltu búa til skilapöntun og tilgreina sölulínu til að skila.

1.  Smelltu á **Sala og markaðssetning** \> **Almennt** \> **Skilapantanir** \> **Allar skilapantanir**.

2.  Í **Aðgerðarsvæði**, í flokknum **Nýtt**, skaltu smella á **Skilapöntun**.

3.  Í skjámyndinni **Stofna skilapöntun** skaltu velja viðskiptavinalykil og smella síðan á **Í lagi**.

4.  Í skjámyndinni **Skilapöntun - RMA-númer: %1, %2** í **Aðgerðasvæði** skal smella á **Finna sölupöntun**.

5.  Í skjámyndinni **Finna sölupöntun** skaltu velja reikningslínuna sem á að skila og smella síðan á **Í lagi**.
    
    Á flýtiflipanum **Línuupplýsingar**, á flipanum **Almennt**, sýnir reiturinn **Lotukenni skila** gildið á upprunalegu sölulínunni. Að auki sýnir reiturinn **Kostnaðarverð skila** kostnaðargildi upphaflegu sölulínunnar.

## <a name="cost-calculation-example"></a>Dæmi um kostnaðarreikning

Þegar þú notar reitinn **Lotukenni skila** á skilapöntunarlínu til að tilgreina kostnaðarverð skila er kostnaðurinn á skilapöntunarlínunni notaður. Ef þú keyrir virkni lokunar eða endurreikning birgða er kostnaðurinn stilltur á upprunalegu sölulínunni. Kostnaðurinn á skilapöntunarlínunni er sjálfkrafa stilltur til að endurspegla sama kostnað á hvert stykki.

1.  Stofna og losa vöru sem heitir Próf. Í skjámyndinni **Upplýsingar um losaðar afurðir** eru eftirfarandi upplýsingar tilgreindar:
    
    1.  Á flýtiflipanum **Stjórna kostnaði**, í reitnum **Vöruflokkur** skal velja flokkinn **Hlutar**.
    
    2.  Á flýtiflipanum **Almennt**, í reitnum **Vörulíkanaflokkur** skal velja **DEF**.
    
    3.  Á flýtiflipanum **Innkaup**, í reitnum **Verð** skal slá inn 10,00 sem kostnaðarverð vörunnar.
    
    4.  Í **Aðgerðasvæði** er smellt á **Víddarflokkar**. Í reitnum **Geymsluvíddarflokkur** skal velja **Svæði og vöruhús eingöngu**. Í reitnum **Rakningarvíddarflokkur** skal velja **Engar virkar rakningarvíddir**.

2.  Stofnaðu innkaupapöntun fyrir 10 stykkjum af prufuvörunni á 6,00 fyrir hvert stykki og bókaðu síðan reikning fyrir innkaupapöntuninni.
    
    Stofnaðu aðra innkaupapöntun fyrir 10 stykkjum af prufuvörunni á 8,00 fyrir hvert stykki og bókaðu síðan reikning fyrir innkaupapöntuninni.

3.  Bókaðu reikning fyrir sölupöntun til að selja fimm stykki af prufuvörunni.
    
    Í þessu tilviki er sölupöntunarlínan kostuð á 35,00 (5 stykki \* 7,00 meðalkostnaður á stykki).

4.  Stofnaðu skilapöntun fyrir viðskiptavin. Í skjámyndinni **Finna sölupöntun** skaltu velja reikningslínuna og smella síðan á **Í lagi**.

5.  Í skjámyndinni **Skilapöntun - RMA-númer: %1, %2** skaltu staðfesta að skilapöntun sé gerð til að skila prufuvörunni. Magn skilapöntunarinnar er stillt á -5,00.
    
    Reiturinn **Lotukenni skila** sýnir lotukenni. Þetta lotukenni er tekið frá upprunalegu sölupöntuninni á vörunni sem seld var viðskiptavini. Reiturinn **Kostnaðarverð skila** sýnir kostnaðarverð upprunalegu sölulínunnar.

6.  Skráðu móttöku á skilavörum.

7.  Bókaðu fylgiseðil fyrir skilavörum.

8.  Bókaðu reikning fyrir skilapöntuninni. Á listasíðunni **Allar sölupantanir** skaltu velja sölupöntun þar sem **Skilapöntun** er pöntunargerðin.

9.  Opnaðu skjámyndina **Birgðafærslur**. Staðfestu að skilin eru kostuð á 7,00 á stykki með því að nota gildið í reitnum **Kostnaðarverð skila** fyrir samtals 35,00 í reitnum **Kostnaðarupphæð**. Þú getur opnað skjámyndina **Birgðafærslur** í skjámyndinni **Skilapöntun - RMA-númer: %1, %2**. Í hnitanetinu **Línur** skaltu smella á **Birgðir** \> **Færslur**.

10. Í „Birgða- og vöruhúsakerfi“ skaltu nota skjámyndina **Lokun og leiðrétting** til að keyra ferlið **3. Loka**.
    
    Þessi aðgerð leiðréttir kostnaðinn á upprunalegu sölulínunni sem var verðlagður á -35,00 (5 stykki \* 7,00) í -30,00 (5 stykki \* 6,00). Þetta er vegna þess að birgðalíkanaflokkurinn notar fyrst inn, fyrst út (FIFO) og 6,00 á stykki er FIFO-kostnaðurinn frá fyrstu innkaupapöntun. Að auki leiðréttir aðgerðin kostnaðinn á sölulínu skila til að passa við kostnaðinn á stykki á upprunalegu sölulínunni. Þess vegna er kostnaður á skilalínu leiðréttur úr 35,00 í 30,00.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
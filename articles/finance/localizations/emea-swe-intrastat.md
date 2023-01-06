---
title: Intrastat í Svíþjóð
description: Þessi grein inniheldur upplýsingar um Intrastat-skýrslugerð í Svíþjóð.
author: AdamTrukawka
ms.date: 08/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: e13076a6b8f18374c012a5b56f13e752010256b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279232"
---
# <a name="swedish-intrastat"></a>Swedish Intrastat

[!include[banner](../includes/banner.md)]

Síðan **Intrastat** er notuð til að útbúa og tilkynna upplýsingar um viðskipti innan landa Evrópusambandsins. Sænska Intrastat-skattskýrslan inniheldur upplýsingar um viðskipti með vörur fyrir skýrslugerð.

Eftirfarandi reitir eru innifaldir í sænsku Intrastat-skattskýrslunni:

   - ISO-kóði samstarfslands
   - Færslukóði
   - Vörukóði
   - Viðbótareining
   - Vægi
   - Upphæð reiknings

## <a name="set-up-intrastat"></a>Setja upp Intrastat

Flyttu inn nýjustu útgáfuna af eftirfarandi skilgreiningum fyrir rafræna skýrslugerð:

   - Intrastat-líkan
   - Intrastat-skýrsla
   - Intrastat (SE)

Frekari upplýsingar er að finna í [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Setja upp færibreytur erlendra viðskipta

1. Í Microsoft Dynamics 365 Finance skal fara í **Skattur** > **Uppsetning** > **Færibreytur erlendra viðskipta**.
2. Í flipanum **Intrasta**, í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **Intrastat (SE)**.
3. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
4. Í flýtiflipanum **Stigveldi vörukóða**, í reitnum **Tegundastigveldi**, velja **Intrastat**.
5. Í reitnum **Færslukóði** skal velja færslukóðann fyrir flutning á eignum. Þú notar þennan kóða fyrir færslur sem búa til raunverulegar eða áætlaðar færslur á eignum gegn greiðslu (fjárhagslegri eða annars konar greiðslu). Þú getur líka notað það til leiðréttinga. Fyrirtæki í Svíþjóð nota eins stafs færslukóða.
6. Í reitnum **Kreditnóta** skal velja færslukóðann fyrir vöruskil.
7. Í flipanum **Eiginleikar lands/svæðis**, í reitnum **Land/svæði**, skal gefa upp öll lönd eða svæði sem fyrirtækið þitt á í viðskiptum við. Fyrir hvert land sem er hluti af ESB, í reitnum **Gerð lands/svæðis**, skal velja **ESB** þannig að landið birtist í Intrastat skýrslunni.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>Setja upp færibreytur afurðar fyrir Intrastat-skattskýrsluna

1. Opna **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar afurðir**.
2. Í hnitanetinu skal velja afurð.
3. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Varningur**, skal velja vörukóðann.
4. Í flýtiflipanum **Stjórna birgðum**, í reitnum **Nettóþyngd**, skal færa inn þyngd afurðar í kílógrömmum.
5. Farðu í **Skattur**  >  **Uppsetning**  >  **Erlend viðskipti**  >  **Intrastat-þjöppun** og veldu reitina sem á að bera saman þegar Intrastat-upplýsingar eru teknar saman. Fyrir Intrastat í Svíþjóð skal velja eftirfarandi reiti:

    - Vara
    - Færslukóði
    - Stefna
    - Land/svæði
    - Leiðrétting
    - Reikningur

## <a name="intrastat-transfer"></a>Intrastat-flutningur

Á síðunni **Intrastat** á aðgerðasvæðinu er hægt að velja **Flutningur** til að flytja sjálfkrafa upplýsingarnar um viðskipti innan samfélags úr sölupöntunum, textum með frjálsum texta, innkaupapöntunum, lánardrottnareikningum, innhreyfingarskjölum afurða lánardrottins, verkreikningum og flutningspöntunum. Aðeins skjöl sem hafa ESB-land sem land eða svæði áfangastaðar (fyrir sendingar) eða vörusendingu (fyrir komur) verða flutt.

Einnig er hægt að færa færslur handvirkt inn með því að velja **Ný** á aðgerðasvæðinu.

### <a name="generate-an-intrastat-report"></a>Mynda Intrastat-skýrslu

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
3. Í svarglugganum **Intrastat skýrsla** skal stilla eftirfarandi reiti.

    | Svæði            | lýsing                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Frá degi        | Veldu upphafsdagsetningu fyrir skýrsluna.                                                                                               |
    | Til dags.          | Veldu lokadagsetningu fyrir skýrsluna.                                                                                                 |
    | Mynda skrá    | Stilltu þennan valkost á **Já** til að búa til .txt-skrá fyrir Intrastat-skýrsluna.                                                       |
    | Skrárnafn        | Færðu inn heiti .txt-skráar.                                                                                                    |
    | Búa til skýrslu  | Stilltu þennan valkost á **Já** til að búa til .xlsx-skrá fyrir Intrastat-skýrsluna.                                                     |
    | Heiti skýrsluskráar | Færðu inn heiti .xlsx-skráar.                                                                                                   |
    | Stefna        | Veldu **Komur** til að fá skýrslu um komur innan samfélags. Veldu **Sendingar** til að fá skýrslu um sendingar innan samfélags. |

4. Veldu **Í lagi** og farðu yfir myndaða skýrslu.

## <a name="example"></a>Dæmi

Dæmið sýnir hvernig á að bóka komur og sendingar fyrir Intrastat. Það notar **DEMF** lögaðilann.

### <a name="preliminary-setup"></a>Bráðabirgða uppsetning

1. Farðu í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar** og veldu lögaðilann **DEMF**.
2. Í flýtiflipanum **Aðsetur** skal velja **Breyta** og síðan í reitnum **Land/svæði** skal velja **SWE (Svíþjóð)**.
3. Flyttu inn nýjustu útgáfu af eftirfarandi skilgreiningum rafrænnar skýrslugerðar:

    - Intrastat-líkan
    - Intrastat-skýrsla
    - Intrastat (SE)

### <a name="create-transaction-codes"></a>Stofna færslukóða

1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færslukóðar**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í reitinn **Færslu** **kóði** skal slá inn **1**.
4. Í reitinn **Heiti** skal færa inn **Venjulegar færslur**.
5. Í aðgerðarúðunni skal velja **Vista**.

### <a name="set-up-foreign-trade-parameters"></a>Setja upp færibreytur erlendra viðskipta

1. Farið í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færibreytur erlendra viðskipta**.
2. Í flipanum **Intrastat** á flýtiflipanum **Almennt** í **Færslu** **kóði** reitnum velurðu **1**.
3. Í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **Intrastat (SE)**.
4. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
5. Í flýtiflipanum **Stigveldi vörukóða**, í reitnum **Tegundastigveldi**, skal ganga úr skugga um að **Intrastat** sé valið.
6. Í flipanum **Eiginleikar lands/svæðis** skal velja **Nýtt**.
7. Í reitnum **Land/svæði viðskiptafélaga** skal velja **SWE**.
8. Í reitnum **Gerð lands/svæðis** skal velja **Innlent**.
9. Í reitnum **Land/svæði viðskiptafélaga** skal velja **DEU** og síðan í reitnum **Gerð lands/svæðis** skal velja **ESB**.

### <a name="set-up-product-information"></a>Setja upp afurðarupplýsingar

1. Opna **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar afurðir**.
2. Í hnitanetinu skal velja **D0001**.
3. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Varningur**, skal velja **100 200 30**.
4. Í flýtiflipanum **Stjórna birgðum**, í hlutanum **Þyngdarmælingar**, í reitinn **Nettóþyngd**, skal færa inn **5**.
5. Í aðgerðarúðunni skal velja **Vista**.

### <a name="change-the-site-address"></a>Breyta aðsetri svæðis

1. Farðu í **Warehouse management** > **Setja upp** > **Vöruhús** > **Svæði**.
2. Í hnitanetinu skal velja **1**.
3. Í flýtiflipanum **Aðsetur** skal velja **Breyta**.
4. Í svarglugganum **Breyta aðsetri**, í reitnum **Land/svæði**, skal velja **SWE**.
5. Veldu **Í lagi**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Stofna sölupöntun með viðskiptavin innan ESB

1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svarglugganum **Stofna sölupöntun**, í flýtiflipanum **Viðskiptavinur**, í hlutanum **Viðskiptavinur**, í reitnum **Viðskiptavinalykill**, skal velja **DE-015**.
4. Í flýtiflipanum **Almennt**, í hlutanum **Geymsluvíddir**, í reitnum **Svæði**, skal velja **1**.
5. Í reitnum **Vöruhús** skal velja **11**.
6. Veldu **Í lagi**.
7. Í flýtiflipanum **Línur**, í flýtiflipanum **Sölupöntun línur**, í reitnum **Vörunúmer**, skal velja **D0001**. Því næst, í reitinn **Magn**, skal færa inn **10**.
8. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Erlend viðskipti**, skal ganga úr skugga um að reitirnir **Færslukóði** og **Varningur** séu sjálfkrafa stilltir.
9. Í aðgerðarúðunni skal velja **Vista**.
10. Á aðgerðasvæðinu, í flipanum **Reikningur**, í hlutanum **Mynda** skal velja á **Reikningur**.
11. Í svarglugganum **Bókun reiknings**, í flýtiflipanum **Færibreytur**, í hlutanum **Færibreyta**, í reitnum **Magn**, skal velja **Allt**.
12. Veldu svo **Í lagi** til að bóka reikninginn.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Færðu færsluna í Intrastatbókina og farðu yfir niðurstöðuna

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Flutningur**.
3. Í svarglugganum **Intrastat (flutningur)**, í hlutanum **Færibreytur**, skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**.
4. Velja **Síu**.
5. Í svarglugganum **Intrastat-sía**, í flipanum **Svið**, skal velja fyrstu línuna og ganga úr skugga um reiturinn **Reitur** er stilltur á **Dagsetning**.
6. Í reitnum **Skilyrði** skal velja daginn í dag.
7. Veldu **Í lagi** til að loka svarglugganum **Intrastat-sía**.
8. Veldu **Í lagi** til að loka svarglugganum **Intrastat (flutningur)** og farðu yfir niðurstöðuna. Línan táknar sölupöntunina sem þú stofnaðir fyrr.

    ![Línur Intrastat-bókar fyrir sölupöntun](media/swe_intrastat_journal_sales_order.png)

9. Veldu færslulínuna og veldu síðan flipann **Almennt** til að skoða frekari upplýsingar.

    ![Upplýsingar um línu Intrastat-bókar fyrir sölupöntun](media/swe_intrastat_journal_sales_order_line_details.png)

10. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
11. Í svarglugganum **Intrastat skýrsla**, í flýtiflipanum **Færibreytur**, í hlutanum **Dagsetning**, skal velja mánuð sölupöntunarinnar sem var stofnuð.
12. Í hlutanum **Valkostir** **útflutnings** skal stilla valkostinn **Mynda skrá** á **Já**. Í reitinn **Skráarheiti** skal síðan færa inn nauðsynlegt heiti.
13. Stilltu valkostinn **Mynda skýrslu** á **Já**. Í reitinn **Heiti skýrsluskráar** skal síðan færa inn nauðsynlegt heiti.
14. Í reitnum **Stefna** skal velja **Sendingar**.
15. Veldu **Í lagi** og farðu yfir skýrsluna á .txt-sniði sem er búið til. Eftirfarandi tafla sýnir gildin í skýrsludæminu.

    | ISO-kóði samstarfslands | Færslukóði | Vörukóði | Viðbótareining | Vægi | Upphæð reiknings |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Farðu yfir skýrsluna á Excel-sniði sem er búið til.

    ![Intrastat-skýrsla](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

1. Farðu í **Viðskiptaskuldir** > **Innkaupapantanir** > **Allar innkaupapantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svarglugganum **Stofna innkaupapöntun**, í reitnum **Lánardrottnalykill**, skal velja **DE-001**.
4. Veldu **Í lagi**.
5. Í **Hausflipanum**, í flýtiflipanum **Erlend** **viðskipti** skal staðfesta að reiturinn **Færslukóði** sé stilltur á **1**.
6. Í flýtiflipanum **Línur**, í flýtiflipanum **Innkaupapöntunarlínur**, í reitnum **Vörunúmer**, skal velja **D0001**. Því næst, í reitinn **Magn**, skal færa inn **6**.
7. Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Aðgerðir**, skal velja **Staðfesta**.
8. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
9. Á aðgerðasvæðinu skal velja **Sjálfgefið frá**. Í reitnum **Sjálfgefið magn fyrir línur** skal velja **Pantað magn**. Veljið síðan **Í lagi**.
10. Í flýtiflipanum **Reikningshaus lánardrottins**, í hlutann **Auðkenning reiknings**, í reitinn **Númer**, skal færa inn **0001**.
11. Á aðgerðasvæðinu skal velja **Bóka** til að bóka reikninginn.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Búa til Intrastat-skattskýrslu fyrir komur

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Flutningur**.
3. Í svarglugganum **Intrastat (flutningur)** skal stilla valkostinn **Reikningur lánardrottins** á **Já**.
4. Veldu **Í lagi** til að flytja færslurnar og fara yfir Intrastat-bókina.

    ![Intrastatbók fyrir innkaupapöntun](media/swe_intrastat_journal_purchase_order.png)

5. Farðu yfir flipann **Almennt** fyrir innkaupapöntunina.

    ![Upplýsingar um línu Intrastatbókar fyrir innkaupapöntun](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
7. Í svarglugganum **Intrastat skýrsla**, í flýtiflipanum **Færibreytur**, í hlutanum **Dagsetning**, skal velja mánuð sölupöntunarinnar sem var stofnuð.
8. Í hlutanum **Valkostir** **útflutnings** skal stilla valkostinn **Mynda skrá** á **Já**. Í reitinn **Skráarheiti** skal síðan færa inn nauðsynlegt heiti.
9. Stilltu valkostinn **Mynda skýrslu** á **Já**. Í reitinn **Heiti skýrsluskráar** skal síðan færa inn nauðsynlegt heiti.
10. Í reitnum **Stefna** skal velja **Komur**.
11. Veldu **Í lagi** og farðu yfir skýrsluna sem er mynduð á .txt-sniði. Eftirfarandi tafla sýnir gildin í skýrsludæminu.

    | ISO-kóði samstarfslands | Færslukóði | Vörukóði | Viðbótareining | Vægi | Upphæð reiknings |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Farðu yfir skýrsluna á Excel-sniði sem er búið til.

    ![Intrastat-komuskýrsla](media/swe_intrastat_arrivals_report.png)

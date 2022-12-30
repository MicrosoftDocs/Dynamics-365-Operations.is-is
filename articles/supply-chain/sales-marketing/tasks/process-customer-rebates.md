---
title: Mynda og vinna úr eftirágreiddum afslætti viðskiptavina
description: Þetta ferli sýnir hvernig á að meðhöndla eftirágreiddan afslátt viðskiptavinar úr myndun kröfu til að senda þær sem uppsafnanir á viðskiptakröfur.
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage, MCRBrokerWriteOffReason, MRCHierarchyAddCust, PdsItemRebateGroup, PdsRebate, PdsRebateProgramTMATable, PdsRebateTable, PdsRebateTableListPagePreviewPane, PdsRebateTrans, PdsRebateType_CustLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a85c027571a6d77ed61cd874bb9d97221b099967
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969088"
---
# <a name="generate-and-process-customer-rebates"></a>Mynda og vinna úr eftirágreiddum afslætti viðskiptavina

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig á að meðhöndla eftirágreiddan afslátt viðskiptavinar úr myndun kröfu til að senda þær sem uppsafnanir á viðskiptakröfur. Það fer í gegnum tiltekið dæmi til að útskýra hvernig mismunandi skilyrði í línum fyrir eftirágreiddan afslátt hafa áhrif endanleg upphæðir sem verður kreditfærð á viðskiptavininn. Nauðsynlegt er að nota USMF sýnigögn fyrirtækisins og framkvæma eftirfarandi verkefni áður en byrjað er á leiðarvísi: (1) Fara á síðu færibreytur viðskiptakrafna og útvíkka á flipanum Verð og svo flipann upplýsingar um Verð og athuga að valkosturinn Virkja verðupplýsingar er stilltur á Já. (2) fara í samningur um eftirágreiddan afslátt síðunni og velja samning um eftirágreiddan afslátt viðskiptavinar: USMF 000001. Ef svæði stöðu verkflæðissamþykkis er ekki stilltur á Samþykkt, þarf að smella á Villuleit í aðgerðarúðunni til að samþykkja hana.


## <a name="review-a-customer-rebate-agreement"></a>Yfirfara samning um eftirágreiddan afslátt
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala- og markaðssetning > Eftirágreiddir afslættir > Samningar um eftirágreiddan afslátt**.
    - Næstu skref skoða skilyrði USMF 000001 samnings. Þetta gerir það auðveldara að átta sig á hvernig lánagildi viðskiptavinar eru reiknaðar seinna í ferlinu.  
    - Samningurinn er fyrir einstaka viðskiptavin, í þessu dæmi viðskiptavinar US-009.  
    - Eftirágreiddir afslættir eru gefnar viðskiptavinar þegar þeir kaupa tiltekna afurð. Í þessu tilfelli hefur afurðar T0020 vörunúmer.   
    - afköst í sölu Viðskiptavinar, sem upphæðir eftirágreidds afsláttur er metið, á að taka saman vikulega.  
    - Stillingin fyrir „Verð er tekið úr” er Brúttó, sem þýðir að söluupphæð línu á hvaða grunn kröfunni er áætluð er ekki lækkað sem nemur línuafslátt.  
    - Svæðið gerð hlés fyrir Eftirágreiddur Afsláttur sýnir aðferð fyrir útreikning á eftirágreiddum afslætti. Í þessu tilfelli er sölumarkmið sem eftirágreidda eru metnir gegn stillt á Magn.   
    - Línur samnings tilgreina gerð upphæðar eftirágreidds afsláttar, virði raunverulegt eftirágreidds afsláttar og í þröskulda. Í þessu dæmi viðskiptavinar uppfylla skilyrði fyrir eftirágreiddan afslátt uppá 20 USA á hverja einingu sem er seld, ef þeirra vikulegt innkaup þeirra á afurðarinnar fellur innan einingar 1 til 50; og eftirágreiddum afslætti uppá 40 usd á hverja einingu, ef þeir kaupa ofan 50 einingar.  
2. Lokið síðunni.

## <a name="generate-rebate-claims"></a>Mynda fyrir kröfur um eftirágreiddan afslátt
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.
2. Smellt er á **Nýtt**. Til að herma eftir hvernig á að mynda kröfur um eftirágreiddan afslátt er næsta verk stofnað sem sölupöntun, þar sem afurð og magn verða viðurkenna viðskiptavinar umrætt fyrir eftirágreiddan afslátt.    
3. Í reitnum **Viðskiptavinalykill** skal færa inn eða velja gildi.
4. Smellt er á **OK**.
5. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
6. Stillið **Magn** á „40“.
7. Undir hlutanum **Sölupöntunarlínur** smellirðu á **Sölupöntunarlína**.
8. Smelltu á **Verðupplýsingar**. Ef þú sértð þennan valkost ekki er það vegna þess að þú stilltir ekki valkostinn **Virkja upplýsingar um verð** á Já áður en þú byrjaðir þessar leiðbeiningar.     
9. Útvíkka hlutann **Eftirágreiddur afsláttur**. Flipinn **Eftirágreiddur afsláttur** telur upp alla samningur um eftirágreiddan afslátt sem á við um gildandi pöntunarlínu og sýnir áætlaða upphæð eftirágreidds afsláttar. Athugið upphæðirnar sem birt eru aðeins vísar um hvað eftirágreidds afsláttar kunna að verða síðar meir. Raunveruleg upphæðir eftirágreidds afsláttar gæti verið mismunandi, allt eftir: umfangi heildarsölu sem viðskiptavinurinn náði samkvæmt reglubundin samningi um eftirágreiddan afslátt ; hvort viðskiptavinar skilaði alla eða hluta af magni; og hvort viðkomandi sölupöntun var reikningsfærð.
10. Lokið síðunni.
11. Smella á **Bæta við línu**.
12. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
13. Stillið **Magn** á „60“.
14. Smellt er á **Vista**.
15. Í **aðgerðasvæðinu** er smellt á **Reikningur**.
16. Smelltu á **Reikningur**.
17. Útvíkkaðu hlutann **Færibreytur**.
18. Í reitnum **Magn** velurðu Allt.
19. Smellt er á **OK**.
20. Smellt er á **OK**.

## <a name="process-rebate-claims"></a>Vinna úr kröfur um eftirágreiddan afslátt
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala- og markaðssetning > Eftirágreiddir afslættir > Eftirágreiddur afsláttur**.
    - Síða eftirágreiddra afslátta þjónar sem vinnusvæði þar sem hægt er að endurskoða, samþykkja og vinna úr kröfum um eftirágreiddan afslátt. Nú muntu vinna kröfur sem voru stofnaðar þegar reikningsfært var sölupöntun fyrir viðskiptavin US-009 sem er viðfangsefni samnings um eftirágreiddan afslátt USMF-000001 .   
    - Fyrsta lína stendur fyrir kröfu um eftirágreiddan afslátt fyrir 800 USD sem er byggð á sölu 40 eininga afurðar T0020, reiknaður sem 20 USD á hverja einingu. Þetta uppfyllir skilyrði fyrir fyrsta hlé í magni í samning um eftirágreiddan afslátt.  
    - Önnur kröfu er fyrir 2,400 USD sem er byggð á sölu 60 eininga afurðar T0020 reiknaður 40 USD á hverja einingu samkvæmt seinni hlé í magni í samningnum.  
    - Báðar kröfurnar eru í stöðunni „Til útreiknings”. Þetta þýðir að þær séu tengd við samning sem rekur afköst í sölu viðskiptavinar með reglulegu millibili og að þær verða að vera reiknuð aftur á lykil fyrir sölu umfang heildarsölu innan viðkomandi tímabils.   
2. Smellt er á **Uppsafna**.
3. Í reitnum **Viðskiptavinur** skal færa inn eða velja gildi.
4. Í reitnum **Upphafsdagur** skaltu velja daginn í dag.
5. Smellt er á **OK**. Þegar aðgerðin **Uppsöfnun** hefur verið keyrð er áætluð kröfuupphæð nú leiðrétt við lykil þar sem heildarsölumagn viðskiptavinar á viðkomandi tímabili er meira en þegar fyrsti eftirágreiddur afslátturinn var myndaður. Nánar, þar sem keypt magn samtals hefur náð 100 einingar, viðskiptavinur er nú hæfur fyrir 40 USD á hverja einingu (samkvæmt á samningnum um annað hlé í magni) eða 4,000 USD samtals upphæð eftirágreidds afsláttar. Munurinn er skráð sem í "leiðrétting" nýrrar kröfu fyrir viðbótar 800 USD. Staða krafna um eftirágreiddan afslátt sem voru hafðar með í Heildaruppfærsla eru nú stillt á Reiknuð. 
6. Í listanum er merkt við allar línur.
7. Smelltu á **Samþykkja**.
8. Smelltu á **Vinnslu**.
9. Í reitnum **Viðskiptavinur** skal færa inn eða velja gildi.
10. Smellt er á **OK**. Skilaboð sýnir að eftirágreiddur afsláttur tókst að vinna og kröfur fyrir stöðu hefur verið breytt til að Merkja. Þetta þýðir að vegna birtingar á uppsöfnunarfærslubók endurgreiðslna:
    - Kröfurnar hafa nú verið fluttar í tímabundna stöðu viðskiptavinar sem frádrættir.
    - Uppsöfnunarlykill eftirágreidds afsláttar hefur verið kreditfærður til að tákna framtíðarskuldir við viðskiptavininn.
    - Kostnaðarlykill eftirágreidds afsláttar hefur verið debetfærður sem staðfesting á kostnaðinum sem stofnað var til í tengslum við sölu.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

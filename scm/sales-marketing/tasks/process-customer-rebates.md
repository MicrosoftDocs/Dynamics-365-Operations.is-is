--- 
title: "Mynda og vinna úr eftirágreiddum afslætti viðskiptavina"
description: "Þetta ferli sýnir hvernig á að meðhöndla eftirágreiddan afslátt viðskiptavinar úr myndun kröfu til að senda þær sem uppsafnanir á viðskiptakröfur."
author: omulvad
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: fb5053ac5c5f9218b95d14baf4ea78f7a40479ff
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="generate-and-process-customer-rebates"></a>Mynda og vinna úr eftirágreiddum afslætti viðskiptavina

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að meðhöndla eftirágreiddan afslátt viðskiptavinar úr myndun kröfu til að senda þær sem uppsafnanir á viðskiptakröfur. Það fer í gegnum tiltekið dæmi til að útskýra hvernig mismunandi skilyrði í línum fyrir eftirágreiddan afslátt hafa áhrif endanleg upphæðir sem verður kreditfærð á viðskiptavininn. Nauðsynlegt er að nota USMF sýnigögn fyrirtækisins og framkvæma eftirfarandi verkefni áður en byrjað er á leiðarvísi: (1) Fara á síðu færibreytur viðskiptakrafna og útvíkka á flipanum Verð og svo flipann upplýsingar um Verð og athuga að valkosturinn Virkja verðupplýsingar er stilltur á Já. (2) fara í samningur um eftirágreiddan afslátt síðunni og velja samning um eftirágreiddan afslátt viðskiptavinar: USMF 000001. Ef svæði stöðu verkflæðissamþykkis er ekki stilltur á Samþykkt, þarf að smella á Villuleit í aðgerðarúðunni til að samþykkja hana.


## <a name="review-a-customer-rebate-agreement"></a>Yfirfara samning um eftirágreiddan afslátt
1. Fara í Sölu og markaðssetningu > Eftirágreiddir afslættir > Samningar um eftirágreiddan afslátt.
    * Næstu skref skoða skilyrði USMF 000001 samnings. Þetta gerir það auðveldara að átta sig á hvernig lánagildi viðskiptavinar eru reiknaðar seinna í ferlinu.  
    * Samningurinn er fyrir einstaka viðskiptavin, í þessu dæmi viðskiptavinar US-009.  
    * Eftirágreiddir afslættir eru gefnar viðskiptavinar þegar þeir kaupa tiltekna afurð. Í þessu tilfelli hefur afurðar T0020 vörunúmer.   
    * afköst í sölu Viðskiptavinar, sem upphæðir eftirágreidds afsláttur er metið, á að taka saman vikulega.  
    * Stillingin fyrir "Verð er tekið úr" er Brúttó, sem þýðir að söluupphæð línu á hvaða grunn kröfunni er áætluð er ekki lækkað sem nemur línuafslátt.  
    * Svæðið gerð hlés fyrir Eftirágreiddur Afsláttur sýnir aðferð fyrir útreikning á eftirágreiddum afslætti. Í þessu tilfelli er sölumarkmið sem eftirágreidda eru metnir gegn stillt á Magn.   
    * Línur samnings tilgreina gerð upphæðar eftirágreidds afsláttar, virði raunverulegt eftirágreidds afsláttar og í þröskulda. Í þessu dæmi viðskiptavinar uppfylla skilyrði fyrir eftirágreiddan afslátt uppá 20 USA á hverja einingu sem er seld, ef þeirra vikulegt innkaup þeirra á afurðarinnar fellur innan einingar 1 til 50; og eftirágreiddum afslætti uppá 40 usd á hverja einingu, ef þeir kaupa ofan 50 einingar.  
2. Lokið síðunni.

## <a name="generate-rebate-claims"></a>Mynda fyrir kröfur um eftirágreiddan afslátt
1. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
2. Smellið á „Nýtt“.
    * Til að herma eftir hvernig á að mynda kröfur um eftirágreiddan afslátt er næsta verk stofnað sem sölupöntun, þar sem afurð og magn verða viðurkenna viðskiptavinar umrætt fyrir eftirágreiddan afslátt.  
3. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
4. Smellið á „Í lagi“.
5. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
6. Stillið magn á „40“.
7. Smellið á „Sölupöntunarlína“.
8. Smellt er á verðupplýsingar.
    * Ef ekki er að sjá þennan valkost, það er vegna þess að þú stilltir ekki virkja upplýsingar um verð valkostinn á Já áður en þú byrjaðir þessar leiðbeiningar.  
9. Útvíkka hlutann Eftirágreiddur afsláttur.
    * Eftirágreiddan Afslátt flipi telur upp alla samningur um eftirágreiddan afslátt sem á við um gildandi pöntunarlínu og sýnir áætlaða upphæð eftirágreidds afsláttar. Athugið upphæðirnar sem birt eru aðeins vísar um hvað eftirágreidds afsláttar kunna að verða síðar meir. Raunveruleg upphæðir eftirágreidds afsláttar gæti verið mismunandi, allt eftir: umfangi heildarsölu sem viðskiptavinurinn náði samkvæmt reglubundin samningi um eftirágreiddan afslátt ; hvort viðskiptavinar skilaði alla eða hluta af magni; og hvort viðkomandi sölupöntun var reikningsfærð.  
10. Lokið síðunni.
11. Smellið á „Bæta við línu“.
12. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
13. Stillið magn á „60“.
14. Smellið á „Vista“.
15. Smellið á „Reikningur“ á aðgerðarúðunni.
16. Smellið á „Reikningur“.
17. Víkkið út færibreytuhlutann.
18. Veljið „Allt“ á svæðinu „Magn“.
19. Smellið á „Í lagi“.
20. Smellið á „Í lagi“.

## <a name="process-rebate-claims"></a>Vinna úr kröfur um eftirágreiddan afslátt
1. Fara í Sölu og markaðssetningu > Eftirágreiddir afslættir > eftirágreiddan afslátt.
    * síða Eftirágreiddir Afslættir þjónar sem vinnusvæði þar sem hægt er að endurskoða, samþykkja og vinna kröfur um eftirágreiddan afslátt. Nú muntu vinna kröfur sem voru stofnaðar þegar reikningsfært var sölupöntun fyrir viðskiptavin U.S.-009 sem er viðfangsefni samnings um eftirágreiddan afslátt USMF 000001 .   
    * Fyrsta lína stendur fyrir kröfu um eftirágreiddan afslátt fyrir 800 USD sem er byggð á sölu 40 eininga afurðar T0020, reiknaður sem 20 USD á hverja einingu. Þetta uppfyllir skilyrði fyrir fyrsta hlé í magni í samning um eftirágreiddan afslátt.  
    * Önnur kröfu er fyrir 2,400 USD sem er byggð á sölu 60 eininga afurðar T0020 reiknaður 40 USD á hverja einingu samkvæmt seinni hlé í magni í samningnum.  
    * Bæði krafa eru í “Til útreiknings” staða. Þetta þýðir að þær séu tengd við samning sem rekur afköst í sölu viðskiptavinar með reglulegu millibili og að þær verða að vera reiknuð aftur á lykil fyrir sölu umfang heildarsölu innan viðkomandi tímabils.   
2. Smellt er á Uppsafnað.
3. Í reitnum Viðskiptavinur skal færa inn eða velja gildi.
4. Veldu daginn í dag í reitinn Upphafsdagur.
5. Smellið á „Í lagi“.
    * Þegar uppsöfnunaraðgerð hefur verið keyrð er áætluð kröfuupphæð nú leiðrétt við lykil þar sem heildarsölumagn viðskiptavinar á viðkomandi tímabili er meira en þegar fyrsti eftirágreiddur afslátturinn var myndaður. Nánar, þar sem keypt magn samtals hefur náð 100 einingar, viðskiptavinur er nú hæfur fyrir 40 USD á hverja einingu (samkvæmt á samningnum um annað hlé í magni) eða 400 USD samtals upphæð eftirágreidds afsláttar. Munurinn er skráð sem í "leiðrétting" nýrrar kröfu fyrir viðbótar 800 USD. Staða krafna um eftirágreiddan afslátt sem voru hafðar með í Heildaruppfærsla eru nú stillt á Reiknuð.   
6. Í listanum er merkt við allar línur.
7. Smellið á Samþykkja.
8. Smellið á Vinnslu.
9. Í reitnum Viðskiptavinur skal færa inn eða velja gildi.
10. Smellið á „Í lagi“.
    * Skilaboð sýnir að eftirágreiddur afsláttur tókst að vinna og kröfur fyrir stöðu hefur verið breytt til að Merkja. Þetta þýðir að vegna bókunar Færslubók fyrir uppsafnaðan eftirágreiddan afslátt : a) kröfur hafa nú verið fluttar í tímabundin stöðu viðskiptavinar sem frádráttur; b) uppsöfnunarlykill eftirágreidds Afsláttar hefur verið kreditfærð til að tákna skuld í framtíðinni við viðskiptavininn; - og c) kostnaðarlykil eftirágreidds Afsláttar hefur verið skuldfærður, hafður með í áföllnum kostnaði í tengslum við sölu.   



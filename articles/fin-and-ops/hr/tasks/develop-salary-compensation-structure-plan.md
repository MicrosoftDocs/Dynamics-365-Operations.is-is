--- 
title: "Þróa uppbyggingu launa og launafyrirkomulag"
description: "Þessi leiðarvísir fyrir verk fer í gegnum ferlið við stofnun launafyrirkomulags fastra launa og virkjun starfsmönnum að vera skráðir í launafyrirkomulag með hæfnisreglum."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 28d044cedbcc9f483a4deb7739aef0f8e3abf9ec
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="develop-salarycompensation-structure-and-plan"></a>Þróa uppbyggingu launa og launafyrirkomulag

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísir fyrir verk fer í gegnum ferlið við stofnun launafyrirkomulags fastra launa og virkjun starfsmönnum að vera skráðir í launafyrirkomulag með hæfnisreglum. Sýnigagnafyrirtækisins til að stofna verkið er USMF og verkið er ætluð fyrir Launa- og Fríðindastjórnendur.


## <a name="create-fixed-compensation-plan"></a>Stofna launafyrirkomulag fastra launa
1. Smellt er á Launastjórnun.
2. Smellt er á launafyrirkomulag fastra launa.
3. Smellið á „Nýtt“.
4. Í reitinn Áætlun skal slá inn gildi.
5. Sláið inn gildi í reitnum „Lýsing“.
6. Í reitnum Gildisdagsetning skal slá inn dagsetningu.
7. Í svæðinu, veljið hvort launafyrirkomulag Fastra launa er Brautar, Stiga eða Þrepa áætlun.
8. Gátreiturinn Ráðleggingar leyfðar virkar sem sjálfgildi fyrir allar aðgerðir sem er bætt við þessa áætlun í vinnslutilviki.  Með því að heimila ráðleggingar gerir það kleift að hnekkja reiknaðri viðmiðunarupphæð við vinnslu launa.
9. Utan marka vikmörk gerir kleift að tilgreina hvernig eigi að meðhöndla upphæðir launa sem falla utan sviðs tilgreinda launafyrirkomulagsins fyrir tiltekið stig.  Ef Vikmörk Utan marka er Ekkert, eru allar upphæðir launa sem á að nota leyfðar.  Óbundnar vikmörk varar notandann við ef launaupphæðin er minna en lágmarks lágmarksupphæð tilvísunartímapunkts fyrir það stig, eða hærri en hámarksupphæð fyrir það stig. Notandinn getur hunsað viðvörunina og haldið áfram.  Bundnar vikmörk mynda villa ef laun starfsmanns eru stillt utan lágmarks og hámarks tilvísunarpunkta fyrir það stig og leiðréttir sjálfkrafa launum starfsmanns til að falla innan sviðsins.
10. svæðið Ráðningarregla er notað þegar launavinnslutilvik er keyrt til að reikna út laun starfsmanns.  Ráðningarreglu með prósentum reiknar hækkun sem er í hlutfalli við lengd þess tíma sem starfsmaður hefur verið í starfi í ferlinu.
11. Í reitinn Gjaldmiðill skal slá inn gildi.
12. Sláðu inn eða veldu gildi í reitnum umreikningur launataxta.
13. Útvíkka hlutann Nýtingarfylki sviðs.
    * Einnig er hægt að bæta við notkunarmörkum sviða til að koma starfsmenn fyrr til þeirra miðpunktur og hægja á því að þeir nái hámarki síns sviðs.  
14. Á þessum tímapunkti, verður að vista launafyrirkomulag Fastra launa að virkja hnappinn Setja upp laun og halda áfram að skilgreina launaskipulag þitt fyrir áætlunina.  Smellið á „Vista“.
15. Smellt er á Setja upp laun.
    * Það eru þrjár leiðir til að stofna launaskipulag. 1: stofna algerlega nýja skipulag með því að velja safn tilvísunarpunkta og bæta stig við stigum til að stofna þitt eigið skipulag. 2: afrita launaskipulag úr fyrirliggjandi áætlun sem upphafspunkt og breyta hann fyrir nýja áætlun. 3: Velja skal núverandi launanet. Ef launanetinu er þegar í notkun fyrir aðra áætlun, munu breytingar á töflunni einnig endurspeglast í hinni áætlun.  
16. Velja Stofna nýtt út frá fyrirliggjandi launafylki valkostinn.
17. Í reitinn afrita frá hnitaneti skal slá inn eða velja gildi.
    * Einnig er hægt að breyta heiti nýs  launanets sem verður stofnað sem afrit af valda netinu.  
18. Smellið á „Í lagi“.
19. Smellt er á Fjöldabreyting.
    * Fjöldabreyting gerir kleift að vinna með upphæðir launafylkis með því að nota prósenta eða flata upphæð fyrir aukningu á eitt eða fleiri stig og/eða tilvísunarpunkta.  
20. Í reitinn Leiðréttingarupphæð skal slá inn númer.
21. Merkið eða afmerkið allar línur í listanum.
22. Smellt er á Nota á hnitanet.
23. Lokið síðunni.
    * Þegar launaskipulag hefur verið stofnuð eða valin, er hægt að velja hvaða tilvísununarpunkta á að nota sem stýripunkt fyrir launafyrirkomulag Fastra launa.  Stýripunkturinn er notuð til að reikna út samanburðarhlutfall starfsmanns.  
24. Sláið inn eða veldu gildi í reitnum stýripunktur.
25. Lokið síðunni.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Stofna hæfnisreglur fyrir nýtt launafyrirkomulag fastra launa
    * Nýja launafyrirkomulag Fastra launa er ekki hægt að úthlutað til starfsmanns fyrr en hæfnisreglur hafa verið skilgreindar fyrir áætlunina.  
1. Smellið á hæfnisreglur
2. Smellið á „Nýtt“.
3. Í reitinn Hæfni skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Gildisdagsetning skal slá inn dagsetningu.
    * Hæfnisreglur eru notaðar fyrir bæði launafyrirkomulög með fastri og breytilegri uppbót.  Í svæðinu gerð, veljið hvaða gerð áætlunar sem þetta safn hæfnisregla er fyrir.  
6. Í reitinn áætlun skal slá inn eða veldu gildi.
    * Veljið skilyrði sem starfsmanns verður að uppfylla til að vera hæfur fyrir launafyrirkomulagið. Skilyrði geta verið Deild, verkalýðsfélag, Staðsetningar (launasvæði), starfshlutverk, vinnslugerð, eða launastig. Starfsmaðurinn verður að uppfylla öll tilgreind skilyrði til að teljast hæfur fyrir launafyrirkomulagið. Ef engin skilyrði eru tilgreind eru allir starfsmenn sem koma til greina fyrir launafyrirkomulagið. Ef starfsmaður uppfyllir skilyrði sem tilgreind er í hæfnisreglu eða hæfnisregla hefur ekki verið tilgreind fyrir launafyrirkomulag, mun launafyrirkomulagið ekki birtast í leitarniðurstöðum þegar stofna á færsla Fastra launa fyrir starfsmann.  
7. Lokið síðunni.
8. Lokið síðunni.



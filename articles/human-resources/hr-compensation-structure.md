---
title: Þróa launaskipulag
description: Þessi grein fer í gegnum ferlið við stofnun fyrirkomulags fastra launa og skráningu starfsmanna í launafyrirkomulagið með hæfnisreglum.
author: andreabichsel
manager: tfehr
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a5e7ef2021e41c13b82523f2dc6a1b09bd1ba9f
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115897"
---
# <a name="develop-a-compensation-structure"></a>Þróa launaskipulag

Þessi grein fer í gegnum ferlið við stofnun fyrirkomulags fastra launa og skráningu starfsmanna í launafyrirkomulagið með hæfnisreglum. Þessi grein notar USMF kynningargögn og gildir um launa- og fríðindastjórnendur.

## <a name="create-a-fixed-compensation-plan"></a>Setja upp fasta launaáætlun

1. Veldu **Launastjórnun**.

2. Veldu **Launafyrirkomulag fastra launa**.

3. Veljið **Nýtt**.

4. Í reitinn **Fyrirkomulag** skal slá inn gildi.

5. Sláið inn gildi í reitnum **Lýsing**.

6. Í reitnum **Gildisdagsetning** skal slá inn dagsetningu.

7. Í reitnum **Gerð** velurðu hvort launafyrirkomulag Fastra launa er **Brautar**, **Stiga** eða **Þrepa** áætlun.

8. Gátreiturinn **Ráðleggingar leyfðar** virkar sem sjálfgildi fyrir allar aðgerðir sem er bætt við þessa áætlun í vinnslutilviki. Með því að heimila ráðleggingar gerir það kleift að hnekkja reiknaðri viðmiðunarupphæð við vinnslu launa.

9. Reiturinn **Vikmörk utan marka** gerir kleift að tilgreina hvernig eigi að meðhöndla upphæðir launa sem falla utan sviðs tilgreinda launafyrirkomulagsins fyrir tiltekið stig. Ef reiturinn **Vikmörk utan marka** er stilltur á **Ekkert** gerir þér kleift að nota hvaða launaupphæð sem er. **Óbundin vikmörk** vara notendur við ef launaupphæðin er lægri en lágmarkið eða hærri en hámark tilvísunartímapunkts fyrir það stig. Notendur geta hunsað viðvörunina og haldið áfram. **Bundin vikmörk** mynda villu ef laun starfsmanns eru stillt utan lágmarks og hámarks tilvísunarpunkta fyrir það stig og leiðréttir sjálfkrafa launum starfsmanns til að falla innan sviðsins.

10. Reiturinn **Ráðningarregla** reiknar laun starfsmanns í vinnslutilviki. **Ráðningarreglan** **Prósenta** reiknar hækkun sem er í hlutfalli við lengd þess tíma sem starfsmaður hefur verið í starfi í ferlinu.

11. Í reitinn **Gjaldmiðill** skal slá inn gildi.

12. Í reitnum **Umreikningur launataxta** slærðu inn eða velur gildi.

13. Útvíkkaðu hlutann **Fylki nýtingar launabils**. Einnig er hægt að bæta við notkunarmörkum sviða til að koma starfsmenn fyrr til þeirra miðpunktur og hægja á því að þeir nái hámarki síns sviðs.

14. Veljið **Vista**. Þetta virkjar hnappinn **Setja upp laun** og heldur áfram að skilgreina launaskipan fyrir áætlunina.

15. Veldu **Setja upp laun**. Þú getur búið til launafyrirkomulag með því að nota eina af þessum þremur aðferðum:

    - Stofna alveg nýtt fyrirkomulag með því að velja safn tilvísunarpunkta og bæta stig við stigum til að stofna þitt eigið skipulag.
    - Afrita launafyrirkomulag úr fyrirliggjandi áætlun sem upphafspunkt og breyta því fyrir nýja áætlun.
    - Velja fyrirliggjandi launanet. Ef önnur áætlun er þegar að nota launanetið endurspeglar hin áætlunin einnig allar breytingar sem eru gerðar á netinu.

16. Veldu **Stofna nýtt út frá fyrirliggjandi launafylki**.

17. Í reitinn **Afrita frá hnitaneti** skal slá inn eða velja gildi. Einnig er hægt að breyta heiti nýs launanets sem þú stofnar með því að afrita valið net.

18. Veljið **Í lagi**.

19. Veldu **Fjöldabreyting**. **Fjöldabreyting** gerir kleift að vinna með upphæðir launafylkis með því að nota prósenta eða flata upphæð fyrir aukningu á eitt eða fleiri stig eða tilvísunarpunkta.

20. Í reitinn **Leiðréttingarupphæð** skal slá inn númer.

21. Merkið eða afmerkið allar línur í listanum.

22. Smellt er á **Nota á hnitanet**.

23. Lokið síðunni. Eftir að launafyrirkomulag hefur verið stofnað eða valið, er hægt að velja hvaða tilvísunarpunkta á að nota sem stýripunkt fyrir fast launafyrirkomulag. Stýripunkturinn er notuð til að reikna út uppbótarhlutfall starfsmanns.

24. Sláið inn eða veldu gildi í reitnum **Stýripunktur**.

25. Lokið síðunni.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Stofna hæfnisreglur fyrir fast launafyrirkomulag

Ekki er hægt að úthluta föstu launafyrirkomulagi til starfsmanns fyrr en hæfnisreglur eru skilgreindar fyrir áætlunina.  

1. Veldu **Hæfnisreglur**.

2. Veljið **Nýtt**.

3. Í reitnum **Hæfnisreglur** slærðu inn gildi.

4. Sláið inn gildi í reitnum **Lýsing**.

5. Í reitnum **Gildisdagsetning** skal slá inn dagsetningu. Bæði föst og breytileg launafyrirkomulög nota hæfnisreglur. Í reitnum **Gerð** velurðu gerð áætlunar.

6. Í reitinn **Áætlun** slærðu inn eða velur gildi. Veljið skilyrði sem starfsmanns verður að uppfylla til að vera hæfur fyrir launafyrirkomulagið. Viðmið geta verið:

    - **Deild**
    - **Verkalýðsfélag**
    - **Staðsetning** (**Launasvæði**)
    - **Vinnsla**
    - **Aðgerð**
    - **Vinnslugerð**
    - **Launastig**
    
    Starfsmaðurinn verður að uppfylla öll tilgreind skilyrði til að teljast hæfur fyrir launafyrirkomulagið. Ef þú skilgreinir engin skilyrði koma allir starfsmenn til greina fyrir launafyrirkomulagið. Ef starfsmaður uppfyllir skilyrði sem tilgreind er í hæfnisreglu eða hæfnisregla hefur ekki verið tilgreind fyrir launafyrirkomulag, mun launafyrirkomulagið ekki birtast í leitarniðurstöðum við stofnun fastrar launaskráar fyrir starfsmann.

7. Lokið síðunni.

8. Lokið síðunni.


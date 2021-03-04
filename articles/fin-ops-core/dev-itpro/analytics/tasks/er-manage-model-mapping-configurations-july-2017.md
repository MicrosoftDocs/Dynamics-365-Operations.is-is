---
title: Stjórna vörum líkana rafrænar skýrslugerðar í mismunandi skilgreiningar rafrænnar skýrslugerðar
description: Eftirfarandi skref útskýra hvernig notanda sem úthlutað hefur verið hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stjórnað líkansvörpun fyrir Rafræna skýrslugerð (ER) úr öðrum grunnstillingum Rafræn skýrslugerð.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e59e9f2dd5a0fa6d5955e3d93d25759a478ede7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684428"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a>Stjórna vörum líkana rafrænar skýrslugerðar í mismunandi skilgreiningar rafrænnar skýrslugerðar

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notanda sem úthlutað hefur verið hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stjórnað líkansvörpun fyrir Rafræna skýrslugerð (ER) úr öðrum grunnstillingum Rafræn skýrslugerð. Í þessum verkefnaleiðbeiningum skal stofna nauðsynlega grunnstillingu Rafræn skýrslugerð fyrir sýnifyrirtæki, Litware, Inc. Til að ljúka þessum verkefnaleiðbeiningum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningum „Stofna grunnstillingarveitu í Rafræna skýrslugerð” og merkja hana sem virka. 

Þar sem grunnstillingar Rafræn skýrslugerð er deilt á meðal fyrirtækja, geturðu lokið við þessar verkefnaleiðbeiningar með því að nota fyrirtækjagagnasafn að eigin vali. Virkni fyrir þessar verkefnaleiðbeiningar eru tiltækar ef þú hefur hlaðið inn einni af eftirfarandi bráðabótum: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 fyrir Dynamics AX 7.0 útgáfuna eða https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 fyrir Dynamics 365 for Operations útfgáfuna.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk. Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Stofna skilgreiningarveitu og merkja hana sem virka“.   

## <a name="add-a-new-er-model-configuration"></a>Bæta við nýrri grunnstillingu líkans í Rafræn skýrslugerð
1. Smelltu á Grunnstillingar skýrslugerðar
    * Bæta við nýrri grunnstillingu líkans. Heitið verður að vera einkvæmt í tré grunnstillingarinnar.  
2. Smellt er á stofna skilgreiningu til að opna fellilistanum.
3. Í svæðið Heiti, Færðu inn „Sýnigagnalíkan“.
    * Sýnigagnalíkan  
4. Smelltu á Stofna skilgreiningu.
5. Smellið á Hönnuður.
6. Smellt er á Nýtt til að opna felligluggann.
7. Í reitnum Heiti skal færa inn ‚rót'.
    * Rót  
8. Smelltu á Bæta við.
9. Smellt er á Nýtt til að opna felligluggann.
10. Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.
    * Fyrirt.  
11. Smelltu á Bæta við.
12. Í reitinn Lýsing skal færa inn textann, Lýsing á lögaðila eða fyrirtæki sem notandi er skráður inn á við keyrslu. 
    * Lýsing á lögaðila eða fyrirtæki sem notandi er skráður inn á við keyrslu.  
13. Smelltu á Rótartilvísun
14. Smellið á „Í lagi“.
15. Smellið á „Vista“.
16. Lokið síðunni.
17. Smellið á „Breyta stöðu“.
18. Smelltu á Ljúka.
19. Smellt er á Í lagi.

## <a name="add-a-new-er-model-mapping-configuration"></a>Bæta við nýrri grunnstillingu vörpunar í rafrænni skýrslugerð
1. Smellt er á stofna skilgreiningu til að opna fellilistanum.
2. Í svæði Nýtt skal slá inn „Vörpun líkans byggð á gagnalíkani Sýnigagnalíkani“.
3. Í svæðið Heiti, færðu inn „Sýnivörpun“.
    * Sýnivörpun  
4. Smelltu á Stofna skilgreiningu.
5. Stækka hlutann Skilyrði
    * Skilyrðaflokki Framkvæmdir hefur verið bætt sjálfkrafa við. Flokkurinn inniheldur skilyrðahlutana sem taka til yfireiningar grunnstillingar gagnalíkansins og er merkt sem Framkvæmd. Þetta þýðir að þetta sýnidæmi um grunnstillingar vörpun líkansvörpunar er talið samsvara því að setja gagnalíkanið í framkvæmd, Sýnigagnalíkan. Þar af leiðandi mun þessi hluti neyða Rafræn skýrslugerð til að hlaða niður grunnstillingum líkansvörpunarinnar, Sýnivörpun frá geymslu Rafræn skýrslugerð þegar grunnstillingar líkans, Sýnigagnalíkan, er hlaðið niður.   
6. Smellið á Hönnuður.
    * Grunnstillingar líkansvörpunar sem þegar hafa verið stofnaðar, innihalda nýja og auða vörpun með sama heiti og grunnstillingin sem þegar hefur verið stofnuð. Þegar valin yfireining grunnstillingar líkans inniheldur líkansvarpanir, munu þær verða afritaðar í nýjar grunnstillingar líkansvörpunar.   
7. Smellið á Hönnuður.
8. Í trénu skal velja „Dynamics 365 for Operations\Table“.
9. Smella á bæta Við rót.
10. Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.
    * Fyrirt.  
11. Í reitinn Tafla skal færa inn ‚CompanyInfo‘.
    * CompanyInfo  
12. Smellið á „Í lagi“.
13. Útvíkka, í trénu „Fyrirtæki“.
14. Í trénu skal víkka út „Fyrirtæki\finna()“.
15. Í trénu skal velja „Fyrirtæki\finna()\Nafn“.
16. Smelltu á Binda.
17. Smellið á „Vista“.
18. Lokið síðunni.
19. Lokið síðunni.
20. Í Aðgerðarrúðunni er smellt á skilgreiningar.
21. Smelltu á Færibreytur notanda
22. Veljið Já í svæðinu Stillingar keyrslu.
23. Smellið á „Í lagi“.
24. Smellið á „Breyta“.
25. Veljið Já í svæðinu drög keyrslu.

## <a name="add-a-new-er-format-configuration"></a>Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð
1. Veljið „Sýnigagnalíkan“, í trénu.
2. Smellt er á stofna skilgreiningu til að opna fellilistanum.
3. Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani Sýnigagnalíkan“.
4. Í svæðið Heiti, færðu inn „Sýnisnið“.
    * Sýnisnið  
5. Smelltu á Stofna skilgreiningu.
6. Smellið á Hönnuður.
7. Smelltu á Bæta við rót til að opna felligluggann.
8. Í trénu skal velja ‚Texti/Strengur'.
9. Smellið á „Í lagi“.
10. Smelltu á flipann Vörpun.
11. Í trénu skal víkka út 'model'.
12. Í trénu skal velja „líkan\Fyrirtæki“.
13. Smelltu á Binda.
14. Smellið á „Vista“.
15. Lokið síðunni.
    * Keyrið drög að útgáfu sniðsins sem þegar hefur verið stofnað til prufu.  
16. Smellið á „Keyra“.
    * Á Útgáfur flýtiflipa, smellið á Keyra.  
17. Smellið á „Í lagi“.
    * Yfirfara úttakið sem inniheldur heiti fyrirtækisins sem notandinn, sem er að keyra þessa grunnstillingu sniðs, er skráður inn á. Áður stofnuð grunnstilling líkansvörpunar er notað af þessari grunnstillingu sniðs vegna þess að það er aðeins ein grunnstilling tiltæk sem inniheldur þær líkansvarpanir sem krafist er.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Bæta við annarri grunnstillingu vörpunar í rafrænni skýrslugerð
1. Veljið „Sýnigagnalíkan“, í trénu.
2. Smellt er á stofna skilgreiningu til að opna fellilistanum.
3. Í svæði Nýtt skal slá inn „Vörpun líkans byggð á gagnalíkani Sýnigagnalíkani“.
4. Í svæðið Heiti, færðu inn „Sýnivörpun (valkostur)“.
    * Sýnivörpun (valkostur)  
5. Smelltu á Stofna skilgreiningu.
6. Smellið á Hönnuður.
7. Smellið á Hönnuður.
8. Í trénu skal velja „Dynamics 365 for Operations\Table“.
9. Smella á bæta Við rót.
10. Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.
    * Fyrirt.  
11. Í reitinn Tafla skal færa inn ‚CompanyInfo‘.
    * CompanyInfo  
12. Smellið á „Í lagi“.
13. Smellið á „Breyta“.
14. Veljið 'String\CONCATENATE', í trénu.
15. Smelltu á Bæta við Aðgerð.
16. Útvíkka, í trénu „Fyrirtæki“.
17. Í trénu skal víkka út „Fyrirtæki\finna()“.
18. Í trénu skal velja „Fyrirtæki\finna()\Nafn“.
19. Smellt er á Bæta við gagnagjafa.
20. Í reitinn Formúla skal færa inn gildi.
    * CONCATENATE(Company.'find()'.Name, ";",  
21. Í trénu skal velja „Fyrirtæki\finna()\Fyrirtæki(DataArea)“.
22. Smellt er á Bæta við gagnagjafa.
23. Í reitinn Formúla skal færa inn gildi.
    * CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)  
24. Smellið á „Vista“.
25. Lokið síðunni.
26. Smellið á „Vista“.
27. Lokið síðunni.
28. Lokið síðunni.
29. Veljið Já í svæðinu drög keyrslu.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Nota fyrirliggjandi grunnstillingu vörpunar í rafrænni skýrslugerð
1. Veljið „Sýnigagnalíkan/Sýnisnið“, í trénu.
2. Smella á Keyra.
    * Valin útgáfudrög að grunnstillingum sniðs Rafræn skýrslugerð er ekki hægt að framkvæma vegna þess að það eru fleiri en ein grunnstilling líkansvörpunar tiltæk fyrir hið óskilgreinda gagnalíkan sem hefur verið valið sem gagnaveita fyrir snið Rafræn skýrslugerð sem verið er að keyra.   
    * Næst muntu skilgreina aðra grunnstillingu fyrir líkansvörpun, sem þá sem líkansvarpanir verða notaðar sem gagnaveitur fyrir, fyrir keyrslu sniðs rafrænar skýrslugerð.   
3. Veljið „Sýnigagnalíkan/Sýnivörpun (valkostur)“, í trénu.
4. Veljið Já í reitnum „Sjálfgefið fyrir líkanavörpun“.
5. Veljið „Sýnigagnalíkan/Sýnisnið“, í trénu.
6. Smella á Keyra.
7. Smellt er á Í lagi.
    * Sjálfgefin grunnstilling líkansvörpunar er notuð af þessari grunnstillingu sniðs til að búa til rafræn skjöl (úttakið sem þegar hefur verið stofnað inniheldur fyrirtækjakóðann).  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
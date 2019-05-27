---
title: Skilgreina vinnuflokka lean-framleiðslu
description: Vinnuflokkur er tiltekna tegund fyrir tilfangaflokka sem hægt er að nota í lean-framleiðsla verkþætti.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, InventLocationIdLookup, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f31fbd2ed8e20b92527af88fc3c955d3c66a364
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566542"
---
# <a name="define-lean-manufacturing-work-cells"></a>Skilgreina vinnuflokka lean-framleiðslu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Vinnuflokkur er tiltekna tegund fyrir tilfangaflokka sem hægt er að nota í lean-framleiðsla verkþætti. Vinnuflokkana hafa ílag og staðsetningar úttaki og skilgreiningu afkastagetu samkvæmt framleiðsluflæðislíkan. Frekari upplýsingar um grunnhugtök lean-framleiðsla vinnuflokka og útreikninga afkasta má sjá í hvítblöð um Lean-framleiðsla. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF


## <a name="create-a-work-cell"></a>Stofna vinnuflokk 
1. Fara á fyrirtækisstjórnun > Tilföng >Tilfangaflokka.
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðið tilfangaflokkur.
    * kenni vinnuflokks er yfirleitt kerfisbundin kóða og verður að vera einkvæmur fyrir lögaðilann.  
4. Sláið inn gildi í reitnum „Lýsing“.
    * Lýsing inniheldur heiti eða titil vinnuflokks.  
5. Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.
    * Vinnuflokkur er staðsett á einu tiltekið svæði. Bæði ílag og úttaks vöruhús og staðsetning verður að vera staðsett á þessu svæði.  
6. Í listanum skal smella á tengilinn í valinni línu.
7. Í reitnum framleiðslueining skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal smella á tengilinn í valinni línu.
    * Veljið framleiðslueiningu sem þessi vinnuflokkur tilheyrir.  
9. Veljið gátreitinn vinnuflokkur.
    * Til að nota á tilfangaflokk sem lean-vinnuflokkur , verður að velja gátreit vinnuflokks.  Athugið að ekki er hægt að breyta þessum eiginleika eftir tilfangaflokkur er stofnuð.  
10. Í reitnum inntaksvöruhús skal smella á fellilistahnappinn til að opna leitina.
11. Í listanum skal smella á tengilinn í valinni línu.
    * Til að stjórna efni og bókhaldi, er efni sem sett er í vinnslusal er yfirleitt úthlutað tiltekið sýndarvöruhús. Hins vegar ef óskað er að fylla á staðsetningar með vöruhúsavinnu þær verður að vera hluti af hráefnisvöruhúsinu sem veitir móttöku.  
12. Í reitnum inntaksstaðsetning skal smella á fellilistahnappinn til að opna leitina.
13. Í listanum skal smella á tengilinn í valinni línu.
    * Athugið að fyrir ferlisverkþátt, er hægt að skrifa yfir ílagsstaðsetningin á almennan hátt eða fyrir tiltekinni afurð eða afurðarafbrigði með því að skilgreina tiltektarverkþáttum sem er matað í ferlisverkþátt. Staðsetningar inntaks fyrir vinnuflokkur má ekki vera númeraplötustýrð.  
14. Í reitnum úttaksvöruhús skal smella á fellilistahnappinn til að opna leitina.
15. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Í mörgum verkþætti framleiðsluflæðis eða framleiðslulínur er oft inntaksvöruhús næsta vinnuflokkur eða sölu- eða flutningsvöruhús þangað sem afurð er yfirleitt flutt eftir framleiðsluferlinu. Hafið í huga þegar mótaðar eru lean-framleiðsla er flutningurinn er yfirleitt úrgangur, sem og skýrslugerð flutnings.  
16. Í listanum skal smella á tengilinn í valinni línu.
17. Í reitnum úttaks staðsetning skal smella á fellilistahnappinn til að opna leitina.
    * Í framleiðsluflæði með mörgum vinnsluferlum er þetta oft ílagsstaðsetningin næsta vinnuflokks.  
18. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
19. Í listanum skal smella á tengilinn í valinni línu.
20. Útvíkka eða draga saman hlutann aðgerð.
    * Gefa verður upp tegund Keyrslutíma til að virkja kostnaðarútreikning og vinnslu lean kanban-vinnslur.  
21. Í reitnum flokkur keyrslutíma skal smella á fellilistahnappinn til að opna leitina.
22. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Kostnaðartegund keyrslutíma er notað í útreikningi staðlaðs kostnaðar og bakfærslukostnaðaraðferð  
23. Í listanum skal smella á tengilinn í valinni línu.
24. Útvíkka eða draga saman hlutann dagatal.
25. Smelltu á Bæta við.
26. Í reitnum dagatal skal smella á fellilistahnappinn til að opna leitina.
27. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Yfirleitt vinnuflokkana á tiltekið staðsetning nota sömu vinnutímadagatal. Ef vinnuflokkana getur haft einstaka vinnutíma, gæti þurft að stofna tiltekna vinnutímadagatal fyrir vinnuflokkur. Athugaðu að dagatalið á að hafa staðlaðan vinnutíma skilgreindar þegar notað fyrir lean-vinnuflokkur þar sem skilgreining afkastagetu er yfirleitt tengt dagvinnutíma vinnudags.  
28. Í listanum skal smella á tengilinn í valinni línu.
29. Útvíkka eða draga saman hluta afkastageta vinnuflokks.
30. Smelltu á Bæta við.
31. Í reitnum líkan framleiðsluflæðis skal smella á fellilistahnappinn til að opna leitina.
32. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Þetta ferli krefst framleiðslu afkastagerð fyrir líkan framleiðsluflæðis, til að sýna skilgreiningu afkastageta.  
33. Í listanum skal smella á tengilinn í valinni línu.
34. Í svæðinu tímabil Afkastageta skal velja valkost.
    * Valkostirnir eru: Staðlaður vinnudagur - afkastageta er sýnd með lengd staðlaður vinnudagur í vinnutímadagatal vinnuflokkur. Fyrir hvern dag er raunverulegum vinnutíma ákvarðast af dagatal og virkar tiltæk afkastageta er reiknuð á grundvelli þess.   Vika - Leyfir vikulegt afkastagetu. Það er engin leiðrétting er gerð með raunverulegum vinnutíma.   Mánuður - Leyfir mánaðarleg afkastagetu. Það er engin leiðrétting með raunverulegum afköstum.   Venjulega er staðlaður vinnudagur er notað fyrir daglegar tímabil og vikulegt afkastageta er notuð fyrir vikuleg tímabil afkastagetu.  
35. Færið inn tölu í svæðið Meðaltal gegnumstreymi magn.
    * Athugið að lean-aðgerð aldrei sett er upp fyrir hámarksgetu í besta mögulega umhverfinu. Í staðinn afkastagetu ætti alltaf að skilgreina fyrir aðgerðir í dæmigerðum aðstæðum í gangi.  
36. Í reitnum Eining skal smella á fellilistahnappinn til að opna leitina.
37. Í listanum skal smella á tengilinn í valinni línu.
38. Leysa breytir Einingu.

## <a name="add-a-financial-dimension"></a>Bæta við fjárhagsvídd
1. Útvíkka eða draga saman hluta fjárhagsvíddir.
    * Athugið að fjárhagsvíddirnar sem eru skilgreindar í framleiðsluflæði hnekkja fjárhagsvídd tiltekið vinnuflokks.    Fjárhagsvíddirnar sem hægt er að velja fara eftir skilgreiningu fjárhagsvíddir kerfisins þíns. Eftirfarandi skref samsvara Sýnigögn gagnasafn í fyrirtæki USMF. Þegar notuð eru öðrum gögnum, þrep á hugsanlega ekki við.  
2. Í reitnum CostCenter skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Víddir sem þarf að vera valinn á lean-vinnuflokkur er háð útfærslu fjárhagsvíddir í áætlunarlíkönum fyrir tiltekna lögaðila.  
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í reitnum ItemGroup skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.

## <a name="save"></a>Vista
1. Smellið á „Vista“.


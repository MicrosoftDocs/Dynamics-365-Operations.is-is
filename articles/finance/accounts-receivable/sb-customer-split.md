---
title: Skipting viðskiptavinar á greiðsluáætlunum
description: Þessi grein lýsir því hvernig á að skipta viðskiptavini þegar áskriftargreiðsla er notuð.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746332"
---
# <a name="customer-split-on-billing-schedules"></a>Skipting viðskiptavinar á greiðsluáætlunum

Á greiðsluáætlun er *reikningslykill* viðskiptavinurinn sem fær sölupöntunarreikninginn svo hann geti greitt reikninginn. Í sumum tilvikum geta fleiri en einn viðskiptavinur greitt reikning. Virknin **Skipting viðskiptavinar** gerir þér kleift að bæta við fleiri viðskiptavinum sem hægt er að skuldfæra fyrir sömu greiðsluáætlun. Til að virkja þessa virkni skaltu fara í **Áskriftargreiðslur \> Endurteknar samningsgreiðslur \> Uppsetning \> Færibreytur fyrir endurteknar samningsgreiðslur** og stilla valkostinn **Skipting viðskiptavinar** á **Já**.

## <a name="customer-split-on-the-billing-schedule-header"></a>Skipting viðskiptavinar á haus greiðsluáætlunar

Eftir að greiðsluáætlun hefur verið útbúin er hægt að bæta fleiri viðskiptavinum við haus hennar.

Til að bæta við viðskiptavini skal fylgja þessum skrefum.

1. Á flipanum **Greiðsluáætlun** veljið **Skipting viðskiptavinar**. Reitirnir **Reikningur viðskiptavinar** og **Heiti reiknings viðskiptavinar** efst tilgreina viðskiptavininn sem er tengdur sem **Viðskiptavinur greiðsluáætlunar**.

    > [!NOTE]
    > Viðskiptavinareikningurinn sem þú bætir við má ekki vera sá sami og reikningurinn.

2. Á flipanum **Skiptar línur viðskiptavinar** velurðu **Bæta við línu**.
3. Veljið viðskiptavin og færið síðan inn prósentuhlutfall hvers reiknings fyrir þann viðskiptavin.
4. Sjálfgefið er að upphafs- og lokadagsetningar greiðsluáætlunarinnar séu notaðar sem upphafs- og lokadagsetningar. Sláðu inn aðra upphafs- og lokadagsetningu ef nýi viðskiptavinurinn mun greiða tilgreinda prósentu fyrir aðeins hluta af greiðsluáætluninni. Ef greiðsluáætlunin er til dæmis með upphafsdagsetninguna 1. janúar og lokadagsetninguna 31. desember og nýi viðskiptavinurinn er rukkaður um 40 prósent fyrstu níu mánuðina skal tilgreina 1. janúar sem upphafsdagsetninguna og 30. september sem lokadagsetninguna og færa inn **40,00** sem prósentuhlutfallið.

Hægt er að bæta fleiri en einum viðskiptavini við skiptilínur viðskiptavina. Í því tilviki má heildarhlutfallið sem slegið er inn ekki fara yfir 100 prósent. Sláðu inn tilvísun viðskiptavinar og staðfestingu viðskiptavinar sem upplýsingasvæði sem verða sýnd í sölupöntunarlínunni meðan á ferlinu **Búa til reikning** stendur.

Upplýsingar um línuna sýna samskiptaupplýsingar, afhendingaraðsetur, reikningsaðsetur og greiðsluupplýsingar þeirra viðskiptavina sem bætt hefur verið við. Þessar upplýsingar birtast einnig á sölupöntuninni fyrir viðskiptavinina.

Ef óútfylltar línur eru á greiðsluáætlun þegar upplýsingum um skiptingu viðskiptavina er bætt við haus greiðsluáætlunarinnar birtast eftirfarandi skilaboð varðandi hvort rúlla eigin breytingum niður: „Á að útfæra breytingar frá haus til lína? Breytingar uppfæra aðeins greiðsluáætlunarlínur sem ekki eru skuldfærðar.“ Veljið **Já** til að uppfæra upplýsingar um skiptingu viðskiptavina á greiðsluáætlunarlínunni. Breytingar verða ekki uppfærðar ef greiðsluáætlunarlínan hefur þegar verið skuldfærð.

Ef greiðsluáætlun er búin til með því að nota valkostinn **Afrita áætlun** verða sjálfgefnar upplýsingar færðar inn á skiptar haustlínur viðskiptavinar. Það má ekki vera það sama og viðskiptavinalykill.

Þegar ferlinu **Búa til reikning** er lokið eru margar sölupantanir stofnaðar. (Fjölmargir sölureikningar verða einnig til ef notast er við sjálfvirka bókun.) Hægt er að skoða þessar sölupantanir og sölureikninga á flipanum **Reikningur** á flýtiflipanum **Upplýsingar um línu** á síðunni **Skoða greiðsluupplýsingar**. **Margar** birtist á reikningsupplýsingalínunni til að gefa til kynna að margar sölupantanir og sölureikningar hafi verið stofnaðir.

## <a name="customer-split-on-billing-schedule-lines"></a>Skipting viðskiptavinar á greiðsluáætlunarlínum

Hægt er að bæta skiptingu viðskiptavina við einstakar greiðsluáætlunarlínur ef aðeins á að skipta tilteknum línum í greiðsluáætlun. Veljið gátreitinn **Skipting viðskiptavinar** á línunni og veljið síðan **Skipting viðskiptavinar** í valmyndinni fyrir greiðsluáætlunarlínuna til að uppfæra eða slá inn upplýsingar um skiptingu viðskiptavinar.

Endurskoðunarupplýsingarnar eru uppfærðar ef greiðsluáætlunin hefur þegar verið skuldfærð, en þá var prósentunni breytt á greiðsluáætlunarlínunni. Allar línur sem eru reikningsfærðar eftir þá breytingu munu nota nýju prósentuna.

> [!NOTE]
> - Ekki er hægt að nota valkost fyrir skiptingu viðskiptavina fyrir vörur á lager.
> - Ef gátreiturinn **Óreikningsfærðar tekjur** er valinn er ekki hægt að velja gátreitinn **Skipting viðskiptavinar**.
> - Ef þú notar **Aðeins tekjuskiptingu** hefur yfirlínan valkostinn **Skipting viðskiptavinar** en undirlínan ekki.

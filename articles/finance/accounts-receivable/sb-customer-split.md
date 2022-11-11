---
title: Skipting viðskiptavina á innheimtuáætlunum
description: Þessi grein lýsir því hvernig á að skipta viðskiptavini þegar áskriftarreikningur er notaður.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746332"
---
# <a name="customer-split-on-billing-schedules"></a>Skipting viðskiptavina á innheimtuáætlunum

Á innheimtuáætlun, sem *reikningsreikning* er viðskiptavinurinn sem fær sölupöntunarreikninginn svo hann geti greitt reikninginn. Í sumum tilfellum geta fleiri en einn viðskiptavinur greitt reikning. The **Viðskiptavinaskipting** virkni gerir þér kleift að bæta við fleiri viðskiptavinum sem hægt er að rukka fyrir sömu innheimtuáætlun. Til að virkja þessa virkni skaltu fara á **Innheimta áskriftar \> Endurtekinn samningsreikningur \> Uppsetning \> Endurteknar innheimtufæribreytur samnings**, og stilltu **Viðskiptavinaskipting** valmöguleika til **Já**.

## <a name="customer-split-on-the-billing-schedule-header"></a>Viðskiptavinaskipting á haus innheimtuáætlunar

Eftir að innheimtuáætlun er búin til er hægt að bæta fleiri viðskiptavinum við haus innheimtuáætlunar.

Til að bæta við viðskiptavini skaltu fylgja þessum skrefum.

1. Á **Innheimtuáætlun** flipa, veldu **Viðskiptavinaskipting**. The **Viðskiptavinareikningur** og **Nafn viðskiptavinarreiknings** reitirnir efst tilgreina viðskiptavininn sem er úthlutað sem **Viðskiptavinur innheimtuáætlunar**.

    > [!NOTE]
    > Viðskiptavinareikningurinn sem þú bætir við getur ekki verið sá sami og reikningsreikningurinn.

2. Á **Skiptar línur viðskiptavina** flipa, veldu **Bæta við línu**.
3. Veldu viðskiptavin og sláðu síðan inn prósentu hvers reiknings fyrir þann viðskiptavin.
4. Sjálfgefið er að upphafs- og lokadagsetningar innheimtuáætlunarinnar eru notaðar sem upphafs- og lokadagsetningar. Sláðu inn mismunandi upphafs- og lokadagsetningar ef nýi viðskiptavinurinn mun greiða tilgreinda prósentu fyrir aðeins hluta af innheimtuáætluninni. Til dæmis, ef innheimtuáætlunin er með upphafsdagsetningu 1. janúar og lokadagsetningu 31. desember, og nýi viðskiptavinurinn er rukkaður um 40 prósent fyrir fyrstu níu mánuðina, skal tilgreina 1. janúar sem upphafsdag og 30. september sem lokadagsetningu, og sláðu inn **40.00** sem hlutfall.

Hægt er að bæta fleiri en einum viðskiptamanni við skiptingarlínur viðskiptavinar. Í þessu tilviki má heildarhlutfallið sem er slegið inn ekki fara yfir 100 prósent. Færið inn tilvísun viðskiptavinar og beiðni viðskiptavinar sem upplýsingareitir sem verða sýndir á sölupöntunarlínunni á meðan **Búðu til reikning** ferli.

Línuupplýsingarnar munu sýna tengiliðaupplýsingar, afhendingarfang, heimilisfang reiknings og greiðsluupplýsingar þeirra viðskiptavina sem bætt var við. Þessar upplýsingar verða einnig sýndar á sölupöntun fyrir viðskiptavini.

Þegar þú bætir upplýsingum um skiptingu viðskiptavina við haus innheimtuáætlunar, ef það eru óinnheimtar línur innheimtuáætlunar á innheimtuáætluninni, færðu eftirfarandi skilaboð sem biðja þig um að rúlla niður breytingarnar: "Viltu færa breytinguna niður frá kl. hausinn á línurnar? Breytingar munu aðeins uppfæra innheimtuáætlunarlínur sem ekki eru innheimtar." Veldu **Já** til að uppfæra upplýsingar um skiptingu viðskiptavinar á innheimtuáætlunarlínunni. Breytingar verða ekki uppfærðar ef innheimtuáætlunarlínan hefur þegar verið innheimt.

Ef innheimtuáætlun er búin til með því að nota **Afrita áætlun** valmöguleika, sjálfgefnar upplýsingar verða færðar inn á skiptar hauslínur viðskiptavina. Það getur ekki verið það sama og viðskiptavinareikningurinn.

Þegar **Búðu til reikning** ferli er lokið verða margar sölupantanir búnar til. (Margir sölureikningar verða einnig búnir til ef sjálfvirk bókun er notuð.) Þessar sölupantanir og sölureikninga er hægt að skoða á **Reikningur** flipann á **Upplýsingar um línu** Flýtiflipi á **Skoða innheimtuupplýsingar** síðu. **Margfeldi** er sýnt á línu innheimtuupplýsinga til að gefa til kynna að margar sölupantanir og sölureikningar hafi verið búnar til.

## <a name="customer-split-on-billing-schedule-lines"></a>Skipting viðskiptavina á línum innheimtuáætlunar

Hægt er að bæta viðskiptamannaskiptingunni við einstakar innheimtuáætlunarlínur ef þú vilt skipta aðeins ákveðnum innheimtuáætlunarlínum. Veldu **Viðskiptavinaskipting** gátreitinn á línunni og veldu síðan **Viðskiptavinaskipting** á valmyndinni fyrir innheimtuáætlunarlínuna til að uppfæra eða slá inn upplýsingar um skiptingu viðskiptavinar.

Endurskoðunarupplýsingarnar eru uppfærðar ef innheimtuáætlun hefur þegar verið innheimt, en þá var hlutfallinu breytt á innheimtuáætlunarlínunni. Allar línur sem eru innheimtar eftir þá breytingu munu nota nýja prósentuna.

> [!NOTE]
> - Ekki er hægt að nota valkostinn fyrir skiptingu viðskiptavina með vörum á lager.
> - Ef **Óinnheimtar tekjur** gátreiturinn er valinn, the **Viðskiptavinaskipting** Ekki er hægt að velja gátreitinn.
> - Ef þú notar **Tekjuskipting eingöngu** valkostur, móðurlínan hefur **Viðskiptavinaskipting** valmöguleika, en undirlínuatriðin gera það ekki.

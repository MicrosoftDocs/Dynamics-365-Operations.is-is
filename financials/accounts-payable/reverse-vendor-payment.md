---
title: "Bakfæra greiðslu lánardrottins"
description: "Þessi grein lýsir muninum á að bakfæra, eyða, ógilda og hafna greiðslu. Einnig útskýrir hún aðferðirnar tvær við að bakfæra ávísun lánardrottins."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6362a958690ba3ba04c44d24d747a3021887037c
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="reverse-a-vendor-payment"></a>Bakfæra greiðslu lánardrottins

[!include[banner](../includes/banner.md)]


Þessi grein lýsir muninum á að bakfæra, eyða, ógilda og hafna greiðslu. Einnig útskýrir hún aðferðirnar tvær við að bakfæra ávísun lánardrottins. 

Einstaka sinnum, eftir að greiðsla lánardrottins hefur verið bókuð, verður að bakfæra greiðsluna. Bakfærsla er ólík eyðingu, ógildingu eða höfnun greiðslu. Aðeins er hægt að eyða greiðslu ef staða hennar er **Stofnað**. Þessi staða tilgreinir að greiðslan hefur verið stofnuð en hefur ekki enn verið mynduð. Þessi takmörkun gildir alltaf, óháð greiðsluaðferð. Hægt er að ógilda óbókaðar ávísanir eftir að þær hafa verið myndaðar en áður en þær hafa verið bókaðar. Ef mynduð greiðsla er gerð sem rafræn sjóðamillifærsla (EFT) er hægt að hafna greiðslu áður en hún er bókuð. Til að hafna greiðslu þarf að breyta gildinu **Greiðslustaða**. Hægt er að endurmynda greiðslu sem hefur verið ógild eða hafnað eftir að gildinu **Greiðslustaða** er breytt til baka í **Ekkert**. 

Bakfærslur eru notaðar eftir að greiðsla er bókuð. Ekki er hægt að bakfæra rafrænar greiðslur eftir að þær hafa verið bókaðar. Í staðinn, verður að stofna nýja færslu fyrir upphæð greiðslu til að fá skuld aftur á reikning lánardrottins. Það eru tvær aðferðir til þess að bakfæra ávísanir. Í einni aðferð eru bakfærslur bókaðar strax þegar smellt er á **Greiðslubakfærsla** á síðunni **Ávísun**. Hin aðferðin er þannig að þegar smellt er á hnappinn **Greiðslubakfærsla** á síðunni **Ávísun** er bakfærslan fyrst send í færslubókina Reiðufjár- og bankastjórnun þar sem skoðunarmaður getur bókað eða hafnað bakfærslunni. 

Til að fræðast um hvaða aðferð fyrirtækið notar skal skoða síðuna **Færibreytur reiðufjár- og bankastjórnunar**. Ef valkosturinn **Nota endurskoðunarferlið fyrir greiðslubakfærslur** er stilltur á **Já** eru bakfærslur sendar í bakfærslubók til skoðunar. Eftirfarandi tafla lýsir því hvernig mismunandi aðferðir til bakfærslu.

| Ef fyrirtækið fer ekki yfir bakfærslur ávísana áður en bókað er                                                                                                                                  | Ef fyrirtækið fer yfir bakfærslur ávísana áður en bókað er                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ávísunin er bakfærð strax þegar smellt er á **Í lagi** á síðunni **Ávísun**.                                                                                                                      | Ávísunin er ekki strax bakfærð. Færslubók fyrir bakfærslu ávísana er stofnuð fyrir endurskoðun. Ef bakfærslubók er eytt er hægt að bakfæra ávísun aftur.                                                                                                                                                                                                                                                                |
| Bókhaldsfærslur fyrir upphaflega ávísunin er bakfærð.                                                                                                                                         | Fjárhagslykillinn úr bókhaldsfærslu upprunalegrar ávísunar er hugsanlega ekki bókaður. Fjárhagsvíddir úr færslubók upphaflegrar ávísuninar eru notaðar sem sjálfgefnar fjárhagsvíddir í færslubók fyrir bakfærslu ávísana. Hægt er að breyta þessum sjálfgefnu gildum. Þegar bakfærslubók er bókuð eru aðallyklar fyrir Viðskiptaskuldir færðir inn sjálfkrafa af bókunarreglunum, sem gætu hafa breyst. |
| Skipan bókhald sem var notaður þegar upprunalega ávísunin var bókuð er notuð til að bakfæra ávísun, jafnvel þótt lykilskipulagi hefur verið breytt. Lyklasamsetningin er ógild. | Ef lykilskipulagi breytt eftir að upphaflega ávísunin var bókaður, þarf hugsanlega nýja fjárhagsvídd fyrir bakfærslu ávísunar. Þessi fjárhagsvídd er hugsanlega ekki færð sjálfvirkt inn úr upphaflegri greiðslubók. Samsetning lykils er villuleitað þegar bakfærsla ávísunar er bókuð.                                                                                                        |
| Fastar víddir eru ekki notaðar á bakfærsluna til að aðstoða við að tryggja að sömu fjárhagslyklar séu bakfærðir.                                                                                      | Fastar víddir notaðar bakfærslubók við bókun. Fjárhagsvíddargildið hugsanlega ekki í lykilfærslu fyrir upprunaleg ávísun, eftir því hvenær föst vídd var skilgreind.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Bakfæra bókaðar ávísanir án þess að endurskoða þær
Ef fyrirtækið vill bóka bakfærslur ávísana strax þegar smellt er á **Greiðslubakfærsla** á síðunni **Ávísanir**. Á síðunni **Færibreytur reiðufjár- og bankastjórnunar** skal stilla valkostinn **Nota endurskoðunarferlið fyrir greiðslubakfærslur** á **Nei**. Á síðunni **Ávísanir** er hægt að velja ávísun til að bakfæra og velja **Greiðslubakfærsla**. Síðan er hægt að færa inn dagsetninguna og ástæðu bakfærslunnar.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Bakfæra bókaðar ávísanir eftir að þær eru endurskoðaðar í bakfærslubók ávísana
Ef fyrirtækið vill að fara yfir bakfærslur ávísana áður en þær eru bókaðar skal stofna í bakfærslubók fyrir yfirferð og á síðunni **Færibreytur reiðufjár- og bankastjórnunar** og stilla valkostinn **Nota endurskoðunarferlið fyrir greiðslubakfærslur** á **Já**. Á síðunni **Ávísanir** er hægt að velja ávísun til að bakfæra og velja **Greiðslubakfærsla**. Síðan er hægt að færa inn dagsetninguna og ástæðu bakfærslunnar. Einnig verður að velja færslubókarheiti til að stofna færslubók í færslubók fyrir bakfærslu ávísana.

### <a name="review-a-reversal"></a>Skoða bakfærslu

Ef þú ert notandi sem á að skoða bakfærslur geturðu annaðhvort samþykkt og bókað færslubókina eða hafnað bakfærslunni með því að eyða færslubókinni. Á síðunni **Færslubók fyrir bakfærslu ávísana** er hægt að velja bakfærslubókina sem á að endurskoða og smellið síðan á **Línur**. Hægt er að skoða bakfærða ávísun og velja síðan einn af eftirfarandi samþykktarkostum:

-   Til að samþykkja og bóka bakfærslubókina er smellt á **Bóka** eða **Bóka og millifæra**.
-   Ef hafna á bakfærslu er bakfærslulínunni eytt.

> [!NOTE]
> Ef færslubókinni er eytt er bakfærslan fjarlægð úr kerfinu en upphaflega ávísunin er áfram í skjámyndinni **Ávísun**. Staða ávísunarinnar er ekki lengur **Bíður afturköllunar**.

## <a name="results-of-posting-a-reversal"></a>Niðurstaða af bókun bakfærslu
Þegar bakfærsla ávísunar er bókuð gerist eftirfarandi:

-   Staða ávísunarinnar er uppfærð í **Afturköllun**.
-   Ef gátreiturinn **Afstemma** var valinn í bakfærsluskjámyndinni við bakfærsluna er ávísunin stemmd af (gátreiturinn **Afstemmt** er valinn) og verður ekki birt í skjámyndinni **Lykilafstemming**.
-   Fylgiskjal bakfærslunnar er bókað á móti bankareikningnum sem ávísunin var gefin út af, til að hækka stöðu bankareikningsins.
-   Fylgiskjalið er bókað í fjárhag.
-   Breytingarupplýsingarnar eru uppfærðar í reitaflokknum **Saga** á síðunni **Ávísun**.

> [!NOTE] 
> Þegar ávísun sem var gefin út vegna samstæðuviðskiptafærslu er bakfærð koma mótfærslurnar úr bókhaldsuppsetningu fyrir samstæðuviðskiptin, ekki úr upphaflegu færslunni. Ef ávísunin sem var bakfærð var gefin út vegna greiðslu til lánardrottins gerist einnig eftirfarandi:

-   Upphaflega greiðslan úr reikningnum sem greiðslan var jöfnuð á móti er ófærð (jöfnunin er bakfærð).
-   Færsla er bókuð á lánardrottnalykill vegna greiðslubakfærslunnar og bakfærða greiðslan er jöfnuð á móti upphaflegu greiðslunni. Reiturinn **Síðasta uppgjörsfylgiskjal** í skjámyndinni **Lánardrottnafærslur** fyrir upphaflegu lánardrottinsgreiðsluna er uppfærður svo að hann sýni fylgiskjalsnúmer bakfærðu færslunnar.

Ef ávísunin sem var bakfærð var gefin út vegna endurgreiðslu viðskiptavinar gerist einnig eftirfarandi:

-   Færsla er bókuð á mótiviðskiptavinalykill vegna greiðslubakfærslunnar og jöfnunin milli upphaflegu greiðslunnar og skjalsins sem greiðslan var upphaflega jöfnuð á móti er bakfærð (neikvæð greiðsla er stofnuð).
-   Bakfærslu á greiðslu er jafnað við upphaflegu greiðsluna. Reiturinn **Síðasta uppgjörsfylgiskjal** á síðunni **Færslur viðskiptavina** fyrir upphaflegu lánardrottinsgreiðsluna er uppfærður svo að hann sýni fylgiskjalsnúmer bakfærðu færslunnar.






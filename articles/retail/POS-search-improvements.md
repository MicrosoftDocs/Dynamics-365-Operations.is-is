---
title: "Leit að vöru og leit að viðskiptavinum í POS"
description: "Þetta efnisatriði gefur yfirlit yfir úrbætur sem hafa verið gerðar á vöru og viðskiptahugbúnaði í Dynamics 365 for Retail."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2af45de0d63b01e71b5009e2f62cfdff6844da7d
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Yfirlit yfir vöru og viðskiptavinaleit í sölustað

[!include[banner](includes/banner.md)]

Modern Point of Sale  (MPOS) og Cloud Point of Sale (CPOS) bjóða upp á þægilegan leitarvirkni sem leyfir verslunarmönnum að fljótt leita að vörum og viðskiptavinum. Leitarastikan er alltaf til staðar efst á MPOS og CPOS, þannig að starfsmenn geti fljótt fundið vörur og viðskiptavini.

Starfsmenn geta leitað að vörum í vöruflokkunum og vörulistunum sem tengjast núverandi verslun og í úrvali og vörulistum sem tengjast öðrum verslunum í fyrirtækinu. Þannig geta gjaldkerar selt og skilað vörum utan framboðs í vöruhúsi. Á sama hátt geta starfsmenn leitað að viðskiptavinum sem tengjast núverandi verslun eða annarri verslun í fyrirtækinu. Auk þess geta starfsmenn leitað að viðskiptavinum sem tengjast öðru fyrirtæki í móðurfyrirtækinu.

## <a name="product-search"></a>Afurðaleit 

Sjálfgefið er að leita að vöru í vöruúrvali verslunar. Þessi tegund leitar er þekktur sem *staðbundin vöruleit*. Hins vegar geta starfsmenn auðveldlega skipt yfir í hvaða verslun sem er í tengslum við núverandi verslun eða þeir geta leitað í annarri verslun. Þessi tegund leitar er þekktur sem *Fjartengd vöruleit*. Til að breyta vörulistanum hnappinn **Flokkar**  til vinstri á síðunni. Efst á glugganum sem birtist skaltu velja hnappinn hnappinn **Breyta vörulista**og þá velja einn af tiltækum vörulista til að skoða. Kerfið mun leita að vörum í valda vörulistanum.

Á síðunni **Breyta verslun** geta starfsmenn auðveldlega valið hvaða verslun sem er, eða þeir geta leitað að vörum í öllum verslunum.

![Breyting á vörulilstanum](./media/Changecatalog.png "Breyting á vörulilstanum")
 
Staðbundin vöruleit leitar innan eftirfarandi vöru eiginleika:

- Afurðarnúmer
- Afurðarnafn
- lýsing
- Víddir
- Strikamerki
- Leita að nafni

### <a name="enhancements-to-local-product-searches"></a>Viðbætur við staðbundna vöruleit

Uppllifun af staðbundinni vöruleit hefur verið gerð notaendavænni. Eftirfarandi endurbætur hafa verið gerðar:

- Fellivalmyndum fyrir vöru og viðskiptavini hefrui verið bætt við leitarreitinn svo starfsmenn geti valið annaðhvort **Vara** eða **Viðskiptavinur** áður en þeir gera leitina. Sjálfgefið er **Vara**valið, eins og sýnt er á myndinni sem hér á eftir.
- Til að leita að mörgum leitarorðum (það er fyrir leitir sem nota leitarskilyrði) geta smásalar stillt á hvort leitarniðurstöður innihalda niðurstöður sem passa við leitarniðurstöður eða aðeins niðurstöður sem passa við öll leitarorð. Þessi stilling er fáanleg í POS virknisniðinu, undir nýjum hópi sem heitir **Vöruleit** Sjálfgefna stillingin er **Samsvara hvaða leitarorði sem er**. Þetta er einnig ráðlögðstilling. Þegar **Samsvara hvaða leitarorði sem er** er notuð í leitarskilmálum eru allar vörur sem eru að fullu eða að hluta til samsvörun einum eða fleiri leitarskilmálum skilað sem niðurstöður og niðurstöðurnar eru sjálfkrafa flokkaðar í hækkandi röð af vörum sem eru mest samsvörun leitarorðs (full eða að hluta).

    Stillingin **Samsvara hvaða leitarorði sem er** skilar aðeins vörum sem passa við öll leitarorð (að fullu eða hluta). Þessi stilling er gagnleg þegar vörunöfnin eru löng og starfsmenn vilja sjá aðeins takmarkaðar vörur í leitarniðurstöðum. Hins vegar er þessi leit með tveimur takmörkunum:

    - Leitin er gerð í einstökum vörueiginleikum. Til dæmis birtast aðeins vörur sem eru með öll leitarorð í að minnsta kosti einum eiginleika voru.
    - Ekki er leitað í víddum.

- Söluaðilar geta nú skilgreint vöruleit til að sýna leitarniðurstöður sem vöruheiti fyrir gerðir notenda. Ný stilling fyrir þessa virkni er að finna í POS virkni sniðinu, undir hópi sem heitir **Vöruleit**. Stillingin heitir **Sýna leitaruppástungur meðan þú skrifa**. Þessi virkni getur hjálpað starfsmönnum að finna fljótt vöruna sem þeir leita að, vegna þess að þeir þurfa ekki að slá inn heitið handvirkt.
- Vöruleit reikniritin leitar nú einnig að leitarorðum í eiginleikanum **Leita í heiti** fyrir vöruna.

![Afurðatillögur](./media/Productsuggestions.png "Afurðatillögur")

## <a name="customer-search"></a>Viðskiptavinaleit

Viðskiptavinaleit er notuð til að finna viðskiptavini í ýmsum tilgangi. Til dæmis gætu gjaldkerar viljað sjá óskalista viðskiptavina eða kaupferil eða bæta við viðskiptavininum við viðskipti. Þegar um er að ræða leit með mörgum leitarorðum skilar viðskiptavinareikniritið öllum viðskiptavinum sem samsvara einhverju leitarorða. Hins vegar birtast viðskiptavinir sem samsvara flestum leitarorðum efst á niðurstöðum. Þessi hegðun er hliðstæð því hvernig aðrar leitarvélar sýna árangur. Þeir sýna fyrst niðurstöðurnar sem passa við leitina sem mest leitað, og þá sýna þær niðurstöðurnar sem að hluta samsvara leitarorðum. Þessi hegðun hjálpar gjaldkea í aðstæðum þar sem þau nota mörg leitarorð  ef eitt af leitarorðum hefur stafsetningarvillu.

Sjálfgefið er að leita viðskiptavina í aðsetursbókum viðskiptavina sem tengjast versluninni. Þessi tegund leitar er þekkt sem *Staðbundin viðskiptavinarleit* Einnig má leita að að viðskiptavinum altækt. Með öðrum orðum geta þeir leitað yfir verslanir félagsins og yfir alla aðra lögaðila. Þessi tegund leitar er þekktur sem *Fjartengd viðskiptavinarleit*

Til að leita altækt geta starfsmenn valið hnappinn **Sía niðurstöður** neðst á síðunni og síðan valið valkostinn **Leita í öllum verslunum**, eins og sýnt er á myndinni á eftir. Í þessu tilviki eru ekki aðeins viðskiptavinir sýndir. Allar tegundir aðila sem eru hluti af hverri aðsetursbók í höfuðstöðvum eru einnig sýndir. Þessir aðilar eru starfsmenn, seljendur, tengiliðir og samkeppnisaðilar.

> [!NOTE]
> Færa þarf inn minnst fjóra stafi til að leit að fjartengdum viðskiptavinum skili niðurstöðum.

Í Fjartengd viðskiptavinarleit er kenni viðskiptavinar ekki sýnt viðskiptavinum frá öðrum lögaðilum aþr sem ekkert kenni viðskiptavinar hefur verið stofnað fyrir þá aðila í núverandi fyrirtæki. Hins vegar, ef starfsmaður opnar síðuna með viðskiptavinarupplýsingum, býr kerfið sjálfkrafa til viðskiptavinarkenni fyrir aðila og tengir einnig aðsetursbækur viðskiptavina verslunar við viðskiptavininn. Þess vegna verður viðskiptavinurinn sýnilegur í staðbundnum leitum sem eru gerðar síðar.

![Altæk viðskiptavinarleit](./media/Globalcustomersearch.png "Altæk viðskiptavinarleit")

### <a name="enhancements-to-local-customer-searches"></a>Viðbætur við staðbundnar leitir að viðskiptavinum

Leit í staðbundnum viðskiptavinum hjálpar starfsmönnum að finna viðskiptavini fljótt eftir símanúmeri. Starfsmenn þurfa ekki að slá inn sérstaka stafi sem hafa verið bætt við símanúmer viðskiptavinarins, svo sem bil, bandstrik eða sviga. Þó gjaldkerar geti geymt símanúmer á hvaða sniði sem er (til dæmis geta þeir innihaldið sviga, vísbendingu, tákn og svo framvegis), geta þeir leitað eftir viðskiptavinum með því að slá inn hluta símanúmer. Ef gjaldkeri hefur með sérstaka stafi þegar hann eða hún slær inn símanúmer, geta aðrir gjaldkerar fundið viðskiptavininn með því að slá inn tölurnar sem birtast eftir sérstafina. Til dæmis, ef símanúmer viðskiptavinar var skráð sem  **123-456-7890**, getur gjaldkeri leitað að viðskiptavininn með því að slá inn **123**, **456**, **7890**, eða **1234567890** eða með því að slá inn fyrstu tölurnar í símanúmerinu.


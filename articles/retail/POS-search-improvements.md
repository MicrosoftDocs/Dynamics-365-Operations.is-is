---
title: "Leit að vöru og leit að viðskiptavinum í sölustað (POS)"
description: "Þetta efnisatriði gefur yfirlit yfir úrbætur sem hafa verið gerðar á vörum og leitaraðgerð viðskiptavina í Microsoft Dynamics 365 for Retail."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/28/2018
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 50b0cec27e343b3b6aba464a04c9883160ab263a
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Leit að vöru og leit að viðskiptavinum í sölustað (POS)

[!include [banner](includes/banner.md)]

Nútíma Point of Sale (MPOS) og Point of Sale (CPOS) í skýi bjóða upp á auðvelda leitaraðgerð á vörum og viðskiptavinum. Leitarstikan er alltaf til staðar efst í gluggum MPOS og CPOS, þannig að starfsmenn geti leitað að vörum og viðskiptavinum á fljótlegan hátt.

Starfsmenn geta leitað að vörum í vöruúrvali og vörulistum sem tengjast núverandi verslun. Þeir geta einnig leitað í vöruúrvali og vörubæklingum sem tengjast öðrum verslunum í fyrirtækinu. Þannig geta gjaldkerar selt og skilað vörum utan framboðs í vöruhúsi. Með svipuðum hætti geta starfsmenn leitað að viðskiptavinum sem tengjast núverandi verslun eða annarri verslun í fyrirtækinu. Auk þess geta starfsmenn leitað að viðskiptavinum sem tengjast öðru fyrirtæki í móðurfyrirtækinu.

## <a name="product-search"></a>Afurðaleit

Sjálfgefið er að vöruleitir séu gerðar á vöruúrvali verslunar. Þessi tegund leitar er þekktur sem *staðbundin vöruleit*. Hins vegar geta starfsmenn auðveldlega skipt yfir í hvaða verslun sem er í tengslum við núverandi verslun eða þeir geta leitað í annarri verslun. Þessi tegund leitar er þekktur sem *Fjartengd vöruleit*. Til að breyta vörulistanum hnappinn **Flokkar**  til vinstri á síðunni. Efst á glugganum sem birtist skaltu velja hnappinn hnappinn **Breyta vörulista**og þá velja einn af tiltækum vörulista til að skoða. Kerfið mun leita að vörum í valda vörulistanum.

Á síðunni **Breyta verslun** geta starfsmenn auðveldlega valið hvaða verslun sem er, eða þeir geta leitað að vörum í öllum verslunum.

![Breyting á vörulilstanum](./media/Changecatalog.png "Breyting á vörulilstanum")
 
Staðbundin vöruleit leitar í eftirfarandi vörueiginleikum:

- Afurðarnúmer
- Afurðarnafn
- lýsing
- Víddir
- Strikamerki
- Leita að nafni

### <a name="enhancements-to-local-product-searches"></a>Viðbætur við staðbundna vöruleit

Reynslan af staðbundinni vöruleit er nú notendavænni. Eftirfarandi endurbætur hafa verið gerðar:

- Fellivalmyndum fyrir vöru og viðskiptavini hefrui verið bætt við leitarreitinn svo starfsmenn geti valið annaðhvort **Vara** eða **Viðskiptavinur** áður en þeir gera leitina. Sjálfgefið er **Vara**valið, eins og sýnt er á myndinni sem hér á eftir.
- Til að leita að mörg lykilorð í leit (það er fyrir leitir sem nota leitarorð) geta smásalar stillt hvort leitarniðurstöður innihaldi niðurstöður sem passa við *eitthvert* leitarorð eða aðeins niðurstöður sem passa við *öll* leitarorð. Þessi stilling er fáanleg í POS virknisniðinu, undir nýjum hópi sem heitir **Vöruleit**. Sjálfgefna stillingin er **Samsvara hvaða leitarorði sem er**. Þetta er einnig ráðlögðstilling. Þegar stillingin **Samsvara hvaða leitarorð sem er** er notuð, er öllum vörum sem passa að fullu eða hluta til við eitt eða fleiri leitarorð skilað sem niðurstöður. Þessar niðurstöður eru sjálfkrafa flokkaðar í hækkandi röð af vörum sem hafa mestu samsvörun við leitarorðin (að fullu eða að hluta).

    Stillingin **Samsvara hvaða leitarorði sem er** skilar aðeins vörum sem passa við öll leitarorð (að fullu eða hluta). Þessi stilling er gagnleg þegar vörunöfnin eru löng og starfsmenn vilja sjá aðeins takmarkaðar vörur í leitarniðurstöðum. Hins vegar er þessi leit með tveimur takmörkunum:

    - Leitin er gerð í einstökum vörueiginleikum. Til dæmis birtast aðeins vörur sem eru með öll leitarorð í að minnsta kosti einum eiginleika voru.
    - Ekki er leitað í víddum.

- Söluaðilar geta nú skilgreint vöruleit til að sýna leitarniðurstöður sem vöruheiti fyrir gerðir notenda. Ný stilling fyrir þessa virkni er að finna í POS-virknisniðinu, undir hópi sem heitir **Vöruleit**. Stillingin heitir **Sýna leitaruppástungur meðan þú skrifa**. Þessi virkni getur hjálpað starfsmönnum að finna fljótt vöruna sem þeir leita að, vegna þess að þeir þurfa ekki að slá inn heitið handvirkt.
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

### <a name="enhancements-to-local-customer-search"></a>Viðbætur við staðbundna leit að viðskiptavinum

Leitir sem eru byggðar á símanúmerinu hafa verið einfaldaðar. Þessar leitir hunsa nú sérstafi, t.d. bilum, bandstrikum og svigum, sem kunna að hafa verið bætt við þegar viðskiptavinurinn var búinn til. Þess vegna þurfa gjaldkerar ekki að hafa áhyggjur af símanúmersniðinu þegar þeir leita. Þeir geta einnig leitað eftir viðskiptavinum með því að slá inn hluta úr símanúmeri. Ef símanúmer inniheldur sérstafi er einnig hægt að finna það með því að leita að tölunum sem birtast eftir sérstafinu. Til dæmis, ef símanúmer viðskiptavinar var slegið inn sem **123-456-7890**, getur gjaldkeri leitað að viðskiptavinum með því að slá inn **123**, **456**, **7890** eða **1234567890** eða með því að slá inn fyrstu tölur símanúmersins.

Hefðbundna viðskiptaleitin getur verið tímafrek vegna þess að hún leitar yfir mörg svæði. Þess í stað geta gjaldkerar nú leitað í einum sérsniðnum eiginleika, eins og nafni, netfangi eða símanúmeri. Eiginleikarnir sem reiknirit viðskiptavinaleitar notar eru sameiginlega þekktir sem *leitarskilyrði viðskiptavinar*. Kerfisstjórinn getur auðveldlega stillt eitt eða fleiri skilyrði sem flýtileiðir sem birtast í POS. Vegna þess að leitin er takmörkuð við eitt skilyrði, eru aðeins viðeigandi leitarniðurstöður sýndar og afköstin er mun betri en afköst staðlaðrar viðskiptavinaleitar. Eftirfarandi skýringarmynd sýnir flýtileiðir viðskiptavinaleitar í POS.

![Flýtileiðir viðskiptavinaleitar](./media/SearchShortcutsPOS.png "Flýtileiðir viðskiptavinaleitar")

Til að stilla leitarskilyrði sem flýtileiðir verður stjórnandinn að opna síðuna **Smásölufæribreytur** í Microsoft Dynamics 365 for Finance and Operations og síðan í flipanum **POS leitarskilyrði** eru öll skilyrði valin sem eiga að birtast sem flýtileiðir.

![Stilla leitarflýtileiðir](./media/ConfigureShortcutsAX.png "Stilla leitarflýtileiðir")

> [!NOTE]
> Ef þú bætir við of mörgum flýtileiðum verður fellivalmyndin á leitarstikunni í POS ofhlaðin og það getur haft áhrif á reynslu starfsmanns af leitinni. Við mælum með að þú bætir aðeins við eins mörgum flýtileiðum og nauðsynlegt er.

Reiturinn **Birta röð** ákvarðar röðina sem flýtileiðir eru sýndar í POS. Skilyrðin sem eru sýnd eru innbyggðir eiginleikar sem reiknirit viðskiptavinaleitar notar til að leita að viðskiptavinum. Hins vegar geta samstarfsaðilar bætt við sérsniðnum eiginleikum sem flýtivísunum. Til að bæta við sérsniðnum eiginleikum sem flýtivísunum þarf kerfisstjórinn að lengja framlengjanlega upptalningu (fasttexti) sem er notuð við leitarskilyrði viðskiptavinar og síðan merkja sérsniðna eiginleika samstarfsaðila sem flýtileiðir. Samstarfsaðilar bera ábyrgð á að skrifa kóðann til að finna niðurstöður þegar sérsniðnar flýtileiðir eru notaðar við leitir.

> [!NOTE]
> Sérsniðnum eiginleika sem er bætt við fasttextann hefur ekki áhrif á staðlað reiknirit viðskiptavinaleitar. Með öðrum orðum mun reiknirit viðskiptavinaleitar ekki leita í sérsniðnum eiginleikum. Notendur geta aðeins notað sérsniðna eiginleika fyrir leitir ef þessum sérsniðna eiginleika er bætt við sem flýtileið eða ef sjálfgefnu reikniriti leitar er hnekkt.


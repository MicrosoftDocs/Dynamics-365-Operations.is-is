---
title: Leit að vöru og leit að viðskiptavinum í sölustað (POS)
description: Þetta efnisatriði gefur yfirlit yfir úrbætur sem hafa verið gerðar á vöru og viðskiptahugbúnaði í Dynamics 365 Commerce.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 2b4c17b41056a35c2d2caaedb4f52998179b3c3e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022856"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Leit að vöru og leit að viðskiptavinum í sölustað (POS)

[!include [banner](includes/banner.md)]

Nútíma Point of Sale (MPOS) og Point of Sale (CPOS) í skýi bjóða upp á auðvelda leitaraðgerð á vörum og viðskiptavinum. Leitarstikan er alltaf til staðar efst í gluggum MPOS og CPOS, þannig að starfsmenn geti leitað að vörum og viðskiptavinum á fljótlegan hátt.

Starfsmenn geta leitað að vörum í vöruúrvali og vörulistum sem tengjast núverandi verslun. Þeir geta einnig leitað í vöruúrvali og vörubæklingum sem tengjast öðrum verslunum í fyrirtækinu. Þannig geta gjaldkerar selt og skilað vörum utan framboðs í vöruhúsi. Með svipuðum hætti geta starfsmenn leitað að viðskiptavinum sem tengjast núverandi verslun eða annarri verslun í fyrirtækinu. Auk þess geta starfsmenn leitað að viðskiptavinum sem tengjast öðru fyrirtæki í móðurfyrirtækinu.

## <a name="product-search"></a>Afurðaleit

Sjálfgefið er að vöruleitir séu gerðar á vöruúrvali verslunar. Þessi tegund leitar er þekktur sem *staðbundin vöruleit*. Hins vegar geta starfsmenn auðveldlega skipt yfir í hvaða verslun sem er í tengslum við núverandi verslun eða þeir geta leitað í annarri verslun. Þessi tegund leitar er þekktur sem *Fjartengd vöruleit*. Til að breyta vörulistanum velurðu hnappinn **Flokkar** til vinstri á síðunni. Efst í glugganum sem birtist skaltu velja hnappinn **Breyta vörulista** og velja síðan einn af tiltækum vörulistum til að skoða. Kerfið mun leita að vörum í valda vörulistanum.

Á síðunni **Breyta verslun** geta starfsmenn auðveldlega valið hvaða verslun sem er, eða þeir geta leitað að vörum í öllum verslunum.

![Vörulistanum breytt](./media/Changecatalog.png "Vörulistanum breytt")

Staðbundin vöruleit leitar í eftirfarandi vörueiginleikum:

- Afurðarnúmer
- Afurðarnafn
- lýsing
- Víddir
- Strikamerki
- Leita að nafni

### <a name="enhancements-to-local-product-searches"></a>Viðbætur við staðbundna vöruleit

Reynslan af staðbundinni vöruleit er nú notendavænni. Eftirfarandi endurbætur hafa verið gerðar:

- Fellivalmyndum fyrir vöru og viðskiptavini hefrui verið bætt við leitarreitinn svo starfsmenn geti valið annaðhvort **Vara** eða **Viðskiptavinur** áður en þeir gera leitina. Sjálfgefið er **Afurð** valin, eins og sýnt er á myndinni sem hér á eftir.
- Til að leita að mörg lykilorð í leit (það er fyrir leitir sem nota leitarorð) geta smásalar stillt hvort leitarniðurstöður innihaldi niðurstöður sem passa við *eitthvert* leitarorð eða aðeins niðurstöður sem passa við *öll* leitarorð. Stillingarnar fyrir þessa virkni er að finna í POS-virknisniðinu, undir nýjum hóp sem heitir **Afurðaleit**. Sjálfgefna stillingin er **Samsvara hvaða leitarorði sem er**. Þetta er einnig ráðlögðstilling. Þegar stillingin **Samsvara hvaða leitarorð sem er** er notuð, er öllum vörum sem passa að fullu eða hluta til við eitt eða fleiri leitarorð skilað sem niðurstöður. Þessar niðurstöður eru sjálfkrafa flokkaðar í hækkandi röð af vörum sem hafa mestu samsvörun við leitarorðin (að fullu eða að hluta).

    Stillingin **Samsvara hvaða leitarorði sem er** skilar aðeins vörum sem passa við öll leitarorð (að fullu eða hluta). Þessi stilling er gagnleg þegar vörunöfnin eru löng og starfsmenn vilja sjá aðeins takmarkaðar vörur í leitarniðurstöðum. Hins vegar er þessi leit með tveimur takmörkunum:

    - Leitin er gerð í einstökum vörueiginleikum. Til dæmis birtast aðeins vörur sem eru með öll leitarorð í að minnsta kosti einum eiginleika voru.
    - Ekki er leitað í víddum.

- Söluaðilar geta nú skilgreint vöruleit til að sýna leitarniðurstöður sem vöruheiti fyrir gerðir notenda. Ný stilling fyrir þessa virkni er að finna í POS-virknisniðinu, undir hópi sem heitir **Vöruleit**. Stillingin heitir **Sýna leitaruppástungur meðan þú skrifa**. Þessi virkni getur hjálpað starfsmönnum að finna fljótt vöruna sem þeir leita að, vegna þess að þeir þurfa ekki að slá inn heitið handvirkt.
- Vöruleit reikniritin leitar nú einnig að leitarorðum í eiginleikanum **Leita í heiti** fyrir vöruna.

![Afurðatillögur](./media/Productsuggestions.png "Afurðatillögur")

## <a name="customer-search"></a>Viðskiptavinaleit

Viðskiptavinaleit er notuð til að finna viðskiptavini í ýmsum tilgangi. Til dæmis gætu gjaldkerar viljað sjá óskalista viðskiptavina eða kaupferil eða bæta við viðskiptavininum við viðskipti. Reitnirit leitar parar saman leitarskilmála og þau gildi sem eru til staðar í eftirfarandi eiginleikum viðskiptavina:

- Nafn
- Netfang
- Símanúmer
- Vildarkortsnúmer
- Aðsetur
- Reikningsnúmer

Meðal þessara eiginleika gefur heitið mestan sveigjanleika fyrir leitir með mörgum leitarorðum, vegna þess að reikniritið skilar öllum viðskiptavinum sem passa við leitarniðurstöður. Viðskiptavinirnir sem samsvara flestum leitarorðum birtast efst í niðurstöðunum. Þessi aðferð hjálpar gjaldkerum í kringumstæðum þar sem þeir leita með því að slá inn fullt nafn, en eftirnafni og fornafni var víxlað við upphaflega gagnaskráningu. Hins vegar, til að skila betri afköstum, varðveita allir aðrir eiginleikar röð leitarorða. Ef röðin af leitarorðum passa ekki við pöntunina sem gögnin eru geymd í verður þess vegna engum niðurstöðum skilað.

Sjálfgefið er að leita viðskiptavina í aðsetursbókum viðskiptavina sem tengjast versluninni. Þessi tegund leitar er þekkt sem *Staðbundin viðskiptavinarleit* Einnig má leita að að viðskiptavinum altækt. Með öðrum orðum geta þeir leitað yfir verslanir félagsins og yfir alla aðra lögaðila. Þessi tegund leitar er þekktur sem *Fjartengd viðskiptavinarleit*

Til að leita altækt geta starfsmenn valið hnappinn **Sía niðurstöður** neðst á síðunni og síðan valið valkostinn **Leita í öllum verslunum**, eins og sýnt er á myndinni á eftir. Í þessu tilviki eru ekki aðeins viðskiptavinir sýndir. Allar tegundir aðila sem eru hluti af hverri aðsetursbók í höfuðstöðvum eru einnig sýndir. Þessir aðilar eru starfsmenn, seljendur, tengiliðir og samkeppnisaðilar.

> [!NOTE]
> Færa þarf inn minnst fjóra stafi til að leit að fjartengdum viðskiptavinum skili niðurstöðum.

Í Fjartengd viðskiptavinarleit er kenni viðskiptavinar ekki sýnt viðskiptavinum frá öðrum lögaðilum aþr sem ekkert kenni viðskiptavinar hefur verið stofnað fyrir þá aðila í núverandi fyrirtæki. Hins vegar, ef starfsmaður opnar síðuna með viðskiptavinarupplýsingum, býr kerfið sjálfkrafa til viðskiptavinarkenni fyrir aðila og tengir einnig aðsetursbækur viðskiptavina verslunar við viðskiptavininn. Þess vegna verður viðskiptavinurinn sýnilegur í staðbundnum leitum sem eru gerðar síðar.

![Altæk viðskiptavinaleit](./media/Globalcustomersearch.png "Altæk viðskiptavinaleit")

### <a name="enhancements-to-local-customer-search"></a>Viðbætur við staðbundna leit að viðskiptavinum

Leitir sem eru byggðar á símanúmerinu hafa verið einfaldaðar. Þessar leitir hunsa nú sérstafi, t.d. bilum, bandstrikum og svigum, sem kunna að hafa verið bætt við þegar viðskiptavinurinn var búinn til. Þess vegna þurfa gjaldkerar ekki að hafa áhyggjur af símanúmersniðinu þegar þeir leita. Þeir geta einnig leitað eftir viðskiptavinum með því að slá inn hluta úr símanúmeri. Ef símanúmer inniheldur sérstafi er einnig hægt að finna það með því að leita að tölunum sem birtast eftir sérstafinu. Til dæmis, ef símanúmer viðskiptavinar var slegið inn sem **123-456-7890**, getur gjaldkeri leitað að viðskiptavinum með því að slá inn **123**, **456**, **7890** eða **1234567890** eða með því að slá inn fyrstu tölur símanúmersins.

Hefðbundna viðskiptaleitin getur verið tímafrek vegna þess að hún leitar yfir mörg svæði. Þess í stað geta gjaldkerar nú leitað í einum eiginleika viðskiptamanns, eins og nafni, netfangi eða símanúmeri. Eiginleikarnir sem reiknirit viðskiptavinaleitar notar eru sameiginlega þekktir sem *leitarskilyrði viðskiptavinar*. Kerfisstjórinn getur auðveldlega stillt eitt eða fleiri skilyrði sem flýtileiðir sem birtast í POS. Vegna þess að leitin er takmörkuð við eitt skilyrði, eru aðeins viðeigandi leitarniðurstöður sýndar og afköstin er mun betri en afköst staðlaðrar viðskiptavinaleitar. Eftirfarandi skýringarmynd sýnir flýtileiðir viðskiptavinaleitar í POS.

![Flýtileiðir viðskiptavinaleitar](./media/SearchShortcutsPOS.png "Flýtileiðir viðskiptavinaleitar")

Til að stilla leitarskilyrði sem flýtileiðir verður stjórnandinn að opna síðuna **Færibreytur Commerce** í Commerce og síðan á flipanum **POS leitarskilyrði** eru öll skilyrði valin sem eiga að birtast sem flýtileiðir.

![Skilgreina flýtileiðir leitar](./media/ConfigureShortcutsAX.png "Skilgreina flýtileiðir leitar")

> [!NOTE]
> Ef þú bætir við of mörgum flýtileiðum verður fellivalmyndin á leitarstikunni í POS ofhlaðin og það getur haft áhrif á reynslu starfsmanns af leitinni. Við mælum með að þú bætir aðeins við eins mörgum flýtileiðum og nauðsynlegt er.

Reiturinn **Birta röð** ákvarðar röðina sem flýtileiðir eru sýndar í POS. Skilyrðin sem eru sýnd eru innbyggðir eiginleikar sem reiknirit viðskiptavinaleitar notar til að leita að viðskiptavinum. Hins vegar geta samstarfsaðilar bætt við sérsniðnum eiginleikum sem flýtivísunum. Til að bæta við sérsniðnum eiginleikum sem flýtivísunum þarf kerfisstjórinn að lengja framlengjanlega upptalningu (fasttexti) sem er notuð við leitarskilyrði viðskiptavinar og síðan merkja sérsniðna eiginleika samstarfsaðila sem flýtileiðir. Samstarfsaðilar bera ábyrgð á að skrifa kóðann til að finna niðurstöður þegar sérsniðnar flýtileiðir eru notaðar við leitir.

> [!NOTE]
> Sérsniðnum eiginleika sem er bætt við fasttextann hefur ekki áhrif á staðlað reiknirit viðskiptavinaleitar. Með öðrum orðum mun reiknirit viðskiptavinaleitar ekki leita í sérsniðnum eiginleikum. Notendur geta aðeins notað sérsniðna eiginleika fyrir leitir ef þessum sérsniðna eiginleika er bætt við sem flýtileið eða ef sjálfgefnu reikniriti leitar er hnekkt.

Í komandi útgáfu af Commerce munu smásalar geta stillt sjálfgefnar leitarstillingar viðskiptavina leitarmöguleika í POS á **Leita í öllum verslunum**. Þessar skilgreiningar geta verið gagnlegar í aðstæðum þar sem leita verður strax í viðskiptavinum sem voru stofnaðir utan POS (til dæmis, jafnvel áður en dreifingarvinnslan er keyrð). Ný valkostur **Sjálfgefnar leitarstillingar viðskiptavina** verður í boði í POS-virkniprófílnum. Stilltu hann á **Á** til að stilla sjálfgefnar leitarstillingar á **Leita í öllum verslunum**. Sérhver tilraun til viðskiptavinaleitar mun síðan gera rauntímakall í höfuðstöðvarnar.

Til að koma í veg fyrir óvænt afkastavandamál eru þessar stillingar faldar á bak við tilraunaútgáfuflagg sem heitir **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Þess vegna, til að sýna stillinguna **Sjálfgefnar leitarstillingar viðskiptavina** í notandaviðmótinu (UI) ætti smásalinn að stofna stuðningsmiða fyrir samþykkisprófun notanda (UAT) og framleiðsluumhverfi. Þegar miðinn hefur verið móttekinn munu tæknimennirnir vinna með söluaðila til að ganga úr skugga um að smásalinn framkvæmi prófanir í umhverfi utan framleiðslu til að meta árangur og framkvæma allar fínstillingar sem krafist er.

---
title: Ráðleggingar um notkun á bókunarreglum
description: Þessi grein lýsir ráðlögðum aðferðum við að stilla færslusnið.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0e321f447b78b88c065e52bb7fad1c445e47b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849903"
---
# <a name="recommended-practices-for-posting-profiles"></a>Ráðleggingar um notkun á bókunarreglum

Það eru nokkrar ráðlagðar venjur sem þú ættir að fylgja þegar þú stillir póstsnið í öllu kerfinu. Þessi grein lýsir mismunandi aðstæðum og samsvarandi ráðlögðum aðferðum.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Stilling á Ekki leyfa handvirka færslu fána

Á **Aðalreikningar** síðu, the **Ekki leyfa handvirka innslátt** gátreiturinn ætti að vera valinn fyrir hvaða aðalreikning sem er notaður fyrir færslusnið. Þessi stilling kemur í veg fyrir að notendur geti bókað dagbókarfærslu handvirkt á aðalreikninginn. Þess vegna hjálpar það að tryggja að undirbókin haldist í jafnvægi við aðalbókina og hjálpar til við að gera afstemmingarferlið auðveldara.

Ef leiðréttingar er þörf á reikningi sem er stjórnað af kerfinu og bókaður sjálfkrafa geturðu notað eina af þessum aðferðum:

- Búðu til aukaaðalreikning þar sem hægt er að bóka leiðréttingarnar. Notaðu síðan heildarreikning eða sérstaka línu á fjárhagsskýrslum þínum til að flokka og leggja saman reikningana.
- Bakfæra upprunalegu færslurnar í viðeigandi undirbók, gera allar nauðsynlegar leiðréttingar og síðan endurbóka færsluna í gegnum sama undirbók.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Að breyta bókunarsniðum eftir að færslur eru til

Ef þú breytir bókunarsniði eftir að færslur eru til, getur afstemmingin mistekist og undirbók og höfuðbók geta farið úr jafnvægi. Almennt mælum við með því að þú **ekki** breyta bókunarsniðinu eftir að færslur eru til staðar.

Ef breytinga er þörf, notaðu eftirfarandi leiðbeiningar til að tryggja heilleika kerfisins:

- Gerðu breytingarnar á lokuðu tímabili.
- Gerðu breytingarnar þegar engar aðrar færslur eiga sér stað í kerfinu.
- Staðfestu höfuðbókina og samræmdu hana við undirbók fyrir og eftir að þú gerir breytingarnar.
- Bókaðar færslur eru ekki uppfærðar ef þú breytir færslusniðinu. Íhugaðu vandlega hvort einhverjar aðlögunarfærslur séu nauðsynlegar fyrir breytinguna þína.
- Ef þú ert að breyta birgðabókunarsniðum skaltu íhuga hvernig breytingarnar munu hafa áhrif á birgðastöðu þína og fjárhagsstöðu. Sumar breytingar gætu krafist þess að þú færð birgðina í 0 (núll), lokar birgðum og færðu birgðina aftur inn eftir að breytingarnar eru gerðar.
- Prófaðu alltaf breytingar þínar í umhverfi sem ekki er í framleiðslu áður en þú gerir þær í framleiðslu.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Notkun gagnagrunnsskráningar til að endurskoða breytingar á færslusniðum

Íhugaðu að setja upp gagnagrunnsskráningu fyrir hvert færslusnið og færibreytutöflur sem stjórna færslu. Síðan, ef færibreytu eða sniði er breytt, muntu hafa fulla endurskoðunarskrá yfir hvaða gildi var breytt, hver breytti því, hvenær því var breytt og hvert fyrra gildið var. Þessar upplýsingar geta verið mikilvægar meðan á afstemmingarferlinu stendur og endurskoðandi þinn gæti þurft fylgiskjölin.

Fyrir frekari upplýsingar, sjá [Stilla gagnagrunnsskráningu](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Notaðu eftirfarandi töflu sem viðmið fyrir algeng töfluheiti sem tengjast færslusniðum og tengdum færslubreytum.

| Síðuheiti | Slóð | Töfluheiti |
|-----------|-----------------|------------|
| Færibreytur viðskiptaskulda | Viðskiptaskuldir&gt; Uppsetning&gt; Færibreytur viðskiptaskulda | VendParm |
| Bókunarregla lánardrottna | Viðskiptaskuldir&gt; Uppsetning&gt; Birtingarsnið söluaðila | VendPosting |
| Gjaldakóði | Viðskiptaskuldir&gt; Uppsetning gjalda&gt; Gjaldkóði eða viðskiptakröfur&gt; Uppsetning gjalda&gt; Gjaldkóði | MarkupTable |
| Greiðsluhættir | Viðskiptaskuldir&gt; Uppsetning greiðslu&gt; Greiðslumáti | VendPaymMode |
| Staðgreiðsluafslættir | Viðskiptaskuldir&gt; Uppsetning greiðslu&gt; Staðgreiðsluafsláttur eða viðskiptakröfur&gt; Uppsetning greiðslu&gt; Staðgreiðsluafsláttur | CashDisc |
| Greiðslugjald (seljandi) | Viðskiptaskuldir&gt; Uppsetning greiðslu&gt; Greiðslugjald | VendPaym Fee |
| Færibreytur viðskiptakrafa | Reikningur fáanlegur&gt; Uppsetning&gt; Færibreytur viðskiptakrafna | CustParm |
| Bókunarreglur viðskiptavina | Reikningur fáanlegur&gt; Uppsetning&gt; Færsluprófíl viðskiptavinar | CustPosting |
| Greiðsluhættir | Reikningur fáanlegur&gt; Uppsetning greiðslu&gt; Greiðslumáti | CustPaymMode |
| Greiðslugjald (viðskiptavinur) | Reikningur fáanlegur&gt; Uppsetning greiðslu&gt; Greiðslumáti | CustPaym Fee |
| Færibreytur fyrir útleigu eignar | Eignaleiga&gt; Uppsetning&gt; Eignaleiga færibreytur | AssetLeasePosting Accounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Bankareikningar | Handbært fé og bankastjórnun&gt; Bankareikningar&gt; Bankareikningar | Bankareikningatöflu |
| Bankafærslugerðir | Handbært fé og bankastjórnun&gt; Uppsetning&gt; Tegundir bankaviðskipta | BankTransType |
| Niðurfellingarreglur | Sameiningar&gt; Uppsetning&gt; Brotthvarfsregla | Ledger Elimination Rule<br>Ledger Elimination RuleLines |
| Kostnaðartegundir | Kostnaðarstjórnun&gt; Uppsetning&gt; Almennt&gt; Kostnaðarflokkar | Verkefnaflokkar |
| Eignafæribreyta | Fastafjármunir&gt; Uppsetning&gt; Fasteignabreytur | Eignastærðir |
| Bókunarreglur eigna | Fastafjármunir&gt; Uppsetning&gt; Birtingarsnið eigna | AssetLedger Accounts<br>Eignaráðstöfunarstærðir |
| Gjaldmiðilsendurmatslyklar | Aðalbók&gt; Gjaldmiðlar&gt; Gjaldeyrisendurmatsreikningar | CurrencyLedgerGainLoss Account |
| Lyklar fyrir sjálfvirkar færslur | Aðalbók&gt; Uppsetning færslu&gt; Reikningar fyrir sjálfvirkar færslur | LedgerSystemAccounts |
| Samstæðulyklar | Aðalbók&gt; Uppsetning færslu&gt; Millifélagareikningar | LedgerIntercompany |
| Skilgreiningar færslubókana | Aðalbók&gt; Uppsetning færslu&gt; Færslubókunarskilgreiningar | JournalizingDefinitionTrans |
| Bókunarskilgreiningar | Aðalbók&gt; Uppsetning færslu&gt; Skilgreiningar á færslu | JournalizingDefinition |
| Bókun (birgðahald) | Vörustjórnun&gt; Uppsetning&gt; Birting&gt; Birting | InventPosting |
| Kostnaðargerðakóðar | Landaður kostnaður&gt; Kostnaðaruppsetning&gt; Kostnaðartegundarkóðar | ITMCostTypeTable |
| Forði | Framleiðslueftirlit&gt; Uppsetning&gt; Auðlindir&gt; Auðlindir | WrkCtrTable |
| Tilfangaflokkar | Framleiðslueftirlit&gt; Uppsetning&gt; Auðlindir&gt; Auðlindahópar | WrkCtrResourceGroup |
| Framleiðsluflokkar | Framleiðslueftirlit&gt; Uppsetning&gt; Framleiðsla&gt; Framleiðsluhópur | ProdGroup |
| Kostnaðartegundir | Framleiðslueftirlit&gt; Uppsetning&gt; Leiðir&gt; Kostnaðarflokkar | ProjCategory |
| Verkflokkar | Verkefnastjórnun og bókhald&gt; Uppsetning&gt; Birting&gt; Verkefnahópar | ProjGroup |
| Uppsetning fjárhagsbókunar (Verkefni) | Verkefnastjórnun og bókhald&gt; Uppsetning&gt; Birting&gt; Uppsetning fjárhagsbókunar | ProjPosting |
| Sjálfgefnir mótlyklar fyrir kostnað | Verkefnastjórnun og bókhald&gt; Uppsetning&gt; Birting&gt; Sjálfgefin jöfnunarreikningur fyrir útgjöldum | ProjDefaultOffsetSetup |
| Bókunarreglur fyrir stjórnun eftirágreidds afsláttar | Stjórnun afsláttar&gt; Uppsetning afsláttarstjórnunar&gt; Afsláttarstjórnunarprófílar | TAMRebatePosting |
| Fjárhagsbókunarhópur (skattur) | Skattur&gt; Uppsetning&gt; Söluskattur&gt; Fjárhagsbókunarhópur | Tax Account Group |

## <a name="changing-groups-after-transactions-exist"></a>Að breyta hópum eftir að færslur eru til

Farðu varlega þegar þú skiptir um hópa í aðalgögnum. Ef þú ert að nota hópa til að skilgreina bókunarsniðin þín, geta allar breytingar á hópi á aðalfærslu haft neikvæð áhrif á getu til að samræma höfuðbók við undirbók. Til dæmis er hægt að stilla birgðabókunarsniðið fyrir sölupöntunartekjur þannig að annar tekjureikningur sé notaður fyrir hvern vöruflokk. Ef þú breytir vöruflokknum sem er úthlutað á vöru eftir að færslur eru til verða tekjur af nýjum færslum færðar inn á uppfærða reikninginn. Hins vegar verða allar tekjur sem voru bókaðar fyrir breytinguna áfram á upprunalega reikningnum.

## <a name="testing-posting-profiles"></a>Prófa póstsnið

Áður en þú byrjar í notkun, og eftir að þú gerir einhverjar breytingar eða viðbætur við póstsniðið þitt eða tengdar færibreytur, ættir þú að prófa hverja atburðarás. Að minnsta kosti ættir þú að prófa hverja færslutegund til að sannreyna að færslan virki rétt. Hins vegar er mælt með því að prófa hverja bókunarprófílfærslu og samsetningu.

Til dæmis, þú ert með tvö viðskiptamannsbókunarsnið, sem hvert um sig hefur þrjár færslur sem eru sértækar fyrir viðskiptavinahópa. Í þessu tilviki ættir þú að prófa hverja tegund viðskipta.

**Birta prófílar:**

- **GEN** – Almenna bókunarsniðið sem hefur einn hóp fyrir starfsmenn, einn fyrir viðskiptavini og einn fyrir millifyrirtæki. Hver hópur bendir á annan viðskiptareikning viðskiptakrafna.
- **PRE** – Fyrirframgreiðslubókunarsniðið sem hefur eina skrá fyrir allar fyrirframgreiðslur sem vísar á fyrirframgreiðslureikninga viðskiptavinarins.

### <a name="testing-scenarios"></a>Prófunarsviðsmyndir

- Ókeypis textareikningur fyrir viðskiptavin í **Starfsmaður** hópur sem notar **GEN** færsluprófíl
- Ókeypis textareikningur fyrir viðskiptavin í **Starfsmaður** hópur sem notar **PRE** færsluprófíl
- Sölupöntunarreikningur fyrir viðskiptavin í **Starfsmaður** hópur sem notar **GEN** færsluprófíl
- Sölupöntunarreikningur fyrir viðskiptavin í **Starfsmaður** hópur sem notar **PRE** færsluprófíl
- Greiðsludagbók viðskiptavinar fyrir viðskiptavin í **Starfsmaður** hópur sem notar **GEN** færsluprófíl
- Greiðsludagbók viðskiptavinar fyrir viðskiptavin í **Starfsmaður** hópur sem notar **PRE** færsluprófíl

Fyrir fyrra dæmi, endurtakið eina prófunaratburðarás fyrir hvern viðskiptavinahóp og endurtakið hvern hóp prófunarsviðsmynda fyrir hverja viðbótarfærslugerð (til dæmis verkreikninga og þjónustustjórnun).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Samræma höfuðbók við undirbók

Höfuðbók ætti að samræma við undirbók á hverju tímabili. Margar einingar innihalda útbúnar skýrslur sem hægt er að nota til að gera þessa afstemmingu. Hins vegar, allt eftir staðbundnum þörfum þínum, gætirðu þurft að þróa sérsniðnar skýrslur eða stækka núverandi skýrslur til að uppfylla skýrslukröfur þínar.

Við mælum með því að þú látir loka og samræma hverja undirbók þína við höfuðbókina áður en þú ferð í notkun. Við mælum líka með því að þú klippir út allar opnar inneignir og opnar færslur áður en þú byrjar í notkun. Sem hluti af þessu ferli ættir þú að keyra fullkomna afstemmingu til að tryggja að flutningur á stöðu og opnum færslum sé í jafnvægi við eldri kerfin og að allar undirbækur séu í jafnvægi við höfuðbókina áður en nýjar færslur eru stofnaðar.

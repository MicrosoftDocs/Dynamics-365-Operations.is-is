---
title: Ráðleggingar um notkun á bókunarreglum
description: Þessi grein lýsir ráðlögðum aðferðum við skilgreiningu bókunarreglna.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849903"
---
# <a name="recommended-practices-for-posting-profiles"></a>Ráðleggingar um notkun á bókunarreglum

Mælt er með nokkrum venjum sem ætti að fylgja þegar bókunarreglur eru grunnstilltar í gegnum kerfið. Þessi grein lýsir mismunandi aðstæðum og samsvarandi ráðlögðum starfsháttum.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Stilling flaggs fyrir banni við handvirkum innslætti

Á síðunni **Aðallyklar** ætti að velja gátreitinn **Ekki leyfa handvirkan innslátt** fyrir alla aðallykla sem notaðir eru fyrir bókunarreglu. Þessi stilling kemur í veg fyrir að notendur geti birt bókarfærslu handvirkt á aðallyklinum. Það auðveldar að ganga úr skugga um að undirbókin sé í samræmi við fjárhaginn og auðveldar afstemmingarferlið.

Ef gera þarf leiðréttingar á lykli sem kerfið stjórnar og er sjálfkrafa bókaður er hægt að nota eina af þessum nálgunum:

- Stofna aukaaðallykil þar sem hægt er að bóka leiðréttingarnar. Notaðu síðan samtölulykil eða sérstaka línu í fjárhagsskýrslum til að flokka og leggja saman lyklana.
- Bakfærðu upprunalegum færslum í viðeigandi undirbók, gerðu nauðsynlegar leiðréttingar og bókaðu svo aftur færslun í gegnum sömu undirbókina.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Breytingar á bókunarreglum eftir að færslur eru til

Ef bókunarreglu er breytt eftir að færslur verða til getur afstemmingin mistekist og mismunur orðið á undirbók og fjárhag. Almennt er mælt með því að breyta **ekki** bókunarreglu eftir að færslur eru til.

Ef gera þarf breytingar skal nota eftirfarandi leiðbeiningar til að tryggja heilleika kerfisins:

- Gerið breytingarnar við lokun tímabils.
- Gerið breytingarnar þegar engar aðrar færslur eiga sér stað í kerfinu.
- Staðfestið fjárhaginn og stemmið af við undirbókina áður og eftir að breytingarnar eru gerðar.
- Bókaðar færslur eru ekki uppfærðar ef bókunarreglunni er breytt. Íhugaðu vandlega hvort þörf sé á leiðréttingarfærslum fyrir breytinguna.
- Ef birgðabókunarreglum er breytt skal íhuga hvernig breytingarnar munu hafa áhrif lagerbirgðir og fjárhagsstöðu. Sumar breytingar gætu krafist þess að birgðir verði færðar niður í 0 (núll), loka birgðum og síðan færa birgðirnar aftur inn eftir að breytingarnar hafa verið gerðar.
- Prófaðu alltaf breytingar þínar í umhverfi sem ekki tengist framleiðslu áður en þú gerir þær í framleiðslu.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Notkun gagnagrunnsskráningar til að endurskoða breytingar á bókunarreglum

Íhugaðu að setja upp gagnagrunnsskráningu fyrir sérhverja bókunarreglu og færibreytutöflur sem stýra bókun. Ef færibreytu eða bókunarreglu er síðan breytt færðu ítarlega eftirlitsfærslu um hvaða gildi var breytt, hver breytti því, hvenær því var breytt og hvað gildið á undan var. Þessar upplýsingar geta verið mikilvægar í afstemmingarferlinu og endurskoðandinn gæti þurft tilheyrandi fylgigögn.

Frekari upplýsingar er að finna í [Skilgreina gagnagrunnsskráningu](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Notaðu eftirfarandi töflu sem tilvísun fyrir algeng töfluheiti sem tengjast bókunarreglum og tengdum bókunarfæribreytum.

| Síðuheiti | Slóð | Heiti töflu |
|-----------|-----------------|------------|
| Færibreytur viðskiptaskulda | Viðskiptaskuldir &gt; Uppsetning &gt; Færibreytur viðskiptaskulda | VendParm |
| Bókunarregla lánardrottna | Viðskiptaskuldir &gt; Uppsetning &gt; Bókunarregla lánardrottins | VendPosting |
| Gjaldakóði | Viðskiptaskuldir &gt; Uppsetning gjalda &gt; Gjaldakóði eða viðskiptakröfur &gt; Uppsetning gjalda &gt; Gjaldakóði | MarkupTable |
| Greiðsluhættir | Viðskiptaskuldir &gt; Greiðsluuppsetning &gt; Greiðslumátar | VendPaymMode |
| Staðgreiðsluafslættir | Viðskiptaskuldir &gt; Greiðsluuppsetning &gt; Staðgreiðsluafslættir eða viðskiptakröfur &gt; Greiðsluuppsetning &gt; Staðgreiðsluafslættir | CashDisc |
| Greiðsluþóknun (lánardrottinn) | Viðskiptaskuldir &gt; Greiðsluuppsetning &gt; Greiðsluþóknun | VendPaymFee |
| Færibreytur viðskiptakrafa | Viðskiptakröfur &gt; Uppsetning &gt; Færibreytur viðskiptakrafa | CustParm |
| Bókunarreglur viðskiptavina | Viðskiptakröfur &gt; Uppsetning &gt; Bókunarregla viðskiptavina | CustPosting |
| Greiðsluhættir | Viðskiptakröfur &gt; Greiðsluuppsetning &gt; Greiðslumáti | CustPaymMode |
| Greiðsluþóknun (viðskiptavinur) | Viðskiptakröfur &gt; Greiðsluuppsetning &gt; Greiðslumátar | CustPaymFee |
| Færibreytur fyrir útleigu eignar | Eignarleiga &gt; Uppsetning &gt; Færibreytur fyrir eignarleigu. | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Bankareikningar | Reiðufjár- og bankastjórnun &gt; Bankareikningar &gt; Bankareikningar | BankAccountsTable |
| Bankafærslugerðir | Reiðufjár- og bankastjórnun &gt; Uppsetning &gt; Bankafærslugerðir | BankTransType |
| Niðurfellingarreglur | Sameining &gt; Uppsetning &gt; Losunarregla | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Kostnaðartegundir | Útgjaldastýring &gt; Uppsetning &gt; Almenn &gt; Kostnaðartegundir | ProjCategories |
| Eignafæribreyta | Eignir &gt; Uppsetning &gt; Eignafæribreytur | AssetParameters |
| Bókunarreglur eigna | Eignir &gt; Uppsetning &gt; Bókunarreglur eigna | AssetLedgerAccounts<br>AssetDisposalParameters |
| Gjaldmiðilsendurmatslyklar | Fjárhagur &gt; Gjaldmiðlar &gt;Gjaldmiðilsendurmatslyklar | CurrencyLedgerGainLossAccount |
| Lyklar fyrir sjálfvirkar færslur | Fjárhagur &gt; Bókunaruppsetning &gt; Lyklar fyrir sjálfvirkar færslur | LedgerSystemAccounts |
| Samstæðulyklar | Fjárhagur &gt; Bókunaruppsetning &gt; Samstæðulyklar | LedgerIntercompany |
| Skilgreiningar færslubókana | Fjárhagur &gt; Bókunaruppsetning &gt; Skilgreiningar færslubókana | JournalizingDefinitionTrans |
| Bókunarskilgreiningar | Fjárhagur &gt; Bókunaruppsetning &gt; Bókunarskilgreiningar | JournalizingDefintion |
| Bókun (birgðir) | Birgðastjórnun&gt;Uppsetning&gt;Bókun&gt;Bókun | InventPosting |
| Kostnaðargerðakóðar | Heildarkostnaður &gt; Kostnaðaruppsetning &gt; Kostnaðargerðakóðar | ITMCostTypeTable |
| Forði | Framleiðslustýring &gt; Uppsetning &gt; Tilföng &gt; Tilföng | WrkCtrTable |
| Tilfangaflokkar | Framleiðslustýring &gt; Uppsetning &gt; Tilföng &gt; Tilfangaflokkar | WrkCtrResourceGroup |
| Framleiðsluflokkar | Framleiðslustýring &gt; Uppsetning &gt; Framleiðsla &gt; Framleiðsluflokkur | ProdGroup |
| Kostnaðartegundir | Framleiðslustýring &gt; Uppsetning &gt; Leiðir &gt; Kostnaðarflokkar | ProjCategory |
| Verkflokkar | Verkefnastjórnun og bókhald &gt; Uppsetning &gt; Bókun &gt; Verkflokkar | ProjGroup |
| Uppsetning fjárhagsbókunar (verkefni) | Verkefnastjórnun og bókhald &gt; Uppsetning &gt; Bókun &gt; Uppsetning fjárhagsbókunar | ProjPosting |
| Sjálfgefnir mótlyklar fyrir kostnað | Verkefnastjórnun og bókhald &gt; Uppsetning &gt; Bókun &gt; Sjálfgefnir mótlyklar fyrir kostnað | ProjDefaultOffsetSetup |
| Bókunarreglur fyrir stjórnun eftirágreidds afsláttar | Stjórnun eftirágreidds afsláttar &gt; Uppsetning bókunar fyrir stjórnun eftirágreidds afsláttar&gt; Bókunarreglur fyrir stjórnun eftirágreidds afsláttar | TAMRebatePosting |
| Fjárhagsbókunarflokkur (skattur) | Skattur &gt; Uppsetning &gt; Virðisaukaskattur &gt; Fjárhagsbókunarflokkur | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Hópum breytt eftir að færslur eru til

Sýnið aðgát þegar skipt er um hópa í aðalgögnum. Ef flokkar eru notaðir til að skilgreina bókunarreglur geta allar breytingar á flokki í aðalgögnum haft neikvæð áhrif á getuna til að afstemma fjárhag við undirbók. Til dæmis er hægt að grunnstilla birgðabókunarregluna fyrir tekjur sölupöntunar þannig að annar tekjulykill er notaður fyrir hvern vöruflokk. Ef vöruflokknum, sem úthlutað er á vöru eftir að færslur eru til, er breytt verða tekjur í nýjum færslum bókaðar í uppfærðan lykil. Allar tekjur sem voru bókaðar fyrir breytinguna verða þó áfram á upprunalega lyklinum.

## <a name="testing-posting-profiles"></a>Prófun bókunarreglna

Áður en keyrsla er framkvæmd og eftir að allar breytingar á eða viðbætur við bókunarreglurnar eða tengdar færibreytur eru gerðar ætti að prófa hverjar aðstæður. Að minnsta kosti ætti að prófa hverja bókunargerð til að staðfesta að hún bóki rétt. Hins vegar er mælt með því að prófa hverja bókunarreglufærslu og samsetningu.

Til dæmis ertu með tvær bókunarreglur viðskiptavinar, hvor þeirra er með þrjár færslur sem eiga við um viðskiptavinaflokka. Í þessu tilfelli ættir þú að prófa hverja tegund færslu.

**Bókunarreglur:**

- **ALM** – Almenna bókunarreglan er með einn flokk fyrir starfsmenn, einn fyrir viðskiptavini og einn fyrir samstæðufyrirtæki. Hver hópur vísar á annan viðskiptalykil viðskiptakrafna.
- **FYR** – Bókunarregla fyrirframgreiðslu sem er með eina færslur fyrir allar fyrirframgreiðslur sem beinast að fyrirframgreiðslulyklum viðskiptavinar.

### <a name="testing-scenarios"></a>Prófun aðstæðna

- Reikningur með frjálsum texta fyrir viðskiptavin í hópnum **Starfsmaður** sem notar bókunarregluna **GEN**
- Reikningur með frjálsum texta fyrir viðskiptavin í hópnum **Starfsmaður** sem notar bókunarregluna **PRE**
- Sölupöntunarreikningur fyrir viðskiptavin í hópnum **Starfsmaður** sem notar bókunarregluna **GEN**
- Sölupöntunarreikningur fyrir viðskiptavin í hópnum **Starfsmaður** sem notar bókunarregluna **PRE**
- Greiðslubók viðskiptavinar fyrir viðskiptavin í hópnum **Starfsmaður** notar bókunarregluna **GEN**
- Greiðslubók viðskiptavinar fyrir viðskiptavin í hópnum **Starfsmaður** notar bókunarregluna **PRE**

Fyrir framangreint dæmi skal endurtaka einar prófunaraðstæður fyrir hvern viðskiptavinaflokk og endurtaka hvern flokk af prófunaraðstæðum fyrir hverja viðbótarfærslugerð (til dæmis verkreikninga og þjónustustjórnun).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Afstemming fjárhags við undirbók

Fjárhagurinn ætti að vera afstemmdur við undirbókina á hverju tímabili. Margar einingar innihalda tilbúnar skýrslur sem hægt er að nota við þessa afstemmingu. En eftir því hvernig staðbundnar kröfur eru gætirðu hins vegar þurft að hanna sérsniðnar skýrslur eða stækka fyrirliggjandi skýrslur til að uppfylla skýrslukröfurnar þínar.

Mælum með að herma eftir lokun tímabils og afstemma sérhverja undirbók við fjárhaginn áður en keyrslan er framkvæmd. Einnig er mælt með því að framkvæma hermikeyrslu á öllum opnum stöðum og opnum færslum á undan fyrstu keyrslu. Sem hluti af þessu ferli ættir þú að keyra heila afstemmingu til að tryggja að flutningur innistæðna og staða opinna færslna stemmi við eldri kerfi og að stöður undirbókar stemmi við fjárhaginn áður en nýjar færslur eru stofnaðar.

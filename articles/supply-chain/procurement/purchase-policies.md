---
title: Yfirlit yfir innkaupareglur
description: Þessi grein gefur upplýsingar um innkaupareglur. Innkauparegla er safn reglna sem stýrir innkaupaferlinu. Innkaupareglur hjálpa innkaupastjórum að innleiða sína innkaupastefnu með því að stofna regluskipulag sem er stilltur saman við stjórnunaráætlun fyrirtækisins fyrir innkaup.
author: kamaybac
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage, PurchReqControlRule, RequisitionReplenishCatAccessPolicyRule, PurchReApprovalPolicyRule, RequisitionReplenishControlRule, PurchReqControlRFQRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11614
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2c69ab02ea9e6a5a5699a204258243d6204413b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825303"
---
# <a name="purchasing-policies-overview"></a>Yfirlit yfir innkaupareglur

[!include [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar um innkaupareglur. Innkauparegla er safn reglna sem stýrir innkaupaferlinu. Innkaupareglur hjálpa innkaupastjórum að innleiða sína innkaupastefnu með því að stofna regluskipulag sem er stilltur saman við stjórnunaráætlun fyrirtækisins fyrir innkaup.

Innkaupastefna samanstendur af safni stefnureglna. Þegar stefnuregla er skilgreind þarf fyrst að velja reglugerð. Síðan er reglan stofnuð fyrir reglugerðina með því að skilgreina stillingar, upphafsdagsetningu og lokadagsetningu fyrir regluna.  

Til dæmis stofnar kerfisstjóri reglu, velur **stefnureglu Vörulista** reglugerð og bætir stefnureglu vörulista við stefnuna. Stefnuregla vörulista tilgreinir að Adventure vörulista verður að nota til innri innkaupa. Eftir að innkaupastefna tengist tilteknu fyrirtæki, sjá starfsmenn fyrirtækis vörulista Adventure þegar þeir stofna innkaupabeiðni.

## <a name="assigning-policies-to-organizations"></a>Úthluta fyrirtækjum reglum
Áður en regla getur tekið gildi, verður að tengja hana við fyrirtæki. Innkaupareglur eru tengdar við **innri stýring Innkaupa** stigveldisáætlun. Því eiga innkaupareglur aðeins við fyrirtæki í stigveldi sem hafa stigveldisáætlun fyrir **innri stýringu Innkaupa**. Einnig er hægt að velja fyrirtæki úr flatur listi yfir lögaðila í töflu CompanyInfo. Þessar lögaðilar eru táknaðir innan reglurammans sem "Fyrirtæki."

## <a name="determining-which-rule-to-apply"></a>Ákvarða hvaða reglu á að nota
Eftir því hvernig innkaupareglur eru skilgreindar, geta margvíslegar reglur haft áhrif á notendur í fyrirtæki. Eftirfarandi dæmi sýna mismunandi leiðir til að skilgreina innkaupareglur og tilgreina hvernig reglum er beitt þegar færsla á sér stað.

### <a name="example-1-simple-purchasing-policy-configuration"></a>Dæmi 1: Einföld innkauparegluskilgreining

Fyrirtæki sem eru lítil og ekki flókin geta sett upp innkaupareglur eftir lögaðila og hægt er að nota aðeins Fyrirtækisskipulag stigveldi.  

Hjá Fabrikam, sem er lítið fyrirtæki, eru innkaupaþarfir svipaðar fyrir allt fyrirtækið. Innkaupareglur eru mismunandi aðeins milli lögaðila fyrirtækisins. Til dæmis starfsmenn í Kanada Fabrikam og starfsmenn Fabrikam í Bandaríkjunum kaupa vöru og þjónustu frá mismunandi vörulistum og mismunandi söluaðilum. Þess vegna setur Fabrikam upp innkaupareglur á stigi lögaðilans.  

Fabrikam stofnar tvær innkaupareglur. Regla A gildir um bandarískan lögaðila hennar, 1111. Regla B gildir um kanadískan lögaðila hennar, 2222. Þegar starfsmaður lögaðila 1111 stofnar innkaupabeiðni, eru stefnureglur afleiddar frá reglu A. Til dæmis vörulistinn sem starfsmaðurinn sér er tilgreind í stefnureglu um vörulista fyrir reglu A.  

Þegar starfsmaður lögaðila 2222 stofnar innkaupabeiðni, eru stefnureglur afleiddar frá reglu B.  

**Ábending:** Ef starfsmaður lögaðila 1111 kaupir vöru fyrir hönd starfsmanns lögaðila 2222, er beitt stefnureglum sem eru tilgreindar fyrir lögaðilann 2222 (sem eru stefnureglur úr reglu B).

### <a name="example-2-complex-purchasing-policy-configuration"></a>Dæmi 2: Flóknar innkaupareglustillingar

Í fyrri dæmi voru allar reglur um innkaup skilgreindar í einu stigveldi fyrirtækis, Fyrirtækisskipulag stigveldi. Hins vegar gæti flókið fyrirtæki skilgreint reglur fyrir mörg stigveldi fyrirtækja.  


Contoso er stórt fyrirtæki sem krefst flókinna innkaupareglna til að stjórna innkaupabeiðnaferlinu. Contoso hefur skilgreint reglur fyrir tvö mismunandi stigveldi fyrirtækisins: Deild og Altæk stýring innkaupa.  

Regla 123 er skilgreind fyrir stigveldi fyrirtækis Deild fyrir Bretlandssölu – söludeild. Í reglu 123 tilgreinir reglan fyrir stýringu innkaupabeiðna að það verður að beita takmörkuninni fyrir lágmarks magn. Í þessari reglu er **Beita takmörkunum á lágmarksmagni pöntunar** valkosturinn valinn.  

Regla 456 er skilgreind fyrir Altæka innkaupastýringu stigveldi fyrirtækis fyrir Sölu- og Markaðssetningardeild. Í reglu 456 tilgreinir reglan fyrir innkaupabeiðnastýringu ekki að það verðui að beita takmörkuninni fyrir lágmarks magn. Í þessari reglu er **Beita takmörkunum á lágmarksmagni pöntunar** valkosturinn afvalinn.  

Sam vinnur í Deild fyrir Bretlandssölu – söludeild í skrifstofu Contoso í Bretlandi. Reglur fyrir bæði Deild og Altæka innkaupastýringu stigveldi fyrirtækis eiga við um hans deild. Þegar Sam stofnar innkaupabeiðni, verður kerfið að ákvarða hvaða reglu á að nota. Kerfisstjórinn setur upp færibreytur fyrir innkaupareglu til að tilgreina að innkaupareglur verður að nota í eftirfarandi forgangsröð:

1.  Innkaup – Altæk
2.  Deild
3.  Fyrirtæki

Þess vegna er reglu 456 beitt á innkaupabeiðnna sem Sam stofnar og lágmarkspöntunarmagns er ekki krafist fyrir innkaupabeiðnina.

## <a name="policy-rules"></a>Stefnureglur
### <a name="catalog-policy-rule"></a>Stefnuregla vörulista

Stefnuregla vörulista ákvarðar hvaða innkaupavörulista notendur sjá þegar þeir stofna innkaupabeiðnir. Ef notanda hefur verið veitt heimild til að panta vörur fyrir hönd annars notanda, notar innkaupabeiðnin stefnureglu vörulista sem skilgreind er fyrir lögaðila umsækjanda og rekstrareiningu til að ákvarða hvaða vörulisti á að birta. Áður en hægt er að skilgreina stefnureglu vörulista þarf að stofna innkaupavörulista og síðan gefa hann út.

### <a name="category-access-policy-rule"></a>Stefnuregla tegundaraðgangs

Stefnuregla tegundaraðgangs ákvarðar hvaða tegundir notendur hafa aðgang að þegar þeir stofna innkaupabeiðnir. Ef engin regla er tilgreind er hægt að bæta öllum innkaupategundum við innkaupabeiðnina.

1.  Velja **Innifela aðalreglu** valmöguleika til að nota stefnureglu tegundaraðgangs móðurfyrirtækisins á tegundina.
2.  Í **Tiltækar tegundir** rúðunni skal velja tegundir sem reglan gildir fyrir. Þegar valin er tegund, er öllum tegundunum sem eru hærri í stigveldinu einnig bætt við **Valdar tegundir** listann.
3.  Velja **Innifela undirtegundir** valkostinn til að nota regluna fyrir allar undirtegundir völdu tegundarinnar.

### <a name="category-policy-rule"></a>Stefnuregla tegunda

Stefnuregla tegunda skilgreinir hvernig notendur geta valið lánardrottna fyrir hverja tegund. Hún skilgreinir einnig kröfur fyrir móttöku- og reikningsfærsluferla.

### <a name="re-approval-rule-for-purchase-orders"></a>Endursamþykktarregla fyrir innkaupapantanir

Endursamþykktarregla er valfrjáls regla sem skilgreinir skilyrði til að krefjast endursamþykktar þegar innkaupapöntun er breytt. Valdir reitir eru metnir í vinnuflæðinu fyrir innkaupapöntun þegar „krefst endursamþykktar á innkaupapöntun“ er sett upp í vinnuflæðinu.

> [!NOTE]
> Dreifing á fjárhagsupphæð verður alltaf endurstillt þegar samþykktri innkaupapöntun, þar sem breyting á stjórnun er virkjuð, er breytt. Því ætti að hafa í huga að eigi að koma í veg fyrir endursamþykkt innkaupapöntunar þegar tilteknum reitum er breytt má EKKI taka reitinn Dreifing á fjárhagsupphæð breytt með sem valinn reit til endursamþykktar. 

### <a name="purchase-requisition-rfq-rule"></a>Tilboðsbeiðnireglur innkaupabeiðni

Tilboðsbeiðnireglur innkaupabeiðni skilgreina skilyrði fyrir kröfu um tilboðsbeiðni fyrir línu innkaupabeiðni. Ef lína uppfyllir skilyrði, birtist "óformleg Tilboðsbeiðni" eða "formleg Tilboðsbeiðni" stimpill á línu innkaupabeiðninnar.

### <a name="purchase-requisition-control-rule"></a>Regla innkaupapantanastýringar

Regla fyrir innkaupapantanastýringar innkaup af gerðinni **Notkun** er valfrjáls regla. Þegar reglur af þessari gerð eru stofnaðar er hægt að stilla valkosti á mismunandi flipum:

-   Á **Verkflæðissending** flipanum er hægt að stilla svæðin sem þarf að færa inn í línu innkaupabeiðninnar til að hægt sé að senda innkaupabeiðnina til samþykkis þegar málefni beiðni er Neysla.
-   Á **Pöntunarmagn** flipa, er hægt að stilla svæðin sem þarf á innkaupabeiðninni undir ákveðnum skilyrðum. Einnig er hægt að framfylgja pöntunarmagni.
-   Á **Dagsetningar** flipa, er hægt að skilgreina hvort dagsetning reikningsskila er sú sama og umbeðin dagsetning.
-   Á **Aðsetur** flipa er hægt að tilgreina hvort notandinn hafi leyfi til að stofna nýtt aðsetur í kerfinu til að nota við innkaupabeiðnina.

### <a name="requisition-purpose-rule"></a>Málefnisregla beiðni

Málefnisregla beiðni er valfrjáls regla sem ákvarðar gerð málefnisbeiðna sem leyfð er fyrir tiltekna lögaðila. Nema annar tilgangur sé tilgreindur í reglunni hafa innkaupabeiðnir sjálfkrafa tilganginn **Neysla** þegar þær eru stofnaðar.

### <a name="replenishment-category-access-policy-rule"></a>Stefnuregla aðgangs fyrir áfyllingartegund

Áfyllingarflokkur fyrir aðgengi tegundareglna er valfrjáls regla sem ákvarðar vörur sem eru tiltækar til að uppfylla eftirspurn innkaupabeiðni fyrir tiltekna lögaðila þegar málefni beiðni er **Áfylling**.

### <a name="replenishment-control-rule"></a>Regla áfyllingarstýringar

Regla áfyllingarstýringar er valfrjáls regla sem skilgreinir svæðin sem þarf að færa inn í línu innkaupabeiðninnar til að hægt sé að senda innkaupabeiðni til samþykkis þegar málefni beiðni er **Áfylling**.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Samlegðarregla stofnunar innkaupapantana og eftirspurnar

Samlegðarregla stofnunar innkaupapantana og eftirspurnar skilgreinir stefnureglur sem nota á þegar innkaupapöntun er stofnuð úr samþykktri innkaupabeiðni. Þegar reglur af þessari gerð eru stofnaðar er hægt að stilla valkosti á mismunandi flipum:

-   Á **Innkaupapöntun skipta** flipa er hægt að skilgreina skilyrði fyrir skiptingu á innkaupabeiðnilínum í aðskildar innkaupapantanir.
-   Á **Flutningur Verðs/afsláttar** flipa er hægt að skilgreina hvenær skal endurreikna verðsamning þegar innkaupapöntun er stofnuð:
    -   **Aðeins ef engin verðsamningur er til staðar** – Verð og afslættir eru aðeins flutt úr innkaupabeiðni ef engir viðskiptasamningar eru til staðar eða grunnverð. Ef viðskiptasamningar eða grunnverð er tiltækt fyrir vöru eða lánardrottin eru verð og afslættir endurreiknuð á grundvelli viðskiptasamningsins eða grunnverðs og notuð í innkaupapöntuninni. Nema annað sé tilgreint er þetta er sjálfgefið atferli.
    -   **Alltaf** – Verð og afslættir eru alltaf flutt úr innkaupabeiðninni.

    Einnig er hægt að leyfa umsækjanda að breyta aðferðinni við flutning verðs og afsláttar fyrir einstakar innkaupabeiðnilínur óháð flutningsreglu verðs/afsláttar sem skilgreind er. Velja skal **Leyfa handvirka hnekkingu á hverja innkaupabeiðnilínu** valkostinn ef óskað er eftir að virkja þessa getu.
-   Á **Flutningur vörulýsingar** flipa er hægt að flytja vörulýsinguna úr innkaupabeiðni þegar hún er upprunnin úr Beiðni um tilboð.
-   Á flipann **Verðþol** er hægt að skilgreina reglur til að beina samþykktum innkaupabeiðnum aftur í gegnum endurskoðunarferlið þegar vöruverð í innkaupavörulista hækkar. Stillið hámarksupphæðina sem nettóupphæð í línuatriði í innkaupabeiðni getur hækkað um frá því að innkaupabeiðnin er samþykkt og þar til innkaupapöntun er stofnuð. Nettó upphæð er reiknuð með því að nota eftirfarandi formúlu: (\[Magn × (einingarverð – Afsláttur)÷ verðeining\] + ýmis Gjöld) × (100 - afsláttarprósenta) ÷ 100. Innkaupabeiðnilínur sem fara fram úr verðþoli er haldið eftir fyrir handvirka úrvinnslu. Reglurnar sem eru stilltar í flipanum **Villa við vinnslu** ákvarða hvernig innkaupabeiðnilínur eru unnar.
-   Á flipanum **Villa við vinnslu** oer hægt að stilla vinnsluregluna sem er beitt á innkaupabeiðni ef staðfesting mistekst við stofnun innkaupapöntunar vegna villu hjá lánardrottni eða villu í verðvikmörkum. Veldu einn af eftirfarandi valkostum:
    -   **Engin aðgerð** – innkaupabeiðnilínur haldast á **Losa samþykktar innkaupabeiðnir** síðu. Staða innkaupabeiðnilínanna er ennþá **Samþykkt**. Hins vegar verður að leysa úr villunum áður en hægt er að gera innkaupapöntun fyrir innkaupabeiðnilínurnar.
    -   **Hætta við innkaupabeiðnilínu**- Innkaupabeiðnilínurnar eru afturkallaðar. Umsækjandi hægt að stofnað nýja innkaupabeiðni fyrir línur sem hætt var við ef hann eða hún enn vill óska eftir línuatriðum.
    -   **Búa til nýja innkaupabeiðnilínu** - Innkaupabeiðnilínurnar eru afturkallaðar. Nýjar innkaupabeiðnir eru svo stofnaðar sem innihalda aðeins innkaupabeiðnilínur sem stóðust ekki villuleit. Þegar nýjar innkaupabeiðnir eru stofnaðar hafa þær stöðuna **Uppkast**. Þessar innkaupabeiðnir er hægt að endursenda til skoðunar eftir villur við villuleit hafa verið leiðréttar. Undirbúningsaðili fyrir innkaupabeiðnilínurnar er látinn vita þegar hætt var við línurnar og að nýjar innkaupabeiðnir hafi verið stofnaðar fyrir innkaupabeiðnilínurnar sem mistókust.
-   Á flipanum **Gera innkaupabeiðni handvirkt** er hægt að skilgreina færibreyturnar sem ákvarða hvort innkaupabeiðni verði að vera unnin handvirkt eða hvort hægt sé að breyta henni sjálfkrafa í innkaupapöntun. Færibreyturnar geta átt við um innri vörulistavörur, ytri vörulistavörur eða vörur sem ekki eru á vörulista. Veldu einn af eftirfarandi valkostum:
    -   **Stofna innkaupapantanir handvirkt** – Stofna innkaupapantanir handvirkt fyrir allar innkaupabeiðnir.
    -   **Stofna innkaupapantanir sjálfvirkt** – Stofna innkaupapantanir sjálfvirkt fyrir allar samþykktar innkaupabeiðnir. Engin innkaupapöntunum er haldið eftir fyrir handvirka stofnun innkaupapöntunar.
    -   **Stofna sjálfvirkt innkaupapantanir, nema við þessi skilyrði** – Stofna innkaupapantanir handvirkt fyrir innkaupabeiðnir sem samsvara skilyrðum sem eru skilgreind. Allar aðrar innkaupabeiðnir sem eru samþykktar er sjálfkrafa breytt í innkaupapantanir. Ef valið er **Stofna innkaupabeiðnir sjálfvirkt nema við eftirfarandi skilyrði** er hægt að bæta við innkaupategundum og lánardrottnum til að tilgreina hvaða samþykktum innkaupabeiðnalínum er haldið eftir fyrir handvirka úrvinnslu. Þessi valkostur getur átt við um innri vörulistavörur, ytri vörulistavörur og vörur sem ekki eru á vörulista. Þegar innkaupategund er valin eru allir undirflokkar fyrir þá innkaupategund einnig valdir. Veljið valkostinn **Allt** fyrir sérstakar gerðir innkaupabeiðnilínu til að halda öllum línum þeirrar línugerðar fyrir handvirka úrvinnslu.

    Ef stofna á innkaupapantanir sjálfkrafa úr samþykktum innkaupabeiðnum þegar runuvinnsla fyrir myndun innkaupapantana er keyrð skal velja valkostinn **Keyra sjálfvirka stofnun innkaupapantana sem runu**. Þessi stilling á aðeins við innkaupabeiðnir sem þarfnast ekki handvirkrar úrvinnslu. Með því að keyra sjálfvirka myndun innkaupapantana sem runuvinnslu er hægt að framkvæma þá aðgerð hvenær sem er þegar tilföngin eru ekki eins takörkuð. Ef valmöguleikinn **Fyrirframgreiðsla skilyrði** er valinn á innkaupabeiðnalínum , veljið valmöguleikann **Þegar innkaupabeiðni er sett upp fyrir fyrirframgreiðslu** til að halda samþykktum innkaupabeiðnilínum fyrir handvirka vinnslu. Innkaupabeiðnir sem eru settar í handvirka úrvinnslu er hægt að sía svo hægt sé að skoða aðeins þær innkaupabeiðnilínur sem krefjast fyrirframgreiðslu.
-   Á **Sameining eftirspurnar** flipanum er hægt að skilgreina færibreyturnar sem ákvarða hvort innkaupabeiðnir sem eru unnar handvirkt geti flokkast sem sameinaðar innkaupabeiðnir. Færibreyturnar geta átt við um innri vörulistavörur, ytri vörulistavörur eða vörur sem ekki eru á vörulista. Veldu einn af eftirfarandi valkostum:
    -   **Ekki heimila sameiningu eftirspurnar** – Engin samþykktar innkaupabeiðnalínur eru hæfar fyrir sameiningu eftirspurnar. Þessi kostur er valinn að sjálfgefnu og á aðeins á innkaupabeiðnilínur sem krefjast handvirkrar úrvinnslu fyrir stofnun innkaupapöntunar.
    -   **Alltaf heimila sameiningu eftirspurnar** – Allar samþykktar innkaupabeiðnalínur eru hæfar fyrir sameiningu eftirspurnar. **Ábending:** Ef valið er **Alltaf heimila sameiningu eftirspurnar** valkosturinn á **Sameining eftirspurnar** flipanum, en **stofna innkaupapantanir Sjálfvirkt** valkosturinn er valinn í flipanum **stofnun Handvirkra innkaupapantana** er öllum innkaupapöntunum haldið eftir fyrir handvirka úrvinnslu.
    -   **Heimila sameiningu eftirspurnar við þessi skilyrði** – Skilgreina þau skilyrði sem ákvarða hvort samþykktar innkaupabeiðnalínur eru hæfar fyrir sameiningu eftirspurnar. Fyrir hverja gerð innkaupabeiðnilínu er hægt að stilla skilyrðin eftir innkaupategund og lánardrottni. Ef valið er **Heimila sameiningu eftirspurnar við þessi skilyrði** er hægt að stilla skilyrðin eftir innkaupategund og lánardrottni fyrir hverja tegund innkaupabeiðnilínu. Þegar innkaupategund er valin eru allir undirflokkar fyrir þá innkaupategund einnig valdir. Ef valinn er valkosturinn **Allt** fyrir tiltekna línugerð eru allar innkaupabeiðnilínur þeirrar línugerðar hæfar fyrir sameiningu eftirspurnar.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
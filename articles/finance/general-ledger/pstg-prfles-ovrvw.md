---
title: Yfirlit yfir bókunarreglur
description: Þessi grein útskýrir hvernig póstprófílar eru notaðir í gegn Microsoft Dynamics 365 forrit.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91078352b6376ee99e7d9ce4546ed200cb80a25a
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135844"
---
# <a name="posting-profiles-overview"></a>Yfirlit yfir bókunarreglur

Í fjármála- og rekstraröppum er hugtakið *birta prófíla* er notað til að lýsa þeim stillingum sem stjórna því hvernig undirbókalyklum er breytt í aðallykla svo hægt sé að nota þá í færslum sem eru bókaðar í aðalbók. Til dæmis stjórna þeir því hvernig viðskiptamanni er breytt í aðalreikning viðskiptakrafna þegar reikningur er bókaður.

Sumar einingar og eiginleikar eru með síðu sem inniheldur orðin „póstprófíl“ í nafninu (til dæmis, **Færsluprófíl viðskiptavinar** eða **Birtingarsnið söluaðila**). Að auki hafa sumar einingar marga möguleika til að stilla fjárhagsbókunina fyrir færslur sem eru búnar til úr undirbókinni. Til dæmis, í **Framleiðslueftirlit** mát geturðu sett upp færsluna eftir framleiðsluhópi, tilföngum eða tilfangaflokki.

Athugaðu að fyrir margar tegundir af færslum er valkostur við bókunarsnið: bókunarskilgreiningar. Fyrir studd skjöl er hægt að nota bókunarskilgreiningar í stað bókunarsniða til að flokka aðallykla og fjárhagsvíddir fyrir bókhaldsfærslur. Ef þú ætlar að nota kvaðir eða forkvaðir þarf bókunarskilgreiningu til að skilgreina reikninga fyrir bókhaldsfærslurnar.

Áður en þú getur stillt færslusnið, færsluskilgreiningar eða **Reikningar fyrir sjálfvirkar færslur** síðu, verður þú að stilla reikningaskrána á **Fjárhagsbók** síðu í lögaðilanum sem þú vilt stilla.

## <a name="posting-types"></a>Birtingartegundir

Í fjármála- og rekstraröppum er bókunartegund notuð til að skilgreina almennan flokk fyrir debet eða kredit. Þessi flokkur er óháður aðalreikningi í fjárhag. Það eru bókunargerðir fyrir hverja debet eða kredit í fjárhag.

Eitt fylgiskjal getur verið með eina eða fleiri bókunargerðir. Til dæmis færsla sem er bókuð í gegnum almenna færslubók þar sem reikningur og mótreikningur er stilltur á **Fjárhagsbók** mun hafa birtingartegund af **Fjárhagsbók** fyrir bæði debet og kredit. Aftur á móti mun reikningur lánardrottins hafa margar bókunargerðir. Þessar bókunargerðir munu innihalda eina línu fyrir stöðu lánardrottins og viðbótarlínur fyrir mótfærslufærsluna, svo sem **Fjárhagsbók**.

Þú getur skoðað færslutegundina **Tegund færslu** sviði á **Almennt** flipi á **Viðskipti með skírteini** síðu.

> [!TIP]
> Þú getur notað **Persónustilling** tækjastiku til að bæta við **Tegund færslu** sviði við rist á **Yfirlit** flipann, eða til að færa hann. Þannig geturðu gert þennan reit auðveldari að nálgast eða skoða þegar þú skoðar fylgiskjöl.

## <a name="detail-settings-for-a-posting-profile"></a>Upplýsingar um stillingar fyrir færslusnið 

Þegar þú stillir póstsnið, **Reikningskóði** reitinn skilgreinir stig stillingarinnar. Eftirfarandi valkostir eru í boði: **Tafla**, **·**, og **Allt**. Samsvörunin hættir eftir fyrstu viðureignina og röðin er frá ákveðnasta stigi til minnsta stigi. Þó að **Reikningskóði** reiturinn gæti verið með aðeins öðru nafni í sumum tilfellum, hegðun og virkni reitsins eru þau sömu. Til dæmis inniheldur birgðabókunarsniðið an **Vörukóði** sviði og an **Reikningskóði** sviði. Báðir vellir hafa **Tafla**, **·**, og **Allt** gildi.

Ef **Aðalreikningur** reiturinn er skilinn eftir auður fyrir færslusnið og þú hefur ekki stillt aðalreikning á **Reikningar fyrir sjálfvirk viðskipti** síðu eða á sértækri einingu eða eiginleikasértækri síðu færðu villuboð þegar þú bókar færslu sem notar bókunargerðina. Venjulega verða skilaboðin: „Reikningurinn fyrir\[ Tegund færslu\] er ekki að finna."

### <a name="table-value"></a>Töflugildi

The **Tafla** gildi vísar til aðalfærslunnar sem er tengd við bókunarsniðið. Hver töfluskrá er sérstök fyrir eitt gildi. Þú tilgreinir það gildi í reitnum sem birtist á eftir **Reikningskóði** sviði. Venjulega er þessi reitur nefndur **Reikningur** eða **Reikningur/hópnúmer**. Nákvæmt nafn er mismunandi, eftir því hvaða síðu það birtist.

Til dæmis, ef þú ert að vinna með færslusnið viðskiptavinar, **Tafla** gildi táknar ákveðinn viðskiptavin. Þess vegna, ef þú velur **Tafla** í **Reikningskóði** reit, verður þú að velja viðskiptavinanúmerið í **Reikningur/hópnúmer** sviði.

The **Tafla** gildi táknar ákveðnustu gerð færslu. Kerfið notar alltaf þetta gildi, jafnvel þótt þú hafir stillt aðra færslu þar sem **Hópur** eða **Allt** gildi er valið. Þetta gildi hnekkir einnig öllum gildum sem þú bjóst til sem sjálfgefin gildi á **Reikningar fyrir sjálfvirkar færslur** síðu.

Við mælum ekki með því að þú notir **Tafla** gildi sem aðalaðferðin til að stjórna færslusniðunum þínum, vegna þess að gagnagæðavandamál geta komið upp ef sérstakt færslusnið er viðhaldið fyrir hverja aðalgagnafærslu. Það er líka erfitt að viðhalda og samræma sérstakt bókunarsnið fyrir hverja aðalgagnafærslu. Þess í stað ætti að nota þetta gildi til að stjórna undantekningum í færslusniðunum þínum.

### <a name="group-value"></a>Hópvirði

The **Hópur** gildi vísar til flokkunarfærslunnar sem er studd af aðalfærslunni sem tengist bókunarsniðinu. Hver hópskrá er sérstök fyrir eitt gildi. Þú tilgreinir það gildi í reitnum sem birtist á eftir **Reikningskóði** sviði. Venjulega er þessi reitur nefndur **Reikningur** eða **Reikningur/hópnúmer**. Nákvæmt nafn er mismunandi, eftir því hvaða síðu það birtist.

The **Hópur** gildi krefst þess að þú stillir fyrst hóp og tengir hann við eina eða fleiri færslur fyrir reikninginn. The **Hópur** gildi er minna sértækt en **Tafla** gildi en nákvæmari en **Allt** gildi. Ef engin skrá hefur verið stillt fyrir töflu reynir kerfið að finna færslu fyrir hópinn sem færslan tilheyrir.

Til dæmis, ef þú ert að vinna með færslusnið viðskiptavinar og þú velur **Hópur** í **Reikningskóði** reit, verður þú að velja viðskiptavinahóp í **Reikningur/hópnúmer** sviði. Þú verður að forskilgreina viðskiptavinahópana á **Viðskiptavinahópur** síðu og þú verður að tilgreina viðskiptavinahóp þegar þú stofnar viðskiptavin.

Ef þú verður að fylgjast með mörgum aðalreikningum fyrir tiltekna færslutegund mælum við með að þú notir **Hópur** gildi. Til dæmis, þú ert með þrjá aðalreikninga viðskiptakrafna: einn fyrir fasta viðskiptavini, einn fyrir starfsmenn og einn fyrir innbyrðis sölu. Í þessu tilviki mælum við með að þú stofnir þrjá viðskiptavinahópa til að skipta viðskiptavinunum upp. Venda síðan hvern viðskiptavinahóp á réttan aðalreikning í bókunarsniði viðskiptavina. Eftirfarandi tafla sýnir viðskiptamannahópana þrjá fyrir þetta dæmi.

| Flokkur viðskiptavinar | Nafn | Lýsing |
|----------------|------|-------------|
| EXT | Ytri viðskiptavinur | Þessi hópur er notaður fyrir alla staðlaða viðskiptavini sem snúa út á við. |
| EMP | Starfsmenn | Þessi hópur er notaður fyrir alla starfsmenn sem gera innkaup frá fyrirtækinu þínu. |
| INT | Sala á milli fyrirtækja | Þessi hópur er notaður fyrir alla samstæðuviðskiptareikninga sem eru notaðir við samþættingu sölu- og innkaupapantana. |

Í færslusniðinu seturðu síðan upp þrjár línur. Í hverri línu velurðu **Hópur** verðmæti og tengdum aðalreikningi.

### <a name="all-value"></a>Öll verðmæti

The **Allt** gildi gefur til kynna að stillingarnar eigi við um allar færslur. Ef þú velur **Allt** gildi í **Reikningskóði** sviði, the **Reikningur/hópnúmer** reiturinn er ekki tiltækur og þú getur ekki valið tiltekna skrá til að beita stillingunum á.

The **Allt** gildi er minnsta sértæka gildið. Það er aðeins notað ef kerfið getur ekki fundið samsvörun fyrir **Tafla** eða **Hópur** gildi. Þú ættir að velja **Allt** gildi þegar þú hefur aðeins einn aðalreikning fyrir ákveðna færslutegund.

Til dæmis, þegar þú ert að vinna með bókunarprófíl viðskiptavina, gilda aðalreikningarnir sem þú tilgreinir fyrir alla aðra viðskiptavini og viðskiptavinahópa sem hafa ekki skrá fyrir tiltekna töflu (viðskiptavin) eða hóp (viðskiptavinahóp).

### <a name="category"></a>Flokkur

Birgðabókunarsnið hafa viðbótargildi sem er sértækt fyrir söluflokkinn eða innkaupaflokkinn. Þetta gildi líkist **Tafla** verðmæti, að því leyti að það á aðeins við tiltekinn sölu- eða innkaupaflokk.

### <a name="default-value"></a>Sjálfgildi

Ef þú býrð ekki til færslu fyrir færslutegund í færslusniði þar sem **Reikningskóði** reiturinn er stilltur á **Allt**, og kerfið getur ekki fundið samsvarandi færsluprófíl fyrir **Hópur** eða **Tafla** gildi, fer kerfið aftur í sjálfgefið gildi sem hægt er að tilgreina á **Reikningar fyrir sjálfvirk viðskipti** síðu. Fyrir frekari upplýsingar, sjá [Reikningar fyrir sjálfvirkar færslur](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Hreinsun reikninga

Hugtakið *hreinsunarreikning* er oft notað í bókhaldi. Sumar birtingartegundir inn Microsoft Dynamics 365 öpp eru að hreinsa reikninga. Með öðrum orðum, staðan á reikningnum er hreinsuð út eða bakfærð þegar önnur færsla er bókuð. Til dæmis, þegar þú bókar vörukvittun innkaupapöntunar, er summan af áætluðum kostnaði vörunnar, auk skatta og allra gjalda á innkaupapöntunarlínunum, bókuð á bókunargerð innkaupauppsöfnunar sem skuld. Síðar, þegar innkaupapöntunin er reikningsfærð, er staðan bakfærð frá bókunargerð innkaupauppsöfnunar og færð á viðskiptareikninginn Viðskiptaskuldir.

## <a name="additional-resources"></a>Frekari upplýsingar

Margar einingar í Dynamics 365 Finance,Dynamics 365 Supply Chain Management,Dynamics 365 Commerce, og Dynamics 365 Project Operations hafa bókunarsnið eða viðbótarstillingar sem stjórna því hvernig bókun í aðalbók virkar. Notaðu eftirfarandi efnisatriði til að læra meira um póstsniðin og póstuppsetningarnar í hverri einingu:

- [Lyklar fyrir sjálfvirkar færslur](accounts-for-auto-transactions.md)
- [Bókun lánardrottnalykils](accts-payble-posting.md)
- [Bókun reikningsskila](accts-recvble-posting.md)
- [Færsla eignarleigu](../asset-leasing/set-up-lease-posting-accts.md)
- Birting eignastýringar (kemur bráðum)
- Reiðufé og bankastjórnun (kemur bráðum)
- Gjaldeyrisendurmatsbókunarreikningar (kemur bráðum)
- Færsla um kostnaðarstjórnun (kemur bráðum)
- [Bókunarregla eigna](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Bókhald milli fyrirtækja (kemur bráðum)
- [Birgðabókun](inventory-posting.md)
- [Landað kostnaðarbókun](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Yfirlit yfir færsluskilgreiningar](posting-definitions.md)
- [Framleiðslubókun](production-posting.md)
- Verkefnastjórnun og bókhaldsfærsla (kemur bráðum)
- Birting þjónustustjórnunar (kemur bráðum)
- Skattskráning (kemur bráðum)
- Tíma- og mætingartilkynning (kemur bráðum)
- Færsla um flutningastjórnun (kemur bráðum)
- Birtingarprófílar afsláttarstjórnunar (kemur bráðum)


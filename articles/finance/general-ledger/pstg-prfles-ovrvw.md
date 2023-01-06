---
title: Yfirlit yfir bókunarreglur
description: Þessi grein útskýrir hvernig bókunarreglur eru notaðar í öllum Microsoft Dynamics 365-forritum.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135844"
---
# <a name="posting-profiles-overview"></a>Yfirlit yfir bókunarreglur

Í fjármála- og rekstrarforritum er hugtakið *bókunarreglur* notað til að lýsa grunnstillingum sem stýra því hvernig lyklum undirbókar er breytt í aðallykla þannig að hægt sé að nota þá í færslum sem bókaðar eru í fjárhaginn. Til dæmis stýra þeir því hvernig viðskiptavini er breytt í aðallykil viðskiptakrafna þegar reikningur er bókaður.

Sumar einingar og eiginleikar eru með síðu sem inniheldur orðin „bókunarregla“ í heitinu (til dæmis **Bókunarregla viðskiptavina** eða **Bókunarregla lánardrottins**). Auk þess eru sumar einingar með marga valkosti til að grunnstilla fjárhagsbókun fyrir færslur sem eru búnar til úr undirbókinni. Í einingunni **Framleiðslustýring** er til dæmis hægt að setja upp bókun eftir framleiðsluflokki, tilfangi eða tilfangaflokki.

Athugaðu að fyrir margar gerðir af færslum er til önnur leið ein bókunarreglur: bókunarskilgreiningar. Fyrir studd skjöl er hægt að nota bókunarskilgreiningar í stað bókunarreglna til að flokka aðallykla og fjárhagsvíddir í bókhaldsfærslur. Ef ætlunin er að nota fjárúthlutanir eða áætlaðar fjárúthlutanir er bókunarskilgreining nauðsynleg til að skilgreina lyklana fyrir bókhaldsfærslurnar.

Áður en hægt er að grunnstilla bókunarreglurnar, bókunarskilgreiningarnar eða síðuna **Lyklar fyrir sjálfvirkar færslur** þarf að grunnstilla bókhaldslykilinn á síðunni **Fjárhagur** í lögaðilanum sem á að grunnstilla.

## <a name="posting-types"></a>Bókunargerðir

Í fjármála- og rekstrarforritum er bókunargerð notuð til að skilgreina almennan flokk fyrir debet og kredit. Þessi flokkur er óháður aðallykli í fjárhag. Bókunargerðir eru til fyrir allar debet- eða kreditfærslur í fjárhagi.

Hægt er að nota eitt fylgiskjal fyrir eina eða fleiri bókunargerðir. Færsla sem er bókuð í gegnum almenna færslubók þar sem lykillinn og mótlykillinn eru stilltir á **Fjárhagur** verður til dæmis með bókunargerðina **Færslubók fjárhags** fyrir bæði debet og kredit. Á móti verður reikningur lánardrottins með mörgum bókunargerðum. Þessar bókunargerðir munu innihalda eina línu fyrir stöðu lánardrottins og viðbótarlínur fyrir mótfærsluna, t.d. **Færslubók fjárhags**.

Hægt er að skoða bókunargerðina í reitnum **Bókunargerð** í flipanum **Almennt** á síðunni **Fylgiskjalafærslur**.

> [!TIP]
> Hægt er að nota tækjastikuna **Sérstillingar** til að bæta reitnum **Bókunargerð** við hnitanetið í flipanum **Yfirlit** eða til að færa hann. Á þennan hátt er auðveldara að nálgast eða skoða þennan reit þegar þú skoðar fylgiskjöl.

## <a name="detail-settings-for-a-posting-profile"></a>Nákvæmar stillingar fyrir bókunarreglu 

Þegar þú skilgreinir bókunarreglur skilgreinir reiturinn **Kóði lykils** stig stillingarinnar. Eftirtaldir valkostir eru í boði: **Tafla**, **Flokkur** og **Allt**. Samsvörunin stöðvast eftir fyrstu samsvörun og röðin er frá sértækasta stiginu til þess almennasta. Þótt reiturinn **Lykilkóði** gæti verið með örlítið annað heiti í sumum tilfellum er hegðun og virkni reitsins sú sama. Til dæmis inniheldur birgðabókunarreglan reitinn **Vörukóði** og reitinn **Lykilkóði**. Báðir reitirnir hafa gildi **Tafla**, **Hópur** og **Allt**.

Ef reiturinn **Aðallykill** er skilinn eftir auður fyrir bókunarreglu og ekki er búið að grunnstilla aðallykil á síðunni **Lyklar fyrir sjálfvirka færslu** eða á síðu tiltekinnar einingar eða eiginleika koma upp villuboð þegar færsla sem notar bókunargerðina er bókuð. Skilaboðin verða yfirleitt: „Reikningurinn fyrir \[Bókunargerð\] finnst ekki.“

### <a name="table-value"></a>Töflugildi

Gildi **Tafla** vísar til aðalskráningarinnar sem tengist bókunarreglunni. Hver töflufærsla gildir fyrir eitt gildi. Þú tilgreinir gildið í reitnum sem birtist á eftir reitnum **Kóði lykils**. Venjulega er þessi reitur nefndur **Lykill** eða **Númer lykils/flokks**. Nákvæmt heiti er breytilegt eftir því hvar á síðunni það birtist.

Ef þú vinnur til dæmis með bókunarreglu viðskiptavinar stendur gildið **Tafla** fyrir tiltekinn viðskiptavin. Ef valið er **Tafla** í reitnum **Lykilkóði** þarf af þeim sökum að velja númer viðskiptavinar í reitnum **Númer lykils/flokks**.

Gildið í **Tafla** sýnir sértækustu tegund færslu. Kerfið notar alltaf þetta gildi, jafnvel þótt þú hafir grunnstillt aðra færslu þar sem gildið **Flokkur** eða **Allt** er valið. Þetta gildi hnekkir líka öllum gildum sem voru búin til sem sjálfgefin gildi á síðunni **Lyklar fyrir sjálfvirkar færslur**.

Ekki er mælt með að nota gildið **Tafla** sem helstu leiðina til að stjórna bókunarreglum þínum því að vandamál varðandi gagnagæði geta komið upp ef aðskildri bókunarreglu er viðhaldið fyrir hverja færslu aðalgagna. Einnig er erfitt að vinna með og afstemma aðskilda bókunarreglu fyrir hverja færslu aðalgagna. Þess í stað ætti að nota þetta gildi til að stjórna undantekningum í bókunarreglunum.

### <a name="group-value"></a>Hópgildi

Gildið **Flokkur** vísar í flokkunarfærsluna sem er studd af aðalfærslunni sem tengist þessar bókunarreglu. Hver hópfærsla gildir fyrir eitt gildi. Þú tilgreinir gildið í reitnum sem birtist á eftir reitnum **Kóði lykils**. Venjulega er þessi reitur nefndur **Lykill** eða **Númer lykils/flokks**. Nákvæmt heiti er breytilegt eftir því hvar á síðunni það birtist.

Gildið **Flokkur** krefst þess að þú grunnstillir flokk og tengir hann við eina eða fleiri færslur fyrir lykilinn. Gildið **Hópur** er minna sértækt en gildið **Tafla** en sértækara en gildið **Allt**. Ef engin færsla hefur verið grunnstillt fyrir töflu reynir kerfið að finna færslu fyrir flokkinn sem færslan tilheyrir.

Ef þú ert til dæmis að vinna með bókunarreglu viðskiptavinar og þú velur **Flokkur** í reitnum **Lykilkóði** þarftu að velja viðskiptavinaflokk í reitnum **Númer lykils/flokks**. Skilgreina þarf viðskiptavinaflokk fyrirfram á síðunni **Viðskiptavinaflokkur** og tilgreina þarf viðskiptavinaflokk þegar viðskiptavinur er stofnaður.

Ef rekja þarf marga aðallykla fyrir ákveðna bókunargerð er mælt með að nota gildið **Flokkur**. Þú ert til dæmis með þrjá aðallykla viðskiptakrafna: einn fyrri venjulega viðskiptavini, einn fyrir starfsmenn og einn fyrir samstæðusölu. Í þessu tilfelli mælum við með því að þú búir til þrjá viðskiptavinaflokka til að flokka viðskiptavinunum. Varpið því næst hverjum viðskiptavinaflokki á réttan aðallykil í bókunarreglu viðskiptavinarins. Eftirfarandi tafla sýnir þrjá viðskiptavinaflokka fyrir þetta dæmi.

| Flokkur viðskiptavinar | Nafn | Lýsing |
|----------------|------|-------------|
| EXT | Ytri viðskiptavinur | Þessi hópur er notaður fyrir alla hefðbundna utanaðkomandi viðskiptavini. |
| STARFSM | Starfsmenn | Þessi hópur er notaður fyrir allt starfsfólk sem gerir innkaup hjá stofnuninni/fyrirtækinu. |
| INT | Samstæðusala | Þessi flokkur er notaður fyrir allar lykla samstæðuviðskiptavina sem notaðir eru með samþættingu sölu- og innkaupapantana. |

Í bókunarreglunni setur þú síðan upp þrjár línur. Í hverri línu er gildið **Hópur** og tengdur aðallykill valin.

### <a name="all-value"></a>Öll gildi

Gildið **Allt** gefur til kynna að stillingarnar eigi við um allar færslur. Ef gildið **Allt** er valið í reitnum **Lykilkóði** er reiturinn **Númer lykils/flokks** ekki tiltækur og ekki er hægt að velja tiltekna færslu til að nota grunnstillinguna á.

Gildið **Allt** er almennasta gildið. Það er aðeins notað ef kerfið finnur ekki samsvörun við gildi **Tafla** eða **Hópur**. Það ætti að velja gildið **Allt** þegar aðeins einn aðallykill er til staðar fyrir tiltekna bókunargerð.

Þegar til dæmis unnið er með bókunarreglu viðskiptavinar eiga aðallyklarnir sem tilgreindir eru við alla aðra viðskiptavini og viðskiptavinaflokka sem eru ekki með færslu fyrir tiltekna töflu (viðskiptavin) eða flokk (viðskiptavinaflokk).

### <a name="category"></a>Flokkur

Birgðabókunarreglur eru með aukalegt gildi sem á sérstaklega við söluflokkinn eða innkaupategundina. Þetta gildi líkist gildinu **Tafla** á þann veg að það á aðeins við um tiltekinn sölu- eða innkaupaflokk.

### <a name="default-value"></a>Sjálfgildi

Ef færsla fyrir bókunargerð í bókunarreglu er ekki stofnuð þar sem reiturinn **Lykilkóði** er stilltur á **Allt** og kerfið finnur ekki samsvarandi færslu bókunarreglu fyrir gildið **Flokkur** eða **Tafla** fer kerfið aftur í sjálfgefna gildið sem hægt er að tilgreina á síðunni **Lyklar fyrir sjálfvirka færslu**. Frekari upplýsingar fást í [Lyklar fyrir sjálfvirkar færslur](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Millireikningar

Hugtakið *millireikningur* er oft notað í bókhaldi. Sumar bókunargerðir í Microsoft Dynamics 365-forritum eru millireikningar. Með öðrum orðum er staðan á lyklinum hreinsuð út eða bakfærð þegar önnur færsla er stofnuð. Til dæmis þegar þú bókar innhreyfingarskjal afurðar vegna innkaupapöntunar er summa áætlaðs kostnaðar á afurðum ásamt sköttum og öllum gjöldum í innkaupapöntunarlínunum bókuð á bókunargerð uppsafnaðra innkaupa sem skuld. Seinna þegar innkaupapöntunin er reikningsfærð er staðan bakfærð úr bókunargerð uppsafnaðra innkaupa og færð yfir í viðskiptalykil viðskiptaskulda.

## <a name="additional-resources"></a>Frekari upplýsingar

Margar einingar í Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Project Operations eru með bókunarreglu eða frekari grunnstillingar sem stýra því hvernig bókun á fjárhag virkar. Notaðu eftirfarandi efnisatriði til að fá frekari upplýsingar um bókunarreglur og bókunaruppsetningar í hverri einingu:

- [Lyklar fyrir sjálfvirkar færslur](accounts-for-auto-transactions.md)
- [Bókun lánardrottnalykils](accts-payble-posting.md)
- [Bókun á viðskiptakröfum](accts-recvble-posting.md)
- [Færsla eignarleigu](../asset-leasing/set-up-lease-posting-accts.md)
- Eignastýringarbókum (væntanlegt)
- Reiðufjár- og bankastjórnun (væntanlegt)
- Bókunarlyklar gjaldmiðilsendurmats (væntanlegt)
- Útgjaldastýringarbókun (væntanlegt)
- [Bókunarregla eigna](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Bókun samstæðulykla (væntanlegt)
- [Birgðabókun](inventory-posting.md)
- [Bókun heildarkostnaðar](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Yfirlit bókunarskilgreininga](posting-definitions.md)
- [Framleiðslubókun](production-posting.md)
- Verkefnastjórnun og bókhald (væntanlegt fljótlega)
- Þjónustustjórnunarbókun (væntanlegt)
- Skattbókun (væntanlegt)
- Tíma- og mætingarbókun (væntanlegt)
- Flutningsstjórnunarbókun (væntanlegt)
- Bókunarreglur fyrir stjórnun eftirágreidds afsláttar (væntanlegt)


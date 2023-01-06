---
title: Bókun innkaupapöntunar
description: Þessi grein lýsir innkaupapöntunarflipa Birgðabókunarreglusíðunnar.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 38a9e2740232b18255109ba867fcdddd5b890774
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151033"
---
# <a name="purchase-order-posting"></a>Bókun innkaupapöntunar

Flipinn **Innkaupapöntun** á síðunni **Birgðabókunarreglur** er notaður til að stjórna því hvernig innkaupapantanir verða bókaðar í fjárhaginn. Tvær meginaðgerðir bóka í fjárhag fyrir innkaupapöntun: 

- Innhreyfingarskjal afurða
- Reikningur

Til að efnisleg færsla (innhreyfingarskjal afurðar) sé bókað í fjárhaginn í innkaupapöntun þarf að velja eftirfarandi gátreiti:

- Gátreiturinn **Bóka innhreyfingarskjal afurða í fjárhag** á síðunni **Færibreytur birgða- og vöruhúsakerfis**.
- Gátreitina **Bóka efnislegar birgðir** og **Safna upp skuld á innhreyfingarskjali afurða** á síðunni **Vörulíkanaflokkar**.

Tilgreina þarf aðallyklana á síðunni **Birgðabókunarregla** fyrir eftirfarandi bókunargerðir:

- Kostnaður vegna keypts efnis sem er móttekið
- Útgjöld innkaupa, óreikningsfærð
- Innkaup, uppsöfnun

Til að fjárhagsfærsla (reikningur) sé bókuð í fjárhaginn í innkaupapöntun þarf að uppfylla eftirfarandi skilyrði:

- Velja þarf gátreitinn **Bóka fjárhagslegar birgðir** á síðunni **Vörulíkanaflokkar** fyrir vöruna sem valin er í innkaupapöntunarlínunni.
- Tilgreina þarf aðallyklana á síðunni **Birgðabókunarregla** fyrir eftirfarandi bókunargerðir:
  - Kostnaður vegna keypts reikningsfærðs efnis
  - Innkaupaútgjöld afurðar
  - Innkaupaútgjöld kostnaðar
  - Afsláttur (valkvæmt)

## <a name="fixed-receipt-price-posting"></a>Bókun á föstu verði innhreyfingar

Hægt er að nota fast verð innhreyfingar sem staðalkostnað fyrir afurð sem leið til að velja valkostinn **Staðalkostnaður** í reitnum **Birgðalíkan** á síðunni **Vörulíkanaflokkar** fyrir vöru. Helsti munurinn er sá að þegar **Fast verð innhreyfingar** er notað verður núverandi kostnaðarverð notað fyrir vöruna þegar innhreyfing birgða er bókuð. Ekkert endurmatsferli kostnaðar er til fyrir **Fast verð innhreyfingar**; þegar fjárhagsuppfærsla er bókuð er núverandi kostnaðarverð notað við bókun. Ef munur er á kostnaðarverði sem notað er við innhreyfingu og reikning mun frávikið vera bókað á rekstrarreikning innhreyfingarverðs.

Til að nota fast kostnaðarverð fyrir vöru þarf að skilgreina eftirfarandi:

- Á síðunni **Vörulíkanaflokkar** skal velja gátreitina **Bóka efnislegar birgðir** og **Fast innhreyfingarverð**. 
- Á síðunni **Færibreytur birgða- og vöruhúsakerfis** skal velja gátreitinn **Bóka fylgiseðil í fjárhag**.
- Á síðunni **Birgðabókunarregla** skal tilgreina aðallykla fyrir eftirfarandi bókunargerðir:
  - Hagnaður á föstu verði innhreyfingar
  - Tap á föstu verði innhreyfingar
  - Mótbókun fasts innhreyfingarverðs

Frekari upplýsingar er að finna á [Fast kostnaðarverð](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="purchase-charges-and-stock-variation-posting"></a>Bókun innkaupagjalda og birgðaafbrigða

Ef þú hyggst reikna með kaupgjöldum og lagerbreytingum skaltu gera eftirfarandi:

- Á síðunni **Færibreytur viðskiptaskulda** í flipanum **Reikningur** skal velja gátreitinn **Bóka á gjaldalykil í fjárhag**.
- Á síðunni **Vörulíkanaflokkar** fyrir valda vöru í innkaupapöntunarlínunni skal velja gátreitina **Bóka efnislegar birgðir**, **Bóka fjárhagslegar birgðir** og **Safna upp skuld á innhreyfingarskjali afurða**.
- Á síðunni **Færibreytur innkaupa og aðfanga** skal velja gátreitinn **Mynda gjöld á innhreyfingarskjali afurða**.
- Á síðunni **Færibreytur birgða- og vöruhúsakerfis** skal velja gátreitinn **Bóka fylgiseðil í fjárhag**.

Á síðunni **Birgðabókunarregla** þarf að tilgreina aðallyklana fyrir eftirfarandi bókunargerðir:

- Útgjöld innkaupa, óreikningsfærð
- Innkaupaútgjöld afurðar
- Birgðaafbrigði

> [!NOTE]
> Bókunargerðin **Gjald** er ekki notað þegar færibreytan **Bóka á gjaldalykil í fjárhag** er valin.

Frekari upplýsingar er að finna í [Reikningsskilaregla bókunar á gjaldalykil](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Skilgreining prófunarbókunarreglu

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðallyklum og lýsingum:

- Dálkurinn **Millireikningur** gefur til kynna að bókunargerðin sé millireikningur. Upphæðin sem er birt á þessum reikningi er sjálfkrafa afturkölluð þegar seinni færsla er bókuð. 
- Dálkurinn **P/F** gefur til kynna **P** fyrir efnislega bókun og **F** fyrir fjárhagslega bókun. 
- Dálkurinn **Fylgja** tilgreinir hvort aðallykill fyrri tiltekna bókunargerð er yfirleitt sá sami og önnur bókunargerð. Gildið í dálkinum gefur til kynna tegund færslu sem er yfirleitt notuð.

> [!NOTE]
> Aðallyklar og aðallyklaheiti eru aðeins tillögur. Við mælum með<!--note from editor: Via Writing Style Guide.--> að þú vinnur með endurskoðanda þínum til að finna út bestu stillingarnar fyrir viðskiptaþarfir þínar.


| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Kostnaður vegna keypts efnis sem er móttekið | 140100</br>140101 | Efnisbirgðir</br>Efni afhent, óreikningsfært | Eign | Debet | Já | P | Kostnaður vegna keypts reikningsfærðs efnis | Notað þegar afurðarinnhreyfing innkaupapöntunar er bókuð, mótlykill lykilsins er „Útgjöld innkaupa, óreikningsfærð“. Upphæðin í þessum lykli er bakfærð þegar reikningur fyrir innkaupapöntun er bókaður. |
| Útgjöld innkaupa, óreikningsfærð | 600180 | Efnisinnhreyfingar | Kostnaður | Debet | Já | P | |Notað þegar afurðarinnhreyfing innkaupapöntunar er bókuð. Tvö fylgiskjöl eru búin til fyrir innhreyfinguna til að rekja frávik innkaupaverðs þegar staðlaður kostnaður er notaður. Mótfærslan á lykilinn á fyrsta fylgiskjalinu er „Uppsöfnuð innkaup“. Jöfnunin á seinna fylgiskjalinu er summan af kostnaði keypts móttekins efnis og frávikslyklum innkaupaverðs. Upphæðirnar sem bókaðar eru í þessum lykli er bakfærðar þegar reikningur fyrir innkaupapöntun er bókaður. |
| Kostnaður vegna keypts reikningsfærðs efnis | 140100 | Efnisbirgðir | Eign | Debet | Nr. | F  |Kostnaður vegna keypts efnis sem er móttekið | Notað þegar reikningur fyrir innkaupapöntun er bókaður. Mótlykill við þennan lykil er „Útgjöld innkaupa fyrir vöru“. Þessi lykill táknar birgðir í efnahagsreikningnum þínum. Lykillinn sem er notaður er yfirleitt sami lykillinn og er notaður fyrir kostnaður afhentra eininga og kostnaður reikningsfærðra eininga fyrir sölupöntun. |
| Innkaupaútgjöld afurðar | 600180 | Efnisinnhreyfing | Kostnaður | Kredit | Já | F  | |Notað þegar reikningur fyrir innkaupapöntun er bókaður. Tvö fylgiskjöl eru búin til fyrir reikninginn til að rekja frávik innkaupaverðs þegar staðalkostnaður er notaður. Mótlykill við þennan lykil er lykillinn „Útgjöld innkaupa, óreikningsfærð“, sem er notaður í bókun innhreyfingar og bakfærður við bókun reiknings. Stendur fyrir kostnað fyrir birgðir sem keyptar eru við reikningsfærslu sem kemur ekki fram á birgðalykli á efnahagsreikningnum. Þetta er bókun hagnaðar og taps fyrir frávik innkaupaverðs sem oftast sést í vöruinnkaupum á staðalkostnaði.|
| Hagnaður fasts innhreyfingarverðs (Innkaup, hagnaður fasts innhreyfingarverðs*) | 510310 | Frávik innkaupaverðs | Kostnaður | Kredit | Nr. | F | Tap á föstu verði innhreyfingar | Notað þegar reikningur innkaupapöntunar er bókaður og munur er á milli reikningsfærðs verðs og sjálfgefins kostnaðar fyrir vöruna. Þessi lykill er notaður þegar munurinn er meiri. Mótlykill við þennan lykil er mótbókun fasts kostnaðarverðs. |
| Tap á föstu verði innhreyfingar (innkaup, tap á föstu verði innhreyfingar*) | 510310 | Frávik innkaupaverðs | Kostnaður | Debet | Nr. | F | Hagnaður á föstu verði innhreyfingar | Notað þegar reikningur innkaupapöntunar er bókaður og munur er á milli reikningsfærðs verðs og sjálfgefins kostnaðar fyrir vöruna. Þessi lykill er notaður þegar munurinn er minni. Mótlykill við þennan lykil er mótbókun fasts kostnaðarverðs. |
| Mótbókun fasts innhreyfingarverðs (Innkaup, mótbókun fasts innhreyfingarverðs*) | 140900 | Birgðaafbrigði | Eign | Bæði | Nr. | F  | |Notað þegar reikningur innkaupapöntunar er bókaður og munur er á milli reikningsfærðs verðs og sjálfgefins kostnaðar fyrir vöruna. Þessi lykill er mótlykill fyrir rekstrarlykla fasts kostnaðarverðs. |
| Gjald | NA | NA | NA | NA | NA | NA | NA | Þessi lykill er ekki lengur notaður. Nota birgðaafbrigðið í staðinn. |
| Birgðaafbrigði | 600170 | Birgðaafbrigði | Kostnaður | Kredit | Nr. | Bæði | | Þessi lykill er notaður þegar: <ul><li>Mismunur er á einingaverði milli innhreyfingarskjals afurða og reiknings.</li><li>Gjöld eru bókuð á vöruna.</li><li>Óbeinn kostnaður hefur verið<!--note from editor: Edit okay?--> bætt við keyptar vörur. </li><li>Mótlykill við þennan lykil er lykillinn „Útgjöld innkaupa, óreikningsfærð“.</li></ul> |
| Innkaup, uppsöfnun | 200140 | Uppsöfnuð innkaup | Bótaábyrgð | Kredit | Y | P | |Notað þegar afurðarinnhreyfing innkaupapöntunar er bókuð og valkosturinn fyrir uppsafnaðar innkaupaupphæðir eru virkur. |
| Áfallinn virðisaukaskattur á innhreyfingu | 250500 | Uppsafnaður virðisaukaskattur | Bótaábyrgð | Kredit | Y | Bæði  | |Þessi lykill er notaður þegar valkosturinn **Bóka efnislegan skatt** er valinn í **Færibreytur birgða- og vöruhúsakerfis** og þú ert með innkaupapöntun með skatti. Upphæðin er bókuð þegar þú uppfærir innkaupapöntunina efnislega (innhreyfingarskjal afurðar) og bakfærð þegar þú bókar innkaupapöntunina fjárhagslega (reikningur). |
| Eignarinnhreyfing (eignadebet*) | 180100 | Efnislegar eignir | Eign | Debet | N | Bæði | Bæði | Þessi lykill er notaður þegar þú velur valkostinn í innkaupapöntunarlínunni fyrir eignir. Samþætting innkaupapöntunar hefur verið grunnstillt til að fá eignina með innhreyfingarskjali afurðar eða reikningi. Frekari upplýsingar um samþættingu á innkaupapöntun eignar er að finna í [Kaupa eignir með innkaupum](/fixed-assets/acquire-assets-procurement). |
| Innkaupaútgjöld kostnaðar | 618900 | Ýmis kostnaður | Kostnaður | Debet | N | Bæði | |Notað þegar innhreyfingarskjal afurðar eða reikningur fyrir innkaupapöntun er bókaður þar sem vörurnar eru ekki á lager eða innkaupategund er notuð. |
| Fyrirframgreiðsla | 132190 | Fyrirframgreiddur kostnaður | Eign | Debet | N | Bæði | | Notað þegar unnið er með fyrirframgreiðslureikning á innkaupapöntun. |


\*Gildi sýnd innan sviga tákna gildið sem er notað í reitnum **Bókunargerð** á síðunni **Fylgiskjalafærslur**. Hægt er að skoða **Bókunargerð** á síðunni **Færslur fylgiskjals** á flipanum **Almennt**.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Eignabókun með innkaupapöntunum

Ef þú notar eininguna **Eignir** og ætlar að kaupa eignir í gegnum innkaupapantanir þarf að grunnstilla bókunargerðina **Eignainnhreyfing** í flipanum **Innkaupapöntun** á síðunni **Birgðabókunarregla**. Frekari upplýsingar er að finna í [Samþætting eigna](/fixed-assets/fixed-asset-integration.md) og [Stofna og eignast eignir úr viðskiptaskuldum](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Bókun fyrirframgreiðslu innkaupapöntunarreiknings

Ef þú hyggst nota eiginleikann **Fyrirframgreiðslureikningur** fyrir innkaupapantanir verður að velja bókunargerðina **Fyrirframgreiðsla** í flipanum **Innkaupapöntun** á síðunni **Birgðabókunarregla**. Frekari upplýsingar er að finna á [Fyrirframgreiðslureikningar samanborið við fyrirframgreiðslur](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Bókun innkaupabeiðni og staðfestingar innkaupapöntunar

Einnig er hægt að grunnstilla staðfestingar innkaupabeiðni og innkaupapöntunar til að bóka áætluð fjárúthlutun og fjárúthlutun í fjárhaginn. Þessum bókunum er stjórnað með bókunarskilgreiningu. Frekari upplýsingar er að finna á [Um fjárúthlutun innkaupapöntunar](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Bókun innkaupategundar

Í stað þess að setja upp birgðabókun fyrir allar vörur, vöruflokk eða staka vöru er hægt að setja upp flokka og stjórna fjárhagsbókuninni með innkaupaflokkum. Frekari upplýsingar um uppsetningu flokka og úthlutun þeirra á vörur er að finna í [Dæmi um grunnstillingu bókunarreglu](#sample-posting-profile-configuration) fyrr í þessari grein.

Þegar flokkar með innkaupapöntunum eða sölureikningum eru notaðir þarf að úthluta tegundastigveldinu á gerðina **Tegundastigveldi innkaupa** á síðunni **Hlutverkaúthlutun tegundastigveldis**.

### <a name="vendor-invoices-with-procurement-categories"></a>Lánardrottnareikningar með innkaupaflokka

Ef fyrirtækið þitt notar innkaupapantanir fyrri sum innkaup en ekki önnur er hægt að vinna úr reikningum sem tengjast ekki innkaupapöntun á ýmsa vegu. Þetta felur í sér að nota færslubækur í **Viðskiptaskuldir** eða með síðunni **Lánardrottnareikningar í bið** sem er notað til að búa til reikninga fyrir innkaupapantanir. Þegar reikningar sem tengjast ekki innkaupapöntun eru búnir til þarf að búa til innkaupaflokka fyrir hverja kostnaðargerð. Varpa þarf flokknum í réttan kostnaðarlykil á síðunni **Birgðabókunarreglur**.

Nákvæmur fjöldi flokka fer eftir fjölda kostnaðarlykla sem notaðir eru til að bóka reikningana. Þú þarft að minnsta kosti eina innkaupategund fyrir hvern aðallykil þar sem þú notar reikninga sem tengjast ekki innkaupapöntun. Hægt er að nota marga flokka fyrir einn aðallykil. Þetta getur verið gagnlegt fyrir nothæfi, leitarmöguleika og skýrslugerð um hvers konar kostnað þú notar.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Ávinningur af því að nota innkaupaflokka fyrir reikninga lánardrottins

Ávinningur af því að nota innkaupaflokka fyrir reikninga lánardrottins er meðal annars:

- Samræmd upplifun notanda: Þegar innkaupaflokkar eru grunnstilltir fyrir kostnað sem tengist ekki innkaupapöntun geta notendur fengið þjálfun í einu ferli fyrir reikningsfærslu með því að nota síðuna **Lánardrottnareikningar í bið**.
- Bætt upplifun skýrslugerðar: Þegar innkaupaflokkar eru grunnstilltir fyrir allar vörur og kostnað sem tengist ekki innkaupapöntun mun eyðsluskýrsla innkaupa greina eyðslu eftir lánardrottni, flokki o.fl.
- Samræmt verkflæði: Þegar **Lánardrottnareikningar í bið** eru notaðir til að vinna úr öll reikningum er hægt að búa til samræmt verkflæði og samþykktarferli með því að nota stakt verkflæði.

## <a name="consignment-inventory-posting"></a>Vörusendingarbirgðabókun

Vörusendingarbirgðir nota sömu fjárhagsbókunina og aðrar keyptar vörur. Lykilmunurinn er sá að þegar birgðirnar eru mótteknar eru engar fjárhagsfærslur skráðar. Til að færa eignarhald yfir á fyrirtækið þegar færslubók **Eignarhaldsbreytinga** er bókuð er fylgiskjal stofnað til að skrá kostnað vörunnar. Frekari upplýsingar er að finna á [Uppsetning vörusendingar](/supply-chain/inventory/consignment.md).

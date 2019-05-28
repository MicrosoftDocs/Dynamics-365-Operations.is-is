---
title: Leita að afurðir og afurðarafbrigði við skráningu pantana
description: Nota skal **Vörunúmer** svæðið til að leita að afurðir og afurðarafbrigði þegar handvirkt eru stofnaðar á sölupöntunarlínu eða innkaupapöntunarlínu. Þannig er hægt að finna afurðarafbrigði á skjótan hátt þegar aðeins er tiltækur skilgreiningarstrengur eða afurðarvíddum.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bf90dc4823599ed6ff8e81986fc35f2210b66b0c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560274"
---
# <a name="search-for-products-and-product-variants-during-order-entry"></a>Leita að afurðir og afurðarafbrigði við skráningu pantana

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

Nota skal **Vörunúmer** svæðið til að leita að afurðir og afurðarafbrigði þegar handvirkt eru stofnaðar á sölupöntunarlínu eða innkaupapöntunarlínu.  Þannig er hægt að finna afurðarafbrigði á skjótan hátt þegar aðeins er tiltækur skilgreiningarstrengur eða afurðarvíddum.

Stundum er ekki best að hafa of mikið af einhverju, og það er sérstaklega satt ef þú selur fjölda af vörum sem eru svipuð og þú ert að reyna að muna vörunúmer eða vöruleitarnöfn í því skyni að finna rétt vöru til að setja á sölupöntun. Hægt er að nota reitinn **Vörunúmer** í sölupöntunarlínu eða innkaupapöntunarlínu sem leitarsvæði. Þú getur slegið inn hvaða hluta af vöruheitinu, númer, eða vídd og fá flettu sem sýnir öll atriðin sem passa við leitarorð.

## <a name="how-searchworks"></a>Hvernig leit virkar
Þegar þú leitar að vörur eða afbrigði, er mikilvægt að skilja hvernig leitareiginleikarnir finnur þær vörur sem passa við textann sem þú slærð inn. Lykil leitarreglur í að afhenda leitarniðurstöður eru:

-   Leitarniðurstöður munu skila hvaða samsvarandi færslu, óháð reitnum þar sem leitartextinn er færð inn.
-   Leitartextinn verður að vera til staðar í samsvarandi færslu í fullt lengd hennar.
-   Samsvörun koma jafnvel þótt leitartextinn fannst í miðju textastrengs í samsvarandi færslu. Það þarf ekki að birtast í upphafi textastrengs.
-   Leitartextinn er meðhöndluð sem einni textastreng jafnvel þó að hún inniheldur auð bil.

### <a name="examples"></a>Dæmi

Eftirfarandi dæmi nota afurðir og afurðarafbrigði sem sýna hvernig leit er meðhöndlaðar í mismunandi aðstæðum. **Skilyrði:**  Undir **Sölu og markaðssetningar &gt; Uppsetning &gt; Leit &gt; Leitarfæribreytur &gt; Leitargerð**, veljið valkostinn  **Full samsvörun**.

| Gerð afurðar     | Afurðarnafn    | Birta afurðarnúmer | Vörunúmer | Grunnstilling |
|------------------|-----------------|------------------------|-------------|---------------|
| Einkvæm afurð | SpeakerMidRange | D0001                  | D0001       | Á ekki við            |
| Afurðarafbrigði  | Virkur hátalari  | D0010:::Svartur         | D0010       | 000005        |
| Afurðarafbrigði  | Virkur hátalari  | D0010:::Hvítur:         | D0010       | Hvítt         |

Ef þú færir inn 'háta' í við **Vörunúmer** svæðinu kemur allar afurðir fyrir ofan sem niðurstaða í uppflettisvæðinu. Ef 'svart' er fært inn í **Vörunúmer** svæðið kemur seinni afurðar sem niðurstaða, því hún hefur textinn 'svart' á birtu afurðarnúmeri. Þessi tvö dæmi sýna að leitin er ekki aðeins í upphafi reits, samsvörun mun eiga sér stað, jafnvel þótt leitartexta er að finna í miðju textastrengs í samsvarandi skrá.  

Ef þú slærð '05' þú verður bara að fá annað afurðarafbrigði sem niðurstaða, vegna þess að það hefur '05' í stillingunum. Þetta sýnir að leitin er þvert á öll virk svæði á síðunni **Leitarskilyrði**.  

Ef þú slærðu inn 'háta 05' kemur engum niðurstöðum. Þetta er því leitina leitar að fulla texta sem færður er inn. Leitin reynir ekki að finna 'háta' og þrengja svo að niðurstöðurnar við þær sem innihalda '05'.  

Hægt er að takmarka fjölda leitarniðurstöður með því að nota **Fjöldi niðurstaðna** á **Sölu og markaðssetningar &gt; Uppsetning &gt; Leit &gt; Leitarfæribreytur**  síðunni. Ef svæðið er stillt á 0, verður allar leitarniðurstöður skilað. Ef þetta er stillt á 10, til dæmis, mun hún skila að hámarki 10 leitarniðurstöður.

## <a name="configure-the-productsearch"></a>Skilgreina leit að afurð
Áður en hægt er að nota afurða og leitareiginleika afurðarafbrigðis, skal fylgja þessum skrefum til að skilgreina leit að afurðar. [![3 skref til að skilgreina afurðarleit search\_AXAppFall ](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>1. skref: Hafa með allar viðeigandi afurð og auðkenni afurðarafbrigðis og víddir í leitarskilyrði

Dæmi um afurð og auðkenni afurðarafbrigðis og víddir sem hægt er að leita eftir eru  **vörunúmer, afurðarheiti**, **Sýna afurðarnúmer, Afbrigði, Lit, Stærð, Stíl, leitarnafn o.s.frv**.  

Farið í **Sala og markaðssetning &gt; Uppsetning &gt; Leita &gt; Leitarskilyrði** síðuna. Á **Leitarskilyrði** síðuna gerir kleift að skilgreina skilyrði fyrir viðskiptavinurinn, viðfangs og afurðaleit. Gangið úr skugga um verið sé að sía síðuna með leitarskilyrði afurðar. Þetta er gert með því að skipta í **Afurð** í valmynd síðu.  

Til að birta afurðarnúmeri á leitarskilyrði, smellið á **Nýtt** í valmyndsíðu. Þetta bætir nýrri færslu við **Leitarskilyrði** hnitanetið. Opna skal **svæðisheiti** uppflettingardálk og velja **DisplayProductNumber**. Til að bæta skilgreiningu afurðar við leitarskilyrði, skal stofna nýja færslu í **Leitarskilyrði** hnitanetinu og velja **configId** í **svæðisheiti** dálk. Stofna færslu á sama hátt með **svæðisheiti** **InventColorId** fyrir litavíddina, **InventSizeId** fyrir stærð víddar, og **InventStyleId** fyrir stíl víddar.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>2. skref: Fylla gagnasafnstöflu sem notaður er fyrir afurðaleit

Í **Leitarskilyrði** síðunni, smellið á **Uppfærsla fyrir leitargögn** hnappinn. Í **uppfærsla fyrir leitargögn** svarglugganum, gangið úr skugga um að  **Uppruni** er stillt á **Afurð**, og smellið svo á **í lagi**. Kerfið mun leggja saman í eina töflu allar valdar leitarskilyrði tilgreind í skrefi 1. Ef þú hefur fjölda af vörum og afurðarafbrigði, getur þetta ferli verið langt og þú getur fengið viðvörun. Við mælum með að áætlir að fylla í leitartöfluna á runuþjóni á þeim tíma þegar þjóninn er ekki of upptekinn.  

Þar til taflan er fyllt út veitir afurðaleit ekki rétt niðurstöður. Ef þú færð engar leitarniðurstöður skal tryggja að þessi tafla er útfyllt.  

Taflan þarf aðeins að vera útfyllt þegar leitarskilyrði er breytt. Nýlega útgefin afurð og afbrigði eru sjálfkrafa bætt við töfluna. Eyddum afurðir og afbrigði eru sjálfkrafa tekin úr töfluna.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>Skref 3: Virkja uppfletting fyrir afurðaleit á sölu og innkaupapöntunarlínur

Þessar aðgerðir er hægt að virkja með því að fara í **Sölu og markaðssetningar &gt; Uppsetning &gt; Leit &gt; Leitarfæribreytur** og stilla **Virkja uppflettingu fyrir leit** á **Já** á flipanum **Almennar**.  

Fyrir færslu í sölupöntunarlínu, er sjálfgefna hegðun að opna **afurðaleit** síðuna þegar byrjað er að því að slá inn í  **Vörunúmer** svæðinu og styðjið á  **Tab** lykill. Síðan **afurðaleit** breytir samhengi við stofnun á pöntunarlínu og má telja hana óþarflega ágenga. Ef óskað er að sækja leitarniðurstöður í uppflettingu og glata ekki samhengi við innfærslu pöntunarlínu, er hægt að nota uppflettingarleit í staðinn. Ef þú leitar að afurð eða afurðarafbrigði en velur ekki neitt á uppflettingu og ýtið á **Tab** lykill, birtist **afurðaleit** síða.




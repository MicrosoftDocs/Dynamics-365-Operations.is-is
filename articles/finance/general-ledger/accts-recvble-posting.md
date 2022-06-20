---
title: Bókun á viðskiptakröfum
description: Þessi grein útskýrir hvernig færslur eru stilltar í Viðskiptakröfur og gefur dæmi um bókunarstillingar.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 492bbd31cae08a93cd68e5ce120d02a62141241b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874575"
---
# <a name="accounts-receivable-posting"></a>Bókun á viðskiptakröfum

[!include [banner](../includes/banner.md)]

Aðal færslusniðið fyrir **Reikningur fáanlegur** mát er póstsnið viðskiptavinarins. Þetta bókunarsnið ákvarðar yfirlitsreikninginn sem er notaður þegar innstæður viðskiptavina eru bókaðar í fjárhag. Yfirlitsreikningur er aðalreikningur. Það er einnig nefnt viðskiptareikningur viðskiptakrafna.

Frekari upplýsingar eru í [Bókunarreglur viðskiptavina](../accounts-receivable/customer-posting-profiles.md).

Nokkrar bókunarstillingar við hliðina á bókunarsniði viðskiptavina eru tiltækar í Viðskiptakröfur. Eftirfarandi hlutar veita frekari upplýsingar um þessar aðrar birtingarstillingar.

## <a name="posting-accounts-for-methods-of-payment"></a>Bókun reikninga fyrir greiðslumáta

Greiðsluaðferðir skilgreina hvernig greiðsla verður bókuð í fjárhag. Þeir stjórna einnig hegðun greiðsluúttaksins. Venjulega er ein greiðslumáti búin til fyrir hverja greiðslutegund sem fyrirtæki þitt samþykkir (til dæmis reiðufé, ávísun, kreditkort, peningapöntun og millifærslu).

Reitirnir í **Birting** kafla um **Almennt** Flýtiflipi stjórnar hvernig greiðsla verður bókuð í fjárhag. Þú verður fyrst að velja gildi í **Tegund reiknings** sviði. Reikningstegundin sem þú velur stjórnar hegðun reikningsins **Greiðslureikningur** sviði. Við mælum með að þú veljir **Banki** í **Tegund reiknings** reitnum og veldu síðan bankareikninginn í **Greiðslureikningur** sviði. Ávinningurinn af þessari nálgun er að kerfið mun bóka greiðsluna í undirbók bankans, sem styður afstemmingu og önnur reiðufjártengd ferli. Eftirfarandi tafla sýnir dæmi um uppsetningu póstsniðs ef þú ert að nota **Handbært fé og bankastjórnun** mát.

| Bókunargerð | Lykilgerð | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Banki | Banki | Bank of Contoso | Bankareikningur sem er tengdur við eign | Kredit | Nr. | Fyrir hvern greiðslumáta skaltu slá inn aðalreikninginn í **Greiðslureikningur** sviði. |

Ef þú ætlar ekki að nota reiðufé og bankastjórnun ættir þú að velja **Fjárhagsbók** í **Tegund reiknings** reitnum og veldu síðan aðalreikninginn í **Greiðslureikningur** sviði. Eftirfarandi tafla sýnir dæmi um uppsetningu bókunarsniðs ef þú ert ekki að nota reiðufé og bankastjórnun.

| Bókunargerð | Lykilgerð | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Fjárhagur | Fjárhagur | 100100: Bank of Contoso | Eign | Kredit | Nr. | Fyrir hvern greiðslumáta skaltu slá inn aðalreikninginn í **Greiðslureikningur** sviði. |

## <a name="bridging-accounts"></a>Brúarreikningar

Brúarbókun er tveggja þrepa ferli sem er notað þegar greiðslur eru bókaðar. Það er valfrjáls eiginleiki sem hægt er að nota með bankareikningum með núllstöðu, til dæmis. Það getur hjálpað til við að tryggja sléttara og tímanlegra bankaafstemmingarferli. Í fyrsta skrefi er greiðsla bókuð á tímabundinn reikning (brúarreikninginn). Í öðru skrefi er bókað færslan bakfærð og færð inn á bankareikninginn þegar greiðslan hreinsar bankann. Eftirfarandi tafla sýnir dæmi um uppsetningu bókunarsniðs fyrir brúarfærslu.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Færslubók fjárhags | 130725 | Óafgreidd reiðufé | Bótaábyrgð | Debet | Já | Fyrir hvern greiðslumáta skaltu slá inn aðalreikninginn í **Brúarreikningur** sviði. |

Fyrir frekari upplýsingar, sjá [Setja upp og vinna úr brúuðum greiðslum](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="posting-accounts-for-customer-cash-discounts"></a>Bókun reikninga fyrir staðgreiðsluafslátt viðskiptavina

Ef fyrirtækið þitt býður viðskiptavinum staðgreiðsluafslátt gegn skjótri greiðslu, verður þú að stilla staðgreiðsluafsláttarkóða og tilgreina hvernig afslættir eigi að bóka í fjárhag. Nokkrir valkostir eru í boði til að tilgreina aðalreikninginn sem er notaður til að bóka staðgreiðsluafslátt viðskiptavinar.

Fyrir frekari upplýsingar, sjá [Staðgreiðsluafsláttur](../cash-bank-management/cash-discounts.md).

## <a name="posting-accounts-for-payment-fees"></a>Bókun reikninga fyrir greiðslugjöld

Greiðslugjöld gera þér kleift að bæta gjaldi sjálfkrafa við greiðslu viðskiptavina þegar sett skilyrði eiga við. Hægt er að innheimta greiðslugjöld á viðskiptavininn, eða þau geta verið færð á bankareikning þinn sem kostnað. Hér eru nokkur dæmi:

- Þú rukkar viðskiptavini um 3 prósent af heildargreiðslunni ef þeir greiða með kreditkorti.
- Bankinn þinn rukkar þig $1.00 fyrir hverja millifærslu sem þú vinnur og millifærslugjaldið er gjaldfært.

Þegar þú stillir greiðslugjald viðskiptavinar, ef þú stillir á **Hleðsla** sviði til **Viðskiptavinur**, hinn **Aðalreikningur** reiturinn verður ekki tiltækur og kerfið notar færslusnið viðskiptavinar til að bóka gjaldið. Ef þú stillir **Hleðsla** sviði til **Fjárhagsbók**, þú verður að stilla **Aðalreikningur** reit inn á aðalreikning þar sem greiðslugjaldið verður bókað. Venjulega mun þessi aðalreikningur vera kostnaðarreikningur. Eftirfarandi tafla sýnir dæmi um uppsetningu bókunarsniðs fyrir bókun greiðslugjalda.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Færslubók fjárhags | 618190 | Bankagjaldskostnaður | Kostnaður | Debet | Nr. |  Ef **Fjárhagsbók** er valið í **Hleðsla** reit, veldu þennan reikning í **Aðalreikningur** reit fyrir greiðslugjaldið. |

Nánari upplýsingar er að finna í [Koma á fót greiðsluþóknunum viðskiptavina](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Bókun reikninga fyrir gjaldkóða

Ef þú verður að fylgjast með söluupphæðum til viðbótar við línuvörur geturðu notað gjaldakóða. Til dæmis gætirðu rukkað vöruflutninga- og afgreiðslugjöld af viðskiptavinum þínum, eða þú gætir rukkað nokkur vöru- og afgreiðslugjöld innanhúss. Hægt er að tilgreina hvort þessar upphæðir séu bókaðar á kostnaðarreikninga eða bætt við kostnað hlutanna.

Þú getur búið til gjaldakóða fyrir Viðskiptakröfur og Viðskiptaskuldir. Þegar þú stillir gjaldkóða verður þú að skilgreina bókunina. Bókunin stjórnar bæði debetreikningi og kreditreikningi. Fyrir hvern gjaldkóða sem þú býrð til geturðu valið bókunartegundina sem er notuð. Eftirfarandi tafla sýnir dæmigerð dæmi um gjaldakóða fyrir viðskiptakröfur.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Greiðsluþóknun | 411400 | Tekjur - Gjöld | Tekjur | Kredit | Nr. | **Dæmi um ófullnægjandi fjármuni:** Debet viðskiptavinur / lánardrottinn og Kreditbókarreikningur |
| Pöntun, farmur | 403500 | Tekjur - Frakt | Tekjur | Kredit | Nr. | **Dæmi um vöruflutninga sem gjaldfærður er á viðskiptavin:** Debet viðskiptavinur / lánardrottinn og Kreditbókarreikningur |
| Eftirágreiddur afsláttur\* | 403200 | Afsláttur | Tekjur | Debet | Nr. | **Dæmi um afslátt viðskiptavina:** Debetbókarreikningur og kreditviðskiptavinur/seljandi |

\* Fyrir afsláttardæmið er bókunin aðeins notuð þegar gjaldkóða er bætt við innkaupapöntunarhaus eða línu. Háþróuð afsláttarvirkni sem er fáanleg í Microsoft Dynamics 365 Supply Chain Management veitir meiri stjórn og sjálfvirkni á afslætti. Fyrir frekari upplýsingar, sjá [Viðskiptavinaafsláttur](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

Taflan á undan sýnir þrjú dæmigerð dæmi um bókunargerðir sem hægt er að nota fyrir gjaldkóða. Það ætti að nota sem leiðbeiningar og sýnishorn. Það veitir ekki tæmandi lista yfir allar mögulegar samsetningar eða birtingargerðir sem hægt er að nota.

Fyrir frekari upplýsingar, sjá [Búðu til gjaldkóða](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Bókun reikninga fyrir þóknun

Þú getur valfrjálst stillt kerfið til að reikna þóknun fyrir sölufulltrúa eða hóp sölufulltrúa á tiltekinni sölupöntun. Ef þú virkjar þessa virkni verður þú að stilla bókunarreikninginn sem er notaður til að reikna út þóknunina. Þessi uppsetning er gerð á **Umboðsskrifstofa** síðu í **Sala og markaðssetning** mát.

Fyrir frekari upplýsingar, sjá [Settu upp reglur um söluþóknun](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md).

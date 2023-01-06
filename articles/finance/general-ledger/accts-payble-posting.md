---
title: Bókanir viðskiptaskulda
description: Í þessari grein er útskýrt hvernig bókanir eru skilgreindar í viðskiptaskuldum og gefin eru upp dæmi um bókunarskilgreiningar.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b3593e01ed4d0a88b5816803f1d67fa7ed5e0f6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908010"
---
# <a name="accounts-payable-posting"></a>Bókun lánardrottnalykils

[!include [banner](../includes/banner.md)]

Aðalbókunarreglan fyrir eininguna **Viðskiptakröfur** er bókunarregla lánardrottins. Þessi bókunarregla ákvarðar safnlykilinn sem notaður er þegar stöður lánardrottna eru bókaðar í fjárhaginn. Safnlykill er aðallykill. Einnig er vísað í hana sem viðskiptalykil viðskiptaskulda.

Frekari upplýsingar er að fá í [Bókunarreglur lánardrottins](../accounts-payable/vendor-posting-profiles.md).

Nokkrar bókunarskilgreiningar fyrir utan bókunarreglu lánardrottins eru í boði í viðskiptaskuldum. Eftirfarandi hlutar veita frekari upplýsingar um þessar öðru bókunarskilgreiningar.

## <a name="methods-of-payment-posting-accounts"></a>Bókunarlyklar greiðslumáta

Greiðslumátar skilgreina hvernig greiðsla er bókuð í fjárhag. Þeir stjórna einnig hegðun greiðsluúttaksins. Venjulega er einn greiðslumáti búinn til fyrir hverja greiðslu sem fyrirtækið framkvæmir (til dæmis reiðufé, ávísun, kreditkort, peningapöntun og símgreiðslu).

Reitirnir í hlutanum **Bókun** í flýtiflipanum **Almennt** á síðunni **Greiðslumátar** (**Viðskiptaskuldir > Greiðsluuppsetning > Geiðslumátar**) stjórna því hvernig greiðsla er bókuð í fjárhaginn. Fyrst þarf að velja gildi í reitnum **Gerð lykils**. Gerð lykils sem þú velur stjórnar hegðuninni í reitnum **Greiðslulykill**. Við mælum með því að þú veljir **Banki** í reitnum **Gerð lykils** og veljir svo bankareikninginn í reitnum **Greiðslulykill**. Ávinningur af aðferðinni er að kerfið mun bóka greiðsluna í undirbók bankans, sem styður afstemmingu og önnur ferli sem tengjast reiðufé. Eftirfarandi tafla sýnir dæmi um skilgreiningu á bókunarreglu ef þú ert að nota eininguna **Reiðufjár- og bankastjórnun**.

| Bókunargerð | Lykilgerð | Dæmi um heiti greiðslulykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Banki | Banki | Bank of America | Bankareikningur sem tengist eign | Debet | Nr. | Sláðu inn aðallykilinn í reitinn **Greiðslulykill** fyrir hvern greiðslumáta. |

Ef þú hyggst ekki nota reiðufjár- og bankastjórnun ættirðu að velja **Fjárhag** í reitnum **Gerð lykils** og síðan velja aðallykilinn í reitnum **Greiðslulykill**. Eftirfarandi tafla sýnir dæmi um skilgreiningu á bókunarreglu ef þú ert **ekki** að nota reiðufjár- og bankastjórnun.

| Bókunargerð | Lykilgerð |Dæmi um greiðslulykil | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Fjárhagur | Fjárhagur | 100100: Bank of America | Eign | Debet | Nr. | Sláðu inn aðallykilinn í reitinn **Greiðslulykill** fyrir hvern greiðslumáta. |

## <a name="bridging-accounts"></a>Millilyklar

Millibókun er tveggja skrefa ferli sem er notað þegar greiðslur eru bókaðar. Þetta er valfrjáls eiginleiki sem hægt er að nota með til dæmis núlljöfnuði á bankareikningum. Það getur hjálpað til við að tryggja einfaldari og tímanlega bankaafstemmingu. Í fyrsta skrefinu er greiðsla lögð inn á tímabundinn reikning (millilykil). Í öðru skrefinu er bókaða færslan bakfærð og bókuð á bankareikninginn þegar greiðslan er samþykkt af bankanum. Eftirfarandi tafla sýnir dæmi um skilgreiningu á bókunarreglu fyrir millibókun.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Færslubók fjárhags | 130725 | Óafstemmt reiðufé | Bótaábyrgð | Debet | Já | Sláðu inn aðallykilinn í reitinn **Millilykill** fyrir hvern greiðslumáta. |

Nánari upplýsingar um það eru í [Uppsetning og vinnsla greiðslna á millilykli](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="customer-cash-discounts-posting-accounts"></a>Bókunarlyklar fyrir staðgreiðsluafslætti viðskiptavinar

Ef fyrirtækið tekur við staðgreiðsluafslætti frá lánardrottnum til að fá greiðslur á fljótlegri hátt þarf að skilgreina kóða staðgreiðsluafsláttar og tilgreina hvernig afslættir eigi að vera bókaðir í fjárhaginn. Nokkrir valkostir eru í boði til að tilgreina aðallykilinn sem er notaður til að bóka staðgreiðsluafslátt viðskiptavinar.

Sjá [Staðgreiðsluafslættir](../cash-bank-management/cash-discounts.md) fyrir frekari upplýsingar.

## <a name="payment-fee-posting-accounts"></a>Bókunarlyklar greiðsluþóknunar

Greiðsluþóknanir gera þér kleift að bæta þóknun sjálfkrafa við greiðslu lánardrottins þegar safn skilyrða er uppfyllt. Hægt er að greiða greiðsluþóknanir til lánardrottins eða bóka þær á bankareikning sem kostnað. Hér eru nokkur dæmi:

- Lánardrottinn leggur 3 prósenta gjald á heildargreiðsluna ef þú greiðir með kreditkorti.
- Bankinn þinn rukkar þig um $ 1,00 fyrir hverja millifærslu sem þú vinnur úr og millifærslugjaldið er kostnaður.

Þegar greiðsluþóknun lánardrottins er skilgreind, ef reiturinn **Gjald** er stilltur á **Lánardrottinn**, verður reiturinn **Aðallykill** óaðgengilegur og kerfið notar bókunarreglu lánardrottins til að bóka þóknunina. Ef þú stillir reitinn **Gjald** á **Fjárhagur** verður þú að stilla reitinn **Aðallykill** á aðallykilinn þar sem greiðsluþóknunin verður bókuð. Venjulega er þessi aðallykill kostnaðarlykill. Eftirfarandi tafla sýnir dæmi um skilgreiningu á bókunarreglu fyrir bókun´ greiðsluþóknunar.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Færslubók fjárhags | 618190 | Kostnaður bankagjalds | Kostnaður | Debet | Nr. | Ef **Fjárhagur** er valið í reitnum **Gjald** skal velja þennan lykil í reitnum **Aðallykill** á síðunni **Greiðsluþóknun**. |

Nánari upplýsingar er að finna í [Skilgreina greiðsluþóknanir lánardrottna](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Bókunarlyklar gjaldakóða

Ef rekja þarf innkaupaupphæðir ásamt línuatriðum er hægt að nota gjaldakóða. Til dæmis kann birgir að innheimt farm- og umsýslugjöld hjá viðskiptavini eða bóka kostnað vegan farm- og umsýslugjalda innanhúss. Þá er hægt að tilgreina hvort upphæðin er birt á kostnaðarreikningum eða bætt við kostnað varanna.

Þú getur búið til skuldfærslukóða fyrir Viðskiptakröfur og Viðskiptaskuldir. Þegar gjaldakóði er skilgreindur verður að skilgreina færsluna. Bókunin stjórnar bæði debetlyklinum og kreditlyklinum. Þegar gjaldakóðar eru stofnaðir er hægt að velja bókunargerðina sem er notuð fyrir hvern gjaldakóða. Eftirfarandi tafla sýnir dæmi um dæmigerða gjaldakóða fyrir viðskiptaskuldir sem eru greiddar á síðunni **Gjaldakóðar**.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Innkaupagjöld | Hafið svæðið autt. | Á ekki við | Atriði | Debet | Nr. | **Dæmi um kaupgjald fyrir vöru:** </p><ul><li>Reitur **Debetgerð** = **Vara**</li><li>  Reitur **Kreditgerð** = **Viðskiptavinur/Lánardrottinn**.</li><li> Bókun vörunnar notar aðallykilinn frá birgðabókunarreglunni. |
| Pöntun, farmur | 600120 | Farmur inn | Tekjur | Debet | Nr. | **Dæmi fyrir farm sem er greiddur til lánardrottins:** </p><ul><li>Reitur **Debetgerð** = **Fjárhagslykill**</li><li> Reitur **Kreditgerð** = **Viðskiptavinur/Lánardrottinn** |
| Eftirágreiddur afsláttur\* | 503160 | Afsláttur lánardrottins (andstæða kostnaðar seldra vara)| Kostnaður | Kredit | Nr. | **Dæmi um afslátt lánardrottins:**</p><ul><li>Reitur **Debetgerð** = **Viðskiptavinur/Lánardrottinn**</li><li>Reiturinn **Kreditgerð** = **Fjárhagslykill** |

\* Fyrir eftirágreiddan afslátt til dæmis er bókunin aðeins notuð þegar skuldfærslukóða er bætt við innkaupapöntunarhaus eða línu. Ítarlegri virkni fyrir eftirágreiddan afslátt sem er í boði í Microsoft Dynamics 365 Supply Chain Management veitir meiri stjórn og sjálfvirkni fyrir eftirágreiddan afslátt. Sjá [Eftirágreiddur afsláttur lánardrottins](../../supply-chain//procurement/vendor-rebates.md) fyrir frekari upplýsingar.

Fyrri taflan sýnir þrjú dæmigerð dæmi um bókunargerðir sem hægt er að nota fyrir gjaldkóða. Það ætti að nota sem leiðbeiningar og valsýnishorn. Ekki er lagður til tæmandi lista yfir allar mögulegar samsetningar eða bókunargerðir sem hægt er að nota.

Nánari upplýsingar má finna í [Stofna gjaldakóða](../accounts-receivable/create-charges-codes.md).

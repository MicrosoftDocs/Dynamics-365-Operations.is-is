---
title: Bókun á viðskiptakröfum
description: Í þessari grein er útskýrt hvernig bókanir eru skilgreindar í viðskiptakröfum og gefin eru upp dæmi um bókunarskilgreiningar.
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
ms.openlocfilehash: 0d679595a1f702c4e3ade138a87c817d245fcf79
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324330"
---
# <a name="accounts-receivable-posting"></a>Bókun á viðskiptakröfum

[!include [banner](../includes/banner.md)]

Aðalbókunarreglan fyrir eininguna **Viðskiptakröfur** er bókunarregla viðskiptavinar. Þessi bókunarregla ákvarðar safnlykilinn sem notaður er þegar stöður viðskiptavina eru bókaðar í fjárhaginn. Safnlykill er aðallykill. Einnig er vísað í hana sem viðskiptalykil viðskiptakrafna.

Skýrsluna **Viðskiptavinur til fjárhagsafstemmingar** er hægt að nota eftir bókun til að hjálpa til við að afstemma stöður viðskiptavina- og lánardrottnalykla. Skýrslan notar upplýsingarnar sem er að finna í safnlyklinum fyrir bókunarreglu viðskiptavinar. Hún notar ekki safnlykilinn úr bókhaldinu sem stofnaður er fyrir skjalið. Ef gerðar eru breytingar á bókunarreglu viðskiptavinar eða viðskiptavinaflokknum sem viðskiptavininum er úthlutað eftir að færslurnar hafa verið bókaðar gæti skýrslan sýnt mun á stöðu viðskiptavina- og fjárhagslykils. Til að skoða aðeins línurnar sem eru með mismun og línur þar sem viðskiptavina- og lánardrottnalyklar eru báðir núll skal velja færibreytuna **Aðeins mismunur** þegar skýrslan er prentuð.

Frekari upplýsingar eru í [Bókunarreglur viðskiptavina](../accounts-receivable/customer-posting-profiles.md).

Nokkrar bókunarskilgreiningar fyrir utan bókunarreglu viðskiptavinar eru í boði í viðskiptakröfum. Eftirfarandi hlutar veita frekari upplýsingar um þessar öðru bókunarskilgreiningar.

## <a name="posting-accounts-for-methods-of-payment"></a>Bókunarlyklar fyrir greiðslumáta

Greiðslumátar skilgreina hvernig greiðsla er bókuð í fjárhag. Þeir stjórna einnig hegðun greiðsluúttaksins. Venjulega er einn greiðslumáti búinn til fyrir hverja greiðslu sem fyrirtækið samþykkir (til dæmis reiðufé, ávísun, kreditkort, peningapöntun og símgreiðslu).

Reitirnir í hlutanum **Bókun** í flýtiflipanum **Almennt** stjórna því hvernig greiðsla er bókuð í fjárhaginn. Fyrst þarf að velja gildi í reitnum **Gerð lykils**. Gerð lykils sem þú velur stjórnar hegðuninni í reitnum **Greiðslulykill**. Við mælum með því að þú veljir **Banki** í reitnum **Gerð lykils** og veljir svo bankareikninginn í reitnum **Greiðslulykill**. Ávinningur af þessari aðferð er að kerfið mun bóka greiðsluna í undirbók bankans, sem styður afstemmingu og önnur ferli sem tengjast reiðufé. Eftirfarandi tafla sýnir dæmi um skilgreiningu á bókunarreglu ef þú ert að nota eininguna **Reiðufjár- og bankastjórnun**.

| Bókunargerð | Lykilgerð | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Banki | Banki | Bank of Contoso | Bankareikningur sem tengist eign | Kredit | Nr. | Sláðu inn aðallykilinn í reitinn **Greiðslulykill** fyrir hvern greiðslumáta. |

Ef þú hyggst ekki nota reiðufjár- og bankastjórnun ættirðu að velja **Fjárhag** í reitnum **Gerð lykils** og síðan velja aðallykilinn í reitnum **Greiðslulykill**. Eftirfarandi tafla sýnir dæmi um skilgreiningu á bókunarreglu ef þú ert ekki að nota reiðufjár- og bankastjórnun.

| Bókunargerð | Lykilgerð | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Fjárhagur | Fjárhagur | 100100: Bank of Contoso | Eign | Kredit | Nr. | Sláðu inn aðallykilinn í reitinn **Greiðslulykill** fyrir hvern greiðslumáta. |

## <a name="bridging-accounts"></a>Millilyklar

Millibókun er tveggja skrefa ferli sem er notað þegar greiðslur eru bókaðar. Þetta er valfrjáls eiginleiki sem hægt er að nota með til dæmis núlljöfnuði á bankareikningum. Það getur hjálpað til við að tryggja einfaldari og tímanlega bankaafstemmingu. Í fyrsta skrefinu er greiðsla lögð inn á tímabundinn reikning (millilykil). Í öðru skrefinu er bókaða færslan bakfærð og bókuð á bankareikninginn þegar greiðslan er samþykkt af bankanum. Eftirfarandi tafla sýnir dæmi um skilgreiningu á bókunarreglu fyrir millibókun.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Færslubók fjárhags | 130725 | Óafstemmt reiðufé | Bótaábyrgð | Debet | Já | Sláðu inn aðallykilinn í reitinn **Millilykill** fyrir hvern greiðslumáta. |

Nánari upplýsingar um það eru í [Uppsetning og vinnsla greiðslna á millilykli](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="posting-accounts-for-customer-cash-discounts"></a>Bókunarlyklar fyrir staðgreiðsluafslætti viðskiptavinar

Ef fyrirtækið býður viðskiptavinum staðgreiðsluafslætti til að fá greiðslur á fljótlegri hátt þarf að skilgreina kóða staðgreiðsluafsláttar og tilgreina hvernig afslættir eigi að vera bókaðir í fjárhaginn. Nokkrir valkostir eru í boði til að tilgreina aðallykilinn sem er notaður til að bóka staðgreiðsluafslátt viðskiptavinar.

Sjá [Staðgreiðsluafslættir](../cash-bank-management/cash-discounts.md) fyrir frekari upplýsingar.

## <a name="posting-accounts-for-payment-fees"></a>Bókunarlyklar fyrir greiðsluþóknanir

Greiðsluþóknanir gera þér kleift að bæta þóknun sjálfkrafa við greiðslu viðskiptavinar þegar safn skilyrða er uppfyllt. Hægt er að innheimta greiðsluþóknanir af viðskiptavini eða bóka þær á bankareikning sem kostnað. Hér eru nokkur dæmi:

- Þú rukkar viðskiptavini um 3 prósent af heildargreiðslunni ef þeir greiða með kreditkorti.
- Bankinn þinn rukkar þig um $ 1,00 fyrir hverja millifærslu sem þú vinnur úr og millifærslugjaldið er kostnaður.

Þegar greiðsluþóknun viðskiptavinar er skilgreind, ef reiturinn **Gjald** er stilltur á **Viðskiptavinur**, verður reiturinn **Aðallykill** óaðgengilegur og kerfið notar bókunarreglu viðskiptavinar til að bóka þóknunina. Ef þú stillir reitinn **Gjald** á **Fjárhagur** verður þú að stilla reitinn **Aðallykill** á aðallykilinn þar sem greiðsluþóknunin verður bókuð. Venjulega er þessi aðallykill kostnaðarlykill. Eftirfarandi tafla sýnir dæmi um skilgreiningu á bókunarreglu fyrir bókun´ greiðsluþóknunar.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Færslubók fjárhags | 618190 | Kostnaður bankagjalds | Kostnaður | Debet | Nr. |  Ef **Fjárhagur** er valið í reitnum **Gjald** skal velja þennan lykil í reitnum **Aðallykill** fyrir greiðsluþóknunina. |

Nánari upplýsingar er að finna í [Koma á fót greiðsluþóknunum viðskiptavina](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Bókun reikninga fyrir gjaldakóða

Ef rekja þarf söluupphæðir ásamt línuatriðum er hægt að nota gjaldakóða. Til dæmis gætir þú innheimt farm- og umsýslugjöld hjá viðskiptavini eða lagt á farm- og umsýslugjöld innanhúss. Þá er hægt að tilgreina hvort upphæðin er birt á kostnaðarreikningum eða bætt við kostnað varanna.

Þú getur búið til skuldfærslukóða fyrir Viðskiptakröfur og Viðskiptaskuldir. Þegar gjaldakóði er skilgreindur verður að skilgreina færsluna. Bókunin stjórnar bæði debetlyklinum og kreditlyklinum. Fyrir hvern gjaldakóða sem er stofnaður er hægt að velja bókunargerðina sem er notuð. Eftirfarandi tafla sýnir dæmi um gjaldkóða fyrir viðskiptakröfur.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Greiðsluþóknun | 411400 | Tekjur – Gjöld | Tekjur | Kredit | Nr. | **Dæmi um ónóga sjóði:** Debetfærsla viðskiptavinar/lánardrottins og kreditfjárhagslykill. |
| Pöntun, farmur | 403500 | Tekjur – Farmur | Tekjur | Kredit | Nr. | **Dæmi um farm sem viðskiptavinur er rukkaður um:** Debetfærsla viðskiptavinar/lánardrottins og kreditfjárhagslykill |
| Eftirágreiddur afsláttur\* | 403200 | Afsláttur | Tekjur | Debet | Nr. | **Dæmi um eftirágreiddan afslátt viðskiptavinar:** Debetfjárhagslykill og kreditfærsla viðskiptavinar/lánardrottins |

\* Fyrir eftirágreiddan afslátt til dæmis er bókunin aðeins notuð þegar skuldfærslukóða er bætt við innkaupapöntunarhaus eða línu. Ítarlegri virkni fyrir eftirágreiddan afslátt sem er í boði í Microsoft Dynamics 365 Supply Chain Management veitir meiri stjórn og sjálfvirkni fyrir eftirágreiddan afslátt. Frekari upplýsingar er að finna í [Eftirágreiddir afslættir viðskiptavinar](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

Fyrri taflan sýnir þrjú dæmigerð dæmi um bókunargerðir sem hægt er að nota fyrir gjaldkóða. Það ætti að nota sem leiðbeiningar og sýnishorn. Ekki er lagður til tæmandi lista yfir allar mögulegar samsetningar eða bókunargerðir sem hægt er að nota.

Nánari upplýsingar má finna í [Stofna gjaldakóða](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Bókunarlyklar fyrir þóknanir

Þú getur stillt kerfið til að reikna út þóknun fyrir sölufulltrúa eða hóp sölufulltrúa á tiltekinni sölupöntun. Ef þessi aðgerð er virkjuð þarf að skilgreina bókunarlykilinn sem er notaður til að reikna út þóknunina. Þessi skilgreining er gerð á síðunni **Bókun þóknunar** í einingunni **Sala og markaðssetning**.

Frekari upplýsingar er að finna í [Setja upp reglur um söluþóknun](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md).

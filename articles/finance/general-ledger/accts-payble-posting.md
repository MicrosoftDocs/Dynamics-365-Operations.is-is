---
title: Bókanir viðskiptaskulda
description: Þessi grein útskýrir hvernig færslur eru stilltar í Viðskiptaskuldir og gefur dæmi um bókunarstillingar.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908010"
---
# <a name="accounts-payable-posting"></a>Bókun lánardrottnalykils

[!include [banner](../includes/banner.md)]

Aðal færslusniðið fyrir **Viðskiptaskuldir** mát er færslusnið söluaðila. Þetta bókunarsnið ákvarðar yfirlitsreikninginn sem er notaður þegar innstæður lánardrottins eru bókaðar í fjárhag. Yfirlitsreikningur er aðalreikningur. Það er einnig nefnt viðskiptareikningur viðskiptaskulda.

Fyrir frekari upplýsingar, sjá [Birtingasnið söluaðila](../accounts-payable/vendor-posting-profiles.md).

Nokkrar bókunarstillingar fyrir utan bókunarsnið lánardrottins eru fáanlegar í Viðskiptaskuldir. Eftirfarandi hlutar veita frekari upplýsingar um þessar aðrar birtingarstillingar.

## <a name="methods-of-payment-posting-accounts"></a>Aðferðir við greiðslubókun reikninga

Greiðsluaðferðir skilgreina hvernig greiðsla verður bókuð í fjárhag. Þeir stjórna einnig hegðun greiðsluúttaksins. Venjulega er ein greiðslumáti búin til fyrir hverja tegund greiðslu sem fyrirtæki þitt gerir (til dæmis reiðufé, ávísun, kreditkort, peningapöntun og vír).

Reitirnir í **Birting** kafla um **Almennt** Flýtiflipi á **Greiðslumáti** síða (**Viðskiptaskuldir > Greiðsluuppsetning > Greiðslumátar**) stjórna því hvernig greiðsla verður bókuð í fjárhag. Þú verður fyrst að velja gildi í **Tegund reiknings** sviði. Reikningstegundin sem þú velur stjórnar hegðun reikningsins **Greiðslureikningur** sviði. Við mælum með að þú veljir **Banki** í **Tegund reiknings** reitnum og veldu síðan bankareikninginn í **Greiðslureikningur** sviði. Ávinningurinn af nálguninni er að kerfið mun bóka greiðsluna í undirbók bankans, sem styður afstemmingu og önnur reiðufjártengd ferli. Eftirfarandi tafla sýnir dæmi um uppsetningu póstsniðs ef þú ert að nota **Handbært fé og bankastjórnun** mát.

| Bókunargerð | Lykilgerð | Dæmi um nafn greiðslureiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Banki | Banki | Bank of America | Bankareikningur sem er tengdur við eign | Debet | Nr. | Fyrir hvern greiðslumáta skaltu slá inn aðalreikninginn í **Greiðslureikningur** sviði. |

Ef þú ætlar ekki að nota reiðufé og bankastjórnun ættir þú að velja **Fjárhagsbók** í **Tegund reiknings** reitnum og veldu síðan aðalreikninginn í **Greiðslureikningur** sviði. Eftirfarandi tafla sýnir dæmi um uppsetningu birtingarsniðs ef þú ert það **ekki** með því að nota reiðufé og bankastjórnun.

| Bókunargerð | Lykilgerð |Dæmi um greiðslureikning | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Fjárhagur | Fjárhagur | 100100: Bank of America | Eign | Debet | Nr. | Fyrir hvern greiðslumáta skaltu slá inn aðalreikninginn í **Greiðslureikningur** sviði. |

## <a name="bridging-accounts"></a>Brúarreikningar

Brúarbókun er tveggja þrepa ferli sem er notað þegar greiðslur eru bókaðar. Það er valfrjáls eiginleiki sem hægt er að nota með bankareikningum með núllstöðu, til dæmis. Það getur hjálpað til við að tryggja sléttara og tímanlegra bankaafstemmingarferli. Í fyrsta skrefi er greiðsla bókuð á tímabundinn reikning (brúarreikninginn). Í öðru skrefi er bókað færslan bakfærð og færð inn á bankareikninginn þegar greiðslan hreinsar bankann. Eftirfarandi tafla sýnir dæmi um uppsetningu bókunarsniðs fyrir brúarfærslu.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Færslubók fjárhags | 130725 | Óafgreidd reiðufé | Bótaábyrgð | Debet | Já | Fyrir hvern greiðslumáta skaltu slá inn aðalreikninginn í **Brúarreikningur** sviði. |

Fyrir frekari upplýsingar, sjá [Setja upp og vinna úr brúuðum greiðslum](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="customer-cash-discounts-posting-accounts"></a>Viðskiptavinur staðgreiðsluafsláttur bókun reikninga

Ef fyrirtæki þitt fær staðgreiðsluafslátt frá lánardrottnum í staðinn fyrir skjóta greiðslu, verður þú að stilla staðgreiðsluafsláttarkóða og tilgreina hvernig afslættir eigi að bóka í fjárhag. Nokkrir valkostir eru í boði til að tilgreina aðalreikninginn sem er notaður til að bóka staðgreiðsluafslátt viðskiptavinar.

Fyrir frekari upplýsingar, sjá [Staðgreiðsluafsláttur](../cash-bank-management/cash-discounts.md).

## <a name="payment-fee-posting-accounts"></a>Bókunarreikningar greiðslugjalds

Greiðslugjöld gera þér kleift að bæta gjaldi sjálfkrafa við greiðslu lánardrottins þegar sett skilyrði eiga við. Hægt er að greiða greiðslugjöld til seljanda, eða þau geta verið færð á bankareikning þinn sem kostnað. Hér eru nokkur dæmi:

- Seljandi rukkar þig um 3 prósent af heildargreiðslunni ef þú borgar með kreditkorti.
- Bankinn þinn rukkar þig $1.00 fyrir hverja millifærslu sem þú framkvæmir og gjaldfært er fyrir símgreiðsluna.

Þegar þú stillir greiðslugjald lánardrottins, ef þú stillir á **Hleðsla** sviði til **Seljandi**, hinn **Aðalreikningur** reiturinn verður ekki tiltækur og kerfið notar bókunarsnið lánardrottins til að bóka gjaldið. Ef þú stillir **Hleðsla** sviði til **Fjárhagsbók**, þú verður að stilla **Aðalreikningur** reit inn á aðalreikning þar sem greiðslugjaldið verður bókað. Venjulega mun þessi aðalreikningur vera kostnaðarreikningur. Eftirfarandi tafla sýnir dæmi um uppsetningu bókunarsniðs fyrir bókun greiðslugjalda.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Færslubók fjárhags | 618190 | Bankagjaldskostnaður | Kostnaður | Debet | Nr. | Ef **Fjárhagsbók** er valið í **Hleðsla** reit, veldu þennan reikning í **Aðalreikningur** sviði á **Greiðslugjald** síðu. |

Nánari upplýsingar er að finna í [Skilgreina greiðsluþóknanir lánardrottna](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Gjaldkóðabókunarreikningar

Ef þú verður að fylgjast með innkaupaupphæðum til viðbótar við línuvörur geturðu notað gjaldakóða. Til dæmis gæti birgir þinn rukkað vöruflutninga- og afgreiðslugjöld af þér, eða það gæti kostað nokkur vöru- og afgreiðslugjöld innanhúss. Hægt er að tilgreina hvort þessar upphæðir séu bókaðar á kostnaðarreikninga eða bætt við kostnað hlutanna.

Þú getur búið til gjaldakóða fyrir Viðskiptakröfur og Viðskiptaskuldir. Þegar þú stillir gjaldkóða verður þú að skilgreina bókunina. Bókunin stjórnar bæði debetreikningi og kreditreikningi. Þegar þú býrð til gjaldakóða geturðu valið bókunartegundina sem er notuð fyrir hvern gjaldkóða. Eftirfarandi tafla sýnir dæmi um dæmigerða gjaldkóða fyrir Viðskiptaskuldir á **Gjaldkóðar** síðu.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Innkaupagjöld | Hafið svæðið autt. | Á ekki við | Atriði | Debet | Nr. | **Dæmi um kaupgjald fyrir vöru:** </p><ul><li>**Debettegund** reit =**Atriði**</li><li>  **Kredittegund** reit =**Viðskiptavinur/seljandi**.</li><li> Vörubókunin notar aðalreikninginn úr birgðabókunarsniðinu. |
| Pöntun, farmur | 600120 | Senda inn | Tekjur | Debet | Nr. | **Dæmi um vöruflutninga sem greiddur er til seljanda:** </p><ul><li>**Debettegund** reit =**Fjárhagsreikningur**</li><li> **Kredittegund** reit =**Viðskiptavinur/seljandi** |
| Eftirágreiddur afsláttur\* | 503160 | Söluafsláttur (Contra COGS)| Kostnaður | Kredit | Nr. | **Dæmi um afslátt frá seljanda:**</p><ul><li>**Debettegund** reit =**Viðskiptavinur/seljandi**</li><li>**Kredittegund** reit =**Fjárhagsreikningur** |

\* Fyrir afsláttardæmið er bókunin aðeins notuð þegar gjaldkóða er bætt við innkaupapöntunarhaus eða línu. Háþróuð afsláttarvirkni sem er fáanleg í Microsoft Dynamics 365 Supply Chain Management veitir meiri stjórn og sjálfvirkni á afslætti. Fyrir frekari upplýsingar, sjá [Afsláttur söluaðila](../../supply-chain//procurement/vendor-rebates.md).

Taflan á undan sýnir þrjú dæmigerð dæmi um bókunargerðir sem hægt er að nota fyrir gjaldkóða. Það ætti að nota sem leiðbeiningar og úrval sýnishorna. Það veitir ekki tæmandi lista yfir allar mögulegar samsetningar eða birtingargerðir sem hægt er að nota.

Fyrir frekari upplýsingar, sjá [Búðu til gjaldkóða](../accounts-receivable/create-charges-codes.md).

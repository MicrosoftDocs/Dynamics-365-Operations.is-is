---
title: Villuelita innhreyfingarskjöl og reikningsfærslur
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innhreyfingarskjöl og reikningsfærslur.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89effb686d60dde9d11f99be51d4101897ad4ea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430758"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Villuelita innhreyfingarskjöl og reikningsfærslur

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innhreyfingarskjöl og reikningsfærslur.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Ég get ekki bókað meira en einn reikning fyrir innkaupapöntunarlínu sem er með vörur flokkaðar eftir tegund.

Magn er áskilið ef bóka á reikninga. Ef fullt magn línu hefur verið reikningsfært fyrir aðeins hluta af upphæð, geturðu þar af leiðandi ekki reikningsfært eftirstandandi upphæð á öðrum reikningi.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Ég fæ upp villuna „Tilvísun hlutar ekki stillt“ við staðfestingu á innkaupapöntun, eða undantekningin „Exception has been thrown by the target of an invocation“ kemur upp við bókun lánardrottnareiknings.

Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.

Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Ég get ekki sameinað mörg innhreyfingarskjöl í eina innkaupapöntun.

Ekki er hægt að sameina mörg innhreyfingarskjöl í eina innkaupapöntun ef mismunandi línur innhreyfingarskjals eru með mismunandi dagsetningar reikningsskila.

Í fyrri útgáfum af Microsoft Dynamics 365 Supply Chain Management var sameining leyfð í þessum aðstæðum. Hins vegar komu oft upp villur þegar það var gert. Dagsetning reikningsskila á innkaupapöntunarlínunum sem eru stofnaðar ættu ekki að vera frábrugðnar dagsetningu reikningsskila í línum innhreyfingarskjals sem þessar innkaupapöntunarlínur voru stofnaðar úr. (Dagsetning reikningsskila á innkaupapöntunarlínum samsvarar dagsetningu reikningsskila í haus innkaupapöntunarinnar.) Þess vegna er sameining margra innhreyfingarskjala í eina innkaupapöntun ekki lengur leyfð.

Dagsetning reikningsskila er notuð, til dæmis fyrir frátektir fjárhagsáætlunar og fjárúthlutunar. Því ætti að halda henni við umbreytingu úr innhreyfingarskjali í innkaupapöntun.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Þegar hætt er við innhreyfingarskjöl er hægt að bóka færslur á frestaðan fjárhagslykil.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef hætt er við innhreyfingarskjal, gerir kerfið kleift að bóka færslur á frestaða fjárhagslykla jafnvel þótt aðallyklum sé frestað.

### <a name="reproduce-the-issue"></a>Framkallaðu vandamálið

Eftirfarandi ferli sýnir eina leið til að endurtaka málið.

1. Á síðunni **Færibreytur viðskiptaskulda**, í flipanum **Almennt**, skal ganga úr skugga um að valkosturinn **Bóka innhreyfingarskjal afurða í fjárhag** sé stilltur á *Já*.
1. Stofnið innkaupapöntun og bætið við pöntunarlínu sem er með magnið *1000* fyrir afurð.
1. Staðfesta innkaupapöntun.
1. Bókið innhreyfingarskjalið og athugið fylgiskjölin.
1. Frestið viðkomandi aðallyklum, *200140* og *140200*.
1. Hættið við bókað innhreyfingarskjal afurðar.
1. Takið eftir að hægt er að bóka færslur á frestaða fjárhagslykla.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Hægt er að bóka færslur á frestaða fjárhagslykla þegar hætt er við innhreyfingarskjöl vegna þess að þessi hegðun leyfir réttar bókanir.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Fylgiskjalsnúmer innhreyfingarskjals er notað þótt ekkert fjárhagsskjal sé búið til við móttöku afurðar.

Ef valkosturinn **Safna upp skuld á innhreyfingarskjali** er stilltur á *Nei* fyrir vörulíkanaflokkinn, munu engar bókanir á fjárhagnum eiga sér stað. Efnislegt tilvik verður hins vegar skráð af bókhaldsástæðum í undirbók og þetta tilvik þarf fylgiskjalsnúmer. Þetta fylgiskjalsnúmer er það fylgiskjalsnúmer sem vísað er til í birgðafærslum.

Mælt er með því að valkosturinn **Safna upp skuld á innhreyfingarskjali** sé stilltur á *Já* eins og lýst er í eftirfarandi bloggfærslu: [Bóka ýmis gjöld þegar afurð er móttekin](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Ekki er kveikt á stillingunni Bóka á gjaldalykil í fjárhag.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál á sér stað þegar innkaupapöntun er reikningsfærð, ef valkosturinn **Bóka á gjaldalykil í fjárhag** er stilltur á *Já* í flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda**.

### <a name="reproduce-the-issue"></a>Framkallaðu vandamálið

Eftirfarandi ferli sýnir eina leið til að endurtaka málið.

1. Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.
1. Í flipanum **Reikningur** skal stilla valkostinn **Bóka á gjaldalykil í fjárhag** á *Já*.
1. Opnið **Birgðastjórnun \> Uppsetning \> Bókun \> Bókun**.
1. Í flipanum **Innkaupapöntun** skal ganga úr skugga um að öllum línum hafi verið eytt í útgjöldum innkaupa fyrir afurðina.
1. Opnið **Viðskiptaskuldir \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Stofna innkaupapöntun. Í reitnum **Lánardrottnalykill** skal velja *1001 Acme Skrifstofuvörur*.
1. Bætið við innpöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *D0011 Leysiprentari*
    - **Svæði:** *1*
    - **Vöruhús:** *11*
    - **Magn:** *4*

1. Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Aðgerð**, skal velja **Staðfesta**.
1. Á aðgerðasvæðinu, í flipanum **Móttaka**, í flokknum **Mynda**, skal velja **Innhreyfingarskjal afurðar**.
1. Í svargluggannn **Bókun innhreyfingarskjals afurða**, í reitinn **Innhreyfingarskjal**, skal færa inn handahófskennt númer og velja síðan **Í lagi**.
1. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
1. Í reitinn **Númer** skal færa inn handahófskennt númer sem reikningsnúmerið.
1. Uppfærið samsvörunarstöðuna og bókið.
1. Takið eftir því að nú kemur upp eftirfarandi villa þegar reikningur er búinn til úr innkaupapöntun: „Númer lykils fyrir færslugerðin Útgjöld innkaupa fyrir afurð er ekki til.“

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þetta fer eftir færibreytustillingunum fyrir reikninga og reikningaflokka. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Bókhald fyrir Útgjöld innkaupa og Afbrigði birgða](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).

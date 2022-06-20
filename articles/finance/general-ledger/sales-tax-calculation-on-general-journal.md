---
title: VSK-útreikningur í almennum færslubókarlínum
description: Þessi grein útskýrir hvernig söluskattar eru reiknaðir fyrir mismunandi gerðir reikninga (lánardrottins, viðskiptamanns, fjárhagsbókar og verks) á færslubókarlínum.
author: EricWangChen
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: a73e145dd26e930c860e9ea31d7dab4f1593c2a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845288"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>VSK-útreikningur í almennum færslubókarlínum
[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig söluskattar eru reiknaðir fyrir mismunandi gerðir reikninga (lánardrottins, viðskiptamanns, fjárhagsbókar og verks) á færslubókarlínum.

Skipta má ferlinu í þrjú skref:

- Ákvarðið stefnu VSK-skatts.

- Ákvarðið VSK-skattupphæð sem verður geymd í tímabundinni VSK-skattatöflu.

- Ákvarðið VSK-skattupphæð og lykil á fylgiskjalið.

## <a name="determine-the-sales-tax-direction"></a>Ákvarðið stefnu VSK-skatts

Hvernig stefna VSK-skatts er ákvörðuð fer eftir gerð lykils í fylgiskjalinu. Stefna VSK-skatts ræðst af samsetningu gerð lykils og VSK-kóða. Eftirfarandi hlutar fjalla nánar um valkostina. 

### <a name="account-type-is-project"></a>Lykilgerðin er Verk

Ef fylgiskjalið er með færslubókarlínu þar sem lykilgerðin er **Verk** beita allar færslubókarlínur í fylgiskjalinu sömu skattastefnu. Eftirfarandi mynd sýnir regluna. Eftirfarandi atriði sýna hugsanlegar skattaleiðbeiningar fyrir verklykla.

•   Ef VSK-skattsnúmerið er neysluskattur, þá er VSK-skattsstefnan Neysluskattur.

•   Ef VSK-skattsnúmerið er undanþegið skatti, þá er VSK-skattsstefnan Innkaup án skatts.

•   Ef VSK-skattsnúmerið er VSK á milli fyrirtækja, þá er VSK-skattsstefnan Útskattur.

•   Ef VSK-skattsnúmerið er bakfært gjald, þá er VSK-skattsstefnan Útskattur.

Annars er stefna VSK-skatts Innskattur.

Eftirfarandi skýringarmynd sýnir regluna myndrænt.

![Möguleikar á skattastefnu vegna verklykla.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Lykilgerðin er Lánardrottinn

Ef fylgiskjalið er með færslubókarlínu þar sem lykilgerðin er **Lánardrottinn** beita allar færslubókarlínur í fylgiskjalinu sömu skattastefnu. Eftirfarandi atriði sýna hugsanlegar skattaleiðbeiningar fyrir lánardrottnalykla. 

•   Ef VSK-skattsnúmerið er neysluskattur, þá er VSK-skattsstefnan Neysluskattur.

•   Ef VSK-skattsnúmerið er undanþegið skatti, þá er VSK-skattsstefnan Innkaup án skatts.

•   Ef VSK-skattsnúmerið er VSK á milli fyrirtækja, þá er VSK-skattsstefnan Útskattur.

•   Ef VSK-skattsnúmerið er bakfært gjald, þá er VSK-skattsstefnan Útskattur.

Annars er stefna VSK-skatts Innskattur.

Eftirfarandi skýringarmynd sýnir regluna myndrænt.

![Möguleikar á skattastefnu vegna lánardrottnalykla.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Lykilgerðin er Viðskiptavinur

Ef fylgiskjal hefur færslubókarlínu þar sem reikningsgerðin er **Viðskiptavinur**, allar færslubókarlínur í fylgiskjalinu gilda í sömu skattstefnu. 

Ef söluskattskóðinn er undanþeginn skatti, þá er söluskattsstefna Tax Free Sale. Annars er stefna VSK-skatts Útskattur.

### <a name="account-type-is-ledger"></a>Lykilgerðin er Fjárhagur

Eftirfarandi mynd sýnir regluna sem gildir þegar fylgiskjalið hefur aðeins dagbókarlínur þar sem gerð lykilsins er **Fjárhagur**. Eftirfarandi atriði sýna hugsanlegar skattaleiðbeiningar fyrir fjárhagslykla.

•   Ef VSK-skattsnúmerið er neysluskattur, þá er VSK-skattsstefnan Neysluskattur.

•   Ef VSK-skattsnúmerið er undanþegið skatti, þá er VSK-skattsstefnan Innkaup án skatts.

Annars, ef dagbókarupphæðin er debet (jákvæð), er VSK-skattsstefna Innskattur; ef dagbókarupphæðin er kredit (neikvæð), þá er VSK-skattsstefna Útskattur.

Eftirfarandi skýringarmynd sýnir regluna myndrænt.

![Möguleikar á skattastefnu vegna fjárhagslykla.](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Hnekkið stefnu VSK-skatts

Þú getur hnekkt stefnu VSK-skatts þegar fylgiskjalið inniheldur aðeins línur þar sem gerð reikningsins er **Fjárhagur**.

Farðu í **Fjárhag \> Bókhaldslykil \> Lyklar \> Aðallyklar** og veldu flýtiflipann **Lögaðili hnekkir**.

## <a name="determine-the-sales-tax-amount"></a>Ákvarðið upphæð VSK-skatts

Í þessum kafla er lýst hvernig VSK-skattsupphæðartákn er reiknað.

![Síða virðisaukaskattsfærslna.](media/sales-tax-amount-sign.jpg)

Eftirfarandi tafla sýnir almennu regluna til að ákvarða stefnu VSK og merki VSK-upphæða í tímabundinni töflu virðisaukaskatts.

| Upphæð færslubókarlínu | Stefna VSK  | Merki VSK-skattupphæðar |
|---------------------|----------------------|-----------------------|
| Jákvætt            | Innskattur | Jákvætt              |
| Jákvætt            | Útskattur    | Neikvætt              |
| Neikvætt            | Innskattur | Neikvætt              |
| Neikvætt            | Útskattur    | Jákvætt              |

Það er sérstök regla fyrir fylgiskjöl sem hafa aðeins línurnar **Verk** eða **Fjárhagur**, þegar VSK-skattshópur eða VSK-skattshópur vöru er valinn á línunni **Fjárhagur**. Þessari reglu er stjórnað af eiginleikanum **Virkja sjálfstæðan útreikning á VSK-skatti fyrir almennar færslubækur**. Þegar slökkt er á þessari aðgerð notar skattafjárhæðin í línunni **Fjárhagur** stefnuna debet/kredit í línunni **Verk**. Þegar kveikt er á þessari aðgerð notar skattafjárhæðin í línunni **Fjárhagur** sína eigin debet-/kreditstefnu. Eftirfarandi töflur sýna regluna fyrir hverja atburðarás. 

**Regla þegar kveikt er á eiginleikanum**

| Færslubókarlínuupphæð verks | Stefna VSK  | Merki VSK-skattupphæðar |
|--------------------------------|----------------------|-----------------------|
| Jákvætt                       | Innskattur | Jákvætt              |
| Neikvætt                       | Innskattur | Neikvætt              |

**Regla þegar slökkt er á eiginleikanum**

| Færslubókarlínuupphæð fjárhags  | Stefna VSK  | Merki VSK-skattupphæðar |
|--------------------------------|----------------------|-----------------------|
| Jákvætt                       | Innskattur | Jákvætt              |
| Neikvætt                       | Innskattur | Neikvætt              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>Ákvarðið VSK-skattupphæð og lykil á fylgiskjalið

Þegar þú bókar VSK-skatt er aðallykillinn sóttur úr forstillingum fjárhagsbókunarflokks. Þegar VSK-skattar eru innskattur notar kerfið innskattslykil sem er tilgreindur í forstillingunum. Fyrir VSK-skatt sem er útskattur notar kerfið útskattslykil sem er tilgreindur í forstillingunum.

Eftirfarandi tafla sýnir almennu regluna.

| Stefna VSK  | Merki VSK-skattupphæðar | VSK-lykill      | Upphæð á fylgiskjali |
|----------------------|-----------------------|------------------------|-------------------|
| Innskattur | Jákvætt              | Viðskiptakröfulykill | Jákvætt (debet)  |
| Innskattur | Neikvætt              | Viðskiptakröfulykill | Neikvætt (kredit)  |
| Útskattur    | Jákvætt              | Viðskiptaskuldalykill    | Neikvætt (kredit)  |
| Útskattur    | Neikvætt              | Viðskiptaskuldalykill    | Jákvætt (debet)  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

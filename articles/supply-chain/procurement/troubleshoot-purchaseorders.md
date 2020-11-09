---
title: Villuleita innkaupapantanir
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innkaupapantanir.
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
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018561"
---
# <a name="troubleshoot-purchase-orders"></a>Villuleita innkaupapantanir

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innkaupapantanir.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>Aðeins er hægt að ljúka aðgerð eftir að línunúmeri er að fullu dreift.

Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.

Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Þegar innkaupapantanir eru fluttar inn í gegnum gagnastjórnun, fylgja númer innkaupapöntunarlínu ekki hækkun sem er skilgreint í kerfisfæribreytum.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Sjálfgefið er að línunúmer sem eru búin til sjálfkrafa fyrir innkaupapöntunarlínur sem eru fluttar inn í gegnum gagnaeininguna *Innkaupapöntunarlínur V2* noti ekki línunúmerahækkun kerfisins sem er tilgreind í kerfisfæribreytum. Ef innkaupapöntun er búin til handvirkt og línum bætt við í gegnum notandaviðmótið, hækka línunúmerin á réttan hátt. Hins vegar ef gagnastjórnunarramminn (DMF) er notaður, hækka þau ekki á réttan hátt.

Þetta vandamál á sér stað vegna þess að þegar innflutningslínur eru fluttar inn í gegnum DMF, ef línunúmerum hefur ekki þegar verið úthlutað á innflutta einingu, notar kerfið DMF-aðferð til að úthluta þeim. Línunúmer hækka alltaf um einn með þessari aðferð.

### <a name="issue-workaround"></a>Lausn á vandamálinu

Gangið úr skugga um að æskileg línunúmer séu þegar gefin upp í línunúmerareitum gagnaeiningarinnar þegar innkaupapöntunarlínurnar eru fluttar inn. Í þessu tilfelli skrifar DMF ekki yfir línunúmerin.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Sjálfgefinn skattflokkur og sjálfgefinn staðgreiðsluafsláttur eru ekki fyllt út í reikningslyklinum.

Ef reikningslykill er notaður sem er frábrugðinn lykli viðskiptavinar, er ekki fyllt út í sjálfgefinn skattflokk og sjálfgefinn staðgreiðsluafslátt í reikningslyklinum þegar innkaupapöntun er búin til.

Þessi hegðun er samkvæmt hönnuninni. Sjálfgefin gildi fyrir skattflokkinn, staðgreiðsluafslætti og aðrar verðupplýsingar byggja á viðskiptavinalyklinum, ekki reikningslyklinum.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Ég fæ upp villuna „Tilvísun hlutar ekki stillt“ við staðfestingu á innkaupapöntun, eða undantekningin „Exception has been thrown by the target of an invocation“ kemur upp við bókun lánardrottnareiknings.

Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.

Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Ein eða fleiri dreifingar á fjárhagsupphæð eru annaðhvort yfir- eða undirdreifðar.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Eftirfarandi villa kemur upp: „Ein eða fleiri dreifingar á fjárhagsupphæð er annaðhvort yfir- eða undirdreifðar.“

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.

Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Get ég birt aðeins innkaupapantanir sem ég stofnaði?

Þessi virkni er ekki tiltæk sem stendur.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Get ég tekið frá birgðir og stofnað færslur á móti skráðum birgðum í innkaupapöntun?

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Jafnvel þegar vörur eru með stöðuna *Skráð* í innkaupapöntun, er enn hægt að taka frá birgðirnar. Með öðrum orðum er hægt að stofna færslur gagnvart skráðum birgðum.

### <a name="reproduce-the-issue"></a>Framkallaðu vandamálið

Eftirfarandi ferli sýnir eina leið til að endurtaka málið.

1. Stofna innkaupapöntun.
2. Skráið innkaupapöntunarlínuna.
3. Takið eftir því að hægt er að mynda frátekningar og færslur gagnvart skráðum birgðum.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessi hegðun er samkvæmt hönnuninni. Væntingin er sú að skráðar vörur séu efnislega komnar í vöruhúsið eða birgðirnar og að hægt sé þar af leiðandi að taka þær frá.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Innkaupapantanir endurspegla ekki tungumálastillingar lögaðilans.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Afurðarheitið á innkaupapöntun er sýnt á tungumáli kerfisins í staðinn fyrir tungumálið sem er stillt fyrir lögaðilann þar sem innkaupapöntunin var búin til.

### <a name="reproduce-the-issue"></a>Framkallaðu vandamálið

Eftirfarandi ferli sýnir eina leið til að endurtaka málið.

1. Stillið kerfistungumálið á *EN-US* (bandaríska ensku).
1. Gangið úr skugga um að það sé til afurð þar sem tungumálin *EN-US* og *DE* (þýska) eru notuð fyrir þýðingar á afurðarheiti.
1. Breytið tungumáli fyrir lögaðila í *DE*.
1. Í lögaðilanum þar sem *DE* er stillt sem tungumál skal stofna innkaupapöntun sem inniheldur afurðina.
1. Takið eftir því að afurðarheitið er enn sýnt á bandarískri ensku (kerfistungumálinu).

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessi hegðun er samkvæmt hönnuninni. Í innkaupapöntunum er afurðin alltaf sýnd á tungumáli kerfisins. Tungumál innkaupapantana er notað þegar staðfestingarbók er stofnuð.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>Listi yfir samþykkta lánardrottna eftir afurðareiningu leyfir ekki að gildisdagsetningunni sé breytt.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Afurð er með samþykktan lánardrottin sem er með t.d. gildisdagsetningu 11. janúar 2018 ( *11/01/2018* ), og lokadaginn *Aldrei*. Ef reynt er að breyta gildisdagsetningunni í 10. janúar 2018 ( *10/01/2018* ) eða 12. janúar 2018 ( *12/01/2018* ) kemur upp eftirfarandi villu:

> Ekki tókst að stofna færslu í lista yfir samþykkta birgja (PdsApproveVendorList). Gildið 'Lokadagsetning' þarf að vera stærra en eða jafnt og gildið fyrir ‚Gildisdagsetning‘.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Aðeins er hægt að framlengja tímabilið þar sem lánardrottinn hefur verið samþykktur. Eftirfarandi reglur gilda:

- Til að breyta gildisdagsetningu þannig að hún sé á undan fyrirliggjandi færslum (tímabilum) fyrir lánardrottin vörunnar, verður lokadagur nýja tímabilsins að vera á undan öllum lokadagsetningum í fyrirliggjandi færslum.
- Til að breyta lokadagsetningunni þannig að hún verði síðar en á fyrirliggjandi tímabilum verður gildisdagsetningin að vera á eftir síðustu lokadagsetningunni í fyrirliggjandi færslu.
- Til að draga úr heildartímabilinu sem lánardrottinn hefur verið samþykktur fyrir, þarf að eyða eða breyta fyrirliggjandi færslum. Að öðrum kosti er hægt að nota rofann **stytta** meðan á innflutningi stendur. Þessi rofi eyðir öllum fyrirliggjandi færslum í töflunni fyrir samþykkta lánardrottna eftir vöru.

Fyrir dæmið sem lýst er í útgáfulýsingunni þar sem færsla er með gildisdagsetningu *11/01/2018* og lokadag *Aldrei* , er hægt að flytja inn nýja færslu sem er með gildisdagsetningu *10/01/2018* og lokadagsetningu *Aldrei*. Hins vegar er ekki hægt að stytta tímabilið þannig að gildisdagsetningin uppfærist í *12/01/2018* í gegnum gagnastjórnun. Þú verður að gera þessa breytingu í gegnum notandaviðmótið.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a>Eftir að ég breyti afhendingaraðsetrinu í haus innkaupapöntunar er afhendingarheitið ekki samstillt.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Aðsetrið í haus innkaupapöntunar er uppfært í aðsetur sem er ekki afhendingaraðsetur. Þótt aðsetrið sé uppfært í innkaupapöntuninni er afhendingarheitið ekki uppfært samkvæmt uppfærða aðsetrinu.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessi hegðun er samkvæmt hönnuninni. Valið aðsetur verður að vera flokkað sem afhendingaraðsetur. Að öðrum kosti er afhendingarheitið ekki uppfært út frá völdu aðsetri.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Get ég fundið notandann sem afturkallaði innkaupapöntunina?

Þessar upplýsingar eru aðeins raktar ef innkaupapöntunin fellur undir breytingastjórnun. Ef breytingastjórnun er notuð, er hægt að sjá hver sendi inn breytinguna (afturköllunina) og hver samþykkti hana.

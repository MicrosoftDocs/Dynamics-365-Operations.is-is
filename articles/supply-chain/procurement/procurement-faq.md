---
title: Algengar spurningar um innkaup
description: Þetta efnisatriði veitir svör við algengum spurningum um virkni innkaupa í Supply Chain Management
author: Henrikan
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 99d44f2409d8207ed7a0fb1fc92a99de42240e86
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577193"
---
# <a name="procurement-faq"></a>Algengar spurningar um innkaup

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir svör við algengum spurningum um virkni innkaupa í Supply Chain Management.

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

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Get ég fundið notandann sem afturkallaði innkaupapöntunina?

Þessar upplýsingar eru aðeins raktar ef innkaupapöntunin fellur undir breytingastjórnun. Ef breytingastjórnun er notuð, er hægt að sjá hver sendi inn breytinguna (afturköllunina) og hver samþykkti hana.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Af hverju get ég ekki tengt innkaupsamning við fyrirliggjandi innkaupapöntun?

Innkaupasamningur verður að vera tengdur við innkaupapöntun þegar innkaupapöntunin er stofnuð. Annars er ekki hægt að tengja innkaupapöntunarlínur við innkaupasamningslínur.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Hvaða athugun ræsir skilaboðin „Uppfæra verð og afslætti sem færð voru inn handvirkt eða með ytra skjali“?

Þegar sendingardagsetningu er breytt gætu borist skilaboð þar sem stendur „Uppfæra verð og afslætti sem færð voru inn handvirkt eða með ytra skjali.“ Þessi skilaboð berast vegna þess að ef sendingardagsetningunni hefur verið breytt gæti annar verð- eða sölusamningur verið ræstur og valdið breytingu á verði. Breyting á sendingardagsetningunni getur einnig haft áhrif á vöruhúsaáætlanir og aðrar tengdar upplýsingar.

Skilaboðin eru ræst þegar einhverjum dagsetninganna eða færibreytanna er breytt. Tilgangur skilaboðanna er að ganga úr skugga um að þú gerir þér grein fyrir verðbreytingum sem geta átt sér stað vegna þessara breytinga.

Skilaboðin eru kvaðning um mat á verðsamningi. Ítarlegri lýsingu má finna í [Reglur um mat á verðsamningi](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Af hverju er ekki hægt að bóka meira en einn reikning fyrir innkaupapöntunarlínu sem er með vörur flokkaðar eftir tegund?

Magn er áskilið ef bóka á reikninga. Ef fullt magn línu hefur verið reikningsfært fyrir aðeins hluta af upphæð, geturðu þar af leiðandi ekki reikningsfært eftirstandandi upphæð á öðrum reikningi.

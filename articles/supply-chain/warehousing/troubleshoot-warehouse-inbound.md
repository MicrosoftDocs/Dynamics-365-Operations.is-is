---
title: Úrræðaleit fyrir vöruhúsaaðgerðir á innleið
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsaaðgerðir á innleið i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920988"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Úrræðaleit fyrir vöruhúsaaðgerðir á innleið

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsaaðgerðir á innleið i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Ég fæ eftirfarandi villuskilaboð: „Gæðapöntun %1 var búin til. Klasaprófíll fannst ekki, athuga skal grunnstillinguna.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þessi villuboð tengjast móttökuferli þar sem kveikt er á gæðastjórnun (QMS). Frekari upplýsingar um færsluna sem myndar villuboðin gætu hjálpað við að lagfæra vandamálið, allt eftir skilgreiningum í umhverfinu.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Fyrst skal yfirfara uppsetningu [Klasatiltekt](set-up-cluster-picking.md) og ganga úr skugga um að klasaforstillingar séu rétt uppsettar. Ekki er hægt að nota valmyndaratriði fartækis fyrir klasatiltekt nema klasaforstillingar séu settar upp. Einnig gæti verið nauðsynlegt að fara yfir aðrar tengdar skilgreiningar í samræmi við umhverfinu.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Móttaka blandaðrar númeraplötu virkar ekki fyrir neinn ráðstöfunarkóða fyrir utan Kredit.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar svæðið **Aðgerð** fyrir ráðstöfunarkóða er stillt á *Kredit* eða *Úrkast* er aðeins hægt að nota valmyndina [Móttaka blandaðrar númeraplötu](mixed-license-plate-receiving.md) valmyndaratriði til að vinna úr skilavörum.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika. Sem stendur eru aðeins [ráðstöfunarkóðar](../service-management/set-up-disposition-codes.md) þar sem reiturinn **Aðgerð** er stilltur á *Kredit* eða *Rýrnun* studdir fyrir móttöku blandaðrar númeraplötu.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Þegar reglubundna verkið Uppfæra innhreyfingarskjöl afurða er keyrt eru óstaðfestar innkaupapantanir staðfestar.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar búið er að keyra reglubundna verkið *Uppfæra innhreyfingarskjöl afurða* staðfestir kerfið sjálfkrafa óstaðfestar innkaupapantanir sem eru með birgðafærslustöðu *Skráð*.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Nýr eiginleiki fyrir meðhöndlun á innleið, *Umframmóttaka á hleðslumagni*, lagar þetta vandamál. Til að kveikja á þessum eiginleika skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæðið og kveikja á eftirfarandi eiginleikum (í þeirri röð sem þeir eru sýndir).

1. Tengja birgðafærslur innkaupapöntunar við farm
1. Umframmóttaka á hleðslumagni

Frekari upplýsingar er að finna á [Bóka skráð afurðamagn á móti innkaupapöntunum](inbound-load-handling.md#post-registered-quantities).

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Þegar pantanir á innleið eru skráðar birtast eftirfarandi villuskilaboð: „Magnið er ekki gilt fyrir einingu“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef reiturinn **Regla um flokkun númeraplötu** er stilltur á *Skilgreint af notanda* fyrir valmyndaratriði fartækis sem er notað til að skrá pantanir á innleið, koma upp villuboð („Magnið er ekki gilt“) og ekki verður hægt að ljúka skráningunni.

### <a name="issue-cause"></a>Ástæða vandamáls

Þegar *Skilgreint af notanda* er notað sem regla um flokkun númeraplötu, skiptir kerfið væntanlegum birgðum niður á aðskildar númeraplötur eins og röðunarflokkur einingar gefur til kynna. Ef runu- og raðnúmer eru notuð til að rekja vöruna sem tekið er á móti þarf að tilgreina magn hverrar runu eða raðnúmers fyrir hverja númeraplötu sem er skráð. Ef magnið sem er tilgreint fyrir númeraplötu er umfram magnið sem þarf enn að taka á móti fyrir núverandi víddir, koma upp villuboð.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þegar vara er skráð með því að nota valmyndaratriði fartækis þar sem reiturinn **Regla um flokkun númeraplötu** er stilltur á *Skilgreint af notanda*, gæti kerfið gert kröfu um að númeraplötunúmer, rununúmer eða raðnúmer verði staðfest eða slegin inn.

Á staðfestingarsíðu númeraplötu sýnir kerfið magnið sem er úthlutað fyrir núverandi númeraplötu. Á staðfestingarsíðum rununúmers og raðnúmers sýnir kerfið magnið sem þarf enn að taka á móti á núverandi númeraplötu. Þar verður einnig reitur þar sem hægt er að slá inn magnið til að skrá fyrir þá samsetningu af númeraplötu og runu- eða raðnúmeri. Í þessu tilfelli skal ganga úr skugga um magnið sem verið er að skrá fyrir númeraplötuna fari ekki umfram magnið sem þarf enn að taka á móti.

Ef verið er að búa til of margar númeraplötur við skráningu á pöntun á innleið verður hægt að breyta gildinu í reitnum **Regla um flokkun númeraplötu** í *Flokkun númeraplötu*, hægt verður að úthluta nýjum röðunarflokki einingar á vöruna eða hægt verður að gera valkostinn **Flokkun númeraplötu** fyrir röðunarflokk einingar óvirkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

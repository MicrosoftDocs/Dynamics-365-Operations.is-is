---
title: Úrræðaleit fyrir vöruhúsaaðgerðir á innleið
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsaaðgerðir á innleið i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645973"
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

Nýr eiginleiki fyrir meðhöndlun á innleið, *Umframmóttaka á hleðslumagni*, lagar þetta vandamál. Til að kveikja á þessum eiginleika skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eftirfarandi eiginleikum (í þeirri röð sem þeir eru sýndir).

1. Tengja birgðafærslur innkaupapöntunar við farm
1. Umframmóttaka á hleðslumagni

Frekari upplýsingar er að finna á [Bóka skráð afurðamagn á móti innkaupapöntunum](inbound-load-handling.md#post-registered-quantities).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
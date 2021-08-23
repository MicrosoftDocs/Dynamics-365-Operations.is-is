---
title: Auka afköst með sjálfvirkum hreinsunarverkum
description: Þessi grein útskýrir hvernig á að leysa nokkur árangursmál hjá Microsoft Dynamics 365 Human Resources með því að hreinsa upp sögu runuvinnslunnar.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 767358705e6f43322c819116d47f4f348ca0966c7859c9f6f22a0f8004615319
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744847"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Fínstilltu árangur með sjálfvirkum hreinsunarverkum

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Úthreyfing**

Microsoft Dynamics 365 Human Resources getur upplifað vandamál við afköst ef saga runuvinnslu verður of stór.

**Orsök**

Runuvinnslur sem keyra oft geta leitt til ósjálfbærs vaxtar í sögu runuvinnslunnar. Þetta getur valdið vandamálum í afköstum. 

**Upplausn**

Tímasettu sjálfvirkt verkefni til að hreinsa úr sögu runuvinnslu. Við mælum með að setja verkið upp til að keyra vikulega en það gæti þurft að keyra hreinsunina oftar eða sjaldnar, allt eftir umhverfi. Eftirfarandi aðferð inniheldur ráðlagðar stillingar okkar, en þú getur breytt þeim í samræmi við þarfir.

1. Veldu í Human Resources **Kerfisstjórnun**.

2. Á slánni **Leita** slærðu inn **Hreinsun á sögu runuvinnslu**.

   ![Leita að hreinsun á runuvinnsluferli.](media/talent-batch-history-cleanup-search-bar.png)

3. Í **Sögutakmörkun (í dögum)** skaltu færa inn **30**.

   ![Setja takmörkun ferils á 30.](media/talent-batch-history-cleanup-history-limit.png)

4. Veldu **Keyra í bakgrunni** og veldu síðan **Endurtekning**.

   ![Stilltu endurtekningu.](media/talent-batch-history-cleanup-recurrence.png)

5. Undir **Skilgreina endurtekningu** stillirðu **Upphafsdag** og **Upphafstíma** til að eiga sér stað utan vinnutíma eða um helgar og velur síðan **ENGIN LOKADAGS.**. 

   ![Skilgreina upphafsdagsetningu og tíma endurtekningar.](media/talent-batch-history-cleanup-define-recurrence.png)

6. Undir **ENDURTEKNINGARMYNSTUR** velurðu **Dagar** og stillir **ENDURTAKA EFTIR TILTEKIÐ BIL** á **7**.

   ![Stilla hreinsun þannig að hún endurtaki sig vikulega.](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Veldu **Í lagi**.

8. Breyta öðrum breytum undir **Keyra í bakgrunni** eftir þörfum og veldu síðan **Í lagi**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
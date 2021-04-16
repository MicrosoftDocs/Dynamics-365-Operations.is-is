---
title: Auka afköst með sjálfvirkum hreinsunarverkum
description: Þessi grein útskýrir hvernig á að leysa nokkur árangursmál hjá Microsoft Dynamics 365 Human Resources með því að hreinsa upp sögu runuvinnslunnar.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 0372833c11e0919fa03d57ea258e81a89ab9ff31
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803946"
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

   ![Leita að hreinsun runuvinnsluferlis](media/talent-batch-history-cleanup-search-bar.png)

3. Í **Sögutakmörkun (í dögum)** skaltu færa inn **30**.

   ![Stilltu sögutakmörkun í 30](media/talent-batch-history-cleanup-history-limit.png)

4. Veldu **Keyra í bakgrunni** og veldu síðan **Endurtekning**.

   ![Stilla endurtekningu](media/talent-batch-history-cleanup-recurrence.png)

5. Undir **Skilgreina endurtekningu** stillirðu **Upphafsdag** og **Upphafstíma** til að eiga sér stað utan vinnutíma eða um helgar og velur síðan **ENGIN LOKADAGS.**. 

   ![Skilgreindu upphafsdag og -tíma endurtekningar](media/talent-batch-history-cleanup-define-recurrence.png)

6. Undir **ENDURTEKNINGARMYNSTUR** velurðu **Dagar** og stillir **ENDURTAKA EFTIR TILTEKIÐ BIL** á **7**.

   ![Stilltu hreinsun til að endurtaka vikulega](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Veljið **Í lagi**.

8. Breyta öðrum breytum undir **Keyra í bakgrunni** eftir þörfum og veldu síðan **Í lagi**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
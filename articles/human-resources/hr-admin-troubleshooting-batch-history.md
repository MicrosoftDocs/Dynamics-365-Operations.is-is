---
title: Auka afköst með sjálfvirkum hreinsunarverkum
description: Þetta efnisatriði útskýrir hvernig á að bæta frammistöðu í Microsoft Dynamics 365 Human Resources með því að hreinsa upp runuvinnsluferil.
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 47cd132c188c39c8700cae6035ae75d0ce71d841
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687220"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Auka afköst með sjálfvirkum hreinsunarverkum


[!INCLUDE [PEAP](../includes/peap-2.md)]

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

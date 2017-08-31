--- 
title: "Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir"
description: "Þessi verklýsing sýnir hvernig á að setja upp eigindabyggða úthlutun."
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 473d01ecddfd58aa72a972ee901673534c9d7c9c
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp eigindabyggða úthlutun. Sem skilyrði, verður að hafa afbrigðalíkan afurðar sem hefur eitt eða fleiri íhluti og eiginleika. Þessi aðferð notar hágæða hátalara líkanið gögn fyrirtækisins sýnigögn USMF. Venjulega notar framleiðslustjóri þetta ferli.


## <a name="create-a-new-price-model"></a>Búa til nýtt verðlíkan
1. Smellið á Skilgreining afurðarafbrigðislíkans
2. Smella á Afbrigðalíkan afurðar
3. Á listanum velurðu línuna fyrir hágæða hátalara, en smelltu ekki á tengilinn fyrir heitið.
4. Í aðgerðasvæðinu er smellt á líkan.
5. Smelltu á Söluverðslíkön.
6. Smellið á „Nýtt“.
7. Sláið inn gildi í reitinn Verðlíkan.
    * Notið nafn sem gerir auðvelt að bera kennsl á líkan.  
8. Sláið inn gildi í reitnum „Lýsing“.
9. Smellið á „Vista“.

## <a name="add-price-elements"></a>Bæta við verðeiningum
1. Smellið á „Breyta“.
    * Hver íhlutur í framleiðslulíkani getur haft grunnverð einingu og fjölda verðsegðarreglna. Einnig er hægt að bæta verði í mismunandi gjaldmiðlum.  
2. Í reitinn Svæði grunnverðs skal slá inn gildi.
    * Til dæmis, skrifið 100.   Grunnverðssegð getur verið tölugildi eða það getur verið samsett af útreikningi sem felur í sér eina eða fleiri eigindir.  
3. Smelltu á Bæta við.
4. I retinum skal færa inn ‚Rosewood‘.
    * Nafn verð segð gerir auðveldara að verð einingarinnar sem stendur. Í þessu dæmi er mælt stofna verðeining fyrir Rosewood speaker cabinet ljúka valkost.  
5. Breyta skilyrði.
    * Skilyrði verð hjálpar til við að tryggja samræmda segðareining verð er innifalinn í söluverði ef tiltekna samsetningu af eigindir eru til staðar.  
6. Í reitnum ConstraintBody skal slá inn 'CabinetFinish=="Rosewood"'.
7. Smellið á „Í lagi“.
8. Í reitinn Framsetning skal slá inn gildi.
    * Til dæmis, skrifið 50.  
9. Lokið síðunni.
10. Lokið síðunni.



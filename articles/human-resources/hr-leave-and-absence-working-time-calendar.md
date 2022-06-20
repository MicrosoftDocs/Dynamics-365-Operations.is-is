---
title: Búa til dagatal fyrir vinnutíma
description: Tilgreindu vinnutímadagatal, frídaga og vinnutíma í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 35fcb7c4068ff2f68970d9c0127491e4a63dab4c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861074"
---
# <a name="create-a-working-time-calendar"></a>Búa til dagatal fyrir vinnutíma


> [!Important]
> Virknin sem getið er um í þessari grein er eins og er í boði fyrir viðskiptavini á sjálfstætt Dynamics 365 Human Resources. Sum eða öll virknin verður í boði sem hluti af síðari útgáfu í tölvukerfi Finance eftir útgáfu 10.0.26 af Finance.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vinnutímadagatal í Dynamics 365 Human Resources sýnir daga og tíma sem starfsmenn vinna í fyrirtækinu þínu. Þegar starfsmaður leggur fram beiðni um leikhlé þurfa þeir ekki að hafa áhyggjur af hátíðum og lokunum.

Til að hagræða í biðbeiðnum skaltu stilla þessa hluti fyrir fyrirtækið þitt:

- Vinnutímadagatal
- Frí og lokanir
- Tími án vinnu

Þú getur bætt við tveimur síðustu hlutunum á meðan þú setur upp vinnutímadagatal. Þú getur einnig stillt eða uppfært þau sérstaklega.

## <a name="set-up-a-working-time-calendar"></a>Setja upp vinnutímadagatal

Settu upp að minnsta kosti eitt vinnutímadagatal sem sýnir daga og vinnutíma. Ef þú ert með staði í mörgum löndum og svæðum gætirðu viljað setja upp vinnutímadagatal fyrir hvert svæði.

1. Á síðunni **Fyrirtækisstjórnun** skal velja **Dagatöl**.

2. Veljið **Nýr** og færið inn heiti og lýsingu á dagatalinu.

3. Undir **Kynslóðarmöguleikar**, veldu vinnudagana fyrir skipulag þitt og sláðu inn vinnutíma. 
   - Til að bæta við fríi eða lokun skaltu velja **Bæta við** hnappinn við hliðina **Frí og lokanir**.
   - Veldu til að bæta við tíma án vinnu, svo sem nesti eða frímínútum **Bæta við** undir **NON-WORK TIME** og sláðu inn nafn og tímasvið.

4. Undir **Dagar** skaltu velja **Búa til** til að búa til dagana í dagatalinu þínu. Sláðu inn tímabilið fyrir dagatalið þitt og veldu síðan **Búa til daga**.

5. Til að bæta við vinnuáætlunum, undir **Vinnuáætlun**, veldu **Bæta við** og sláðu síðan inn tíma fyrir hvert verkáætlun.

## <a name="configure-holidays-and-closures"></a>Stilla frí og lokanir

Þú getur bætt við eða breytt frí og lokun aðskildum frá dagatali fyrir vinnutíma.

1. Á síðunni **Fyrirtækisstjórnun** skal velja **Frí og lokanir**.

2. Veljið **Nýr** og færið inn heiti og dagsetningu fyrir fríið eða lokunina.

## <a name="configure-non-work-time"></a>Stilla tíma án vinnu

Þú getur bætt við eða breytt tíma án vinnu aðskildum frá dagatali fyrir vinnutíma.

1. Á **Stjórn stofnunarinnar** síðu, veldu **EKKI VINNUTÍMI**.

2. Veldu **Nýtt** og sláðu inn heiti og tímabil fyrir tíma án vinnu.

Ef þú hefur gert kleift að forskoða eiginleikann Leyfi og fjarvistir vegna orlofsréttinda, notar Human Resources frídaga og lokunardagsetningar til að ákvarða fjölda daga til að aðlaga fyrir starfsmenn sem skráðir eru í dagatalið.

## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)
- [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

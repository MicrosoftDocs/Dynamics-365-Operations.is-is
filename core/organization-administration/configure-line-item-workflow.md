---
title: "Skilgreina Verkflæði línuatriðis"
description: "Þessu efnisatriði útskýrir hvernig skilgreina á verkflæðiseiningu línuatriðis."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 6c2b2c863d0783bd436db57d9fd3c7c5aa8dba5c
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-line-item-workflow"></a>Skilgreina Verkflæði línuatriðis

Þessu efnisatriði útskýrir hvernig skilgreina á verkflæðiseiningu línuatriðis.

Til að skilgreina verkflæðiseiningu línuatriðis í verkflæðisritlinum, hægrismellt er á einingu og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu. Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir verkflæðiseining línuatriðis.

## <a name="name-the-lineitem-workflow-element"></a>Heiti lineitem verkflæðiseiningu
Fylgið þessum skrefum til að færa inn heiti á verkflæðin línuatriðis.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Á svæðinu **Heiti ** skal færa inn einkvæmt heiti fyrir verkflæðiseiningu línuatriðis.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Tilgreina hvort sama verkflæði er notað til að vinna úr öllum línuatriðum
Fylgið eftirfarandi skrefum til að tilgreina hvort sama verkflæði er notað til að vinna úr öllum línuatriðum í skjali.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Ef sama verkflæðið vinna öllum línuatriðum á skjal, smelltu þá á **Nota eitt verkflæði fyrir öll línuatriði**. Síðan velja verkflæði sem á að nota við vinnslu á línuatriði.
3.  Ef tiltekið verkflæði á að vinna línuvörur sem uppfylla ákveðin skilyrði, smellið á **Nota verkflæði fyrir hvert línuatriði**. Fylgdu síðan þessum skrefum til að tilgreina sett af skilyrðum:
    1.  Smelltu á **Bæta við**.
    2.  Í töflunni skal velja skilyrði.
    3.  Á **heiti Skilyrðis** flipanum, færið inn heiti fyrir skilyrði sem verið er að skilgreina.
    4.  Smellið á **bæta við skilyrði ** til að slá inn skilyrðin.
    5.  Færið inn öll önnur skilyrði sem krafist er.
    6.  Hægt er að sannreyna að skilyrðin sem voru færð inn hafi verið sett upp rétt með því að smella á **prófa**. Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu og smelltu svo á **prófa**. Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst. Smelltu á **Í lagi ** eða **hætta við ** til að fara aftur síðuna **forstillingar**.

    Á **Verkflæði** flipanum, veljið verkflæðið velja verkflæði sem á að nota við vinnslu línuatriði sem uppfylla skilyrðasettin sem þú skilgreindir.




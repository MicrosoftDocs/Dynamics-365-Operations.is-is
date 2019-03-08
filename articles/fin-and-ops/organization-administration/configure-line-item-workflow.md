---
title: Skilgreina verkflæði línuatriðis
description: Þessu efnisatriði útskýrir hvernig skilgreina á verkflæðiseiningu línuatriðis.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66e79389bba4566176330914ace462110cd0aa22
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "336107"
---
# <a name="configure-line-item-workflows"></a>Skilgreina verkflæði línuatriðis

[!include [banner](../includes/banner.md)]

Þessu efnisatriði útskýrir hvernig skilgreina á verkflæðiseiningu línuatriðis.

Til að skilgreina verkflæðiseiningu línuatriðis í verkflæðisritlinum, hægrismellt er á einingu og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu. Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir verkflæðiseining línuatriðis.

## <a name="name-the-line-item-workflow-element"></a>Nefndu verkflæðiseiningu línuatriðis

Fylgið þessum skrefum til að færa inn heiti á verkflæðin línuatriðis.

1. Í vinstri glugganum, smelltu á **grunnstillingar**.
2. Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir verkflæðiseiningu línuatriðis.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Tilgreina hvort sama verkflæði er notað til að vinna úr öllum línuatriðum

Fylgið eftirfarandi skrefum til að tilgreina hvort sama verkflæði er notað til að vinna úr öllum línuatriðum í skjali.

1. Í vinstri glugganum, smelltu á **grunnstillingar**.
2. Ef sama verkflæðið vinna öllum línuatriðum á skjal, smelltu þá á **Nota eitt verkflæði fyrir öll línuatriði**. Síðan velja verkflæði sem á að nota við vinnslu á línuatriði.
3. Ef tiltekið verkflæði á að vinna línuvörur sem uppfylla ákveðin skilyrði, smellið á **Nota verkflæði fyrir hvert línuatriði**. Fylgdu síðan þessum skrefum til að tilgreina sett af skilyrðum:

    1. Smelltu á **Bæta við**.
    2. Í töflunni skal velja skilyrði.
    3. Á **heiti Skilyrðis** flipanum, færið inn heiti fyrir skilyrði sem verið er að skilgreina.
    4. Smellið á **bæta við skilyrði** til að slá inn skilyrðin.
    5. Færið inn öll önnur skilyrði sem krafist er.
    6. Hægt er að sannreyna að skilyrðin sem voru færð inn hafi verið sett upp rétt með því að smella á **prófa**. Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu og smelltu svo á **prófa**. Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst. Smelltu á **Í lagi** eða **hætta við** til að fara aftur síðuna **forstillingar**.

    Á **Verkflæði** flipanum, veljið verkflæðið velja verkflæði sem á að nota við vinnslu línuatriði sem uppfylla skilyrðasettin sem þú skilgreindir.

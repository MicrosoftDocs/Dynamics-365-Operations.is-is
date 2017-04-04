---
title: "Meðhöndlun staðgreiðsluafslætti fyrir ofgreiðslu"
description: "Þessi grein er sýnir aðstæður sem sýna hvernig greiðsla er meðhöndluð þegar viðskiptavinurinn tekur notar staðgreiðsluafslátt en borgar einnig of mikið."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 451273a8ee98f7033795182e754f76aca3788f47
ms.lasthandoff: 03/31/2017


---

# <a name="handling-cash-discounts-for-overpayments"></a>Meðhöndlun staðgreiðsluafslætti fyrir ofgreiðslu

Þessi grein er sýnir aðstæður sem sýna hvernig greiðsla er meðhöndluð þegar viðskiptavinurinn tekur notar staðgreiðsluafslátt en borgar einnig of mikið. 

Reikningur er talinn ofgreiddur þegar greiðsluupphæð er hærri en á upphæð reiknings mínus staðgreiðsluafsláttur. Til að tilgreina hvernig fáanlegur staðgreiðsluafsláttarmismunur er unninn þegar reikningur er ofgreiddur, í **stýring staðgreiðsluafsláttar** og **Hámark ofgreiðslu eða vangreiðslu** svæði á við **Færibreytur viðskiptakrafna** síðu. Í eftirfarandi dæmi, sem viðskiptavinurinn hefur ofgreitt reikninginn um 0,50.

| Heildarupphæð reiknings | Tiltækur staðgreiðsluafsláttur | Fjárhæð sem greiða á, sem felur í sér staðgreiðsluafslátt | Upphæð sem viðskiptavinur greiðir í raun |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Stjórnun staðgreiðsluafsláttar= Tilgreint
Þegar **Tiltekna** er valin í á **stýring staðgreiðsluafsláttar** á í **lyklar fyrir sjálfvirkar færslur** síðu er tekinn fullt staðgreiðsluafsláttar. Upphæð fyrir ofgreiðslu er annað hvort bókuð í fjárhagslykil mismunar fyrir staðgreiðsluafslátt eða skilið eftir stöðu á reikningi viðskiptavinar. Þessi Hegðun fer eftir því hvort upphæð ofgreiðslu er milli 0,00 og upphæðin sem færð er inn í á** Hámark ofgreiðslu eða vangreiðslu** svæði, eða hvort upphæð fyrir ofgreiðslu er meira en **Hámark ofgreiðslu eða vangreiðslu** upphæð.

### <a name="scenario-1"></a>Aðstæður 1

Í þessum aðstæðum er  ofgreiðsluupphæð á milli 0,00 og hámarks ofgreiðslu eða vangreiðslu. Reikningur er sleginn inn upp á 105,00 og staðgreiðsluafslátt er tiltækan ef reikningurinn er greiddur innan sjö daga.

| Heildarupphæð reiknings | Tiltækur staðgreiðsluafsláttur | Fjárhæð sem greiða á, sem felur í sér staðgreiðsluafslátt |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Viðskiptavinurinn sendir greiðslu fyrir 95,00 innan tímabils staðgreiðsluafslátt. Greiðslu er jafnað á móti reikningi fyrir 105.00. Eftir að reikningur og greiðsla er jöfnuð ,  munu eftirfarandi færslur stofnast á viðskiptakröfur fyrir viðskiptavini.

| Færsla   | Upphæð | Staða |
|---------------|--------|---------|
| Reikningur       | 105,00 | 0,00    |
| Greiðsla       | -95,00 | 0,00    |
| Staðgreiðsluafsláttur | -10,50 | 0,00    |

Eftirfarandi bókhaldsfærslur eru búnar til greiðslu og jöfnun. **Greiðsla**

| Reikningur             | Debetupphæð | Kreditupphæð |
|---------------------|--------------|---------------|
| Reiðufé                | 95,00        |               |
| Viðskiptakröfur |              | 95,00         |

**Uppgjör**

| Reikningur                                                                                                          | Debetupphæð | Kreditupphæð |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Staðgreiðsluafsláttur ( **aðallykils fyrir afslátt viðskiptavina** svæði á í **staðgreiðsluafslætti** síðuna)                 | 10,50        |               |
| Viðskiptakröfur                                                                                              |              | 10,50         |
| Staðgreiðsluafsláttur (í **staðgreiðsluafsláttur viðskiptavinar ** reitur á í **lykill fyrir sjálfvirk færsla** síðuna) |              | 0,50          |
| Viðskiptakröfur                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>Aðstæður 2

Í þessum aðstæðum fer ofgreiðsla upphæðar yfir hámarks upphæð ofgreiðsla eða vangreiðsla . Reikningur er sleginn inn upp á 105,00 og staðgreiðsluafslátt er tiltækan ef reikningurinn er greiddur innan sjö daga.

| Heildarupphæð reiknings | Tiltækur staðgreiðsluafsláttur | Fjárhæð sem greiða á, sem felur í sér staðgreiðsluafslátt |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Viðskiptavinurinn sendir greiðslu fyrir 95,00 innan tímabils staðgreiðsluafslátt. Greiðslu er jafnað á móti reikningi fyrir 105.00. Eftir að reikningur og greiðsla er jöfnuð ,  munu eftirfarandi færslur stofnast á viðskiptakröfur fyrir viðskiptavini.

| Færsla   | Upphæð | Staða |
|---------------|--------|---------|
| Reikningur       | 105,00 | 0,00    |
| Greiðsla       | -95,00 | -0,50   |
| Staðgreiðsluafsláttur | -10,50 | 0,00    |

Ofgreiðsluupphæð 0,50 verður að vera áfram opin staða greiðslunnar og hægt er að jafna gegn annan reikning. Eftirfarandi bókhaldsfærslur eru búnar til greiðslu og jöfnun. **Greiðsla**

| Reikningur             | Debetupphæð | Kreditupphæð |
|---------------------|--------------|---------------|
| Reiðufé                | 95,00        |               |
| Viðskiptakröfur |              | 95,00         |

**Uppgjör**

| Reikningur                                                                                          | Debetupphæð | Kreditupphæð |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Staðgreiðsluafsláttur ( **aðallykils fyrir afslátt viðskiptavina** svæði á í **staðgreiðsluafslætti** síðuna) | 10,50        |               |
| Viðskiptakröfur                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Stjórnun staðgreiðsluafsláttar= ótilgreint
Þegar **ótiltekna** er valin í á **stýring staðgreiðsluafsláttar** á í **lyklar fyrir sjálfvirkar færslur** síðu er upphæð staðgreiðsluafsláttar minnkuð sem nemur upphæð ofgreiðslu. Þessi hegðun á alltaf við, óháð hvort upphæð ofgreiðslu er yfir eða undir upphæðin sem færð er inn í á **Hámark ofgreiðslu eða vangreiðslu** svæði.

### <a name="scenario-3"></a>Aðstæður 3

Í þessum aðstæðum er Reikningur sleginn inn upp á 105,00 og staðgreiðsluafslátt er tiltækan ef reikningurinn er greiddur innan sjö daga.

| Heildarupphæð reiknings | Tiltækur staðgreiðsluafsláttur | Fjárhæð sem greiða á, sem felur í sér staðgreiðsluafslátt |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Viðskiptavinurinn sendir greiðslu fyrir 95,00 innan staðgreiðsluafsláttardagsetningar. Greiðslu er jafnað á móti reikningi fyrir 105.00. Eftir að reikningur og greiðsla er jöfnuð ,  munu eftirfarandi færslur stofnast á viðskiptakröfur fyrir viðskiptavini.

| Færsla   | Upphæð | Staða |
|---------------|--------|---------|
| Reikningur       | 105,00 | 0,00    |
| Greiðsla       | -95,00 | -0,00   |
| Staðgreiðsluafsláttur | -10,00 | 0,00    |

Upphæð staðgreiðsluafsláttar er minnkað úr í 10,50 10,00. Greiðslu og reiknings litið jöfnuð. **Greiðsla**

| Reikningur             | Debetupphæð | Kreditupphæð |
|---------------------|--------------|---------------|
| Reiðufé                | 95,00        |               |
| Viðskiptakröfur |              | 95,00         |

**Uppgjör**

| Reikningur                                                                                          | Debetupphæð | Kreditupphæð |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Staðgreiðsluafsláttur ( **aðallykils fyrir afslátt viðskiptavina** svæði á í **staðgreiðsluafslætti** síðuna) | 10,50        |               |
| Viðskiptakröfur                                                                              |              | 10,50         |





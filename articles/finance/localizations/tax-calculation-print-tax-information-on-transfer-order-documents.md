---
title: Prenta skattaupplýsingar á skjöl flutningspantana
description: Í þessu efnisatriði er útskýrt hvernig hægt er að prenta skattaupplýsingarnar sem eru ákvarðaðar af skattaútreikningsþjónustunni á skjöl flutningspöntunar.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e74336270ab46fc19adb4c797745c9582028391a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687472"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Prenta skattaupplýsingar á skjöl flutningspantana

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að prenta skattaupplýsingar á skjöl flutningspöntunar. Hægt er að prenta bráðabirgðareikningsskjal flutningspöntunar fyrir birgðaflutning sem litið er á sem framboð innan samfélags og kaup innan samfélags undir virðisaukaskattsreglum Evrópusambandsins. 

Eftirfarandi skatttengdum gögnum er bætt við skjöl flutningspöntunar:

- Nöfnin og senda-frá og senda-til aðsetrin fyrir birgðaflutninginn
- Skattauðkennisnúmer birgja og viðtakanda
- Einingarverð og skattskyld upphæð afhentrar vöru
- Skattkóði, skatthlutfall, skattupphæð og skattareglur

Til að stilla þessi gögn þarf að ljúka við eftirfarandi meginskref.

1. [Virkja og setja upp skattaeiginleika fyrir flutningspantanir](tasks/Tax-feature-support-for-transfer-order.md).
2. [Stofna og setja upp mörg skattskráningarnúmer fyrir lögaðila](emea-multiple-vat-registration-numbers.md).
3. Setja upp undanþágukóða, lýsingu, skattareglur og prentkóða í skattkóðum. Fyrir þetta dæmi eru þrír skattkóðar búnir til og samstilltir í Microsoft Dynamics 365 Fjármál: **NL-Undanþegin**, **-RC-21**, og **BE-RC+21**.

    1. Í Finance skal fara í **Skattur** \> **Uppsetning** \> **Söluskattur** \> **Skattaundanþágunúmer**.
    2. Veldu **Breyta** og sláðu inn lýsingu á undanþágukóða **EB**. Sláðu til dæmis inn **Skattfrjáls EB-sending með skattskráningarnúmeri**.
    3. Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkur**.
    4. Veldu skattkóðann **BE-RC-21** og svo **Skattareglur**.
    5. Veljið **Nýtt**.
    6. Í reitnum **Tungumál** skal velja **EN-US**. Í reitinn **Texti** skal síðan færa inn **Skjal sem sýnir flutning á vörum samkvæmt grein 138. 2. c) í EB VSK tilskipun 2006/112/EB**.
    7. Lokið síðunni.
    8. Á flýtiflipanum **Almennt**, í reitnum **Prenta**, skal velja **VSK-hlutfall**.
    8. Veldu skattkóðann **NL-Exempt** og síðan á flýtiflipanum **Almennt** í reitnum **Prenta** skal velja **VSK-hlutfall**.

    > [!NOTE] 
    > Skattkóðinn, skatthlutfallið og lýsing skattaundanþágu eru ekki prentuð á skjöl flutningspöntunar ef engri lýsingu á undanþágukóða eða skattreglu er viðhaldið fyrir skattkóðann.

## <a name="print-the-transfer-order---shipment-document"></a>Prenta flutningspöntun - sendingarskjal

Eftir að flutningur er sendur skal fylgja þessum skrefum til að prenta út flutningspöntun - sendingarskjal.

1. Farðu í **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Flutningspantanir** \> **Sending**.
2. Á flipanum **Færibreytur**, í flokknum **Prenta**, skal virkja **Skattaupplýsingar**.
3. Á flipanum **Færslur til að taka með** skal velja **Sía**, velja flutningspöntunarnúmerið og síðan velja **Í lagi**.
4. Veldu **Í lagi** til að prenta flutningspöntun - sendingarskjal.

## <a name="print-the-transfer-order---receipt-document"></a>Prenta flutningspöntun - innhreyfingarskjal

Eftir að flutningur er móttekinn skal fylgja þessum skrefum til að prenta út flutningspöntun - innhreyfingarskjal.

1. Farðu í **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Flutningspantanir** \> **Taka á móti**.
2. Á flipanum **Færibreytur**, í flokknum **Prenta**, skal virkja **Skattaupplýsingar**.
3. Á flipanum **Færslur til að taka með** skal velja **Sía**, velja flutningspöntunarnúmerið og síðan velja **Í lagi**.
4. Veldu **Í lagi** til að prenta flutningspöntun - innhreyfingarskjal.

## <a name="print-the-transfer-overview-document"></a>Prenta skjal flutningsyfirlits

Fylgdu þessum skrefum til að prenta skjal flutningsyfirlits.

> [!NOTE]
> Skattaupplýsingar eru aðeins í boði þegar flutningspöntunin hefur verið send eða móttekin.

1. Farðu í **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Flutningspantanir** \> **Flutningsyfirlit**.
2. Á flipanum **Færibreytur**, í flokknum **Prenta**, skal virkja **Skattaupplýsingar**.
3. Á flipanum **Færslur til að taka með** skal velja **Sía**, velja flutningspöntunarnúmerið og síðan velja **Í lagi**.
4. Veldu **Í lagi** til að prenta skjal flutningsyfirlits.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]

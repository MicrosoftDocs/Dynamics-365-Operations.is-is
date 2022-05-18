---
title: Skilgreina hæfni
description: Hægt er að rekja hæfni starfsmanns í Dynamics 365 Human Resources. Einnig er hægt að tilgreina hæfni sem krafist er fyrir tiltekna vinnslu.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 7c853ad71aecd7f5d214c02da97f7956ff2391df
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695957"
---
# <a name="configure-skills"></a>Skilgreina hæfni

> [!IMPORTANT]
> Virknin sem bent er á í þessu efnisatriði er eins og er í boði fyrir mannauðsviðskiptavini á fjármálainnviðum.  


Hægt er að rekja hæfni starfsmanns í Dynamics 365 Human Resources. Einnig er hægt að tilgreina hæfni sem krafist er fyrir tiltekna vinnslu.

Dæmi um hæfni sem hægt er að rekja eru:

- Eftirlitsyfirvald - getan til að hafa umsjón með vinnu annarra.
- Forysta - Geta til að leiða starfsmenn og fyriristækjasvið.
- Áætlanagerð – Geta til að horfa fram á við, til að búa til yfirlýst markmið og fylgja þeim eftir.
- HTML-Möguleika á að skrifa html-kóða.

Ef þú hefur ekki þegar sett upp hæfnisgerðir og matslíkön þarftu að bæta einhverjum við áður en hæfni er búin til.

Eftirfarandi aðilar geta fært inn hæfni fyrir starfsmann:

- Starfskraftar geta sjálfir skráð hæfni sína í sjálfsafgreiðslu starfsmanns. Þessi hæfni krefst samþykkis stjórnanda.
- Stjórnendur geta fært inn hæfni fyrir starfsmenn sína. Hægt er að stofna vinnuflæði sem samþykkir þessa hæfni sjálfkrafa.

## <a name="create-a-skill-type"></a>Stofna hæfnisgerð

Hæfnisgerðir eru flokkar sem einstaka hæfni fellur undir, t.d. stjórnun eða sölu.

1. Á vinnusvæðinu **Þróun starfsmanns** skal velja **Tenglar**.

2. Undir **Uppsetning á hæfni** skal velja **Hæfnisgerðir**.

3. Veljið **Nýtt**.

4. Ljúktu við eftirfarandi reiti:

   - **Hæfnisgerð**: Færið inn heiti fyrir hæfnisgerðina.
   - **Lýsing**: Færið inn lýsingu á hæfnisgerðinni.

5. Veldu **Vista**.

## <a name="create-a-rating-model"></a>Búa til einkunnalíkan

Matslíkön hjálpa til við að meta raunverulegt stig einstaklings af hæfni, stig sem þeir eiga að vinna að ná, eða þá hæfni sem krafist er fyrir vinnslu. Hvert stig í einkunnalíkani fær úthlutað stuðli.

1. Á vinnusvæðinu **Þróun starfsmanns** skal velja **Tenglar**.

2. Undir **Uppsetning á hæfni** skal velja **Matslíkön**.

3. Veljið **Nýtt**.

4. Ljúktu við eftirfarandi reiti:

   - **Mat**: Færið inn heiti fyrir matslíkanið, t.d. **Hæfni**.
   - **Lýsing**: Færið inn lýsingu á matslíkaninu, t.d. **Hæfnismat**.

5. Í hlutanum **Stig** skal velja **Nýtt**. Fyrir hvert stig sem bæta á við þarf að ljúka eftirfarandi reitum:

   - **Stig**: Færið inn heiti fyrir stigið.
   - **Lýsing**: Færið inn lýsingu fyrir stigið.
   - **Stuðull**: Færið inn gildi stuðuls frá 0-9. Stuðlar hjálpa til við að staðla einkunnir vegna hæfni sem notast við mismunandi matslíkön. Hvert stig verður að hafa einkvæman stuðul. Stig með hærri stuðul hafa meira vægi í einkunnalíkani.

   Haldið áfram að bæta stigum við eftir þörfum. Færa má inn allt að 10 stig fyrir hvert matslíkan.

6. Veldu **Vista**.

## <a name="create-a-skill"></a>Stofna hæfni

Áður en hægt er að úthluta hæfni eða stofna leit að hæfnisskrá eða stofna hæfnisprófíl þarf að færa inn upplýsingar um hæfni á síðunni **Hæfni**. Fyrir hverja hæfni er hægt að velja gerð hæfni og einkunnalíkan.

1. Á vinnusvæðinu **Þróun starfsmanns** skal velja **Tenglar**.

2. Undir **Uppsetning á hæfni** skal velja **Hæfni**.

3. Veljið **Nýtt**.

4. Ljúktu við eftirfarandi reiti:

   - **Hæfni**: Færið inn heiti fyrir hæfnina.
   - **Lýsin**: Færið inn lýsingu á hæfninni.
   - **Mat**: Veljið matslíkanið sem á að nota fyrir þessa hæfni.
   - **Hæfnisgerð**: Veljið af listanum yfir hæfnisgerðir.

5. Veldu **Vista**.

## <a name="see-also"></a>Sjá einnig

[Slá inn hæfni](hr-develop-enter-skills.md)<br>
[Kortleggja hæfni](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

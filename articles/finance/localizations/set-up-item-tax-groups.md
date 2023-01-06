---
title: Setja upp vöruskattsflokka
description: Í þessari grein er útskýrt hvernig á að setja upp skattflokka vöru í skattaútreikningsþjónustu.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 3bc705bc8173ad2bc8ef883e6dc80b0a187314ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846464"
---
# <a name="set-up-item-tax-groups"></a>Setja upp vöruskattsflokka

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að setja upp skattflokka vöru í skattaútreikningsþjónustu. Einnig er útskýrt hvernig á að setja upp fylki gildissviðsreglu fyrir skattflokk vöru og skilgreina línur í fylkinu.

Hugmyndin um skattflokka vöru í skattaútreikningsþjónustunni líkist hugmyndinni um VSK-flokka vöru í Microsoft Dynamics 365 Finance. Þeir eru hópar skattkóða. Skattaútreikningsþjónustan notar skurðpunkt skattflokks og skattflokks til að ákvarða skattkóða.

> [!IMPORTANT]
> Uppsetning skattflokka vöru í skattaútreikningsþjónustunni er óháð lögaðila. Aðeins er hægt að ljúka við þessa uppsetningu í Regulatory Configuration Service (RCS) einu sinni. Þegar þú virkjar þjónustu skattaútreiknings í fjármálum eru skattahópar sjálfkrafa samstilltir fyrir valinn lögaðila.

## <a name="set-up-an-item-tax-group"></a>Setja upp skattflokk vöru 

Fylgdu þessum skrefum til að setja upp skattflokk vöru.

1. Skrá inn á [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Farið í **Vinnusvæði** \> **Altækir eiginleikar** \> **Skattaútreikningur**.
3. Veljið eiginleikann og útgáfuna sem á að setja upp og veljið svo **Breyta**.
4. Í flipanum **Almennt** skal velja **Útgáfa skilgreiningar**.
5. Í flipanum **Skattflokkur vöru** skal velja **Stjórna dálki**. Ef þú ert að setja upp skattflokk vöru í fyrsta skipti eru reitirnir í svarglugganum **Stjórna dálki** sjálfkrafa stilltir.
6. Í listanum til vinstri skal stækka hnútinn **Línur** og velja gátreitinn fyrir **Skattflokk vöru**.

    ![Skattflokkur vöru valinn undir línuhnútnum í svarglugganum „Stjórna dálkum“.](media/select-item-tax-group.png)

7. Veldu hægri örvarhnappurtil að bæta **Skattflokki vöru** við listann yfir **Valdir dálkar** hægra megin.

    ![Skattflokki vöru var bætt við lista yfir valda dálka.](media/add-item-tax-group.png)

8. Veldu **Í lagi**.

## <a name="configure-an-item-tax-group"></a>Skilgreina skattflokk vöru

Þegar skattflokkur vöru hefur verið settur upp er fylki gildissviðsreglu búið til. Hægt er að bæta línum við fylkið til að stilla skattahóp vörunnar.

1. Í flipanum **Skattflokkur vörur** skal velja **Bæta við**.
2. Í reitinn **Skattflokkur vöru** skal færa inn heiti á skattflokki vöru.

    > [!IMPORTANT]
    > Við mælum með því að heiti skattahópsins sé takmarkað við 10 stafi. Þetta heiti er samstillt við Finance, sem hefur 10 stafa hámark fyrir heiti VSK-flokks vöru.

3. Í retinum **Skattkóðar** skal velja gátreitinn fyrir hvern skattkóða sem á að vera með í skattflokki vörunnar. Hægt er að hafa marga skattkóða með í einum skattflokki.

    ![Margir skattkóðar valdir í reitnum Skattkóðar.](media/multiple-tax-codes-selection.png)

4. Endurtaktu skref 1 til 3 til að bæta við fleiri skattflokkum.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

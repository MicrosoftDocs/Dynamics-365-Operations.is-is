---
title: Setja upp skattflokka
description: Í þessari grein er útskýrt hvernig á að setja upp skatthópa í Skattaútreikningsþjónustu.
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
ms.openlocfilehash: 89c5670ee7e78f2dc51f128c3ae8d284bb6b925b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862900"
---
# <a name="set-up-tax-groups"></a>Setja upp skattflokka

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að setja upp skatthópa í Skattaútreikningsþjónustu. Einnig er útskýrt hvernig á að setja upp fylki gildissviðsreglu fyrir skattflokk og skilgreina línur í fylkinu.

Hugtakið skatthópar í Skattaútreikningsþjónustu líkist hugtakinu söluskatthópar í Microsoft Dynamics 365 Finance. Þeir eru hópar skattkóða. Skattaútreikningsþjónustan notar skurðpunkt skattflokks og skattflokks til að ákvarða skattkóða.

Skattahópar í skattaútreikningsþjónustunni eru þó frábrugðnir söluskattshópum í Finance þar sem það eru engar aðrar færibreytur á þeim, svo sem **Neysluskattur** og **Undanþeginn skattur**. Þess í stað eru þessar breytur tiltækar á skattkóðastigi.

> [!IMPORTANT]
> Uppsetning skattkóða í skattaútreikningsþjónustunni er óháð lögaðila. Aðeins er hægt að ljúka við þessa uppsetningu í Regulatory Configuration Service (RCS) einu sinni. Þegar þú virkjar skattaútreikningsþjónustu í fjármálum eru skattahópar sjálfkrafa samstilltir fyrir valinn lögaðila.

## <a name="set-up-a-tax-group"></a>Setja upp skattaflokk

Fylgið þessum skrefum til að setja upp skattflokk.

1. Skrá inn á [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Farið í **Vinnusvæði** \> **Altækir eiginleikar** \> **Skattaútreikningur**.
3. Veljið eiginleikann og útgáfuna sem á að setja upp og veljið svo **Breyta**.
4. Í flipanum **Almennt** skal velja **Útgáfa skilgreiningar**.
5. Í flipanum **Skattflokkur** skal velja **Stjórna dálki**. Ef þú ert að setja upp skattflokk í fyrsta skipti eru reitirnir í svarglugganum **Stjórna dálki** sjálfkrafa stilltir.
6. Í listanum til vinstri skal stækka hnútinn **Línur** og velja gátreitinn fyrir **Skattflokkur**.

    ![Skattahópur valinn undir Línuhnút í svarglugganum Stjórna dálkum.](media/select-tax-group.png)

7. Veldu hægri örvatakkann til að bæta **Skattaflokkur** við listann yfir **Valdir dálkar** hægra megin.

    ![Skattahópi bætt við lista yfir valda dálka.](media/add-tax-group.png)

8. Veldu **Í lagi**.

## <a name="configure-a-tax-group"></a>Grunnstilla skattflokk

Þegar skattflokkur hefur verið settur upp er fylki gildissviðsregla skattflokksins búin til. Hægt er að bæta línum við fylkið til að stilla skattflokkinn.

1. Á flipanum **Skatthópur** velurðu **Bæta við**.
2. Færið inn heiti skattflokksins í svæðinu **Skatthópur**.

    > [!IMPORTANT]
    > Við mælum með því að takmarka heiti skattahópsins við 10 stafi. Þetta heiti er samstillt við Finance sem hefur 10 stafa hámark fyrir nöfn söluskattshópa.

3. Í **Skattkóðar** reitnum er hakað við hvern skattkóða sem taka á með í skattahópnum. Hægt er að hafa marga skattkóða í einum skattflokki.

    ![Margir skattkóðar valdir í reitnum Skattkóðar.](media/multiple-tax-codes-selection.png)

4. Endurtakið skref 1 til og með 3 til að bæta við fleiri skattflokkum.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

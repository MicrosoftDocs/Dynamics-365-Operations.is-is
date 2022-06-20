---
title: Setja upp skattflokka
description: Þessi grein útskýrir hvernig á að setja upp skattflokka í Skattútreikningsþjónustunni.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862900"
---
# <a name="set-up-tax-groups"></a>Setja upp skattflokka

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp skattflokka í Skattútreikningsþjónustunni. Það útskýrir einnig hvernig á að setja upp reglufylki skattaflokks gilda og stilla línur í fylkinu.

Hugtakið skattflokkar í Skattútreikningsþjónustunni líkist hugtakinu söluskattsflokkar í Microsoft Dynamics 365 Fjármál. Þetta eru hópar skattakóða. Skattútreikningsþjónustan notar skurðpunkta skattflokks og vöruskattsflokks til að ákvarða skattkóðana.

Hins vegar eru skattflokkar í Skattútreikningsþjónustunni frábrugðnir söluskattsflokkum í Fjármálum að því leyti að engar aukafæribreytur eru á þeim, s.s.**Notaðu skatt** og **Undanþágur skattur**. Þess í stað eru þessar færibreytur tiltækar á skattakóðastigi.

> [!IMPORTANT]
> Uppsetning skattflokka í Skattútreikningsþjónustunni er lögaðili-agnostic. Þú getur aðeins klárað þessa uppsetningu í Regulatory Configuration Service (RCS) einu sinni. Þegar þú virkjar skattaútreikningsþjónustuna í Finance, eru skattflokkar sjálfkrafa samstilltir fyrir valda lögaðila.

## <a name="set-up-a-tax-group"></a>Settu upp skattaflokk

Fylgdu þessum skrefum til að setja upp skattaflokk.

1. Skrá inn [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Fara til **Vinnurými** \> **Hnattvæðingareiginleikar** \> **Skattútreikningur**.
3. Veldu eiginleikann og útgáfuna sem þú vilt setja upp og veldu síðan **Breyta**.
4. Á **Almennt** flipa, veldu **Stillingarútgáfa**.
5. Á **Skattahópur** flipa, veldu **Stjórna dálki**. Ef þú ert að setja upp skattaflokk í fyrsta skipti eru reitirnir í **Stjórna dálki** svarglugginn er sjálfkrafa stilltur.
6. Í listanum til vinstri, stækkaðu **Línur** hnút og veldu gátreitinn fyrir **Skattahópur**.

    ![Skattflokkur valinn undir línuhnút í glugganum Stjórna dálkum.](media/select-tax-group.png)

7. Veldu hægri örvarhnappinn til að bæta við **Skattahópur** til **Valdir dálkar** lista til hægri.

    ![Skattflokkur bætt við Valda dálka listann.](media/add-tax-group.png)

8. Veldu **Í lagi**.

## <a name="configure-a-tax-group"></a>Stilltu skattaflokk

Eftir að þú hefur sett upp skattflokk er gildisreglufylki skattaflokks stofnuð. Hægt er að bæta línum við fylkið til að stilla skattaflokkinn.

1. Á **Skattahópur** flipa, veldu **Bæta við**.
2. Í **Skattahópur** reit, sláðu inn nafn skattahópsins.

    > [!IMPORTANT]
    > Við mælum með að þú takmarkir nafn skattahópsins við 10 stafi. Þetta nafn er samstillt við Finance, sem hefur hámark 10 stafi fyrir nöfn söluskattshópa.

3. Í **Skattkóðar** reit skaltu velja gátreitinn fyrir hvern skattkóða sem þú vilt hafa með í skattaflokknum. Þú getur sett marga skattkóða með í einum skattaflokki.

    ![Margir skattkóðar valdir í reitnum Skattkóðar.](media/multiple-tax-codes-selection.png)

4. Endurtaktu skref 1 til 3 til að bæta við fleiri skattaflokkum.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Setja upp vöruskattsflokka
description: Þessi grein útskýrir hvernig á að setja upp vöruskattflokka í Skattútreikningsþjónustunni.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846464"
---
# <a name="set-up-item-tax-groups"></a>Setja upp vöruskattsflokka

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp vöruskattflokka í Skattútreikningsþjónustunni. Það útskýrir einnig hvernig á að setja upp gildisreglufylki vöruskattaflokks og stilla línur í fylkinu.

Hugtakið vöruskattsflokkar í Skattútreikningsþjónustunni líkist hugtakinu vöruskattsflokkar í Microsoft Dynamics 365 Fjármál. Þetta eru hópar skattakóða. Skattútreikningsþjónustan notar skurðpunkta skattflokks og vöruskattsflokks til að ákvarða skattkóðana.

> [!IMPORTANT]
> Uppsetning vöruskattsflokka í Skattútreikningsþjónustunni er lögaðili-agnostic. Þú getur aðeins klárað þessa uppsetningu í Regulatory Configuration Service (RCS) einu sinni. Þegar þú virkjar skattreikningaþjónustuna í Finance eru vöruskattflokkar samstilltir sjálfkrafa fyrir valda lögaðila.

## <a name="set-up-an-item-tax-group"></a>Settu upp vöruskattflokk 

Fylgdu þessum skrefum til að setja upp vöruskattflokk.

1. Skrá inn [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Fara til **Vinnurými** \> **Hnattvæðingareiginleikar** \> **Skattútreikningur**.
3. Veldu eiginleikann og útgáfuna sem þú vilt setja upp og veldu síðan **Breyta**.
4. Á **Almennt** flipa, veldu **Stillingarútgáfa**.
5. Á **Vöruskattflokkur** flipa, veldu **Stjórna dálki**. Ef þú ert að setja upp vöruskattflokk í fyrsta skipti munu reitirnir í **Stjórna dálki** svarglugginn er sjálfkrafa stilltur.
6. Í listanum til vinstri, stækkaðu **Línur** hnút og veldu gátreitinn fyrir **Hlutaskattshópur**.

    ![Vöruskattsflokkur valinn undir línuhnútnum í Stjórna dálkum svarglugganum.](media/select-item-tax-group.png)

7. Veldu hægri örvarhnappinn til að bæta við **Hlutaskattshópur** til **Valdir dálkar** lista til hægri.

    ![Skattaflokkur vöru bætt við listann Valdir dálkar.](media/add-item-tax-group.png)

8. Veldu **Í lagi**.

## <a name="configure-an-item-tax-group"></a>Stilla vöruskattflokk

Eftir að þú hefur sett upp vöruskattflokk er gildisreglufylki stofnað. Hægt er að bæta línum við fylkið til að stilla vöruskattflokkinn.

1. Á **Vöruskattflokkur** flipa, veldu **Bæta við**.
2. Í **Vöruskattflokkur** reit skal slá inn nafn vöruskattsflokks.

    > [!IMPORTANT]
    > Við mælum með að þú takmarkir nafn vöruskattsflokks við 10 stafi. Þetta nafn er samstillt við Finance, sem hefur hámark 10 stafi fyrir nöfn vöruskattsflokka.

3. Í **Skattkóðar** reit, veljið gátreitinn fyrir hvern skattkóða sem á að hafa með í vöruskattflokknum. Þú getur sett marga skattkóða með í einum vöruskattflokki.

    ![Margir skattkóðar valdir í reitnum Skattkóðar.](media/multiple-tax-codes-selection.png)

4. Endurtaktu skref 1 til 3 til að bæta við fleiri vöruskattflokkum.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

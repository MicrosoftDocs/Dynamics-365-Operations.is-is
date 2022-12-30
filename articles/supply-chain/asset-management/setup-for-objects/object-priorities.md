---
title: Þjónustustig eignar
description: Þessi grein útskýrir þjónustustig eigna í Eignastýringu.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7429b30253f540925e67ff9239667a0a404f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908686"
---
# <a name="asset-service-levels"></a>Þjónustustig eignar

[!include [banner](../../includes/banner.md)]

 

Þessi grein útskýrir þjónustustig eigna í Eignastýringu. Stig eignaþjónustunnar eru tengd eignum og eru færð yfir í viðhaldsbeiðnir og verkbeiðnir. Þau eru notuð til að reikna út forgang verkbeiðna við tímasetningu verkbeiðna. Hægt er að breyta þjónustustigum eigna ef þörf er á.

Nánari upplýsingar um uppsetninguna sem er tengd útreikningi á matseinkunnum fyrir tímasetningar verkbeiðni, sjá [Færibreytur eignastýringar](../setup-for-objects/enterprise-asset-management-parameters.md). Þú verður að setja upp að minnsta kosti eina sjálfgefna skrá fyrir þjónustustig eigna. Þessi sjálfgefna skrá er notuð ef engin önnur samsvörun finnst við tímasetningu verkbeiðni.

**Dæmi 1:** Sjálfgefið þjónustustig sem er notað ef engin önnur samsvörun er að finna. Í þessari skrá velurðu aðeins þjónustustig.

**Dæmi 2:** Hátt þjónustustig sem notað er til að skipuleggja störf fyrir Volvo vörubifreiðarvél. Í þessari skrá velurðu viðeigandi eignategund (svo sem **Vél í vörubíl**), framleiðandi (**Volvo**), og þjónustustig.

## <a name="set-up-asset-service-levels"></a>Setja upp þjónustustig eigna

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignaþjónustustig**.
2. Veljið **Ný** til að stofna nýja skrá.
3. Taktu viðeigandi val í háð því smáatriðum sem krafist er fyrir þjónustustig eigna í reitunum **Virk staðsetning**, **Gerð eigna**, **Framleiðandi**, **Fyrirmynd**, **Eignir**, **Gerð verkbeiðni**, og **Þjónustustig**.

    > [!NOTE]
    > Þegar eignaþjónustustigið er notað við viðhaldsbeiðnir og verkbeiðnir fer Eignastjórn í gegnum allar færslur þjónustustigsins til að athuga hvort mögulegt sé samsvörun. Það athugar alltaf sértækustu samsetninguna fyrst. Með öðrum orðum, Eignastjórnun kannar fyrst hvort samsvörun finnist fyrir reitinn **Gerð verkbeiðni**. Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Eignir**, og svo framvegis. Eins og þú sérð á skipulagi síðunnar **Þjónustustig eigna** þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá velur eignastjórnun hverja skrá frá hægri til vinstri fyrir leik. Ef engin samsvörun er notuð er sjálfgefna skráin sem hefur ekkert val í þeim reitum notuð.

4. Í reitnum **Þjónustustig** velurðu tölu sem gefur til kynna þjónustustigið (forgang).


> [!NOTE]
> Ef þú breytir færslu eignaþjónustustigs á **Þjónustustig** síðu eftir að þú hefur þegar notað það í verkbeiðni, þjónustustig fyrir viðhaldsbeiðnir og verkbeiðnir er ekki uppfært í samræmi við það.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Setja upp ástæðukóða
description: Dynamics 365 Human Resources notar ástæðukóða til að útskýra hvers vegna fríðindi starfsmanns er að breytast.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 692bd5acd574492526644849fb555e5856b4463f
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323420"
---
# <a name="set-up-reason-codes"></a>Setja upp ástæðukóða

Dynamics 365 Human Resources notar ástæðukóða til að útskýra hvers vegna fríðindi starfsmanns er að breytast.

> [!NOTE]
> Frá og með janúar 2021 fluttust ástæðukóðar yfir á vinnusvæðið **Starfsmannastjórnun** í staðinn fyrir vinnusvæðið **Fríðindastjórnun**. Frekari upplýsingar er að finna í [Flytja ástæðukóða handvirkt yfir í starfsmannastjórnun](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Stofna ástæðukóða

1. Á vinnusvæðinu **Starfsmannastjórnun** (eða vinnusvæðinu **Fríðindastjórnun** ef ástæðukóðarnir hafa ekki verið fluttir) skal velja **Tenglar** og síðan velja **Ástæðukóðar**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Ástæðukóði** | Einstakt nafn til að bera kennsl á ástæðu þess að starfsmaður myndi breyta skráningu í fríðindaáætlun. |
   | **Lýsing** | Lýsing á ástæðukóðanum. |

4. Undir **Aðstæður sem eiga við** skal stilla **Fríðindastjórnun** á **Já**. (Á ekki við ef ástæðukóðar hafa ekki verið yfirfærðir á vinnusvæðið **Starfsmannastjórnun**.)

5. Veldu **Vista**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Flytja ástæðukóða handvirkt yfir í starfsmannastjórnun

Í janúar 2021 verða ástæðukóðar fluttir yfir á vinnusvæðið **Starfsmannastjórnun** í staðinn fyrir vinnusvæðið **Fríðindastjórnun**. Flest gögn ástæðukóða munu flytjast sjálfkrafa yfir í umhverfið. Hugsanlega flytjast ekki sum gögn ástæðukóða. Sem dæmi þá eru ástæðukóðar nú með 15 stafi að hámarki, þannig að ástæðukóðar sem eru lengri en 15 stafir munu ekki flytjast sjálfkrafa.

Borði birtist á síðunni **Tenglar** á vinnusvæðinu **Fríðindastjórnun** sem gefur flutninginn til kynna og hvort einhverjir ástæðukóðar flytjist ekki.

1. Veljið **Ástæðukóðar** fyrir upplýsingar um stöðu flutnings.

   [![Ástæðukóðar.](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Veljið ástæðukóða sem ekki tókst að flytja.

   [![Staða á flutningi ástæðukóða.](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Veljið **Yfirfæra ástæðukóða**.

   [![Yfirfæra ástæðukóða.](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. Í glugganum **Yfirfærsla ástæðukóða fríðinda** eru tvær möguleikar á vörpun í ástæðukóða starfsmannastjórnunar:

   - Til að nota fyrirliggjandi ástæðukóða í starfsmannastjórnun skal velja einn úr fellilistanum **Nota fyrirliggjandi ástæðukóða**.
     > [!NOTE]
     > Aðeins er hægt að nota fyrirliggjandi ástæðukóða í starfsmannastjórnun ef annar ástæðukóði fríðindastjórnunar hefur ekki enn verið færður í hana.
   - Til að stofna nýjan ástæðukóða í starfsmannastjórnun skal slá nýjan inn í **Nýr ástæðukóði** og síðan færa inn lýsingu í **Ný lýsing**.

   [![Varpa í ástæðukóða starfsmannastjórnunar.](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Þegar ástæðukóðar hafa verið fluttir yfir í starfsmannastjórnun er möguleikinn á að nota þá í fríðindastjórnun sjálfkrafa stilltur á **Já**.

[![Nota ástæðukóða í fríðindastjórnun.](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

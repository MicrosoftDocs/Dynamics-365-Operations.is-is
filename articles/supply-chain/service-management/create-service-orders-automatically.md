---
title: "Stofna þjónustupantanir sjálfkrafa"
description: "Þú getur búið til þjónustupantanir fyrir eina þjónustusamning eða fyrir nokkra þjónustusamninga."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c39e5b5eb79859b0a76c357edfee953ca90c0c4a
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-orders-automatically"></a>Stofna þjónustupantanir sjálfkrafa    

[!include [banner](../includes/banner.md)]


Þú getur búið til þjónustupantanir fyrir eina þjónustusamning eða fyrir nokkra þjónustusamninga. Þegar þær eru búnar til, er hægt að skoða þjónustupantanir þínar í **þjónustupantanir** skjámynd.

Þjónustupantanir eru aðeins búnar til fyrir gildistíma þjónustusamningsins. Ef bilið sem þú tilgreinir í **Búa til þjónustupantanir** er fyrir upphafsdag eða eftir lokadag þjónustusamningsins eru þjónustupantanir aðeins búnar til fyrir þann hluta bilsins sem er innan dagsetningar þjónustusamningsins.

Þegar þú stofnar þjónustupantanir handvirkt eða sjálfvirkt úr þjónustusamningslínu, verður þjónustupöntunin að vera á því tímabili sem er skilgreint af upphafs- og lokadagsetningu línunnar nema þú setir ekki lokadag á línu.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Stofna þjónustupantanir fyrir þjónustusamning sjálfvirkt

1.  Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.

2.  Velja þjónustusamning.

3.  Smelltu á **Afhenda** flipann og smelltu síðan **Áætlað þjónustupantanir**.

4.  Tilgreindu dagsetningar í **Frá dagsetningu** og **Til dagsetningar** reitum til að skilgreina þjónustutímabilið.

5.  Veldu **Sýna upplýsingaskrá** gátreitur til að birta lista yfir þjónustupantanir sem eru búin til.

6.  Veldu færslugerðir í reitahópnum **Nær yfir færslugerðir**. Færslugerðirnar tákna línurnar sem eru búnar til í þjónustusamningnum og hver færslugerð sem þú velur býr til nokkrar þjónustupantanir, allt eftir því þjónustutímabili sem er tilgreint á þjónustusamningslínu.

7.  Til að búa til einhverjar þjónustupantanir sem vantar í samfelldri röð þjónustupantana skaltu velja gátreitur **Samfellt**.

8.  Smellið á **Í lagi**.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Stofna þjónustupantanir fyrir marga þjónustusamninga sjálfvirkt

1.  Smelltu á **þjónustukerfi** \> **Reglubundið** \> **þjónustupantanir** \> **Búa til þjónustupantanir**.

2.  Smelltu á **Velja** til að velja að bæta við eða fjarlægja viðmiðanir til að nota til að búa til þjónustupantanir.

3.  Smellið á **Í lagi**.

## <a name="see-also"></a>Sjá einnig

[Þjónustupantanir](service-orders.md)

[Býr til þjónustupantanir sjálfvirkt](auto-create-service-orders.md)

  




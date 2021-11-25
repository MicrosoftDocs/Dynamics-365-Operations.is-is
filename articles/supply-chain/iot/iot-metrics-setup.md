---
title: Setja upp mælieiningar fyrir IoT-gervigreind
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp mælieiningar fyrir IoT-gervigreind.
author: tonyafehr
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85db0211c32ad4e27c3a9a65d2c74c5a39687f9c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783099"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>Setja upp mælieiningar fyrir IoT-gervigreind

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>Skilgreina mælieiningar

Ef á að skoða gröf tímaraða yfir skilaboðin þín í Microsoft Dynamics 365 Supply Chain Management þarftu að setja upp mælieiningarnar með því að fylgja þessum skrefum.

1. Afritaðu tengistrenginn fyrir Redis-skyndiminni:

    1. Í Azure-gáttinni skal fara í Redis-skyndiminni.
    2. Farðu í **Stillingar** \> **Aðgangslyklar**.
    3. Afritið gildið í reitnum **Aðaltengistrengur**.

2. Í Supply Chain Management er farið í **Framleiðslustýring \> Uppsetning \> IoT-gervigreind \> Færibreytur atburðarásar**.
3. Á síðunni **Færibreytur atburðarásar**, á flipanum **Tímaröð**, í reitnum **Tengistrengur fyrir mælingageymslu Redis**, skal líma tengistrenginn sem var afritaður hér á undan. Þetta skref gerir kleift að sjá mælieiningar úr Azure IoT Hub á myndrænan hátt í Supply Chain Management. Þegar gildið er límt í reitinn er það sýnt sem **\*\*\*\*\*\***.

    > [!NOTE]
    > Í hvert sinn sem þú uppfærir tengistreng Redis-skyndiminnis þarftu einnig að uppfæra þennan reit.

4. Farðu í **Framleiðslustýring \> Fyrirspurnir og skýrslur \> IoT-gervigreind \> Mælingalyklar**.
5. Á síðunni **Mælingalyklar** skal velja **Uppfæra**.
6. Í svarglugganum **Uppfæra mælilykla** skaltu taka eftir því að **Keyra í bakgrunni** er valið í reitnum. Veldu **Í lagi**.

Allir mælingalyklarnir í Redis-skyndiminninu eru sóttir og þeim bætt við listann **Mælingalyklar**. Mælingagildi birtast ekki fyrr en þú [virkjar aðstæðurnar](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>Skilgreina tímaröð tilfangastöðu

Til að stilla tímaröð **Tilfangastöðu** skal fylgja þessum skrefum.

1. Í Supply Chain Management er farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Staða tilfanga**.
2. Á síðunni **Staða tilfanga** skal velja **Stilla**.
2. Í svarglugganum **Stilla**, í listanum **Tilfang**, skal velja atriði til að fylgjast með.
3. Veldu hnappinn **Breyta** fyrir **Tímaröð 1**.
4. Í svarglugganum **Velja tímaröð** skal velja mælieiningu í hnitanetinu. (Einnig er hægt að nota tengilinn **Uppfæra mælingalykla** til að uppfæra mælingalykla úr þessum svarglugga.)
5. Veldu **Í lagi** til að fara aftur í svargluggann **Stilla**.
6. Sláðu inn birtingarnafn.
7. Í reitnum **Sýna gögn frá** skal velja tímaramma.
8. Veldu **Í lagi**.

Grafið er sýnt.

## <a name="delete-a-metric-key"></a>Eyða mælingalykli

1. Í Supply Chain Management skal fara í **Framleiðslustýring \> Fyrirspurnir og skýrslur \> IoT-gervigreind \> Mælingalyklar**.
2. Á síðunni **Mælingalyklar** skal velja mælingalykilinn sem á að eyða.
3. Veljið **Eyða**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
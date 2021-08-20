---
title: Reikna álag
description: Þetta efni útskýrir hvernig á að reikna út álag í eignastýringu.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eed75cd5268b19d819d42e764bdbb5e6f4c79a0a732c5023b3fc40da798e2ca1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757879"
---
# <a name="calculate-capacity-load"></a>Reikna álag

[!include [banner](../../includes/banner.md)]


Í eignastjórnun geturðu reiknað út álag á:

- áætlunarlínur viðhalds  
- verkbeiðnir sem hafa ekki enn verið áætlaðar  
- áætlaðar verkbeiðnir

Þetta er gagnlegt ef þú vilt fá yfirsýn yfir áætlað álag yfir ákveðið tímabil. Hægt er að gera útreikning á álagi á allar eignir eða valdar eignir. Þú getur líka gert útreikning á aðgerðum niðurtíma vegna viðhalds eða verkbeiðnahópum.

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Álag**, eða **Eignastýring** > **Sameiginlegt** > **Verkbeiðnihópar** > **Allir verkbeiðnihópar** / **Virkir verkbeiðnihópar** > veldu verkbeiðnihóp af listanum > hnappinum **Álag**, eða **Eignastýringu** > **Sameiginlegt** > **Niðurtími vegna viðhalds** > **Allur niðurtími vegna viðhalds** / **Virkur niðurtími vegna viðhalds** > veldu viðhaldsaðgerðir á listanum > hnappnum **Álag**.

2. Í glugganum **Reikna álag** velurðu tímabil fyrir útreikninginn í reitunum **Upphafsdagsetning/-tími** og **Lokadagsetning/-tími**.

3. Veldu „Já“ á skiptihnappnum **Hafa viðhaldsskema með** ef þú vilt láta viðhaldsskemalínur fylgja með í útreikningnum.

4. Veldu „Já“ á skiptihnappnum **Hafa verkbeiðni með** ef þú vilt láta verkbeiðnivinnslur fylgja með í útreikningnum.

5. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að álagslínur séu varðandi virkar staðsetningar. 

    Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur og verkbeiðnir fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. 
    
    Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar viðhaldsskemalínur og allar verkbeiðnir á öllum virkum staðsetningarstigum sem þær tengjast.

6. Smellið á **Í lagi** til að byrja að reikna.

7. Í hópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn. Í skjámyndinni hér að neðan eru valdir hnappar **Flokka eftir** auðkenndir með bláum lit. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

    ![Mynd 1.](media/01-capacity-planning.png)

>[!NOTE]
>Ef þú vilt einbeita þér aðeins að afkastagetuáætlun varðandi áætlaðar verkbeiðnir skal sjá [Reikna álag á áætlaðar verkbeiðnir](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
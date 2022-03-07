---
title: Kostnaðarstýring eignavillu
description: Þetta efni skýrir kostnaðarstýringu eignabilunar í eignastýringu.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c36fc791fac6cce0433935adb88eb8cdc23003368204a87efc12cf5a419ec9d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752034"
---
# <a name="asset-fault-cost-control"></a>Kostnaðarstýring eignavillu

[!include [banner](../../includes/banner.md)]

 

Í eignastýringu er hægt að reikna út kostnað vegna skráningar á eignabilunum til að fá yfirlit yfir raunkostnað miðað við kostnað fjárhagsáætlunar. Raunkostnaður byggist á bókfærðum færslum. Dagsetningin er bilunardagsetningin sem einkennið var skráð á.

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Kostnaðarstýringu eignabilunar**.

2. Í valmyndinni **Kostnaðarstýring eignabilunar** velurðu fjárhagsvídd sem sett er inn í útreikninginn, ef þess þarf.

4. Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með kostnað við núll.

5. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að kostnaðarstýringarlínur séu varðandi virkar staðsetningar. 

    Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar kostnaðarstýringarlínur eignabilunar fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. 
    
    Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar kostnaðarstýringarlínur eignabilana á öllum virkum staðsetningarstigum sem þær tengjast.

6. Ef þú vilt takmarka leitina geturðu valið sérstakar eignir, bilunardagsetningar og bilunarástæður á flýtiflipanum **Færslur til að taka með**.

7. Smellið á **Í lagi** til að byrja að reikna.

8. Smelltu á hnappana **Flokka eftir** til að sýna nauðsynleg smáatriði við útreikninginn. Valdir hnappar **Flokka eftir** eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

## <a name="example"></a>Dæmi

Þetta dæmi sýnir útreikning á kostnaðarstýringu eignabilunar.

- Reiturinn **Upprunaleg fjárhagsáætlun** sýnir fjárhagsáætlunarkostnað vegna kostnaðar við spá um verkbeiðni. 
- Reiturinn **Raunkostnaður** sýnir bókaðan kostnað vegna verkbeiðna. 
- Reiturinn **Ráðstafaður kostnaður** sýnir heildarkostnað sem fyrirtækið þitt skuldbindur sig til vegna verkbeiðna.

    ![Mynd 1.](media/05-controlling-and-reporting.png)

Upplýsingar um hvernig setja skuli upp bilanir er að finna í efnisatriðinu [Bilanastjórnun](../setup-for-work-orders/fault-management.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
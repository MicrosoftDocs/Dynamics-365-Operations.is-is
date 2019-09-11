---
title: Kostnaðarstýring eignavillu
description: Þetta efni skýrir kostnaðarstýringu eignabilunar í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918304"
---
# <a name="asset-fault-cost-control"></a>Kostnaðarstýring eignavillu

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Í eignastýringu er hægt að reikna út kostnað vegna skráningar á eignabilunum til að fá yfirlit yfir raunkostnað miðað við kostnað fjárhagsáætlunar vegna bilunar. Raunkostnaður byggist á bókfærðum færslum. Dagsetningin er bilunardagsetningin sem einkennið var skráð á.

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Kostnaðarstýringu eignabilunar**.

2. Í valmyndinni **Kostnaðarstýring eignabilunar** velurðu fjárhagsvídd sem sett er inn í útreikninginn, ef þess þarf.

4. Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með kostnað við núll.

5. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að kostnaðarstýringarlínur séu varðandi virkar staðsetningar. Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar kostnaðarstýringarlínur eignabilunar fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar kostnaðarstýringarlínur eignabilana á öllum virkum staðsetningarstigum sem þær tengjast.

6. Ef þú vilt takmarka leitina geturðu valið sérstakar eignir, bilunardagsetningar og bilunarástæður á flýtiflipanum **Færslur til að taka með**.

7. Smellið á **Í lagi** til að byrja að reikna.

8. Í aðgerðarrúðahópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn. Valdir aðgerðarrúðahnappar eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

Myndin hér að neðan sýnir dæmi um útreikning á kostnaðarstýringu eigna vegna villu.

![Mynd 1](media/05-controlling-and-reporting.png)

Sjá kaflann [Bilanastjórnun](../setup-for-work-orders/fault-management.md) til að fá upplýsingar um hvernig á að setja upp bilanir.

>[!NOTE]
>Reiturinn **Upprunaleg fjárhagsáætlun** sýnir fjárhagsáætlunarkostnað vegna kostnaðar við spá um verkbeiðni. Reiturinn **Raunkostnaður** sýnir bókaðan kostnað vegna verkbeiðna. Reiturinn **Ráðstafaður kostnaður** sýnir heildarkostnað sem fyrirtækið þitt skuldbindur sig til vegna verkbeiðna.


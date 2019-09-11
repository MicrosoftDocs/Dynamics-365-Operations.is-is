---
title: Reikna vöruspá
description: Þetta efni útskýrir hvernig á að reikna út vöruspá í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 9091ff7a394cd08b68e78c8f668d7cd962003e6d
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886771"
---
# <a name="calculate-item-forecast"></a>Reikna vöruspá

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Rétt eins og þú getur gert útreikninga á álagi, sem lýst er í fyrri hlutanum, geturðu einnig gert vöruspárútreikninga á

- Áætlunarlínur viðhalds  
- Verkbeiðnir sem hafa ekki enn verið áætlaðar  
- Verkbeiðnir á dagskrá

Þetta er gagnlegt ef þú vilt fá yfirsýn yfir væntanlega notkun vöru (varahluti sem og aðrar vörur sem þarf til að ljúka verkbeiðnum) fyrir tiltekið tímabil. Hægt er að gera útreikning á vöruspá á allar eignir eða valdar eignir. Þú getur líka gert útreikninga á aðgerðum niðurtíma vegna viðhalds (**Allar aðgerðir niðurtíma vegna viðhalds** eða **Aðgerðir virks niðurtíma vegna viðhalds**) eða í verkbeiðnasafni (**Öll verkbeiðnasöfn** eða **Virk verkbeiðnasöfn**).

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Vöruspá**, eða **Eignastýring** > **Sameiginlegt** > **Verkbeiðnihópar** > **Allir verkbeiðnihópar** / **Virkir verkbeiðnihópar** > veldu verkbeiðnihóp af listanum > hnappinum **Vöruspá**, eða **Eignastýringu** > **Sameiginlegt** > **Niðurtími vegna viðhalds** > **Allur niðurtími vegna viðhalds** / **Virkur niðurtími vegna viðhalds** > veldu niðurtímaaðgerðir vegna viðhalds á listanum > hnappnum **Vöruspá**.

2. Í glugganum **Reikna vöruspá** velurðu tímabil fyrir útreikninginn í reitunum **Upphafsdagsetning/-tími** og **Lokadagsetning/-tími**.

3. Veldu „Já“ á skiptihnappnum **Hafa viðhaldsskema með** ef þú vilt láta viðhaldsskemalínur fylgja með í vöruspárútreikningnum.

4. Veldu „Já“ á skiptihnappnum **Hafa verkbeiðni með** ef þú vilt láta verkbeiðnivinnslur fylgja með í spárútreikningnum.

5. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að vöruspárlínur séu varðandi virkar staðsetningar. Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur og verkbeiðnir fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar viðhaldsskemalínur og allar verkbeiðnir á öllum virkum staðsetningarstigum sem þær tengjast.

6. Smellið á **Í lagi** til að byrja að reikna.

7. Í aðgerðarrúðahópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn. Valdir aðgerðarrúðuhópshnappar eru auðkenndir í bláum lit. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

8. Smelltu á hnappinn **Sýna víddir** ef þú vilt sjá afurð, geymslu eða rakningarvíddir sem tengjast vörunum. Veldu viðeigandi gátreiti og smelltu á **Í lagi**.

Myndin hér að neðan sýnir skjámynd af viðmótinu.

![Mynd 1](media/02-capacity-planning.png)

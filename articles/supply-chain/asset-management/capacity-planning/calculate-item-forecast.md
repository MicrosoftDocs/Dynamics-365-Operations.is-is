---
title: Reikna vöruspá
description: Í þessari grein er útskýrt hvernig á að reikna út spá í Eignastýringu.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 25e9b00533fb183b27c1bbe616cf6f414b44b5e7
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016102"
---
# <a name="calculate-item-forecast"></a>Reikna vöruspá

[!include [banner](../../includes/banner.md)]

 

Rétt eins og þú getur gert útreikninga á álagi, sem lýst er í fyrri hlutanum, geturðu einnig gert vöruspárútreikninga á:

- áætlunarlínur viðhalds  
- verkbeiðnir sem hafa ekki enn verið áætlaðar  
- áætlaðar verkbeiðnir

Þetta er gagnlegt ef þú vilt fá yfirsýn yfir væntanlega notkun vöru (varahluti sem og aðrar vörur sem þarf til að ljúka verkbeiðnum) fyrir tiltekið tímabil. Hægt er að gera útreikning á vöruspá á allar eignir eða valdar eignir. Þú getur líka gert útreikninga á aðgerðum niðurtíma vegna viðhalds (**Allar aðgerðir niðurtíma vegna viðhalds** eða **Aðgerðir virks niðurtíma vegna viðhalds**) eða í verkbeiðnasafni (**Öll verkbeiðnasöfn** eða **Virk verkbeiðnasöfn**).

1. Smelltu á **Eignastýring** > **Fyrirspurnir** > **Vöruspá** eða **Eignastýring** > **Verkbeiðnihópar** > **Allir verkbeiðnihópar** / **Virkir verkbeiðnihópar** > veldu verkbeiðnihóp í listanum > hnappurinn **Vöruspá** eða **Eignastýring** > **Niðurtímaaðgerðir vegna viðhalds** > **Allar niðurtímaaðgerðir vegna viðhalds** / **Virkar niðurtímaaðgerðir vegna viðhalds** > velja niðurtímaaðgerð vegna viðhalds í listanum > hnappurinn **Vöruspá**.

2. Í glugganum **Reikna vöruspá** velurðu tímabil fyrir útreikninginn í reitunum **Upphafsdagsetning/-tími** og **Lokadagsetning/-tími**.

3. Veldu „Já“ á skiptihnappnum **Hafa viðhaldsskema með** ef þú vilt láta viðhaldsskemalínur fylgja með í vöruspárútreikningnum.

4. Veldu „Já“ á skiptihnappnum **Hafa verkbeiðni með** ef þú vilt láta verkbeiðnivinnslur fylgja með í spárútreikningnum.

5. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að vöruspárlínur séu varðandi virkar staðsetningar. 

      Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur og verkbeiðnir fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. 
  
      Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar viðhaldsskemalínur og allar verkbeiðnir á öllum virkum staðsetningarstigum sem þær tengjast.

6. Smellið á **Í lagi** til að byrja að reikna.

7. Í hópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn. Í skjámyndinni hér að neðan eru valdir hnappar **Flokka eftir** auðkenndir með bláum lit. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

8. Smelltu á hnappinn **Sýna víddir** ef þú vilt sjá afurð, geymslu eða rakningarvíddir sem tengjast vörunum. Veldu viðeigandi gátreiti og smelltu á **Í lagi**.

![Mynd 1.](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
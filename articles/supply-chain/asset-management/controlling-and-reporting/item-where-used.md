---
title: Notkunarstaður vöru
description: Þetta efni útskýrir hvernig á að fá yfirlit yfir hvar hlutur er notaður í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: db0932c5a52030c1a7f0411163aee120e2173ca0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021140"
---
# <a name="item-where-used"></a>Notkunarstaður vöru

[!include [banner](../../includes/banner.md)]

 

Þú getur gert útreikning fyrir tiltekinn hlut til að fá yfirlit yfir hvar í eignastjórnun hluturinn hefur verið notaður. Niðurstöðurnar sýna samhengið sem hluturinn hefur verið notaður á meðan á líftíma hans stóð. Síðuna **Notkunarstaður vöru** er hægt að opna í aðalvalmyndinni fyrir eignastjórnun og einnig er hægt að nálgast hana af eftirfarandi síðum:

- [Eignauppskriftir](../objects/object-BOM.md)

- [Varahlutir í sjálfgefinni tegund eigna](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [Flokkar viðhaldsverkgerðar og viðhaldsverkgerðir, afbrigði viðhaldsverkgerðar, viðskipti viðhaldsvinnslu og viðhaldsgátlistar](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [Viðhaldsspá](../work-orders/maintenance-forecasts.md)

- [Innkaup](../work-orders/procurement.md)

- [Innkaup verkbeiðni](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Gerðu útreikning notkunarstað vöru

1. Smelltu á **Eignastjórnun** > **Fyrirspurnir** > **Notkunarstaður vöru** eða veldu hnappinn **Notkunarstaður vöru** á einni af síðunum sem nefndar eru hér að ofan.

2. Í glugganum **Notkunarstaður vöru** skaltu velja hlutinn sem þú vilt gera útreikning fyrir í reitnum **Vörunúmer**.

3. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að vörulínur séu varðandi virkar staðsetningar. 

    Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa virkt staðsetningarskipulag, verða allar vörulínur fyrir virka staðsetningu sýndar á efsta þrepi. Þess vegna er hægt að bæta tengslum/magni á línu frá virkum staðsetningum sem eru staðsettar á lægra stigi. 
    
    Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar vörulínur á öllum virkum staðsetningarstigum sem þær tengjast.

4. Í hlutanum **Hafa með** velurðu „Já“ á skiptihnöppunum sem þú vilt hafa með í útreikningnum.

5. Smellið á **Í lagi** til að byrja að reikna.

6. Á flipanum **Notkunarstaður vöru** velurðu hnappana **Flokka eftir** til að sýna nauðsynleg smáatriði við útreikninginn. Valdir hnappar **Flokka eftir** eru auðkenndir. Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.

7. Ef þú vilt sýna mál sem tengjast vörunni skaltu smella á **Sýna víddir** og velja víddirnar sem á að sýna.

## <a name="example"></a>Dæmi

Á skjámyndinni hér að neðan sérðu dæmi um útreikning á vöru þar sem notað er vörunúmerið "1000".

![Dæmi um útreikning á notkunarstað vöru](media/12-controlling-and-reporting.png)


---
title: Birgðamörk staðsetningar
description: Þetta efnisatriði lýsir virkni fyrir birgðamörk staðsetningar.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e0adb9d05f0db9bbfe6bfbe72564a4e5e839f163
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004577"
---
# <a name="location-stocking-limits"></a>Birgðamörk staðsetningar

[!include [banner](../includes/banner.md)]

Þú getur notað **Birgðamörk staðsetningar** (**Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Birgðamörk staðsetningar**) til að hafa umsjón með afkastagetu farms á staðsetningum vöruhúss án þess að þurfa að nota ítarlegri ferla fyrir rúmmálsútreikninga á efnislegum afurðum.

Tilgangurinn með birgðamörk staðsetningar er að meta hámarksmagn sem staðsetning getur innihaldið. Hægt er að setja upp eiginleikann á einhverju af stigunum þremur, sem hvert um sig er með eigin flipa á síðunni **Birgðamörk staðsetningar**:

- Afurðir
- Afurðarafbrigði
- Tegundir gáma

Fyrir hvert stig er hægt að skilgreina mismunandi reitargildi. Kerfið mun síðan meta afkastagetu tiltekinnar staðsetningar, byggt á **Magn** og **Eining** gildinu fyrir hverja línu. Það velur fyrst nákvæmustu jöfnunarfærsluna. Til dæmis verður lína sem hefur gildið í **Kenni staðsetningarforstillingar** metin fyrir línu sem er aðeins með gildi í **Vöruhúsi**. Eftirstöðvar afkastagetu verða einnig metnar á grundvelli gildisins **Magn** fyrir færslu í birgðamörkum staðsetningar.

Í hlutanum **Vörur** hluta síðunnar er hægt að skilgreina eftirfarandi reitargildi fyrir leit að birgðamörkum staðsetningar:

- Vöruhús
- Auðkenni forstillingar staðsetningar
- Staður
- Auðkenni stærðarflokks umbúða
- Vörunúmer
- Eining

> [!NOTE]
> Ekki þarf að skilgreina gildið **Eining** fyrir hverja staðsetningu birgðamarksmarka. Útreikningar afkastagetu staðsetningar verða byggðir á magni birgðaeininga. Ef engin einingaumreikningur er skilgreindur fyrir gildi sem er notað er takmörkunarfærslu staðsetningar sleppt þar sem annað **Vörunúmer** er skilgreint fyrir það.

## <a name="example--purchase-order-receiving"></a>Dæmi: Móttaka innkaupapöntunar

Þetta dæmi miðast við hreint *USMF* sýnigagnasett, þar sem eftirfarandi gildi eru stillt á flipanum **Afurðarafbrigði** á síðunni **Birgðamörk staðsetningar**.

| Vöruhús | Auðkenni forstillingar staðsetningar | Vörunúmer | Stærð | Magn | Eining |
|-----------|---------------------|-------------|------|----------|------|
| 24        | Hæð               | D0013       | M    | 300      | Ea   |
| 24        | Hæð               | D0013       | L    | 240      | Ea   |
| 24        | Hæð               | D0013       | L    | 360      | Ea   |

Mismunandi mælieiningar afurðarafbrigða eru settar upp fyrir afurðirnar. Þessi afbrigði eru jöfnuð við birgðamörk staðsetningar fyrir þrjú bretti (PL):

- **Stærð M:** 1 PL = 100 hver (Ea)
- **Stærð L:** 1 PL = 80 ea
- **Stærð S:** 1 PL = 120 Ea

Þess vegna getur hver staðsetning þar sem **Kenni staðsetningarforstillingar** er stillt á *GÓLF* borið *3* *PL* af vörunúmeri *D0013*.

### <a name="prepare-for-the-example"></a>Undirbúa dæmið

Í þessu dæmi er viðtökuflæði innkaupapöntunar fyrir tvær línur keyrt. Hins vegar verður fyrst að uppfæra sýnigögnin á eftirfarandi hátt til að tryggja að staðsetningar leyfi blandaðar vörur sem á að framkvæma, aðeins auðar staðsetningar *FL-002* til *FL-004* eru notaðar og engin opin vinna er á innleið.

1. Fyrir staðsetningu *FL-001* skal breyta gildinu í **Staðsetningarforstillingunni** úr *FLOOR* í *FLOOR-05*.
1. Fyrir *GÓF* staðsetningarforstillinguna skal stilla **Leyfa blandaðar vörur** valkostinn á *Já*.
1. Stofna innkaupapöntun sem er með eftirfarandi tvær línur.

    | Vöruhús | Vörunúmer | Stærð | Magn | Eining |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | L    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Vinna úr dæmi

Þú munt fyrst fá magn af *4* af einingu *PL* í stærðinni *S*, og yfirfara staðsetningarlínur fyrir vinnuna sem er stofnuð. Þú munt síðan fá magn af *4* af einingu *PL* í stærðinni *L* og yfirfara staðsetningarlínustaðsetningar fyrir vinnuna sem er stofnuð.

1. Í vöruhúsaforritinu skal skrá sig inn með því að nota *24* sem notandakenni og *1* sem aðgangsorð.
1. Veljið **Innleið** \> **Móttaka innkaupa**.
1. Taka á móti *4* *stk* af vörunúmeri *D0013* í stærðinni *L*.
1. Yfirfara vinnu frágangsvinnu sem var stofnuð. Þú ættir að sjá eftirfarandi niðurstöður:

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Taka á móti *4* *stk* af vörunúmeri *D0013* í stærðinni *L*.
1. Yfirfara vinnu frágangsvinnu sem var stofnuð. Þú ættir að sjá eftirfarandi niðurstöður:

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

Miðað við niðurstöðurnar kemst þú hugsanlega að þeirri niðurstöðu að kerfinu hafi mistekist að úthluta réttum staðsetningum frágangs. Hvers vegna bætti kerfið annars aðeins *1* *PL* af stærðinni *L* á staðsetningu *FL-003* í síðasta skrefi og ekki *2* *PL*? Hvers vegna er ekki *3* *PL* fyrir frágangsvinnu á þá staðsetningu?

Til að útskýra þessa bilun þarf að skilja valskilyrðin fyrir birgðamörk staðsetningar. Kerfið velur nákvæmustu jöfnunarfærsluna. Í þessu dæmi er nákvæmasta samsvarandi færsla sú lína þar sem gildið **Stærð** er *L*, **Magn** er *240*, og gildið **Eining** er *Ea*. Þar sem þú ert þegar með opna vinnu frá fyrri kvittun magns af *120* *Ea* af stærðinni *S* eru eftirstöðvar afkastagetu reiknaðar sem *240* – *120* = *120* *Ea*. Þess vegna getur eftirstandandi afkastageta aðeins borið *1* *PL* af *80* *Ea*.

> [!NOTE]
> Ekki er hægt að nota birgðatakmarkanir staðsetningar til að hafa stjórnun, til dæmis, áfyllingu á vörum sem hafa annað magn á sama stað. Í þessu tilvikum skal nota *áfyllingarsniðmát*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
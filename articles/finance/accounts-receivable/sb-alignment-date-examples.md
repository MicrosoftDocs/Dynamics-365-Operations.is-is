---
title: Atburðarás fyrir jöfnunardagsetningu
description: Þetta efnisatriði gefur dæmi sem sýna hvernig jöfnunardagsetningar virka í áskriftarreikningi.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e80797e8dd532bb4b2ef78422b459487430d83d6
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629716"
---
# <a name="alignment-date-scenarios"></a>Atburðarás fyrir jöfnunardagsetningu

Þetta efnisatriði gefur dæmi sem sýna hvernig jöfnunardagsetningar virka í áskriftarreikningi.

Fyrir þessi dæmi, innheimtuupplýsingar fyrir innheimtuáætlun hefur jöfnunardagsetningu 31. október 2019. Fyrstu innheimtuupplýsingar fyrir línuna lýkur 31. október 2019 og er hlutfallslegt í samræmi við það. Línan endurnýjast sjálfkrafa með því að nota upphafsdag endurnýjunar 11. nóvember.

> [!NOTE]
> Árið skiptir máli vegna þess að það getur valdið því að jöfnunardagsetningin er meira eða minna en ár. Fyrir þessi dæmi er hlutfallsaðferðin stillt á **Mánaðarlega** á **Endurteknar innheimtufæribreytur samnings** síðu. Ef það er stillt á **Daglega**, sumar hlutafjárhæðir verða mismunandi.

## <a name="scenario-1-no-alignment"></a>Atburðarás 1: Engin jöfnun

Innheimtuáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagur:** 1. maí 2019
- **Loka dagsetning:** 31. desember 2024
- **Magn:** $1,000

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 30/4/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2020 | 4/30/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2021 | 4/30/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2022 | 4/30/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2023 | 4/30/2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>Sviðsmynd 2: Stytta röðun

Innheimtuáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagur:** 1. maí 2019
- **Loka dagsetning:** 31. desember 2024
- **Magn:** $1,000
- **Jöfnunardagur:** 31. desember 2019

Fyrsta endurnýjunarupphæð er til skemmri tíma en eins árs.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 1/1/2020 | 31/12/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>Atburðarás 3: Lengri jöfnun

Innheimtuáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagur:** 1. maí 2019
- **Loka dagsetning:** 31. desember 2024
- **Magn:** $1,000
- **Jöfnunardagur:** 31. desember 2020

Fyrsta endurnýjunarupphæð er til meira en eins árs.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 31/12/2020 | | | 1.00 | | 1.00 | 1,666.67 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>Sviðsmynd 4: Samræming við annan lokamánuð

Innheimtuáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagur:** 1. maí 2019
- **Loka dagsetning:** 31. október 2024
- **Magn:** $1,000
- **Jöfnunardagur:** 31. desember 2019

> [!NOTE]
> Þessi atburðarás er ekki algeng.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 1/1/2020 | 31/12/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>Sviðsmynd 5: Eitt ár að hluta

Innheimtuáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagur:** 1. maí 2019
- **Loka dagsetning:** 31. desember 2019
- **Magn:** $1,000
- **Jöfnunardagur** : 31. desember 2019

Í þessari atburðarás er jöfnunardagsetningin ekki nauðsynleg. Þessi atburðarás er algeng fyrir sjálfvirka endurnýjun.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>Sviðsmynd 6: Reiknaðar dagsetningar

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hneka upphafsdagsetningu:** Nei
- **Upphafsdagsetningar stuðnings og endurnýjunar:** Upphaf næsta mánaðar
- **Bókunardagur reiknings:** 22. júní 2019
- **Jöfnunardagur:** 31. desember 2020

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 7/1/2019 | 7/31/2019 | | | 1.00 | | 1.00 | 297.60 |
| 8/1/2019 | 31/12/2020 | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>Atburðarás 7: Reiknaðar dagsetningar og framtíðarfærslur

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hneka upphafsdagsetningu:** Nei
- **Upphafsdagsetningar stuðnings og endurnýjunar:** Upphaf næsta mánaðar
- **Bókunardagur reiknings:** 22. júní 2019
- **Jöfnunardagur:** 31. desember 2020

Fyrir þessa atburðarás er jöfnunardagsetningunni breytt í 31. desember 2021.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 8/1/2019 | 31/12/2020 | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Atburðarás 8: Handvirkar dagsetningar og mörg ár

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hneka upphafsdagsetningu:** Já
- **Upphafsdagur endurnýjunar:** 1. júlí 2020
- **Lokadagur endurnýjunar:** 31. desember 2024
- **Jöfnunardagur:** 31. desember 2021

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Atburðarás 9: Handvirkar dagsetningar, mörg ár og annar lokamánuður

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hneka upphafsdagsetningu:** Já
- **Upphafsdagur endurnýjunar:** 1. júlí 2020
- **Lokadagur endurnýjunar:** 31. október 2024
- **Jöfnunardagur:** 31. desember 2021

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>Atburðarás 10: Jöfnun án hlutfalls

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hneka upphafsdagsetningu:** Nei
- **Bókunardagur reiknings:** 22. júní 2019
- **Jöfnunardagur:** 31. desember 2019

Upphafsdagur endurnýjunar og jöfnunardagsetningar eru leiðréttar þannig að báðar upphafsdagsetningar séu eftir bókunardagsetningu.

- **Upphafsdagur endurnýjunar:** 1. janúar 2020
- **Lokadagur endurnýjunar:** 31. desember 2020

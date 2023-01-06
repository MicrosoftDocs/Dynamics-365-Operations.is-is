---
title: Aðstæður fyrir dagsetningu stillingar
description: Í þessari grein eru dæmi sem sýna hvernig samræmdar dagsetningar virka í áskriftargreiðslum.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 102e3a104be5be287f914172160e95aff65d0b18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872616"
---
# <a name="alignment-date-scenarios"></a>Aðstæður fyrir dagsetningu stillingar

Í þessari grein eru dæmi sem sýna hvernig samræmdar dagsetningar virka í áskriftargreiðslum.

Í þessum dæmum eru greiðsluupplýsingar fyrir greiðsluáætlun með samsræmingardaginn 31. október 2019. Fyrsta greiðsluupplýsingarnar fyrir línuna endar þann 31. október 2019 og er hlutfallslega skipt í samræmi við það. Línan er endurnýjuð sjálfkrafa með því að nota upphafsdagsetningu endurnýjunar 11. nóvember.

> [!NOTE]
> Árið skiptir máli vegna þess að það getur valdið því að samræmingardagurinn sé meira eða minna en ár. Fyrir þessi dæmi er aðferð hlutfallsskiptingar stillt á **Mánaðarlega** á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**. Ef hún er stillt á **Daglega** munu sumar hlutaupphæðir vera mismunandi.

## <a name="scenario-1-no-alignment"></a>Aðstæður 1: Engin samræming

Greiðsluáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagsetning:** 1. maí 2019
- **Lokadagsetning:** 31. desember 2024
- **Fjárhæð:** USD 1.000

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 1/5/2019 | 30/4/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/5/2020 | 30/4/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/5/2021 | 30/4/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/5/2022 | 30/4/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/5/2023 | 30/4/2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/5/2024 | 31/12/2024 | | | 1.00 | | 1.00 | 666,67 |

## <a name="scenario-2-shortened-alignment"></a>Aðstæður 2: Styttri samræming

Greiðsluáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagsetning:** 1. maí 2019
- **Lokadagsetning:** 31. desember 2024
- **Fjárhæð:** USD 1.000
- **Dagsetning röðunar**: 31. desember, 2019

Fyrsta endurnýjunarfjárhæð gildir í minna en eitt ár.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 1/5/2019 | 31/12/2019 | | | 1.00 | | 1.00 | 666,67 |
| 1/1/2020 | 31/12/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 31/12/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 31/12/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 31/12/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 31/12/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>Aðstæður 3: Lengri samræming

Greiðsluáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagsetning:** 1. maí 2019
- **Lokadagsetning:** 31. desember 2024
- **Fjárhæð:** USD 1.000
- **Dagsetning röðunar**: 31. desember, 2020

Fyrsta endurnýjunarfjárhæð gildir í meira en eitt ár.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 1/5/2019 | 31/12/2020 | | | 1.00 | | 1.00 | 1.666,67 |
| 1/1/2021 | 31/12/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 31/12/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 31/12/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 31/12/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>Aðstæður 4: Samræming með mismunandi lokamánuði

Greiðsluáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagsetning:** 1. maí 2019
- **Lokadagsetning:** 31. október 2024
- **Fjárhæð:** USD 1.000
- **Dagsetning röðunar**: 31. desember, 2019

> [!NOTE]
> Þessar aðstæður eru ekki algengar.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 1/5/2019 | 31/12/2019 | | | 1.00 | | 1.00 | 666,67 |
| 1/1/2020 | 31/12/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 31/12/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 31/12/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 31/12/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 31/10/2024 | | | 1.00 | | 1.00 | 833,33 |

## <a name="scenario-5-single-partial-year"></a>Aðstæður 5: Hluti úr ári

Greiðsluáætlunin er sett upp með eftirfarandi gögnum:

- **Upphafsdagsetning:** 1. maí 2019
- **Lokadagsetning:** 31. desember 2019
- **Fjárhæð:** USD 1.000
- **Dagsetning röðunar**: 31. desember, 2019

Í þessum aðstæðum er samræmingardagurinn ekki nauðsynlegur. Þessar aðstæður eru algengar fyrir sjálfvirka endurnýjun.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 1/5/2019 | 31/12/2019 | | | 1.00 | | 1.00 | 666,67 |

## <a name="scenario-6-calculated-dates"></a>Aðstæður 6: Reiknaðar dagsetningar

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hnekkja upphafsdagsetningu:** Nei
- **Upphafsdagsetningar þjónustu og endurnýjunar:** Frá og með næsta mánuði
- **Bókunardagsetning reiknings:** 22. júní 2019
- **Dagsetning röðunar**: 31. desember, 2020

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 1/7/2019 | 31/7/2019 | | | 1.00 | | 1.00 | 297,60 |
| 1/8/2019 | 31/12/2020 | | | 1.00 | | 1.00 | 6.936,00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>Sviðsmynd 7: Reiknaðar dagsetningar og bókanir eftir þær

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hnekkja upphafsdagsetningu:** Nei
- **Upphafsdagsetningar þjónustu og endurnýjunar:** Frá og með næsta mánuði
- **Bókunardagsetning reiknings:** 22. júní 2019
- **Dagsetning röðunar**: 31. desember, 2020

Í þessum aðstæðum er samræmingardeginum breytt í 31. desember 2021.

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 22/6/2019 | 22/6/2019 | | | 1.00 | | 1.00 | 0,00 |
| 1/8/2019 | 31/12/2020 | | | 1.00 | | 1.00 | 4.250,00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Sviðsmynd 8: Handvirkar dagsetningar og mörg ár

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hnekkja upphafsdagsetningu:** Já
- **Upphafsdagur endurnýjunar:** 1. júlí 2020
- **Lokadagsetning endurnýjunar:** 31. desember 2024
- **Dagsetning röðunar**: 31. desember, 2021

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 22/6/2019 | 22/6/2019 | | | 1.00 | | 1.00 | 0,00 |
| 1/7/2020 | 31/12/2021 | | | 1.00 | | 1.00 | 375,00 |
| 1/1/2022 | 31/12/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 31/12/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 31/12/2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Aðstæður 9: Handvirkar dagsetningar, mörg ár og annar lokamánuður

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hnekkja upphafsdagsetningu:** Já
- **Upphafsdagur endurnýjunar:** 1. júlí 2020
- **Lokadagur endurnýjunar:** 31. október 2024
- **Dagsetning röðunar**: 31. desember, 2021

| Upphafsdagsetning innheimtu | Lokadagsetning innheimtu | Fyrri lestur | Núverandi lestur | Magn fært inn | Óráðstafað magn | Reikningshæft magn | Einingarverð |
|---|---|---|---|---|---|---|---|
| 22/6/2019 | 22/6/2019 | | | 1.00 | | 1.00 | 0,00 |
| 1/7/2020 | 31/12/2021 | | | 1.00 | | 1.00 | 375,00 |
| 1/1/2022 | 31/12/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 31/12/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 31/10/2024 | | | 1.00 | | 1.00 | 208,33 |

## <a name="scenario-10-alignment-without-proration"></a>Aðstæður 10: Samræming án hlutfallslegrar skiptingar

Stuðningurinn og endurnýjunin er sett upp með eftirfarandi gögnum:

- **Hnekkja upphafsdagsetningu:** Nei
- **Bókunardagsetning reiknings:** 22. júní 2019
- **Dagsetning röðunar**: 31. desember, 2019

Upphafsdagsetningu endurnýjunar og samræmingardögunum er breytt þannig að báðar upphafsdagsetningarnar koma á eftir bókunardagsetningunni.

- **Upphafsdagur endurnýjunar:** 1. janúar 2020
- **Lokadagsetning endurnýjunar:** 31. desember 2020

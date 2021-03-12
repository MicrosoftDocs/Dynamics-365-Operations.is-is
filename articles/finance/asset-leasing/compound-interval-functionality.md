---
title: Virkni samsetts tímabils
description: Þetta efnisatriði veitir upplýsingar sem gera notanda kleift að velja á milli mánaðarlegra, ársfjórðungslegra, hálfsárslegra og árslegra tímabila.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5978abfd4341bbca76ff0211f029097c3d2d785c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971454"
---
# <a name="compounding-interval-functionality"></a>Virkni samsetts tímabils

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði veitir upplýsingar sem gera notanda kleift að velja á milli mánaðarlegra, ársfjórðungslegra, hálfsárslegra og árslegra tímabila. Samsett tímabil eru notuð til að ákvarða fjölda samsettra tímabila á ári í greiðsluáætlun leigusamnings. Hvert af fjórum dæmunum í þessu efnisatriði sýnir hvernig greiðsluáætlun leigu mun líta út fyrir annað tímabil.

Ekki er hægt að velja samsett tímabil sem er sjaldnar en greiðslutíðni leigusamningsins. Til dæmis er ekki hægt að nota ársfjórðungsleg samsett tímabil með mánaðarlegri greiðslu og ekki er hægt að nota árlegt samsett tímabil með hálfsárslegri greiðslu. Ef reynt er að velja samsett tímabil sem er sjaldnar en greiðslutíðni leigusamnings birtast villuboð.

> [!NOTE]
> Í öllum fjórum dæmum í þessu efnisatriði passar samsett tímabil við greiðslutíðnina.

## <a name="examples"></a>Dæmi

### <a name="setup-for-all-four-leases"></a>Uppsetning fyrir allar fjórar leigur

Eftirfarandi töflur sýna gildin sem eru stillt á flipunum **Almennt** og **Greiðsluáætlunarlínur** fyrir þá fjóra leigusamninga sem eru notaðir í þessum dæmum.

**Almennt**

| Svæði                      | Virði                        |
|----------------------------|------------------------------|
| Vextir á nýju lánsfé | **5%**                       |
| Tegund afborgunar               | **Venjulegar afborganir**         |
| Samsett tímabil       | Sjá einstök dæmi. |
| Greiðslutíðni          | **Mánaðarlega**                  |
| Upphafsdagsetning          | **1/1/2020**                 |

**Flipi greiðsluáætlunarlína**

| Svæði             | Virði                        |
|-------------------|------------------------------|
| Upphafsdagsetning        | **1/1/2020**                 |
| Tímabil           | **120**                      |
| Tímabil   | **Mánuðir**                   |
| Lokadagsetning          | **31/12/2029**               |
| Greiðslutíðni | Sjá einstök dæmi. |
| Upphæð greiðslu    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>Leigusamningur 1: Mánaðarlega samsett tímabil og mánaðarleg greiðslutíðni

Eftirfarandi tafla sýnir fyrstu 12 mánuði greiðsluáætlunarinnar. Athugið eftirfarandi upplýsingar:

- Gildið í dálknum „Tímabil“ eykst um 1 mánaðarlega, þar sem hver mánuður er nýtt samsett tímabil.
- Í formúlunni í dálknum „Núverandi gildi“ er genginu deilt með 12, þar sem það eru 12 samsett tímabil á hverju ári. Veldisvísirinn (þ.e. brjóstleturstalan) samsvarar gildinu í dálkinum „Tímabil“.

| Tímabil | Mánuður | Dagsetning       | Upphæð greiðslu | Núvirði                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 31/1/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>1</sup> = 49.792,53  |
| 2      | 2     | 29/2/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>2</sup> = 49.585,92  |
| 3      | 3     | 31/3/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>3</sup> = 49.380,17  |
| 4      | 4     | 30/4/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>4</sup> = 49.175,28  |
| 5      | 5     | 31/5/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>5</sup> = 48.971,23  |
| 6      | 6     | 30/6/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>6</sup> = 48.768,03  |
| 7      | 7     | 31/7/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>7</sup> = 48.565,67  |
| 8      | 8     | 31/8/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>8</sup> = 48.364,15  |
| 9      | 9     | 30/9/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>9</sup> = 48.163,47  |
| 10     | 10    | 31/10/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>10</sup> = 47.963,62 |
| 11     | 11    | 30/11/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>11</sup> = 47.764,61 |
| 12     | 12    | 31/12/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>12</sup> = 47.566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>Leigusamningur 2: Ársfjórðungslega samsett tímabil og ársfjórðungsleg greiðslutíðini

Eftirfarandi tafla sýnir fyrstu 12 mánuði greiðsluáætlunarinnar. Athugið eftirfarandi upplýsingar:

- Gildið í dálknum „Tímabil“ eykst um 1 á þriggja mánaða fresti (það er ársfjórðungslega), þar sem hver ársfjórðungur er nýtt samsett tímabil.
- Í formúlunni í dálknum „Núverandi gildi“ er genginu deilt með 4, þar sem það eru 4 samsett tímabil á hverju ári. Veldisvísirinn samsvarar gildinu í dálknum „Tímabil“.

| Tímabil | Mánuður | Dagsetning       | Upphæð greiðslu | Núvirði                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31/1/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 29/2/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 31/3/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 49.382,72 |
| 2      | 4     | 30/4/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 31/5/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 30/6/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 48.773,05 |
| 3      | 7     | 31/7/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 31/8/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 30/9/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 48.170,92 |
| 4      | 10    | 31/10/2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 30/11/2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 31/12/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 47.576,21 |

> [!NOTE]
> Ef afborgunargerðinni er breytt í **Framsettar afborganir** verður greiðslan í upphafi ársfjórðungsins í enda hans.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>Leigusamningur 3: Hálfsárs samsett tímabil og ársfjórðungsleg greiðslutíðni

Eftirfarandi tafla sýnir fyrstu 12 mánuði greiðsluáætlunarinnar. Athugið eftirfarandi upplýsingar:

- Gildið í dálknum „Tímabil“ eykst um 1 á sex mánaða fresti (það er á hálfs árs fresti), þar sem hvert hálft ár er nýtt samsett tímabil.
- Í formúlunni í dálknum „Núverandi gildi“ er genginu deilt með 2, þar sem það eru 2 samsett tímabil á hverju ári. Veldisvísirinn samsvarar gildinu í dálknum „Tímabil“.

| Tímabil | Mánuður | Dagsetning       | Upphæð greiðslu | Núvirði                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31/1/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 29/2/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 31/3/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 30/4/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 31/5/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 30/6/2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 48.780,49 |
| 2      | 7     | 31/7/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 31/8/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 30/9/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 31/10/2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 30/11/2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 31/12/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 47.590,72 |

> [!NOTE]
> Ef afborgunargerðinni er breytt í **Framsettar afborganir** verður greiðslan í janúar og júlí í stað júní og desember.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>Leiga 4: Árlegt samsett tímabil og árleg greiðslutíðni

Eftirfarandi tafla sýnir fyrstu 12 mánuði greiðsluáætlunarinnar. Athugið eftirfarandi upplýsingar:

- Gildið í dálknum „Tímabil“ eykst um 1 á tólf mánaða fresti (það er á árs fresti), þar sem hvert ár er nýtt samsett tímabil.
- Í formúlunni í dálknum „Núverandi gildi“ er genginu deilt með 1, þar sem það er 1 samsett tímabil á hverju ári. Veldisvísirinn samsvarar gildinu í dálknum „Tímabil“.

| Tímabil | Mánuður | Dagsetning       | Upphæð greiðslu | Núvirði                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31/1/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 29/2/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 31/3/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 30/4/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 31/5/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 30/6/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 31/7/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 31/8/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 30/9/2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 31/10/2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 30/11/2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 31/12/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 47.619,05 |

> [!NOTE]
> Ef afborgunargerðinni er breytt í **Framsettar afborganir** verður greiðslan í janúar í stað desember.

---
title: Dæmi og rök fyrir birgðavirðisskýrslu
description: Þetta efnisatriði gefur nokkur dæmi um niðurstöður sem eru settar fram á hverri gerð birgðavirðisskýrslu. Birgðavirðisskýrslur veita upplýsingar um efnislegt og fjárhagslegt magn og fjárhæðir birgða þinna.
author: banluo-ms
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: banluo
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4ad85058c8743895185d3da2e8975711f1e3bc2c
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798406"
---
# <a name="inventory-value-report-examples-and-logic"></a>Dæmi og rök fyrir birgðavirðisskýrslu

[!include [banner](../includes/banner.md)]

Birgðavirðisskýrslur veita upplýsingar um efnislegt og fjárhagslegt magn og fjárhæðir birgða þinna. Þetta efnisatriði gefur nokkur dæmi um niðurstöður sem eru settar fram á hverri gerð birgðavirðisskýrslu.

Fyrir frekari upplýsingar um hvernig á að búa til og nota hverja gerð birgðavirðisskýrslu, sjá [Birgðavirðisskýrslur](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Sýnidæmi sem er notað í þessum dæmum

Dæmin í þessu efnisatriði byggja á dæmi um birgðafærslugögnin sem lýst er í þessum hluta.

### <a name="storage-dimension-setup"></a>Uppsetning geymsluvíddar

Dæmi kerfisins inniheldur eftirfarandi uppsetningu geymsluvídda.

| Nafn | Í gangi | Efnislegar birgðir | Fjárhagslegar birgðir |
|---|---|---|---|
| Svæði | Já | Já | Já |
| Vöruhús | Já | Já | Ekkert |

### <a name="inventory-model"></a>Birgðalíkan

Fyrir dæmikerfið er birgðalíkanið fyrir útgefnar vörur *FIFO*, og **Kostnaðarverð** reiturinn fyrir birgðalíkanið er stilltur á *Taktu með líkamlegt gildi*.

### <a name="inventory-transactions"></a>Birgðafærslur

Dæmikerfið inniheldur eftirfarandi birgðafærslur fyrir losaða vöru sem hefur vörunúmerið *B0001*.

| Tilvísun | Vefsvæði | Vöruhús | Innhreyfing | Gefa út | Efnisleg dagsetning | Fjárhagsdagsetning | Magn | Kostnaðarupphæð | Efnisleg kostnaðarupphæð |
|---|---|---|---|---|---|---|---|---|---|
| Innkaupapöntun | 1 | 11 | Innkeypt | | 15. mars | 15. mars | 10 | 1.000 | 1.000 |
| Innkaupapöntun | 2 | 21 | Innkeypt | | 15. mars | 15. mars | 10 | 2,000 | 2,000 |
| Innkaupapöntun | 1 | 11 | Móttekið | | 15. apríl | | 5 | | 375 |
| Flutningspöntun | 1 | 11 | | Selt | 2. maí | 2. maí | -5 | -458,33 | -458,33 |
| Flutningspöntun | 1 | 12 | Innkeypt | | 2. maí | 2. maí | 5 | 458.33 | 458.33 |
| Sölupöntun | 1 | 12 | | Selt | 3. maí | 3. maí | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Uppsetning birgðavirðisskýrslu

Dæmikerfið inniheldur uppsetningu birgðagildisskýrslu sem hefur eftirfarandi stillingar:

- **Svið:** *Birtingardagur*
- **Birgðir:** *Já*
- **Reiknaðu meðaleiningakostnað:** *Já*
- **Heildarmagn og verðmæti:** *Já*
- **Síða, skoða:** *Valið*
- **Auðkenni auðlindar, skoða:** *Já*
- **Stig:** *Samtals*

## <a name="inventory-value-report-example-1"></a>Dæmi um birgðavirðisskýrslu 1

Eftirfarandi tafla og myndir sýna niðurstöðurnar þegar þú notar sýnishornsgögn og skýrslustillingar sem lýst er fyrr í þessu efnisatriði.

| Gerð forða | Tilföng | Vefsvæði | Tilvísun | Birgðir: Fjárhagslegt magn | Birgðir: Fjárhagsleg upphæð | Birgðir: Bókað efnislegt magn | Birgðir: Bókuð efnisleg upphæð | Birgðir: Magn | Birgðir: Upphæð | Meðalverð á einingu |
|---|---|---|---|---|---|---|---|---|---|---|
| Efni | B0001 | 1 | Lokastaða | 9.00 | 908.33 | 5.00 | 375.00 | 14.00 | 1,283.33 | 91.67 |
| Efni | B0001 | 2 | Lokastaða | 10,00 | 2,000.00 | 0,00 | 0,00 | 10,00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Staðlað birgðavirðisskýrsla til dæmis 1

Eftirfarandi mynd sýnir staðalinn **Birgðaverðmæti** skýrslu til dæmis 1. (Veldu myndina til að opna stærri útgáfu.)

[![Birgðavirðisskýrsla til dæmis 1.](media/inventory-value-report-ex1-small.png "Birgðavirðisskýrsla til dæmis 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Birgðavirðisskýrsla geymsluskýrsla til dæmis 1

Eftirfarandi mynd sýnir **Geymsla birgðavirðisskýrslu** skýrslu til dæmis 1. (Veldu myndina til að opna stærri útgáfu.)

[![Birgðavirðisskýrsla geymsluskýrsla til dæmis 1.](media/inventory-value-report-storage-ex1-small.png "Birgðavirðisskýrsla geymsluskýrsla til dæmis 1")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Dæmi um birgðavirðisskýrslu 2

Eftirfarandi tafla og myndir sýna niðurstöðurnar þegar þú notar sýnishornsgögnin sem lýst er fyrr í þessu efni, en þú breytir gildi **Stig** sviði til *Viðskipti* í skýrslustillingunni og þú stillir **Frá dags** sviði til *15. mars* þegar þú keyrir skýrsluna.

| Gerð forða | Tilföng | Vefsvæði | Dagsetning | Númer | Tilvísun | Birgðir: Fjárhagslegt magn | Birgðir: Fjárhagsleg upphæð | Birgðir: Bókað efnislegt magn | Birgðir: Bókuð efnisleg upphæð | Birgðir: Magn | Birgðir: Upphæð |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Efni | B0001 | 1 | 15.3.2021 | 00000126 | Innkaupapöntun | 0,00 | 0,00 | 10,00 | 1,000.00 | **10.00** | **1,000.00** |
| Efni | B0001 | 1 | 15.3.2021 | 00000126 | Innkaupapöntun | 10,00 | 1,000.00 | -10,00 | -1.000,00 | **0.00** | **0.00** |
| Efni | B0001 | 1 | 15.4.2021 | 00000128 | Innkaupapöntun | 0,00 | 0,00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Efni | B0001 | 1 | 2.5.2021 | 000003 | Flutningspöntunarsending | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |
| Efni | B0001 | 1 | 2.5.2021 | 000003 | Móttaka flutningspöntunar | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Efni | B0001 | 1 | 3/5/2021 | 000835 | Sölupöntun | 0,00 | 0,00 | 1.00 | -91,67 | **-1.00** | **-91.67** |
| Efni | B0001 | 1 | 3/5/2021 | 000835 | Sölupöntun | 1.00 | -91,67 | 1.00 | 91.67 | **0.00** | **0.00** |
| Efni | B0001 | 2 | 15.3.2021 | 00000127 | Innkaupapöntun | 0,00 | 0,00 | 10,00 | 2,000.00 | **10.00** | **2,000.00** |
| Efni | B0001 | 2 | 15.3.2021 | 00000127 | Innkaupapöntun | 10,00 | 2,000.00 | -10,00 | -2.000,00 | **0.00** | **0.00** |
| Efni | B0001 | 2 | 2.5.2021 | 000003 | Flutningspöntunarsending | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Efni | B0001 | 2 | 2.5.2021 | 000003 | Móttaka flutningspöntunar | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Staðlað birgðavirðisskýrsla til dæmis 2

Eftirfarandi mynd sýnir staðalinn **Birgðaverðmæti** skýrslu til dæmis 2. (Veldu myndina til að opna stærri útgáfu.)

[![Birgðavirðisskýrsla til dæmis 2.](media/inventory-value-report-ex2-small.png "Birgðavirðisskýrsla til dæmis 2")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Birgðavirðisskýrsla geymsluskýrsla til dæmis 2

Eftirfarandi mynd sýnir **Geymsla birgðavirðisskýrslu** skýrslu til dæmis 2. (Veldu myndina til að opna stærri útgáfu.)

[![Birgðavirðisskýrsla geymsluskýrsla til dæmis 2.](media/inventory-value-report-storage-ex2-small.png "Birgðavirðisskýrsla geymsluskýrsla til dæmis 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Dæmi um birgðavirðisskýrslu 3

Við mælum með að þú keyrir birgðavirðisskýrslur eftir endurútreikning eða birgðalokun, svo að þú hafir færslur og upphæðir sem endurútreikningurinn eða birgðalokunin hefur áhrif á.

Eftirfarandi undirkaflar sýna birgðavirðisskýrslur sem eru búnar til eftir að þú lokar birgðum til 30. maí.

### <a name="example-3-when-the-totals-level-is-used"></a>Dæmi 3 þegar heildarstigið er notað

Eftirfarandi tafla sýnir niðurstöðurnar þegar þú notar sýnishornsgögn og skýrslustillingar sem lýst er fyrr í þessu efnisatriði. (Í þeirri skýrslustillingu er **Stig** reiturinn er stilltur á *Samtals* .)

| Gerð forða | Tilföng | Vefsvæði | Tilvísun | Birgðir: Fjárhagslegt magn | Birgðir: Fjárhagsleg upphæð | Birgðir: Bókað efnislegt magn | Birgðir: Bókuð efnisleg upphæð | Birgðir: Magn | Birgðir: Upphæð | Meðalverð á einingu |
|---|---|---|---|---|---|---|---|---|---|---|
| Efni | B0001 | 1 | Lokastaða | 9.00 | 900.00 | 5.00 | 375.00 | 14.00 | 1,275.00 | 91.07 |
| Efni | B0001 | 2 | Lokastaða | 10,00 | 2,000.00 | 0,00 | 0,00 | 10,00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Dæmi 3 þegar Færslustigið er notað

Eftirfarandi tafla sýnir niðurstöðurnar þegar þú notar sýnishornsgögnin sem lýst er fyrr í þessu efni, en þú breytir gildi **Stig** sviði til *Viðskipti* í skýrslustillingunni.

| Gerð forða | Tilföng | Vefsvæði | Dagsetning | Númer | Tilvísun | Birgðir: Fjárhagslegt magn | Birgðir: Fjárhagsleg upphæð | Birgðir: Bókað efnislegt magn | Birgðir: Bókuð efnisleg upphæð | Birgðir: Magn | Birgðir: Upphæð |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Efni | B0001 | 1 | 15.3.2021 | 00000126 | Innkaupapöntun | 0,00 | 0,00 | 10,00 | 1,000.00 | 10,00 | 1,000.00 |
| Efni | B0001 | 1 | 15.3.2021 | 00000126 | Innkaupapöntun | 10,00 | 1,000.00 | -10,00 | -1.000,00 | 0,00 | 0,00 |
| Efni | B0001 | 1 | 15.4.2021 | 00000128 | Innkaupapöntun | 0,00 | 0,00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Efni | B0001 | 1 | 2.5.2021 | 000003 | Flutningspöntunarsending | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Efni | B0001 | 1 | 2.5.2021 | 000003 | Móttaka flutningspöntunar | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Efni | B0001 | 1 | 3/5/2021 | 000835 | Sölupöntun | 0,00 | 0,00 | 1.00 | -91,67 | 1.00 | -91,67 |
| Efni | B0001 | 1 | 3/5/2021 | 000835 | Sölupöntun | 1.00 | -91,67 | 1.00 | 91.67 | 0,00 | 0,00 |
| Efni | B0001 | 1 | 31.5.2021 | 000835 | Sölupöntun | 0,00 | -8.33 | 0,00 | 0,00 | 0,00 | -8.33 |
| Efni | B0001 | 1 | 31.5.2021 | 000003 | Flutningspöntunarsending | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
| Efni | B0001 | 1 | 31.5.2021 | 000003 | Móttaka flutningspöntunar | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Efni | B0001 | 2 | 15.3.2021 | 00000127 | Innkaupapöntun | 0,00 | 0,00 | 10,00 | 2,000.00 | 10,00 | 2,000.00 |
| Efni | B0001 | 2 | 15.3.2021 | 00000127 | Innkaupapöntun | 10,00 | 2,000.00 | -10,00 | -2.000,00 | 0,00 | 0,00 |
| Efni | B0001 | 2 | 2.5.2021 | 000003 | Flutningspöntunarsending | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Efni | B0001 | 2 | 2.5.2021 | 000003 | Móttaka flutningspöntunar | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Efni | B0001 | 2 | 31.5.2021 | 000003 | Flutningspöntunarsending | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Efni | B0001 | 2 | 31.5.2021 | 000003 | Móttaka flutningspöntunar | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
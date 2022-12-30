---
title: Dæmi og rök fyrir birgðavirðisskýrslu
description: Í þessari grein eru nokkur dæmi um niðurstöður sem koma fram á hvers kyns birgðavirðisskýrslu. Birgðavirðisskýrslur gefa upplýsingar um efnislegar birgðir, fjárhagslegt magn og upphæðir.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e6c6387be5204fde6ebc7a4983567801900974af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877654"
---
# <a name="inventory-value-report-examples-and-logic"></a>Dæmi og rök fyrir birgðavirðisskýrslu

[!include [banner](../includes/banner.md)]

Birgðavirðisskýrslur gefa upplýsingar um efnislegar birgðir, fjárhagslegt magn og upphæðir. Í þessari grein eru nokkur dæmi um niðurstöður sem koma fram á hvers kyns birgðavirðisskýrslu.

Frekari upplýsingar um hvernig eigi að mynda og nota hvers kyns birgðavirðisskýrslur eru í [Birgðavirðisskýrslur](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Sýnidæmi sem er notað í þessum dæmum

Dæmin í þessari grein byggja á dæmi um birgðafærslugögnin sem lýst er í þessum hluta.

### <a name="storage-dimension-setup"></a>Uppsetning geymsluvíddar

Dæmi kerfisins inniheldur eftirfarandi uppsetningu geymsluvídda.

| Nafn | Í gangi | Efnislegar birgðir | Fjárhagslegar birgðir |
|---|---|---|---|
| Svæði | Já | Já | Já |
| Vöruhús | Já | Já | Nei |

### <a name="inventory-model"></a>Birgðalíkan

Fyrir dæmi kerfisins er birgðalíkan útgefinna afurða *FIFO* og stillingin **Kostnaðarverð** reiturinn fyrir birgðalíkanið er stilltur á *Taka efnislegt virði með*.

### <a name="inventory-transactions"></a>Birgðafærslur

Dæmi kerfisins inniheldur eftirfarandi birgðafærslur fyrir útgefna afurð sem er með vörunúmerið *B0001*.

| Tilvísun | Svæði | Vöruhús | Innhreyfing | Gefa út | Efnisleg dagsetning | Fjárhagsdagsetning | Magn | Kostnaðarupphæð | Efnisleg kostnaðarupphæð |
|---|---|---|---|---|---|---|---|---|---|
| Innkaupapöntun | 1 | 11 | Innkeypt | | 15. mars | 15. mars | 10 | 1.000 | 1.000 |
| Innkaupapöntun | 2 | 21 | Innkeypt | | 15. mars | 15. mars | 10 | 2,000 | 2,000 |
| Innkaupapöntun | 1 | 11 | Móttekið | | 15. apríl | | 5 | | 375 |
| Flutningspöntun | 1 | 11 | | Selt | 2. maí | 2. maí | -5 | -458,33 | -458,33 |
| Flutningspöntun | 1 | 12 | Innkeypt | | 2. maí | 2. maí | 5 | 458.33 | 458.33 |
| Sölupöntun | 1 | 12 | | Selt | 3. maí | 3. maí | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Skilgreining birgðavirðisskýrslu

Dæmakerfið inniheldur er stillingar fyrir birgðavirðisskýrslu með eftirfarandi stillingum:

- **Afmörkun:**  *Birtingardagsetning*
- **Birgðir:** *Já*
- **Reikna meðalkostnað einingar:** *J‘a*
- **Heildarmagn og gildi:** *Já*
- **Vefsvæði, Skoða:** *Valið*
- **Kenni tilfangs, skoða:** *Já*
- **Stig:** *alls*

## <a name="inventory-value-report-example-1"></a>Birgðavirðisskýrsla dæmi 1

Eftirfarandi tafla og myndir sýna niðurstöðurnar þegar þú notar sýnishorn og skýrslugerð sem lýst er fyrr í þessari grein.

| Gerð tilfanga | Tilföng | Svæði | Tilvísun | Birgðir: Fjárhagslegt magn | Birgðir: Fjárhagsleg upphæð | Birgðir: Bókað efnislegt magn | Birgðir: Bókuð efnisleg upphæð | Birgðir: Magn | Birgðir: Upphæð | Meðalverð á einingu |
|---|---|---|---|---|---|---|---|---|---|---|
| Efni | B0001 | 1 | Lokastaða | 9.00 | 908,33 | 5.00 | 375,00 | 14.00 | 1,283.33 | 91.67 |
| Efni | B0001 | 2 | Lokastaða | 10,00 | 2,000.00 | 0,00 | 0,00 | 10,00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Stöðluð birgðavirðisskýrsla til dæmis 1

Eftirfarandi mynd sýnir staðlaða **Birgðavirðisskýrslu** fyrir dæmi 1. (Veldu myndina til að opna stærri útgáfu.)

[![Skýrsla um birgðavirði til dæmis 1.](media/inventory-value-report-ex1-small.png "Skýrsla um birgðavirði, til dæmis 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Geymsluskýrsla birgðavirðisskýrslu fyrir dæmi 1.

Eftirfarandi mynd sýnir skýrsluna **Geymsla birgðavirðisskýrslu** fyrir dæmi 1. (Veldu myndina til að opna stærri útgáfu.)

[![Geymsluskýrsla birgðavirðisskýrslu fyrir dæmi 1.](media/inventory-value-report-storage-ex1-small.png "Geymsluskýrsla birgðavirðisskýrslu fyrir dæmi 1.")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Birgðavirðisskýrsla dæmi 2

Eftirfarandi tafla og myndir sýna niðurstöðurnar þegar þú notar sýnigögnin sem lýst er fyrr í þessari grein, en þú breytir gildinu á reitnum **Stig** í *Færslur* í skýrsluskilgreiningunni og þú stillir reitinn **Frá dagsetning** á *15. mars* þegar skýrslan er keyrð.

| Gerð tilfanga | Tilföng | Svæði | Dagsetning | Númer | Tilvísun | Birgðir: Fjárhagslegt magn | Birgðir: Fjárhagsleg upphæð | Birgðir: Bókað efnislegt magn | Birgðir: Bókuð efnisleg upphæð | Birgðir: Magn | Birgðir: Upphæð |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Efni | B0001 | 1 | 15/3/2021 | 00000126 | Innkaupapöntun | 0,00 | 0,00 | 10,00 | 1,000.00 | **10.00** | **1,000.00** |
| Efni | B0001 | 1 | 15/3/2021 | 00000126 | Innkaupapöntun | 10,00 | 1,000.00 | -10,00 | -1.000,00 | **0.00** | **0.00** |
| Efni | B0001 | 1 | 15/4/2021 | 00000128 | Innkaupapöntun | 0,00 | 0,00 | 5.00 | 375,00 | **5.00** | **375.00** |
| Efni | B0001 | 1 | 2/5/2021 | 000003 | Flutningspöntunarsending | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |
| Efni | B0001 | 1 | 2/5/2021 | 000003 | Móttaka flutningspöntunar | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Efni | B0001 | 1 | 3/5/2021 | 000835 | Sölupöntun | 0,00 | 0,00 | 1.00 | -91,67 | **-1.00** | **-91.67** |
| Efni | B0001 | 1 | 3/5/2021 | 000835 | Sölupöntun | 1.00 | -91,67 | 1.00 | 91.67 | **0.00** | **0.00** |
| Efni | B0001 | 2 | 15/3/2021 | 00000127 | Innkaupapöntun | 0,00 | 0,00 | 10,00 | 2,000.00 | **10.00** | **2,000.00** |
| Efni | B0001 | 2 | 15/3/2021 | 00000127 | Innkaupapöntun | 10,00 | 2,000.00 | -10,00 | -2.000,00 | **0.00** | **0.00** |
| Efni | B0001 | 2 | 2/5/2021 | 000003 | Flutningspöntunarsending | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Efni | B0001 | 2 | 2/5/2021 | 000003 | Móttaka flutningspöntunar | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Stöðluð birgðavirðisskýrsla til dæmis 2

Eftirfarandi mynd sýnir **Birgðavirðisskýrsluna** fyrir dæmi 2. (Veldu myndina til að opna stærri útgáfu.)

[![Skýrsla um birgðavirði til dæmis 2.](media/inventory-value-report-ex2-small.png "Skýrsla um birgðavirði, til dæmis 2")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Geymsluskýrsla birgðavirðisskýrslu fyrir dæmi 2.

Eftirfarandi dæmi sýnir skýrsluna **Geymsla birgðavirðisskýrslu** fyrir dæmi 2. (Veldu myndina til að opna stærri útgáfu.)

[![Geymsluskýrsla birgðavirðisskýrslu fyrir dæmi 2.](media/inventory-value-report-storage-ex2-small.png "Geymsluskýrsla birgðavirðisskýrslu fyrir dæmi 2.")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Birgðavirðisskýrsla dæmi 3

Mælt er með að keyra birgðavirðisskýrslur eftir endurútreikning eða birgðalokun svo þú sért með færslur og upphæðir sem endurútreikningur eða birgðalokun hefur áhrif á.

Eftirfarandi undirkaflar sýna skýrslur um birgðavirði sem verða til eftir að þú lokar birgðum til 30. maí.

### <a name="example-3-when-the-totals-level-is-used"></a>Dæmi 3 þegar samtölustigið er notað

Eftirfarandi tafla sýna niðurstöðurnar þegar þú notar sýnishorn og skýrslugerð sem lýst er fyrr í þessari grein. (Í þeirri skýrslu er svæðið **Stig** stillt á *Samtala*.)

| Gerð tilfanga | Tilföng | Svæði | Tilvísun | Birgðir: Fjárhagslegt magn | Birgðir: Fjárhagsleg upphæð | Birgðir: Bókað efnislegt magn | Birgðir: Bókuð efnisleg upphæð | Birgðir: Magn | Birgðir: Upphæð | Meðalverð á einingu |
|---|---|---|---|---|---|---|---|---|---|---|
| Efni | B0001 | 1 | Lokastaða | 9.00 | 900,00 | 5.00 | 375,00 | 14.00 | 1,275.00 | 91.07 |
| Efni | B0001 | 2 | Lokastaða | 10,00 | 2,000.00 | 0,00 | 0,00 | 10,00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Dæmi 3 þegar færslustigið er notað

Eftirfarandi tafla sýna niðurstöðurnar þegar þú notar sýnigögnin sem lýst er fyrr í þessari grein, en þú breytir gildinu á reitnum **Stig** í *Færslur* í skýrsluskilgreiningunni.

| Gerð tilfanga | Tilföng | Svæði | Dagsetning | Númer | Tilvísun | Birgðir: Fjárhagslegt magn | Birgðir: Fjárhagsleg upphæð | Birgðir: Bókað efnislegt magn | Birgðir: Bókuð efnisleg upphæð | Birgðir: Magn | Birgðir: Upphæð |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Efni | B0001 | 1 | 15/3/2021 | 00000126 | Innkaupapöntun | 0,00 | 0,00 | 10,00 | 1,000.00 | 10,00 | 1,000.00 |
| Efni | B0001 | 1 | 15/3/2021 | 00000126 | Innkaupapöntun | 10,00 | 1,000.00 | -10,00 | -1.000,00 | 0,00 | 0,00 |
| Efni | B0001 | 1 | 15/4/2021 | 00000128 | Innkaupapöntun | 0,00 | 0,00 | 5.00 | 375,00 | 5.00 | 375,00 |
| Efni | B0001 | 1 | 2/5/2021 | 000003 | Flutningspöntunarsending | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Efni | B0001 | 1 | 2/5/2021 | 000003 | Móttaka flutningspöntunar | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Efni | B0001 | 1 | 3/5/2021 | 000835 | Sölupöntun | 0,00 | 0,00 | 1.00 | -91,67 | 1.00 | -91,67 |
| Efni | B0001 | 1 | 3/5/2021 | 000835 | Sölupöntun | 1.00 | -91,67 | 1.00 | 91.67 | 0,00 | 0,00 |
| Efni | B0001 | 1 | 31/5/2021 | 000835 | Sölupöntun | 0,00 | -8,33 | 0,00 | 0,00 | 0,00 | -8,33 |
| Efni | B0001 | 1 | 31/5/2021 | 000003 | Flutningspöntunarsending | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
| Efni | B0001 | 1 | 31/5/2021 | 000003 | Móttaka flutningspöntunar | 0,00 | 41,67 | 0,00 | 0,00 | 0,00 | 41,67 |
| Efni | B0001 | 2 | 15/3/2021 | 00000127 | Innkaupapöntun | 0,00 | 0,00 | 10,00 | 2,000.00 | 10,00 | 2,000.00 |
| Efni | B0001 | 2 | 15/3/2021 | 00000127 | Innkaupapöntun | 10,00 | 2,000.00 | -10,00 | -2.000,00 | 0,00 | 0,00 |
| Efni | B0001 | 2 | 2/5/2021 | 000003 | Flutningspöntunarsending | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Efni | B0001 | 2 | 2/5/2021 | 000003 | Móttaka flutningspöntunar | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Efni | B0001 | 2 | 31/5/2021 | 000003 | Flutningspöntunarsending | 0,00 | 41,67 | 0,00 | 0,00 | 0,00 | 41,67 |
| Efni | B0001 | 2 | 31/5/2021 | 000003 | Móttaka flutningspöntunar | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |

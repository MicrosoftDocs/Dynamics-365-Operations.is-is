---
title: Dæmi og rök fyrir aldursgreiningarskýrslu birgða
description: Í þessu efnisatriði er að finna dæmi sem sýna hvernig á að túlka niðurstöður aldursgreiningarskýrslu.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6e708e4dc818f20fc8d835053da75c2fe9c98f6
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759545"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Dæmi og rök fyrir aldursgreiningarskýrslu birgða

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna dæmi sem sýna hvernig á að túlka niðurstöður skýrslu **Aldursgreiningar**. Þessi skýrsla flokkar lagerbirgðir og birgðavirði fyrir valda vöru eða vöruflokk í nokkra tímaramma. Í þessu efnisatriði eru einnig innri rök skýrslunnar sýnd.

Dæmin í þessu efnisatriði sýna niðurstöður sem eru birtar í staðlaðri skýrslu **Aldursgreiningarskýrslu**. Við mælum hinsvegar almennt með því að notuð sé útgáfan [Skýrsla um aldursgreiningu birgða](inventory-aging-report-storage.md) fyrir þessa skýrslu, sérstaklega þegar þarf að vinna úr mörgum vörum og vöruhúsum. Skýrsla um aldursgreiningu birgða vistar hverja skýrslu sem búin er til, sýnir niðurstöðurnar sem gagnvirka síðu og graf, og gerir kleift að flytja út allar vistaðar skýrslur.

## <a name="sample-data-that-is-used-in-these-examples"></a>Sýnidæmi sem er notað í þessum dæmum

Dæmin í þessu efnisatriði byggja á dæmi um birgðafærslugögnin sem lýst er í þessum hluta.

### <a name="storage-dimension-setup"></a>Uppsetning geymsluvíddar

Dæmi kerfisins inniheldur eftirfarandi uppsetningu geymsluvídda.

| Nafn      | Í gangi | Efnislegar birgðir | Fjárhagslegar birgðir |
|-----------|--------|--------------------|---------------------|
| Svæði      | Já    | Já                | Já                 |
| Vöruhús | Já    | Já                | Ekkert                  |

### <a name="inventory-model"></a>Birgðalíkan

Fyrir dæmi kerfisins er birgðalíkan útgefinna afurða *FIFO* og stillingin **Kostnaðarverð** fyrir birgðalíkanið er *Taka efnislegt virði með*.

### <a name="inventory-transactions"></a>Birgðafærslur

Dæmi kerfisins inniheldur eftirfarandi birgðafærslur fyrir útgefna afurð sem er með vörunúmerið *1000*.

| Tilvísun      | Svæði | Vöruhús | Innhreyfing   | Úthreyfing | Efnisleg dagsetning | Fjárhagsdagsetning | Magn | Kostnaðarupphæð | Efnisleg kostnaðarupphæð |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Innkaupapöntun | 1    | 11        | Innkeypt |       | 15. mars      | 15. mars       | 10       | 1.000       | 1.000                |
| Innkaupapöntun | 2    | 21        | Innkeypt |       | 15. mars      | 15. mars       | 10       | 2,000       | 2,000                |
| Innkaupapöntun | 1    | 11        | Móttekið  |       | 15. apríl      |                | 5        |             | 375                  |
| Flutningspöntun | 1    | 11        |           | Selt  | 2. maí         | 2. maí          | -5       | -458,33     | -458,33              |
| Flutningspöntun | 1    | 12        | Innkeypt |       | 2. maí         | 2. maí          | 5        | 458.33      | 458.33               |
| Sölupöntun    | 1    | 12        |           | Selt  | 3. maí         | 3. maí          | -1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Hvernig magn og upphæðir í hverjum tímaramma er reiknað

Með því að nota sýnigögnin sem lýst er í fyrri hlutunum er hægt að keyra skýrsluna **Aldursgreining** sem er með eftirfarandi stillingum:

- **Frá og með dagsetningunni:** *9. maí 2020*
- **Svæði:** *Yfirlit*
- **Vöruhús:** *Nei*
- **Vörunúmer:** *Samtala*
- **Aldursgreiningartímabil:** Stillið þennan reit til að búa til mánaðarramma.

Í þessu tilfelli mun innihald skýrslunnar sem búin er til líkjast eftirfarandi dæmi.

<table>
<thead>
<tr>
    <th rowspan="2">Vörunúmer</th>
    <th rowspan="2">Svæði</th>
    <th rowspan="2">Lagerbirgðir</th>
    <th rowspan="2">Virði á lager</th>
    <th rowspan="2">Magn birgðavirðis</th>
    <th rowspan="2">Birgðavirði</th>
    <th rowspan="2">Meðaleiningarkostnaður</th>
    <th colspan="2">8.5.2020–1.5.2020</th>
    <th colspan="2">30.4.2020–1.4.2020</th>
    <th colspan="2">31.3.2020–1.3.2020</th>
</tr>
<tr>
    <th>P1:Magn</th>
    <th>P1:Upphæð</th>
    <th>P2:Magn</th>
    <th>P2:Upphæð</th>
    <th>P3:Magn</th>
    <th>P3:Upphæð</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 samtals</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

Athugið eftirfarandi upplýsingar í þessari sýniskýrslu:

- Gildin **Magn birgðavirðis**, **Birgðavirði** og **Meðalkostnaður einingar** sem sýnd eru í skýrslunni eru gildi fyrir fjárhagsbirgðavíddina (**Svæði**, í þessu tilfelli).

    Til dæmis, fyrir svæði 1, sýnir skýrslan eftirfarandi upplýsingar:

    - Gildið **Magn birgðavirðis** er *14* (= 10 + 5 – 5 + 5 – 1).
    - Gildið **Birgðavirði** er *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).
    - Gildið **Meðalkostnaður einingar** er *91,67*.
    - Gildið **Virði á lager** og gildið **Upphæð** í hverjum tímaramma eru reiknuð með því að nota gildið **Meðalkostnaður einingar**.

- Skýrslan ákvarðar magn á lager fyrir hvern tímaramma með því að draga saman heildarmagn móttekið af birgðum fyrir hvern tímaramma. Hún notar fyrst inn, fyrst út (FIFO) regluna til að draga frá heildarmagn losunar, óháð birgðalíkaninu sem varan notar.

Ef sama skýrslan er keyrð aftur, en í þetta skipti eru báðir reitirnir **Svæði** og **Vöruhús** eru stilltir á *Skoða*, mun nýja skýrslan líkjast eftirfarandi dæmi.

<table>
<thead>
<tr>
    <th rowspan="2">Vörunúmer</th>
    <th rowspan="2">Svæði</th>
    <th rowspan="2">Vöruhús</th>
    <th rowspan="2">Lagerbirgðir</th>
    <th rowspan="2">Virði á lager</th>
    <th rowspan="2">Magn birgðavirðis</th>
    <th rowspan="2">Birgðavirði</th>
    <th rowspan="2">Meðaleiningarkostnaður</th>
    <th colspan="2">8.5.2020–1.5.2020</th>
    <th colspan="2">30.4.2020–1.4.2020</th>
    <th colspan="2">31.3.2020–1.3.2020</th>
</tr>
<tr>
    <th>P1:Magn</th>
    <th>P1:Upphæð</th>
    <th>P2:Magn</th>
    <th>P2:Upphæð</th>
    <th>P3:Magn</th>
    <th>P3:Upphæð</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 samtals</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Í þetta skipti er svæði 1 skipt niður í tvær raðir, ein fyrir vöruhús 11 og ein fyrir vöruhús 12. Hinsvegar eru gildin **Magn birgðavirðis**, **Birgðavirði** og **Meðalkostnaður einingar** enn þau sömu vegna þess að **Vöruhús** er ekki fjárhagsbirgðavídd.

Takið auk þess eftir því að dreift magn á svæði 1 er annað. Í fyrstu skýrslunni sem var keyrð hunsaði kerfið millifærslupöntunina sem átti sér stað á sama svæðinu og dró frá magn sölureikningsins frá tímarammanum **31.3.2020 - 1.3.2020** á svæði 1. Í nýju skýrslunni dregur kerfið hins vegar frá magn sölureikningsins frá tímarammanum **8.5.2020 - 1.5.2020** í vöruhúsi 12.

## <a name="effects-of-inventory-closing"></a>Áhrif birgðalokunar

Ef keyrð er birgðalokun fyrir maí og fyrri skýrslan síðan keyrð aftur, en reiturinn **Frá og með dagsetningunni** er stilltur á *31. maí 2020* koma eftirfarandi niðurstöður í ljós:

- Gildin **Birgðavirði** og **Meðalkostnaður einingar** eru uppfærð.
- Gildið **Virði á lager** og gildið **Upphæð** í hverjum tímaramma eru uppfærð í samræmi.

Nýja skýrslan mun líkjast eftirfarandi dæmi.

<table>
<thead>
<tr>
    <th rowspan="2">Vörunúmer</th>
    <th rowspan="2">Svæði</th>
    <th rowspan="2">Vöruhús</th>
    <th rowspan="2">Lagerbirgðir</th>
    <th rowspan="2">Virði á lager</th>
    <th rowspan="2">Magn birgðavirðis</th>
    <th rowspan="2">Birgðavirði</th>
    <th rowspan="2">Meðaleiningarkostnaður</th>
    <th colspan="2">31.5.2020–1.5.2020</th>
    <th colspan="2">30.4.2020–1.4.2020</th>
    <th colspan="2">31.3.2020–1.3.2020</th>
</tr>
<tr>
    <th>P1:Magn</th>
    <th>P1:Upphæð</th>
    <th>P2:Magn</th>
    <th>P2:Upphæð</th>
    <th>P3:Magn</th>
    <th>P3:Upphæð</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0,00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 samtals</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>

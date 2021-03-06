---
title: Endurmat á gjaldmiðli í samstæðufyrirtæki
description: Þetta efnisatriði lýsir því hvernig á að endurmeta gjaldmiðil í samstæðufyrirtæki.
author: roschlom
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c901d5ccd8c8b2146daa49752b7d8b70bbfca722
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818417"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Endurmat á gjaldmiðli í samstæðufyrirtæki

[!include [banner](../includes/banner.md)]

Þegar gögn frá einum bókhaldsgjaldmiðill til annars eru sameinuð, verður samt að keyra gjaldmiðilsendurmatið ef breyting á gjaldmiðla verður , þannig að lykilsstöður þínar séu rétt endurmetnar. Þegar gögnum eru sameinuð í upphafi, nota á **umreikningur Gjaldmiðils** flipa til að velja fyrstu gengi fyrir þýðingu á meðan á sameiningarferlinu stendur. Eftir að nýtt gengi er fært inn (til dæmis í næsta mánuð), verður að endurmeta stöðu lykils. Óinnleystur hagnaður eða tap er síðan uppfærð til samræmis, byggt á nýju gengi og dagsetningu. Eftirfarandi dæmi sýnir bókhaldsfærslur sem eru stofnaðar á meðan vinnslu stendur.

## <a name="company-setup"></a>Uppsetning fyrirtækis
-   **Uppruna/rekstrar fyrirtæki (USMF)** – Bandarískum dollurum (USD) eru notaðar sem á bókhalds og skýrslugjaldmiðill.
-   **Sameinað fyrirtæki (CON)** – Evrur (EUR) eru notaðar sem á bókhalds og skýrslugjaldmiðill.
    -   **Innleystur hagnaður** – fjárhagslykill 801500
    -   **Innleystur tap** – fjárhagslykill 801600
    -   **Óinnleystur hagnaður**– fjárhagslykill 801600
    -   **Óinnleyst tap**– fjárhagslykill 801400

## <a name="original-transactions"></a>Upphaflegar færslur
### <a name="cash-receipt-transactions-in-usmf"></a>innhreyfingarfærslur Reiðufés í USMF

| Dagsetning       | Fjárhagslykill               | Gjaldmiðill | Upphæð |
|------------|------------------------------|----------|--------|
| 10/11/2015 | 110110 – Reiðufé                | USD      | 500    |
| 10/11/2015 | 130100 – Viðskiptakröfur | USD      | -500   |

## <a name="exchange-rates"></a>Gengi gjaldmiðla

| Úr gjaldmiðli | Í gjaldmiðil | Upphafsdagsetning | Gengi |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 10/1/2015  | 200           |
| EUR           | USD         | 11/1/2015  | 150           |
| EUR           | USD         | 12/1/2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>Framkvæma sameiningu fyrir Október 2015
### <a name="balances-in-the-consolidation-company"></a>Stöður í samstæðufyrirtækinu

| Fjárhagslykill | Gjaldmiðill | Upphæð | Útreikningur    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50%  |
| 130100         | EUR      | -250   | -500 USD × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 30 Nóvember 2015
### <a name="balances-in-the-consolidation-company"></a>Stöður í samstæðufyrirtækinu

| Fjárhagslykill | Gjaldmiðill | Upphæð  | Útreikningur                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333,33  | Upprunaleg upphæð uppá 500 × 66,6667%  |
| 130100         | EUR      | -333,33 | Upprunaleg upphæð uppá -500 × 66,6667% |
| 801400         | EUR      | 83,33   | 333,33 – 250                       |
| 801600         | EUR      | -83,33  | -333,33 – (-250)                   |

Þú munst sjá viðbótarfærslur fyrir upphæðir skýrslugjaldmiðils.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 31 desember 2015
### <a name="balances-in-the-consolidation-company"></a>Stöður í samstæðufyrirtækinu

| Fjárhagslykill | Gjaldmiðill | Upphæð  | Útreikningur                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Upprunaleg upphæð uppá 500 × 1                           |
| 130100         | EUR      | -500,00 | Upprunaleg upphæð uppá -500 × 1                          |
| 801400         | EUR      | 250     | 500 – 333.33 = 166.67 166.67 + 83.33 = 250           |
| 801600         | EUR      | -250    | -500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
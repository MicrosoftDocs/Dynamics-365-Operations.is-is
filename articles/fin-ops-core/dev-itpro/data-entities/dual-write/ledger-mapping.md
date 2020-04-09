---
title: Samþættur fjárhagur
description: Þetta efni lýsir samþættingu fjárhagsupplýsinga milli Finance and Operations og annarra forrita Dynamics 365 með Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6f1a1c7329f0936147fb8f7a8e0e9fea14f7dd4b
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173016"
---
# <a name="integrated-ledger"></a><span data-ttu-id="2ec0c-103">Samþættur fjárhagur</span><span class="sxs-lookup"><span data-stu-id="2ec0c-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="2ec0c-104">Í viðskiptaforriti skilgreina fjárhagsgögn kjarna sem settur er upp fyrir hvernig fyrirtæki stundar viðskipti.</span><span class="sxs-lookup"><span data-stu-id="2ec0c-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="2ec0c-105">Til dæmis lýsa fjárhagsupplýsingar fjárhagsárinu sem fyrirtækið fylgir, gjaldmiðlinum sem það stundar viðskipti í og reikninga sem það notar.</span><span class="sxs-lookup"><span data-stu-id="2ec0c-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="2ec0c-106">Þetta efni lýsir samþættingu þessara grunnupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="2ec0c-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="2ec0c-107">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="2ec0c-107">Templates</span></span>

<span data-ttu-id="2ec0c-108">Fjárhagsupplýsingar innihalda safn af grunnfjárhagseiningaspjöldum sem virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="2ec0c-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="2ec0c-109">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="2ec0c-109">Finance and Operations apps</span></span>      | <span data-ttu-id="2ec0c-110">Líkanadrifin forrit í Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2ec0c-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="2ec0c-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="2ec0c-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="2ec0c-112">Gjaldmiðlar</span><span class="sxs-lookup"><span data-stu-id="2ec0c-112">Currencies</span></span>                       | <span data-ttu-id="2ec0c-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="2ec0c-113">transactioncurrencies</span></span>            |
<span data-ttu-id="2ec0c-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="2ec0c-114">FiscalCalendar</span></span>                   | <span data-ttu-id="2ec0c-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="2ec0c-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="2ec0c-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="2ec0c-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="2ec0c-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="2ec0c-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="2ec0c-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="2ec0c-118">ExchRateType</span></span>                     | <span data-ttu-id="2ec0c-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="2ec0c-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="2ec0c-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="2ec0c-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="2ec0c-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="2ec0c-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="2ec0c-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="2ec0c-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="2ec0c-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="2ec0c-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="2ec0c-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="2ec0c-124">MainAccountCategory</span></span>              | <span data-ttu-id="2ec0c-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="2ec0c-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="2ec0c-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="2ec0c-126">MainAccount</span></span>                      | <span data-ttu-id="2ec0c-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="2ec0c-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="2ec0c-128">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="2ec0c-128">Ledger</span></span>                           | <span data-ttu-id="2ec0c-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="2ec0c-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="2ec0c-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="2ec0c-130">ExchangeRates</span></span>                    | <span data-ttu-id="2ec0c-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="2ec0c-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="2ec0c-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="2ec0c-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="2ec0c-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="2ec0c-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="2ec0c-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="2ec0c-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="2ec0c-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="2ec0c-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="2ec0c-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="2ec0c-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="2ec0c-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="2ec0c-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="2ec0c-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="2ec0c-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="2ec0c-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="2ec0c-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]





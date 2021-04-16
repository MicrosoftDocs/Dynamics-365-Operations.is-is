---
title: VSK-upplýsingar eftir fjárhagsfærslum (skýrsla)
description: Þetta efnisatriði útskýrir hvernig nota á skýrsluna VSK-upplýsingar eftir fjárhagsfærslum til að skoða og prenta upplýsingar um höfuðbókarviðskipti sem VSK-skattur er reiknaður út fyrir.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 75913edcbac0151d5d27d866ff5430b194c62738
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815261"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="2b8c2-103">VSK-upplýsingar eftir fjárhagsfærslum (skýrsla)</span><span class="sxs-lookup"><span data-stu-id="2b8c2-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b8c2-104">Þetta efnisatriði útskýrir hvernig nota á skýrsluna **VSK-upplýsingar eftir fjárhagsfærslum** til að skoða og prenta upplýsingar um höfuðbókarviðskipti sem VSK-skattur er reiknaður út fyrir.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="2b8c2-105">Skattalyklar samanborið við lykla sem ekki eru skattur</span><span class="sxs-lookup"><span data-stu-id="2b8c2-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="2b8c2-106">Skýrslan **VSK-upplýsingar eftir fjárhagsfærslum** sýnir skattafærslur bæði fyrir skattalykla og utan skatta.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="2b8c2-107">Þessir reikningar eru flokkaðir á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="2b8c2-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="2b8c2-108">**Skattalykill** - Lykill er talinn skattalykill þegar skattafærsla er bókuð og aðallykillinn á færslubókarlínunni **Virðisaukaskattur** er skattalykill, svo sem greiðslulykill VSK eða viðskiptaskuldalykill VSK.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="2b8c2-109">**Lykill sem er ekki skattur** - Lykill er talinn tengjast ekki skatti þegar skattafærsla er bókuð og aðallykillinn á upprunalegri færslu er lykill sem tengist ekki skatti, svo sem tekjulykill eða kostnaðarlykill.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="2b8c2-110">Fyrir skattalykla sýna dálkarnir **Uppruni**, **Innskattur** og **Útskattur** í skýrslunni **0** (núll).</span><span class="sxs-lookup"><span data-stu-id="2b8c2-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="2b8c2-111">Fyrir lykla sem ekki eru skattur sýna þeir dálkar fjárhæðir.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="2b8c2-112">Síun á gögnum í skýrslunni</span><span class="sxs-lookup"><span data-stu-id="2b8c2-112">Filtering the data on the report</span></span>

<span data-ttu-id="2b8c2-113">Þegar skýrslan er mynduð eru eftirfarandi sjálfgefnir reitir tiltækir.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="2b8c2-114">Nota má þessai reiti til að sía út hvaða gögn eru sýnd í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="2b8c2-115">Svæði</span><span class="sxs-lookup"><span data-stu-id="2b8c2-115">Field</span></span>                      | <span data-ttu-id="2b8c2-116">Lýsing</span><span class="sxs-lookup"><span data-stu-id="2b8c2-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="2b8c2-117">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="2b8c2-117">Date</span></span>                       | <span data-ttu-id="2b8c2-118">Notaðu reitina í hlutunum **Frá** og **Til** til að skilgreina tímabil fyrir skattafærslur.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="2b8c2-119">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="2b8c2-119">Main account</span></span>               | <span data-ttu-id="2b8c2-120">Notaðu reitina í hlutunum **Frá** og **Til** til að skilgreina tímabil fyrir aðallykla.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="2b8c2-121">VSK-kóði</span><span class="sxs-lookup"><span data-stu-id="2b8c2-121">Sales tax code</span></span>             | <span data-ttu-id="2b8c2-122">Notaðu reitina í hlutunum **Frá** og **Til** til að skilgreina tímabil fyrir VSK-kóða.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="2b8c2-123">Flokkun</span><span class="sxs-lookup"><span data-stu-id="2b8c2-123">Grouping</span></span>                   | <span data-ttu-id="2b8c2-124">Veldu hvort skýrslan eigi að vera flokkuð eftir fjárhagslykli eða VSK-kóða.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="2b8c2-125">Millisamtala eftir VSK-kóða</span><span class="sxs-lookup"><span data-stu-id="2b8c2-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="2b8c2-126">Stilltu þennan valkost á **Já** til að sýna millisamstölur eftir VSK-kóða.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="2b8c2-127">Eingöngu samtölur</span><span class="sxs-lookup"><span data-stu-id="2b8c2-127">Totals only</span></span>                | <span data-ttu-id="2b8c2-128">Stilltu þennan valkost á **Já** til að sýna aðeins samtölur.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="2b8c2-129">Eingöngu aðallyklar</span><span class="sxs-lookup"><span data-stu-id="2b8c2-129">Main accounts only</span></span>         | <span data-ttu-id="2b8c2-130">Stilltu þennan valkost á **Já** til að taka innihalda aðallykla í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="2b8c2-131">Sýnir aðeins lykla án skatta í skýrslunni</span><span class="sxs-lookup"><span data-stu-id="2b8c2-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="2b8c2-132">Til að sýna aðeins lykla sem ekki eru skattar í skýrslunni skaltu setja upp síuskilyrði, svo sem stjörnu (\*), eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Skýrsla sem sýnir lykla án skatta](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
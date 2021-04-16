---
title: Prenta VSK-greiðslu eftir kóðaskýrslu
description: Þetta efni veitir upplýsingar um stillingar og aðgerðir sem þarf til að prenta VSK-greiðslu eftir kóðaskýrslu í bókhalds- eða skattkóðagjaldmiðli.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815453"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="11783-103">Prenta VSK-greiðslu eftir kóðaskýrslu</span><span class="sxs-lookup"><span data-stu-id="11783-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11783-104">Til að prenta skýrsluna **VSK-greiðsla eftir kóða** ferðu í **Skattur** \> **Fyrirspurnir og skýrslur** \> **VSK-skýrslur** \> **VSK-greiðsla eftiri kóða**.</span><span class="sxs-lookup"><span data-stu-id="11783-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="11783-105">Sjálfgefið er að skýrslufjárhæðir séu búnar til í bókhaldsgjaldmiðli lögaðila fyrir alla skýrslukóða sem settir eru upp á síðunni **Kóðar fyrir virðisaukaskattskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="11783-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="11783-106">Þú getur einnig búið til þessa skýrslu þannig að hún sýni VSK-greiðslufjárhæðir í gjaldmiðlum VSK-kóða fyrir alla skýrslukóða sem er úthlutað á VSK-kóða á síðunni **VSK-kóðar**.</span><span class="sxs-lookup"><span data-stu-id="11783-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="11783-107">Kveikja á eiginleikanum</span><span class="sxs-lookup"><span data-stu-id="11783-107">Turn on the feature</span></span>

<span data-ttu-id="11783-108">Á vinnusvæðinu **Eiginleikastjórnun** kveikirðu á eftirfarandi eiginleika: **Mynda VSK-greiðslu eftir kóðaskýrslu í gjaldmiðli VSK-kóða**.</span><span class="sxs-lookup"><span data-stu-id="11783-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="11783-109">Keyrðu skýrsluna</span><span class="sxs-lookup"><span data-stu-id="11783-109">Run the report</span></span>

1. <span data-ttu-id="11783-110">Farðu í **Skatt** \> **Fyrirspurnir og skýrslur** \> **VSK-skýrslur** \> **VSK-greiðsla eftir kóða**.</span><span class="sxs-lookup"><span data-stu-id="11783-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="11783-111">Í reitnum **Skýrslugjaldmiðill** velurðu eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="11783-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="11783-112">**Bókhaldsgjaldmiðill** - Prentaðu skýrlslufjárhæðirnar í bókhaldsgjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="11783-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="11783-113">**Gjaldmiðill VSK-kóða** - Prentaðu skýrslufjárhæðirnar í gjaldmiðlum VSK-kóða.</span><span class="sxs-lookup"><span data-stu-id="11783-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Svarglugginn VSK-greiðsla eftir kóða](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="11783-115">Eftirfarandi skýringarmynd sýnir dæmi um skýrsluna sem er búin til.</span><span class="sxs-lookup"><span data-stu-id="11783-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="11783-116">Skýrslan sýnir að skýrslukóðinn **101** er með gjaldmiðilinn **EUR** ef reiturinn **VSK-gjaldmiðill** er stilltur á **EUR** fyrir VSK-kóðann sem skýrslukóðanum er úthlutað á.</span><span class="sxs-lookup"><span data-stu-id="11783-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Dæmi um VSK-greiðslu eftir kóðaskýrslu](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
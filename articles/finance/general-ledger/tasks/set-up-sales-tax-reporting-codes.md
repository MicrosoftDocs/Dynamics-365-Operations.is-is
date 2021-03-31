---
title: Setja upp skýrslugerðarkóða virðisaukaskatts
description: Skýrslugerðakóðar söluskatts vísa í númer svæða sem má finna í söluskattskýrslu.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be24e18da63d1a613c3c6e72f7c767c7af9b6656
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222144"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="25679-103">Setja upp skýrslugerðarkóða virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="25679-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25679-104">Skýrslugerðakóðar söluskatts vísa í númer svæða sem má finna í söluskattskýrslu.</span><span class="sxs-lookup"><span data-stu-id="25679-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="25679-105">Þær eru notaðar við skýrsluútlit tiltekinna landa.</span><span class="sxs-lookup"><span data-stu-id="25679-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="25679-106">Þær eru einnig notaðar á VSK-greiðslu eftir kóðaskýrslu.</span><span class="sxs-lookup"><span data-stu-id="25679-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="25679-107">Þessi skýrsla sýnir upphæð virðisaukaskatts fyrir jöfnunartímabil sem er sundurliðuð fyrir hvern skýrslugerðarkóða.</span><span class="sxs-lookup"><span data-stu-id="25679-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="25679-108">Eftir að skýrslugerðarkóðar söluskatts eru stofnaðir er hægt að vísa í þá á flipa skýrsluuppsetningar sem hægt er að opna á síðunni **VSK-kóði**.</span><span class="sxs-lookup"><span data-stu-id="25679-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="25679-109">Þessi skráning notar sýnigögn DEMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="25679-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="25679-110">Í **Skoðunarrúðunni** ferðu í **Skattur > Uppsetning > Virðisaukaskattur > Skýrslugerðarkóðar vsk**.</span><span class="sxs-lookup"><span data-stu-id="25679-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="25679-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="25679-111">Click **New**.</span></span>
3. <span data-ttu-id="25679-112">Velurðu útlit skýrslu sem skýrslan kóði tilheyra í.</span><span class="sxs-lookup"><span data-stu-id="25679-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="25679-113">Þessi uppsetning er notuð til að sía tiltæk skýrslugerðarkóða fyrir VSK-kóða.</span><span class="sxs-lookup"><span data-stu-id="25679-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="25679-114">Hver VSK-kóði tilheyrir jöfnunartímabili sem tilheyrir VSK-yfirvöldum sem notast við skýrsluútlit.</span><span class="sxs-lookup"><span data-stu-id="25679-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="25679-115">Í reitinn **Skýrslugerðarkóði** skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="25679-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="25679-116">Færið inn lýsingu til að birta í skýrslum í reitnum **Skýrslutexti**.</span><span class="sxs-lookup"><span data-stu-id="25679-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="25679-117">Færið inn lýsingu vegna innri málefna í svæðinu **Stutta lýsingu**.</span><span class="sxs-lookup"><span data-stu-id="25679-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="25679-118">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="25679-118">Click **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
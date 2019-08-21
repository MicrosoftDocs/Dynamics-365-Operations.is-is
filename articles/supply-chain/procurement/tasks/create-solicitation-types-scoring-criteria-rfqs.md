---
title: Búa til gerðir auglýsinga og viðmið fyrir stigagjöf fyrir tilboðsbeiðnir
description: Þessari handbók sýnir hvernig á að stofna gerð beiðni og tengja þetta við aðferð við stigagjöf.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a3e0d00d674af913953d7fd01183b0289c20d3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844107"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="0dfa0-103">Búa til gerðir auglýsinga og viðmið fyrir stigagjöf fyrir tilboðsbeiðnir</span><span class="sxs-lookup"><span data-stu-id="0dfa0-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0dfa0-104">Þessari handbók sýnir hvernig á að stofna gerð beiðni og tengja þetta við aðferð við stigagjöf.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="0dfa0-105">Hún sýnir einnig hvernig á að nota gerð beiðni fyrir beiðni um tilboð (BUT) sem ákvarðar síðan sjálfgefna aðferð við stigagjöf.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="0dfa0-106">Þessum verkefnum myndi venjulega að framkvæma af Innkaupastjóra.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="0dfa0-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="0dfa0-108">Þú þarft að hafa aðferð við stigagjöf tiltækt áður en byrjað er.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="0dfa0-109">Stofna gerð beiðnar</span><span class="sxs-lookup"><span data-stu-id="0dfa0-109">Create a solicitation type</span></span>
1. <span data-ttu-id="0dfa0-110">Farið í Innkaup og aðföng > Uppsetning > Tilboðsbeiðni > Gerð beiðni.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="0dfa0-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-111">Click New.</span></span>
3. <span data-ttu-id="0dfa0-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0dfa0-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0dfa0-114">Í svæðinu aðferð við Stigagjöf, skal velja stigagjöf sem á að nota fyrir þessa gerð beiðni.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="0dfa0-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-115">Click Save.</span></span>
7. <span data-ttu-id="0dfa0-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="0dfa0-117">Nota Gerð beiðni</span><span class="sxs-lookup"><span data-stu-id="0dfa0-117">Use the solicitation type</span></span>
1. <span data-ttu-id="0dfa0-118">Fara í innkaup og aðföng > Beiðnir um tilboð > Allar beiðnir um tilboð.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="0dfa0-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-119">Click New.</span></span>
3. <span data-ttu-id="0dfa0-120">Í reitnum gerð beiðni skal velja gerð beiðni sem þú varst að stofna.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="0dfa0-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-121">Click OK.</span></span>
5. <span data-ttu-id="0dfa0-122">Afrita skilyrði fyrir stigagjöf</span><span class="sxs-lookup"><span data-stu-id="0dfa0-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="0dfa0-123">Sýndar stigagjafir eru þær sem koma úr aðferð við stigagjöf sem þú tengdir við gerð beiðninnar.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="0dfa0-124">Hægt er að velja að bæta við eða eyða skilyrði á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="0dfa0-125">Einnig er hægt að bæta við nýjum skilyrði með því að afrita þær frá öðrum aðferðir við stigagjöf .</span><span class="sxs-lookup"><span data-stu-id="0dfa0-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="0dfa0-126">Smella á Afrita skilyrði</span><span class="sxs-lookup"><span data-stu-id="0dfa0-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="0dfa0-127">Færa inn eða velja gildi í reitnum aðferð við stigagjöf.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="0dfa0-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-128">Click OK.</span></span>
9. <span data-ttu-id="0dfa0-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0dfa0-129">Close the page.</span></span>


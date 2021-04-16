---
title: Grunnstilla hæfnisvalkosti persónulegs tengiliðar
description: Grunnstilla hæfnisvalkosti fyrir persónulega tengiliði í Microsoft Dynamics 365 Human Resources. Persónulegir tengiliðir geta verið rétthafar eða skjólstæðingar.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49a519aafc56c303765619a66d815d79b668d0f9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790885"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="4d814-104">Grunnstilla hæfnisvalkosti persónulegs tengiliðar</span><span class="sxs-lookup"><span data-stu-id="4d814-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4d814-105">Þessi grein sýnir þér hvernig á að stilla gerðir af persónulegum tengiliðum til að nota í ávinningi hjá Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4d814-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="4d814-106">Persónulegir tengiliðir geta verið rétthafar eða skjólstæðingar.</span><span class="sxs-lookup"><span data-stu-id="4d814-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="4d814-107">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfiskostir persónulegs tengliðar**.</span><span class="sxs-lookup"><span data-stu-id="4d814-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="4d814-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4d814-108">Select **New**.</span></span>

3. <span data-ttu-id="4d814-109">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="4d814-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4d814-110">Svæði</span><span class="sxs-lookup"><span data-stu-id="4d814-110">Field</span></span> | <span data-ttu-id="4d814-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="4d814-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4d814-112">**Hæfnisvalkostur**</span><span class="sxs-lookup"><span data-stu-id="4d814-112">**Eligibility option**</span></span> | <span data-ttu-id="4d814-113">Einstakt nafn eða kóða fyrir hæfileika til að bera kennsl á hæfisvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="4d814-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="4d814-114">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="4d814-114">**Description**</span></span> | <span data-ttu-id="4d814-115">Stutt lýsing á hæfisvalkosti.</span><span class="sxs-lookup"><span data-stu-id="4d814-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="4d814-116">**Hæfniskóði tengiliðar**</span><span class="sxs-lookup"><span data-stu-id="4d814-116">**Contact eligibility code**</span></span> | <span data-ttu-id="4d814-117">Kerfiskóðinn sem lýsir best hæfnisvalkosti einstaklingsins.</span><span class="sxs-lookup"><span data-stu-id="4d814-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="4d814-118">Hægt er að velja um:</span><span class="sxs-lookup"><span data-stu-id="4d814-118">You can choose from:</span></span> <ul><li><span data-ttu-id="4d814-119">Vensl</span><span class="sxs-lookup"><span data-stu-id="4d814-119">Relationship</span></span></li><li><span data-ttu-id="4d814-120">Nemandi</span><span class="sxs-lookup"><span data-stu-id="4d814-120">Student</span></span></li><li><span data-ttu-id="4d814-121">Skjólstæðingur of gamall</span><span class="sxs-lookup"><span data-stu-id="4d814-121">Overage dependent</span></span></li><li><span data-ttu-id="4d814-122">Hreyfihamlaður skjólstæðingur sem er of gamall</span><span class="sxs-lookup"><span data-stu-id="4d814-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="4d814-123">**Staða**</span><span class="sxs-lookup"><span data-stu-id="4d814-123">**Status**</span></span> | <span data-ttu-id="4d814-124">Staða hæfisvalkosts.</span><span class="sxs-lookup"><span data-stu-id="4d814-124">The status of the eligibility option.</span></span> <span data-ttu-id="4d814-125">Ef staða fyrir hæfisvalkost er stillt á óvirk geturðu ekki valið þann valkost fyrir persónulegan tengilið fyrir persónulega tengiliði.</span><span class="sxs-lookup"><span data-stu-id="4d814-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="4d814-126">**Vensl**</span><span class="sxs-lookup"><span data-stu-id="4d814-126">**Relationship**</span></span> | <span data-ttu-id="4d814-127">Tilgreinir samband persónulegra tengiliða og starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="4d814-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="4d814-128">Þessi reitur er aðeins virkur ef hæfnisnúmer tengiliðar er stillt á Samband.</span><span class="sxs-lookup"><span data-stu-id="4d814-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="4d814-129">**Aldur**</span><span class="sxs-lookup"><span data-stu-id="4d814-129">**Age**</span></span> | <span data-ttu-id="4d814-130">Hámarksaldur gjaldgengs persónulegs tengiliðar vegna bótakerfisins.</span><span class="sxs-lookup"><span data-stu-id="4d814-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="4d814-131">Þessi reitur er aðeins virkur ef þú velur samband.</span><span class="sxs-lookup"><span data-stu-id="4d814-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="4d814-132">Þessi aldur er borinn saman við reiknaðan aldur persónulegra tengiliða.</span><span class="sxs-lookup"><span data-stu-id="4d814-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="4d814-133">Reiknaður aldur er: (Dagsetning umfjöllunar - fæðingardagur persónulegs tengiliðar / 365).</span><span class="sxs-lookup"><span data-stu-id="4d814-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="4d814-134">Þessi tala er alltaf heiltala.</span><span class="sxs-lookup"><span data-stu-id="4d814-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="4d814-135">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4d814-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
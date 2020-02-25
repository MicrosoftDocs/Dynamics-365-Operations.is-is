---
title: Grunnstilla hæfnisvalkosti persónulegs tengiliðar
description: Grunnstilla hæfnisvalkosti fyrir persónulega tengiliði í Microsoft Dynamics 365 Human Resources. Persónulegir tengiliðir geta verið rétthafar eða skjólstæðingar.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009433"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="e244c-104">Grunnstilla hæfnisvalkosti persónulegs tengiliðar</span><span class="sxs-lookup"><span data-stu-id="e244c-104">Configure personal contact eligibility options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e244c-105">Þessi grein sýnir þér hvernig á að stilla gerðir af persónulegum tengiliðum til að nota í ávinningi hjá Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e244c-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e244c-106">Persónulegir tengiliðir geta verið rétthafar eða skjólstæðingar.</span><span class="sxs-lookup"><span data-stu-id="e244c-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="e244c-107">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfiskostir persónulegs tengliðar**.</span><span class="sxs-lookup"><span data-stu-id="e244c-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="e244c-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e244c-108">Select **New**.</span></span>

3. <span data-ttu-id="e244c-109">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="e244c-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e244c-110">Svæði</span><span class="sxs-lookup"><span data-stu-id="e244c-110">Field</span></span> | <span data-ttu-id="e244c-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="e244c-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e244c-112">**Hæfnisvalkostur**</span><span class="sxs-lookup"><span data-stu-id="e244c-112">**Eligibility option**</span></span> | <span data-ttu-id="e244c-113">Einstakt nafn eða kóða fyrir hæfileika til að bera kennsl á hæfisvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="e244c-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="e244c-114">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="e244c-114">**Description**</span></span> | <span data-ttu-id="e244c-115">Stutt lýsing á hæfisvalkosti.</span><span class="sxs-lookup"><span data-stu-id="e244c-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="e244c-116">**Hæfniskóði tengiliðar**</span><span class="sxs-lookup"><span data-stu-id="e244c-116">**Contact eligibility code**</span></span> | <span data-ttu-id="e244c-117">Kerfiskóðinn sem lýsir best hæfnisvalkosti einstaklingsins.</span><span class="sxs-lookup"><span data-stu-id="e244c-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="e244c-118">Hægt er að velja um:</span><span class="sxs-lookup"><span data-stu-id="e244c-118">You can choose from:</span></span> <ul><li><span data-ttu-id="e244c-119">Vensl</span><span class="sxs-lookup"><span data-stu-id="e244c-119">Relationship</span></span></li><li><span data-ttu-id="e244c-120">Nemandi</span><span class="sxs-lookup"><span data-stu-id="e244c-120">Student</span></span></li><li><span data-ttu-id="e244c-121">Skjólstæðingur of gamall</span><span class="sxs-lookup"><span data-stu-id="e244c-121">Overage dependent</span></span></li><li><span data-ttu-id="e244c-122">Hreyfihamlaður skjólstæðingur sem er of gamall</span><span class="sxs-lookup"><span data-stu-id="e244c-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="e244c-123">**Staða**</span><span class="sxs-lookup"><span data-stu-id="e244c-123">**Status**</span></span> | <span data-ttu-id="e244c-124">Staða hæfisvalkosts.</span><span class="sxs-lookup"><span data-stu-id="e244c-124">The status of the eligibility option.</span></span> <span data-ttu-id="e244c-125">Ef staða fyrir hæfisvalkost er stillt á óvirk geturðu ekki valið þann valkost fyrir persónulegan tengilið fyrir persónulega tengiliði.</span><span class="sxs-lookup"><span data-stu-id="e244c-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="e244c-126">**Vensl**</span><span class="sxs-lookup"><span data-stu-id="e244c-126">**Relationship**</span></span> | <span data-ttu-id="e244c-127">Tilgreinir samband persónulegra tengiliða og starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="e244c-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="e244c-128">Þessi reitur er aðeins virkur ef hæfnisnúmer tengiliðar er stillt á Samband.</span><span class="sxs-lookup"><span data-stu-id="e244c-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="e244c-129">**Aldur**</span><span class="sxs-lookup"><span data-stu-id="e244c-129">**Age**</span></span> | <span data-ttu-id="e244c-130">Hámarksaldur gjaldgengs persónulegs tengiliðar vegna bótakerfisins.</span><span class="sxs-lookup"><span data-stu-id="e244c-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="e244c-131">Þessi reitur er aðeins virkur ef þú velur samband.</span><span class="sxs-lookup"><span data-stu-id="e244c-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="e244c-132">Þessi aldur er borinn saman við reiknaðan aldur persónulegra tengiliða.</span><span class="sxs-lookup"><span data-stu-id="e244c-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="e244c-133">Reiknaður aldur er: (Dagsetning umfjöllunar - fæðingardagur persónulegs tengiliðar / 365).</span><span class="sxs-lookup"><span data-stu-id="e244c-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="e244c-134">Þessi tala er alltaf heiltala.</span><span class="sxs-lookup"><span data-stu-id="e244c-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="e244c-135">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e244c-135">Select **Save**.</span></span> 

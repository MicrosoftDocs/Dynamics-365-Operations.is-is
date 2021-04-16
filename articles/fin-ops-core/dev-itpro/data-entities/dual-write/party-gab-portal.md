---
title: Notkun Power Portal með gagnalíkani aðila
description: Þetta efnisatriði lýsir breytingum á vefhlutverkum Power Portal vegna gagnalíkans aðila í tvöfaldri skráningu.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833091"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="24f0a-103">Notkun Power Portal með gagnalíkani aðila</span><span class="sxs-lookup"><span data-stu-id="24f0a-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="24f0a-104">Útgáfa tvöfaldrar skráningar niðurröðunarþjónustu, útgáfa 2.0.999.0 og nýrri, inniheldur breytingar gagnalíkans á aðila- og altækri tengiliðaskrá fyrir reikninginn og tengiliðatöflur.</span><span class="sxs-lookup"><span data-stu-id="24f0a-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="24f0a-105">Breytingarnar gera tengls við marga möguleg sem styðja ítarleg viðskiptaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="24f0a-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="24f0a-106">Þessar breytingar eru ekki studdar af vefhlutverkum vefgáttar, þar á meðal viðskiptavinagátt, sem eru sendar eins og þær eru eða sem voru til staðar í umhverfinu áður en sett var upp tvöföld skráning.</span><span class="sxs-lookup"><span data-stu-id="24f0a-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="24f0a-107">Til að vefhlutverkin virki sem skyldi er nauðsynlegt að búa til nýtt vefhlutverk með nýja gagnalíkaninu.</span><span class="sxs-lookup"><span data-stu-id="24f0a-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="24f0a-108">Með öðrum orðum hafa töflurnar breyst en töfluheimildir í viðskiptavinagáttinni hafa ekki breyst.</span><span class="sxs-lookup"><span data-stu-id="24f0a-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="24f0a-109">Þetta efnisatriði útskýrir hvernig á að búa til nýtt vefhlutverk sem virka með nýja ítarlega gagnalíkaninu.</span><span class="sxs-lookup"><span data-stu-id="24f0a-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="24f0a-110">Þessi skýringarmynd sýnir töflutengslin **án** gagnalíkans aðila- og altækrar aðsetursbókar:</span><span class="sxs-lookup"><span data-stu-id="24f0a-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![án aðilalíkans](media/without-party-model.PNG)

<span data-ttu-id="24f0a-112">Þessi skýringarmynd sýnir töflutengslin **með** gagnalíkani aðila- og altækrar aðsetursbók:</span><span class="sxs-lookup"><span data-stu-id="24f0a-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![með aðilalíkani](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="24f0a-114">Stofna nýja töfluheimild</span><span class="sxs-lookup"><span data-stu-id="24f0a-114">Create a new table permission</span></span>

<span data-ttu-id="24f0a-115">Fylgið þessum skrefum til að búa til þessar nýju töfluheimildir:</span><span class="sxs-lookup"><span data-stu-id="24f0a-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="24f0a-116">Skráðu þig inn á [Power Apps](https://make.powerapps.com), og farðu í forritin þín.</span><span class="sxs-lookup"><span data-stu-id="24f0a-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="24f0a-117">Veljið forritið fyrir gáttarumsjón.</span><span class="sxs-lookup"><span data-stu-id="24f0a-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="24f0a-118">Í hliðarstikunni skal velja **Öryggi > Töfluheimildir**.</span><span class="sxs-lookup"><span data-stu-id="24f0a-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="24f0a-119">Búa þarft til þrjár nýjar heimildir:</span><span class="sxs-lookup"><span data-stu-id="24f0a-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="24f0a-120">Tenging tengiliðs við aðila</span><span class="sxs-lookup"><span data-stu-id="24f0a-120">Contact to Party connection</span></span>
    + <span data-ttu-id="24f0a-121">Tenging aðila að reikningi</span><span class="sxs-lookup"><span data-stu-id="24f0a-121">Party to Account connection</span></span>
    + <span data-ttu-id="24f0a-122">Reikningur til að panta tengingu</span><span class="sxs-lookup"><span data-stu-id="24f0a-122">Account to Order connection</span></span>

4. <span data-ttu-id="24f0a-123">Búa til og vista nýja heimild fyrir tengingu tengiliðs við aðila og stilla þessar færibreytur:</span><span class="sxs-lookup"><span data-stu-id="24f0a-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="24f0a-124">**Heiti**: Tenging aðila að reikningi (eða eigið val)</span><span class="sxs-lookup"><span data-stu-id="24f0a-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="24f0a-125">**Töfluheiti**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="24f0a-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="24f0a-126">**Vefsvæði**: Gátt viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="24f0a-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="24f0a-127">**Umfang**: Tengiliður</span><span class="sxs-lookup"><span data-stu-id="24f0a-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="24f0a-128">**Réttindi**: Velja allt</span><span class="sxs-lookup"><span data-stu-id="24f0a-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="24f0a-129">**Vefhlutverk**: Sannvottaðir notendur, fulltrúi viðskiptavinar (eða eigið val)</span><span class="sxs-lookup"><span data-stu-id="24f0a-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="24f0a-130">Búa til og vista nýja heimild fyrir tengingu aðila að reikningi og stilla þessar færibreytur:</span><span class="sxs-lookup"><span data-stu-id="24f0a-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="24f0a-131">**Heiti**: Tenging aðila að reikningi (eða eigið val)</span><span class="sxs-lookup"><span data-stu-id="24f0a-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="24f0a-132">**Töfluheiti**: reikningur</span><span class="sxs-lookup"><span data-stu-id="24f0a-132">**Table Name**: account</span></span>
    + <span data-ttu-id="24f0a-133">**Vefsvæði**: Gátt viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="24f0a-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="24f0a-134">**Umfang**: Yfireining</span><span class="sxs-lookup"><span data-stu-id="24f0a-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="24f0a-135">**Réttindi**: Velja allt</span><span class="sxs-lookup"><span data-stu-id="24f0a-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="24f0a-136">**Heimild yfirtöflu**: Tenging tengiliðs við aðilia</span><span class="sxs-lookup"><span data-stu-id="24f0a-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="24f0a-137">Búa til og vista nýja heimild fyrir Reikningur til að panta tengingu, stilla þessar færibreytur:</span><span class="sxs-lookup"><span data-stu-id="24f0a-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="24f0a-138">**Heiti**: Tenging reiknings við pöntun (eða eigið val)</span><span class="sxs-lookup"><span data-stu-id="24f0a-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="24f0a-139">**Töfluheiti**: salesorder</span><span class="sxs-lookup"><span data-stu-id="24f0a-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="24f0a-140">**Vefsvæði**: Gátt viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="24f0a-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="24f0a-141">**Umfang**: Yfireining</span><span class="sxs-lookup"><span data-stu-id="24f0a-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="24f0a-142">**Réttindi**: Velja allt</span><span class="sxs-lookup"><span data-stu-id="24f0a-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="24f0a-143">**Heimild yfirtöflu**: Tenging aðila að reikningi</span><span class="sxs-lookup"><span data-stu-id="24f0a-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

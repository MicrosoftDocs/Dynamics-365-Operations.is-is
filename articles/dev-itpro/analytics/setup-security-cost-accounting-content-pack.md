---
title: "Setja upp öryggisbúnað fyrir Power BI-efni greiningar á kostnaðarbókhaldi"
description: "Í þessu efnisatriði er útskýrt hvernig hægt er að yfirfæra aðgang á færslustigi í kostnaðarbókhaldi í línu á færslustigi í Microsoft Power BI. Þessi virkni hjálpar til við að tryggja að notendur sjá aðeins Power BI-gögn sem þeir fá aðgang að."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0c0faf0b12368273decacfae88c57707b350bf4
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="4e661-104">Setja upp öryggisbúnað fyrir Power BI-efni greiningar á kostnaðarbókhaldi</span><span class="sxs-lookup"><span data-stu-id="4e661-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4e661-105">Í þessu efnisatriði er útskýrt hvernig hægt er að yfirfæra aðgang á færslustigi í kostnaðarbókhaldi í línu á færslustigi í Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="4e661-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="4e661-106">Þessi virkni hjálpar til við að tryggja að notendur sjá aðeins Power BI-gögn sem þeir fá aðgang að.</span><span class="sxs-lookup"><span data-stu-id="4e661-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

<a name="overview"></a><span data-ttu-id="4e661-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4e661-107">Overview</span></span>
--------

<span data-ttu-id="4e661-108">Í **Greiningu á kostnaðarbókhaldi** notar Microsoft Power BI öryggi á línustigi til að takmarka aðgang notenda.</span><span class="sxs-lookup"><span data-stu-id="4e661-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="4e661-109">Öryggi er byggt á aðgangsstigi stigveldis fyrirtækis sem eru sett upp í færibreytum kostnaðarbókhalds.</span><span class="sxs-lookup"><span data-stu-id="4e661-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="4e661-110">Nánari upplýsingar um **Greiningu á kostnaðarbókhaldi** Power BI innihald er að finna í [Power BI-efni greiningar á kostnaðarbókhaldi](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="4e661-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="4e661-111">Uppsetning</span><span class="sxs-lookup"><span data-stu-id="4e661-111">Setup</span></span>
<span data-ttu-id="4e661-112">Til að yfirfæra öryggi á aðgangsstigi til Power BI þarf eigandi Power BI að fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e661-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span> <span data-ttu-id="4e661-113">**Athugasemd:** Notandinn sem gefur út Power BI-efni **Greiningar á kostnaðarbókhaldi** verður sjálfvirkt eigandi.</span><span class="sxs-lookup"><span data-stu-id="4e661-113">**Note:** The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="4e661-114">Aðeins eigandi getur sett upp öryggi í Power BI.</span><span class="sxs-lookup"><span data-stu-id="4e661-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="4e661-115">Þar að auki, þar til að eigandi bætir við öðrum notendum á PowerBI.com getur enginn nema eigandinn séð hvaða gögn í Power BI-efni **Greiningar á kostnaðarbókhaldi**.</span><span class="sxs-lookup"><span data-stu-id="4e661-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1.  <span data-ttu-id="4e661-116">Birta Power BI í skilgreiningarskránni.</span><span class="sxs-lookup"><span data-stu-id="4e661-116">Publish the definition file to Power BI.</span></span>
2.  <span data-ttu-id="4e661-117">Skráðu þig inn á PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="4e661-117">Sign in to PowerBI.com.</span></span>
3.  <span data-ttu-id="4e661-118">Finna gagnamengi fyrir Power BI-efni **Greiningar á kostnaðarbókhaldi**</span><span class="sxs-lookup"><span data-stu-id="4e661-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4.  <span data-ttu-id="4e661-119">Opnaðu öryggissíðuna.</span><span class="sxs-lookup"><span data-stu-id="4e661-119">Open the security page.</span></span> 

    ![Opna öryggissíðuna](./media/CA-picture-1.png)

5.  <span data-ttu-id="4e661-121">Hlutverkið **Stjórnborð kostnaðarhlutar** er þegar stofnað.</span><span class="sxs-lookup"><span data-stu-id="4e661-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="4e661-122">Bæta við öðrum aðilum sem eru hluti af stigveldisskipan aðgangsstigs kostnaðarbókhalds.</span><span class="sxs-lookup"><span data-stu-id="4e661-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span> 

    ![Bæta við meðlimum](./media/CA-picture-2.png)

<span data-ttu-id="4e661-124">Notendur sem er bætt við hlutverkið **Stjórnborð kostnaðarhlutar** sjá aðeins gögnin sem þeir hafa heimild til að sjá, samkvæmt skilgreiningu í stigveldisskipan aðgangsstigs kostnaðarbókhalds.</span><span class="sxs-lookup"><span data-stu-id="4e661-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span> <span data-ttu-id="4e661-125">**Athugasemd:** Öryggi á línustigi gildir í reitum og skýrslum í Microsoft Dynamics 365 for Finance and Operations sem eru innfelld úr Power BI.</span><span class="sxs-lookup"><span data-stu-id="4e661-125">**Note:** Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="4e661-126">Uppfæri öryggi</span><span class="sxs-lookup"><span data-stu-id="4e661-126">Updating security</span></span>
<span data-ttu-id="4e661-127">Ef uppfærslur eru gerðar á öryggi á aðgangsstigi í kostnaðarbókhaldi, og þú vilt að Power BI endurspegli þessar uppfærslur, þarf að uppfæra einingaverslun fyrir Power BI-efni **Greiningar á kostnaðarbókhaldi**.</span><span class="sxs-lookup"><span data-stu-id="4e661-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="4e661-128">Eftir að þú lýkur uppfærslu á einingaverslun úr Finance and Operations verður að uppfæra gervinga á PowerBI.com. Nánari upplýsingar um hvernig á að gera uppfærslu á einingaverslun í [Uppfærsla einingaverslun](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="4e661-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com. For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="4e661-129">Eigandi Power BI-efnis **Greining kostnaðarbókhalds** verður einnig að gera uppfærslu einingaverslunar ef nýir notendur fá aðgang að stigveldisskipan.</span><span class="sxs-lookup"><span data-stu-id="4e661-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="4e661-130">Þar að auki verður eigandi að bæta við nýjum notendum við hlutverk **Stjórnborð kostnaðarhlutar** á PowerBI.com, svo að öryggi á línustigi sé notað fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="4e661-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="4e661-131">Afvirkjun öryggis</span><span class="sxs-lookup"><span data-stu-id="4e661-131">Disabling security</span></span>
<span data-ttu-id="4e661-132">Gerum ráð fyrir að fyrirtækið vilji takmarka gagnaaðgengi.</span><span class="sxs-lookup"><span data-stu-id="4e661-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="4e661-133">Ef af einhverri ástæðu, öryggi færibreyturnar verður óvirkt þegar kostnaðarbókhald er keyrt, eigandinn verður að bæta notendum við í hlutverkið **Kostnaðarbókari** í Power BI í staðinn.</span><span class="sxs-lookup"><span data-stu-id="4e661-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="4e661-134">Ef öryggislyklinum er breytt úr virkri stöðu í óvirka stöðu, er góð hugmynd að fjarlægja notendur úr hlutverkinu **Stjórnborð kostnaðarhlutar**.</span><span class="sxs-lookup"><span data-stu-id="4e661-134">If you change security from an enabled state to a disabled state, it’s a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="4e661-135">Og öfugt ef þú endurvirkjar öryggisstillingar.</span><span class="sxs-lookup"><span data-stu-id="4e661-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="4e661-136">Notendur geta tilheyrt báðum hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="4e661-136">Users can belong to both roles.</span></span> <span data-ttu-id="4e661-137">Sameiginlegar aðgangur er sameining beggja hlutverka.</span><span class="sxs-lookup"><span data-stu-id="4e661-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="4e661-138">Í tilfelli Power BI-efnis **Greining á kostnaðarbókhaldi** hafa notendur með sameiginlegan aðgang óheftan gagnaaðgang.</span><span class="sxs-lookup"><span data-stu-id="4e661-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="4e661-139">Ef markmiðið er að nota takmarkaðan aðgang verður að úthluta notendum eingöngu á hlutverk **Stjórnborð kostnaðarhlutar**.</span><span class="sxs-lookup"><span data-stu-id="4e661-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="4e661-140">Þessar uppfærslur á öryggi á línustigi taka strax gildi.</span><span class="sxs-lookup"><span data-stu-id="4e661-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="4e661-141">Notendur sem verða fyrir áhrifum ættu að endurræsa vafra sína.</span><span class="sxs-lookup"><span data-stu-id="4e661-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e661-142">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4e661-142">Additional resources</span></span>
<span data-ttu-id="4e661-143">Til að fræðast nánar um öryggi á línustigi Power BI, sjá [Stjórna öryggi líkansins í Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="4e661-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>





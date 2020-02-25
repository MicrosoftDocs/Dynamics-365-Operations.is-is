---
title: Nýjungar eða breytingar í Dynamics 365 Talent (7. janúar 2020)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974431"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="3c988-103">Nýjungar eða breytingar í Dynamics 365 Talent (7. janúar 2020)</span><span class="sxs-lookup"><span data-stu-id="3c988-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="3c988-104">Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="3c988-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="3c988-105">Breytingar í Attract</span><span class="sxs-lookup"><span data-stu-id="3c988-105">Changes in Attract</span></span>

<span data-ttu-id="3c988-106">Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="3c988-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="3c988-107">Breytingar í Onboard</span><span class="sxs-lookup"><span data-stu-id="3c988-107">Changes in Onboard</span></span>

<span data-ttu-id="3c988-108">Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="3c988-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="3c988-109">Breytingar í Core HR</span><span class="sxs-lookup"><span data-stu-id="3c988-109">Changes in Core HR</span></span>

<span data-ttu-id="3c988-110">Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="3c988-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="3c988-111">Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3c988-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="3c988-112">Get ekki eytt starfsmönnum sem eru ekki með atvinnuskrá - (386157)</span><span class="sxs-lookup"><span data-stu-id="3c988-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="3c988-113">Þessi breyting bætir við eyðingarvalkosti í **Starfsmenn án atvinnu** form.</span><span class="sxs-lookup"><span data-stu-id="3c988-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="3c988-114">Starfsmenn birtast á þessu formi þegar engin framtíð, virk eða söguleg ráðning er fyrir hendi fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="3c988-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="3c988-115">Í þessari útgáfu er eyða aðeins virkt fyrir kerfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="3c988-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="3c988-116">Í útgáfu næstu viku verður öryggi hins vegar uppfært svo að allir notendur sem hafa aðstoðarmannahlutverk HR geti fjarlægt starfsmenn án atvinnu.</span><span class="sxs-lookup"><span data-stu-id="3c988-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="3c988-117">Þú getur einnig gert þessar breytingar handvirkt með því að fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3c988-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="3c988-118">Farðu í **Öryggisskilgreining**.</span><span class="sxs-lookup"><span data-stu-id="3c988-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="3c988-119">Á flipanum **Réttindi** síaðu listann **Réttindi** á **Viðhalda starfsmönnum**.</span><span class="sxs-lookup"><span data-stu-id="3c988-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="3c988-120">Í dálkinum **Tilvísanir** veldu **Birta valmyndaratriðin**.</span><span class="sxs-lookup"><span data-stu-id="3c988-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="3c988-121">Í **Yfirlitsvalmyndaratriði** velurðu **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="3c988-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="3c988-122">Stilltu **Eyða** leyfi til að veita.</span><span class="sxs-lookup"><span data-stu-id="3c988-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="3c988-123">Veldu flipann **Óbirtir hlutir**.</span><span class="sxs-lookup"><span data-stu-id="3c988-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="3c988-124">Velja **Birta allt**.</span><span class="sxs-lookup"><span data-stu-id="3c988-124">Select **Publish all**.</span></span>

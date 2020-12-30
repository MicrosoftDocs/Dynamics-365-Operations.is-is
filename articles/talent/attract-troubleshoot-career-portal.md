---
title: Attract-notendur geta ekki sótt um störf á starfagátt
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem Attract notendur geta ekki sótt um störf á starfagáttinni.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461485"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="07687-103">Attract-notendur geta ekki sótt um störf á starfagátt</span><span class="sxs-lookup"><span data-stu-id="07687-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="07687-104">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="07687-104">Issue</span></span>

<span data-ttu-id="07687-105">Attract-notendur geta ekki sótt um störf á starfagátt.</span><span class="sxs-lookup"><span data-stu-id="07687-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="07687-106">Þegar þeir reyna að sækja um starf sem var stofnað á Dynamics 365 Talent: Attract hleður vafrinn síðuna stöðugt og klárar ekki aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="07687-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="07687-107">Orsök</span><span class="sxs-lookup"><span data-stu-id="07687-107">Cause</span></span>

<span data-ttu-id="07687-108">Þetta vandamál kemur upp þegar Talent Relationship Team er ekki með Talent notandahlutverkið.</span><span class="sxs-lookup"><span data-stu-id="07687-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="07687-109">Upplausn</span><span class="sxs-lookup"><span data-stu-id="07687-109">Resolution</span></span>

<span data-ttu-id="07687-110">Úthlutið Talent notandahlutverkinu í Talent Relationship Team.</span><span class="sxs-lookup"><span data-stu-id="07687-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="07687-111">Skráðu þig inn á [Power Platform stjórnendamiðstöðina](https://admin.powerplatform.microsoft.com) með einhverjum eftirtalinna skilríkja stjórnanda:</span><span class="sxs-lookup"><span data-stu-id="07687-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="07687-112">Dynamics 365 stjórnandi</span><span class="sxs-lookup"><span data-stu-id="07687-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="07687-113">Altækur stjórnandi</span><span class="sxs-lookup"><span data-stu-id="07687-113">Global admin</span></span>
   - <span data-ttu-id="07687-114">Power Platform stjórnandi</span><span class="sxs-lookup"><span data-stu-id="07687-114">Power Platform admin</span></span>

2. <span data-ttu-id="07687-115">Í yfirlitssvæðinu skal velja **Umhverfi**, og síðan umhverfið þar sem á að úthluta Talent notandahlutverkinu á Talent Relationship Team.</span><span class="sxs-lookup"><span data-stu-id="07687-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Velja umhverfi](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="07687-117">Í svæðinu **Umhverfi** skal velja **Umhverfisveffang** og skrá inn í stjórnendagátt umhverfis (til dæmis, https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="07687-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="07687-118">Veljið **Stillingar**, veljið **Kerfi** og svo **Öryggi**.</span><span class="sxs-lookup"><span data-stu-id="07687-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Skoða öryggi](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="07687-120">Velja **teymi**.</span><span class="sxs-lookup"><span data-stu-id="07687-120">Select **Teams**.</span></span>

   ![Velja teymi](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="07687-122">Leitið að **Talent Relationship Team** í leitarglugganum og veljið svo teymið úr leitarniðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="07687-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="07687-123">Veljið **STJÓRNA HLUTVERKUM** á borðanum.</span><span class="sxs-lookup"><span data-stu-id="07687-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="07687-124">Í svarglugganum **Stjórna teymishlutverkum** skal velja **Talent notandi** af listanum yfir tiltæk hlutverk og síðan velja **Í lagi** til að nota hlutverkið.</span><span class="sxs-lookup"><span data-stu-id="07687-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Nota hlutverk](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="07687-126">Prófaðu breytingarnar:</span><span class="sxs-lookup"><span data-stu-id="07687-126">Test your changes:</span></span>

   1. <span data-ttu-id="07687-127">Skráðu þig inn í starfagátt úr nýjum vafraglugga.</span><span class="sxs-lookup"><span data-stu-id="07687-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="07687-128">Sækja um starfið í starfagátt.</span><span class="sxs-lookup"><span data-stu-id="07687-128">Apply for the job from the career portal.</span></span> 
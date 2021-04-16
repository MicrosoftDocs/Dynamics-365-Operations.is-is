---
title: Vinna úr breytingum á viðburðum
description: Vinnsla á atburði í lífi atburða í Microsoft Dynamics 365 Human Resources vegna viðburðabreytinga.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3cddc6205660b48abd9067bfdcaa04c9d2ba541
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790909"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="9c3a7-103">Vinna úr breytingum á viðburðum</span><span class="sxs-lookup"><span data-stu-id="9c3a7-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9c3a7-104">Vinnsla á atburði í lífi atburða í Microsoft Dynamics 365 Human Resources vegna tveggja viðburðabreytinga:</span><span class="sxs-lookup"><span data-stu-id="9c3a7-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="9c3a7-105">Afmælisdagurinn breytist</span><span class="sxs-lookup"><span data-stu-id="9c3a7-105">Birthday changes</span></span>
- <span data-ttu-id="9c3a7-106">Hæfisregla hnekkir breytingum á gildistíma</span><span class="sxs-lookup"><span data-stu-id="9c3a7-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="9c3a7-107">Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Vinnsla viðburðabreytinga**.</span><span class="sxs-lookup"><span data-stu-id="9c3a7-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="9c3a7-108">Í valmyndinni **Keyra viðburðabreytingu**, tilgreindu gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="9c3a7-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="9c3a7-109">Svæði</span><span class="sxs-lookup"><span data-stu-id="9c3a7-109">Field</span></span> | <span data-ttu-id="9c3a7-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="9c3a7-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9c3a7-111">Skráningartímabil</span><span class="sxs-lookup"><span data-stu-id="9c3a7-111">Enrollment period</span></span> | <span data-ttu-id="9c3a7-112">Innritunartímabilið til að vinna úr viðburðabreytingum fyrir.</span><span class="sxs-lookup"><span data-stu-id="9c3a7-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="9c3a7-113">Lögaðili</span><span class="sxs-lookup"><span data-stu-id="9c3a7-113">Legal entity</span></span> | <span data-ttu-id="9c3a7-114">Lögaðilinn til að vinna úr viðburðabreytingum fyrir.</span><span class="sxs-lookup"><span data-stu-id="9c3a7-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="9c3a7-115">Ef þú vilt keyra ferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="9c3a7-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="9c3a7-116">Færið inn upplýsingar fyrir ferlið.</span><span class="sxs-lookup"><span data-stu-id="9c3a7-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="9c3a7-117">Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9c3a7-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="9c3a7-118">Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9c3a7-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="9c3a7-119">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9c3a7-119">Select **OK**.</span></span> <span data-ttu-id="9c3a7-120">Ferlið keyrir með breytunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="9c3a7-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="9c3a7-121">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9c3a7-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
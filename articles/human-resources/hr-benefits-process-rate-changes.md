---
title: Vinna úr breytingum á hlutfalli
description: Vinnu breytinga á ávinningi hlutfall í Microsoft Dynamics 365 Human Resources þegar ný eða núverandi bótakerfi hefur breytingu á stillingum hæfisreglna.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 850709480326f6a0871f19ea1bb287631cd58b42
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229942"
---
# <a name="process-rate-changes"></a><span data-ttu-id="08602-103">Vinna úr breytingum á hlutfalli</span><span class="sxs-lookup"><span data-stu-id="08602-103">Process rate changes</span></span>

<span data-ttu-id="08602-104">Vinnu breytinga á ávinningi hlutfall í Microsoft Dynamics 365 Human Resources þegar ný eða núverandi bótakerfi hefur breytingu á stillingum hæfisreglna.</span><span class="sxs-lookup"><span data-stu-id="08602-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="08602-105">Ef ný hæfisregla er búin til og þeim er úthlutað í áætlunina biður þetta kerfið um að endurkeyra hæfi starfsmanna til að athuga hvort starfsmenn geti nú verið gjaldgengir í áætlunina á grundvelli nýrra hæfiskosta.</span><span class="sxs-lookup"><span data-stu-id="08602-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="08602-106">Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Vinnsla uppfærslu á taxtabreytingum**.</span><span class="sxs-lookup"><span data-stu-id="08602-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="08602-107">Í valmyndinni **Keyra uppfærsluferli fríðindataxta**, tilgreindu gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="08602-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="08602-108">Svæði</span><span class="sxs-lookup"><span data-stu-id="08602-108">Field</span></span> | <span data-ttu-id="08602-109">Lýsing</span><span class="sxs-lookup"><span data-stu-id="08602-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="08602-110">**Skráningartímabil**</span><span class="sxs-lookup"><span data-stu-id="08602-110">**Enrollment period**</span></span> | <span data-ttu-id="08602-111">Innritunartímabilið til að vinna úr taxtabreytingum fyrir.</span><span class="sxs-lookup"><span data-stu-id="08602-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="08602-112">Ef þú vilt keyra ferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="08602-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="08602-113">Færið inn upplýsingar fyrir ferlið.</span><span class="sxs-lookup"><span data-stu-id="08602-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="08602-114">Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="08602-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="08602-115">Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="08602-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="08602-116">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="08602-116">Select **OK**.</span></span> <span data-ttu-id="08602-117">Ferlið keyrir með breytunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="08602-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="08602-118">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="08602-118">Select **OK**.</span></span>

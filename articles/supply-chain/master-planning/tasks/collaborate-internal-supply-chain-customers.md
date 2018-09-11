--- 
title: "Vinna með birgjum innri aðfangakeðju"
description: "Þessi verklýsing sýnir hvernig á að skoða allar áætlaðar pantanir sem verða uppfylltar af samstæðulánardrottinn."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 19a4083fc0f5339ba357be1fcef6be3119388ae2
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="dec6f-103">Vinna með birgjum innri aðfangakeðju</span><span class="sxs-lookup"><span data-stu-id="dec6f-103">Collaborate with internal supply chain customers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dec6f-104">Þessi verklýsing sýnir hvernig á að skoða allar áætlaðar pantanir sem verða uppfylltar af samstæðulánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="dec6f-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="dec6f-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.</span><span class="sxs-lookup"><span data-stu-id="dec6f-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="dec6f-106">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="dec6f-106">Click Master planning.</span></span>
2. <span data-ttu-id="dec6f-107">Í reitinn áætlun skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="dec6f-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="dec6f-108">Í reitinn Áætlun skal velja áætlun 10.</span><span class="sxs-lookup"><span data-stu-id="dec6f-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="dec6f-109">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="dec6f-109">Click Run.</span></span>
4. <span data-ttu-id="dec6f-110">Í svæðinu Fjölda þráða skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="dec6f-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="dec6f-111">Þetta táknar fjölda samhliða þráða sem kemur til með að vera notuð við aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="dec6f-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="dec6f-112">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dec6f-112">Click OK.</span></span>
    * <span data-ttu-id="dec6f-113">Þetta gæti tekið nokkra stund.</span><span class="sxs-lookup"><span data-stu-id="dec6f-113">This may take a while.</span></span>  
6. <span data-ttu-id="dec6f-114">Smellt er á Áætluð eftirspurn innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="dec6f-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="dec6f-115">Smellt er á áætlaða eftirspurn innan samstæðu á útleið</span><span class="sxs-lookup"><span data-stu-id="dec6f-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="dec6f-116">Þessi síða gefur yfirlit yfir alla áætlaða eftirspurn sem verður uppfyllt af innri lánardrottni aðfangakeðju.</span><span class="sxs-lookup"><span data-stu-id="dec6f-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="dec6f-117">Víkkaðu út hlutann Upplýsingar um eftirspurn uppstreymis.</span><span class="sxs-lookup"><span data-stu-id="dec6f-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="dec6f-118">Í þessum hluta er hægt að sjá upplýsingar um hvernig verður hægt að uppfylla eftirspurnina.</span><span class="sxs-lookup"><span data-stu-id="dec6f-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="dec6f-119">Hugsanlega þarf að bíða eftir aðaláætlanagerð til að vera keyrð hjá birginum áður en þú getur séð frekari upplýsingar hér.</span><span class="sxs-lookup"><span data-stu-id="dec6f-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  



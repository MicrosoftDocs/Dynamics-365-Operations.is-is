---
title: Vinna með birgjum innri aðfangakeðju
description: Þessi verklýsing sýnir hvernig á að skoða allar áætlaðar pantanir sem verða uppfylltar af samstæðulánardrottni.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84c42e550d51e40b7f777c3da67ed765519ddfd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430355"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="8c649-103">Vinna með birgjum innri aðfangakeðju</span><span class="sxs-lookup"><span data-stu-id="8c649-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c649-104">Þessi verklýsing sýnir hvernig á að skoða allar áætlaðar pantanir sem verða uppfylltar af samstæðulánardrottni.</span><span class="sxs-lookup"><span data-stu-id="8c649-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="8c649-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.</span><span class="sxs-lookup"><span data-stu-id="8c649-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="8c649-106">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="8c649-106">Click Master planning.</span></span>
2. <span data-ttu-id="8c649-107">Í reitinn áætlun skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="8c649-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="8c649-108">Í reitinn Áætlun skal velja áætlun 10.</span><span class="sxs-lookup"><span data-stu-id="8c649-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="8c649-109">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="8c649-109">Click Run.</span></span>
4. <span data-ttu-id="8c649-110">Í svæðinu Fjölda þráða skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="8c649-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="8c649-111">Þetta táknar fjölda samhliða þráða sem kemur til með að vera notuð við aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="8c649-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="8c649-112">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8c649-112">Click OK.</span></span>
    * <span data-ttu-id="8c649-113">Þetta gæti tekið nokkra stund.</span><span class="sxs-lookup"><span data-stu-id="8c649-113">This may take a while.</span></span>  
6. <span data-ttu-id="8c649-114">Smellt er á Áætluð eftirspurn innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="8c649-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="8c649-115">Smellt er á áætlaða eftirspurn innan samstæðu á útleið</span><span class="sxs-lookup"><span data-stu-id="8c649-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="8c649-116">Þessi síða gefur yfirlit yfir alla áætlaða eftirspurn sem verður uppfyllt af innri lánardrottni aðfangakeðju.</span><span class="sxs-lookup"><span data-stu-id="8c649-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="8c649-117">Víkkaðu út hlutann Upplýsingar um eftirspurn uppstreymis.</span><span class="sxs-lookup"><span data-stu-id="8c649-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="8c649-118">Í þessum hluta er hægt að sjá upplýsingar um hvernig verður hægt að uppfylla eftirspurnina.</span><span class="sxs-lookup"><span data-stu-id="8c649-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="8c649-119">Hugsanlega þarf að bíða eftir aðaláætlanagerð til að vera keyrð hjá birginum áður en þú getur séð frekari upplýsingar hér.</span><span class="sxs-lookup"><span data-stu-id="8c649-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  


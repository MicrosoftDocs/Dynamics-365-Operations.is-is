---
title: Skoða áætlaða eftirspurn á útleið innan samstæðu
description: Þessi verklýsing sýnir hvernig á að skoða allar áætlaðar pantanir sem verða uppfylltar af samstæðulánardrottinn.
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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bc3addb11d77a5098e80a5826bfea289d232548
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254288"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="8202c-103">Skoða áætlaða eftirspurn á útleið innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="8202c-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8202c-104">Þessi verklýsing sýnir hvernig á að skoða allar áætlaðar pantanir sem verða uppfylltar af samstæðulánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="8202c-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="8202c-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.</span><span class="sxs-lookup"><span data-stu-id="8202c-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="8202c-106">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="8202c-106">Click Master planning.</span></span>
2. <span data-ttu-id="8202c-107">Í reitinn áætlun skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="8202c-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="8202c-108">Í reitinn Áætlun skal velja áætlun 10.</span><span class="sxs-lookup"><span data-stu-id="8202c-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="8202c-109">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="8202c-109">Click Run.</span></span>
4. <span data-ttu-id="8202c-110">Í svæðinu Fjölda þráða skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="8202c-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="8202c-111">Þetta táknar fjölda samhliða þráða sem kemur til með að vera notuð við aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="8202c-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="8202c-112">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8202c-112">Click OK.</span></span>
    * <span data-ttu-id="8202c-113">Þetta gæti tekið nokkra stund.</span><span class="sxs-lookup"><span data-stu-id="8202c-113">This may take a while.</span></span>  
6. <span data-ttu-id="8202c-114">Smellt er á Áætluð eftirspurn innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="8202c-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="8202c-115">Smellt er á áætlaða eftirspurn innan samstæðu á útleið</span><span class="sxs-lookup"><span data-stu-id="8202c-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="8202c-116">Þessi síða gefur yfirlit yfir alla áætlaða eftirspurn sem verður uppfyllt af innri lánardrottni aðfangakeðju.</span><span class="sxs-lookup"><span data-stu-id="8202c-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="8202c-117">Víkkaðu út hlutann Upplýsingar um eftirspurn uppstreymis.</span><span class="sxs-lookup"><span data-stu-id="8202c-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="8202c-118">Í þessum hluta er hægt að sjá upplýsingar um hvernig verður hægt að uppfylla eftirspurnina.</span><span class="sxs-lookup"><span data-stu-id="8202c-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="8202c-119">Hugsanlega þarf að bíða eftir aðaláætlanagerð til að vera keyrð hjá birginum áður en þú getur séð frekari upplýsingar hér.</span><span class="sxs-lookup"><span data-stu-id="8202c-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
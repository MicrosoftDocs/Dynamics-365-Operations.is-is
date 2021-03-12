---
title: Setja upp tilraun
description: Í þessu efnisatriði er lýst hvernig á að setja upp tilraun í þjónustu þriðja aðila.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 1a60eb459d6d6f710e43ac5418b9375420ca8387
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000791"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="80e88-103">Setja upp tilraun</span><span class="sxs-lookup"><span data-stu-id="80e88-103">Set up an experiment</span></span>

<span data-ttu-id="80e88-104">Þegar búið er að [skilgreina og ákvarða hvaða árangursmælingar á að nota](experimentation-identify.md) þarf að setja upp tilraunina í þjónustu þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="80e88-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="80e88-105">Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="80e88-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="80e88-106">Önnur skref eru afgreidd í aðskildum efnisatriðum.</span><span class="sxs-lookup"><span data-stu-id="80e88-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="80e88-107">[ ![Tilraunaferli notanda - Uppsetning](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="80e88-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="80e88-108">Setja upp tilraun í þjónustu þriðja aðila</span><span class="sxs-lookup"><span data-stu-id="80e88-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="80e88-109">Nú ætti að vera búið að velja þjónustu þriðja aðila til að keyra og fylgjast með tilrauninni og setja upp tengil tilraunarinnar.</span><span class="sxs-lookup"><span data-stu-id="80e88-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="80e88-110">Þessi skilyrði eru skráð í [Tilraunagerð í Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="80e88-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="80e88-111">Fylgið skrefunum sem þarf til að búa til tilraunir í þjónustu þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="80e88-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="80e88-112">Ef tengillinn er skilgreindur á réttan hátt verður fullbúinn listi yfir allar tilraunir sem settar eru upp í þjónustu þriðja birtur í vefsmið Commerce innan 5 mínútna.</span><span class="sxs-lookup"><span data-stu-id="80e88-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="80e88-113">Setja upp árangursmælingar</span><span class="sxs-lookup"><span data-stu-id="80e88-113">Set up your success metrics</span></span>
<span data-ttu-id="80e88-114">Sérhver tilraun þarf mælingar til að mæla áhrif afbrigðanna og til að sannprófa tilgátuna.</span><span class="sxs-lookup"><span data-stu-id="80e88-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="80e88-115">Fylgið skrefunum hér að neðan til að virkja útreikning á mælingum í þjónustu þriðja aðila með virkum tilvikum fjarmælinga úr Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="80e88-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="80e88-116">Til að setja upp árangursmælingar skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="80e88-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="80e88-117">Í vefsmið Commerce skal velja **Síður** á vinstra yfirlitssvæðinu og síðan velja síðuna sem á að safna mælingum fyrir.</span><span class="sxs-lookup"><span data-stu-id="80e88-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="80e88-118">Farið í hlutann **Kenni tilvika til að fylgjast með** á eiginleikasvæðinu hægra megin á síðunni eða einingunni sem á að fylgjast með.</span><span class="sxs-lookup"><span data-stu-id="80e88-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="80e88-119">Velja **Skoða**.</span><span class="sxs-lookup"><span data-stu-id="80e88-119">Select **View**.</span></span> <span data-ttu-id="80e88-120">Listi yfir öll tilvikskenni birtist.</span><span class="sxs-lookup"><span data-stu-id="80e88-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="80e88-121">Afritið tilvikið sem á að rekja, og límið tilvikslykilinn á tilgreindan stað í þjónustu þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="80e88-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="80e88-122">Ef þörf er á fleiri en einu tilviki skal afrita lyklana einn í einu.</span><span class="sxs-lookup"><span data-stu-id="80e88-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="80e88-123">Til að fá upplýsingar um öll tiltæk tilvik og eigindir, þar á meðal síðuyfirlit og tekjurakningu, skal skoða [Tilvik Commerce-íhluta fyrir greiningu og bilanaleit](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="80e88-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="80e88-124">Farið í gegnum öll önnur skref til að rekja mælingar eins og krafist er í þjónustu þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="80e88-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="80e88-125">Fyrra skref</span><span class="sxs-lookup"><span data-stu-id="80e88-125">Previous step</span></span>
[<span data-ttu-id="80e88-126">Auðkenna tilgátu og ákvarða mælieiningar fyrir tilraun</span><span class="sxs-lookup"><span data-stu-id="80e88-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="80e88-127">Næsta skref</span><span class="sxs-lookup"><span data-stu-id="80e88-127">Next step</span></span>
[<span data-ttu-id="80e88-128">Tengja og breyta tilraun</span><span class="sxs-lookup"><span data-stu-id="80e88-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

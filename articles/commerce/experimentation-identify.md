---
title: Auðkenna tilgátu og ákvarða mælieiningar fyrir tilraun
description: Þetta efnisatriði lýsir því hvernig hægt er að bera kennsl á tilgátuna og árangursmælingar fyrir tilraun sem keyrð verður á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a3f5d44e008e4092557d75c8f5d830d5ae36a091
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799049"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="9de82-103">Auðkenna tilgátu og ákvarða árangursmælingar fyrir tilraun</span><span class="sxs-lookup"><span data-stu-id="9de82-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="9de82-104">Fyrsti áfangi í tilraunaferlinu felur í sér að auðkenna tilgátu tilraunarinnar og ákvarða mælieiningarnar sem fylgst verður með til að meta árangur.</span><span class="sxs-lookup"><span data-stu-id="9de82-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="9de82-105">Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í [uppsetningu og vinnslu á tilraun](experimentation-overview.md) á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9de82-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="9de82-106">Önnur skref eru afgreidd í aðskildum efnisatriðum.</span><span class="sxs-lookup"><span data-stu-id="9de82-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="9de82-107">[ ![Tilraunastarfssemi notanda - Auðkenna](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9de82-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="9de82-108">Tilgáta er yfirlýsing þar sem þú spáir fyrir um útkomu tilraunarinnar.</span><span class="sxs-lookup"><span data-stu-id="9de82-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="9de82-109">Margir þættir koma við sögu þegar tilgáta er skilgreind, t.d. rannsóknir á hegðun notanda og gögn vefsvæðis sem safnað hefur verið saman.</span><span class="sxs-lookup"><span data-stu-id="9de82-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="9de82-110">Með tilgátunni skilgreinir þú þá forsendu eða kenningu sem þú vilt sannprófa með tilrauninni.</span><span class="sxs-lookup"><span data-stu-id="9de82-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="9de82-111">Dæmi um tilgátu fyrir tilraunina gæti verið að „*mynd af hvítum stuttermabol á heimasíðunni minni mun auka fjölda smella frekar en dökkblá peysa yfir sumarmánuðina vegna þess að fólk vill klæðast einhverju léttu og í ljósum litum yfir sumartímann.*“</span><span class="sxs-lookup"><span data-stu-id="9de82-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="9de82-112">Í slíku tilfelli býrðu til afbrigði sem innihalda hvítan stuttermabol og dökkbláa peysu og gefur bæði út á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="9de82-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="9de82-113">Til að sannprófa tilgátu ætti velgengni eða mislukkun tilraunar að vera tengd beint við aðgerðir notanda; til dæmis hvort notandi vefsvæðisins smellir á tengil eða hnapp.</span><span class="sxs-lookup"><span data-stu-id="9de82-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks on a link or button.</span></span> <span data-ttu-id="9de82-114">Þessar aðgerðir verða að samsvara tilvikum sem þjónusta þriðja aðila sem fylgir tilrauninni eftur verður tilkynnt um.</span><span class="sxs-lookup"><span data-stu-id="9de82-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="9de82-115">Með tímanum verður hlutfall notenda sem grípa til aðgerðarinnar gefið upp sem mælieining sem hægt er að nota til að búa til skýrslur og gera greiningar.</span><span class="sxs-lookup"><span data-stu-id="9de82-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="9de82-116">Til að skoða öll tilvik og eiginleika skal skoða [Tilvik Commerce-íhluta fyrir greiningu og bilanaleit](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="9de82-116">To review all of the available events and attributes, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>

## <a name="previous-step"></a><span data-ttu-id="9de82-117">Fyrra skref</span><span class="sxs-lookup"><span data-stu-id="9de82-117">Previous step</span></span>
[<span data-ttu-id="9de82-118">Tilraunir í Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9de82-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="9de82-119">Næsta skref</span><span class="sxs-lookup"><span data-stu-id="9de82-119">Next step</span></span>
[<span data-ttu-id="9de82-120">Setja upp tilraun</span><span class="sxs-lookup"><span data-stu-id="9de82-120">Set up an experiment</span></span>](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
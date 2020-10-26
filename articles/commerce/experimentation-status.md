---
title: Fara yfir stöðu tilraunar
description: Í þessu efnisatriði er útskýrt hvaða staða tilraun er með í tilraunaferlinu í Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930217"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="35dfd-103">Fara yfir stöðu tilraunar</span><span class="sxs-lookup"><span data-stu-id="35dfd-103">Review the status of an experiment</span></span>
<span data-ttu-id="35dfd-104">Mörg skref fylgja því að setja upp og keyra tilraun í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="35dfd-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="35dfd-105">Upplýsingar um tilraunaferlið er að finna í [Tilraunagerð í Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="35dfd-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="35dfd-106">Til að komast að því hvar tilraun er stödd í ferlinu skal fara í flipann **Tilraunir** í vefsmiðnum.</span><span class="sxs-lookup"><span data-stu-id="35dfd-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="35dfd-107">Listi yfir tilraunir er sýndur með stöðu hverrar tilraunar í bæði Commerce og þjónustu þriðja aðila sem er notaður til að gera kleift að stofna tilraunir, úthluta afbrigðum og greina gögn.</span><span class="sxs-lookup"><span data-stu-id="35dfd-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="35dfd-108">Í dálknum **Staða Commerce** er hugsanlegt að eftirfarandi gildi séu sýnd.</span><span class="sxs-lookup"><span data-stu-id="35dfd-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="35dfd-109">**Drög** - Tilraunin er tengd við síðu eða brot í Commerce og verið er að breyta henni.</span><span class="sxs-lookup"><span data-stu-id="35dfd-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="35dfd-110">**Birt** - Afbrigði tilrauna eru tilbúin til birtingar á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="35dfd-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="35dfd-111">Ef tilraunin er í gangi í þjónustu þriðja aðila, sjá notendur vefsvæðisins afbrigði síðunnar eða brotsins eins og þjónusta þriðja aðila hefur valið.</span><span class="sxs-lookup"><span data-stu-id="35dfd-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="35dfd-112">**Óbirt** - Tilraunin er ekki lengur í boði á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="35dfd-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="35dfd-113">Notendur vefsvæðis sjá aðeins sjálfgefna útgáfu síðunnar eða brotsins, jafnvel þótt tilraunin sé í gangi í þjónustu þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="35dfd-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="35dfd-114">**Lokið** - Tilraunin hefur haft sinn gang og afbrigði var sett á netið fyrir alla notendur vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="35dfd-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="35dfd-115">Á sama hátt, í dálknum **staða þriðja aðila**, verða eftirfarandi gildi sýnd til að gefa til kynna stöðu tilraunanna í þjónustu þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="35dfd-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="35dfd-116">**Drög** - Tilraunin er sett upp í þjónustu þriðja aðila en hefur ekki verið sett í gang.</span><span class="sxs-lookup"><span data-stu-id="35dfd-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="35dfd-117">**Í gangi** - Tilraunin var sett í gang í þjónustu þriðja aðila og er að safna gögnum.</span><span class="sxs-lookup"><span data-stu-id="35dfd-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="35dfd-118">**Gert hlé** - Tilraunin hefur verið stöðvuð og er ekki að safna gögnum.</span><span class="sxs-lookup"><span data-stu-id="35dfd-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="35dfd-119">Nauðsynlegt er að halda áfram með tilraunina til að hún geti safnað gögnum á nýjan leik.</span><span class="sxs-lookup"><span data-stu-id="35dfd-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="35dfd-120">**Safnvistað** - Tilraunin hefur haft sinn gang og hefur verið skrásett í þjónustu þriðja aðila til síðari nota.</span><span class="sxs-lookup"><span data-stu-id="35dfd-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="35dfd-121">Skýringarmyndin hér að neðan sýnir bæði settin af stöðum og hvernig þau tengjast hvort öðru.</span><span class="sxs-lookup"><span data-stu-id="35dfd-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="35dfd-122">[ ![Stöður tilraunavinnu](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="35dfd-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>
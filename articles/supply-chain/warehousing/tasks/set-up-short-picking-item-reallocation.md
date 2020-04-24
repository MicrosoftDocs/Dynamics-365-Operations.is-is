---
title: Setja upp endurúthlutun fyrir stutta vörutiltekt
description: Þessi verklýsing sýnir hvernig starfsmenn vöruhúss geta fundið aðrar staðsetningar fljótt ef það eru ekki nægilegar birgðir á staðsetningunni þangað sem þeim var beint.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e860a54c2306f8140947b77cdcb538160a84e06f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216806"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="3b64c-103">Setja upp endurúthlutun fyrir stutta vörutiltekt</span><span class="sxs-lookup"><span data-stu-id="3b64c-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b64c-104">Þessi verklýsing sýnir hvernig starfsmenn vöruhúss geta fundið aðrar staðsetningar fljótt ef það eru ekki nægilegar birgðir á staðsetningunni þangað sem þeim var beint.</span><span class="sxs-lookup"><span data-stu-id="3b64c-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn't sufficient inventory at the location they've been directed to.</span></span> <span data-ttu-id="3b64c-105">Það er hægt að nota sjálfvirkt endurúthlutunarferli, sem notar staðsetningarleiðbeiningar til að sækja vörur ef þær eru tiltækar á aðra staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="3b64c-105">It's possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they're available at another location.</span></span> <span data-ttu-id="3b64c-106">Einnig er þegar handvirka endurúthlutunin er notuð, er lista yfir staðsetningar með tiltæku magni sýndur í fartækinu, þar sem starfsmaður í vöruhúsi getur valið hvaða staðsetningar til að nota birgðir úr.</span><span class="sxs-lookup"><span data-stu-id="3b64c-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="3b64c-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="3b64c-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="3b64c-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="3b64c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="3b64c-109">Setja upp vinnuundantekningar</span><span class="sxs-lookup"><span data-stu-id="3b64c-109">Set up work exceptions</span></span>
1. <span data-ttu-id="3b64c-110">Í **Skoðunarrúðu** ferðu í **Vöruhúsakerfi > Uppsetning > Vinna > Undantekningar verks**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-110">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="3b64c-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-111">Click **New**.</span></span> <span data-ttu-id="3b64c-112">Það er hægt að skilgreina margar vinnuundantekningar ásamt mismunandi endurúthlutunarreglum til að gera starfsmaður í vöruhúsi mögulegt að velja eitt á grundvelli þess sem sendingin sem verið er að vinna þarf.</span><span class="sxs-lookup"><span data-stu-id="3b64c-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="3b64c-113">Í reitinn **Kenni undantekningar verks** skaltu færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="3b64c-113">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="3b64c-114">Gefðu vinnuundantekningunni titil sem segir til um tilgang hennar.</span><span class="sxs-lookup"><span data-stu-id="3b64c-114">Give the work exception a title to indicate what it's used for.</span></span> <span data-ttu-id="3b64c-115">Til dæmis, handbók fyrir of litla tiltekt.</span><span class="sxs-lookup"><span data-stu-id="3b64c-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="3b64c-116">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="3b64c-116">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="3b64c-117">í reitnum **Gerð undantekningar** skaltu velja „of lítil tiltekt“.</span><span class="sxs-lookup"><span data-stu-id="3b64c-117">In the **Exception** type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="3b64c-118">Veldu gátreitinn **Leiðrétta birgðir**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-118">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="3b64c-119">Þessi valkostur þýðir að birgðir verða sjálfvirkt leiðréttar á 0 á staðsetningu þar sem tiltekt er of lítil.</span><span class="sxs-lookup"><span data-stu-id="3b64c-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="3b64c-120">Í reitinn **Sjálfgefinn kóði leiðréttingargerðar** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="3b64c-120">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="3b64c-121">Til dæmis í USMF er hægt að velja "Remove Res Adj Out".</span><span class="sxs-lookup"><span data-stu-id="3b64c-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="3b64c-122">Í reitnum **Endurúthlutun vöru** er valið "Handvirkt".</span><span class="sxs-lookup"><span data-stu-id="3b64c-122">In the **Item reallocation** field, select 'Manual'.</span></span> <span data-ttu-id="3b64c-123">Ef valið er Handvirkt, eða Sjálfvirkar og Handvirkar, þarf starfsmaður í vöruhúsi að geta notað handvirka endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="3b64c-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="3b64c-124">Setja upp starfsmann til að nota handvirka endurúthlutun vöru</span><span class="sxs-lookup"><span data-stu-id="3b64c-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="3b64c-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3b64c-125">Close the page.</span></span>
2. <span data-ttu-id="3b64c-126">Í **Skoðunarrúðu** ferðu í **Vöruhúsakerfi > Uppsetning > Vinna > Starfskraftur**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-126">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="3b64c-127">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-127">Click **Edit**.</span></span>
4. <span data-ttu-id="3b64c-128">Í listanum skal velja starfskraft 24.</span><span class="sxs-lookup"><span data-stu-id="3b64c-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="3b64c-129">Útvíkkaðu flýtiflipann **Vinna**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-129">Expand the **Work** fastTab.</span></span>
6. <span data-ttu-id="3b64c-130">Veldu „Já“ í reitnum **Leyfa handvirka endurúthlutun vöru**.</span><span class="sxs-lookup"><span data-stu-id="3b64c-130">Select 'Yes' in the **Allow manual item reallocation** field.</span></span>


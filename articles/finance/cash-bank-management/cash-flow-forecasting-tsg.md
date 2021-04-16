---
title: Úrræðaleit vegna uppsetningar sjóðstreymisspár
description: Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina sjóðstreymisspár. Þar er svarað algengum spurningum um uppsetningu sjóðstreymis, uppfærslur á sjóðstreymi og sjóðstreymi Power BI.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827315"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="2b846-104">Úrræðaleit vegna uppsetningar sjóðstreymisspár</span><span class="sxs-lookup"><span data-stu-id="2b846-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b846-105">Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina sjóðstreymisspár.</span><span class="sxs-lookup"><span data-stu-id="2b846-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="2b846-106">Þar er svarað algengum spurningum um uppsetningu sjóðstreymis, uppfærslur á sjóðstreymi og sjóðstreymi Power BI.</span><span class="sxs-lookup"><span data-stu-id="2b846-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="2b846-107">Hvers vegna er sjóðstreymi sýnd fyrir aðeins einn lögaðila?</span><span class="sxs-lookup"><span data-stu-id="2b846-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="2b846-108">Sjóðstreymisspá er skilgreind og reiknuð fyrir hvern lögaðila fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="2b846-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="2b846-109">Power BI-skýrslur og möguleiki sjóðsstreymisspáa í Fjármálainnsýn sýna niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="2b846-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="2b846-110">Setja verður upp sjóðstreymisspá fyrir hvern lögaðila sem á að skoða spá fyrir.</span><span class="sxs-lookup"><span data-stu-id="2b846-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="2b846-111">Farið yfir skilgreiningu sjóðstreymisspár í öllum lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="2b846-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="2b846-112">Að öðrum kosti skal fara yfir skilgreiningu allra lögaðila fyrir sjóðstreymisspá og ganga úr skugga um að þær séu rétt stilltar.</span><span class="sxs-lookup"><span data-stu-id="2b846-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="2b846-113">Hvers vegna sýnir Power BI ekki öll sjóðstreymisgögnin?</span><span class="sxs-lookup"><span data-stu-id="2b846-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="2b846-114">Ljúka þarf nokkrum skrefum áður en sjóðstreymisspár geta birst í Power BI-yfirlitum.</span><span class="sxs-lookup"><span data-stu-id="2b846-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="2b846-115">Farið yfir eftirfarandi gátlista og gangið úr skugga um að öllum skrefum sé lokið:</span><span class="sxs-lookup"><span data-stu-id="2b846-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="2b846-116">Setjið upp sjóðstreymi fyrir hvern lögaðila.</span><span class="sxs-lookup"><span data-stu-id="2b846-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="2b846-117">Í færibreytum fjárhags skal stilla gjaldmiðil kerfisins og gerð gengisins.</span><span class="sxs-lookup"><span data-stu-id="2b846-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="2b846-118">Stillið fjárhagsbókhaldsgjaldmiðilinn og gerð gengisins.</span><span class="sxs-lookup"><span data-stu-id="2b846-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="2b846-119">Færið inn gengið milli færslugjaldmiðils og bókhaldsgjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="2b846-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="2b846-120">Færið inn gengið milli bókhaldsgjaldmiðils og kerfisgjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="2b846-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="2b846-121">Færið inn gengið milli bókhaldsgjaldmiðils og hvers bankagjaldmiðils fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="2b846-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="2b846-122">Hvers vegna virkaði sjóðstreymi Power BI í fyrri útgáfum en er nú autt?</span><span class="sxs-lookup"><span data-stu-id="2b846-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="2b846-123">Gangið úr skugga um að mælingarnar „Sjóðstreymismæling V2“ og „LedgerCovLiquidityMeasurement“ úr einingaverslun hafi verið skilgreindar.</span><span class="sxs-lookup"><span data-stu-id="2b846-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="2b846-124">Frekari upplýsingar um það hvernig á að vinna með gögn í einingaverslun er að finna í [Power BI samþætting við einingaverslun](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="2b846-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="2b846-125">Gangið úr skugga um að búið sé að fara í gegnum öll skrefin sem þarf að taka til að skoða Power BI-efni.</span><span class="sxs-lookup"><span data-stu-id="2b846-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="2b846-126">Frekari upplýsingar má finna á [Yfirlit yfir reiðufé Power BI efni](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="2b846-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="2b846-127">Hafa einingar einingaverslunar verið uppfærðar?</span><span class="sxs-lookup"><span data-stu-id="2b846-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="2b846-128">Nauðsynlegt er að uppfæra einingarnar reglulega til að tryggja að gögnin séu uppfærð og nákvæm.</span><span class="sxs-lookup"><span data-stu-id="2b846-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="2b846-129">Til að uppfæra handvirkt tiltekna einingu skal fara í **Kerfisstjórnun \> Uppsetning \> Einingaverslun**, velja eininguna og því næst velja **Uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="2b846-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="2b846-130">Einnig er hægt að uppfæra gögnin sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="2b846-130">The data can also be updated automatically.</span></span> <span data-ttu-id="2b846-131">Á síðunni **Einingaverslun** skal stilla valkostinn **Virkja sjálfvirka uppfærslu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2b846-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="2b846-132">Hvaða útreikningsaðferð á að nota við útreikninga sjóðstreymisspár?</span><span class="sxs-lookup"><span data-stu-id="2b846-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="2b846-133">Útreikningsaðferð sjóðstreymisspár er með tvo mikilvæga valkosti.</span><span class="sxs-lookup"><span data-stu-id="2b846-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="2b846-134">Valkosturinn **Ný** reiknar sjóðstreymisspár fyrir ný skjöl og skjöl sem hafa breyst síðan síðasta runuvinnsla var keyrð.</span><span class="sxs-lookup"><span data-stu-id="2b846-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="2b846-135">Þessi valkostur keyrir oft hraðar því hann vinnur með minni undirmengi skjala.</span><span class="sxs-lookup"><span data-stu-id="2b846-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="2b846-136"> **Samtala** valkosturinn mun endurreikna sjóðstreymisspár fyrir hvert skjal í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="2b846-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="2b846-137">Þessi valkostur tekur lengri tíma vegna þess að það er meiri vinna sem þarf að ljúka.</span><span class="sxs-lookup"><span data-stu-id="2b846-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="2b846-138">Hvernig bæti ég afköst á endurtekinni runuvinnslu fyrir sjóðsstreymisspá?</span><span class="sxs-lookup"><span data-stu-id="2b846-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="2b846-139">Mælt er með því að sjóðstreymisspá sé keyrð á hverjum degi utan vinnutíma með því að nota **Nýja** útreikningsaðferð.</span><span class="sxs-lookup"><span data-stu-id="2b846-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="2b846-140">Mælt er með þessari nálgun sex daga vikunnar.</span><span class="sxs-lookup"><span data-stu-id="2b846-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="2b846-141">Svo skal keyra sjóðstreymisspá einu sinni í viku með því að nota **Samtals** útreikningsaðferðina á þeim degi sem minnst er að gera.</span><span class="sxs-lookup"><span data-stu-id="2b846-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


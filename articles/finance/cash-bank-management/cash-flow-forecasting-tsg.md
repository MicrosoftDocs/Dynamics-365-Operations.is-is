---
title: Úrræðaleit vegna uppsetningar sjóðstreymisspár
description: Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina sjóðstreymisspár. Þar er svarað algengum spurningum um uppsetningu sjóðstreymis, uppfærslur á sjóðstreymi og sjóðstreymi Power BI.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1cde9321259753bd0cacab3706c7f8455598ff3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232490"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="26167-104">Úrræðaleit vegna uppsetningar sjóðstreymisspár</span><span class="sxs-lookup"><span data-stu-id="26167-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26167-105">Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina sjóðstreymisspár.</span><span class="sxs-lookup"><span data-stu-id="26167-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="26167-106">Þar er svarað algengum spurningum um uppsetningu sjóðstreymis, uppfærslur á sjóðstreymi og sjóðstreymi Power BI.</span><span class="sxs-lookup"><span data-stu-id="26167-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="26167-107">Hvers vegna er sjóðstreymi sýnd fyrir aðeins einn lögaðila?</span><span class="sxs-lookup"><span data-stu-id="26167-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="26167-108">Sjóðstreymisspá er skilgreind og reiknuð fyrir hvern lögaðila fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="26167-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="26167-109">Power BI-skýrslur og möguleiki sjóðsstreymisspáa í Fjármálainnsýn sýna niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="26167-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="26167-110">Setja verður upp sjóðstreymisspá fyrir hvern lögaðila sem á að skoða spá fyrir.</span><span class="sxs-lookup"><span data-stu-id="26167-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="26167-111">Farið yfir skilgreiningu sjóðstreymisspár í öllum lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="26167-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="26167-112">Að öðrum kosti skal fara yfir skilgreiningu allra lögaðila fyrir sjóðstreymisspá og ganga úr skugga um að þær séu rétt stilltar.</span><span class="sxs-lookup"><span data-stu-id="26167-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="26167-113">Hvers vegna sýnir Power BI ekki öll sjóðstreymisgögnin?</span><span class="sxs-lookup"><span data-stu-id="26167-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="26167-114">Ljúka þarf nokkrum skrefum áður en sjóðstreymisspár geta birst í Power BI-yfirlitum.</span><span class="sxs-lookup"><span data-stu-id="26167-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="26167-115">Farið yfir eftirfarandi gátlista og gangið úr skugga um að öllum skrefum sé lokið:</span><span class="sxs-lookup"><span data-stu-id="26167-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="26167-116">Setjið upp sjóðstreymi fyrir hvern lögaðila.</span><span class="sxs-lookup"><span data-stu-id="26167-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="26167-117">Í færibreytum fjárhags skal stilla gjaldmiðil kerfisins og gerð gengisins.</span><span class="sxs-lookup"><span data-stu-id="26167-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="26167-118">Stillið fjárhagsbókhaldsgjaldmiðilinn og gerð gengisins.</span><span class="sxs-lookup"><span data-stu-id="26167-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="26167-119">Færið inn gengið milli færslugjaldmiðils og bókhaldsgjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="26167-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="26167-120">Færið inn gengið milli bókhaldsgjaldmiðils og kerfisgjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="26167-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="26167-121">Færið inn gengið milli bókhaldsgjaldmiðils og hvers bankagjaldmiðils fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="26167-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="26167-122">Hvers vegna virkaði sjóðstreymi Power BI í fyrri útgáfum en er nú autt?</span><span class="sxs-lookup"><span data-stu-id="26167-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="26167-123">Gangið úr skugga um að mælingarnar „Sjóðstreymismæling V2“ og „LedgerCovLiquidityMeasurement“ úr einingaverslun hafi verið skilgreindar.</span><span class="sxs-lookup"><span data-stu-id="26167-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="26167-124">Frekari upplýsingar um hvernig á að vinna með gögn í einingaverslun er að finna í [Power BI samþætting við einingaverslun](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Gangið úr skugga um að búið sé að fara í gegnum öll skrefin sem þarf að taka til að skoða Power BI-efni.</span><span class="sxs-lookup"><span data-stu-id="26167-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="26167-125">Frekari upplýsingar má finna á [Yfirlit yfir reiðufé Power BI efni](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="26167-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="26167-126">Hafa einingar einingaverslunar verið uppfærðar?</span><span class="sxs-lookup"><span data-stu-id="26167-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="26167-127">Nauðsynlegt er að uppfæra einingarnar reglulega til að tryggja að gögnin séu uppfærð og nákvæm.</span><span class="sxs-lookup"><span data-stu-id="26167-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="26167-128">Til að uppfæra handvirkt tiltekna einingu skal fara í **Kerfisstjórnun \> Uppsetning \> Einingaverslun**, velja eininguna og því næst velja **Uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="26167-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="26167-129">Einnig er hægt að uppfæra gögnin sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="26167-129">The data can also be updated automatically.</span></span> <span data-ttu-id="26167-130">Á síðunni **Einingaverslun** skal stilla valkostinn **Virkja sjálfvirka uppfærslu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="26167-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
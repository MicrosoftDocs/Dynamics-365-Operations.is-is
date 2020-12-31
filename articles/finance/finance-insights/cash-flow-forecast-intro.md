---
title: Sjóðstreymispá (forútgáfa)
description: Þetta efnisatriði lýsir eiginleika sjóðsstreymisspár.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645249"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="6672d-103">Sjóðstreymispá (forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="6672d-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6672d-104">Sjóðstreymi er nauðsynlegt fyrir öll fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="6672d-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="6672d-105">Jafnvel arðbær fyrirtæki geta staðið frammi fyrir gjaldþroti ef þau hafa ekki nægt sjóðstreymi.</span><span class="sxs-lookup"><span data-stu-id="6672d-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="6672d-106">Sjóðstreymisspáreiginleikinn í fjármálainnsýn getur auðveldað fyrirtækjum að fylgjast með og stjórna sjóðsstöðu með árangursríkum hætti.</span><span class="sxs-lookup"><span data-stu-id="6672d-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="6672d-107">Þessi eiginleiki notar vélnám til að hjálpa fyrirtækjum að spá fyrir um sjóðstreymi sem eru nákvæmari en þau hafa áður verið.</span><span class="sxs-lookup"><span data-stu-id="6672d-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="6672d-108">Það getur einnig hjálpað stjórnendum að taka ákvarðanir sem hámarka tækifæri eftir núverandi reiðufjárstöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="6672d-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="6672d-109">Í flestum fyrirtækjum er stjórnun sjóðstreymis og keyrsla sjóðstreymisspár leiðinlegt og endurtekningarsamt handvirkt ferli.</span><span class="sxs-lookup"><span data-stu-id="6672d-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="6672d-110">Flest fyrirtæki reiða sig á Microsoft Excel-lausnir sem eru með mismikið flækjustig.</span><span class="sxs-lookup"><span data-stu-id="6672d-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="6672d-111">Áskoranir um nákvæmar spár fyrir sjóðstreymi eru eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="6672d-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="6672d-112">Gögn eru ekki tiltæk fyrir ákvarðanatöku vegna þess að þau eru dreifð á mörgum stöðum, þar á meðal:</span><span class="sxs-lookup"><span data-stu-id="6672d-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="6672d-113">Áætlanakerfi fyrir bókhalds- eða fyrirtækistilfang</span><span class="sxs-lookup"><span data-stu-id="6672d-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="6672d-114">Hugbúnaður fjárhagsáætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="6672d-114">Financial planning software</span></span>
  - <span data-ttu-id="6672d-115">Excel</span><span class="sxs-lookup"><span data-stu-id="6672d-115">Excel</span></span>
  - <span data-ttu-id="6672d-116">Fleiri hugbúnaðarforrit</span><span class="sxs-lookup"><span data-stu-id="6672d-116">Additional software applications</span></span> 
- <span data-ttu-id="6672d-117">Spár byggjast á innri þekkingu sem staðsett er í sílóum innan hvers léns eða deildar.</span><span class="sxs-lookup"><span data-stu-id="6672d-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="6672d-118">Mæling á nákvæmni sjóðstreymisspár eftir að fjárhagstölur eru komnar óvisst og erfitt ferli.</span><span class="sxs-lookup"><span data-stu-id="6672d-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="6672d-119">Upplýsingar um getu sjóðstreymisspárinnar</span><span class="sxs-lookup"><span data-stu-id="6672d-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="6672d-120">Eiginleiki sjóðstreymisspár inniheldur eftirfarandi virkni.</span><span class="sxs-lookup"><span data-stu-id="6672d-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="6672d-121">Auðveldar samþættingu sjóðsstreymisgagna úr ytri kerfum í Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="6672d-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="6672d-122">Sjóðsstreymisspár geta einnig notað inn-útflutningsramma gagna.</span><span class="sxs-lookup"><span data-stu-id="6672d-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="6672d-123">Þessi rammi auðveldar samþættingu við Excel OData.</span><span class="sxs-lookup"><span data-stu-id="6672d-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="6672d-124">Einnig er hægt að sameina gögn af ólíkum uppruna til að stofna heildstæða sjóðsstreymislausn.</span><span class="sxs-lookup"><span data-stu-id="6672d-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="6672d-125">Kynnir til sögunnar snjalla reiðufjárstöðu.</span><span class="sxs-lookup"><span data-stu-id="6672d-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="6672d-126">Staða reiðufjár er stofnuð á grundvelli greiðsluhegðunar viðskiptavinar til að spá fyrir um hvenær fyrirtæki getur búist við því að fá greitt reiðufé á reikninga sína.</span><span class="sxs-lookup"><span data-stu-id="6672d-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="6672d-127">Þar er einnig hægt að greina söguleg mynstur greiðslna til lánardrottna til að spá fyrir um hvenær reikningar og pantanir eru líklegar til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="6672d-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="6672d-128">Kynnir hugvitsamlega sjóðsstreymisspá fyrir langtímaspá með því að nota tímaraðaspár í gegnum sjálfvirka samþættingu við AI Builder.</span><span class="sxs-lookup"><span data-stu-id="6672d-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="6672d-129">Býður upp á möguleikann á að vista tiltekna sjóðsstreymisstöðu eða spár, breyta þeim, bera þær saman og mæla frammistöðu spánna við rauntölur.</span><span class="sxs-lookup"><span data-stu-id="6672d-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="6672d-130">Virkjar hvað-ef-greiningu í gegnum samanburð skyndimynda.</span><span class="sxs-lookup"><span data-stu-id="6672d-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="6672d-131">Til dæmis er hægt að búa til margar skyndimyndir sem tákna bjartsýna, svartsýna og raunhæfa sýn á sjóðstreymi notanda og síðan bera saman og skoða mismuninn.</span><span class="sxs-lookup"><span data-stu-id="6672d-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="6672d-132">Býður upp á möguleika á því að skoða sjóðsstreymisspá í mörgum gjaldmiðlum, þvert á lögaðila, og sía og skoða sjóðstreymi sem tengist bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="6672d-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="6672d-133">Gerir notendum kleift að sía og skoða bankareikninga sem tengjast fjárhagsvíddum.</span><span class="sxs-lookup"><span data-stu-id="6672d-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="6672d-134">Sjóðstreymisspáin í Dynamics 365 Finance mun gera fyrirtækinu kleift að umbreyta leiðinlegri, flókinni, en endurtekningarsamri vörpun sjóðstreymis í einfalt, sjálfvirkt ferli.</span><span class="sxs-lookup"><span data-stu-id="6672d-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="6672d-135">Með því að gera leiðinlegustu þætti sjóðstreymisspár sjálfvirka er hægt að leggja áherslu á mikilvæga ákvörðunartöku til að ná æskilegri rekstrarniðurstöðu.</span><span class="sxs-lookup"><span data-stu-id="6672d-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="6672d-136">Setja upp vídd fyrir sjóðsstreymisspá</span><span class="sxs-lookup"><span data-stu-id="6672d-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="6672d-137">Nýr flipi á síðunni **Uppsetning sjóðstreymisspár** gerir notendum kleift að hafa stjórn á því hvaða fjárhagsvíddir eru notaðar fyrir síun í vinnusvæðinu **Sjóðsstreymisspá**.</span><span class="sxs-lookup"><span data-stu-id="6672d-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="6672d-138">Þessi flipi mun aðeins birtast þegar eiginleiki sjóðstreymisspár er virkur.</span><span class="sxs-lookup"><span data-stu-id="6672d-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="6672d-139">Á flipanum **Víddir** skal velja víddir af listanum sem á að nota fyrir síun og nota örvalyklana til að fara þá í dálkinn til hægri.</span><span class="sxs-lookup"><span data-stu-id="6672d-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="6672d-140">Aðeins er hægt að velja tvær víddir til að sía spárgögn sjóðstreymisspár.</span><span class="sxs-lookup"><span data-stu-id="6672d-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="6672d-141">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="6672d-141">Privacy notice</span></span>
<span data-ttu-id="6672d-142">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="6672d-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>

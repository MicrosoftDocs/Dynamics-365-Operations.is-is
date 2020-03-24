---
title: Yfirlit yfir tvöfalt skriftarverk
description: Þetta efni veitir yfirlit tvöföld skriftarverk. Tvöföld skriftarverk er grunngerð sem veitir nær rauntíma samskipti á milli Microsoft Dynamics 365 líkanaknúinna forrita og Finance and Operations forrita.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c4a643d4981364cea5b549118c201ac8a9798e02
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113875"
---
# <a name="dual-write-overview"></a><span data-ttu-id="3fbcc-104">Yfirlit yfir tvöfalt skriftarverk</span><span class="sxs-lookup"><span data-stu-id="3fbcc-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a><span data-ttu-id="3fbcc-105">Hvað er tvískipt skriftarverk?</span><span class="sxs-lookup"><span data-stu-id="3fbcc-105">What is dual-write?</span></span>

<span data-ttu-id="3fbcc-106">Tvöföld skriftarverk er tilbúin grunngerð sem veitir nær rauntíma samskipti á milli líkanaknúninna forrita í Microsoft Dynamics 365 og Finance and Operations forrita.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="3fbcc-107">Þegar gögn um viðskiptavini, afurðir, fólk og rekstur streyma út fyrir forritamörk, verðar allar deildir fyrirtækis öflugri.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="3fbcc-108">Tvöföld skriftarverk veitir þétt samtengingu, tvíátta samþættingu milli Finance and Operations forrita og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3fbcc-109">Allar gagnabreytingar í forritum Finance and Operations valda skrifum í Common Data Service og allar gagnabreytingar í Common Data Service valda skrifum í forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="3fbcc-110">Þetta sjálfvirka gagnaflæði veitir samþætta notendaupplifun í forritunum.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Gagnasamband milli forrita](media/dual-write-overview.jpg)

<span data-ttu-id="3fbcc-112">Tvíritun hefur tvo þætti: *Innviðaþátt* og *forritsþátt*.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="3fbcc-113">Grunnvirki</span><span class="sxs-lookup"><span data-stu-id="3fbcc-113">Infrastructure</span></span>

<span data-ttu-id="3fbcc-114">Innbyggingin með tvískiptum skrifum er teygjanleg og áreiðanleg og inniheldur eftirfarandi lykilatriði:</span><span class="sxs-lookup"><span data-stu-id="3fbcc-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="3fbcc-115">Samstillt og tvíátta gagnaflæði milli forrita</span><span class="sxs-lookup"><span data-stu-id="3fbcc-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="3fbcc-116">Samstilling, ásamt spilunar-, hlé- og tímaflakksstillingum til að styðja við kerfið í net- og ótengdum/ósamstilltum stillingum.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="3fbcc-117">Geta til að samstilla upphafsgögn milli forritanna</span><span class="sxs-lookup"><span data-stu-id="3fbcc-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="3fbcc-118">Samþjöppuð sýn á verkþátta- og villuskrár fyrir gagnastjórnendur</span><span class="sxs-lookup"><span data-stu-id="3fbcc-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="3fbcc-119">Geta til að stilla sérsniðnar viðvaranir og viðmiðunarmörk og gerast áskrifandi að tilkynningum</span><span class="sxs-lookup"><span data-stu-id="3fbcc-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="3fbcc-120">Leiðandi notendaviðmót (UI) fyrir síun og umbreytingu</span><span class="sxs-lookup"><span data-stu-id="3fbcc-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="3fbcc-121">Geta til að stilla og skoða ósjálfstæði og sambönd eininga</span><span class="sxs-lookup"><span data-stu-id="3fbcc-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="3fbcc-122">Stækkanleiki fyrir bæði staðlaðar og sérsniðnar einingar og kort</span><span class="sxs-lookup"><span data-stu-id="3fbcc-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="3fbcc-123">Áreiðanleg stjórnun á líftíma forrits</span><span class="sxs-lookup"><span data-stu-id="3fbcc-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="3fbcc-124">Tilbúin uppsetningarupplifun viðskiptavina fyrir nýja viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="3fbcc-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="3fbcc-125">Forrit</span><span class="sxs-lookup"><span data-stu-id="3fbcc-125">Application</span></span>

<span data-ttu-id="3fbcc-126">Tvöföld skriftarverk búa til vörpun á milli hugtaka í Finance and Operations forritum og hugtökum í líkanaknúnum forritum í Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="3fbcc-127">Þessi samþætting styður eftirfarandi atburðarásir:</span><span class="sxs-lookup"><span data-stu-id="3fbcc-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="3fbcc-128">Samþættur aðalviðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="3fbcc-128">Integrated customer master</span></span>
+ <span data-ttu-id="3fbcc-129">Aðgangur að vildarkortum viðskiptavina og verðlaunapunkta</span><span class="sxs-lookup"><span data-stu-id="3fbcc-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="3fbcc-130">Samræmd afurðarsniðmátaupplifun</span><span class="sxs-lookup"><span data-stu-id="3fbcc-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="3fbcc-131">Meðvitund um stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="3fbcc-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="3fbcc-132">Samþætt lánardrottinssniðmát</span><span class="sxs-lookup"><span data-stu-id="3fbcc-132">Integrated vendor master</span></span>
+ <span data-ttu-id="3fbcc-133">Aðgangur að fjárhags- og skattatilvísunargögnum</span><span class="sxs-lookup"><span data-stu-id="3fbcc-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="3fbcc-134">Reynsla verðvélar eftir þörfum</span><span class="sxs-lookup"><span data-stu-id="3fbcc-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="3fbcc-135">Samþætt reynsla viðfangs til sjóðstreymis</span><span class="sxs-lookup"><span data-stu-id="3fbcc-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="3fbcc-136">Geta til að þjóna bæði eigin eignum og eignum viðskiptavina í gegnum umboðsmenn svæðisins</span><span class="sxs-lookup"><span data-stu-id="3fbcc-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="3fbcc-137">Samþætt reynsla af öflun til að greiða</span><span class="sxs-lookup"><span data-stu-id="3fbcc-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="3fbcc-138">Innbyggt athæfi og athugasemdir fyrir gögn viðskiptavina og skjöl</span><span class="sxs-lookup"><span data-stu-id="3fbcc-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="3fbcc-139">Geta til að leita að tiltækum birgðum og smáatriðum</span><span class="sxs-lookup"><span data-stu-id="3fbcc-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="3fbcc-140">Verk til reiðfjár-upplifun</span><span class="sxs-lookup"><span data-stu-id="3fbcc-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="3fbcc-141">Geta til að takast á við mörg heimilisföng og hlutverk í gegnum aðilahugtakið</span><span class="sxs-lookup"><span data-stu-id="3fbcc-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="3fbcc-142">Stjórnun á einum stað fyrir notendur</span><span class="sxs-lookup"><span data-stu-id="3fbcc-142">Single source management for users</span></span>
+ <span data-ttu-id="3fbcc-143">Innbyggðar rásir fyrir smásölu og markaðssetningu</span><span class="sxs-lookup"><span data-stu-id="3fbcc-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="3fbcc-144">Sýnileiki í kynningum og afslætti</span><span class="sxs-lookup"><span data-stu-id="3fbcc-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="3fbcc-145">Biðja um þjónustu aðgerðir</span><span class="sxs-lookup"><span data-stu-id="3fbcc-145">Request-for-service functions</span></span>
+ <span data-ttu-id="3fbcc-146">Staumlínulagaðar þjónustuaðgerðir</span><span class="sxs-lookup"><span data-stu-id="3fbcc-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="3fbcc-147">Helstu ástæður til að nota tvískipt skrif</span><span class="sxs-lookup"><span data-stu-id="3fbcc-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="3fbcc-148">Tvöföld skrifa veitir samþættingu gagna í öllu forritum Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="3fbcc-149">Þessi öflugi rammi tengir umhverfi og gerir ólíkum viðskiptaforritum kleift að vinna saman.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="3fbcc-150">Hér eru helstu ástæður þess að þú ættir að nota tvískipt skrif:</span><span class="sxs-lookup"><span data-stu-id="3fbcc-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="3fbcc-151">Tvöföld skrifa veitir þétt samtengd, næstum rauntíma og tvíátta samþættingu milli forrita Finance and Operations og líkanadrifinna forrita í Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="3fbcc-152">Þessi samþætting gerir Microsoft Dynamics 365 að því eina sem þarf fyrir allar viðskiptalausnir þínar.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="3fbcc-153">Viðskiptavinir sem nota Dynamics 365 Finance og Dynamics 365 Supply Chain Management, en sem nota lausnir utan Microsoft fyrir stjórnun tengsla við viðskiptavini (CRM), fara í átt að Dynamics 365 fyrir tvískiptan stuðning.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="3fbcc-154">Gögn frá viðskiptavinum, vörum, rekstri, verkefnum og net hlutanna (IoT) renna sjálfkrafa til Common Data Service í gegnum tvískipt skrif.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="3fbcc-155">Þessi tenging er mjög gagnleg fyrir fyrirtæki sem hafa áhuga á Microsoft Power Platform stækkanir.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="3fbcc-156">Tvöfaldur-skrifa innviði fylgir meginreglunni um enga kóða/lágkóða.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="3fbcc-157">Lágmarks verkfræðiátak er krafist til að framlengja venjulegar varpanir frá töflu til töflu og fela í sér sérsniðnar varpanir.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="3fbcc-158">Tvöföld skriftarverk styðja bæði netstillingu og ótengda stillingu.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="3fbcc-159">Microsoft er eina fyrirtækið sem býður upp á stuðning við net- og ótengdar stillingar.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="3fbcc-160">Hvað þýðir tvískipt skrif fyrir notendur og arkitekta CRM vörur?</span><span class="sxs-lookup"><span data-stu-id="3fbcc-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="3fbcc-161">Tvöfaldur skrifa sjálfvirkt gagnaflæðið á milli Finance and Operations forrita og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3fbcc-162">Í framtíðarútgáfum verða hugtök í líkanaknúnum forritum í Dynamics 365 (til dæmis viðskiptavini, tengiliður, tilvitnun og röð) stiguð til viðskiptavina á miðjum markaði og efri miðju markaðarins.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="3fbcc-163">Í fyrstu útgáfunni er mest af sjálfvirkni meðhöndluð með tvískiptum lausnum.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="3fbcc-164">Í framtíðarútgáfum verða þessar lausnir hluti af Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="3fbcc-165">Með því að skilja væntanlegar breytingar á Common Data Service, þú getur sparað þér áreynslu til langs tíma.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="3fbcc-166">Hér eru sumar af mikilvægum breytingunum:</span><span class="sxs-lookup"><span data-stu-id="3fbcc-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="3fbcc-167">Common Data Service mun hafa ný hugtök, svo sem fyrirtæki og aðila.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="3fbcc-168">Þessi hugtök hafa áhrif á öll forrit sem eru byggð á Common Data Service, svo sem Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="3fbcc-169">Starfsemi og athugasemdir eru sameinaðar og stækkaðar til að styðja bæði C1 (notendur kerfisins) og C2 (viðskiptavini kerfisins).</span><span class="sxs-lookup"><span data-stu-id="3fbcc-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="3fbcc-170">Hér eru sumar af komandi breytingunum í Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="3fbcc-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="3fbcc-171">Tugagagnagerð kemur í stað peningagagnagerðarinnar.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="3fbcc-172">Dagvirkni mun styðja fyrri, nútíð og framtíðargögn á sama stað.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="3fbcc-173">Það verður meiri stuðningur við gjaldmiðil og gengi og **Gengi** forritunarviðmót forrita (API) verður endurskoðað.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="3fbcc-174">Stuðningur við umreiking eininga verður studdur.</span><span class="sxs-lookup"><span data-stu-id="3fbcc-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="3fbcc-175">Fyrir frekari upplýsingar um væntanlegar breytingar, sjá [Gögn í Common Data Service - áfangi 1 og 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span><span class="sxs-lookup"><span data-stu-id="3fbcc-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span></span>

---
title: Tvöföld skrif – yfirlit
description: Þetta efnisatriði inniheldur yfirlit yfir tvöfalda skráningu sem býður upp á svo gott sem rauntímasamskipti á milli viðskiptvinaforita og Finance and Operations forrita.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 76c2f07ac5c25eea576cbb69256e76fbef4d86ca
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754113"
---
# <a name="dual-write-overview"></a><span data-ttu-id="a6bda-103">Tvöföld skrif – yfirlit</span><span class="sxs-lookup"><span data-stu-id="a6bda-103">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="a6bda-104">Hvað er tvískipt skriftarverk?</span><span class="sxs-lookup"><span data-stu-id="a6bda-104">What is dual-write?</span></span>

<span data-ttu-id="a6bda-105">Tvöföld skrif er tilbúið tölvukerfi sem býður upp á samskipti í rauntíma á milli forrita viðskiptavina og Finance and Operations-forrita.</span><span class="sxs-lookup"><span data-stu-id="a6bda-105">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="a6bda-106">Þegar gögn um viðskiptavini, afurðir, fólk og rekstur streyma út fyrir forritamörk, verðar allar deildir fyrirtækis öflugri.</span><span class="sxs-lookup"><span data-stu-id="a6bda-106">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="a6bda-107">Tvöföld skriftarverk veitir þétt samtengingu, tvíátta samþættingu milli Finance and Operations forrita og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a6bda-107">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="a6bda-108">Allar gagnabreytingar í forritum Finance and Operations valda skrifum í Dataverse og allar gagnabreytingar í Dataverse valda skrifum í forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6bda-108">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="a6bda-109">Þetta sjálfvirka gagnaflæði veitir samþætta notendaupplifun í forritunum.</span><span class="sxs-lookup"><span data-stu-id="a6bda-109">This automated data flow provides an integrated user experience across the apps.</span></span>

![Gagnasamband milli forrita](media/dual-write-overview.jpg)

<span data-ttu-id="a6bda-111">Tvíritun hefur tvo þætti: *Innviðaþátt* og *forritsþátt*.</span><span class="sxs-lookup"><span data-stu-id="a6bda-111">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="a6bda-112">Grunnvirki</span><span class="sxs-lookup"><span data-stu-id="a6bda-112">Infrastructure</span></span>

<span data-ttu-id="a6bda-113">Innbyggingin með tvískiptum skrifum er teygjanleg og áreiðanleg og inniheldur eftirfarandi lykilatriði:</span><span class="sxs-lookup"><span data-stu-id="a6bda-113">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="a6bda-114">Samstillt og tvíátta gagnaflæði milli forrita</span><span class="sxs-lookup"><span data-stu-id="a6bda-114">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="a6bda-115">Samstilling, ásamt spilunar-, hlé- og tímaflakksstillingum til að styðja við kerfið í net- og ótengdum/ósamstilltum stillingum.</span><span class="sxs-lookup"><span data-stu-id="a6bda-115">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="a6bda-116">Geta til að samstilla upphafsgögn milli forritanna</span><span class="sxs-lookup"><span data-stu-id="a6bda-116">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="a6bda-117">Samsett yfirlit yfir verkþætti og villukladda fyrir gangastjórnendur</span><span class="sxs-lookup"><span data-stu-id="a6bda-117">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="a6bda-118">Geta til að stilla sérsniðnar viðvaranir og viðmiðunarmörk og gerast áskrifandi að tilkynningum</span><span class="sxs-lookup"><span data-stu-id="a6bda-118">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="a6bda-119">Leiðandi notendaviðmót (UI) fyrir síun og umbreytingu</span><span class="sxs-lookup"><span data-stu-id="a6bda-119">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="a6bda-120">Geta til að stilla og skoða töflutengsl og sambönd</span><span class="sxs-lookup"><span data-stu-id="a6bda-120">Ability to set and view table dependencies and relationships</span></span>
+ <span data-ttu-id="a6bda-121">Stækkunarhæfni fyrir bæði staðlaðar og sérsniðnar töflur og kort</span><span class="sxs-lookup"><span data-stu-id="a6bda-121">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="a6bda-122">Áreiðanleg stjórnun á líftíma forrits</span><span class="sxs-lookup"><span data-stu-id="a6bda-122">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="a6bda-123">Tilbúin uppsetningarupplifun viðskiptavina fyrir nýja viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="a6bda-123">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="a6bda-124">Forrit</span><span class="sxs-lookup"><span data-stu-id="a6bda-124">Application</span></span>

<span data-ttu-id="a6bda-125">Tvöföld skrif stofnar vörpun milli hugtaka í Finance and Operations-forritum og hugataka í forritum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="a6bda-125">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="a6bda-126">Þessi samþætting styður eftirfarandi atburðarásir:</span><span class="sxs-lookup"><span data-stu-id="a6bda-126">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="a6bda-127">Samþætt aðalsniðmát viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="a6bda-127">Integrated customer master</span></span>
+ <span data-ttu-id="a6bda-128">Aðgangur að vildarkortum viðskiptavina og verðlaunapunkta</span><span class="sxs-lookup"><span data-stu-id="a6bda-128">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="a6bda-129">Samræmd afurðarsniðmátaupplifun</span><span class="sxs-lookup"><span data-stu-id="a6bda-129">Unified product mastering experience</span></span>
+ <span data-ttu-id="a6bda-130">Meðvitund um stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="a6bda-130">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="a6bda-131">Samþætt lánardrottinssniðmát</span><span class="sxs-lookup"><span data-stu-id="a6bda-131">Integrated vendor master</span></span>
+ <span data-ttu-id="a6bda-132">Aðgangur að fjárhags- og skattatilvísunargögnum</span><span class="sxs-lookup"><span data-stu-id="a6bda-132">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="a6bda-133">Reynsla verðvélar eftir þörfum</span><span class="sxs-lookup"><span data-stu-id="a6bda-133">On-demand price engine experience</span></span>
+ <span data-ttu-id="a6bda-134">Samþætt reynsla viðfangs til sjóðstreymis</span><span class="sxs-lookup"><span data-stu-id="a6bda-134">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="a6bda-135">Geta til að þjóna bæði eigin eignum og eignum viðskiptavina í gegnum umboðsmenn svæðisins</span><span class="sxs-lookup"><span data-stu-id="a6bda-135">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="a6bda-136">Samþætt reynsla af öflun til að greiða</span><span class="sxs-lookup"><span data-stu-id="a6bda-136">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="a6bda-137">Innbyggt athæfi og athugasemdir fyrir gögn viðskiptavina og skjöl</span><span class="sxs-lookup"><span data-stu-id="a6bda-137">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="a6bda-138">Geta til að leita að tiltækum birgðum og smáatriðum</span><span class="sxs-lookup"><span data-stu-id="a6bda-138">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="a6bda-139">Verk til reiðfjár-upplifun</span><span class="sxs-lookup"><span data-stu-id="a6bda-139">Project-to-cash experience</span></span>
+ <span data-ttu-id="a6bda-140">Geta til að takast á við mörg heimilisföng og hlutverk í gegnum aðilahugtakið</span><span class="sxs-lookup"><span data-stu-id="a6bda-140">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="a6bda-141">Stjórnun á einum stað fyrir notendur</span><span class="sxs-lookup"><span data-stu-id="a6bda-141">Single source management for users</span></span>
+ <span data-ttu-id="a6bda-142">Innbyggðar rásir fyrir smásölu og markaðssetningu</span><span class="sxs-lookup"><span data-stu-id="a6bda-142">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="a6bda-143">Sýnileiki í kynningum og afslætti</span><span class="sxs-lookup"><span data-stu-id="a6bda-143">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="a6bda-144">Biðja um þjónustu aðgerðir</span><span class="sxs-lookup"><span data-stu-id="a6bda-144">Request-for-service functions</span></span>
+ <span data-ttu-id="a6bda-145">Staumlínulagaðar þjónustuaðgerðir</span><span class="sxs-lookup"><span data-stu-id="a6bda-145">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="a6bda-146">Helstu ástæður til að nota tvískipt skrif</span><span class="sxs-lookup"><span data-stu-id="a6bda-146">Top reasons to use dual-write</span></span>

<span data-ttu-id="a6bda-147">Tvöföld skrifa veitir samþættingu gagna í öllu forritum Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a6bda-147">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="a6bda-148">Þessi öflugi rammi tengir umhverfi og gerir ólíkum viðskiptaforritum kleift að vinna saman.</span><span class="sxs-lookup"><span data-stu-id="a6bda-148">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="a6bda-149">Hér eru helstu ástæður þess að þú ættir að nota tvískipt skrif:</span><span class="sxs-lookup"><span data-stu-id="a6bda-149">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="a6bda-150">Tvöföld skrifa veitir þétt samtengd, næstum rauntíma og tvíátta samþættingu milli forrita Finance and Operations og líkanadrifinna forrita í Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a6bda-150">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="a6bda-151">Þessi samþætting gerir Microsoft Dynamics 365 að því eina sem þarf fyrir allar viðskiptalausnir þínar.</span><span class="sxs-lookup"><span data-stu-id="a6bda-151">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="a6bda-152">Viðskiptavinir sem nota Dynamics 365 Finance og Dynamics 365 Supply Chain Management, en sem nota lausnir utan Microsoft fyrir stjórnun tengsla við viðskiptavini (CRM), fara í átt að Dynamics 365 fyrir tvískiptan stuðning.</span><span class="sxs-lookup"><span data-stu-id="a6bda-152">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="a6bda-153">Gögn frá viðskiptavinum, vörum, rekstri, verkefnum og net hlutanna (IoT) renna sjálfkrafa til Dataverse í gegnum tvískipt skrif.</span><span class="sxs-lookup"><span data-stu-id="a6bda-153">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="a6bda-154">Þessi tenging er gagnleg fyrir fyrirtæki sem hafa áhuga á Power Platform útvíkkun.</span><span class="sxs-lookup"><span data-stu-id="a6bda-154">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="a6bda-155">Tvöfaldur-skrifa innviði fylgir meginreglunni um enga kóða/lágkóða.</span><span class="sxs-lookup"><span data-stu-id="a6bda-155">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="a6bda-156">Lágmarks verkfræðiátak er krafist til að framlengja venjulegar varpanir frá töflu til töflu og fela í sér sérsniðnar varpanir.</span><span class="sxs-lookup"><span data-stu-id="a6bda-156">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="a6bda-157">Tvöföld skriftarverk styðja bæði netstillingu og ótengda stillingu.</span><span class="sxs-lookup"><span data-stu-id="a6bda-157">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="a6bda-158">Microsoft er eina fyrirtækið sem býður upp á stuðning við net- og ótengdar stillingar.</span><span class="sxs-lookup"><span data-stu-id="a6bda-158">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="a6bda-159">Hvað þýða tvöföld skrif fyrir þróunaraðila og hönnuði forrita viðskiptavina?</span><span class="sxs-lookup"><span data-stu-id="a6bda-159">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="a6bda-160">Tvöföld skrif gerir gagnaflæði á milli Finance and Operations forrita og forrit fyrir viðskiptavini sjálfvirk.</span><span class="sxs-lookup"><span data-stu-id="a6bda-160">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="a6bda-161">Tvöföld skrif samanstendur af tveimur AppSource lausnum sem eru settar upp á Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a6bda-161">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="a6bda-162">Lausnirnar víkka út töfluskema, viðbætur og verkflæði á Dataverse þannig að hægt sé að kvarða þær fyrir ERP-stærð.</span><span class="sxs-lookup"><span data-stu-id="a6bda-162">The solutions expand the table schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="a6bda-163">Fyrir árangursríka innleiðingu verða þróunaraðilar og hönnuðir forrita viðskiptavina að hafa skilning á þessum breytingum og vinna með viðkomandi í Finance and Operations-forritum.</span><span class="sxs-lookup"><span data-stu-id="a6bda-163">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="a6bda-164">Ef búa á til samstæðu með Finance and Operations-forritum gera tvöföld skrif nauðsynlegar breytingar í Dataverse-skemanu.</span><span class="sxs-lookup"><span data-stu-id="a6bda-164">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="a6bda-165">Ef ætlunin er að skilja áætlunina er hægt að koma í veg fyrir endurvinnslu tiltekinnar hönnunr og þróunar í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="a6bda-165">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="a6bda-166">Þegar AppSource pakkinn fyrir tvöföld skrif er uppsettur mun Dataverse innihald ný hugtök á borð við fyrirtæki og aðila.</span><span class="sxs-lookup"><span data-stu-id="a6bda-166">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="a6bda-167">Þessi hugtök aðstoða forrit sem byggja á Dataverse, þar á meðal Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service, að eiga samskipti við Finance and Operations-forrit.</span><span class="sxs-lookup"><span data-stu-id="a6bda-167">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="a6bda-168">Starfsemi og athugasemdir eru sameinaðar og stækkaðar til að styðja bæði C1 (notendur kerfisins) og C2 (viðskiptavini kerfisins).</span><span class="sxs-lookup"><span data-stu-id="a6bda-168">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="a6bda-169">Til að koma í veg fyrir gagnatap við flutning á milli Finance and Operations-forrita og Dataverse, er hægt að útvíkka fjölda aukastafa í gagnagerð gjaldmiðils fyrir forrit viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="a6bda-169">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="a6bda-170">Eiginleikinn þýðir sjálfkrafa fyrirliggjandi línur í nýja útvíkkaða stöðu á lýsigagnalagi.</span><span class="sxs-lookup"><span data-stu-id="a6bda-170">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="a6bda-171">Í þessu ferli er gjaldmiðilsgildið þýtt með tugagögnum, frekar en peningagögnum, og gjaldmiðilsgildið styður 10 aukastafi.</span><span class="sxs-lookup"><span data-stu-id="a6bda-171">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="a6bda-172">Velja þarf þennan eiginleiki er innskráður og fyrirtæki sem þurfa ekki meira en 4 aukastafi þurfa ekki að velja hann.</span><span class="sxs-lookup"><span data-stu-id="a6bda-172">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="a6bda-173">Nánari upplýsingar er að finna í [Flutningur gagnagerðar gjaldmiðils fyrir tvöföld skrif](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="a6bda-173">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="a6bda-174">[Dagsetningarvirkni](../../dev-tools/date-effectivity.md) verður bætt við Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a6bda-174">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="a6bda-175">Það styður gögn í fortíð, nútíð og framtíð í sömu töflu.</span><span class="sxs-lookup"><span data-stu-id="a6bda-175">It will support past, present, and future data on the same table.</span></span>

+ <span data-ttu-id="a6bda-176">[Umreikningur eininga](../../../../supply-chain/pim/tasks/manage-unit-measure.md) er studdur fyrir vörur, tilboð, pantanir og reikninga.</span><span class="sxs-lookup"><span data-stu-id="a6bda-176">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="a6bda-177">Frekari upplýsingar um breytingar á næstunni er að finna í [Nýjungar eða breytingar í tvöföldum skrifum](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="a6bda-177">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
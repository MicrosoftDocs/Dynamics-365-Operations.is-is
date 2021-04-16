---
title: Yfirlit skjalaprentunar
description: Hægt er að prenta skjöl með því að nota annaðhvort staðbundinn prentara eða nettengt tæki. Þessi grein gefur yfirlit yfir hvernig skjöl eru prentuð.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d41e299f0076e1016e8ddae8584bfec338a73a9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749394"
---
# <a name="document-printing-overview"></a><span data-ttu-id="a0d01-104">Yfirlit skjalaprentunar</span><span class="sxs-lookup"><span data-stu-id="a0d01-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0d01-105">Hægt er að prenta skjöl með því að nota annaðhvort staðbundinn prentara eða nettengt tæki.</span><span class="sxs-lookup"><span data-stu-id="a0d01-105">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="a0d01-106">Þessi grein gefur yfirlit yfir hvernig skjöl eru prentuð.</span><span class="sxs-lookup"><span data-stu-id="a0d01-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="a0d01-107">Yfirlit prentunar</span><span class="sxs-lookup"><span data-stu-id="a0d01-107">Printing overview</span></span>

<span data-ttu-id="a0d01-108">Forritið veitir samþættar þjónustur og biðlaraforrit sem auðvelda að búa til, geyma og dreifa skjölum sem styðja viðskiptastarfsemi.</span><span class="sxs-lookup"><span data-stu-id="a0d01-108">The application provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="a0d01-109">Hægt er að prenta skjöl með því að nota annaðhvort staðbundinn prentara eða nettengt tæki.</span><span class="sxs-lookup"><span data-stu-id="a0d01-109">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="a0d01-110">Að auki er hægt að flytja út síður og skýrslur beint frá viðskiptavini, sem PDF-skrár eða Microsoft Office skjöl.</span><span class="sxs-lookup"><span data-stu-id="a0d01-110">In addition, you can export pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="a0d01-111">Að lokum gerir úthlutað vinnuálag þér kleift að prenta viðskiptaskjöl beint úr fartæki með því að nota nettilföng.</span><span class="sxs-lookup"><span data-stu-id="a0d01-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="a0d01-112">Þótt prentskilyrði geta verið breytileg, þurfa allar atvinnugreinar yfirleitt að búa til afrit af viðskiptaskjölum með því að nota forritið.</span><span class="sxs-lookup"><span data-stu-id="a0d01-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using the application.</span></span> <span data-ttu-id="a0d01-113">Prentun skjala á nettækjum frá hýstum forritum hefur í för með sér einstakt sett af áskorunum.</span><span class="sxs-lookup"><span data-stu-id="a0d01-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="a0d01-114">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="a0d01-114">Here are some examples:</span></span>

- <span data-ttu-id="a0d01-115">Prentrekill er hugsanlega ekki tiltækur á tæki notanda.</span><span class="sxs-lookup"><span data-stu-id="a0d01-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="a0d01-116">Tæki notanda kann að vera ótengt fyrirtækjanetinu.</span><span class="sxs-lookup"><span data-stu-id="a0d01-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="a0d01-117">Með því að nota sérstakan hýsil og fylgja nokkrum einföldum skrefum getur kerfisstjóri stillt uppsetningar þannig að notendur geti prentað beint úr viðskiptaforritum á nettækjum.</span><span class="sxs-lookup"><span data-stu-id="a0d01-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="application-printing-scenarios"></a><span data-ttu-id="a0d01-118">Atburðarprentun atburðarása</span><span class="sxs-lookup"><span data-stu-id="a0d01-118">Application printing scenarios</span></span> 

<span data-ttu-id="a0d01-119">Eftirfarandi tafla lýsir þremur aðalprentmyndum.</span><span class="sxs-lookup"><span data-stu-id="a0d01-119">The following table describes the three primary printing scenarios.</span></span>

| <span data-ttu-id="a0d01-120">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="a0d01-120">Scenario</span></span>                        | <span data-ttu-id="a0d01-121">Markmið</span><span class="sxs-lookup"><span data-stu-id="a0d01-121">Goal</span></span>                                                      | <span data-ttu-id="a0d01-122">Lausn</span><span class="sxs-lookup"><span data-stu-id="a0d01-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="a0d01-123">1. Prenta það sem sést</span><span class="sxs-lookup"><span data-stu-id="a0d01-123">1. Printing what you see</span></span>        | <span data-ttu-id="a0d01-124">Prenta það sem er sýnt í vafranum.</span><span class="sxs-lookup"><span data-stu-id="a0d01-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="a0d01-125">„Prentvæn“ útgáfa af vefsíðu er búin til fyrir vafrann.</span><span class="sxs-lookup"><span data-stu-id="a0d01-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="a0d01-126">2. Gagnvirk prentun</span><span class="sxs-lookup"><span data-stu-id="a0d01-126">2. Interactive printing</span></span>         | <span data-ttu-id="a0d01-127">Prenta nákvæmnisskjal á staðbundnu tengdu tæki.</span><span class="sxs-lookup"><span data-stu-id="a0d01-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="a0d01-128">Hægt er að flytja út PDF-útgáfa af skýrslunni og hlaðið henni niður í vafrann.</span><span class="sxs-lookup"><span data-stu-id="a0d01-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="a0d01-129">3. Prenta á nettæki</span><span class="sxs-lookup"><span data-stu-id="a0d01-129">3. Printing on a network device</span></span> | <span data-ttu-id="a0d01-130">Senda nákvæmnisskjal á lén prenttækis.</span><span class="sxs-lookup"><span data-stu-id="a0d01-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="a0d01-131">Nákvæmnisskjal er sent á biðlaraforrit sem keyrir á þjóni sem er hýstur á léni viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="a0d01-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="a0d01-132">Vegna þess að lausnin er breytileg, er háð aðstæðum, veita forrit innbyggðar þjónustur og verkfæri til að hjálpa notendum að ná markmiðum sínum:</span><span class="sxs-lookup"><span data-stu-id="a0d01-132">Because the solution varies, depending on the scenario, applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="a0d01-133">**Aðstæður 1** er studd af myndþýðingu vafrans á HTML5-biðlara.</span><span class="sxs-lookup"><span data-stu-id="a0d01-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="a0d01-134">**Aðstæður 2** notar biðlaraforrit og þjónustu Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a0d01-134">**Scenario 2** uses client applications and Microsoft 365 services.</span></span>
- <span data-ttu-id="a0d01-135">**Aðstæður 3** krefst stuðnings frá biðlaraforritum og þjónustum sem eru hýstar í Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d01-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="a0d01-136">Til viðbótar við verkvanginn sem er notaður á Azure-áskriftina, veita Finance and Operations forrit viðskiptavinum samþætt Azure-forrit frá fyrsta aðila sem auðveldar þeim að nota á lénhýst tæki til að prenta skjöl.</span><span class="sxs-lookup"><span data-stu-id="a0d01-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="a0d01-137">Þjónustuyfirlit</span><span class="sxs-lookup"><span data-stu-id="a0d01-137">Service overview</span></span>
<span data-ttu-id="a0d01-138">Á meðan skjöl sem eru búin til af hýstum forritum bíða eftir að vera prentuð á nettengdu tæki, eru þau geymd í Azure blob-geymslu.</span><span class="sxs-lookup"><span data-stu-id="a0d01-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="a0d01-139">[Setja upp eftirlitsbúnað skjalasendingar til að virkja nettengda prentun](install-document-routing-agent.md) notar Azure sannvottun til að koma á öruggri rás til Azure-þjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="a0d01-139">The [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="a0d01-140">**Framkvæmdaröð**</span><span class="sxs-lookup"><span data-stu-id="a0d01-140">**Execution sequence**</span></span>

1. <span data-ttu-id="a0d01-141">Skýrslan er búin til af Microsoft SQL Server Reporting Services (SSRS) og er geymd í Azure blob-geymslu.</span><span class="sxs-lookup"><span data-stu-id="a0d01-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="a0d01-142">Viðhengdar prentarastillingar eru geymdar með skjalinu.</span><span class="sxs-lookup"><span data-stu-id="a0d01-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="a0d01-143">Leiðarmiðlari skjals spyr brautarröð Azure Service um virk verk.</span><span class="sxs-lookup"><span data-stu-id="a0d01-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="a0d01-144">Skjalinu er hlaðið niður með Leiðarmiðlara skjals og spólað á netprentarann.</span><span class="sxs-lookup"><span data-stu-id="a0d01-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="a0d01-145">Biðlaramiðuð lausnin leyfir viðskiptavinum að stjórna umfangi prentþarfa.</span><span class="sxs-lookup"><span data-stu-id="a0d01-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="a0d01-146">Viðskiptavinir sem eru með mikið magn til prentunar geta sett upp marga Leiðarmiðlara skjals til að auka fjölda samhliða prentaðgerða.</span><span class="sxs-lookup"><span data-stu-id="a0d01-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="a0d01-147">Að öðrum kosti þurfa sumir viðskiptavinir mjög fáar uppsetningar á Leiðarmiðlara skjals til að takast á við væntanlegar prentþarfir.</span><span class="sxs-lookup"><span data-stu-id="a0d01-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="a0d01-148">Þjónustuíhlutir fyrir netprentun</span><span class="sxs-lookup"><span data-stu-id="a0d01-148">Service components for network printing</span></span>

<span data-ttu-id="a0d01-149">Eftirfarandi skýringarmynd sýnir grunníhluti sem hjálpa til við að styðja netprentunaraðgerðir.</span><span class="sxs-lookup"><span data-stu-id="a0d01-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="a0d01-150">[![þjónustu-hlutar-fyrir-net-prentun\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="a0d01-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="a0d01-151">Athugaðu að hægt er að skrá einn prentara með mörgum miðlum skjalasendingar.</span><span class="sxs-lookup"><span data-stu-id="a0d01-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="a0d01-152">Til að leysa kjörstillingar prentara notar hýst þjónusta netslóðina sem ber kennsl á hvern prentara fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="a0d01-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="a0d01-153">Þar af leiðandi, jafnvel þegar prentari er skráður af mörgum biðlurum, birtist hann sem eitt val á lista yfir prentara sem eru í boði í forritunum.</span><span class="sxs-lookup"><span data-stu-id="a0d01-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in applications.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
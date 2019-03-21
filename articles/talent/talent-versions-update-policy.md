---
title: Kerfiskröfur og uppfærsluregla Talent
description: Þetta efnisatriði inniheldur lista yfir kröfur Dynamics 365 for Talent. Þar er uppfærslustefnuna einnig að finna.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 64362ae9e4ebb63ca6da2cd2f41376d1d9047694
ms.sourcegitcommit: c6af2de37309b574dcb69c9caad436b55136600f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/26/2019
ms.locfileid: "768486"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="342ac-104">Kerfiskröfur og uppfærsluregla Talent</span><span class="sxs-lookup"><span data-stu-id="342ac-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="342ac-105">Þetta efnisatriði inniheldur lista yfir kröfur Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="342ac-105">This topic lists requirements for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="342ac-106">Þar er uppfærslustefnuna einnig að finna.</span><span class="sxs-lookup"><span data-stu-id="342ac-106">The update policy is outlined, as well.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="342ac-107">Studdir vafrar</span><span class="sxs-lookup"><span data-stu-id="342ac-107">Supported web browsers</span></span>

<span data-ttu-id="342ac-108">Microsoft Dynamics 365 for Talent vefforrit er hægt að keyra í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:</span><span class="sxs-lookup"><span data-stu-id="342ac-108">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="342ac-109">Microsoft Edge (nýjasta almenna útgáfa) á Windows-10</span><span class="sxs-lookup"><span data-stu-id="342ac-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="342ac-110">Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7</span><span class="sxs-lookup"><span data-stu-id="342ac-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="342ac-111">Google Chrome (síðasta almenna útgáfan)</span><span class="sxs-lookup"><span data-stu-id="342ac-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="342ac-112">Apple Safari (síðasta almenna útgáfan)</span><span class="sxs-lookup"><span data-stu-id="342ac-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="342ac-113">Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra.</span><span class="sxs-lookup"><span data-stu-id="342ac-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="342ac-114">Til að sækja myndir sem eru myndaðar úr Verkskráningu og hafa þær með í Microsoft Word-skjöl, verður að hafa viðauka við Króm uppsett.</span><span class="sxs-lookup"><span data-stu-id="342ac-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="342ac-115">Verkflæðisritillinn er ræstur sem ClickOnce-forrit.</span><span class="sxs-lookup"><span data-stu-id="342ac-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="342ac-116">Aðeins Microsoft Edge og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce-forrit.</span><span class="sxs-lookup"><span data-stu-id="342ac-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="342ac-117">Verkflæðisritlinum ClickOnce hugbúnaðurinn krefst á 64-bita samhæfar stýrikerfi.</span><span class="sxs-lookup"><span data-stu-id="342ac-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="342ac-118">Til að forskoða PDF-skrár er mælt með því að notaðir séu nýjustu vafrarnir eins og Microsoft Edge (nýjasta tiltæka útgáfa fyrir almenning) Windows 10 eða Google Chorme (nýjasta tiltæka útgáfa fyrir almenning) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölvu.</span><span class="sxs-lookup"><span data-stu-id="342ac-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="342ac-119">Netþarfir</span><span class="sxs-lookup"><span data-stu-id="342ac-119">Network requirements</span></span>
> * <span data-ttu-id="342ac-120">Dynamics 365 for Talent er hannað fyrir net með biðtíma minni en 250-300 millisekúndum (ms.).</span><span class="sxs-lookup"><span data-stu-id="342ac-120">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="342ac-121">Þetta er biðtíma vafra biðlara Microsoft Azure gagnamiðstöðvar sem hýsir Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="342ac-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="342ac-122">Mælt er með því að prófa biðtíma á netinu á [www.azurespeed.com](https://www.azurespeed.com "Azure biðtímapróf").</span><span class="sxs-lookup"><span data-stu-id="342ac-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="342ac-123">Bandvíddarþarfir fyrir Dynamics 365 for Talent fara eftir aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="342ac-123">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="342ac-124">Flestar dæmigerðar aðstæður krefjast bandvíddar yfir meira en 50 kílóbætum á sekúndu (KBps).</span><span class="sxs-lookup"><span data-stu-id="342ac-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="342ac-125">Ekki skal reikna bandvíddarkröfur úr biðlarastaðsetningu með því að margfalda fjölda notenda með lágmarks bandvíddarkröfum.</span><span class="sxs-lookup"><span data-stu-id="342ac-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="342ac-126">Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út.</span><span class="sxs-lookup"><span data-stu-id="342ac-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="342ac-127">Nota sýnisútgáfa af Dynamics 365 for Talent fyrir viðskiptavini sem hafa áhyggjur af bandvíddaþörf.</span><span class="sxs-lookup"><span data-stu-id="342ac-127">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="342ac-128">Studd Microsoft Office forrit</span><span class="sxs-lookup"><span data-stu-id="342ac-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="342ac-129">Til að keyra Microsoft Excel og Word innbætur verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett.</span><span class="sxs-lookup"><span data-stu-id="342ac-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="342ac-130">Frekari upplýsingar um kröfur útgáfu er hægt að finna á [Úrræðaleit Office samþættingar](../dev-itpro/office-integration/office-integration-troubleshooting.md "Úrræðaleit Office samþættingar").</span><span class="sxs-lookup"><span data-stu-id="342ac-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="342ac-131">Til að skoða skjöl sem eru mynduð af virkninni Flytja inn í Excel eða Flytja inn í Word verður að hafa Microsoft Office 2007 eða nýrri útgáfu uppsetta.</span><span class="sxs-lookup"><span data-stu-id="342ac-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="update-policy"></a><span data-ttu-id="342ac-132">Uppfæra stefnu</span><span class="sxs-lookup"><span data-stu-id="342ac-132">Update policy</span></span>

<span data-ttu-id="342ac-133">Microsoft Dynamics 365 for Talent er þjónustað sem ský vara.</span><span class="sxs-lookup"><span data-stu-id="342ac-133">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="342ac-134">Uppfærslur fyrir Dynamics 365 for Talent eru samfelldar og settar inn sjálfvirkt af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="342ac-134">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="342ac-135">Uppfærslur eru gefnar út með reglubundnum hætti, uppfærslur eru gerðar fyrir allt umhverfi.</span><span class="sxs-lookup"><span data-stu-id="342ac-135">Updates are released on a regular cadence, updates will be made to all environments.</span></span>  <span data-ttu-id="342ac-136">Dynamics 365 for Talent er stutt samkvæmt [Microsoft Support Lifecycle policy](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle") sem býður upp á stöðugar og einfaldar leiðbeiningar fyrir tiltækileika stuðnings við vöru.</span><span class="sxs-lookup"><span data-stu-id="342ac-136">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>

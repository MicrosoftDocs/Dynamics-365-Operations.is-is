---
title: Kerfiskröfur
description: Þessi grein lýsir kröfum fyrir Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e7d7389c1bcf0f6024464e37b36d39efae5b832
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112938"
---
# <a name="system-requirements"></a><span data-ttu-id="843e1-103">Kerfiskröfur</span><span class="sxs-lookup"><span data-stu-id="843e1-103">System requirements</span></span>

<span data-ttu-id="843e1-104">Þessi grein lýsir kröfum fyrir Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="843e1-104">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="843e1-105">Það gefur líka upp löndin og svæðin þar sem Human Resources er tiltækt og upplýsingar um tungumál og staðfæringar fyrir gögn Human Resources.</span><span class="sxs-lookup"><span data-stu-id="843e1-105">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="843e1-106">Studdir vafrar</span><span class="sxs-lookup"><span data-stu-id="843e1-106">Supported web browsers</span></span>

<span data-ttu-id="843e1-107">Human Resources er hægt að keyra í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:</span><span class="sxs-lookup"><span data-stu-id="843e1-107">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="843e1-108">Microsoft Edge (nýjasta almenna útgáfa) á Windows-10</span><span class="sxs-lookup"><span data-stu-id="843e1-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="843e1-109">Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7</span><span class="sxs-lookup"><span data-stu-id="843e1-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="843e1-110">Google Chrome (síðasta almenna útgáfan)</span><span class="sxs-lookup"><span data-stu-id="843e1-110">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="843e1-111">Apple Safari (síðasta almenna útgáfan)</span><span class="sxs-lookup"><span data-stu-id="843e1-111">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="843e1-112">Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra.</span><span class="sxs-lookup"><span data-stu-id="843e1-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="843e1-113">Til að sækja myndir sem eru myndaðar úr Verkskráningu og hafa þær með í Microsoft Word-skjöl, verður að hafa viðauka við Króm uppsett.</span><span class="sxs-lookup"><span data-stu-id="843e1-113">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="843e1-114">Verkflæðisritillinn er ræstur sem ClickOnce-forrit.</span><span class="sxs-lookup"><span data-stu-id="843e1-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="843e1-115">Aðeins Microsoft Edge og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce-forrit.</span><span class="sxs-lookup"><span data-stu-id="843e1-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="843e1-116">Verkflæðisritlinum ClickOnce hugbúnaðurinn krefst á 64-bita samhæfar stýrikerfi.</span><span class="sxs-lookup"><span data-stu-id="843e1-116">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="843e1-117">Til að forskoða PDF-skrár er mælt með því að notaðir séu nýjustu vafrarnir eins og Microsoft Edge (nýjasta tiltæka útgáfa fyrir almenning) Windows 10 eða Google Chorme (nýjasta tiltæka útgáfa fyrir almenning) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölvu.</span><span class="sxs-lookup"><span data-stu-id="843e1-117">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="843e1-118">Netþarfir</span><span class="sxs-lookup"><span data-stu-id="843e1-118">Network requirements</span></span>
> * <span data-ttu-id="843e1-119">Human Resources er hannað fyrir net með biðtíma minni en 250-300 millisekúndum (ms.).</span><span class="sxs-lookup"><span data-stu-id="843e1-119">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="843e1-120">Þetta er biðtíma vafra biðlara Microsoft Azure gagnamiðstöðvar sem hýsir Human Resources.</span><span class="sxs-lookup"><span data-stu-id="843e1-120">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="843e1-121">Mælt er með er prófað biðtíma á netinu á [www.azurespeed.com](https://www.azurespeed.com "Azure biðtímapróf").</span><span class="sxs-lookup"><span data-stu-id="843e1-121">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="843e1-122">Bandvíddarþarfir fyrir Human Resources fara eftir aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="843e1-122">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="843e1-123">Flestar dæmigerðar aðstæður krefjast bandvíddar yfir meira en 50 kílóbætum á sekúndu (KBps).</span><span class="sxs-lookup"><span data-stu-id="843e1-123">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="843e1-124">Ekki skal reikna bandvíddarkröfur úr biðlarastaðsetningu með því að margfalda fjölda notenda með lágmarks bandvíddarkröfum.</span><span class="sxs-lookup"><span data-stu-id="843e1-124">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="843e1-125">Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út.</span><span class="sxs-lookup"><span data-stu-id="843e1-125">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="843e1-126">Nota sýnisútgáfa af Human Resources fyrir viðskiptavini sem hafa áhyggjur af bandvíddaþörf.</span><span class="sxs-lookup"><span data-stu-id="843e1-126">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="843e1-127">Studd Microsoft Office forrit</span><span class="sxs-lookup"><span data-stu-id="843e1-127">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="843e1-128">Til að keyra Microsoft Excel og Word innbætur verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett.</span><span class="sxs-lookup"><span data-stu-id="843e1-128">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="843e1-129">Sjá frekari upplýsingar um þarfir útgáfu í [Úrrætðaleit samþættingar á Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Úrræðaleit fyrir Office-samþættingu").</span><span class="sxs-lookup"><span data-stu-id="843e1-129">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="843e1-130">Til að skoða skjöl sem eru mynduð af virkninni Flytja inn í Excel eða Flytja inn í Word verður að hafa Microsoft Office 2007 eða nýrri útgáfu uppsetta.</span><span class="sxs-lookup"><span data-stu-id="843e1-130">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="843e1-131">Svæði í boði, tungumál og staðfærsla</span><span class="sxs-lookup"><span data-stu-id="843e1-131">Regional availability, languages, and localization</span></span>

<span data-ttu-id="843e1-132">Hægt er að hlaða niður PDF skrá yfir lönd, svæði og tungumál sem Human Resources styður á [Alþjóðlegt framboð á Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="843e1-132">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="843e1-133">Á meðan notandaviðmót er staðfært á önnur tungumál eru öll gögn notanda geymd á því tungumáli sem þau voru færð inn á.</span><span class="sxs-lookup"><span data-stu-id="843e1-133">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="843e1-134">Hægt er að búa til tölvupósta og sniðmát á öðrum tungumálum, en gögn á borð við upplýsingar um áætlanagerð eru einungis í boði á ensku sem stendur.</span><span class="sxs-lookup"><span data-stu-id="843e1-134">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="843e1-135">Ef þú ert þróunaraðili og hefur áhuga á að búa til lands- eða svæðisbundnar sérstillingar, eða að finna lausnir fyrir land eða svæði sem Microsoft styður ekki sem stendur skaltu skoða [Alþjóðavæðing](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="843e1-135">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

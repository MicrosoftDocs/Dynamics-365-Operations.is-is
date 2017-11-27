---
title: "Kerfiskröfur fyrir uppsetningu í skýi"
description: "Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, fyrir uppsetningar skýs."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="8c50f-103">Kerfiskröfur fyrir uppsetningu í skýi</span><span class="sxs-lookup"><span data-stu-id="8c50f-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8c50f-104">Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, fyrir uppsetningar skýs.</span><span class="sxs-lookup"><span data-stu-id="8c50f-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="8c50f-105">Áður en Finance and Operations er sett upp skal, þegar viðeigandi, tryggja að kerfið sem verið er að vinna með uppfylli eða fari fram úr lágmarks kröfum um net, vél- og hugbúnað.</span><span class="sxs-lookup"><span data-stu-id="8c50f-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="8c50f-106">Studdir vafrar</span><span class="sxs-lookup"><span data-stu-id="8c50f-106">Supported web browsers</span></span>
<span data-ttu-id="8c50f-107">Vefforritið getur keyrt í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:</span><span class="sxs-lookup"><span data-stu-id="8c50f-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="8c50f-108">Microsoft Edge (nýjasta almenna útgáfa) á Windows-10</span><span class="sxs-lookup"><span data-stu-id="8c50f-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="8c50f-109">Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c50f-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="8c50f-110">Google Chrome (nýjasta almenna útgáfa) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölva</span><span class="sxs-lookup"><span data-stu-id="8c50f-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="8c50f-111">Apple Safari (nýjasta almenna útgáfa) á Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eða Apple iPad</span><span class="sxs-lookup"><span data-stu-id="8c50f-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="8c50f-112">Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra.</span><span class="sxs-lookup"><span data-stu-id="8c50f-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="8c50f-113">Þú verður að setja upp prufuútgáfu af Chrome viðauka til að virkja Verkskráningu til að sækja skjámyndir og hafa þær með í Microsoft Word skjölum sem eru búin til.</span><span class="sxs-lookup"><span data-stu-id="8c50f-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="8c50f-114">Verkflæðisritillinn er ræstur sem ClickOnce-forrit.</span><span class="sxs-lookup"><span data-stu-id="8c50f-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="8c50f-115">Aðeins Edge Microsoft og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce forrit.</span><span class="sxs-lookup"><span data-stu-id="8c50f-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="8c50f-116">Verkflæðisritillinn í ClickOnce-hugbúnaðurinn krefst á 64-bita samhæfðs stýrikerfis.</span><span class="sxs-lookup"><span data-stu-id="8c50f-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="8c50f-117">Hönnunarviðmót fyrir fjárhagsskýrslugerð er ræst sem ClickOnce forritsins.</span><span class="sxs-lookup"><span data-stu-id="8c50f-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="8c50f-118">Það krefst á 64-bita samhæfðs stýrikerfis.</span><span class="sxs-lookup"><span data-stu-id="8c50f-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="8c50f-119">Ef verið er að nota Chrome, verður að setja upp ClickOnce viðauka til að sækja skýrslu hönnuður biðlara.</span><span class="sxs-lookup"><span data-stu-id="8c50f-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="8c50f-120">Ef verið er að nota Chrome með nafnlausum afhendingarmáta, skal ganga úr skugga um að ClickOnce viðaukanum verður einnig virkur fyrir nafnlausan ham.</span><span class="sxs-lookup"><span data-stu-id="8c50f-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="8c50f-121">Til að forskoða PDF-skrár er mælt með því að notaðir séu vafrar eins og Microsoft Edge (nýjasta tiltæka útgáfa fyrir almenning) Windows 10 eða Google Chorme (nýjasta tiltæka útgáfa fyrir almenning) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölvu.</span><span class="sxs-lookup"><span data-stu-id="8c50f-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="8c50f-122">Studdir vafrar fyrir sölustað smásöluskýs</span><span class="sxs-lookup"><span data-stu-id="8c50f-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="8c50f-123">Retail Cloud POS getur keyrt í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:</span><span class="sxs-lookup"><span data-stu-id="8c50f-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="8c50f-124">Microsoft Edge (nýjasta almenna útgáfa) á Windows-10</span><span class="sxs-lookup"><span data-stu-id="8c50f-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="8c50f-125">Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c50f-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="8c50f-126">Chrome (síðustu almennu útgáfu) á Windows 10, Windows 8.1 eða Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c50f-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="8c50f-127">Netþarfir</span><span class="sxs-lookup"><span data-stu-id="8c50f-127">Network requirements</span></span>
-   <span data-ttu-id="8c50f-128">Finance and Operations er hannað fyrir net með biðtíma upp á 250–300 millisekúndum (ms.) eða minna.</span><span class="sxs-lookup"><span data-stu-id="8c50f-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="8c50f-129">Þetta er biðtími frá vafra biðlara til Microsoft Azure gagnamiðstöðvar sem hýsir Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c50f-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="8c50f-130">Mælt er með er prófað biðtíma á netinu á <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="8c50f-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="8c50f-131">Bandvíddarkröfur fyrir Finance and Operations fara eftir aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="8c50f-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="8c50f-132">Flestar dæmigerðar aðstæður krefjast bandvíddar yfir meira en 50 kílóbætum á sekúndu (KBps).</span><span class="sxs-lookup"><span data-stu-id="8c50f-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="8c50f-133">Hins vegar fyrir aðstæður sem hafa miklar farmþarfir, eins og aðstæður sem fela í sér vinnusvæði eða yfirgripsmikil sérsnið, er mælt með fleiri bandvíddum.</span><span class="sxs-lookup"><span data-stu-id="8c50f-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="8c50f-134">Almennt séð, er Finance and Operations bestuð fyrir Internetið.</span><span class="sxs-lookup"><span data-stu-id="8c50f-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="8c50f-135">Fjöldi ferða fram og til baka frá biðlara vafra til Azure gagnamiðstöð er mjög lítill og allt farmur þjöppuð.</span><span class="sxs-lookup"><span data-stu-id="8c50f-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="8c50f-136">Ekki reikna þarfir bandvídd frá staðsetningu biðlara með því að margfalda notendur eftir þörfum lágmarksbandvíddar.</span><span class="sxs-lookup"><span data-stu-id="8c50f-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="8c50f-137">Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út.</span><span class="sxs-lookup"><span data-stu-id="8c50f-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="8c50f-138">Viðskiptavinir sem hafa áhyggjur af bandvíddaþörf ættu að nota sýnisútgáfa af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c50f-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="8c50f-139">.NET Framework þarfir</span><span class="sxs-lookup"><span data-stu-id="8c50f-139">.NET Framework requirements</span></span>
<span data-ttu-id="8c50f-140">Finance and Operations krefst Microsoft .NET Framework útgáfu 4.6.2 fyrir öll ClickOnce forrit, eins og leiðarmiðlara skjals.</span><span class="sxs-lookup"><span data-stu-id="8c50f-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="8c50f-141">Sjá leiðbeiningar með uppsetningu, [Uppsetningu .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="8c50f-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="8c50f-142">Studd forrit Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="8c50f-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="8c50f-143">Eftirfarandi forrit Microsoft Office eru studd í skýi og innanhúsnýtingu Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="8c50f-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="8c50f-144">Til að nota Office-innbætur fyrir Microsoft Excel og Word verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett.</span><span class="sxs-lookup"><span data-stu-id="8c50f-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="8c50f-145">Sjá frekari upplýsingar um þarfir útgáfu [Office samþættingu úrræðaleit](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="8c50f-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="8c50f-146">Til að skoða skjöl sem eru myndaðar Út í Excel- eða Útflutnings í Word virkni, sem verður að hafa Microsoft Office 2007 eða sett upp síðar.</span><span class="sxs-lookup"><span data-stu-id="8c50f-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="8c50f-147">Þarfir Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="8c50f-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="8c50f-148">Ef Modern POS Smásala mun nota ótengdan gagnagrunn, verður tölvan að uppfylla öll kerfisskilyrði fyrir Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8c50f-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="8c50f-149">Gagnagrunnur fyrir Retail Modern POS mun virka á Microsoft SQL Server 2012 með Þjónustupakka 3 eða nýrri, Microsoft SQL Server 2014 með Þjónustupakka 2 eða nýrri, og Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8c50f-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="8c50f-150">Við mælum með því að þú notir ávalt nýjustu fáanlegu útgáfu og að þú setjir upp alla nýjustu þjónustupakkana.</span><span class="sxs-lookup"><span data-stu-id="8c50f-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="8c50f-151">Studd stýrikerfi</span><span class="sxs-lookup"><span data-stu-id="8c50f-151">Supported operating systems</span></span>

-   <span data-ttu-id="8c50f-152">Retail Modern POS er 32-bita hugbúnaður en hún mun keyra á x86 og x64 hönnun.</span><span class="sxs-lookup"><span data-stu-id="8c50f-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="8c50f-153">Retail Modern POS er aðeins studd í útgáfum Windows 10 Pro, Enterprise og Enterprise Long Term Servicing Branch (LTSB).</span><span class="sxs-lookup"><span data-stu-id="8c50f-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="8c50f-154">Lágmarksþörf kerfis</span><span class="sxs-lookup"><span data-stu-id="8c50f-154">Minimum system requirements</span></span>

-   <span data-ttu-id="8c50f-155">Lágmarks studd lausn er 1280 × 1024.</span><span class="sxs-lookup"><span data-stu-id="8c50f-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="8c50f-156">Í tölvu sem keyrir Retail Modern POS á verður að uppfylla þær þarfir:</span><span class="sxs-lookup"><span data-stu-id="8c50f-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="8c50f-157">Það verður að hafa, lágmarki tvískiptur kjarnauppsetning gjörva sem keyrir á minna en 2 gigahertz (GHz).</span><span class="sxs-lookup"><span data-stu-id="8c50f-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="8c50f-158">Hún verður að hafa, að lágmarki, 3 gígabæt (GB) af RAM.</span><span class="sxs-lookup"><span data-stu-id="8c50f-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="8c50f-159">Hún verður að hafa aðgang á Internetinu.</span><span class="sxs-lookup"><span data-stu-id="8c50f-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="8c50f-160">Kjarnapakki fyrir Retail Hardware Station.</span><span class="sxs-lookup"><span data-stu-id="8c50f-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="8c50f-161">Studd stýrikerfi</span><span class="sxs-lookup"><span data-stu-id="8c50f-161">Supported operating systems</span></span>

-   <span data-ttu-id="8c50f-162">Retail Hardware Station er 32-bita hugbúnaður, en hún mun keyra á x86 og x64 hönnun.</span><span class="sxs-lookup"><span data-stu-id="8c50f-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="8c50f-163">Retail Hardware Station er stutt á eftirfarandi stýrikerfum:</span><span class="sxs-lookup"><span data-stu-id="8c50f-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="8c50f-164">Windows 7 Professional, Enterprise og Embedded editions</span><span class="sxs-lookup"><span data-stu-id="8c50f-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="8c50f-165">Windows 7 er eingöngu stutt ef Internet Explorer 11 er uppsett handvirkt í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="8c50f-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="8c50f-166">Windows 8.1 Update 1 Professional Enterprise og Embedded editions</span><span class="sxs-lookup"><span data-stu-id="8c50f-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="8c50f-167">Windows 10 Pro Enterprise og Enterprise LTSB editions</span><span class="sxs-lookup"><span data-stu-id="8c50f-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="8c50f-168">Lágmarksþörf kerfis</span><span class="sxs-lookup"><span data-stu-id="8c50f-168">Minimum system requirements</span></span>

<span data-ttu-id="8c50f-169">Tölvan verður að uppfylla alla kerfiskröfur fyrir uppsetningu og notkun eftirfarandi atriða:</span><span class="sxs-lookup"><span data-stu-id="8c50f-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="8c50f-170">Internet Upplýsingaþjónusta (IIS)</span><span class="sxs-lookup"><span data-stu-id="8c50f-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="8c50f-171">Vélbúnaður þriðja aðila</span><span class="sxs-lookup"><span data-stu-id="8c50f-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="8c50f-172">Þarfir fyrir Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="8c50f-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="8c50f-173">Studd stýrikerfi</span><span class="sxs-lookup"><span data-stu-id="8c50f-173">Supported operating systems</span></span>

-   <span data-ttu-id="8c50f-174">Retail Store Scale Unit er 32-bita hugbúnaður, en hún mun keyra á x86 og x64 hönnun.</span><span class="sxs-lookup"><span data-stu-id="8c50f-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="8c50f-175">Retail Store Scale Unit er stutt á eftirfarandi stýrikerfum:</span><span class="sxs-lookup"><span data-stu-id="8c50f-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="8c50f-176">Windows 7 Professional, Enterprise og Embedded editions</span><span class="sxs-lookup"><span data-stu-id="8c50f-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="8c50f-177">Windows 8.1 Update 1 Professional Enterprise og Embedded editions</span><span class="sxs-lookup"><span data-stu-id="8c50f-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="8c50f-178">Windows 10 Pro Enterprise og Enterprise LTSB editions</span><span class="sxs-lookup"><span data-stu-id="8c50f-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="8c50f-179">Lágmarksþörf kerfis</span><span class="sxs-lookup"><span data-stu-id="8c50f-179">Minimum system requirements</span></span>

-   <span data-ttu-id="8c50f-180">4 GB RAM</span><span class="sxs-lookup"><span data-stu-id="8c50f-180">4 GB of RAM</span></span>
-   <span data-ttu-id="8c50f-181">1.6 GHz ferðatímabilinu CPU hraða á kjarnauppsetning (kjarna Tvær eru lágmarks.)</span><span class="sxs-lookup"><span data-stu-id="8c50f-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="8c50f-182">Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)</span><span class="sxs-lookup"><span data-stu-id="8c50f-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="8c50f-183">Ráðlagðar kerfisþarfir</span><span class="sxs-lookup"><span data-stu-id="8c50f-183">Recommended system requirements</span></span>

-   <span data-ttu-id="8c50f-184">6 GB RAM</span><span class="sxs-lookup"><span data-stu-id="8c50f-184">6 GB of RAM</span></span>
-   <span data-ttu-id="8c50f-185">2.4 GHz i7 (eða jafngildi) ferðatímabilinu CPU hraða á kjarnauppsetning (Fjórum kjarna ráðlagðar.)</span><span class="sxs-lookup"><span data-stu-id="8c50f-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="8c50f-186">Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)</span><span class="sxs-lookup"><span data-stu-id="8c50f-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="8c50f-187">Kröfur um connector</span><span class="sxs-lookup"><span data-stu-id="8c50f-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="8c50f-188">Studd stýrikerfi</span><span class="sxs-lookup"><span data-stu-id="8c50f-188">Supported operating systems</span></span>

-   <span data-ttu-id="8c50f-189">Tengillinn fyrir Microsoft Dynamics AX er með tvö mismunandi uppsetningarforrit, eitt fyrir Async Server Connector service og annað fyrir Real-time service for Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="8c50f-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="8c50f-190">Báðir íhlutir eru 32-bita hugbúnaður, en munu keyra bæði á x86 og x64 hönnun.</span><span class="sxs-lookup"><span data-stu-id="8c50f-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="8c50f-191">Bæði íhlutir eru studdir stýrikerfi eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8c50f-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="8c50f-192">Windows 7 Professional, Enterprise og Embedded editions</span><span class="sxs-lookup"><span data-stu-id="8c50f-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="8c50f-193">Windows 8.1 Update 1 Professional Enterprise og Embedded editions</span><span class="sxs-lookup"><span data-stu-id="8c50f-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="8c50f-194">Windows 10 Pro Enterprise og Enterprise LTSB editions</span><span class="sxs-lookup"><span data-stu-id="8c50f-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="8c50f-195">Microsoft Windows Server 2012 R2 og Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8c50f-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="8c50f-196">Lágmarksþörf kerfis</span><span class="sxs-lookup"><span data-stu-id="8c50f-196">Minimum system requirements</span></span>
-   <span data-ttu-id="8c50f-197">2 GB af RAM (Mælt er með 4 GB af RAM.)</span><span class="sxs-lookup"><span data-stu-id="8c50f-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="8c50f-198">1.6 GHz ferðatímabilinu CPU hraða á kjarnauppsetning (kjarna Tvær eru lágmarks.)</span><span class="sxs-lookup"><span data-stu-id="8c50f-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="8c50f-199">Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)</span><span class="sxs-lookup"><span data-stu-id="8c50f-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="8c50f-200">Kröfur til þróunar á staðbundna VMs</span><span class="sxs-lookup"><span data-stu-id="8c50f-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="8c50f-201">Sjá upplýsingar um þarfir fyrir þróun á staðbundna hýsilsheiti vélar (VMs) [VL keyrslu á verslunarsvæðis](../../dev-itpro/dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="8c50f-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../../dev-itpro/dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="8c50f-202">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8c50f-202">See also</span></span>

[<span data-ttu-id="8c50f-203">Sækja um mat afrit af Dynamics 365 til Fjármála og Aðgerðir Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="8c50f-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)


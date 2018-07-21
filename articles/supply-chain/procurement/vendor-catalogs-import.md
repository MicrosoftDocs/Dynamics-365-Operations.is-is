---
title: "Flytja inn vörulista lánardrottins"
description: "Þetta efnisatriði lýsir ferlinu til að flytja inn vörulistagögn lánardrottins."
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: 
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: d9e1202b7b4f995c9e54002df93c53c0976373fe
ms.contentlocale: is-is
ms.lasthandoff: 07/21/2018

---

# <a name="import-vendor-catalogs"></a><span data-ttu-id="c78dd-103">Flytja inn vörulista lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c78dd-103">Import vendor catalogs</span></span>
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="c78dd-104">Innflutningar á vörulisti lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c78dd-104">Vendor catalogs import</span></span>

<span data-ttu-id="c78dd-105">Í Microsoft Dynamics 365 for Finance and Operations geta innkaupasérfræðingar stofnað og unnið með vörulista sem starfsmenn fyrirtækis geta notað þegar þeir panta vörur og þjónustu til innri notkunar.</span><span class="sxs-lookup"><span data-stu-id="c78dd-105">In Microsoft Dynamics 365 for Finance and Operations, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="c78dd-106">Til að stofna innkaupavörulista er hægt að bæta við vörum og þjónustu sem eiga að vera í boði fyrir starfsmenn, annaðhvort með því að flytja inn innkaupavörulisti eða handvirkt bæta innkaupavörulista við afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="c78dd-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="c78dd-107">Hægt er að hlaða upp vörulistagögnum sem lánardrottinn hefur sent með biðlara Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c78dd-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="c78dd-108">Afurðargögnin sem lánardrottinn sendir til þín sem skáarformið viðhaldsbeiðni vörulista (CMR) verður að vera á XML-skráarsniði.</span><span class="sxs-lookup"><span data-stu-id="c78dd-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="c78dd-109">CMR-skráin ætti að innihalda upplýsingar um afurðirnar sem lánardrottinn veitir fyrirtækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="c78dd-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="c78dd-110">Flytja inn vörulistagögn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c78dd-110">Import vendor catalog data</span></span>

<span data-ttu-id="c78dd-111">Til að flytja inn vörulistagögn lánardrottins þarf að ljúka eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="c78dd-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1.  <span data-ttu-id="c78dd-112">Settu upp verk á vinnusvæði Gagnastjórnunar þar sem þú hefur skilgreint reglur gagnavörpunar.</span><span class="sxs-lookup"><span data-stu-id="c78dd-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="c78dd-113">Veldu **Gagnastjórnun** og veldu síðan **Setja upp hlutverk fyrir gagnaverk**.</span><span class="sxs-lookup"><span data-stu-id="c78dd-113">Select **Data management** and then select **Set up roles for data projects**.</span></span> 

2.  <span data-ttu-id="c78dd-114">Settu upp tegundastigveldi innkaupa og úthlutaðu lánardrottnum þínum á innkaupaflokka.</span><span class="sxs-lookup"><span data-stu-id="c78dd-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="c78dd-115">Ef þú notar vörukóða skaltu bæta vörukóðanum við innkaupaflokka.</span><span class="sxs-lookup"><span data-stu-id="c78dd-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="c78dd-116">Til að fá upplýsingar um uppsetningu á tegundastigveldi innkaupa skaltu sjá [Setja upp tegundastigveldi innkaupa](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="c78dd-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3.  <span data-ttu-id="c78dd-117">Stilla lánardrottinn fyrir innflutning vörulista.</span><span class="sxs-lookup"><span data-stu-id="c78dd-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="c78dd-118">Veldu lánardrottin og veldu síðan **Innkaup** > **Setja upp** > **Stilla lánardrottin fyrir vörulistainnflutning**.</span><span class="sxs-lookup"><span data-stu-id="c78dd-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4.  <span data-ttu-id="c78dd-119">Stilla verkflæði fyrir vörulistainnflutning.</span><span class="sxs-lookup"><span data-stu-id="c78dd-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="c78dd-120">Stofna CMR-skráarsniðmát og deila því með lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="c78dd-120">Create a CMR file template and share this with your vendor.</span></span>

5.  <span data-ttu-id="c78dd-121">Veldu **Innkaup og aðföng** \> **Algengt** \> **Vörulistar** \> **Vörulistar lánardrottins** til að stofna vörulista lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c78dd-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="c78dd-122">Skrárnar fyrir viðhaldsbeiðni vörulista (CMR) sem þú færð frá lánardrottni eru flokkaðar í þessum vörulista.</span><span class="sxs-lookup"><span data-stu-id="c78dd-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6.  <span data-ttu-id="c78dd-123">Hlaða upp CMR-skránni.</span><span class="sxs-lookup"><span data-stu-id="c78dd-123">Upload the CMR file.</span></span>

7.  <span data-ttu-id="c78dd-124">Yfirfara, samþykkja eða hafna afurðum í vörulista lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c78dd-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="c78dd-125">Vörunum er sjálfkrafa varpað á innkaupaflokka í Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c78dd-125">The products are automatically mapped to the procurement categories in Dynamics 365 for Finance and Operations.</span></span> 
    
<span data-ttu-id="c78dd-126">Samþykktum afurðum er bætt við afurðarsniðmát og sendar til valins lögaðila.</span><span class="sxs-lookup"><span data-stu-id="c78dd-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="c78dd-127">Aðeins er hægt að bæta samþykktum afurðum við innkaupavörulistann.</span><span class="sxs-lookup"><span data-stu-id="c78dd-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="c78dd-128">Mynda sniðmát fyrir innflutningsskrá vörulista</span><span class="sxs-lookup"><span data-stu-id="c78dd-128">Generate a catalog import file template</span></span>

<span data-ttu-id="c78dd-129">Sniðmát fyrir innflutningsskrá vörulista er XSD-skrá sem notuð er til að stofna CMR-skrá fyrir afurðir lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c78dd-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor’s products.</span></span> <span data-ttu-id="c78dd-130">Hægt er að nota CMR-skrána til að stofna nýjan vörulista, skipta út fyrirliggjandi vörulista eða breyta fyrirliggjandi vörulista.</span><span class="sxs-lookup"><span data-stu-id="c78dd-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1.  <span data-ttu-id="c78dd-131">Veldu **Innkaup og aðföng** \> **Vörulistar** \> **Vörulistar lánardrottins** og tvísmelltu á vörulistann sem þú vilt vinna með.</span><span class="sxs-lookup"><span data-stu-id="c78dd-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor catalogs** and double-click the catalog that you want to work with.</span></span>

2.  <span data-ttu-id="c78dd-132">Sæktu núverandi sniðmát vörulistainnflutnings (XSD-skrá).</span><span class="sxs-lookup"><span data-stu-id="c78dd-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="c78dd-133">Á síðunni **Uppfæra vörulista**, á **Aðgerðarsvæði**, á flipanum **Vörulistar** í flokknum **Tengdar upplýsingar** skaltu smella á **Búa til sniðmát vörulista** og velja **Innkaupategund**.</span><span class="sxs-lookup"><span data-stu-id="c78dd-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    -   <span data-ttu-id="c78dd-134">Með valkostinum **Innkaupaflokkar** er hægt að búa til sniðmát vörulista sem inniheldur innkaupaflokka þar sem lánardrottni er heimilað að útvega afurðir.</span><span class="sxs-lookup"><span data-stu-id="c78dd-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="c78dd-135">Í svarglugganum **Vista sem** skaltu velja staðsetningu þar sem á að geyma sniðmát fyrir vörulistaskrá og vista skrána.</span><span class="sxs-lookup"><span data-stu-id="c78dd-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="c78dd-136">Nánari upplýsingar og dæmi er að finna í þessari bloggfærslu: [Vörulistar lánardrottins í Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="c78dd-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>


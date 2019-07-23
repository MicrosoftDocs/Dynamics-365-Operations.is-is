---
title: (ER) Flytja inn skilgreiningar úr RCS
description: Þetta efni gefur upplýsingar um hvernig notandi getur flutt inn nýja útgáfu af ER-skilgreiningum úr RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c458cf815837fb7e4688c4c0443b7962cac403a5
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727007"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="bda6a-103">(ER) Flytja inn skilgreiningar úr RCS</span><span class="sxs-lookup"><span data-stu-id="bda6a-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bda6a-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="bda6a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="bda6a-105">Í þessu dæmi munt þú velja útgáfu af ER-skilgreiningum sem hafa verið skilgreindar í RCS-tilviki og flytja hana inn í núverandi tilvik Finance and Operations fyrir sýnisfyrirtækið, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningunum er deilt milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="bda6a-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current Finance and Operations instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="bda6a-106">Til að ljúka þessum skrefum verður fyrst að ljúka skrefunum í efninu [Stofna skilgreiningaveitu og merkja hana sem virka](er-configuration-provider-mark-it-active-2016-11.md) í RCS.</span><span class="sxs-lookup"><span data-stu-id="bda6a-106">To complete these steps, you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="bda6a-107">Til að ljúka þessum skrefum verður þú einnig að hafa aðgang að RCS-tilviki sem inniheldur að minnsta kosti eina ER-skilgreiningu í annaðhvort stöðunni **Lokið** eða **Deilt**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="bda6a-108">Farðu í **Fyrirtækisstjórnun** > **Vinnusvæði** > **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="bda6a-109">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="bda6a-110">Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í efninu [Stofna skilgreiningaveitu og merkja hana sem virka](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="bda6a-110">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="bda6a-111">Ef þú ert ekki með neinu RCS-umhverfi sem úthlutað á fyrirtækið skaltu smella á ytri tengilinn **Regulatory Services – Skilgreiningar** og fylgja leiðbeiningunum til að úthluta RCS-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="bda6a-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="bda6a-112">Smelltu á **Rafrænar skýrslufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="bda6a-113">Smelltu á flipann **RCS**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="bda6a-114">Ef RCS-umhverfinu hefur þegar verið úthlutað á fyrirtækið skaltu nota vefslóðirnar sem eru á síðunni til að fá aðgang að því.</span><span class="sxs-lookup"><span data-stu-id="bda6a-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="bda6a-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bda6a-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="bda6a-116">Skráðu nýja ER-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="bda6a-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="bda6a-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="bda6a-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="bda6a-118">Veldu veituna Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="bda6a-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="bda6a-119">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="bda6a-119">Click Repositories.</span></span> 
4. <span data-ttu-id="bda6a-120">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="bda6a-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="bda6a-121">Í reitnum gerð geymslu fyrir grunnstillingar, færðu inn "RCS".</span><span class="sxs-lookup"><span data-stu-id="bda6a-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="bda6a-122">Smellið á Stofna gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="bda6a-122">Click Create repository.</span></span> 
7. <span data-ttu-id="bda6a-123">Sláðu inn eða veldu gildi í heitareitnum RCS-umhverfisbirting.</span><span class="sxs-lookup"><span data-stu-id="bda6a-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="bda6a-124">Veldu viðeigandi RCS-tilvik.</span><span class="sxs-lookup"><span data-stu-id="bda6a-124">Select the desired RCS instance.</span></span> <span data-ttu-id="bda6a-125">Athugaðu að þú getur verið með nokkur slík.</span><span class="sxs-lookup"><span data-stu-id="bda6a-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="bda6a-126">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="bda6a-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="bda6a-127">Flyttu inn ER-skilgreiningar úr RCS-geymslu</span><span class="sxs-lookup"><span data-stu-id="bda6a-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="bda6a-128">Smelltu á **Sýna síur**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="bda6a-129">Sláðu inn síugildið „RCS“ í reitinn **Heiti** með því að nota síuvirknitáknið **hefst á**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="bda6a-130">Þegar þú opnar valda geymslu á síðunni **Tengjast við Regulatory Configuration Services** skaltu smella á tengilinn **Smella hér til að tengjast Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="bda6a-131">Smelltu á **Opna**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-131">Click **Open**.</span></span> 
5. <span data-ttu-id="bda6a-132">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="bda6a-132">Click **Close**.</span></span> 
6. <span data-ttu-id="bda6a-133">Veldu viðeigandi útgáfu af ER-skilgreiningum og smelltu á **Flytja inn** til að færa það inn í núverandi tilvik Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bda6a-133">Select the desired version of ER configuration and click **Import** to bring it in the current Finance and Operations instance.</span></span>


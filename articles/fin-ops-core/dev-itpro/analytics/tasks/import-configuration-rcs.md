---
title: (ER) Flytja inn skilgreiningar úr RCS
description: Þetta efni gefur upplýsingar um hvernig notandi getur flutt inn nýja útgáfu af ER-skilgreiningum úr RCS.
author: NickSelin
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77d637b2ec1deeabc04a6796644363b330f5756e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744892"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="2214e-103">(ER) Flytja inn skilgreiningar úr RCS</span><span class="sxs-lookup"><span data-stu-id="2214e-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2214e-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="2214e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="2214e-105">Í þessu dæmi munt þú velja útgáfu af ER-skilgreiningum sem hafa verið skilgreindar í RCS-tilviki og flytja hana inn í núverandi tilvik fyrir sýnisfyrirtækið, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningunum er deilt milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="2214e-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="2214e-106">Til að ljúka þessum skrefum verður fyrst að ljúka skrefunum í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2214e-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="2214e-107">Til að ljúka þessum skrefum verður þú einnig að hafa aðgang að RCS-tilviki sem inniheldur að minnsta kosti eina ER-skilgreiningu í annaðhvort stöðunni **Lokið** eða **Deilt**.</span><span class="sxs-lookup"><span data-stu-id="2214e-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="2214e-108">Farðu í **Fyrirtækisstjórnun** > **Vinnusvæði** > **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="2214e-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="2214e-109">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**.</span><span class="sxs-lookup"><span data-stu-id="2214e-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="2214e-110">Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2214e-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="2214e-111">Ef engu RCS-umhverfi er úthlutað fyrir fyrirtækið skaltu velja ytri tengilinn **Regulatory services – skilgreining** og fylgja svo leiðbeiningunum til að úthluta RCS-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="2214e-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="2214e-112">Veljið **Rafrænar skýrslugerðarfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="2214e-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="2214e-113">Veljið flipann **RCS**.</span><span class="sxs-lookup"><span data-stu-id="2214e-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="2214e-114">Ef RCS-umhverfinu hefur þegar verið úthlutað á fyrirtækið skaltu nota vefslóðirnar sem eru á síðunni til að fá aðgang að því.</span><span class="sxs-lookup"><span data-stu-id="2214e-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="2214e-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2214e-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="2214e-116">Skráðu nýja ER-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="2214e-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="2214e-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2214e-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="2214e-118">Veldu veituna Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="2214e-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="2214e-119">Veldu Geymslur.</span><span class="sxs-lookup"><span data-stu-id="2214e-119">Select Repositories.</span></span> 
4. <span data-ttu-id="2214e-120">Veldu Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="2214e-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="2214e-121">Í reitnum gerð geymslu fyrir grunnstillingar, færðu inn "RCS".</span><span class="sxs-lookup"><span data-stu-id="2214e-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="2214e-122">Veljið Stofna geymslu.</span><span class="sxs-lookup"><span data-stu-id="2214e-122">Select Create repository.</span></span> 
7. <span data-ttu-id="2214e-123">Sláðu inn eða veldu gildi í heitareitnum RCS-umhverfisbirting.</span><span class="sxs-lookup"><span data-stu-id="2214e-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="2214e-124">Veldu viðeigandi RCS-tilvik.</span><span class="sxs-lookup"><span data-stu-id="2214e-124">Select the desired RCS instance.</span></span> <span data-ttu-id="2214e-125">Hægt er að hafa nokkra þeirra.</span><span class="sxs-lookup"><span data-stu-id="2214e-125">You can have several of them.</span></span> 
9. <span data-ttu-id="2214e-126">Veljið Í lagi.</span><span class="sxs-lookup"><span data-stu-id="2214e-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="2214e-127">Flytja inn skilgreiningar rafrænnar skýrslugerðar úr RCS-gagnageymslu</span><span class="sxs-lookup"><span data-stu-id="2214e-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="2214e-128">Velja **Sýna síur**.</span><span class="sxs-lookup"><span data-stu-id="2214e-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="2214e-129">Sláðu inn síugildið „RCS“ í reitinn **Heiti** með því að nota síuvirknitáknið **hefst á**.</span><span class="sxs-lookup"><span data-stu-id="2214e-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="2214e-130">Þegar valin geymsla er opnuð á **Tengjast við Regulatory Configuration Services** skal velja tengilinn **Smelltu hér til að tengjast Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="2214e-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="2214e-131">Veljið **Opna**.</span><span class="sxs-lookup"><span data-stu-id="2214e-131">Select **Open**.</span></span> 
5. <span data-ttu-id="2214e-132">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="2214e-132">Select **Close**.</span></span> 
6. <span data-ttu-id="2214e-133">Veljið æskilega útgáfu af skilgreiningu rafrænnar skýrslugerðar og veljið **Flytja inn** til að færa hana inn í núverandi tilvik.</span><span class="sxs-lookup"><span data-stu-id="2214e-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
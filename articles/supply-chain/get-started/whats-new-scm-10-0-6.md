---
title: Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.6. (nóvember 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 83798af9c39ae8845125026903741882356d8845
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909330"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="261ab-103">Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.6. (nóvember 2019)</span><span class="sxs-lookup"><span data-stu-id="261ab-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="261ab-104">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span><span class="sxs-lookup"><span data-stu-id="261ab-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="261ab-105">Þessi útgáfa er með byggingarnúmer 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="261ab-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="261ab-106">Þótt almennur framboðsdagur sé í nóvember eru nýju eiginleikarnir tiltækir til snemmbærrar útgáfu í október.</span><span class="sxs-lookup"><span data-stu-id="261ab-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="261ab-107">Frekari upplýsingar um útgáfu 10.0.6 er að finna í [Frekari upplýsingar](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="261ab-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="261ab-108">V2 gagnaeining afbrigðalíkana afurðar</span><span class="sxs-lookup"><span data-stu-id="261ab-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="261ab-109">Önnur útgáfa fyrir gagnaeininguna „vöruuppsetningarlíkön“ er gefin út (kallað „Vöruuppsetningarmódel V2“).</span><span class="sxs-lookup"><span data-stu-id="261ab-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="261ab-110">Sjálfgefið sniðmát „418-vöruuppsetningarlíkön“ þarf einnig að vera þannig að það notar nýju „Vöruuppsetningarmódelin V2“ gagnaeininguna í innflutnings- / útflutningsramma sniðmátunum.</span><span class="sxs-lookup"><span data-stu-id="261ab-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="261ab-111">Sniðmátið verður ekki uppfært sjálfvirkt þannig að þú verður að hlaða sniðmátið sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="261ab-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="261ab-112">V2 einingin flytur út eina röð sem aðskild skrá í viðhengi í staðinn fyrir að vera í röð og leysa stærðartakmarkanir V1 einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="261ab-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="261ab-113">Hvað þarftu að gera til að gera þessa breytingu?</span><span class="sxs-lookup"><span data-stu-id="261ab-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="261ab-114">Þar sem V1 einingin hefur verið felld úr gildi ættir þú að byrja að flytja úr V1 til V2.</span><span class="sxs-lookup"><span data-stu-id="261ab-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="261ab-115">Ef þú ert að nota sniðmátið „418 vörulíkan“ geturðu smellt á hnappinn „hlaðið sjálfgefið sniðmát“ og endurhlaðið sniðmátið „418 - módel vörustillinga“</span><span class="sxs-lookup"><span data-stu-id="261ab-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="261ab-116">Ef þú þarft að halda eindrægni við núverandi kerfi geturðu haldið áfram að nota það sniðmát og (úrelt) V1 eininguna þar til þú færir samþættingarnar í nýja sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="261ab-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="261ab-117">Eiginleikastjórnunarviðbætur</span><span class="sxs-lookup"><span data-stu-id="261ab-117">Feature management enhancements</span></span>
<span data-ttu-id="261ab-118">Eiginleikastjórnun gerir þér nú kleift að virkja alla nýja eiginleika sjálfgefið, krefjast staðfestingar til að virkja eiginleika og virkja alla eiginleika sem ekki hafa þegar verið gerðir virkir.</span><span class="sxs-lookup"><span data-stu-id="261ab-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="261ab-119">Ábyrgðaraðili innkaupasamnings</span><span class="sxs-lookup"><span data-stu-id="261ab-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="261ab-120">Þú hefur nú getu til að skilgreina aðal- og framhaldsaðila á flokkunarformi innkaupasamnings og innkaupasamningum sem af því hljótast.</span><span class="sxs-lookup"><span data-stu-id="261ab-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="261ab-121">Þetta veitir notandanum aðgang að þeim sem hefur umsjón með samningunum.</span><span class="sxs-lookup"><span data-stu-id="261ab-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="261ab-122">RFQ-tengill í línu innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="261ab-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="261ab-123">Þú getur bætt við tilvísunartengil frá innkaupapöntunarlínunum aftur í samsvarandi RFQ línur sem þeir eru upprunnar frá, þannig að notandinn getur auðveldlega fengið styðjandi skjal beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="261ab-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="261ab-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="261ab-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="261ab-125">Villuleiðréttingar</span><span class="sxs-lookup"><span data-stu-id="261ab-125">Bug fixes</span></span>
<span data-ttu-id="261ab-126">Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.6, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="261ab-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="261ab-127">Update 30 fyrir verkvang</span><span class="sxs-lookup"><span data-stu-id="261ab-127">Platform update 30</span></span>
<span data-ttu-id="261ab-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 inniheldur verkvangsuppfærslu 30.</span><span class="sxs-lookup"><span data-stu-id="261ab-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="261ab-129">Til að læra meira um verkvangsuppfærslu 30, sjá [Hvað er nýtt eða breytt í verkvangsuppfærslu 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="261ab-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="261ab-130">Dynamics 365: 2019 útgáfa bylgja 2 áætlun</span><span class="sxs-lookup"><span data-stu-id="261ab-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="261ab-131">Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?</span><span class="sxs-lookup"><span data-stu-id="261ab-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="261ab-132">Skoðaðu [Dynamics 365: 2019 útgáfu bylgju 2 áætlun](/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="261ab-132">Check out the [Dynamics 365: 2019 release wave 2 plan](/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="261ab-133">Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="261ab-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="261ab-134">Fjarlægðir og úreltir eiginleikar Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="261ab-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="261ab-135">Efnið [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="261ab-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="261ab-136">*Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.</span><span class="sxs-lookup"><span data-stu-id="261ab-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="261ab-137">*Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="261ab-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="261ab-138">Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í efninu [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.</span><span class="sxs-lookup"><span data-stu-id="261ab-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="261ab-139">Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði.</span><span class="sxs-lookup"><span data-stu-id="261ab-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="261ab-140">Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.</span><span class="sxs-lookup"><span data-stu-id="261ab-140">Typically, these are functional updates that need to be made to the compiler.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
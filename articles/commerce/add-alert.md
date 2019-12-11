---
title: Viðvörunareining
description: Þetta efni fjallar um viðvörunareiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785353"
---
# <a name="alert-module"></a><span data-ttu-id="3779f-103">Viðvörunareining</span><span class="sxs-lookup"><span data-stu-id="3779f-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3779f-104">Þetta efni fjallar um viðvörunareiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3779f-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3779f-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="3779f-105">Overview</span></span>

<span data-ttu-id="3779f-106">Viðvörunareining er notuð til að sýna upplýsingarskilaboð á síðu.</span><span class="sxs-lookup"><span data-stu-id="3779f-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="3779f-107">Viðvörunareiningar styðja textaskilaboð og tengil.</span><span class="sxs-lookup"><span data-stu-id="3779f-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="3779f-108">Hægt er að nota þær til að sýna kynningar á öllu svæðinu sem birtast á öllum síðum svæðis rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="3779f-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="3779f-109">Viðvörunareiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="3779f-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="3779f-110">Dæmi um viðvörunareiningar í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="3779f-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="3779f-111">Hægt er að nota viðvörunareiningar í síðuhausnum til að gefa til kynna kynningar eða skilaboð á öllu svæðinu.</span><span class="sxs-lookup"><span data-stu-id="3779f-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="3779f-112">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="3779f-112">Here are some examples:</span></span>

<span data-ttu-id="3779f-113">„Árlegri útsölu lýkur eftir 10 daga“</span><span class="sxs-lookup"><span data-stu-id="3779f-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="3779f-114">„Stórsparnaður með útsölu fyrir skólann.</span><span class="sxs-lookup"><span data-stu-id="3779f-114">"Save big with back to school sale.</span></span> <span data-ttu-id="3779f-115">Verslaðu núna."</span><span class="sxs-lookup"><span data-stu-id="3779f-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="3779f-116">Eiginleikar viðvörunareiningar</span><span class="sxs-lookup"><span data-stu-id="3779f-116">Alert module properties</span></span>

| <span data-ttu-id="3779f-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="3779f-117">Property name</span></span>  | <span data-ttu-id="3779f-118">Virði</span><span class="sxs-lookup"><span data-stu-id="3779f-118">Value</span></span>                              | <span data-ttu-id="3779f-119">Lýsing</span><span class="sxs-lookup"><span data-stu-id="3779f-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="3779f-120">Texti</span><span class="sxs-lookup"><span data-stu-id="3779f-120">Text</span></span>           | <span data-ttu-id="3779f-121">Texti</span><span class="sxs-lookup"><span data-stu-id="3779f-121">Text</span></span>                               | <span data-ttu-id="3779f-122">Textaboðin sem birtast í viðvörunareiningunni.</span><span class="sxs-lookup"><span data-stu-id="3779f-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="3779f-123">Textajöfnun</span><span class="sxs-lookup"><span data-stu-id="3779f-123">Text alignment</span></span> | <span data-ttu-id="3779f-124">**Hægri**, **Vinstri** eða **Miðja**</span><span class="sxs-lookup"><span data-stu-id="3779f-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="3779f-125">Gildi sem skilgreinir hvernig texti er samstilltur í viðvörunareiningunni.</span><span class="sxs-lookup"><span data-stu-id="3779f-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="3779f-126">Hunsa viðvörun</span><span class="sxs-lookup"><span data-stu-id="3779f-126">Dismiss alert</span></span>  | <span data-ttu-id="3779f-127">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="3779f-127">**True** or **False**</span></span>              | <span data-ttu-id="3779f-128">Ef gildi er stillt á **Satt** getur viðskiptavinurinn hafnað viðvöruninni.</span><span class="sxs-lookup"><span data-stu-id="3779f-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="3779f-129">Tengill</span><span class="sxs-lookup"><span data-stu-id="3779f-129">Link</span></span>           | <span data-ttu-id="3779f-130">Vefslóð</span><span class="sxs-lookup"><span data-stu-id="3779f-130">URL</span></span>                                | <span data-ttu-id="3779f-131">Slóðin fyrir valfrjálsan tengil.</span><span class="sxs-lookup"><span data-stu-id="3779f-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="3779f-132">Bæta viðvörunareiningu við á síðu</span><span class="sxs-lookup"><span data-stu-id="3779f-132">Add an alert module to a page</span></span> 

<span data-ttu-id="3779f-133">Fylgdu þessum skrefum til að bæta viðvörunareiningu við síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="3779f-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3779f-134">Búðu til síðusniðmát sem heitir **viðvörunarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="3779f-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="3779f-135">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við viðvörunareiningu.</span><span class="sxs-lookup"><span data-stu-id="3779f-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="3779f-136">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="3779f-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="3779f-137">Notaðu viðvörunarsniðmátið sem þú bjóst til til að búa til síðu sem heitir **viðvörunarsíða**.</span><span class="sxs-lookup"><span data-stu-id="3779f-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="3779f-138">Í hólfinu **Aðal** á nýju síðunni bætirðu við viðvörunareiningu.</span><span class="sxs-lookup"><span data-stu-id="3779f-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="3779f-139">Sláðu inn viðvörunatexta í stillingum fyrir viðvörunareininguna.</span><span class="sxs-lookup"><span data-stu-id="3779f-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="3779f-140">Þú getur breytt öðrum eiginleikum ef þú vilt sérsníða viðvörunareininguna frekar.</span><span class="sxs-lookup"><span data-stu-id="3779f-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="3779f-141">Vistaðu og forskoðaðu síðuna.</span><span class="sxs-lookup"><span data-stu-id="3779f-141">Save and preview the page.</span></span> <span data-ttu-id="3779f-142">Efst á síðunni ættirðu að sjá viðvörun sem hefur textann sem þú bættir við.</span><span class="sxs-lookup"><span data-stu-id="3779f-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="3779f-143">Athuga á síðunni og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="3779f-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="3779f-144">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3779f-144">Additional resources</span></span>

[<span data-ttu-id="3779f-145">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="3779f-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3779f-146">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="3779f-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="3779f-147">Eining með fjölbreyttu efni</span><span class="sxs-lookup"><span data-stu-id="3779f-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="3779f-148">Staðsetningareining efnis</span><span class="sxs-lookup"><span data-stu-id="3779f-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="3779f-149">Eiginleikaeining</span><span class="sxs-lookup"><span data-stu-id="3779f-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="3779f-150">Hetjueining</span><span class="sxs-lookup"><span data-stu-id="3779f-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="3779f-151">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="3779f-151">Video player module</span></span>](add-video-player.md)

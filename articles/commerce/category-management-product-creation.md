---
title: Stjórna afurðaflokkum og afurðum
description: Þetta efnisatriði lýsir því hvernig vörustjórar geta notað flokka smásöluafurða til að stjórna tengslum milli afurðastigveldis Commerce og upplýsinga um losaðar afurðir.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9d47a866703b830e84e3f2e37a02d9d58f73987b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413126"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="6eeea-103">Stjórna afurðaflokkum og afurðum</span><span class="sxs-lookup"><span data-stu-id="6eeea-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="6eeea-104">Þetta efnisatriði lýsir betri leið til að stjórna afurðaflokkum og afurðum í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6eeea-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="6eeea-105">Viðbæturnar gera vörustjórum kleift að skoða byggingu á eiginleikum afurðar sem er deilt milli stigveldis afurðar og upplýsinga um losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="6eeea-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="6eeea-106">Til að læra meira um stjórnun á flokkum afurða í vinnusvæðinu **Flokka- og afurðastjórnun** skal velja reitinn **Afurðastigveldi Commerce**.</span><span class="sxs-lookup"><span data-stu-id="6eeea-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="6eeea-107">Takið eftir aukinni uppbyggingu á síðunni **Afurðastigveldi Commerce** sem birtist.</span><span class="sxs-lookup"><span data-stu-id="6eeea-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="6eeea-108">Í fyrri útgáfum forritsins var eiginleikum afurða skipt niður í *grunneiginleika afurðar* og *eiginleika smásöluafurðar* byggt á notkunareiginleikum þeirra.</span><span class="sxs-lookup"><span data-stu-id="6eeea-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="6eeea-109">Eiginleikar smásöluafurðar eru *altækir* í notkunareiginleikum þeirra.</span><span class="sxs-lookup"><span data-stu-id="6eeea-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="6eeea-110">M.ö.o., fyrir hvern eiginleika afurðar er sama gildi deilt með öllum lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="6eeea-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="6eeea-111">Hins vegar eru grunneiginleikar afurðar *sértækir fyrir hvern lögaðila*.</span><span class="sxs-lookup"><span data-stu-id="6eeea-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="6eeea-112">Með öðrum orðum, fyrir tiltekinn grunneiginleika afurðar getur gildið verið mismunandi milli lögaðila, fer allt eftir einstökum viðskiptakröfum hvers lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6eeea-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="6eeea-113">Með aukinni byggingu á flokkum afurðar eru eiginleikar afurða röklega greindir í sundur eftir notkunareiginleikum þeirra innan hóps til að endurspegla byggingu skjámyndar fyrir upplýsingar um losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="6eeea-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Svæði flokkuð á grundvelli notkunareiginleika](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="6eeea-115">Hægt er að skipta á milli þess að stjórna sértækum eiginleikum lögaðila yfir alla lögaðila og stjórna þeim fyrir tiltekinn lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6eeea-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="6eeea-116">Til að stjórna eiginleikum yfir alla lögaðila skal velja **Skoða fyrir alla lögaðila** (eða **Breyta fyrir alla lögaðila**).</span><span class="sxs-lookup"><span data-stu-id="6eeea-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Skoða/breyta fyrir alla lögaðila](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="6eeea-118">Til að stjórna eiginleikum fyrir tiltekinn lögaðila skal velja **Skoða fyrir tiltekinn lögaðila** (eða **Breyta fyrir tiltekinn lögaðila**).</span><span class="sxs-lookup"><span data-stu-id="6eeea-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Skoða/breyta fyrir tiltekinn lögaðila](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="6eeea-120">Auk þess getur vörustjóri í betrumbættu byggingunni á flokkum afurðar nú einnig skilgreint sjálfgildi fyrir viðbótarsett af eiginleikum afurðar á stigi einstakra flokka.</span><span class="sxs-lookup"><span data-stu-id="6eeea-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="6eeea-121">Þegar afurðir eru síðan búnar til öðlast þær sjálfgefið gildi fyrir afurðaeiginleika þeirra sem byggist á tengslum þessara eiginleika við einstakan flokk í stigveldi smásöluafurðar.</span><span class="sxs-lookup"><span data-stu-id="6eeea-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="6eeea-122">Þessir erfðu eiginleikar afurðar er einnig hægt að breyta fyrir hverja afurð til að uppfylla einstakar viðskiptakröfur.</span><span class="sxs-lookup"><span data-stu-id="6eeea-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="6eeea-123">Val á eiginleikum til að uppfæra afurðir á síðunni Afurðastigveldi Commerce</span><span class="sxs-lookup"><span data-stu-id="6eeea-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="6eeea-124">Hægt er að nota nýju betrumbættu bygginguna fyrir eiginleika afurðar til að velja hvaða uppfærðu eiginleikar afurðar á að flytja til tengdra afurða.</span><span class="sxs-lookup"><span data-stu-id="6eeea-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="6eeea-125">Á síðunni **Afurðastigveldi Commerce**, skal velja á aðgerðasvæðinu **Flokkur** og síðan velja **Uppfæra afurðir** til að opna svargluggann **Uppfæra afurðir**.</span><span class="sxs-lookup"><span data-stu-id="6eeea-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Uppfæra svarglugga afurða](media/NewUpdateProductsEnhancedView.PNG)

---
title: Skilgreina fjárhagsvíddir
description: Þessi leiðarvísir fyrir verk sýnir hvernig bætt er við einingu afrita fjárhagsvídd og sérstillta fjárhagsvídd.
author: aprilolson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c93a67d0c4a8443eaf40b094770ed6ce29da527b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834453"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="7815b-103">Skilgreina fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="7815b-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7815b-104">Þessi leiðarvísir fyrir verk sýnir hvernig bætt er við einingu afrita fjárhagsvídd og sérstillta fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="7815b-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="7815b-105">Leiðbeiningarnar nota USMF sýnigögn fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="7815b-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="7815b-106">Stofna fjárhagsvídd afritaðra eininga.</span><span class="sxs-lookup"><span data-stu-id="7815b-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="7815b-107">Farðu í **Skoðunarrúðu > Kerfiseiningar > Fjárhag > Bókhaldslykill > Víddir > Fjárhagsvíddir**.</span><span class="sxs-lookup"><span data-stu-id="7815b-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="7815b-108">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7815b-108">Click **New**.</span></span>
3. <span data-ttu-id="7815b-109">Í reitnum **Notandagildi** skal velja kerfisskilgreinda einingu til að byggja fjárhagsvíddina á.</span><span class="sxs-lookup"><span data-stu-id="7815b-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="7815b-110">Í reitinn **Heiti víddar** skal slá inn gildi til að lýsa fjárhagsvíddinni.</span><span class="sxs-lookup"><span data-stu-id="7815b-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="7815b-111">Heitið getur verið annað en kerfisskilgreind eining en má ekki innihalda bil eða sérstafi.</span><span class="sxs-lookup"><span data-stu-id="7815b-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="7815b-112">Smellið á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="7815b-112">Click **Activate**.</span></span> <span data-ttu-id="7815b-113">Virkjun fjárhagsvíddar uppfærir töflu með fjárhagsvíddarheitinu og fjarlægir eyddum víddum.</span><span class="sxs-lookup"><span data-stu-id="7815b-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="7815b-114">Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð en fjárhagsvídd er ekki hægt að nota fyrr en hún er virkjuð.</span><span class="sxs-lookup"><span data-stu-id="7815b-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="7815b-115">Smelltu á **Loka** í virkjunarskilaboðunum.</span><span class="sxs-lookup"><span data-stu-id="7815b-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="7815b-116">Smellið á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="7815b-116">Click **Activate**.</span></span> <span data-ttu-id="7815b-117">Hægt er að tímasetja virkjun víddar þannig að hún keyri í runu á tilteknum degi og tíma.</span><span class="sxs-lookup"><span data-stu-id="7815b-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="7815b-118">Í **Aðgerðasvæði** er smellt á **Víddargildi**.</span><span class="sxs-lookup"><span data-stu-id="7815b-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="7815b-119">Sum víddargildi eru bundin fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="7815b-119">Some dimension values are company specific.</span></span> <span data-ttu-id="7815b-120">Hægt er að staðfesta hvort þær eru bundnar fyrirtæki með því hvort heiti fyrirtækisins er sýnt í lista yfir víddargildi.</span><span class="sxs-lookup"><span data-stu-id="7815b-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="7815b-121">Stofna sérstillta fjárhagsvídd</span><span class="sxs-lookup"><span data-stu-id="7815b-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="7815b-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7815b-122">Close the page.</span></span>
2. <span data-ttu-id="7815b-123">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7815b-123">Click **New**.</span></span>
3. <span data-ttu-id="7815b-124">Í reitnum **Nota virði frá** skaltu velja **Sérsniðin vídd**.</span><span class="sxs-lookup"><span data-stu-id="7815b-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="7815b-125">Í reitinn **Heiti víddar** skal slá inn gildi til að lýsa fjárhagsvíddinni.</span><span class="sxs-lookup"><span data-stu-id="7815b-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="7815b-126">Heitið getur ekki innihaldið bil eða sérstafi.</span><span class="sxs-lookup"><span data-stu-id="7815b-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="7815b-127">Einnig er hægt að tilgreina lykilsíu til að takmarka magn og gerð upplýsinga sem hægt er að færa inn víddargildi fyrir.</span><span class="sxs-lookup"><span data-stu-id="7815b-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="7815b-128">Hægt er að færa inn stafi sem eru þeir sömu og fyrir hvert víddargildi eins og stafi eða bandstrik.</span><span class="sxs-lookup"><span data-stu-id="7815b-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="7815b-129">Einnig er hægt að færa inn tákn (#) og merki (&) sem frátakara fyrir stafi og tölustafi sem breytast í hvert skipti sem víddargildi eru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="7815b-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="7815b-130">Nota skal númeratákn (#) sem frátakara fyrir tölustafi og merki (&) sem frátakara fyrir stafi.</span><span class="sxs-lookup"><span data-stu-id="7815b-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="7815b-131">Dæmi: Til að takmarka víddargildi við stafina CC og þrjár tölur færirðu inn CC-### sem sniðsíu.</span><span class="sxs-lookup"><span data-stu-id="7815b-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="7815b-132">Smellið á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="7815b-132">Click **Activate**.</span></span> <span data-ttu-id="7815b-133">Virkjun fjárhagsvíddar uppfærir töflu með fjárhagsvíddarheitinu og fjarlægir eyddum víddum.</span><span class="sxs-lookup"><span data-stu-id="7815b-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="7815b-134">Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð en fjárhagsvídd er ekki hægt að nota fyrr en hún er virkjuð.</span><span class="sxs-lookup"><span data-stu-id="7815b-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="7815b-135">Smellið á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="7815b-135">Click **Activate**.</span></span> <span data-ttu-id="7815b-136">Hægt er að tímasetja virkjun víddar þannig að hún keyri í runu á tilteknum degi og tíma.</span><span class="sxs-lookup"><span data-stu-id="7815b-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="7815b-137">Í **Aðgerðasvæði** er smellt á **Víddargildi**.</span><span class="sxs-lookup"><span data-stu-id="7815b-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="7815b-138">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7815b-138">Click **New**.</span></span>
9. <span data-ttu-id="7815b-139">Í reitnum **Víddargildi** skal slá inn heiti til að lýsa því fjárhagsvíddargildi.</span><span class="sxs-lookup"><span data-stu-id="7815b-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="7815b-140">Í reitnum **Lýsing** skal færa inn lýsingu sem lýsir fjárhagsvíddargildi.</span><span class="sxs-lookup"><span data-stu-id="7815b-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
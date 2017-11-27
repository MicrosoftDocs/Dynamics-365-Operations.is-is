---
title: "Fjárhagsvíddir"
description: "Þessi efnisgrein lýsir ýmsum gerðum fjárhagsvídda og hvernig þær eru settar upp."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 274a5e696bfde4f5e27bc186fadbab69f5fc655d
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="financial-dimensions"></a><span data-ttu-id="b7245-103">Fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="b7245-103">Financial dimensions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b7245-104">Þessi efnisgrein útskýrir ýmsar gerðir fjárhagsvídda og hvernig þær eru settar upp.</span><span class="sxs-lookup"><span data-stu-id="b7245-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="b7245-105">Nota skal skjámyndina **Fjárhagsvíddir** til að stofna fjárhagsvíddir sem nota má sem hluta lykils fyrir bókhaldslykla.</span><span class="sxs-lookup"><span data-stu-id="b7245-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="b7245-106">Til eru tvær gerðir fjárhagsvídda: sérsniðnar víddir og afritaðar víddir.</span><span class="sxs-lookup"><span data-stu-id="b7245-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="b7245-107">Sérsniðnar víddir eru samnýttar á milli lögaðila og gildi eru færð inn og þeim stjórnað af notendum.</span><span class="sxs-lookup"><span data-stu-id="b7245-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="b7245-108">Fyrir afritaðar víddir eru víddir hvers gildis skilgreindar annars staðar í kerfinu, eins og Viðskiptavinum eða Verslunum.</span><span class="sxs-lookup"><span data-stu-id="b7245-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="b7245-109">Sumar afritaðar víddir eru samnýttar á milli lögaðila, en aðrar afritaðar víddir eru bundnar fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="b7245-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="b7245-110">Eftir að búið er að stofna fjárhagsvíddir skal nota síðuna **Fjárhagsvíddargildi** til að úthluta fleiri eiginleikum fyrir hverja fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="b7245-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="b7245-111">Hægt er að nota fjárhagsvíddir til að tákna lögaðila.</span><span class="sxs-lookup"><span data-stu-id="b7245-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="b7245-112">Ekki þarf að stofna á lögaðila í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="b7245-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="b7245-113">Hins vegar eru kostnaðarjafnaðar fjárhagsvíddir ekki hannaðar til að taka á rekstrar- eða viðskiptaþörfum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="b7245-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="b7245-114">Eiginlekin millieiningabókhalds í Finance and Operations er hannaður til að eiga aðeins við bókhaldsfærslur sem eru stofnaðar fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="b7245-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="b7245-115">Áður en fjárhagsvíddir eru settar upp sem lögaðilar skal meta viðskiptaferli á eftirfarandi svæðum til að ákvarða hvort þessi uppsetning muni gagnast fyrirtækinu:</span><span class="sxs-lookup"><span data-stu-id="b7245-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="b7245-116">Birgðir</span><span class="sxs-lookup"><span data-stu-id="b7245-116">Inventory</span></span>
- <span data-ttu-id="b7245-117">Sölu og innkaup milli fjárhagsvíddir og lögaðila</span><span class="sxs-lookup"><span data-stu-id="b7245-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="b7245-118">útreikningur VSK og skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="b7245-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="b7245-119">Aðgerðaskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="b7245-119">Operational reporting</span></span>

<span data-ttu-id="b7245-120">Hér eru sumar af skorðunum:</span><span class="sxs-lookup"><span data-stu-id="b7245-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="b7245-121">Hægt er að nota virkni virðisaukaskatts ekki með fjárhagsvíddum, aðeins við lögaðila.</span><span class="sxs-lookup"><span data-stu-id="b7245-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="b7245-122">Sumar skýrslur innihalda ekki fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="b7245-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="b7245-123">Þar af leiðandi gæti þurft að breyta skýrslunum til að gera skýrslu eftir fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="b7245-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="b7245-124">Sérsniðnar víddir</span><span class="sxs-lookup"><span data-stu-id="b7245-124">Custom dimensions</span></span>

<span data-ttu-id="b7245-125">Til að stofna notandaskilgreinda fjárhagsvídd er í reitnum **Nota gildi frá** valin **&lt; Sérsniðin vídd &gt;**.</span><span class="sxs-lookup"><span data-stu-id="b7245-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="b7245-126">Einnig er hægt að tilgreina lykilsíu til að takmarka magn og gerð upplýsinga sem hægt er að færa inn víddargildi fyrir.</span><span class="sxs-lookup"><span data-stu-id="b7245-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="b7245-127">Hægt er að færa inn stafi sem eru þeir sömu og fyrir hvert víddargildi eins og stafi eða bandstrik (-).</span><span class="sxs-lookup"><span data-stu-id="b7245-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="b7245-128">Einnig er hægt að slá inn tölumerki (\#) og og-merki (&) sem frátakara fyrir stafi og tölur sem breytast í hvert skipti sem víddargildi er stofnað.</span><span class="sxs-lookup"><span data-stu-id="b7245-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="b7245-129">Notaðu tölumerki (\#) sem frátakara fyrir tölu og og-merki (&) sem frátakara fyrir staf.</span><span class="sxs-lookup"><span data-stu-id="b7245-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="b7245-130">Reiturinn fyrir sniðsíuna er aðeins tiltækur þegar valið er **&lt; Sérsniðin vídd &gt;** í reitnum **Nota gildi frá**.</span><span class="sxs-lookup"><span data-stu-id="b7245-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="b7245-131">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="b7245-131">**Example**</span></span>

<span data-ttu-id="b7245-132">Til að takmarka víddargildi við stafina „CC“ og þrjár tölur færirðu inn **CC-\#\#\#** sem sniðsíu.</span><span class="sxs-lookup"><span data-stu-id="b7245-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="b7245-133">Einingastuddar víddir</span><span class="sxs-lookup"><span data-stu-id="b7245-133">Entity-backed dimensions</span></span>

<span data-ttu-id="b7245-134">Að búa til einingastuddar fjárhagsvíddir skal í svæðinu **Nota gildi frá** velja kerfisskilgreindar einingar til að byggja fjárhagsvídd á.</span><span class="sxs-lookup"><span data-stu-id="b7245-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="b7245-135">Fjárhagsvíddargildi eru síðan stofnuð úr þeirri einingu.</span><span class="sxs-lookup"><span data-stu-id="b7245-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="b7245-136">Til dæmis skal velja Verk til að stofna víddargildi fyrir **Verk**.</span><span class="sxs-lookup"><span data-stu-id="b7245-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="b7245-137">Víddargildi eru síðan stofnuð fyrir hvert heiti verks.</span><span class="sxs-lookup"><span data-stu-id="b7245-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="b7245-138">Síðan **Fjárhagsvíddargildi** sýna gildi fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="b7245-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="b7245-139">Ef þessi gildi eru bundin tilteknu fyrirtæki sýnir síðan einnig fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="b7245-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="b7245-140">Notkun vídda</span><span class="sxs-lookup"><span data-stu-id="b7245-140">Activating dimensions</span></span>

<span data-ttu-id="b7245-141">Þegar fjárhagsvídd er virkjuð er taflan uppfærð þannig að hún felur í sér heiti fjárhagsvíddarinnar.</span><span class="sxs-lookup"><span data-stu-id="b7245-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="b7245-142">Eyddar víddir eru fjarlægðar.</span><span class="sxs-lookup"><span data-stu-id="b7245-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="b7245-143">Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð.</span><span class="sxs-lookup"><span data-stu-id="b7245-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="b7245-144">Hins vegar er ekki hægt að nota fjárhagsvídd neins staðar fyrri en hún er gerð virk.</span><span class="sxs-lookup"><span data-stu-id="b7245-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="b7245-145">Til dæmis er ekki hægt að bæta fjárhagsvídd við lykilskipulag þar til að fjárhagsvídd hefur verið virkjuð.</span><span class="sxs-lookup"><span data-stu-id="b7245-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="b7245-146">Þegar smellt er á **Virkja** eru allar víddir uppfærðar og sýna stöðu breytingar.</span><span class="sxs-lookup"><span data-stu-id="b7245-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="b7245-147">Þýðingar</span><span class="sxs-lookup"><span data-stu-id="b7245-147">Translations</span></span>

<span data-ttu-id="b7245-148">Á síðunni **Textaþýðing** er hægt að færa inn texta fyrir valda fjárhagsvídd á mismunandi tungumálum.</span><span class="sxs-lookup"><span data-stu-id="b7245-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="b7245-149">Á síðunni **Þýðing aðallykils** er hægt að færa inn texta fyrir aðallykil á mismunandi tungumálum.</span><span class="sxs-lookup"><span data-stu-id="b7245-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="b7245-150">Lögaðili hnekkir</span><span class="sxs-lookup"><span data-stu-id="b7245-150">Legal entity overrides</span></span>

<span data-ttu-id="b7245-151">Ekki eru allar víddir gildar fyrir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="b7245-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="b7245-152">Þar að auki kunna sumar víddir að vera aðeins viðeigandi fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="b7245-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="b7245-153">Í þessum tilfellum er hægt að nota hlutann **Lögaðili hnekkir** til að tilgreina hvaða fyrirtæki ætti ekki að nota víddir fyrir, hver er eigandi og tímabilið sem víddin er virk.</span><span class="sxs-lookup"><span data-stu-id="b7245-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="b7245-154">Eyðing fjárhagsvídda</span><span class="sxs-lookup"><span data-stu-id="b7245-154">Deleting financial dimensions</span></span>

<span data-ttu-id="b7245-155">Til að viðhalda heilleika gagna er sjaldan hægt að eyða fjárhagsvíddum.</span><span class="sxs-lookup"><span data-stu-id="b7245-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="b7245-156">Ef reynt er að eyða fjárhagsvíddum eru eftirfarandi skilyrði metin:</span><span class="sxs-lookup"><span data-stu-id="b7245-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="b7245-157">Hefur fjárhagsvíddin verið notuð á einhverjar bókaðar eða óbókaðar færslur eða einhverja gerð af víddarsamsetningu gilda?</span><span class="sxs-lookup"><span data-stu-id="b7245-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="b7245-158">Er fjárhagsvíddin notuð í öllu virku lykilskipulagi, ítarleg reglu skipulag fjárhagsvídd eða fjárhagsvídd set?</span><span class="sxs-lookup"><span data-stu-id="b7245-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="b7245-159">Er fjárhagsvídd hluti af sjálfgefinu samþættingarsniði fjárhagsvíddar?</span><span class="sxs-lookup"><span data-stu-id="b7245-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="b7245-160">Hefur fjárhagsvídd verið uppsett sem sjálfgefin vídd?</span><span class="sxs-lookup"><span data-stu-id="b7245-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="b7245-161">Ef einhverjum skilyrðum er mætt er ekki hægt að eyða fjárhagsvíddinni.</span><span class="sxs-lookup"><span data-stu-id="b7245-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="b7245-162">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="b7245-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="b7245-163">Skilgreina fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="b7245-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="b7245-164">Viðhalda sjálfgefnum sniðmátum fjárhagsvídda</span><span class="sxs-lookup"><span data-stu-id="b7245-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)


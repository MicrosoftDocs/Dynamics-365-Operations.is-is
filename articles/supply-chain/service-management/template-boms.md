---
title: "Sniðmátsuppskriftir"
description: "Sniðmátsuppskrift veitir staðlaðan lista yfir íhluti fyrir þjónustuhluti sem eru reglulega þjónustaðir."
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: f9c61ecd79f38301f46e3c21a33ec2801f33d19f
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---

# <a name="template-boms"></a><span data-ttu-id="51f4e-103">Sniðmátsuppskriftir</span><span class="sxs-lookup"><span data-stu-id="51f4e-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="51f4e-104">Sniðmátsuppskrift veitir þér staðlaðan lista yfir íhluti fyrir þjónustuhluti sem eru reglulega þjónustaðir.</span><span class="sxs-lookup"><span data-stu-id="51f4e-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="51f4e-105">Íhlutirnir sem eru taldir upp í sniðmátsuppskrift tákna einstaka undiríhluti þjónustuhlutarins.</span><span class="sxs-lookup"><span data-stu-id="51f4e-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="51f4e-106">Með því að nota sniðmátsuppskrift fyrir þjónustuhlut er hægt að halda skrá yfir þá undiríhluti sem hefur verið skipt út á þjónustuhlutnum.</span><span class="sxs-lookup"><span data-stu-id="51f4e-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="51f4e-107">Til þess að nota sniðmátsuppskrift í þjónustusamningi eða þjónustupöntun er hún tengd við þjónustuhlutatengsl.</span><span class="sxs-lookup"><span data-stu-id="51f4e-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="51f4e-108">Þú getur aðeins notað eina sniðmátsuppskrift á þjónustuhlut.</span><span class="sxs-lookup"><span data-stu-id="51f4e-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="51f4e-109">Stofna sniðmátsuppskrift</span><span class="sxs-lookup"><span data-stu-id="51f4e-109">Create a template BOM</span></span>

<span data-ttu-id="51f4e-110">Eftirfarandi tafla inniheldur upplýsingar um hinar ýmsu aðferðir sem hægt er að nota til að stofna sniðmátsuppskrift.</span><span class="sxs-lookup"><span data-stu-id="51f4e-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51f4e-111">Aðferð</span><span class="sxs-lookup"><span data-stu-id="51f4e-111">Method</span></span></p></th>
<th><p><span data-ttu-id="51f4e-112">lýsing</span><span class="sxs-lookup"><span data-stu-id="51f4e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51f4e-113">Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="51f4e-113">Production</span></span></p></td>
<td><p><span data-ttu-id="51f4e-114">Sniðmátsuppskriftin byggist á framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="51f4e-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="51f4e-115">Þessi valkostur á aðeins við ef þú starfar í vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="51f4e-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="51f4e-116">Kostirnir eru þeir að notandinn fær gildandi og ítarlegan lista yfir íhlutina sem eru í tiltekinni vöru.</span><span class="sxs-lookup"><span data-stu-id="51f4e-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51f4e-117">Vara BOM</span><span class="sxs-lookup"><span data-stu-id="51f4e-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="51f4e-118">Sniðmátsuppskrift er byggð á uppskriftarvöru.</span><span class="sxs-lookup"><span data-stu-id="51f4e-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="51f4e-119">Uppskriftarvaran, ólíkt framleiðsluuppskrift, er fastur listi yfir þá íhluti sem gera vöru.</span><span class="sxs-lookup"><span data-stu-id="51f4e-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51f4e-120">Fyrirliggjandi sniðmát</span><span class="sxs-lookup"><span data-stu-id="51f4e-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="51f4e-121">Sniðmátið er byggt á fyrirliggjandi sniðmátsuppskrift.</span><span class="sxs-lookup"><span data-stu-id="51f4e-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51f4e-122">Beinskiptur</span><span class="sxs-lookup"><span data-stu-id="51f4e-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="51f4e-123">Ef þú veist hvaða varahlutum er venjulega skipt út á þjónustuhlut getur þú stofnað sniðmátsuppskriftina þína handvirkt.</span><span class="sxs-lookup"><span data-stu-id="51f4e-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="51f4e-124">Þessi aðferð hjálpar til við að ganga úr skugga um að íhlutirnir sem eru hluti af sniðmátinu endurspegli raunverulegar kröfur vinnustaðarins.</span><span class="sxs-lookup"><span data-stu-id="51f4e-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="51f4e-125">Notaðu sniðmátsuppskriftina í þjónustusamning eða þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="51f4e-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="51f4e-126">Þú getur notað sniðmátsuppskrift í þjónustusamning, þjónustupöntun eða bæði.</span><span class="sxs-lookup"><span data-stu-id="51f4e-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="51f4e-127">Þjónustusamningurinn felur yfirleitt í sér langtímasamband við viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="51f4e-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="51f4e-128">Endurnýjunarsagan sem skráð er í þjónustuuppskriftnni eru gagnlegar upplýsingar fyrir þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="51f4e-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="51f4e-129">Þú getur einnig nota sniðmátsuppskrift í þjónustupöntun til að skrá sögu þjónustunnar sem hefur verið framkvæmd á þjónustuhlut.</span><span class="sxs-lookup"><span data-stu-id="51f4e-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="51f4e-130">Afrita sögu þjónustuuppskriftar</span><span class="sxs-lookup"><span data-stu-id="51f4e-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="51f4e-131">Þú getur afritað sögu þjónustuuppskriftarlínu frá einum þjónustusamningi til annars.</span><span class="sxs-lookup"><span data-stu-id="51f4e-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="51f4e-132">Með því að afrita þjónustusöguna milli þjónustusamninga geturðu varðveitt skrárnar yfir útskipti fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="51f4e-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="51f4e-133">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="51f4e-133">**Example**</span></span>

<span data-ttu-id="51f4e-134">Settur hefur verið upp þriggja ára þjónustusamningur fyrir bíl viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="51f4e-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="51f4e-135">Á því tímabili verður viðskiptavinurinn vanur þeirri góðu þjónustu sem fyrirtækið veitir.</span><span class="sxs-lookup"><span data-stu-id="51f4e-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="51f4e-136">Þess vegna, eftir að samningurinn rennur út, vill viðskiptavinurinn setja upp nýjan.</span><span class="sxs-lookup"><span data-stu-id="51f4e-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="51f4e-137">Þá er mögulegt að semja um hagstæðari kjör fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="51f4e-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="51f4e-138">Vegna þess að skráin yfir skipta íhluti gæti verið gagnleg í framtíðinni, afritar þú sögu þjónustuuppskriftar í nýja samninginn.</span><span class="sxs-lookup"><span data-stu-id="51f4e-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="51f4e-139">Breyta sniðmátsuppskrift</span><span class="sxs-lookup"><span data-stu-id="51f4e-139">Modify the template BOM</span></span>

<span data-ttu-id="51f4e-140">Ef sniðmátsuppskrift hefur ekki verið tengt við þjónustuhlut geturðu breytt eða eytt línum í henni.</span><span class="sxs-lookup"><span data-stu-id="51f4e-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="51f4e-141">Eftir að sniðmátsuppskrift er tengd við þjónustuhlut geturðu aðeins breytt staðbundinni útgáfu af uppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="51f4e-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="51f4e-142">Ef ætlunin er að tvítaka uppsetningu staðbundinnar útgáfu af sniðmátsuppskrift er hægt að stofna nýja sniðmátsuppskrift, byggða á staðbundnu útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="51f4e-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="51f4e-143">Nánari upplýsingar er að finna í [Breyta þjónustuuppskrift](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="51f4e-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="51f4e-144">Ef þú skiptir út vöru í uppskriftinni getur þú skráð skiptin á uppskriftarlínu í uppskriftarhönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="51f4e-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="51f4e-145">Valfrjálst er hægt að búa til þjónustupöntunarlínu fyrir skipta hlutinn.</span><span class="sxs-lookup"><span data-stu-id="51f4e-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="51f4e-146">Ef þú býrð til þjónustupöntunarlínu geturðu reikningsfært vöruna sem kom í staðinn.</span><span class="sxs-lookup"><span data-stu-id="51f4e-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="51f4e-147">Ef þú býrð ekki til þjónustupöntunarlínu fyrir skipti er skráningin á skiptunum geymd til að fylgjast með sögu þjónustuhlutarins.</span><span class="sxs-lookup"><span data-stu-id="51f4e-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="51f4e-148">Breyttu hvernig upplýsingar á uppskriftarlínunni birtast</span><span class="sxs-lookup"><span data-stu-id="51f4e-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="51f4e-149">Þú getur breytt því hvernig upplýsingar á uppskriftarlínunni birtast fyrir öll sniðmát og þjónustuuppskriftir.</span><span class="sxs-lookup"><span data-stu-id="51f4e-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="51f4e-150">Breytingarnar eru gerðar á öllum sniðmátsuppskriftum og þjónustuuppskriftum.</span><span class="sxs-lookup"><span data-stu-id="51f4e-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="51f4e-151">Þetta á við um þær sem eru tengdar við þjónustuhluti.</span><span class="sxs-lookup"><span data-stu-id="51f4e-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="51f4e-152">Setja upp númeraraðir fyrir sniðmátsuppskriftir</span><span class="sxs-lookup"><span data-stu-id="51f4e-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="51f4e-153">Til að nota sniðmátuppskriftir verður þú að setja upp tvær númeraraðir.</span><span class="sxs-lookup"><span data-stu-id="51f4e-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="51f4e-154">Settu upp eina númeraröð fyrir sniðmátsuppskriftina og eina fyrir línunúmer uppskriftarsögunnar.</span><span class="sxs-lookup"><span data-stu-id="51f4e-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="51f4e-155">Númeraraðir eru notaðar til að úthluta auðkennum til skráa sem þarfnast þeirra.</span><span class="sxs-lookup"><span data-stu-id="51f4e-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="51f4e-156">Áður en þú getur úthlutar númeraröð til sniðmátsuppskriftar eða línunúmer uppskriftarsögu verður þú að setja upp kóða númeraraða.</span><span class="sxs-lookup"><span data-stu-id="51f4e-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="51f4e-157">Setja upp númeraraðir</span><span class="sxs-lookup"><span data-stu-id="51f4e-157">Set up number sequences</span></span>

1.  <span data-ttu-id="51f4e-158">Á listasíðunni **Númeraraðir** skaltu stofna númeraraðir fyrir sniðmátsuppskriftir og línunúmer uppskriftarsögu.</span><span class="sxs-lookup"><span data-stu-id="51f4e-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="51f4e-159">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Færibreytur þjónustustjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="51f4e-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="51f4e-160">Smelltu á **Númeraraðir** og veldu síðan kóða númeraraðar fyrir tilvísanir númeraraðarinnar sem þú stofnaðir í skjámyndinni **Númeraraðir**.</span><span class="sxs-lookup"><span data-stu-id="51f4e-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="51f4e-161">Skjámyndinni er lokað til að vista breytingar.</span><span class="sxs-lookup"><span data-stu-id="51f4e-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="51f4e-162">Línunúmer uppskriftarsögunnar er notað af kerfinu til að tengja færslur í uppskrfitarsögunni við þjónustusamning eða þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="51f4e-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="51f4e-163">Númerið birtist ekki í notendaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="51f4e-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="51f4e-164">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="51f4e-164">See also</span></span>

[<span data-ttu-id="51f4e-165">Stofna sniðmátsuppskrift</span><span class="sxs-lookup"><span data-stu-id="51f4e-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="51f4e-166">Stjórna sniðmátsuppskriftum í tengslum hluta</span><span class="sxs-lookup"><span data-stu-id="51f4e-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="51f4e-167">Breyta þjónustuuppskrift</span><span class="sxs-lookup"><span data-stu-id="51f4e-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 




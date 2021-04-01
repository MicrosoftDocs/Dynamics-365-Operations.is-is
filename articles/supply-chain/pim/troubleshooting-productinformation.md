---
title: Úrræðaleit fyrir afurðarupplýsingar
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með afurðarupplýsingar.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a9db8e0081a0d47ec8d74680fe99a0934b99bb5c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223363"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="6832f-103">Úrræðaleit fyrir afurðarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="6832f-103">Troubleshoot product information</span></span>

<span data-ttu-id="6832f-104">Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með afurðarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="6832f-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="6832f-105">Ekki er hægt að eyða losaðri afurð.</span><span class="sxs-lookup"><span data-stu-id="6832f-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6832f-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6832f-106">Issue description</span></span>

<span data-ttu-id="6832f-107">Hægt er að eyða útgefinni afurð og öllum afbrigðum hennar aðeins ef útgefna afurðin er ekki með neinar tengdar færslur.</span><span class="sxs-lookup"><span data-stu-id="6832f-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6832f-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6832f-108">Issue resolution</span></span>

<span data-ttu-id="6832f-109">Fylgið eftirfarandi skrefum til að eyða útgefinni afurð eða afurðarsniðmáti.</span><span class="sxs-lookup"><span data-stu-id="6832f-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="6832f-110">Loka öllum opnum færslum fyrir vörurnar.</span><span class="sxs-lookup"><span data-stu-id="6832f-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="6832f-111">Minnka birgðir í 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="6832f-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="6832f-112">Framkvæma birgðalokun.</span><span class="sxs-lookup"><span data-stu-id="6832f-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="6832f-113">Eyða öllum afurðarafbrigðum fyrir afurðarsniðmát sem á að eyða.</span><span class="sxs-lookup"><span data-stu-id="6832f-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="6832f-114">Get ég breytt vörunúmeri útgefinnar afurðar?</span><span class="sxs-lookup"><span data-stu-id="6832f-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="6832f-115">Í flestum tilfellum er ekki hægt að breyta vörunúmerum fyrir útgefnar afurðir vegna þess að slík breyting veldur því að gögn skemmist.</span><span class="sxs-lookup"><span data-stu-id="6832f-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="6832f-116">Aðeins er hægt að breyta vörunúmeri ef nauðsynlegt er að gera við skemmd gögn sem fyrri endurnefning á aðallykli olli þeirri útgefnu afurð eins og minnst er á í listanum yfir [fjarlægðir eða úreltir eiginleikar fyrir Finance and Operations 10.0.0 með verkvangsuppfærslu 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="6832f-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="6832f-117">Ef ætlunin er að breyta vörunúmerum fyrir útgefnar afurðir er hægt að [kjósa um þessa hugmynd í hugmyndagáttinni](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="6832f-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="6832f-118">Sjálfgefna losunarreglan úr afurðinni er ekki færð inn í uppskriftarlínuna.</span><span class="sxs-lookup"><span data-stu-id="6832f-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6832f-119">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6832f-119">Issue description</span></span>

<span data-ttu-id="6832f-120">Þegar vöru er bætt við uppskriftarlínu notar kerfið ekki sjálfgefnar upplýsingar um losunarreglu sem er sett upp fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="6832f-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="6832f-121">Með öðrum orðum birtist losunarregla afurðarinnar ekki á síðunni **Uppskriftarlína**.</span><span class="sxs-lookup"><span data-stu-id="6832f-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6832f-122">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6832f-122">Issue resolution</span></span>

<span data-ttu-id="6832f-123">Ef losunarregla er tilgreind í uppskriftarlínu, á hún við um þá uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="6832f-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="6832f-124">Ef losunarreglan er hinsvegar auð, eða hún er ekki sett upp í uppskriftarlínu, mun losunarreglan sem er stillt fyrir vöruna samt eiga við þá uppskriftarlínu, jafnvel þótt hún sjáist ekki í uppskriftarlínunni.</span><span class="sxs-lookup"><span data-stu-id="6832f-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="6832f-125">Sjálfgefin reikniregla fyrir aðra eiginleika í Microsoft Dynamics 365 Supply Chain Management virkar yfirleitt ekki á þennan hátt.</span><span class="sxs-lookup"><span data-stu-id="6832f-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="6832f-126">Hins vegar er ekki hægt að breyta núverandi hegðun.</span><span class="sxs-lookup"><span data-stu-id="6832f-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="6832f-127">Annars gætu sumar fyrirliggjandi sérstillingar sem reiða sig á hana verið í ólagi.</span><span class="sxs-lookup"><span data-stu-id="6832f-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="6832f-128">Kerfið gerir mér kleift að vista tvítekin strikamerki fyrir mismunandi vörur eða sömu vöruna sem er með aðrar víddir.</span><span class="sxs-lookup"><span data-stu-id="6832f-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="6832f-129">Sem stendur framfylgir kerfið ekki einkvæmum strikamerkjum og viðbót þessarar takmörkunar myndi leiða til bilunar.</span><span class="sxs-lookup"><span data-stu-id="6832f-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="6832f-130">Í reynd hefur Microsoft sannanir fyrir því að sumar núverandi uppsetningar viðskiptavinar myndu verða skemmast með þessari breytingu.</span><span class="sxs-lookup"><span data-stu-id="6832f-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="6832f-131">Við munum hinsvegar íhuga víðtækari hönnunarbreytingu til að virkja þennan eiginleika í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="6832f-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="6832f-132">Ég fæ eftirfarandi villuboð: „Ekki er hægt að stofna staðsetningu vöruhúss vegna þess að varan er ekki á lager“.</span><span class="sxs-lookup"><span data-stu-id="6832f-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="6832f-133">Velja skal framleiðsluvalkostinn Í birgðum í tengdum líkanaflokki ef ætlunin er að setja vörurnar í birgðir.</span><span class="sxs-lookup"><span data-stu-id="6832f-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6832f-134">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6832f-134">Issue description</span></span>

<span data-ttu-id="6832f-135">Þetta vandamál á sér stað ef eftirfarandi skrefum er fylgt til að reyna að búa til sniðmát fyrir vöru sem ekki er í birgðum.</span><span class="sxs-lookup"><span data-stu-id="6832f-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="6832f-136">Opnið útgefna afurð sem er ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="6832f-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="6832f-137">Á aðgerðasvæðinu, í flipanum **Valkostir**, skal velja **Upplýsingar um færslu**.</span><span class="sxs-lookup"><span data-stu-id="6832f-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="6832f-138">Í svarglugganum **Upplýsingar um færslu** skal velja **Sniðmát fyrirtækjareikninga**.</span><span class="sxs-lookup"><span data-stu-id="6832f-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="6832f-139">Eftirfarandi villuboð birtast í þessu tilvikum:</span><span class="sxs-lookup"><span data-stu-id="6832f-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="6832f-140">Ekki er hægt að stofna staðsetningu vöruhúss vegna þess að varan er ekki á lager.</span><span class="sxs-lookup"><span data-stu-id="6832f-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="6832f-141">Velja skal framleiðsluvalkostinn Í birgðum í tengdum líkanaflokki ef ætlunin er að setja vörurnar í birgðir.</span><span class="sxs-lookup"><span data-stu-id="6832f-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6832f-142">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6832f-142">Issue resolution</span></span>

<span data-ttu-id="6832f-143">Ferlið við stofnun afurðasniðmáts krefst sérstakrar reiknireglu sem miðast við afurð.</span><span class="sxs-lookup"><span data-stu-id="6832f-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="6832f-144">Þess vegna er ekki hægt að nota almenna hnappinn **Sniðmát fyrirtækjareikninga** í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="6832f-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="6832f-145">Fylgdu þess í stað eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="6832f-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="6832f-146">Opna útgefna afurð.</span><span class="sxs-lookup"><span data-stu-id="6832f-146">Open a released product.</span></span>
1. <span data-ttu-id="6832f-147">Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Nýtt**, skal velja **Sniðmát \> Stofna samnýtt sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="6832f-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="6832f-148">Sjálfgefnum hjálpartexta sem er bætt við í afurðareigindir er ekki færður í útgefna afurð.</span><span class="sxs-lookup"><span data-stu-id="6832f-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="6832f-149">Lýsing og hjálpartexti sem bætt er við afurðareigindir eru ekki sýnilegir eða sjálfgefið færðir inn í útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="6832f-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="6832f-150">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="6832f-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="6832f-151">Sjálfgefið magn sem fært er inn er frábrugðið þegar það er skráð úr uppskrift og þegar það er skráð úr uppskriftarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="6832f-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6832f-152">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6832f-152">Issue description</span></span>

<span data-ttu-id="6832f-153">Að sjálfgefnu, þegar vöru er bætt við uppskrift er magnið stillt á 1 í stað þess magns sem er skilgreint í reitnum **Lágmarks pöntunarmagn** á síðunni **Sjálfgefnar pöntunarstillingar** fyrir valda afurð.</span><span class="sxs-lookup"><span data-stu-id="6832f-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="6832f-154">Þegar vöru er hinsvegar bætt við úr uppskriftarútgáfu og varan og afbrigðið er valið, tekur magnið sem er sjálfgefið fært inn með í reikninginn lágmarksmagnið sem er stillt í sjálfgefnum pöntunarstillingum fyrir tilteknar víddir.</span><span class="sxs-lookup"><span data-stu-id="6832f-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6832f-155">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6832f-155">Issue resolution</span></span>

<span data-ttu-id="6832f-156">Búist er við þessari hegðun.</span><span class="sxs-lookup"><span data-stu-id="6832f-156">This behavior is expected.</span></span> <span data-ttu-id="6832f-157">Sú staðreynd að reiknireglan sé ólík uppskriftinni og uppskriftarútgáfunni er hinsvegar þekkt vandamál.</span><span class="sxs-lookup"><span data-stu-id="6832f-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="6832f-158">Þessari hegðun verður samt sem áður ekki breytt vegna þess að breyting gæti haft áhrif á margar ólíkar aðstæður viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="6832f-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="6832f-159">Í upplýsingum um útgefna afurð get ég ekki breytt viðhengdum myndum sem hlaðið var upp úr gagnaeiningu fyrir viðhengi afurðarskjala.</span><span class="sxs-lookup"><span data-stu-id="6832f-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6832f-160">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6832f-160">Issue description</span></span>

<span data-ttu-id="6832f-161">Þetta vandamál getur komið upp þegar mynd er hengd við vöru með því að nota gagnaeininguna *Viðhengd skjöl afurða*.</span><span class="sxs-lookup"><span data-stu-id="6832f-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="6832f-162">Í þessu tilviki er vörumyndin sýnd fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="6832f-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="6832f-163">Ef þú velur hinsvegar **Breyta mynd** verður ekkert sýnt í listanum yfir myndir sem hlaðnar eru upp.</span><span class="sxs-lookup"><span data-stu-id="6832f-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="6832f-164">Auk þess eru engin viðhengi sýnd fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="6832f-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6832f-165">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6832f-165">Issue resolution</span></span>

<span data-ttu-id="6832f-166">Einingin *EcoResProductDocumentAttachmentEntity* (*Viðhengd skjöl afurða*) flytur inn viðhengd skjöl fyrir *afurðir* en ekki fyrir *útgefnar afurðir*.</span><span class="sxs-lookup"><span data-stu-id="6832f-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="6832f-167">(Útgefnar afurðir eru einnig þekktar sem *vörur*.) Til að skoða viðhengi fyrir vöru á síðunni **Upplýsingar um losaðar afurðir** þarf að nota eininguna *EcoResReleasedProductDocumentAttachmentEntity* (*Viðhengd skjöl fyrir útgefnar afurðir*) í staðinn.</span><span class="sxs-lookup"><span data-stu-id="6832f-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="6832f-168">Tengillinn Microsoft Flow sýnir eftirfarandi villuboð: „Uppfærsla ekki leyfð fyrir reit „ProductNumber“.</span><span class="sxs-lookup"><span data-stu-id="6832f-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6832f-169">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6832f-169">Issue description</span></span>

<span data-ttu-id="6832f-170">Þetta vandamál á sér stað ef reynt er að uppfæra reitinn **Afurðarnúmer** með því að nota V2 eininguna *Útgefnar afurðir* og Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="6832f-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6832f-171">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6832f-171">Issue resolution</span></span>

<span data-ttu-id="6832f-172">Búist er við þessari hegðun.</span><span class="sxs-lookup"><span data-stu-id="6832f-172">This behavior is expected.</span></span> <span data-ttu-id="6832f-173">Möguleikinn á að breyta afurðarnúmerinu fyrir útgefna afurð var fjarlægður í Dynamics 365 Finance and Operations 10.0.0 með verkvangsuppfærslu 24 til að hjálpa til við að koma í veg fyrir skemmdir á gögnum.</span><span class="sxs-lookup"><span data-stu-id="6832f-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="6832f-174">Í undantekningartilfellum, þar sem nauðsynlegt er að lagfæra gagnaskemmdir sem voru gerðar af fyrri endurnefningu á aðallykli útgefinnar afurðar, geturðu beðið notendaþjónustu Microsoft um að fjarlægja takmörkunina tímabundið.</span><span class="sxs-lookup"><span data-stu-id="6832f-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="6832f-175">Ég get ekki stofnað útgefið afurðarafbrigði í öðrum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6832f-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6832f-176">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6832f-176">Issue description</span></span>

<span data-ttu-id="6832f-177">Ef reynt er að gefa út afurðarsniðmát án afbrigða og síðan stofna afbrigðin í hverjum lögaðila (fyrirtæki) fyrir sig eins og þarf að gera, þá geturðu ekki gefið út afbrigðin með því að nota uppástungur um afbrigði.</span><span class="sxs-lookup"><span data-stu-id="6832f-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="6832f-178">Einnig verður ekki hægt að stofna afbrigðin handvirkt.</span><span class="sxs-lookup"><span data-stu-id="6832f-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6832f-179">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6832f-179">Issue resolution</span></span>

<span data-ttu-id="6832f-180">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="6832f-180">This behavior is by design.</span></span> <span data-ttu-id="6832f-181">Tengsl afurðarsniðmáts og víddanna sem sniðmátið getur tekið eru geymdar á samnýttu stigi.</span><span class="sxs-lookup"><span data-stu-id="6832f-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="6832f-182">Þess vegna er ekki hægt að stofna tiltækar víddir fyrir samnýtt afurðarsniðmát í tilteknum lögaðila þar sem þessar víddir eru gefnar út og síðan endurtaka ferlið í hverjum lögaðila fyrir sig þar sem víddirnar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="6832f-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="6832f-183">Þess í stað þarftu að breyta útgáfuferlinu til að aðlagast hönnunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="6832f-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="6832f-184">Hér er ferlið fyrir losun afurða.</span><span class="sxs-lookup"><span data-stu-id="6832f-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="6832f-185">Stofnið samnýtt afurðarsniðmát og víddirnar sem hægt er að gefa út í lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="6832f-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="6832f-186">Losið afurðirnar í lögaðilana annaðhvort með því að nota uppástungur um afbrigði eða bæta samsetningum handvirkt við sem á að losa.</span><span class="sxs-lookup"><span data-stu-id="6832f-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="6832f-187">Að öðrum kosti er hægt að stofna útgefna afurð með beinum hætti.</span><span class="sxs-lookup"><span data-stu-id="6832f-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="6832f-188">Þegar ég sleppi losa afbrigði í öðru fyrirtæki fæ ég eftirfarandi villuboð: „Afurðarafbrigði hefur þegar verið stofnað með tilgreindri vídd“.</span><span class="sxs-lookup"><span data-stu-id="6832f-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6832f-189">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6832f-189">Issue description</span></span>

<span data-ttu-id="6832f-190">Ef afurðarafbrigði hefur þegar verið losað í fyrirtæki A, og reynt er að losa það í fyrirtæki B með því að nota hnappinn **Nýtt** á síðunni **Útgefin afurðarafbrigði** koma upp eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="6832f-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="6832f-191">Afurðarafbrigði hefur þegar verið stofnað með tilgreindri vídd.</span><span class="sxs-lookup"><span data-stu-id="6832f-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6832f-192">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6832f-192">Issue resolution</span></span>

<span data-ttu-id="6832f-193">Hnappurinn **Nýtt** á síðunni **Útgefin afurðarafbrigði** stofnar afbrigðið og losar það í samhengi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="6832f-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="6832f-194">Ef afbrigðið hefur þegar verið stofnað er ekki hægt að nota hnappinn **Nýtt** til að losa það í annað fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="6832f-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="6832f-195">Til að laga vandamálið skal opna síðuna **Afurðarsniðmát** og velja **Losa afurð** til að losa fyrirliggjandi afbrigði í æskilegt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="6832f-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
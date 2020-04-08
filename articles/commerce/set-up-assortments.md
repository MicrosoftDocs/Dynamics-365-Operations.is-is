---
title: Setja upp vöruúrval
description: Þessi grein lýsir því hvað vöruúrval er og útskýrir hvernig á að setja upp vöruúrval í Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26614d319453041177e8072793f09f52ebfd51fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022931"
---
# <a name="set-up-assortments"></a><span data-ttu-id="215a2-103">Setja upp úrval</span><span class="sxs-lookup"><span data-stu-id="215a2-103">Set up assortments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="215a2-104">Þessi grein lýsir því hvað vöruúrval er og útskýrir hvernig á að setja upp vöruúrval í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="215a2-104">This article describes what an assortment is and explains how to set up assortments in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="215a2-105">Úrval er safn tengdra afurða sem úthlutað er á viðskiptarás, eins og verslun á staðnum eða netverslun.</span><span class="sxs-lookup"><span data-stu-id="215a2-105">An assortment is a collection of related products that you assign to a commerce channel, such as a brick-and-mortar store or an online store.</span></span> <span data-ttu-id="215a2-106">Notið úrval til að auðkenna vörurnar sem eru tiltækar í hverri verslun.</span><span class="sxs-lookup"><span data-stu-id="215a2-106">You use assortments to identify the products that are available in each store.</span></span> <span data-ttu-id="215a2-107">Úrval getur innihaldið tegundir afurða.</span><span class="sxs-lookup"><span data-stu-id="215a2-107">An assortment can include categories of products.</span></span> <span data-ttu-id="215a2-108">Þess vegna, Allar afurðir sem eru tengdar valinni tegund eru með í úrvalinu.</span><span class="sxs-lookup"><span data-stu-id="215a2-108">Therefore, all products that are assigned to a specific category are included in the assortment.</span></span> <span data-ttu-id="215a2-109">Úrval getur einnig innihaldið tilteknar vörur og tiltekinn afbrigði afurða.</span><span class="sxs-lookup"><span data-stu-id="215a2-109">An assortment can also include specific products and specific variants of products.</span></span> <span data-ttu-id="215a2-110">Með því að setja upp úrval er hægt að tengja þúsundum afurðir við rásir samtímis , í hvaða samsetningu sem verslununum krefjast.</span><span class="sxs-lookup"><span data-stu-id="215a2-110">By setting up an assortment, you can assign thousands of products to your channels at that same time, in any combination that your stores require.</span></span> <span data-ttu-id="215a2-111">Hægt er að setja upp eins mörg vöruúrval sem þú krefst.</span><span class="sxs-lookup"><span data-stu-id="215a2-111">You can set up as many product assortments as you require.</span></span> <span data-ttu-id="215a2-112">Hægt er að taka með hverja vöru í einni eða fleiri úrvali og hvert úrval er hægt að úthluta á einn eða fleiri rásir.</span><span class="sxs-lookup"><span data-stu-id="215a2-112">Each product can be included in one or more assortments, and each assortment can be assigned to one or more channels.</span></span> <span data-ttu-id="215a2-113">Til dæmis er geturðu skilgreint einn úrval sem inniheldur grunnsamsetningu afurða.</span><span class="sxs-lookup"><span data-stu-id="215a2-113">For example, you define one assortment that includes a base set of products.</span></span> <span data-ttu-id="215a2-114">Allar verslanir taka við þessu úrvali.</span><span class="sxs-lookup"><span data-stu-id="215a2-114">All stores receive this assortment.</span></span> <span data-ttu-id="215a2-115">Svo er er að skilgreina annað úrval sem inniheldur aðeins stóran íþróttabúnað.</span><span class="sxs-lookup"><span data-stu-id="215a2-115">You then define another assortment that includes only large sporting equipment.</span></span> <span data-ttu-id="215a2-116">Aðeins stærri verslununum þínum fá úrvalið.</span><span class="sxs-lookup"><span data-stu-id="215a2-116">Only your larger stores receive this assortment.</span></span> <span data-ttu-id="215a2-117">Eftirfarandi skýringarmynd sýnir hvernig hægt er að úthluta afurðir í úrval, og hvernig þær úrvali geta tilheyrt rásum.</span><span class="sxs-lookup"><span data-stu-id="215a2-117">The following diagram shows how products can be assigned to assortments, and how those assortments can be assigned to channels.</span></span>

![Vensl vöruúrvals](./media/assortments_relationship.gif)

## <a name="prerequisites"></a><span data-ttu-id="215a2-119">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="215a2-119">Prerequisites</span></span>

<span data-ttu-id="215a2-120">Áður en hægt er að setja upp úrval og úthluta henni til viðskiptarásar, verður að ljúka eftirfarandi verkum.</span><span class="sxs-lookup"><span data-stu-id="215a2-120">Before you can set up an assortment and assign it to a commerce channel, you must complete the following tasks.</span></span>

| <span data-ttu-id="215a2-121">Verk</span><span class="sxs-lookup"><span data-stu-id="215a2-121">Task</span></span>                              | <span data-ttu-id="215a2-122">Lýsing</span><span class="sxs-lookup"><span data-stu-id="215a2-122">Description</span></span> |
|-----------------------------------|-------------|
| <span data-ttu-id="215a2-123">Setja upp rás.</span><span class="sxs-lookup"><span data-stu-id="215a2-123">Set up a channel.</span></span>          | <span data-ttu-id="215a2-124">Rásir fela í sér verslunarhúsnæði, netverslanir og markaðstorg á netinu.</span><span class="sxs-lookup"><span data-stu-id="215a2-124">Channels represent a brick-and-mortar store, an online store, or an online marketplace.</span></span> <span data-ttu-id="215a2-125">Þú verður að setja upp að minnsta kosti eina rás og skilgreina valkosti fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="215a2-125">You must set up at least one channel and configure the options for the store.</span></span> <span data-ttu-id="215a2-126">Úrval er úthlutað á verslanir til að auðkenna vörurnar sem fylgir ákveðna verslun.</span><span class="sxs-lookup"><span data-stu-id="215a2-126">Assortments are assigned to stores to identify the products that a particular store carries.</span></span> |
| <span data-ttu-id="215a2-127">Stofna stigveldi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="215a2-127">Create an organization hierarchy.</span></span> | <span data-ttu-id="215a2-128">Eftir að setja upp viðskiptarása fyrir fyrirtækið, þarf að skilgreina stigveldi fyrirtækis sem táknar skipulag fyrirtækisins fyrir rásir.</span><span class="sxs-lookup"><span data-stu-id="215a2-128">After you set up the commerce channels for your organization, you must configure an organization hierarchy that represents the organizational structure of your channels.</span></span> <span data-ttu-id="215a2-129">Til dæmis getur stigveldi fyrirtækis verið notað fyrir úrval, áfyllingu eða skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="215a2-129">An organization hierarchy can be used for assortments, replenishment, and reporting.</span></span> <span data-ttu-id="215a2-130">Með því að bæta rásum við stigveldi fyrirtækis, geturðu úthlutað vöruúrvali á verslunarhópa.</span><span class="sxs-lookup"><span data-stu-id="215a2-130">By adding your channels to an organization hierarchy, you can assign assortments to groups of stores.</span></span> <span data-ttu-id="215a2-131">Í stað þess að úthluta úrvalinu sérstaklega á hverja verslun, úthlutarðu úrvalið á hástigs fyrirtækishnúta.</span><span class="sxs-lookup"><span data-stu-id="215a2-131">Instead of assigning the assortment individually to each store, you assign the assortment to the high-level organization node.</span></span> <span data-ttu-id="215a2-132">Svo í hvert sinn sem nýrri rás er bætt við fyrirtækishnúta á háu stigi, erfir sú rás sjálfkrafa allt úrval sem var úthlutað á fyrirtækishnút á hærra stigi.</span><span class="sxs-lookup"><span data-stu-id="215a2-132">Then, whenever a new channel is added to the high-level organization node, that channel automatically inherits any assortments that were assigned to the higher-level organization node.</span></span> <span data-ttu-id="215a2-133">Þú getur tengt úrval aðeins við rásir sem eru innifaldar í stigveldi fyrirtækis sem er úthlutað á tilganginn **Viðskiptaúrval**.</span><span class="sxs-lookup"><span data-stu-id="215a2-133">You can assign assortments only to channels that are included in an organization hierarchy that is assigned the **Commerce assortment** purpose.</span></span> |
| <span data-ttu-id="215a2-134">Skilgreina afurðir.</span><span class="sxs-lookup"><span data-stu-id="215a2-134">Define products.</span></span>                  | <span data-ttu-id="215a2-135">Áður en hægt er að bæta vörum við úrvalið, verður að bæta þeim í Commerce.</span><span class="sxs-lookup"><span data-stu-id="215a2-135">Before you can add products to an assortment, you must add them in Commerce.</span></span> <span data-ttu-id="215a2-136">Hægt er að bæta afurðum handvirkt eða flytja þær frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="215a2-136">You can add products manually, or you can import them from a vendor.</span></span> <span data-ttu-id="215a2-137">Þegar búið er að bæta við afurðum, þarf að losa þær á lögaðila.</span><span class="sxs-lookup"><span data-stu-id="215a2-137">After you add the products, you must release them to a legal entity.</span></span> <span data-ttu-id="215a2-138">Aðeins afurðir sem hafa verið losaðar til lögaðila geta verið gerðar tiltækar á rásum þínum.</span><span class="sxs-lookup"><span data-stu-id="215a2-138">Only products that have been released to a legal entity can be made available to your channels.</span></span> <span data-ttu-id="215a2-139">Afurðir sem enn hefur ekki verið losað til lögaðila er hægt að bæta við úrval og hægt er að samþykkja úrvalinu.</span><span class="sxs-lookup"><span data-stu-id="215a2-139">Products that haven't yet been released to a legal entity can be added to an assortment, and the assortment can be approved.</span></span> <span data-ttu-id="215a2-140">Hinsvegar, þar til afurðir sem hafa verið losaðar til lögaðila geta þær ekki verið gerðar tiltækar á rásunum.</span><span class="sxs-lookup"><span data-stu-id="215a2-140">However, until the products have been released to a legal entity, they can't be made available to the channels.</span></span> |
| <span data-ttu-id="215a2-141">Setja upp tegundastigveldi.</span><span class="sxs-lookup"><span data-stu-id="215a2-141">Set up a category hierarchy.</span></span>      | <span data-ttu-id="215a2-142">Þegar viðskiptaafurðir eru stofnaðar, er hægt að flokka þær með því að nota tegundarstigveldi eiginleika.</span><span class="sxs-lookup"><span data-stu-id="215a2-142">When you create your commerce products, you can group and categorize them by using the category hierarchy feature.</span></span> <span data-ttu-id="215a2-143">Hægt er að stofna eina kjarnauppsetning stigveldis til að flokka öllum afurðum sem dreifa skal gegnum rásir.</span><span class="sxs-lookup"><span data-stu-id="215a2-143">You can create one core hierarchy to group and categorize all products that you distribute through your channels.</span></span> <span data-ttu-id="215a2-144">Einnig er hægt að stofna aðskildar, viðbótartegundastigveldi til að flokka afurðir fyrir sérstaka tilgangi, svo sem kynningartilboð eða í úrvali.</span><span class="sxs-lookup"><span data-stu-id="215a2-144">You can also create separate, supplemental category hierarchies to group or categorize your products for special purposes, such as promotions or assortments.</span></span> <span data-ttu-id="215a2-145">Með því að nota tegundastigveldi er hægt að tengja allar afurðir í tiltekinni tegund við úrval.</span><span class="sxs-lookup"><span data-stu-id="215a2-145">By using category hierarchies, you can assign all the products in a specific category to an assortment.</span></span> <span data-ttu-id="215a2-146">Allar afurðir sem bætt er við tegundina sem er tekin með í úrvalið er sjálfkrafa teknar með í úrvalið.</span><span class="sxs-lookup"><span data-stu-id="215a2-146">Any products that are added to the category that is included in the assortment are automatically included in the assortment.</span></span> <span data-ttu-id="215a2-147">Síðan, í næsta sinn sem verkraðari viðskiptaúrvals er keyrð, þessar afurðir verða tiltækar til rása sem er tengdur við úrvalið.</span><span class="sxs-lookup"><span data-stu-id="215a2-147">Then, the next time that the commerce assortment scheduler is run, these products become available to the channels that the assortment is assigned to.</span></span> |

## <a name="setting-up-an-assortment"></a><span data-ttu-id="215a2-148">Setja upp vöruúrval.</span><span class="sxs-lookup"><span data-stu-id="215a2-148">Setting up an assortment</span></span>

<span data-ttu-id="215a2-149">Eftir að forkröfur er lokið er hægt að stofna úrval og úthluta á rásir.</span><span class="sxs-lookup"><span data-stu-id="215a2-149">After you complete the prerequisites, you can create an assortment and assign it to your channels.</span></span> <span data-ttu-id="215a2-150">Til að setja upp vöruúrval, Það verður að ljúka eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="215a2-150">To set up an assortment, you must complete the following tasks.</span></span>

1. <span data-ttu-id="215a2-151">Stofna nýtt vöruúrval eða afrita fyrirliggjandi vöruúrval</span><span class="sxs-lookup"><span data-stu-id="215a2-151">Create a new assortment, or copy an existing assortment.</span></span>
2. <span data-ttu-id="215a2-152">Veljið rásir eða hástigs flokka af rása sem úrvalið á við.</span><span class="sxs-lookup"><span data-stu-id="215a2-152">Select the channels or the high-level groups of channels that the assortment applies to.</span></span>
3. <span data-ttu-id="215a2-153">Bæta afurðaflokka, stakar afurðir eða afurðarafbrigði við úrvali.</span><span class="sxs-lookup"><span data-stu-id="215a2-153">Add product categories, individual products, or product variants to the assortment.</span></span> <span data-ttu-id="215a2-154">Hægt er að taka með allar vörur í tiltekinni tegund, eða hægt er að útiloka valdar afurðir úr tegund sem er tekin með í úrvalið.</span><span class="sxs-lookup"><span data-stu-id="215a2-154">You can include all products in a specific category, or you can exclude selected products from a category that is included in the assortment.</span></span>
4. <span data-ttu-id="215a2-155">Birta vöruúrval</span><span class="sxs-lookup"><span data-stu-id="215a2-155">Publish the assortment.</span></span> <span data-ttu-id="215a2-156">Verkraðari úrvals er keyrður sjálfkrafa þegar úrval er birt.</span><span class="sxs-lookup"><span data-stu-id="215a2-156">When you publish an assortment, the assortment scheduler is automatically run.</span></span> <span data-ttu-id="215a2-157">Þetta ferli myndar lista yfir afurðir.</span><span class="sxs-lookup"><span data-stu-id="215a2-157">This process generates the list of products.</span></span> <span data-ttu-id="215a2-158">Síðan þegar þessu ferli er lokið verða þessar afurðir tiltækar til rása sem er tengdur við úrvalið.</span><span class="sxs-lookup"><span data-stu-id="215a2-158">When this process is completed, the products become available to the channels that the product assortment is assigned to.</span></span> <span data-ttu-id="215a2-159">Ef breytingar eru gerðar á úrval sem hefur verið birt eða á rás sem úrvalinu er úthlutað á, þarf að uppfæra úrvalinu.</span><span class="sxs-lookup"><span data-stu-id="215a2-159">If changes are made to an assortment that has been published, or to the channels that the assortment is assigned to, the assortment must be updated.</span></span> <span data-ttu-id="215a2-160">Hægt er að keyra verkraðari úrvals sem runuvinnslu til að uppfæra úrvalinu þegar breytingar eru gerðar.</span><span class="sxs-lookup"><span data-stu-id="215a2-160">To update the assortment when changes are made, you can run the assortment scheduler as a batch job.</span></span>
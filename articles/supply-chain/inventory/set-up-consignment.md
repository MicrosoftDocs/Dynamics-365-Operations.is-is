---
title: Uppsetning vörusendingar
description: Í þessu efnisatriði er útskýrt hvernig á að skilgreina aðgerðir vörusendingabirgða á innleið.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5229559647274d4c845325c6b86afbdba43f29e0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834170"
---
# <a name="set-up-consignment"></a><span data-ttu-id="ac7eb-103">Uppsetning vörusendingar</span><span class="sxs-lookup"><span data-stu-id="ac7eb-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac7eb-104">Í þessu efnisatriði er útskýrt hvernig á að skilgreina aðgerðir vörusendingabirgða á innleið.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="ac7eb-105">Vörusendingarbirgðir eru birgðir sem eru í eigu lánardrottinn en geymd á þínu svæði.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="ac7eb-106">Þegar þú ert tilbúinn að nota eða neyta birgða, tekurðu yfir eignarhald birgðanna.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="ac7eb-107">Þetta efnisatriði lýsir uppsetningu sem þarf til að virkja ferli vörusendingar.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="ac7eb-108">Frekari upplýsingar um hvernig ferli vörusendinga eru í [Setja upp vörusendingu](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="ac7eb-108">For more information about consignment processes, see [Set up consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="ac7eb-109">Birgðaeigendur</span><span class="sxs-lookup"><span data-stu-id="ac7eb-109">Inventory owners</span></span>
<span data-ttu-id="ac7eb-110">Til að skrá efnislegar vörusendingabirgðir á innleið, þarf að skilgreina lánardrottinseiganda.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="ac7eb-111">Þetta er gert á **eigandi birgða** síðuna.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="ac7eb-112">Þegar velja **lánardrottnalykil** myndar þetta sjálfgefin gildi fyrir **Heiti** og **Eigandi** svæðum.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="ac7eb-113">Gildið í **Eiganda** svæði verður sýnilegt til lánadrottna, svo þú gætir viljað breyta þeim, ef nöfn á lánardrottnalykill eru ekki auðvelt fyrir utanaðkomandi fólki til að bera kennsl á.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="ac7eb-114">Mögulegt er að breyta á **Eigandi** svæði, en aðeins fram að þeim punkti þegar vista á **eigandi birgða** færslan.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="ac7eb-115">Í **Heiti** svæði er fyllt út með nafn þess aðila sem lánardrottnalykill er tengd við, og þessu er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="ac7eb-116">[![birgðaeigendur](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="ac7eb-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="ac7eb-117">Rakningarvíddarflokkur</span><span class="sxs-lookup"><span data-stu-id="ac7eb-117">Tracking dimension group</span></span>
<span data-ttu-id="ac7eb-118">Vörur sem nota á í ferli vörusendingar verður að tengjast við **rakningarvíddarflokkur** þar sem víddin **Eigandi** er stillt á **Virk**.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="ac7eb-119">Vídd eiganda hefur ávallt **Efnislegar birgðir** og **Fjárhagslegar birgðir** valkostir valinn.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="ac7eb-120">**Þekjuáætlun eftir vídd** er aldrei valin.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="ac7eb-121">[![rakningarvíddarflokkur](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="ac7eb-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="ac7eb-122">Færslubók eignarhaldsbreytingar birgða</span><span class="sxs-lookup"><span data-stu-id="ac7eb-122">Inventory ownership change journal</span></span>
<span data-ttu-id="ac7eb-123">**Birgðafærslubók fyrir breytingu á eignarhaldi** er notuð til að rekja flutninga á eignarhaldi vörusendingabirgða úr lánardrottni í núverandi lögaðila sem neytir þess.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="ac7eb-124">Eins og öllum birgðabók verður það að vera tilgreindur með heiti birgðabókar.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="ac7eb-125">Þessi nöfn eru stofnaðar á **heiti birgðabóka** síðuna og **færslubókargerð** verður að vera stillt á **breytingu á Eignarhaldi**.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="ac7eb-126">[![færslubók eignarhaldsbreytingar birgða](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="ac7eb-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="ac7eb-127">Samstarf lánardrottna í ferli vörusendingar</span><span class="sxs-lookup"><span data-stu-id="ac7eb-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="ac7eb-128">Ef lánardrottnana þínir nota viðmót fyrir samstarf lánardrottna, geta þeir nota þetta að vakta notkun á birgðum á þínu svæði.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="ac7eb-129">Nánari upplýsingar um uppsetningu á lánardrottnum til að nota samstarf lánardrottna er að finna í [Öryggi notanda í gátt lánardrottins](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="ac7eb-129">For more information about setting up vendors to use vendor collaboration, see [Vendor portal user security](../procurement/configure-security-vendor-portal-users.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Yfirlit rása
description: Þetta efnisatriði sýnir yfirlit yfir rásir í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7f5d527dd14d24c06aef874de0088bb07c49849b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800544"
---
# <a name="channels-overview"></a><span data-ttu-id="9eb32-103">Yfirlit rása</span><span class="sxs-lookup"><span data-stu-id="9eb32-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9eb32-104">Þetta efnisatriði sýnir yfirlit yfir rásir í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9eb32-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="9eb32-105">Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja hverja rás upp.</span><span class="sxs-lookup"><span data-stu-id="9eb32-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="9eb32-106">Gerðir rása</span><span class="sxs-lookup"><span data-stu-id="9eb32-106">Types of Channels</span></span>

<span data-ttu-id="9eb32-107">Dynamics 365 Commerce styður þrjár mismunandi rásategundir: smásölu, símaver og netrásir.</span><span class="sxs-lookup"><span data-stu-id="9eb32-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="9eb32-108">Smásölurásir</span><span class="sxs-lookup"><span data-stu-id="9eb32-108">Retail channels</span></span>

<span data-ttu-id="9eb32-109">Smásölurásir standa fyrir hefbundnar verslanir.</span><span class="sxs-lookup"><span data-stu-id="9eb32-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="9eb32-110">Hvert verslun getur haft sína eigin afgreiðslukassa á sölustað, tekju- og kostnaðarlykla og starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="9eb32-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="9eb32-111">Rásir símavers</span><span class="sxs-lookup"><span data-stu-id="9eb32-111">Call center channels</span></span>

<span data-ttu-id="9eb32-112">Símaversrásir sýna símaverspöntun og stjórnun viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="9eb32-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="9eb32-113">Netrásir</span><span class="sxs-lookup"><span data-stu-id="9eb32-113">Online channels</span></span>

<span data-ttu-id="9eb32-114">Netrásir eru netverslanir á netinu.</span><span class="sxs-lookup"><span data-stu-id="9eb32-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="9eb32-115">Þegar rásarkerfi er stofnað verður að stofna svæði með því að nota Microsoft Dynamics 365 Commerce svæðasmíð eða lausn annars þriðja aðila fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="9eb32-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="9eb32-116">Grunnatriði rásaruppsetningar</span><span class="sxs-lookup"><span data-stu-id="9eb32-116">Channel setup basics</span></span>

<span data-ttu-id="9eb32-117">Uppsetning rásar er framkvæmd í viðskiptatækinu.</span><span class="sxs-lookup"><span data-stu-id="9eb32-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="9eb32-118">Hver rás getur haft sínar eigin greiðsluaðferðir, verðhópa, stigveldi vöru, úrval og vöruúrval.</span><span class="sxs-lookup"><span data-stu-id="9eb32-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="9eb32-119">Eftir að þú stofnar rás úthlutarðu þeim afurðum sem þú vilt að verslunin selji.</span><span class="sxs-lookup"><span data-stu-id="9eb32-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="9eb32-120">Hver rásartegund hefur einstakt sett af eiginleikum sem kann að þurfa að stilla.</span><span class="sxs-lookup"><span data-stu-id="9eb32-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="9eb32-121">Til dæmis þarf verslunarrás að fá úthlutað starfsmönnum, skrám og viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="9eb32-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="9eb32-122">Þegar ný rás er búin til þarf að tengja hana við stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="9eb32-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="9eb32-123">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="9eb32-123">Channel setup prerequisites</span></span>

<span data-ttu-id="9eb32-124">Áður en hægt er að setja upp rás verður að klára nokkur forsenduverk sem byggjast á gerð rásarinnar.</span><span class="sxs-lookup"><span data-stu-id="9eb32-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="9eb32-125">Fyrir frekari upplýsingar, sjá [Forsendur rásaruppsetningar](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="9eb32-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="9eb32-126">Setja upp rás</span><span class="sxs-lookup"><span data-stu-id="9eb32-126">Set up a channel</span></span>

<span data-ttu-id="9eb32-127">Eftir að þú hefur lokið forsendum verkefna, notaðu eftirfarandi tengla til að fá frekari leiðbeiningar um uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="9eb32-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="9eb32-128">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="9eb32-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="9eb32-129">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="9eb32-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="9eb32-130">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="9eb32-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="9eb32-131">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9eb32-131">Additional resources</span></span>

[<span data-ttu-id="9eb32-132">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="9eb32-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="9eb32-133">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="9eb32-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="9eb32-134">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="9eb32-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="9eb32-135">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="9eb32-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="9eb32-136">Setja upp stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="9eb32-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
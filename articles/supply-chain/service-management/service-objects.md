---
title: Yfirlit yfir þjónustuhluti
description: Þjónustuhlutir eru eignir og afurðir viðskiptavinar sem hægt er að framkvæma þjónustu við.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ac26083609a337a8d78929dd6f736e1a7c26767
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215149"
---
# <a name="service-objects-overview"></a><span data-ttu-id="7160a-103">Yfirlit yfir þjónustuhluti</span><span class="sxs-lookup"><span data-stu-id="7160a-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7160a-104">Þjónustuhlutir eru eignir og afurðir viðskiptavinar sem hægt er að framkvæma þjónustu við.</span><span class="sxs-lookup"><span data-stu-id="7160a-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="7160a-105">Eftir þeirr gerð þjónustu sem er gefin geta hlutir verið áþreifanlegt eða óáþreifanlegt:</span><span class="sxs-lookup"><span data-stu-id="7160a-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="7160a-106">Dæmi um efnislega hluti eru vél eða bygging, sem geta sætt áþreifanlegum þjónustuverkum.</span><span class="sxs-lookup"><span data-stu-id="7160a-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="7160a-107">Áþreifanlegur þjónustuhlutur getur einnig verið birgðavara sem er stofnuð í skjámyndinni Upplýsingar um losaða afurð.</span><span class="sxs-lookup"><span data-stu-id="7160a-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="7160a-108">Eftir birgðavíddarflokkurinn sem er tengdur vörunni, hægt er að stofna þjónustuhlut upplýsingastigi sem inniheldur raðnúmer vöru.</span><span class="sxs-lookup"><span data-stu-id="7160a-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="7160a-109">Þetta er gagnlegt ef um er að fylgjast með nákvæma vöruna sem táknar þann þjónustuhlut.</span><span class="sxs-lookup"><span data-stu-id="7160a-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="7160a-110">Efnislegar þjónustuhlut getur einnig verið vara sem er ekki beint tengdur framleiðsla fyrirtækis eða birgðakeðju.</span><span class="sxs-lookup"><span data-stu-id="7160a-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="7160a-111">Til dæmis verkfæri setts sem er notað fyrir viðgerðir í þjónustupöntun getur þjónustuhlut sem er ekki í birgðum.</span><span class="sxs-lookup"><span data-stu-id="7160a-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="7160a-112">Í þessu tilfelli skrárðu það ekki sem birgðavöru.</span><span class="sxs-lookup"><span data-stu-id="7160a-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="7160a-113">Óáþreifanlegir hlutir eru óefnislegir hlutir, eins og reikningsflokkur eða lagalegt fylgiskjal, sem hægt er að framkvæma þjónustuverk fyrir.</span><span class="sxs-lookup"><span data-stu-id="7160a-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="7160a-114">Dæmi óefnislegs þjónustuhluts</span><span class="sxs-lookup"><span data-stu-id="7160a-114">Example of an intangible service object</span></span>

<span data-ttu-id="7160a-115">Fyrirtæki A viðheldur fjárhagslegum færslum fyrir lítilla fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="7160a-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="7160a-116">Einn af viðskiptavinum fyrirtækis A er fótboltaliðið á staðnum, sem fyrirtæki A sér um vikulegt bókhald fyrir og árlega endurskoðun á reikningum klúbbsins.</span><span class="sxs-lookup"><span data-stu-id="7160a-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="7160a-117">Reikningar félagsins eru settir upp í skjámyndinni Þjónustuhlutir og tilgreindir sem hluturinn í þjónustusamningnum.</span><span class="sxs-lookup"><span data-stu-id="7160a-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="7160a-118">Það eru tvær þjónustusamningslínur fyrir hlutinn.</span><span class="sxs-lookup"><span data-stu-id="7160a-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="7160a-119">Lína 1 er vikulegt bókhald með vikulegt bil úthlutað á línuna, og lína 2 er árleg endurskoðun með árlegu millibili úthlutað.</span><span class="sxs-lookup"><span data-stu-id="7160a-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7160a-120">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="7160a-120">Related topics</span></span>

[<span data-ttu-id="7160a-121">Stofna þjónustuhluta</span><span class="sxs-lookup"><span data-stu-id="7160a-121">Create service objects</span></span>](create-service-objects.md)


---
title: Skila raðnúmerastýrðum afurðum á sölustað
description: Í þessu efnisatriði eru útskýrðir möguleikarnir á að staðfesta röðuðum vörum sem hluti af skilaferlinu í Microsoft Dynamics 365 Commerce forriti sölustaðar.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129813"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="4337c-103">Skila raðnúmerastýrðum afurðum á sölustað</span><span class="sxs-lookup"><span data-stu-id="4337c-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4337c-104">Í þessu efnisatriði eru útskýrðir möguleikarnir á að staðfesta röðuðum vörum sem hluti af skilaferlinu í Microsoft Dynamics 365 Commerce forriti sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="4337c-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="4337c-105">Í Commerce-útgáfu 10.0.20 og nýrri er boðið upp á nýjan eiginleika sem heitir **Upplifun samræmdrar skilavinnslu á sölustað**.</span><span class="sxs-lookup"><span data-stu-id="4337c-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="4337c-106">Til að nota staðfestingu raðnúmers við vinnslu á skilapöntun á sölustað þarf að kveikja á þessum eiginleika.</span><span class="sxs-lookup"><span data-stu-id="4337c-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="4337c-107">Upplýsingar um möguleika annarra sem þessi eiginleiki veitir þegar kveikt er á honum er að finna í [Stofna skil á sölustað](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="4337c-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="4337c-108">Ekki er hægt að slökkva á eiginleikanum eftir að kveikt er á honum.</span><span class="sxs-lookup"><span data-stu-id="4337c-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="4337c-109">Valkostir fyrir staðfestingu á röðuðum skilum</span><span class="sxs-lookup"><span data-stu-id="4337c-109">Options for validating serialized returns</span></span>

<span data-ttu-id="4337c-110">Þegar kveikt er á eiginleikanum **Upplifun samræmdrar skilavinnslu á sölustað** geta fyrirtæki staðfest skil á raðnúmerastýrðum vörum í gegnum sölustað.</span><span class="sxs-lookup"><span data-stu-id="4337c-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="4337c-111">Þessi möguleiki getur varað notendur við ef raðnúmerið sem verið að skila er ólíkt upprunalega raðnúmerinu sem var selt.</span><span class="sxs-lookup"><span data-stu-id="4337c-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="4337c-112">Í Commerce-útgáfu 10.0.20 og nýrri eru skilaboðin sem notendur fá aðeins viðvörunarboð.</span><span class="sxs-lookup"><span data-stu-id="4337c-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="4337c-113">Notendur geta haldið áfram að vinna úr skilum varðandi raðnúmer sem er ólíkt raðnúmerinu sem var upprunalega selt.</span><span class="sxs-lookup"><span data-stu-id="4337c-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="4337c-114">Til að stilla villuleit raðnúmers fyrir fyrirtæki þegar kveikt hefur verið á eiginleikanum **Upplifun samræmdrar skilavinnslu á sölustað** skal fara í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Commerce-færibreytur** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="4337c-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="4337c-115">Í flipanum **Birgðir**, í flýtiflipanum **Birgðaaðgerðir verslunar**, skal stilla valkostinn **Virkja villuleit raðnúmera á skilum sölustaðar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="4337c-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="4337c-116">Skilavinnsla fyrir raðnúmeraðar vörur á sölustað</span><span class="sxs-lookup"><span data-stu-id="4337c-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="4337c-117">Ef valkosturinn **Virkja villuleit raðnúmera á skilum sölustaðar** hefur verið stilltur á **Já**, þegar raðnúmerastýrðri vöru er skilað í gegnum sölustað, getur notandinn slegið inn raðnúmerið fyrir skilalínuna í upplýsingasvæðið á síðunni **Afurðir sem hægt er að skila**.</span><span class="sxs-lookup"><span data-stu-id="4337c-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="4337c-118">Ef raðnúmerið sem er fært inn passar ekki við upprunalegt raðnúmer sem var selt fyrir sölufærsluna fær notandinn upp viðvörunarboð.</span><span class="sxs-lookup"><span data-stu-id="4337c-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="4337c-119">Forritið kemur hinsvegar ekki í veg fyrir að notandinn geti haldið áfram að vinna úr skilunum.</span><span class="sxs-lookup"><span data-stu-id="4337c-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="4337c-120">Sem stendur styður sölustaðurinn villuleit raðnúmera eingöngu fyrir skilalínur þar sem upprunalegt pöntunarmagn er ekki meira en einn.</span><span class="sxs-lookup"><span data-stu-id="4337c-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="4337c-121">Ef upprunalega sölupöntunarlínan var búin til í rás sem er ekki á sölustað og ef magnið sem var pantað fyrir raðnúmeraða vöru í tiltekinni sölulínu er meira en einn verður ekki hægt að skila vörunni á réttan hátt í gegnum sölustað.</span><span class="sxs-lookup"><span data-stu-id="4337c-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4337c-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4337c-122">Additional resources</span></span>

[<span data-ttu-id="4337c-123">Stofna skil á sölustað</span><span class="sxs-lookup"><span data-stu-id="4337c-123">Create returns in POS</span></span>](POS-returns.md)

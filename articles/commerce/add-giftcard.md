---
title: Gjafakortseining
description: Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261573"
---
# <a name="gift-card-module"></a><span data-ttu-id="1a6f8-103">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="1a6f8-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a6f8-104">Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1a6f8-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="1a6f8-105">Overview</span></span>

<span data-ttu-id="1a6f8-106">Gjafakort eru algeng greiðsluform og hægt er að nota gjafakortseininguna í kassaeiningu til að taka við gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="1a6f8-107">Gjafakortseiningin styður Dynamics 365, SVS og Givex gjafakort.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="1a6f8-108">Gjafakort SVS og Givex eru innleyst með Adyen greiðsluþjónustuaðila.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="1a6f8-109">Nánari upplýsingar um stuðning við utanaðkomandi gjafakort eins og SVS og Givex er að finna í [Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="1a6f8-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

## <a name="module-properties"></a><span data-ttu-id="1a6f8-110">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="1a6f8-110">Module properties</span></span>

- <span data-ttu-id="1a6f8-111">**Sýna fleiri reiti** - Þessi eiginleiki skilgreinir hvaða reiti skuli birta fyrir gjafakort auk gjafakortsnúmersins sem er alltaf birt sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-111">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="1a6f8-112">Til dæmis styðja sum gjafakort með birtinu á persónuauðkenni (PIN) og önnur styðja birtingu PIN og gildistíma.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-112">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="1a6f8-113">Að öðrum kosti væri hægt að stilla þennan eiginleika á „Enginn“, sem myndi aðeins sýna gjafakortsnúmerið og enga viðbótarreiti.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-113">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="1a6f8-114">Studd gildi:</span><span class="sxs-lookup"><span data-stu-id="1a6f8-114">Supported values:</span></span>
-   <span data-ttu-id="1a6f8-115">PIN</span><span class="sxs-lookup"><span data-stu-id="1a6f8-115">PIN</span></span>
-   <span data-ttu-id="1a6f8-116">Gildistími</span><span class="sxs-lookup"><span data-stu-id="1a6f8-116">Expiration date</span></span>
-   <span data-ttu-id="1a6f8-117">PIN og lokadagur</span><span class="sxs-lookup"><span data-stu-id="1a6f8-117">PIN and expiration date</span></span> 
-   <span data-ttu-id="1a6f8-118">None</span><span class="sxs-lookup"><span data-stu-id="1a6f8-118">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="1a6f8-119">Vefstillingar fyrir gjafakortseiningar</span><span class="sxs-lookup"><span data-stu-id="1a6f8-119">Site settings for gift card modules</span></span>

<span data-ttu-id="1a6f8-120">Í vefsvæðishönnuði Commerce undir **Vefstillingar \> Viðbætur** er stilling gjafakortseiningar sem kallast **Studd gerð gjafakorts**.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-120">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="1a6f8-121">Þessi stilling styður þrjú gildi:</span><span class="sxs-lookup"><span data-stu-id="1a6f8-121">This setting supports three values:</span></span>
- <span data-ttu-id="1a6f8-122">**Dynamics 365 gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365 gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-122">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="1a6f8-123">Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-123">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="1a6f8-124">**SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Givex og SVS gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-124">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="1a6f8-125">Þessi stilling er studd fyrir innskráða og nafnlausa notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-125">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="1a6f8-126">**Dynamics 365, SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365, Givex og SVS gjafakortum.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-126">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="1a6f8-127">Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-127">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="1a6f8-128">Bæta gjafakortseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="1a6f8-128">Add a gift card module to a page</span></span>

<span data-ttu-id="1a6f8-129">Leiðbeiningar um hvernig bæta skuli gjafakortseiningu við greiðslusíðu og stilla nauðsynlega eiginleika er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f8-129">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a6f8-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1a6f8-130">Additional resources</span></span>

[<span data-ttu-id="1a6f8-131">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="1a6f8-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1a6f8-132">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="1a6f8-132">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1a6f8-133">Stuðningur við utanaðkomandi gjafakort</span><span class="sxs-lookup"><span data-stu-id="1a6f8-133">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

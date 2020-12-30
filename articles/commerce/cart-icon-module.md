---
title: Körfutáknseining
description: Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ebc5cfa490a4c8538fd081aced0844ed01d63a26
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/07/2020
ms.locfileid: "4413318"
---
# <a name="cart-icon-module"></a><span data-ttu-id="c6c40-103">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="c6c40-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6c40-104">Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c6c40-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c6c40-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c6c40-105">Overview</span></span>

<span data-ttu-id="c6c40-106">Körfutákneiningin táknar körfuna í hauseiningu síðunnar og sýnir fjölda af vörum í körfunni.</span><span class="sxs-lookup"><span data-stu-id="c6c40-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="c6c40-107">Körfutáknseiningin birtir einnig yfirlit yfir körfu (einnig þekkt sem smákarfa) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="c6c40-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="c6c40-108">Smákarfan veitir notanda yfirlit yfir hluti í körfunni án þess að þurfa að fara á körfusíðuna.</span><span class="sxs-lookup"><span data-stu-id="c6c40-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="c6c40-109">Að auki gerir það notandanum einnig kleift að fara beint á greiðslusíðu ef viðkomandi er ánægður með yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="c6c40-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="c6c40-110">Þetta dregur úr fjölda síðnaferða og gerir afgreiðsluna hraðari.</span><span class="sxs-lookup"><span data-stu-id="c6c40-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="c6c40-111">Stuðningur við fyrir körfueiningu er tiltækur í Dynamics 365 Commerce útgáfu 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="c6c40-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="c6c40-112">Eftirfarandi mynd sýnir dæmi um einingu körfutákns sem sýnir smákörfu í Fabrikam-fyrirsögninni.</span><span class="sxs-lookup"><span data-stu-id="c6c40-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Dæmi um körfutáknseiningu](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="c6c40-114">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="c6c40-114">Module properties</span></span>

- <span data-ttu-id="c6c40-115">**Sýna smákörfu** - Þegar satt gerir þessi eiginleiki kleift að birta yfirlit yfir körfu (smákörfu) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="c6c40-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="c6c40-116">Þessi virkni er aðeins studd fyrir skjáborðsgáttir.</span><span class="sxs-lookup"><span data-stu-id="c6c40-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="c6c40-117">Bæta körfutáknseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="c6c40-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="c6c40-118">Til að bæta við einingunni fyrir körfutákn, sjá [Hauseiningu](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="c6c40-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6c40-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c6c40-119">Additional resources</span></span>

[<span data-ttu-id="c6c40-120">Körfueining</span><span class="sxs-lookup"><span data-stu-id="c6c40-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c6c40-121">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="c6c40-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c6c40-122">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="c6c40-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="c6c40-123">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="c6c40-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="c6c40-124">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="c6c40-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="c6c40-125">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="c6c40-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="c6c40-126">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="c6c40-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c6c40-127">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="c6c40-127">Gift card module</span></span>](add-giftcard.md)

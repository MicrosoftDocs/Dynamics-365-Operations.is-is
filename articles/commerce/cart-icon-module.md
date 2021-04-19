---
title: Körfutáknseining
description: Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793082"
---
# <a name="cart-icon-module"></a><span data-ttu-id="07c3b-103">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="07c3b-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="07c3b-104">Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="07c3b-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="07c3b-105">Körfutákneiningin táknar körfuna í hauseiningu síðunnar og sýnir fjölda af vörum í körfunni.</span><span class="sxs-lookup"><span data-stu-id="07c3b-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="07c3b-106">Körfutáknseiningin birtir einnig yfirlit yfir körfu (einnig þekkt sem smákarfa) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="07c3b-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="07c3b-107">Smákarfan veitir notanda yfirlit yfir hluti í körfunni án þess að þurfa að fara á körfusíðuna.</span><span class="sxs-lookup"><span data-stu-id="07c3b-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="07c3b-108">Að auki gerir það notandanum einnig kleift að fara beint á greiðslusíðu ef viðkomandi er ánægður með yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="07c3b-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="07c3b-109">Þetta dregur úr fjölda síðnaferða og gerir afgreiðsluna hraðari.</span><span class="sxs-lookup"><span data-stu-id="07c3b-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="07c3b-110">Stuðningur við fyrir körfueiningu er tiltækur í Dynamics 365 Commerce útgáfu 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="07c3b-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="07c3b-111">Eftirfarandi mynd sýnir dæmi um einingu körfutákns sem sýnir smákörfu í Fabrikam-fyrirsögninni.</span><span class="sxs-lookup"><span data-stu-id="07c3b-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Dæmi um körfutáknseiningu](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="07c3b-113">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="07c3b-113">Module properties</span></span>

- <span data-ttu-id="07c3b-114">**Sýna smákörfu** - Þegar satt gerir þessi eiginleiki kleift að birta yfirlit yfir körfu (smákörfu) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="07c3b-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="07c3b-115">Þessi virkni er aðeins studd fyrir skjáborðsgáttir.</span><span class="sxs-lookup"><span data-stu-id="07c3b-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="07c3b-116">Bæta körfutáknseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="07c3b-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="07c3b-117">Til að bæta við einingunni fyrir körfutákn, sjá [Hauseiningu](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="07c3b-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07c3b-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="07c3b-118">Additional resources</span></span>

[<span data-ttu-id="07c3b-119">Körfueining</span><span class="sxs-lookup"><span data-stu-id="07c3b-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="07c3b-120">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="07c3b-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="07c3b-121">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="07c3b-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="07c3b-122">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="07c3b-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="07c3b-123">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="07c3b-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="07c3b-124">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="07c3b-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="07c3b-125">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="07c3b-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="07c3b-126">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="07c3b-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Körfutáknseining
description: Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661148"
---
# <a name="cart-icon-module"></a><span data-ttu-id="f60a6-103">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="f60a6-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f60a6-104">Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f60a6-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f60a6-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f60a6-105">Overview</span></span>

<span data-ttu-id="f60a6-106">Körfutákneiningin táknar körfuna í hauseiningu síðunnar og sýnir fjölda af vörum í körfunni.</span><span class="sxs-lookup"><span data-stu-id="f60a6-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="f60a6-107">Körfutáknseiningin birtir einnig yfirlit yfir körfu (einnig þekkt sem smákarfa) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="f60a6-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="f60a6-108">Smákarfan veitir notanda yfirlit yfir hluti í körfunni án þess að þurfa að fara á körfusíðuna.</span><span class="sxs-lookup"><span data-stu-id="f60a6-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="f60a6-109">Að auki gerir það notandanum einnig kleift að fara beint á greiðslusíðu ef viðkomandi er ánægður með yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="f60a6-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="f60a6-110">Þetta dregur úr fjölda síðnaferða og gerir afgreiðsluna hraðari.</span><span class="sxs-lookup"><span data-stu-id="f60a6-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="f60a6-111">Eftirfarandi mynd sýnir dæmi um einingu körfutákns sem sýnir smákörfu í Fabrikam-fyrirsögninni.</span><span class="sxs-lookup"><span data-stu-id="f60a6-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Dæmi um körfutáknseiningu](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="f60a6-113">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="f60a6-113">Module properties</span></span>

- <span data-ttu-id="f60a6-114">**Sýna smákörfu** - Þegar satt gerir þessi eiginleiki kleift að birta yfirlit yfir körfu (smákörfu) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="f60a6-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="f60a6-115">Þessi virkni er aðeins studd fyrir skjáborðsgáttir.</span><span class="sxs-lookup"><span data-stu-id="f60a6-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="f60a6-116">Bæta körfutáknseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="f60a6-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="f60a6-117">Til að bæta við einingunni fyrir körfutákn, sjá [Hauseiningu](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="f60a6-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f60a6-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f60a6-118">Additional resources</span></span>

[<span data-ttu-id="f60a6-119">Körfueining</span><span class="sxs-lookup"><span data-stu-id="f60a6-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f60a6-120">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="f60a6-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f60a6-121">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="f60a6-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f60a6-122">Eining sendingaraðseturs</span><span class="sxs-lookup"><span data-stu-id="f60a6-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f60a6-123">Eining afhendingarvalkosta</span><span class="sxs-lookup"><span data-stu-id="f60a6-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f60a6-124">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="f60a6-124">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f60a6-125">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="f60a6-125">Gift card module</span></span>](add-giftcard.md)

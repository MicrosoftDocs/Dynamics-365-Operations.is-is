---
title: Körfutáknseining
description: Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261572"
---
# <a name="cart-icon-module"></a><span data-ttu-id="da9a7-103">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="da9a7-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da9a7-104">Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="da9a7-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da9a7-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="da9a7-105">Overview</span></span>

<span data-ttu-id="da9a7-106">Körfutákneiningin táknar körfuna í hauseiningu síðunnar og sýnir fjölda af vörum í körfunni.</span><span class="sxs-lookup"><span data-stu-id="da9a7-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="da9a7-107">Körfutáknseiningin birtir einnig yfirlit yfir körfu (einnig þekkt sem smákarfa) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="da9a7-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="da9a7-108">Smákarfan veitir notanda yfirlit yfir hluti í körfunni án þess að þurfa að fara á körfusíðuna.</span><span class="sxs-lookup"><span data-stu-id="da9a7-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="da9a7-109">Að auki gerir það notandanum einnig kleift að fara beint á greiðslusíðu ef viðkomandi er ánægður með yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="da9a7-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="da9a7-110">Þetta dregur úr fjölda síðnaferða og gerir afgreiðsluna hraðari.</span><span class="sxs-lookup"><span data-stu-id="da9a7-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="da9a7-111">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="da9a7-111">Module properties</span></span>

- <span data-ttu-id="da9a7-112">**Sýna smákörfu** - Þegar satt gerir þessi eiginleiki kleift að birta yfirlit yfir körfu (smákörfu) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="da9a7-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="da9a7-113">Þessi virkni er aðeins studd fyrir skjáborðsgáttir.</span><span class="sxs-lookup"><span data-stu-id="da9a7-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="da9a7-114">Bæta körfutáknseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="da9a7-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="da9a7-115">Til að bæta við einingunni fyrir körfutákn, sjá [Hauseiningu](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="da9a7-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="da9a7-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="da9a7-116">Additional resources</span></span>

[<span data-ttu-id="da9a7-117">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="da9a7-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="da9a7-118">Körfueining</span><span class="sxs-lookup"><span data-stu-id="da9a7-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="da9a7-119">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="da9a7-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="da9a7-120">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="da9a7-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="da9a7-121">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="da9a7-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="da9a7-122">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="da9a7-122">Footer module</span></span>](author-footer-module.md)

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
ms.openlocfilehash: 6771a84118504cd5c8e44302380eb970e4658902
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411090"
---
# <a name="cart-icon-module"></a><span data-ttu-id="3d832-103">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="3d832-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3d832-104">Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3d832-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3d832-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="3d832-105">Overview</span></span>

<span data-ttu-id="3d832-106">Körfutákneiningin táknar körfuna í hauseiningu síðunnar og sýnir fjölda af vörum í körfunni.</span><span class="sxs-lookup"><span data-stu-id="3d832-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="3d832-107">Körfutáknseiningin birtir einnig yfirlit yfir körfu (einnig þekkt sem smákarfa) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="3d832-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="3d832-108">Smákarfan veitir notanda yfirlit yfir hluti í körfunni án þess að þurfa að fara á körfusíðuna.</span><span class="sxs-lookup"><span data-stu-id="3d832-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="3d832-109">Að auki gerir það notandanum einnig kleift að fara beint á greiðslusíðu ef viðkomandi er ánægður með yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="3d832-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="3d832-110">Þetta dregur úr fjölda síðnaferða og gerir afgreiðsluna hraðari.</span><span class="sxs-lookup"><span data-stu-id="3d832-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="3d832-111">Eftirfarandi mynd sýnir dæmi um einingu körfutákns sem sýnir smákörfu í Fabrikam-fyrirsögninni.</span><span class="sxs-lookup"><span data-stu-id="3d832-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Dæmi um körfutáknseiningu](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="3d832-113">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="3d832-113">Module properties</span></span>

- <span data-ttu-id="3d832-114">**Sýna smákörfu** - Þegar satt gerir þessi eiginleiki kleift að birta yfirlit yfir körfu (smákörfu) þegar músin sveimar yfir körfutákninu.</span><span class="sxs-lookup"><span data-stu-id="3d832-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="3d832-115">Þessi virkni er aðeins studd fyrir skjáborðsgáttir.</span><span class="sxs-lookup"><span data-stu-id="3d832-115">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="3d832-116">Bæta körfutáknseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="3d832-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="3d832-117">Til að bæta við einingunni fyrir körfutákn, sjá [Hauseiningu](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="3d832-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="3d832-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3d832-118">Additional resources</span></span>

[<span data-ttu-id="3d832-119">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="3d832-119">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3d832-120">Körfueining</span><span class="sxs-lookup"><span data-stu-id="3d832-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3d832-121">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="3d832-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3d832-122">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="3d832-122">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3d832-123">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="3d832-123">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="3d832-124">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="3d832-124">Footer module</span></span>](author-footer-module.md)

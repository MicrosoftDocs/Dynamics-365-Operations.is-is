---
title: "Sala og skil á afurðum utan vöruúrvals"
description: "Með Dynamics 365 for Retail er hægt að selja og skila vörum utan úrvals."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: 
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7fa5b240bc9c9f96ae5483be316eff62df915570
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="be5ec-103">Sala og skil á afurðum utan vöruúrvals</span><span class="sxs-lookup"><span data-stu-id="be5ec-103">Sell and return products outside of an assortment</span></span>
<span data-ttu-id="be5ec-104">Algeng aðstæður fyrir allar söluaðilann er að selja vörur til þeirra viðskiptavina eða samþykkja skil frá viðskiptavinum þeirra jafnvel þótt þeir ekki að framkvæma tilteknar vörur sínar verslun (með öðrum orðum vara eru ekki assorted í verslun).</span><span class="sxs-lookup"><span data-stu-id="be5ec-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="be5ec-105">Hér eru nokkrar dæmigerðar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="be5ec-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="be5ec-106">Við söluaðilann áskilinn hafa allar þeirra vara í ákveðna verslun.</span><span class="sxs-lookup"><span data-stu-id="be5ec-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="be5ec-107">Eftirstandandi vörurnar eru geymdar í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="be5ec-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="be5ec-108">Aðstoðarmaður í verslun getur hjálpað til við viðskiptavini með því að leita eða fletting fyrir vörurnar í vöruhúsinu bæta í körfu til að og ljúka við útskráning með því að velja afhendingaraðferðina, eins og sendingar í aðsetur úr vöruhúsi eða letting viðskiptavina sem taka upp vörunni úr gildandi verslun eða frá annarri verslun.</span><span class="sxs-lookup"><span data-stu-id="be5ec-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="be5ec-109">Við söluaðilann áskilinn bera ákveðnum vörum í versluninni eða áskilinn eru þær lager verslun viðskiptavinar skoðaðar fyrr en vörurnar eru tiltækar í aðrar verslanir.</span><span class="sxs-lookup"><span data-stu-id="be5ec-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="be5ec-110">Aðstoðarmaður í verslun getur hjálpað til við viðskiptavini með því að leita eða skoða vara á verslun, bæta í körfu til að og útskráning við að ljúka með því að velja afhendingaraðferðina fyrir.</span><span class="sxs-lookup"><span data-stu-id="be5ec-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="be5ec-111">Við söluaðilann margar verslanir í og samkvæmt ákveðnum borgar eða póstnúmer og áskilinn á að láta viðskiptavinina aftur vörur á sömu þær voru keyptar inn í verslunina.</span><span class="sxs-lookup"><span data-stu-id="be5ec-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="be5ec-112">Þess í stað getur viðskiptavinir skila vörum í hvaða annarri verslun.</span><span class="sxs-lookup"><span data-stu-id="be5ec-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="be5ec-113">Þær algengar aðstæður eru í boði fyrir smásala með Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="be5ec-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="be5ec-114">Með Retail er hægt að:</span><span class="sxs-lookup"><span data-stu-id="be5ec-114">With Retail, you can:</span></span>
+ <span data-ttu-id="be5ec-115">Leita eða fletta að vörur í aðrar verslanir.</span><span class="sxs-lookup"><span data-stu-id="be5ec-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="be5ec-116">Leita eða fletta losaðar allar vörur.</span><span class="sxs-lookup"><span data-stu-id="be5ec-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="be5ec-117">Stofna cash-and-carry færslur viðskiptavinar eða pantanir.</span><span class="sxs-lookup"><span data-stu-id="be5ec-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="be5ec-118">Velja valkosti fyrir viðskiptavinapöntunum afhendingar.</span><span class="sxs-lookup"><span data-stu-id="be5ec-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="be5ec-119">Taka vörur í annarri verslun eða verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="be5ec-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="be5ec-120">Hætta við pöntun á verslunarinnar eða annarri verslun.</span><span class="sxs-lookup"><span data-stu-id="be5ec-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="be5ec-121">Pöntun með eða án móttöku á núverandi verslun eða annarri verslun aftur.</span><span class="sxs-lookup"><span data-stu-id="be5ec-121">Return an order with or without the receipt at the current store or another store.</span></span>


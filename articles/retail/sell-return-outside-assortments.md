---
title: Sala og skil á afurðum sem ekki eru hluti af úrvali verslunar
description: Með Dynamics 365 for Retail getur þú selt og skilað afurðum út fyrir vöruúrval.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 653a388de1a972fae488abd81f349d1b138fc716
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "352299"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="f7ad6-103">Sala og skil á afurðum sem ekki eru hluti af úrvali verslunar</span><span class="sxs-lookup"><span data-stu-id="f7ad6-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f7ad6-104">Algengar aðstæður fyrir smásöluaðila er að selja afurðir til viðskiptavina eða samþykkja skil frá viðskiptavinum þeirra, jafnvel þótt þeir séu ekki með tiltekna afurð í versluninni (með öðrum orðum, afurðirnar eru ekki valdar fyrir verslunina).</span><span class="sxs-lookup"><span data-stu-id="f7ad6-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="f7ad6-105">Hér eru nokkrar dæmigerðar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="f7ad6-106">Smásöluaðili er ekki með allar afurðir sínar í tiltekinni verslun.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="f7ad6-107">Eftirstandandi vörurnar eru geymdar í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="f7ad6-108">Aðstoðarmaður í verslun getur hjálpað til við viðskiptavini með því að leita eða fletting fyrir vörurnar í vöruhúsinu bæta í körfu til að og ljúka við útskráning með því að velja afhendingaraðferðina, eins og sendingar í aðsetur úr vöruhúsi eða letting viðskiptavina sem taka upp vörunni úr gildandi verslun eða frá annarri verslun.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="f7ad6-109">Smásöluaðili er ekki með tilteknar afurðir í versluninni eða er ekki með þær í birgðum verslunar sem viðskiptavinurinn heimsótti, en afurðirnar eru fáanlegar í öðrum verslunum.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="f7ad6-110">Aðstoðarmaður í verslun getur hjálpað til við viðskiptavini með því að leita eða skoða vara á verslun, bæta í körfu til að og útskráning við að ljúka með því að velja afhendingaraðferðina fyrir.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="f7ad6-111">Smásöluaðili er með margar verslanir í tiltekinni borg eða nágrenni hennar eða í póstnúmeri og vill ekki neyða viðskiptavini til að skila afurðunum í sömu verslun og þær voru keyptar í.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="f7ad6-112">Þess í stað getur viðskiptavinir skila vörum í hvaða annarri verslun.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="f7ad6-113">Þessar algengu aðstæður eru tiltækar fyrir smásala sem nota Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="f7ad6-114">Með Retail er hægt að:</span><span class="sxs-lookup"><span data-stu-id="f7ad6-114">With Retail, you can:</span></span>

+ <span data-ttu-id="f7ad6-115">Leita eða fletta að vörur í aðrar verslanir.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="f7ad6-116">Leita eða fletta losaðar allar vörur.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="f7ad6-117">Stofna cash-and-carry færslur viðskiptavinar eða pantanir.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="f7ad6-118">Velja valkosti fyrir viðskiptavinapöntunum afhendingar.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="f7ad6-119">Taka vörur í annarri verslun eða verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="f7ad6-120">Hætta við pöntun á verslunarinnar eða annarri verslun.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="f7ad6-121">Pöntun með eða án móttöku á núverandi verslun eða annarri verslun aftur.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-121">Return an order with or without the receipt at the current store or another store.</span></span>

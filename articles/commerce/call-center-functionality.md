---
title: Söluvirkni símavers
description: Þessi grein veitir yfirlit yfir söluvirkni símavera í Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d188138654ba20d8393ed4bca8124a65402daff2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991441"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="0a6fb-103">Söluvirkni símavers</span><span class="sxs-lookup"><span data-stu-id="0a6fb-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="0a6fb-104">Í Dynamics 365 Commerce er símaver tegund rásar sem hægt er að skilgreina í forritinu.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="0a6fb-105">Með því að skilgreina tiltekna rás fyrir símaverseiningar þínar er kerfinu gert kleift að binda ákveðin sjálfgildi gagna og sjálfgildi pöntunarvinnslu við sölupantanir sem búnar eru til af notanda símaversrásarinnar.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="0a6fb-106">Eiginleikar símavers eru meðal annars ítarlegt verð og kynningar, vörulistar, gjafakort, vildarkerfi og afsláttarmiðar.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="0a6fb-107">Símaverspantanir eru einnig notaðar af sölustað (POS) forritinu til að styðja við tilvik pöntunaruppfyllingar þvert á rásir.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="0a6fb-108">Það er mikilvægt að hafa í huga að þótt aðrar atvinnugreinar utan Commerce geti nýtt sér kerfiseiningu símavers, hefur núverandi útgáfa símaversforritsins ekki verið fínstillt fyrir notkun í tilvikum vinnslu pantana á milli fyrirtækja (B2B), eða í tilvikum þar sem pantanir hafa mjög margar sölulínur.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large number of sales lines.</span></span> <span data-ttu-id="0a6fb-109">Mælt er með því að notendur sem vilja nýta sér eiginleika símavers fyrir vinnslu pantana sem eru fyrir utan dæmigerða beint-til-neytanda færsluvinnslu, taki sér nægan tíma til að prófa og sannreyna að það að opna fyrir virkni símavers muni uppfylla þarfir um virkni og afköst.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="0a6fb-110">Auk þess að styðja við stofnun pöntunar býður kerfiseining símavers einnig upp á notendavænt þjónustuforrit fyrir viðskiptavini sem auðveldar notendum að finna viðskiptavinareikninga og yfirfara öll tengd gögn og eigindir viðskiptavinapantana.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="0a6fb-111">Þjónustuskjárinn fyrir viðskiptavini er hannaður til að gera notanda kleift að fá aðgang að gögnum tengdum pöntunum fljótt, sem gerir þeim kleift að svara algengustu spurningum tengdum pöntunum frá viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-111">The customer service screen is designed to enable a user to quickly access order-related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="0a6fb-112">Þessi síða veitir tengla á viðeigandi fylgiskjöl sem tengjast uppsetningu, grunnstillingu og notkunarvirkni eiginleika símaversins.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="0a6fb-113">Grunnstilla símaverið</span><span class="sxs-lookup"><span data-stu-id="0a6fb-113">Configure the call center</span></span>

[<span data-ttu-id="0a6fb-114">Setja upp símaversrásir</span><span class="sxs-lookup"><span data-stu-id="0a6fb-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="0a6fb-115">Grunnstilla pöntunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="0a6fb-115">Configure order processing</span></span>

[<span data-ttu-id="0a6fb-116">Setja upp og vinna með viðvaranir vegna svika fyrir símaver</span><span class="sxs-lookup"><span data-stu-id="0a6fb-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="0a6fb-117">Skilgreina og vinna með símaverspantanir í bið</span><span class="sxs-lookup"><span data-stu-id="0a6fb-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="0a6fb-118">Grunnstilla greiðsluvinnslu</span><span class="sxs-lookup"><span data-stu-id="0a6fb-118">Configure payment processing</span></span>

[<span data-ttu-id="0a6fb-119">Greiðslumátar í símaverum</span><span class="sxs-lookup"><span data-stu-id="0a6fb-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="0a6fb-120">Grunnstilla afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="0a6fb-120">Configure delivery modes</span></span>

[<span data-ttu-id="0a6fb-121">Grunnstilla afhendingarmáta og gjöld í símaveri</span><span class="sxs-lookup"><span data-stu-id="0a6fb-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="0a6fb-122">Grunnstilla beina markaðssetningu</span><span class="sxs-lookup"><span data-stu-id="0a6fb-122">Configure direct marketing</span></span>

[<span data-ttu-id="0a6fb-123">Vörulistar símavers</span><span class="sxs-lookup"><span data-stu-id="0a6fb-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="0a6fb-124">Setja upp greiningu nýleika-, tíðni- og peningastigs (RFM)</span><span class="sxs-lookup"><span data-stu-id="0a6fb-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="0a6fb-125">Grunnstilla samfelldniáætlun</span><span class="sxs-lookup"><span data-stu-id="0a6fb-125">Configure continuity programs</span></span>

[<span data-ttu-id="0a6fb-126">Setja upp samfelldniáætlanir fyrir símaver</span><span class="sxs-lookup"><span data-stu-id="0a6fb-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)

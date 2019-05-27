---
title: Söluvirkni símavers
description: Þessi grein veitir yfirlit yfir söluvirkni símavera í Microsoft Dynamics 365 for Retail.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8b78762ce70b318e1f77e1e49ffaa7b72f01667f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549481"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="d5d86-103">Söluvirkni símavers</span><span class="sxs-lookup"><span data-stu-id="d5d86-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5d86-104">Í Dynamics 365 for Retail er símaver tegund smásölurásar sem hægt er að skilgreina í forritinu.</span><span class="sxs-lookup"><span data-stu-id="d5d86-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="d5d86-105">Með því að skilgreina tiltekna rás fyrir símaverseiningar þínar er kerfinu gert kleift að binda ákveðin sjálfgildi gagna og sjálfgildi pöntunarvinnslu við sölupantanir sem búnar eru til af notanda símaversrásarinnar.</span><span class="sxs-lookup"><span data-stu-id="d5d86-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="d5d86-106">Eiginleikar símavers eru meðal annars ítarlegt smásöluverð og kynningar, vörulistar, gjafakort, vildarkerfi og afsláttarmiðar.</span><span class="sxs-lookup"><span data-stu-id="d5d86-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="d5d86-107">Símaverspantanir eru einnig notaðar af sölustað (POS) forritinu til að styðja við tilvik pöntunaruppfyllingar þvert á rásir.</span><span class="sxs-lookup"><span data-stu-id="d5d86-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="d5d86-108">Það er mikilvægt að hafa í huga að þótt aðrar atvinnugreinar utan smásölu geti nýtt sér kerfiseiningu símavers, hefur núverandi útgáfa Dynamics 365 for Retail símaversforritsins ekki verið fínstillt fyrir notkun í tilvikum vinnslu pantana á milli fyrirtækja (B2B), eða í tilvikum þar sem pantanir hafa mjög margar sölulínur.</span><span class="sxs-lookup"><span data-stu-id="d5d86-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="d5d86-109">Mælt er með því að notendur sem vilja nýta sér eiginleika símavers fyrir vinnslu pantana sem eru fyrir utan dæmigerða beint-til-neytanda færsluvinnslu, taki sér nægan tíma til að prófa og sannreyna að það að opna fyrir virkni símavers muni uppfylla þarfir um virkni og afköst.</span><span class="sxs-lookup"><span data-stu-id="d5d86-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="d5d86-110">Auk þess að styðja við stofnun pöntunar býður kerfiseining símavers einnig upp á notendavænt þjónustuforrit fyrir viðskiptavini sem auðveldar notendum að finna viðskiptavinareikninga og yfirfara öll tengd gögn og eigindir viðskiptavinapantana.</span><span class="sxs-lookup"><span data-stu-id="d5d86-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="d5d86-111">Þjónustuskjárinn fyrir viðskiptavini er hannaður til að gera notanda kleift að fá aðgang að gögnum tengdum pöntunum fljótt, sem gerir þeim kleift að svara algengustu spurningum tengdum pöntunum frá viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="d5d86-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="d5d86-112">Þessi síða veitir tengla á viðeigandi fylgiskjöl sem tengjast uppsetningu, grunnstillingu og notkunarvirkni eiginleika símaversins í Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="d5d86-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="d5d86-113">Grunnstilla símaverið</span><span class="sxs-lookup"><span data-stu-id="d5d86-113">Configure the call center</span></span>

[<span data-ttu-id="d5d86-114">Uppsetning valkosta pantanavinnslu</span><span class="sxs-lookup"><span data-stu-id="d5d86-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="d5d86-115">Grunnstilla pöntunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="d5d86-115">Configure order processing</span></span>

[<span data-ttu-id="d5d86-116">Uppsetning svikaviðvarana</span><span class="sxs-lookup"><span data-stu-id="d5d86-116">Set up fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="d5d86-117">Handvirk biðstaða pantana</span><span class="sxs-lookup"><span data-stu-id="d5d86-117">Manual Order Holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="d5d86-118">Grunnstilla greiðsluvinnslu</span><span class="sxs-lookup"><span data-stu-id="d5d86-118">Configure payment processing</span></span>

[<span data-ttu-id="d5d86-119">Greiðsluhættir í símaveri</span><span class="sxs-lookup"><span data-stu-id="d5d86-119">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="d5d86-120">Grunnstilla afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="d5d86-120">Configure delivery modes</span></span>

[<span data-ttu-id="d5d86-121">Grunnstilla afhendingarmáta og gjöld í símaveri</span><span class="sxs-lookup"><span data-stu-id="d5d86-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="d5d86-122">Grunnstilla beina markaðssetningu</span><span class="sxs-lookup"><span data-stu-id="d5d86-122">Configure direct marketing</span></span>

[<span data-ttu-id="d5d86-123">Vörulistar símavers</span><span class="sxs-lookup"><span data-stu-id="d5d86-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="d5d86-124">Uppsetning RFM-greiningar</span><span class="sxs-lookup"><span data-stu-id="d5d86-124">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="d5d86-125">Grunnstilla samfelldniáætlun</span><span class="sxs-lookup"><span data-stu-id="d5d86-125">Configure continuity programs</span></span>

[<span data-ttu-id="d5d86-126">Uppsetning samfelldniáætlunar fyrir símaver</span><span class="sxs-lookup"><span data-stu-id="d5d86-126">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)

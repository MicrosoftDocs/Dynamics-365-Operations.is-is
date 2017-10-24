---
title: "Pantanir í bið"
description: "Þetta efnisatriði lýsir pöntunum í bið með því að nota Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14dab07075a3f042e0095b912e51768ccb086f0e
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="order-holds"></a><span data-ttu-id="1892f-103">Pantanir í bið</span><span class="sxs-lookup"><span data-stu-id="1892f-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="1892f-104">Þetta efnisatriði lýsir pöntunum í bið með því að nota Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1892f-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="1892f-105">Hægt er að setja pöntun í bið af mismunandi ástæðum.</span><span class="sxs-lookup"><span data-stu-id="1892f-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="1892f-106">Til dæmis gætirðu sett pöntun í bið þar til hægt er að staðfesta aðsetur viðskiptavinar eða greiðsluhætti eða þar til stjórnandinn getur farið yfir lánamark viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="1892f-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="1892f-107">Meðan á söluferli stendur, eru tímar þegar sölupöntun verður að vera sett í bið.</span><span class="sxs-lookup"><span data-stu-id="1892f-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="1892f-108">Til dæmis gæti sölupöntunin verið í bið vegna vandamála við greiðslu viðskiptavinar, grunar um svik, eða hún bíður yfirferðar af stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="1892f-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="1892f-109">Þegar sölupöntun er sett í bið, er biðkóða pantana úthlutað til þess að tilgreina ástæðu fyrir biðpöntunina.</span><span class="sxs-lookup"><span data-stu-id="1892f-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="1892f-110">Biðkóðar sölupantana eru skilgreindir í **Sala og markaðssetning** &gt; **Uppsetning** &gt; **Sölupantanir** &gt; **Biðkóðar pantana**.</span><span class="sxs-lookup"><span data-stu-id="1892f-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="1892f-111">Hægt er að setja sölupöntun í bið handvirkt við stofnun pöntunarinnar eða síðar.</span><span class="sxs-lookup"><span data-stu-id="1892f-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="1892f-112">Þar að auki er hægt að setja pöntun í bið sjálfkrafa, byggt á reglum vegna svika.</span><span class="sxs-lookup"><span data-stu-id="1892f-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="1892f-113">Þegar sölupöntun er í bið gæti þurft að uppfæra hana með tilliti til frekari upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="1892f-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="1892f-114">Einnig gætir þú viljað skrá sölupöntunina út á meðan haldið er áfram að vinna í henni.</span><span class="sxs-lookup"><span data-stu-id="1892f-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="1892f-115">Hægt er að skrá út sölupöntun, skrá hana aftur inn og jafnvel hnekkja útskráningu gerða af öðrum notanda með því að nota biðpöntunarvinnusvæði (**Smásala** &gt; **Viðskiptavinur** &gt; **Pöntun í bið**).</span><span class="sxs-lookup"><span data-stu-id="1892f-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="1892f-116">Þegar pöntun er tilbúið til að ljúka, verður að fjarlægja þær úr bið áður en hægt er að ljúka við ferli.</span><span class="sxs-lookup"><span data-stu-id="1892f-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>





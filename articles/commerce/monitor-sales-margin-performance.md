---
title: Fylgjast með sölu og afköstum framlegðar
description: Hægt er að fylgjast með sölu og afköstum framlegðar í rauntíma með því að nota Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a7ea2bd9388e2fcfc6ae5f17d61054092cbac58c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796947"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="ddc39-103">Eftirlit með sölu og framlegð</span><span class="sxs-lookup"><span data-stu-id="ddc39-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ddc39-104">Hægt er að fylgjast með sölu og afköstum framlegðar í rauntíma með því að nota Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ddc39-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ddc39-105">Sem hluti af Commerce geta notendur fylgst með sölu og afköstum framlegðar í rauntíma milli mismunandi stiga í stigveldi fyrirtækis fyrir eftirfarandi víddir:</span><span class="sxs-lookup"><span data-stu-id="ddc39-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="ddc39-106">Vörur</span><span class="sxs-lookup"><span data-stu-id="ddc39-106">Products</span></span>
- <span data-ttu-id="ddc39-107">Flokkar</span><span class="sxs-lookup"><span data-stu-id="ddc39-107">Categories</span></span>
- <span data-ttu-id="ddc39-108">Afslættir</span><span class="sxs-lookup"><span data-stu-id="ddc39-108">Discounts</span></span>
- <span data-ttu-id="ddc39-109">Ár sem tímabil</span><span class="sxs-lookup"><span data-stu-id="ddc39-109">Years as time period</span></span>
- <span data-ttu-id="ddc39-110">Afgreiðslukassar/afgreiðslustöðvar</span><span class="sxs-lookup"><span data-stu-id="ddc39-110">Registers/terminals</span></span>
- <span data-ttu-id="ddc39-111">Starfsmaður/starfsmenn</span><span class="sxs-lookup"><span data-stu-id="ddc39-111">Staff/employees</span></span>
- <span data-ttu-id="ddc39-112">Viðskiptavinir</span><span class="sxs-lookup"><span data-stu-id="ddc39-112">Customers</span></span>
- <span data-ttu-id="ddc39-113">Rekstrareiningar</span><span class="sxs-lookup"><span data-stu-id="ddc39-113">Operating units</span></span>

<span data-ttu-id="ddc39-114">Þar að auki eru tvær einkvæmar skýrslur sem leyfa notendum að fylgjast með sölu og afköstum framlegðar með því að kafa niður frá efsta tegundahnúti niður á staka laufhnúta tegundarinnar í sjálfgefnu flokkastigveldi afurða. Þessar skýrslur nýta sér uppbyggingu stigveldishnita.</span><span class="sxs-lookup"><span data-stu-id="ddc39-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="ddc39-115">Notendur geta einnig kafað frá efstu rekstrareiningunum niður á einstakar rásir í stigveldi fyrirtækisins sem skilgreindur er sem sjálfgefið stigveldi fyrirtækis fyrir skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="ddc39-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="ddc39-116">Hægt er að opna skýrslurnar úr öllum af eftirfarandi stöðum:</span><span class="sxs-lookup"><span data-stu-id="ddc39-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="ddc39-117">**Stjórnun verslunar** vinnusvæði &gt; **Retail og Commerce** &gt; **Rásir** &gt; **Stjórnun verslana** &gt; **Skýrslur**</span><span class="sxs-lookup"><span data-stu-id="ddc39-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="ddc39-118">**Flokka- og afurðastjórnun** vinnusvæði &gt; **Retail og Commerce** &gt; **Afurð og flokkar** &gt; **Stjórnun verslana** &gt; **Skýrslur**</span><span class="sxs-lookup"><span data-stu-id="ddc39-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="ddc39-119">**Stjórnun verðlagningar og afslátta** vinnusvæði &gt; **Retail og Commerce** &gt; **Verðlagning og afslættir** &gt; **Stjórnun verslana** &gt; **Skýrslur**</span><span class="sxs-lookup"><span data-stu-id="ddc39-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="ddc39-120">**Fyrirspurnir og skýrslur** hlutinn &gt; **Retail og Commerce** &gt; **Fyrirspurnir og skýrslur** &gt; **Söluskýrslur**</span><span class="sxs-lookup"><span data-stu-id="ddc39-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
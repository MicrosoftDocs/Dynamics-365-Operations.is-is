---
title: Fylgjast með sölu og afköstum framlegðar
description: Hægt er að fylgjast með sölu og afköstum framlegðar í rauntíma með því að nota Dynamics 365 Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a7b2b6ba8115b43ef2e52e934bf8364e6f4044e7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413092"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="3241f-103">Eftirlit með sölu og framlegð</span><span class="sxs-lookup"><span data-stu-id="3241f-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3241f-104">Hægt er að fylgjast með sölu og afköstum framlegðar í rauntíma með því að nota Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3241f-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3241f-105">Sem hluti af Commerce geta notendur fylgst með sölu og afköstum framlegðar í rauntíma milli mismunandi stiga í stigveldi fyrirtækis fyrir eftirfarandi víddir:</span><span class="sxs-lookup"><span data-stu-id="3241f-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="3241f-106">Vörur</span><span class="sxs-lookup"><span data-stu-id="3241f-106">Products</span></span>
- <span data-ttu-id="3241f-107">Flokkar</span><span class="sxs-lookup"><span data-stu-id="3241f-107">Categories</span></span>
- <span data-ttu-id="3241f-108">Afslættir</span><span class="sxs-lookup"><span data-stu-id="3241f-108">Discounts</span></span>
- <span data-ttu-id="3241f-109">Ár sem tímabil</span><span class="sxs-lookup"><span data-stu-id="3241f-109">Years as time period</span></span>
- <span data-ttu-id="3241f-110">Afgreiðslukassar/afgreiðslustöðvar</span><span class="sxs-lookup"><span data-stu-id="3241f-110">Registers/terminals</span></span>
- <span data-ttu-id="3241f-111">Starfsmaður/starfsmenn</span><span class="sxs-lookup"><span data-stu-id="3241f-111">Staff/employees</span></span>
- <span data-ttu-id="3241f-112">Viðskiptavinir</span><span class="sxs-lookup"><span data-stu-id="3241f-112">Customers</span></span>
- <span data-ttu-id="3241f-113">Rekstrareiningar</span><span class="sxs-lookup"><span data-stu-id="3241f-113">Operating units</span></span>

<span data-ttu-id="3241f-114">Þar að auki eru tvær einkvæmar skýrslur sem leyfa notendum að fylgjast með sölu og afköstum framlegðar með því að kafa niður frá efsta tegundahnúti niður á staka laufhnúta tegundarinnar í sjálfgefnu flokkastigveldi afurða. Þessar skýrslur nýta sér uppbyggingu stigveldishnita.</span><span class="sxs-lookup"><span data-stu-id="3241f-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="3241f-115">Notendur geta einnig kafað frá efstu rekstrareiningunum niður á einstakar rásir í stigveldi fyrirtækisins sem skilgreindur er sem sjálfgefið stigveldi fyrirtækis fyrir skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="3241f-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="3241f-116">Hægt er að opna skýrslurnar úr öllum af eftirfarandi stöðum:</span><span class="sxs-lookup"><span data-stu-id="3241f-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="3241f-117">**Stjórnun verslunar** vinnusvæði &gt; **Retail og Commerce** &gt; **Rásir** &gt; **Stjórnun verslana** &gt; **Skýrslur**</span><span class="sxs-lookup"><span data-stu-id="3241f-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="3241f-118">**Flokka- og afurðastjórnun** vinnusvæði &gt; **Retail og Commerce** &gt; **Afurð og flokkar** &gt; **Stjórnun verslana** &gt; **Skýrslur**</span><span class="sxs-lookup"><span data-stu-id="3241f-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="3241f-119">**Stjórnun verðlagningar og afslátta** vinnusvæði &gt; **Retail og Commerce** &gt; **Verðlagning og afslættir** &gt; **Stjórnun verslana** &gt; **Skýrslur**</span><span class="sxs-lookup"><span data-stu-id="3241f-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="3241f-120">**Fyrirspurnir og skýrslur** hlutinn &gt; **Retail og Commerce** &gt; **Fyrirspurnir og skýrslur** &gt; **Söluskýrslur**</span><span class="sxs-lookup"><span data-stu-id="3241f-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>

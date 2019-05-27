---
title: Fylgjast með sölu og afköstum framlegðar
description: Hægt er að fylgjast með sölu og afköstum framlegðar í rauntíma með því að nota Microsoft Dynamics 365 for Retail.
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
ms.openlocfilehash: e2b3591f6403542c79457d12ae850ad40d9253a1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555651"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="66d45-103">Eftirlit með sölu og framlegð</span><span class="sxs-lookup"><span data-stu-id="66d45-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="66d45-104">Hægt er að fylgjast með sölu og afköstum framlegðar í rauntíma með því að nota Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="66d45-104">You can monitor sales and margin performance in real time using Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="66d45-105">Sem hluti af Dynamics 365 for Retail geta notendur fylgst með sölu og afköstum framlegðar í rauntíma milli mismunandi stiga í stigveldi fyrirtækis fyrir eftirfarandi víddir:</span><span class="sxs-lookup"><span data-stu-id="66d45-105">As part of Dynamics 365 for Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="66d45-106">Vörur</span><span class="sxs-lookup"><span data-stu-id="66d45-106">Products</span></span>
- <span data-ttu-id="66d45-107">Flokkar</span><span class="sxs-lookup"><span data-stu-id="66d45-107">Categories</span></span>
- <span data-ttu-id="66d45-108">Afslættir</span><span class="sxs-lookup"><span data-stu-id="66d45-108">Discounts</span></span>
- <span data-ttu-id="66d45-109">Ár sem tímabil</span><span class="sxs-lookup"><span data-stu-id="66d45-109">Years as time period</span></span>
- <span data-ttu-id="66d45-110">Afgreiðslukassar/afgreiðslustöðvar</span><span class="sxs-lookup"><span data-stu-id="66d45-110">Registers/terminals</span></span>
- <span data-ttu-id="66d45-111">Starfsmaður/starfsmenn</span><span class="sxs-lookup"><span data-stu-id="66d45-111">Staff/employees</span></span>
- <span data-ttu-id="66d45-112">Viðskiptavinir</span><span class="sxs-lookup"><span data-stu-id="66d45-112">Customers</span></span>
- <span data-ttu-id="66d45-113">Rekstrareiningar</span><span class="sxs-lookup"><span data-stu-id="66d45-113">Operating units</span></span>

<span data-ttu-id="66d45-114">Þar að auki eru tvær einkvæmar skýrslur sem leyfa notendum að fylgjast með sölu og afköstum framlegðar með því að kafa niður frá efsta tegundahnúti niður á staka laufhnúta tegundarinnar í sjálfgefnu flokkastigveldi smásöluafurða. Þessar skýrslur nýta sér uppbyggingu stigveldishnita.</span><span class="sxs-lookup"><span data-stu-id="66d45-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="66d45-115">Notendur geta einnig kafað frá efstu rekstrareiningunum niður á einstakar rásir í stigveldi fyrirtækisins sem skilgreindur er sem sjálfgefið stigveldi fyrirtækis fyrir skýrslugerð stigveldisins.</span><span class="sxs-lookup"><span data-stu-id="66d45-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="66d45-116">Hægt er að opna skýrslurnar úr öllum af eftirfarandi stöðum:</span><span class="sxs-lookup"><span data-stu-id="66d45-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="66d45-117">**Stjórnun smásöluverslunar** vinnusvæði&gt; **Smásala** &gt; **Rásir** &gt; **Stjórnun smásöluverslana** &gt; **Skýrslur**</span><span class="sxs-lookup"><span data-stu-id="66d45-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="66d45-118">**Flokka- og afurðastjórnun** vinnusvæði&gt; **Smásala** &gt; **Afurð og flokkar** &gt; **Stjórnun smásöluverslana** &gt; **Skýrslur**</span><span class="sxs-lookup"><span data-stu-id="66d45-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="66d45-119">**Stjórnun verðlagningar og afslátta** vinnusvæði &gt; **Smásala** &gt; **Verðlagning og afslættir** &gt; **Stjórnun smásöluverslana** &gt; **Skýrslur**</span><span class="sxs-lookup"><span data-stu-id="66d45-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="66d45-120">**Fyrirspurnir og skýrslur** hlutinn &gt; **Smásala** &gt; **Fyrirspurnir og skýrslur** &gt; **Söluskýrslur**</span><span class="sxs-lookup"><span data-stu-id="66d45-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>

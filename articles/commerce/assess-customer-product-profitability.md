---
title: Meta arðsemi viðskiptavinar og afurðar
description: Þessi grein útskýrir hvernig hægt er að nota greiningar í minni og rauntíma til að nálgast, skoða og fá innsýn í arðsemi viðskiptavina og afurða úr gögnum Dynamics 365 Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3218a29995791ce0d9a42d5b6d898d6e548f0f1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413136"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="4b681-103">Meta arðsemi viðskiptavinar og afurðar</span><span class="sxs-lookup"><span data-stu-id="4b681-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4b681-104">Þessi grein útskýrir hvernig hægt er að nota greiningar í minni og rauntíma til að nálgast, skoða og fá innsýn í arðsemi viðskiptavina og afurða úr gögnum Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4b681-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="4b681-105">Hluti af Commerce er að notendur geta skoðað arðsemisgreiningu stærstu viðskiptavina (10 til 100) milli mismunandi stiga í stigveldi fyrirtækisins, byggt á einu af eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="4b681-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="4b681-106">Söluupphæð</span><span class="sxs-lookup"><span data-stu-id="4b681-106">Sales amount</span></span>
- <span data-ttu-id="4b681-107">Magn</span><span class="sxs-lookup"><span data-stu-id="4b681-107">Quantity</span></span>
- <span data-ttu-id="4b681-108">Brúttóhagnaðarhlutfall</span><span class="sxs-lookup"><span data-stu-id="4b681-108">Gross profit margin</span></span>
- <span data-ttu-id="4b681-109">Framlegðarprósenta</span><span class="sxs-lookup"><span data-stu-id="4b681-109">Margin percentage</span></span>

<span data-ttu-id="4b681-110">Fyrir þetta mat, er hægt að nota „Út úr kassanum“ **Stærstu viðskiptavinir** skýrsluna sem hægt er að opna úr öllum af eftirfarandi stöðum:</span><span class="sxs-lookup"><span data-stu-id="4b681-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="4b681-111">**Verslunarstjórnun** vinnusvæði &gt; **Retail og Commerce** &gt; **Rásir** &gt; **Verslunarstjórnun** &gt; **Skýrslur** &gt; **Skýrsla um stærstu viðskiptavinina**</span><span class="sxs-lookup"><span data-stu-id="4b681-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="4b681-112">**Fyrirspurnir og skýrslur** hluti &gt; **Retail og Commerce** &gt; **Fyrirspurnir og skýrslur** &gt; **Söluskýrslur** &gt; **Skýrsla um stærstu viðskiptavinina**</span><span class="sxs-lookup"><span data-stu-id="4b681-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="4b681-113">Einnig geta notendur skoðað arðsemisgreiningu mest seldu varanna (10 til 100) milli mismunandi stiga í stigveldi fyrirtækisins, byggt á einu af eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="4b681-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="4b681-114">Söluupphæð</span><span class="sxs-lookup"><span data-stu-id="4b681-114">Sales amount</span></span>
- <span data-ttu-id="4b681-115">Magn</span><span class="sxs-lookup"><span data-stu-id="4b681-115">Quantity</span></span>
- <span data-ttu-id="4b681-116">Brúttóhagnaðarhlutfall</span><span class="sxs-lookup"><span data-stu-id="4b681-116">Gross profit margin</span></span>
- <span data-ttu-id="4b681-117">Framlegðarprósenta</span><span class="sxs-lookup"><span data-stu-id="4b681-117">Margin percentage</span></span>

<span data-ttu-id="4b681-118">Fyrir þetta mat, er hægt að nota „Út úr kassanum“ **Mest seldu vörurnar** skýrsluna sem hægt er að opna úr öllum af eftirfarandi stöðum:</span><span class="sxs-lookup"><span data-stu-id="4b681-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="4b681-119">**Verslunarstjórnun** vinnusvæði &gt; **Retail og Commerce** &gt; **Rásir** &gt; **Verslunarstjórnun** &gt; **Skýrslur** &gt; **Skýrsla um mest seldu afurðirnar**</span><span class="sxs-lookup"><span data-stu-id="4b681-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="4b681-120">**Flokka- og afurðastjórnun** vinnusvæði &gt; **Retail og Commerce** &gt; **Afurðir og flokkar** &gt; **Verslunarstjórnun** &gt; **Skýrslur** &gt; **Skýrsla yfir mest seldu afurðirnar**</span><span class="sxs-lookup"><span data-stu-id="4b681-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="4b681-121">**Fyrirspurnir og skýrslur** hluti &gt; **Retail og Commerce** &gt; **Fyrirspurnir og skýrslur** &gt; **Söluskýrslur** &gt; **Skýrsla um mest seldu afurðirnar**</span><span class="sxs-lookup"><span data-stu-id="4b681-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>

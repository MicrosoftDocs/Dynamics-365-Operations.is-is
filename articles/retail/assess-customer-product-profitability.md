---
title: Meta arðsemi viðskiptavinar og afurðar
description: Þessi grein útskýrir hvernig hægt er að nota greiningar í minni og rauntíma til að nálgast, skoða og fá innsýn í arðsemi viðskiptavina og afurða úr gögnum Dynamics 365 Retail.
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
ms.openlocfilehash: 5a9bebf948bd4602556f70a5a79690621a03261e
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023591"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="5428d-103">Meta arðsemi viðskiptavinar og afurðar</span><span class="sxs-lookup"><span data-stu-id="5428d-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5428d-104">Þessi grein útskýrir hvernig hægt er að nota greiningar í minni og rauntíma til að nálgast, skoða og fá innsýn í arðsemi viðskiptavina og afurða úr gögnum Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="5428d-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Retail data.</span></span>

<span data-ttu-id="5428d-105">Hluti af Retail er að notendur geta skoðað arðsemisgreiningu stærstu viðskiptavina (10 til 100) milli mismunandi stiga í stigveldi fyrirtækisins, byggt á einu af eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="5428d-105">As part of Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="5428d-106">Söluupphæð</span><span class="sxs-lookup"><span data-stu-id="5428d-106">Sales amount</span></span>
- <span data-ttu-id="5428d-107">Magn</span><span class="sxs-lookup"><span data-stu-id="5428d-107">Quantity</span></span>
- <span data-ttu-id="5428d-108">Brúttóhagnaðarhlutfall</span><span class="sxs-lookup"><span data-stu-id="5428d-108">Gross profit margin</span></span>
- <span data-ttu-id="5428d-109">Framlegðarprósenta</span><span class="sxs-lookup"><span data-stu-id="5428d-109">Margin percentage</span></span>

<span data-ttu-id="5428d-110">Fyrir þetta mat, er hægt að nota „Út úr kassanum“ **Stærstu viðskiptavinir** skýrsluna sem hægt er að opna úr öllum af eftirfarandi stöðum:</span><span class="sxs-lookup"><span data-stu-id="5428d-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="5428d-111">**Stjórnun smásöluverslunar** vinnusvæði &gt; **Smásala** &gt; **Rásir** &gt; **Stjórnun smásöluverslunar** &gt; **Skýrslur** &gt; **Skýrsla um stærstu viðskiptavinina**</span><span class="sxs-lookup"><span data-stu-id="5428d-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="5428d-112">**Fyrirspurnir og skýrslur** hlutinn &gt; **Smásala** &gt; **Fyrirspurnir og skýrslur** &gt; **Söluskýrslur** &gt; **Skýrsla um stærstu viðskiptavinina**</span><span class="sxs-lookup"><span data-stu-id="5428d-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="5428d-113">Einnig geta notendur skoðað arðsemisgreiningu mest seldu varanna (10 til 100) milli mismunandi stiga í stigveldi fyrirtækisins, byggt á einu af eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="5428d-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="5428d-114">Söluupphæð</span><span class="sxs-lookup"><span data-stu-id="5428d-114">Sales amount</span></span>
- <span data-ttu-id="5428d-115">Magn</span><span class="sxs-lookup"><span data-stu-id="5428d-115">Quantity</span></span>
- <span data-ttu-id="5428d-116">Brúttóhagnaðarhlutfall</span><span class="sxs-lookup"><span data-stu-id="5428d-116">Gross profit margin</span></span>
- <span data-ttu-id="5428d-117">Framlegðarprósenta</span><span class="sxs-lookup"><span data-stu-id="5428d-117">Margin percentage</span></span>

<span data-ttu-id="5428d-118">Fyrir þetta mat, er hægt að nota „Út úr kassanum“ **Mest seldu vörurnar** skýrsluna sem hægt er að opna úr öllum af eftirfarandi stöðum:</span><span class="sxs-lookup"><span data-stu-id="5428d-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="5428d-119">**Stjórnun smásöluverslunar** vinnusvæði &gt; **Smásala** &gt; **Rásir** &gt; **Stjórnun smásöluverslunar** &gt; **Skýrslur** &gt; **Skýrsla um mest seldu afurðirnar**</span><span class="sxs-lookup"><span data-stu-id="5428d-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="5428d-120">**Flokka- og afurðastjórnun** vinnusvæði &gt; **Smásala** &gt; **Afurðir og flokkar** &gt; **Stjórnun smásöluverslana** &gt; **Skýrslur** &gt; **Skýrsla yfir mest seldu afurðirnar**</span><span class="sxs-lookup"><span data-stu-id="5428d-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="5428d-121">**Fyrirspurnir og skýrslur** hlutinn &gt; **Smásala** &gt; **Fyrirspurnir og skýrslur** &gt; **Söluskýrslur** &gt; **Skýrsla um mest seldu afurðirnar**</span><span class="sxs-lookup"><span data-stu-id="5428d-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>

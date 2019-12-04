---
title: Samþættur skattur
description: Þetta efni lýsir samþættingu skattaupplýsinga milli Finance and Operations og Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b6be53e9a2065373ca37c2791568a8161823803f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772411"
---
## <a name="integrated-tax"></a><span data-ttu-id="98be4-103">Samþættur skattur</span><span class="sxs-lookup"><span data-stu-id="98be4-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98be4-104">Skattuppsetningargögn skilgreina uppsetningu bæði á óbeinum sköttum (VSK, GST, virðisaukaskattur) og staðgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="98be4-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="98be4-105">Það lýsir skattaútreikningsreglu, skatthlutfalli, skattabókhaldi, uppgjöri og öðrum hugtökum.</span><span class="sxs-lookup"><span data-stu-id="98be4-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="98be4-106">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="98be4-106">Templates</span></span>

<span data-ttu-id="98be4-107">Skattaupplýsingar innihalda safn af einingaspjöldum sem virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="98be4-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="98be4-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="98be4-108">Finance and Operations</span></span>   | <span data-ttu-id="98be4-109">Forritið Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="98be4-109">Customer Engagement application</span></span>
-------------------------|---------------------------------
<span data-ttu-id="98be4-110">Skattkóðar</span><span class="sxs-lookup"><span data-stu-id="98be4-110">Tax codes</span></span>                  | <span data-ttu-id="98be4-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="98be4-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="98be4-112">Skattflokkar</span><span class="sxs-lookup"><span data-stu-id="98be4-112">Tax groups</span></span>               | <span data-ttu-id="98be4-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="98be4-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="98be4-114">Vöruskattflokkar</span><span class="sxs-lookup"><span data-stu-id="98be4-114">Tax item groups</span></span>          | <span data-ttu-id="98be4-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="98be4-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="98be4-116">Skattaundanþágur</span><span class="sxs-lookup"><span data-stu-id="98be4-116">Tax Exemptions</span></span>           | <span data-ttu-id="98be4-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="98be4-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="98be4-118">Skattayfirvöld</span><span class="sxs-lookup"><span data-stu-id="98be4-118">Tax Authorities</span></span>          | <span data-ttu-id="98be4-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="98be4-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="98be4-120">Staðgreiðsluskattskóðar</span><span class="sxs-lookup"><span data-stu-id="98be4-120">Withholding tax codes</span></span>      | <span data-ttu-id="98be4-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="98be4-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="98be4-122">Staðgreiðsluskattsflokkar</span><span class="sxs-lookup"><span data-stu-id="98be4-122">Withholding tax groups</span></span>   | <span data-ttu-id="98be4-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="98be4-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="98be4-124">Fjárhagslykilshópur fyrir skatt</span><span class="sxs-lookup"><span data-stu-id="98be4-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="98be4-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="98be4-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]


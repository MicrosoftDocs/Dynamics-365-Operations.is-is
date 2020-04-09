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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173086"
---
# <a name="integrated-tax"></a><span data-ttu-id="e3779-103">Samþættur skattur</span><span class="sxs-lookup"><span data-stu-id="e3779-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e3779-104">Skattuppsetningargögn skilgreina uppsetningu bæði á óbeinum sköttum (VSK, GST, virðisaukaskattur) og staðgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="e3779-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="e3779-105">Það lýsir skattaútreikningsreglu, skatthlutfalli, skattabókhaldi, uppgjöri og öðrum hugtökum.</span><span class="sxs-lookup"><span data-stu-id="e3779-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="e3779-106">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="e3779-106">Templates</span></span>

<span data-ttu-id="e3779-107">Skattaupplýsingar innihalda safn af einingaspjöldum sem virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="e3779-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="e3779-108">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="e3779-108">Finance and Operations apps</span></span> | <span data-ttu-id="e3779-109">Líkanadrifin forrit í Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e3779-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="e3779-110">lýsing</span><span class="sxs-lookup"><span data-stu-id="e3779-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="e3779-111">Skattkóðar</span><span class="sxs-lookup"><span data-stu-id="e3779-111">Tax codes</span></span>                   | <span data-ttu-id="e3779-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e3779-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="e3779-113">Skattflokkar</span><span class="sxs-lookup"><span data-stu-id="e3779-113">Tax groups</span></span>                 | <span data-ttu-id="e3779-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e3779-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="e3779-115">Vöruskattflokkar</span><span class="sxs-lookup"><span data-stu-id="e3779-115">Tax item groups</span></span>             | <span data-ttu-id="e3779-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="e3779-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="e3779-117">Skattaundanþágur</span><span class="sxs-lookup"><span data-stu-id="e3779-117">Tax Exemptions</span></span>             | <span data-ttu-id="e3779-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="e3779-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="e3779-119">Skattayfirvöld</span><span class="sxs-lookup"><span data-stu-id="e3779-119">Tax Authorities</span></span>             | <span data-ttu-id="e3779-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="e3779-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="e3779-121">Staðgreiðsluskattskóðar</span><span class="sxs-lookup"><span data-stu-id="e3779-121">Withholding tax codes</span></span>       | <span data-ttu-id="e3779-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e3779-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="e3779-123">Staðgreiðsluskattsflokkar</span><span class="sxs-lookup"><span data-stu-id="e3779-123">Withholding tax groups</span></span>     | <span data-ttu-id="e3779-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e3779-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="e3779-125">Fjárhagslykilshópur fyrir skatt</span><span class="sxs-lookup"><span data-stu-id="e3779-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="e3779-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="e3779-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]


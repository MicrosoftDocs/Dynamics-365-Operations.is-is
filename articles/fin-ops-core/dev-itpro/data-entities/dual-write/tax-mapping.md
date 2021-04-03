---
title: Samþættur skattur
description: Þetta efni lýsir samþættingu skattaupplýsinga milli Finance and Operations og Dataverse.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7501ef21492a96c81b971e1d9077beaba9be897b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560338"
---
# <a name="integrated-tax"></a><span data-ttu-id="54cc4-103">Samþættur skattur</span><span class="sxs-lookup"><span data-stu-id="54cc4-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="54cc4-104">Skattuppsetningargögn skilgreina uppsetningu bæði á óbeinum sköttum (VSK, GST, virðisaukaskattur) og staðgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="54cc4-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="54cc4-105">Það lýsir skattaútreikningsreglu, skatthlutfalli, skattabókhaldi, uppgjöri og öðrum hugtökum.</span><span class="sxs-lookup"><span data-stu-id="54cc4-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="54cc4-106">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="54cc4-106">Templates</span></span>

<span data-ttu-id="54cc4-107">Skattagögn innihalda safn af töflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="54cc4-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="54cc4-108">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="54cc4-108">Finance and Operations apps</span></span> | <span data-ttu-id="54cc4-109">Líkanadrifin forrit í Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="54cc4-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="54cc4-110">lýsing</span><span class="sxs-lookup"><span data-stu-id="54cc4-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="54cc4-111">VSK-flokkur vöru</span><span class="sxs-lookup"><span data-stu-id="54cc4-111">Item sales tax group</span></span> | <span data-ttu-id="54cc4-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="54cc4-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="54cc4-113">Skattayfirvöld</span><span class="sxs-lookup"><span data-stu-id="54cc4-113">Sales tax authorities</span></span> | <span data-ttu-id="54cc4-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="54cc4-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="54cc4-115">Eining undanþágukóða virðisaukaskatts fyrir CDS</span><span class="sxs-lookup"><span data-stu-id="54cc4-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="54cc4-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="54cc4-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="54cc4-117">VSK-flokkar</span><span class="sxs-lookup"><span data-stu-id="54cc4-117">Sales tax groups</span></span> | <span data-ttu-id="54cc4-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="54cc4-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="54cc4-119">Fjárhagsbókunarflokkar virðisaukaskatts V2</span><span class="sxs-lookup"><span data-stu-id="54cc4-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="54cc4-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="54cc4-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="54cc4-121">Staðgreiðsluskattskóðar</span><span class="sxs-lookup"><span data-stu-id="54cc4-121">Withholding tax codes</span></span> | <span data-ttu-id="54cc4-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="54cc4-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="54cc4-123">Staðgreiðsluskattsflokkar</span><span class="sxs-lookup"><span data-stu-id="54cc4-123">Withholding tax groups</span></span> | <span data-ttu-id="54cc4-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="54cc4-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
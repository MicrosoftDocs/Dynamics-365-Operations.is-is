---
title: Samþætting nærrirauntímagagna á milli Finance and Operations og Common Data Service.
description: Þetta efnisatriði veitir yfirlit yfir samþættingu á milli Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797229"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a><span data-ttu-id="f36d9-103">Samþætting nærrirauntímagagna á milli Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f36d9-103">Near-real-time data integration between Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="f36d9-104">Í núverandi stafræna heimi nota vistkerfi fyrirtækja Microsoft Dynamics 365 pakkann sem heild.</span><span class="sxs-lookup"><span data-stu-id="f36d9-104">In the current digital world, business ecosystems use the Microsoft Dynamics 365 suite as a whole.</span></span> <span data-ttu-id="f36d9-105">Vegna þess að gögn frá fólki, viðskiptavinum, aðgerðum og Internet of Things (IoT) tækjum streyma inn í eina uppsprettu er tækifæri fyrir stafrænar endurgjafarlykkjur.</span><span class="sxs-lookup"><span data-stu-id="f36d9-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="f36d9-106">Til að ná þessari reynslu er samþætting á milli Dynamics 365 for Finance and Operations og Dynamics 365 fyrir forritið Customer Engagement nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="f36d9-106">To achieve this experience, integration between Dynamics 365 for Finance and Operations and Dynamics 365 for Customer Engagement applications is essential.</span></span> <span data-ttu-id="f36d9-107">Forrit Customer Engagement eru byggð ofan á Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f36d9-107">Customer Engagement applications are built on top of Common Data Service.</span></span> <span data-ttu-id="f36d9-108">Sameining gagna Finance and Operations við Common Data Service gerir forritum Customer Engagement kleift að eiga samræmd og lipur samskipti við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f36d9-108">Integration between Finance and Operations data with Common Data Service lets Customer Engagement applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="f36d9-109">Finance and Operations og Common Data Service bjóða upp á samstillingu gagna í rauntíma milli forritanna Finance and Operations og Customer Engagement með tvískiptum ramma.</span><span class="sxs-lookup"><span data-stu-id="f36d9-109">Finance and Operations and Common Data Service provide near-real-time data synchronization between Finance and Operations and Customer Engagement applications via a dual-write framework.</span></span> <span data-ttu-id="f36d9-110">Umfjöllunin er breið og spannar 28 yfirborðssvið Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f36d9-110">The coverage is broad and spans 28 surface areas of Finance and Operations.</span></span> <span data-ttu-id="f36d9-111">Markmiðið er að bjóða upp á „One Dynamics 365“ notendaupplifun með óaðfinnanlegu gagnastreymi sem tengir viðskiptaferla milli forrita.</span><span class="sxs-lookup"><span data-stu-id="f36d9-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Yfirlitsmynd arkitektúrs](media/dual-write-overview.jpg)

<span data-ttu-id="f36d9-113">Eftirfarandi gildistillögur eru í boði fyrir viðskiptavini:</span><span class="sxs-lookup"><span data-stu-id="f36d9-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="f36d9-114">Stigveldi fyrirtækis í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f36d9-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="f36d9-115">Fyrirtækishugtak í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f36d9-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="f36d9-116">Samþættur aðalviðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="f36d9-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="f36d9-117">Samþættur aðallánardrottinn</span><span class="sxs-lookup"><span data-stu-id="f36d9-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="f36d9-118">Sameinað afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="f36d9-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="f36d9-119">Kerfiskröfur</span><span class="sxs-lookup"><span data-stu-id="f36d9-119">System requirements</span></span>

<span data-ttu-id="f36d9-120">Samstillt, tvíátta, nær rauntíma gagnaflæði krefst eftirfarandi útgáfa:</span><span class="sxs-lookup"><span data-stu-id="f36d9-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="f36d9-121">Microsoft Dynamics 365 for Finance and Operations útgáfa 10.0.4 (júlí 2019) með verkvangsuppfærslu 28 eða hærra</span><span class="sxs-lookup"><span data-stu-id="f36d9-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="f36d9-122">Microsoft Dynamics 365 for Customer Engagement útgáfa 9.1. (4.2) eða nýrri</span><span class="sxs-lookup"><span data-stu-id="f36d9-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="f36d9-123">Leiðbeiningar um uppsetningu</span><span class="sxs-lookup"><span data-stu-id="f36d9-123">Setup instructions</span></span>

<span data-ttu-id="f36d9-124">Fylgdu þessum skrefum til að setja upp samþættingu á milli Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f36d9-124">Follow these steps to set up integration between Finance and Operations and Common Data Service.</span></span>
    
1. <span data-ttu-id="f36d9-125">Upplýsingar um uppsetningu tvískiptakerfisins er að finna í [skref-fyrir-skref leiðbeiningar](https://aka.ms/dualwrite-docs) um tilkynningu forskoðunar á tvöföldum skrifum.</span><span class="sxs-lookup"><span data-stu-id="f36d9-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="f36d9-126">Sæktu og settu upp lausnina úr [Finance and Operations, Common Data Service og samþættingu Customer Engagement](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer hópur.</span><span class="sxs-lookup"><span data-stu-id="f36d9-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="f36d9-127">Pakkinn inniheldur fimm lausnir:</span><span class="sxs-lookup"><span data-stu-id="f36d9-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="f36d9-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="f36d9-128">Dynamics365Company</span></span>
    + <span data-ttu-id="f36d9-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="f36d9-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="f36d9-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="f36d9-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="f36d9-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="f36d9-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="f36d9-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="f36d9-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="f36d9-133">Fylgdu framkvæmdarskipuninni fyrir [samstilla fyrstu tilvísunargögn](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="f36d9-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="f36d9-134">Ef þú lendir í tvískiptum samstillingarvandamálum skaltu skoða [Úrræðaleiðbeiningar fyrir samþættingu gagna](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="f36d9-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f36d9-135">Þú getur ekki keyrt tvískipt skrif og [Viðfang til sjóðsstreymis](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="f36d9-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="f36d9-136">Ef þú ert að keyra lausnina Viðfang til sjóðsstreymis verður þú að fjarlægja hana.</span><span class="sxs-lookup"><span data-stu-id="f36d9-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="f36d9-137">Þú verður einnig að slökkva á tvöföldum skrifasniðmátum viðskiptavinar og lánardrottins sem eru hluti af lausninni Viðfang til sjóðsstreymis.</span><span class="sxs-lookup"><span data-stu-id="f36d9-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>

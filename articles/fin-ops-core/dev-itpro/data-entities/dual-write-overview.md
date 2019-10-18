---
title: Samþætting nærrirauntímagagna á milli Finance and Operations og Common Data Service.
description: Þetta efni veitir yfirlit yfir samþættingu á milli Finance and Operations og Common Data Service.
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
ms.openlocfilehash: b7d9e6be6fb2fef85bcf1182f89b8e370abea3d6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184486"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="ba0c6-103">Samþætting gagna í næstum rauntíma við Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ba0c6-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="ba0c6-104">Í núverandi stafrænum heimi nota vistkerfi fyrirtækja Microsoft Dynamics 365 forritin sem heild.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="ba0c6-105">Vegna þess að gögn frá fólki, viðskiptavinum, aðgerðum og Internet of Things (IoT) tækjum streyma inn í eina uppsprettu er tækifæri fyrir stafrænar endurgjafarlykkjur.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="ba0c6-106">Til að ná þessari reynslu er samþætting á milli forrita Finance and Operations og annarra forrita Dynamics 365 nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="ba0c6-107">Sum forrit eru byggð ofan á Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="ba0c6-108">Sameining gagna á milli forrita Finance and Operations við Common Data Service gerir öðrum forritum kleift að eiga samræmd og lipur samskipti við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="ba0c6-109">Forrit Finance and Operations og Common Data Service bjóða upp á samstillingu gagna í rauntíma milli forrita Finance and Operations og annarra forrita Dynamics 365 með tvískiptum ramma.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="ba0c6-110">Umfjöllunin er breið og spannar 28 yfirborðssvið í forritinu.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="ba0c6-111">Markmiðið er að bjóða upp á „One Dynamics 365“ notendaupplifun með óaðfinnanlegu gagnastreymi sem tengir viðskiptaferla milli forrita.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Yfirlitsmynd arkitektúrs](media/dual-write-overview.jpg)

<span data-ttu-id="ba0c6-113">Eftirfarandi gildistillögur eru í boði fyrir viðskiptavini:</span><span class="sxs-lookup"><span data-stu-id="ba0c6-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="ba0c6-114">Stigveldi fyrirtækis í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ba0c6-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="ba0c6-115">Fyrirtækishugtak í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ba0c6-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="ba0c6-116">Samþættur aðalviðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="ba0c6-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="ba0c6-117">Samþættur aðallánardrottinn</span><span class="sxs-lookup"><span data-stu-id="ba0c6-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="ba0c6-118">Sameinað afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="ba0c6-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="ba0c6-119">Kerfiskröfur</span><span class="sxs-lookup"><span data-stu-id="ba0c6-119">System requirements</span></span>

<span data-ttu-id="ba0c6-120">Samstillt, tvíátta, nær rauntíma gagnaflæði krefst eftirfarandi útgáfa:</span><span class="sxs-lookup"><span data-stu-id="ba0c6-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="ba0c6-121">Microsoft Dynamics 365 for Finance and Operations útgáfa 10.0.4 (júlí 2019) með verkvangsuppfærslu 28 eða hærra</span><span class="sxs-lookup"><span data-stu-id="ba0c6-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="ba0c6-122">Microsoft Dynamics 365 for Customer Engagement útgáfa 9.1. (4.2) eða nýrri</span><span class="sxs-lookup"><span data-stu-id="ba0c6-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="ba0c6-123">Leiðbeiningar um uppsetningu</span><span class="sxs-lookup"><span data-stu-id="ba0c6-123">Setup instructions</span></span>

<span data-ttu-id="ba0c6-124">Fylgdu þessum skrefum til að setja upp samþættingu á milli forritum Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-124">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="ba0c6-125">Upplýsingar um uppsetningu tvískiptakerfisins er að finna í [skref-fyrir-skref leiðbeiningar](https://aka.ms/dualwrite-docs) um tilkynningu forskoðunar á tvöföldum skrifum.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="ba0c6-126">Sæktu og settu upp lausnina úr [Finance and Operations, Common Data Service og samþættingu Customer Engagement](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer hópur.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="ba0c6-127">Pakkinn inniheldur fimm lausnir:</span><span class="sxs-lookup"><span data-stu-id="ba0c6-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="ba0c6-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="ba0c6-128">Dynamics365Company</span></span>
    + <span data-ttu-id="ba0c6-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="ba0c6-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="ba0c6-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="ba0c6-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="ba0c6-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="ba0c6-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="ba0c6-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="ba0c6-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="ba0c6-133">Fylgdu framkvæmdarskipuninni fyrir [samstilla fyrstu tilvísunargögn](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="ba0c6-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="ba0c6-134">Ef þú lendir í tvískiptum samstillingarvandamálum skaltu skoða [Úrræðaleiðbeiningar fyrir samþættingu gagna](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="ba0c6-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba0c6-135">Þú getur ekki keyrt tvískipt skrif og [Viðfang til sjóðsstreymis](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="ba0c6-136">Ef þú ert að keyra lausnina Viðfang til sjóðsstreymis verður þú að fjarlægja hana.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="ba0c6-137">Þú verður einnig að slökkva á tvöföldum skrifasniðmátum viðskiptavinar og lánardrottins sem eru hluti af lausninni Viðfang til sjóðsstreymis.</span><span class="sxs-lookup"><span data-stu-id="ba0c6-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>

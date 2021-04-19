---
title: algengar spurningar um Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce matsumhverfi.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e42618a522f5ad551f608605300c30b5ffb8e299
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795932"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="dbfe1-103">Dynamics 365 Commerce algengar spurningar um matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="dbfe1-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dbfe1-104">Þetta efnisatriði veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce matsumhverfi.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="dbfe1-105">**Er hægt að nota Commerce-matsumhverfi sem netverslun rafrænna viðskipta fyrir viðskiptavini sem innleiða smásölu eins og er?**</span><span class="sxs-lookup"><span data-stu-id="dbfe1-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="dbfe1-106">Nei.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-106">No.</span></span> <span data-ttu-id="dbfe1-107">Commerce-matsumhverfi er aðeins fyrir mat.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="dbfe1-108">Ef þú þarft umhverfi fyrir viðskiptavini sem útfærir Retail skaltu hafa samband við Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="dbfe1-109">**Er hægt að nota Commerce-matsumhverfi til að úthluta eiginleikum rafrænna viðskipta ásamt fyrirliggjandi forriti/umhverfi sem innleiðir smásölu?**</span><span class="sxs-lookup"><span data-stu-id="dbfe1-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="dbfe1-110">Nei (aðallega).</span><span class="sxs-lookup"><span data-stu-id="dbfe1-110">No (mostly).</span></span> <span data-ttu-id="dbfe1-111">Íhlutir Commerce-mats eru aðeins í boði fyrir umhverfi sem samsvarar skilgreiningum sem eru tilgreindar í skilyrðum og úthlutunarleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="dbfe1-112">Þar að auki verða nauðsynleg grunnsýnigögn ekki tiltæk í umhverfum sem voru sett upp með upphaflegri útgáfu sem er eldri en 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="dbfe1-113">**Hvaða kostnaður fylgir því að setja upp Commerce-matsumhverfi á Microsoft Azure í gegnum Microsoft Dynamics Lifecycle Services?**</span><span class="sxs-lookup"><span data-stu-id="dbfe1-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="dbfe1-114">Hefðbundið Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce sýniútgáfuumhverfi höfuðstöðva (sýndarvél \[SV\]) verður hýst í Azure-áskriftinni þinni.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="dbfe1-115">Þú getur notað [Reiknivél fyrir verðlagningu í Azure](https://azure.microsoft.com/pricing/calculator/) að áætla þennan kostnað.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="dbfe1-116">Aðrir þættir, svo sem Commerce Scale Unit, Commerce-vefsmiður og rafræna viðskiptasvæðið þitt verða í boði sem SaaS-þjónusta og hýst af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="dbfe1-117">**Hvaða löng og svæði Azure eru studd eins og er fyrir Commerce-matsumhverfið?**</span><span class="sxs-lookup"><span data-stu-id="dbfe1-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="dbfe1-118">Aðeins er hægt að nota Commerce-matsumhverfið á svæðum Norður-Ameríku.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="dbfe1-119">**Er til niðurhalanlegur sýndardiskur (VHD) sem hefur fullkominn OneBox sýndarvél (VM) valkost?**</span><span class="sxs-lookup"><span data-stu-id="dbfe1-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="dbfe1-120">Dynamics 365 Commerce og Commerce Scale Unit eru SaaS-þjónusta og verða að vera hýst í skýinu.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="dbfe1-121">**Hversu lengi er hægt að nota matsumhverfi í Commerce?**</span><span class="sxs-lookup"><span data-stu-id="dbfe1-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="dbfe1-122">Commerce-matsumhverfið er með 30 daga gildistíma frá þeim degi þegar SaaS-íhlutir á borð við Commerce Scale Unit, Commerce-vefsmiður og rafrænt viðskiptasvæðið þitt er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="dbfe1-123">**Get ég framlengt tímamörkunum fyrir matsumhverfið mitt í Commerce?**</span><span class="sxs-lookup"><span data-stu-id="dbfe1-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="dbfe1-124">Framlenging á tímamörkum er undantekning sem þarf að skoða sérstaklega fyrir hvert mál.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="dbfe1-125">Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð.</span><span class="sxs-lookup"><span data-stu-id="dbfe1-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbfe1-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="dbfe1-126">Additional resources</span></span>

[<span data-ttu-id="dbfe1-127">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="dbfe1-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="dbfe1-128">Úthluta Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="dbfe1-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="dbfe1-129">Stilla Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="dbfe1-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="dbfe1-130">Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="dbfe1-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="dbfe1-131">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="dbfe1-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
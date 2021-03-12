---
title: Eining kökusamþykkis
description: Þetta efnisatriði fjallar um einingar kökusamþykkis og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 504232285267fb3663093a84a371e0040233ce23
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993526"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="86b70-103">Eining kökusamþykkis</span><span class="sxs-lookup"><span data-stu-id="86b70-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86b70-104">Þetta efnisatriði fjallar um einingar kökusamþykkis og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86b70-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="86b70-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="86b70-105">Overview</span></span>

<span data-ttu-id="86b70-106">Eining kökusamþykkis biður notendur vefsvæðis um að veita sérstaklega samþykki fyrir kökum fyrir alla eiginleika eða einingar sem rekja vafrakökur.</span><span class="sxs-lookup"><span data-stu-id="86b70-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="86b70-107">Samþykki er nauðsynlegt í fyrsta skipti sem notandi skoðar svæði í nýrri vafralotu.</span><span class="sxs-lookup"><span data-stu-id="86b70-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="86b70-108">Þegar samþykki er móttekið er það rakið og notandinn er ekki beðinn um samþykki aftur.</span><span class="sxs-lookup"><span data-stu-id="86b70-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="86b70-109">Nánari upplýsingar eru í [Reglufylgni köku](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="86b70-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="86b70-110">Ef samþykki fyrir kökum er ekki móttekið birtast eiginleikar eða einingar sem þurfa samþykki köku ekki á síðunni.</span><span class="sxs-lookup"><span data-stu-id="86b70-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="86b70-111">Til dæmis krefst greiðslueining, samfélagsmiðlaeining og eiginleiki æskilegrar verslunar samþykkis köku og birtast ekki ef samþykki er ekki móttekið.</span><span class="sxs-lookup"><span data-stu-id="86b70-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="86b70-112">Hægt er að stilla einingu fyrir kökusamþykki á hausbroti síðu til að hægt sé að framfylgja því þegar síðu er hlaðið.</span><span class="sxs-lookup"><span data-stu-id="86b70-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="86b70-113">Samþykkiseining kökunnar á að vera með skýrum skilaboðum sem upplýsa notanda vefsvæðisins um notkun á kökunni á vefsvæðinu og ætti að veita tengil á persónuverndarsíðu svæðisins.</span><span class="sxs-lookup"><span data-stu-id="86b70-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="86b70-114">Eftirfarandi mynd sýnir dæmi um kökusamþykkisskilaboðum með tengli á persónuverndarstefnu svæðisins sem birtist á haus vefsvæðis.</span><span class="sxs-lookup"><span data-stu-id="86b70-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="86b70-115">![Dæmi um einingu fyrir kökusamþykki](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="86b70-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="86b70-116">Einingareiginleikar kökusamþykkis</span><span class="sxs-lookup"><span data-stu-id="86b70-116">Cookie consent module properties</span></span>

| <span data-ttu-id="86b70-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="86b70-117">Property name</span></span>             | <span data-ttu-id="86b70-118">Virði</span><span class="sxs-lookup"><span data-stu-id="86b70-118">Value</span></span>                 | <span data-ttu-id="86b70-119">lýsing</span><span class="sxs-lookup"><span data-stu-id="86b70-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="86b70-120">Sniðinn texti</span><span class="sxs-lookup"><span data-stu-id="86b70-120">Rich Text</span></span>                  | <span data-ttu-id="86b70-121">Sniðinn texti</span><span class="sxs-lookup"><span data-stu-id="86b70-121">Rich Text</span></span> | <span data-ttu-id="86b70-122">Tilgreinir tilkynningu sniðins text til notenda síðunnar um að vefsvæðið notar vafrakökur og að notendur ættu að samþykkja fulla virkni fyrir notkun á kökum.</span><span class="sxs-lookup"><span data-stu-id="86b70-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="86b70-123">Tenglar</span><span class="sxs-lookup"><span data-stu-id="86b70-123">Links</span></span> | <span data-ttu-id="86b70-124">URL</span><span class="sxs-lookup"><span data-stu-id="86b70-124">URL</span></span> | <span data-ttu-id="86b70-125">Hægt er að bæta einum eða fleiri tenglum við persónuverndarsíðu svæðis sem lýsir þeim gerðum af kökum sem raktar eru á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="86b70-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="86b70-126">Bæta við samþykkiseiningu fyrir köku á síður svæðis</span><span class="sxs-lookup"><span data-stu-id="86b70-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="86b70-127">Til að hægt sé að bæta samþykkiseiningu köku við margar svæðissíður má bæta henni við samnýtt brot síðuhauss.</span><span class="sxs-lookup"><span data-stu-id="86b70-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="86b70-128">Eftir að hausbrotum er bætt við allar síður verður tilkynning um kökusamþykki sjálfkrafa birti í fyrsta skipti sem notandi sem er á svæðinu fer yfir á einhverja síðu.</span><span class="sxs-lookup"><span data-stu-id="86b70-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="86b70-129">Frekari upplýsingar um síðubrot og einingar má finna í [Hauseining](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="86b70-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86b70-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="86b70-130">Additional resources</span></span>

[<span data-ttu-id="86b70-131">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="86b70-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="86b70-132">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="86b70-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="86b70-133">Reglufylgni köku</span><span class="sxs-lookup"><span data-stu-id="86b70-133">Cookie compliance</span></span>](cookie-compliance.md)

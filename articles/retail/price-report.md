---
title: Smásöluverðskýrslur
description: Þetta efnisatriði veitir yfirlit yfir verðskýrslueiginleikann sem hægt er að nota til að skoða væntanlegar verðbreytingar á völdum afurðum.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 72f4d248f3ac49bbfd8e5a7a12352d92b89bb0eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564948"
---
# <a name="retail-price-reports"></a><span data-ttu-id="c9bf9-103">Smásöluverðskýrslur</span><span class="sxs-lookup"><span data-stu-id="c9bf9-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="c9bf9-104">Til þess að geta veitt viðskiptavinum sínum samkeppnishæf verð breyta söluaðliar oft verðum á afurðum.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="c9bf9-105">Verslunarstjórar vilja nálgast á auðveldan hátt nýlegar eða væntanlegar verðbreytingar svo þeir geti gert áætlun um nauðsynleg tilföng til að uppfæra verðmerkingar sem sjást í hillum verslunar.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="c9bf9-106">Með útgáfu 10.0 af Dynamics 365 for Retail getur verslunarstjóri opnað skýrsluna **Verð** með því að fletta upp á **Allar smásöluverslanir \> Verslun \> Verðskýrsla** og skoða uppfærð verð fyrir afurðirnar sem tengjast versluninni.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-106">With release 10.0 of Dynamics 365 for Retail, a store manager can open the **Price** report by navigating to **All retail stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="c9bf9-107">Til að virkja verðskýrsluna verður að kveikja á færibreytunni **Virkja verðskýrslu fyrir smásöluverslun**.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-107">To enable the price report, the **Enable price report for Retail store** parameter must be turned on.</span></span> <span data-ttu-id="c9bf9-108">Þessi færibreyta er staðsett í flipanum **Smásölufæribreytur \> Afslættir \> Ýmislegt**. Þegar síðan **Verðskýrsla** er opnuð birtist svargluggi með ýmsum skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-108">This parameter is located on the **Retail parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="c9bf9-109">Tiltækar skilgreiningar eru sýndar hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="c9bf9-110">Grunnstilling</span><span class="sxs-lookup"><span data-stu-id="c9bf9-110">Configuration</span></span> | <span data-ttu-id="c9bf9-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="c9bf9-111">Description</span></span> |
|---|---|
| <span data-ttu-id="c9bf9-112">Frá dagsetningu / Til dagsetningar</span><span class="sxs-lookup"><span data-stu-id="c9bf9-112">From date / To date</span></span>| <span data-ttu-id="c9bf9-113">Dagsetningabilið sem verðskýrslan ætti að vera búin til fyrir.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="c9bf9-114">Tímalengdin er sem stendur takmörkuð við 7 daga.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="c9bf9-115">Rás</span><span class="sxs-lookup"><span data-stu-id="c9bf9-115">Channel</span></span>| <span data-ttu-id="c9bf9-116">Smásöluverslunin sem verðskýrslan ætti að vera búin til fyrir.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-116">The retail store for which the price report should be generated.</span></span> |
| <span data-ttu-id="c9bf9-117">Sýna afurðir með tiltækar birgðir</span><span class="sxs-lookup"><span data-stu-id="c9bf9-117">Display products with available inventory</span></span>| <span data-ttu-id="c9bf9-118">Ef þetta er stillt á **Já** verða verðin sýnd fyrir aðeins þessar afurðir sem eru með tiltækar efnislegar birgðir sem stendur í versluninni.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="c9bf9-119">Sýna verð á afbrigðum</span><span class="sxs-lookup"><span data-stu-id="c9bf9-119">Display prices for variants</span></span> | <span data-ttu-id="c9bf9-120">Ef þetta er stillt á **Já** verða verðin sýnd fyrir afbrigðin ásamt afurðarsniðmátunum.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="c9bf9-121">Aðeins ætti að stilla þetta á **Kveikja** ef þú ert með verð sem miðast við afbrigði, vegna þess að fjöldi lína eykst umtalsvert.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="c9bf9-122">Í framtíðarútgáfum munum við virkja víddarmiðuð verð svo verslunarstjórinn geti valið víddirnar þar sem sýna á verðin.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="c9bf9-123">Sýna afurðir með verðbreytingum</span><span class="sxs-lookup"><span data-stu-id="c9bf9-123">Display products with price changes</span></span> | <span data-ttu-id="c9bf9-124">Ef þetta er stillt á **Já** verða verðin sýnd fyrir aðeins þessar dagsetningar sem verðinu hefur verið breytt.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="c9bf9-125">Verðið fyrir *Einum degi á undan* valdri **Frá dagsetningu** verður alltaf sýnt svo verslunarstjórinn geti auðveldlega borið kennsl á afurðirnar sem hafa ekki breyst í verði yfir allt tímabilið sem var valið, og svo hann geti einnig skoðað núgildandi verð.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="c9bf9-126">Eftir að skýrslan er búin til er hægt að hlaða niður Excel-skránni fyrir allar nauðsynlegar viðbótarsíur.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="c9bf9-127">Einnig er hægt að nota verðskýrsluna til að athuga eldri verð á afurðum fyrir fyrri dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="c9bf9-127">The price report can also be used to check the historical prices of products for past dates.</span></span>

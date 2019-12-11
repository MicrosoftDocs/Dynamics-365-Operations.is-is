---
title: Virkja ráðleggingar um afurðir
description: Þetta efni útskýrir hvernig hægt er að gera tillögur um vörur sem byggjast á námi gervigreindarvélar (AI-ML) í boði fyrir viðskiptavini Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770140"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="c5a80-103">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="c5a80-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c5a80-104">Þetta efni útskýrir hvernig hægt er að gera tillögur um vörur sem byggjast á námi gervigreindarvélar (AI-ML) í boði fyrir viðskiptavini Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c5a80-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="c5a80-105">Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="c5a80-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="c5a80-106">Ráðleggingar fyrir skoðun</span><span class="sxs-lookup"><span data-stu-id="c5a80-106">Recommendations pre-check</span></span>
<span data-ttu-id="c5a80-107">Áður en það er gert kleift, vinsamlegast hafðu í huga að afurðatillögur eru aðeins studdar fyrir viðskiptavini F&O sem styðja smíði 10.0.6 og hafa flutt geymslu sína með BDL.</span><span class="sxs-lookup"><span data-stu-id="c5a80-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="c5a80-108">Að auki skal tryggja að RetailSale mælingar hafi verið gerðar virkar.</span><span class="sxs-lookup"><span data-stu-id="c5a80-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="c5a80-109">Til að læra meira um þetta uppsetningarferli skaltu fara [hingað.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="c5a80-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="c5a80-110">Kveikja á tillögum</span><span class="sxs-lookup"><span data-stu-id="c5a80-110">Turn on recommendations</span></span>

<span data-ttu-id="c5a80-111">Til að kveikja á afurðatillögum skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c5a80-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="c5a80-112">Farðu í **Retail** &gt; **Afurðatillögur** &gt; **Tillögufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="c5a80-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="c5a80-113">Á listanum yfir sameiginlegar færibreytur velurðu **Tillögulistar**.</span><span class="sxs-lookup"><span data-stu-id="c5a80-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="c5a80-114">Stillið valkostinn **Virkja tillögur** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c5a80-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![virkja afurðatillögur](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="c5a80-116">Þetta ferli hefur ferlið við að mynda afurðatillögulista.</span><span class="sxs-lookup"><span data-stu-id="c5a80-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="c5a80-117">Allt að nokkrar klukkustundir gætu verið nauðsynlegar áður en listarnir eru tiltækir og sjást á sölustað (POS) eða í Dynamics 365 for Commerce.</span><span class="sxs-lookup"><span data-stu-id="c5a80-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="c5a80-118">Stilla færibreytur tillögulista</span><span class="sxs-lookup"><span data-stu-id="c5a80-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="c5a80-119">Sjálfgefið er að AI-ML-byggðir afurðatillögulistar veiti leiðbeinandi gildi.</span><span class="sxs-lookup"><span data-stu-id="c5a80-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="c5a80-120">Þú getur breytt sjálfgefnum gildum svo að þau henti flæði fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c5a80-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="c5a80-121">Til að læra meira um hvernig eigi að breyta sjálfgefnum færibreytum skaltu fara í [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="c5a80-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="c5a80-122">Sýna tillögur um POS tæki</span><span class="sxs-lookup"><span data-stu-id="c5a80-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="c5a80-123">Eftir að hafa gert tillögur í bakvinnslunni virkar verður að bæta tillöguglugganum við á POS skjánum með skipulagstólinu.</span><span class="sxs-lookup"><span data-stu-id="c5a80-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="c5a80-124">Til að læra meira um þetta ferli skaltu fara [hingað.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="c5a80-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c5a80-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c5a80-125">Additional resources</span></span>

[<span data-ttu-id="c5a80-126">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="c5a80-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c5a80-127">Bæta við listum með afurðartillögum við síður</span><span class="sxs-lookup"><span data-stu-id="c5a80-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="c5a80-128">Bæta tillöguglugga við POS tæki</span><span class="sxs-lookup"><span data-stu-id="c5a80-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)



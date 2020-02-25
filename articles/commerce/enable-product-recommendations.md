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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024957"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="4c664-103">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="4c664-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4c664-104">Þetta efni útskýrir hvernig hægt er að gera tillögur um vörur sem byggjast á námi gervigreindarvélar (AI-ML) í boði fyrir viðskiptavini Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4c664-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="4c664-105">Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="4c664-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="4c664-106">Ráðleggingar fyrir skoðun</span><span class="sxs-lookup"><span data-stu-id="4c664-106">Recommendations pre-check</span></span>

<span data-ttu-id="4c664-107">Áður en það er gert kleift, vinsamlegast hafðu í huga að afurðatillögur eru aðeins studdar fyrir viðskiptavini Commerce sem hafa flutt geymslu sína með Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="4c664-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="4c664-108">Sjá leiðbeiningar um hvernig virkja skuli ADLS [Hvernig á að virkja ADLS í Dynamics 365 umhverfi](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4c664-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="4c664-109">Að auki skal tryggja að RetailSale mælingar hafi verið gerðar virkar.</span><span class="sxs-lookup"><span data-stu-id="4c664-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="4c664-110">Til að læra meira um þetta uppsetningarferli skaltu fara [hingað.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="4c664-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="4c664-111">Kveikja á tillögum</span><span class="sxs-lookup"><span data-stu-id="4c664-111">Turn on recommendations</span></span>

<span data-ttu-id="4c664-112">Til að kveikja á afurðatillögum skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4c664-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="4c664-113">Farðu í **Retail og Commerce &gt; Afurðatillögur &gt; Færibreytur tillögulista**.</span><span class="sxs-lookup"><span data-stu-id="4c664-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="4c664-114">Á listanum yfir sameiginlegar færibreytur velurðu **Tillögulistar**.</span><span class="sxs-lookup"><span data-stu-id="4c664-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="4c664-115">Stillið valkostinn **Virkja tillögur** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="4c664-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![virkja afurðatillögur](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="4c664-117">Þetta ferli hefur ferlið við að mynda afurðatillögulista.</span><span class="sxs-lookup"><span data-stu-id="4c664-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="4c664-118">Allt að nokkrar klukkustundir gætu verið nauðsynlegar áður en listarnir eru tiltækir og sjást á sölustað (POS) eða í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4c664-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="4c664-119">Stilla færibreytur tillögulista</span><span class="sxs-lookup"><span data-stu-id="4c664-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="4c664-120">Sjálfgefið er að AI-ML-byggðir afurðatillögulistar veiti leiðbeinandi gildi.</span><span class="sxs-lookup"><span data-stu-id="4c664-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="4c664-121">Þú getur breytt sjálfgefnum gildum svo að þau henti flæði fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="4c664-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="4c664-122">Til að læra meira um hvernig eigi að breyta sjálfgefnum færibreytum skaltu fara í [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="4c664-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="4c664-123">Sýna tillögur um POS tæki</span><span class="sxs-lookup"><span data-stu-id="4c664-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="4c664-124">Eftir að hafa gert tillögur í bakvinnslu Commerce virkar verður að bæta tillöguglugganum við á POS skjánum með skipulagstólinu.</span><span class="sxs-lookup"><span data-stu-id="4c664-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="4c664-125">Til að fræðast um þetta ferli, sjá [Bættu ráðleggingastjórnun við viðskiptaskjáinn á POS tækjum](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="4c664-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="4c664-126">Virkja sérsniðnar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="4c664-126">Enable personalized recommendations</span></span>

<span data-ttu-id="4c664-127">Til að læra meira um hvernig á að fá persónulegar ráðleggingar, sjá [Virkja persónulegar ráðleggingar](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="4c664-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c664-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4c664-128">Additional resources</span></span>

[<span data-ttu-id="4c664-129">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="4c664-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4c664-130">Virkja sérsniðnar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="4c664-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="4c664-131">Bæta við listum með afurðartillögum við síður</span><span class="sxs-lookup"><span data-stu-id="4c664-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="4c664-132">Bæta tillöguglugga við POS tæki</span><span class="sxs-lookup"><span data-stu-id="4c664-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4c664-133">Yfirlit yfir vörusafnseiningu</span><span class="sxs-lookup"><span data-stu-id="4c664-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="4c664-134">Virkja ADLS í Dynamics 365-umhverfinu</span><span class="sxs-lookup"><span data-stu-id="4c664-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)


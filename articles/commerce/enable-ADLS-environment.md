---
title: Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi
description: Þetta efnisatriði útskýrir hvernig á að virkja og prófa Azure Data Lake Storage fyrir Dynamics 365 Commerce-umhverfi, sem er forsenda fyrir því að virkja afurðartillögur.
author: bebeale
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61f96dae0643e3383afd91864e4c145f3b5c04c8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792608"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="873cc-103">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="873cc-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="873cc-104">Þetta efnisatriði útskýrir hvernig á að virkja og prófa Azure Data Lake Storage fyrir Dynamics 365 Commerce-umhverfi, sem er forsenda fyrir því að virkja afurðartillögur.</span><span class="sxs-lookup"><span data-stu-id="873cc-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

<span data-ttu-id="873cc-105">Í Dynamics 365 Commerce-lausn eru allar upplýsingar um vöru og viðskipti raktar í Entity verslun umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="873cc-105">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="873cc-106">Til að gera þessi gögn aðgengileg öðrum þjónustum Dynamics 365, t.d. gagnagreiningu, viðskiptagreind og sérsniðnum tillögum, er nauðsynlegt að tengja umhverfið við Azure Data Lake Storage Gen 2 lausn í eigu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="873cc-106">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="873cc-107">Þar sem Azure Data Lake Storage er skilgreint í umhverfi eru öll nauðsynleg gögn spegluð úr einingaversluninni og á sama tíma vernduð og undir stjórn viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="873cc-107">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="873cc-108">Ef afurðartillögur eða sérsniðnar tillögur eru einnig virkjaðar í umhverfinu verður stafli afurðartillagna gefin aðgangur að sérstakri möppu í Azure Data Lake Storage til að sækja gögn viðskiptavinar og reikna út tillögur byggt á þeim.</span><span class="sxs-lookup"><span data-stu-id="873cc-108">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="873cc-109">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="873cc-109">Prerequisites</span></span>

<span data-ttu-id="873cc-110">Viðskiptavinir verða að hafa Azure Data Lake Storage skilgreint í Azure-áskrift sem þeir eru með.</span><span class="sxs-lookup"><span data-stu-id="873cc-110">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="873cc-111">Þetta efnisatriði nær ekki yfir kaup á Azure-áskrift eða uppsetningu Azure Data Lake Storage-virkjaðs geymslulykils.</span><span class="sxs-lookup"><span data-stu-id="873cc-111">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="873cc-112">Frekari upplýsingar um Azure Data Lake Storage eru í [Azure Data Lake Storage Gen2 opinberum skjölum](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="873cc-112">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="873cc-113">Skref skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="873cc-113">Configuration steps</span></span>

<span data-ttu-id="873cc-114">Þessi hluti nær yfir skilgreiningarskrefin sem nauðsynleg eru til að virkja Azure Data Lake Storage í umhverfi því að það tengist afurðartillögum.</span><span class="sxs-lookup"><span data-stu-id="873cc-114">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="873cc-115">Fyrir ítarlegra yfirlit yfir skrefin sem þarf til að virkja Azure Data Lake Storage skal skoða [Gera einingaverslun tiltæka sem Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="873cc-115">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="873cc-116">Gera Azure Data Lake Storage virkt í umhverfinu</span><span class="sxs-lookup"><span data-stu-id="873cc-116">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="873cc-117">Skráðu þig inn á bakgagnasafn umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="873cc-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="873cc-118">Leitapu að **Kerfisfæribreytum** og farðu á flipann **Gagnatengingar**.</span><span class="sxs-lookup"><span data-stu-id="873cc-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="873cc-119">Stilltu **Virkja samþættingu Data Lake** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="873cc-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="873cc-120">Stilltu **Hlutauppfærsla Data Lake** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="873cc-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="873cc-121">Næst færirðu inn eftirfarandi áskildar upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="873cc-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="873cc-122">**Forritsauðkenni** // **Leynilykill forrits** // **DNS-heiti** - Nauðsynlegt til að tengjast við KeyVault þar sem Azure Data Lake Storage-leynilykillinn er geymdur.</span><span class="sxs-lookup"><span data-stu-id="873cc-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="873cc-123">**Leyniheiti** - Leyniheitið sem geymt er í KeyVault og notað til að sannvotta við Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="873cc-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="873cc-124">Vistaðu breytingarnar þínar efst í vinstra horninu á síðunni.</span><span class="sxs-lookup"><span data-stu-id="873cc-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="873cc-125">Eftirfarandi mynd sýnir dæmi um skilgreiningu Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="873cc-125">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Dæmi um skilgreiningu Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="873cc-127">Prófa Azure Data Lake Storage-tenginguna</span><span class="sxs-lookup"><span data-stu-id="873cc-127">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="873cc-128">Prófaðu tenginguna við KeyVault með því að nota tengilinn **Prófa Azure-lykil**.</span><span class="sxs-lookup"><span data-stu-id="873cc-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="873cc-129">Prófið tenginguna við Azure Data Lake Storage með því að nota tengilinn **Azure Storage**.</span><span class="sxs-lookup"><span data-stu-id="873cc-129">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="873cc-130">Ef prófunin tekst ekki skaltu athuga aftur hvort allar viðbættar KeyVault-upplýsingar hér að ofan séu réttar og reyna síðan aftur.</span><span class="sxs-lookup"><span data-stu-id="873cc-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="873cc-131">Þegar tengiprófin hafa gengið, verður þú að gera sjálfvirka endurnýjun fyrir Entity verslunina.</span><span class="sxs-lookup"><span data-stu-id="873cc-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="873cc-132">Fylgdu þessum skrefum til að gera sjálfvirka endurnýjun fyrir Entity verslun.</span><span class="sxs-lookup"><span data-stu-id="873cc-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="873cc-133">Leita að **Entity-verslun**.</span><span class="sxs-lookup"><span data-stu-id="873cc-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="873cc-134">Á listanum til vinstri ferðu í færsluna **RetailSales** og velur **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="873cc-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="873cc-135">Gakktu úr skugga um að **Sjálfvirk uppfærsla virk** sé stillt á **Já**, veldu **Endurnýja** og veldu síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="873cc-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="873cc-136">Eftirfarandi mynd sýnir dæmi um Entity verslun með sjálfvirka endurnýjun virka.</span><span class="sxs-lookup"><span data-stu-id="873cc-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Dæmi um verslun Entity með sjálfvirka endurnýjun virka](./media/exampleADLSConfig2.png)

<span data-ttu-id="873cc-138">Azure Data Lake Storage er nú skilgreint fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="873cc-138">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="873cc-139">Ef ekki er lokið þegar, fylgdu skrefunum fyrir [sem gerir ráð fyrir vöru og sérstillingu](enable-product-recommendations.md) fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="873cc-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="873cc-140">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="873cc-140">Additional resources</span></span>

[<span data-ttu-id="873cc-141">Gera einingaverslun tiltæka sem Data Lake</span><span class="sxs-lookup"><span data-stu-id="873cc-141">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="873cc-142">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="873cc-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="873cc-143">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="873cc-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="873cc-144">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="873cc-144">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="873cc-145">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="873cc-145">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="873cc-146">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="873cc-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="873cc-147">Bæta við afurðatillögum á sölustað</span><span class="sxs-lookup"><span data-stu-id="873cc-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="873cc-148">Bæta tillögum við færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="873cc-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="873cc-149">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="873cc-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="873cc-150">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="873cc-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="873cc-151">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="873cc-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="873cc-152">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="873cc-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

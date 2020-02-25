---
title: Virkja ADLS í Dynamics 365 Commerce umhverfi
description: Þetta efni útskýrir hvernig á að virkja og prófa Azure Data Lake Storage (ADLS) fyrir Dynamics 365 Commerce umhverfi, sem er forsenda þess að hægt sé að gera ráð fyrir afurð.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025254"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="921cf-103">Virkja ADLS í Dynamics 365 Commerce umhverfi</span><span class="sxs-lookup"><span data-stu-id="921cf-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="921cf-104">Þetta efni útskýrir hvernig á að virkja og prófa Azure Data Lake Storage (ADLS) fyrir Dynamics 365 Commerce umhverfi, sem er forsenda þess að hægt sé að gera ráð fyrir afurð.</span><span class="sxs-lookup"><span data-stu-id="921cf-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="921cf-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="921cf-105">Overview</span></span>

<span data-ttu-id="921cf-106">Í Dynamics 365 Commerce-lausn eru allar upplýsingar um vöru og viðskipti raktar í Entity verslun umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="921cf-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="921cf-107">Til að gera þessi gögn aðgengileg öðrum Dynamics 365 þjónustu, svo sem gagnagreiningum, viðskiptagreind og persónulegum ráðleggingum, er nauðsynlegt að tengja umhverfið við viðskiptavini í eigu Azure Data Lake Storage Gen 2 (ADLS) lausn.</span><span class="sxs-lookup"><span data-stu-id="921cf-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="921cf-108">Þar sem ADLS er stillt í umhverfi eru öll nauðsynleg gögn spegluð úr Entity versluninni meðan þau eru enn vernduð og undir stjórn viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="921cf-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="921cf-109">Ef tillögur um vöru eða sérsniðnar ráðleggingar eru einnig gerðar virkar í umhverfinu, þá mun vöruframkvæmdastakkanum fá aðgang að sérstaka möppu í ADLS til að sækja gögn viðskiptavinarins og reikna meðmæli byggða á þeim.</span><span class="sxs-lookup"><span data-stu-id="921cf-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="921cf-110">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="921cf-110">Prerequisites</span></span>

<span data-ttu-id="921cf-111">Viðskiptavinir þurfa að hafa ADLS stillt í Azure áskrift sem þeir eiga.</span><span class="sxs-lookup"><span data-stu-id="921cf-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="921cf-112">Þetta efni fjallar ekki um kaup á Azure áskrift eða uppsetningu ADLS-geymslureiknings.</span><span class="sxs-lookup"><span data-stu-id="921cf-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="921cf-113">Nánari upplýsingar um ADLS er að finna í [ADLS opinberum fylgiskjölum](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="921cf-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="921cf-114">Skref skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="921cf-114">Configuration steps</span></span>

<span data-ttu-id="921cf-115">Þessi hluti fjallar um nauðsynlegar stillingar til að gera ADLS kleift í umhverfi.</span><span class="sxs-lookup"><span data-stu-id="921cf-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="921cf-116">Virkja ADLS í umhverfinu</span><span class="sxs-lookup"><span data-stu-id="921cf-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="921cf-117">Skráðu þig inn á bakgagnasafn umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="921cf-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="921cf-118">Leitapu að **Kerfisfæribreytum** og farðu á flipann **Gagnatengingar**.</span><span class="sxs-lookup"><span data-stu-id="921cf-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="921cf-119">Stilltu **Virkja samþættingu Data Lake** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="921cf-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="921cf-120">Stilltu **Hlutauppfærsla Data Lake** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="921cf-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="921cf-121">Næst færirðu inn eftirfarandi áskildar upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="921cf-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="921cf-122">**Auðkenni forrits** // **Leynilykill forrits** // **DNS-heiti** - Nauðsynlegt til að tengjast KeyVault þar sem ADLS-leynilykillinn er geymdur.</span><span class="sxs-lookup"><span data-stu-id="921cf-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="921cf-123">**Leyniheiti** - Leyniheitið sem geymt er í KeyVault og notað til að sannvotta með ADLS.</span><span class="sxs-lookup"><span data-stu-id="921cf-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="921cf-124">Vistaðu breytingarnar þínar efst í vinstra horninu á síðunni.</span><span class="sxs-lookup"><span data-stu-id="921cf-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="921cf-125">Eftirfarandi mynd sýnir dæmi um ADLS-stillingu.</span><span class="sxs-lookup"><span data-stu-id="921cf-125">The following image shows an example ADLS configuration.</span></span>

![Dæmi um ADLS-stillingu](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="921cf-127">Prófa ADLS-tengingu</span><span class="sxs-lookup"><span data-stu-id="921cf-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="921cf-128">Prófaðu tenginguna við KeyVault með því að nota tengilinn **Prófa Azure-lykil**.</span><span class="sxs-lookup"><span data-stu-id="921cf-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="921cf-129">Prófaðu tenginguna við ADLS með því að nota tengilinn **Prófa Azure-geymslu**.</span><span class="sxs-lookup"><span data-stu-id="921cf-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="921cf-130">Ef prófunin tekst ekki skaltu athuga aftur hvort allar viðbættar KeyVault-upplýsingar hér að ofan séu réttar og reyna síðan aftur.</span><span class="sxs-lookup"><span data-stu-id="921cf-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="921cf-131">Þegar tengiprófin hafa gengið, verður þú að gera sjálfvirka endurnýjun fyrir Entity verslunina.</span><span class="sxs-lookup"><span data-stu-id="921cf-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="921cf-132">Fylgdu þessum skrefum til að gera sjálfvirka endurnýjun fyrir Entity verslun.</span><span class="sxs-lookup"><span data-stu-id="921cf-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="921cf-133">Leita að **Entity-verslun**.</span><span class="sxs-lookup"><span data-stu-id="921cf-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="921cf-134">Á listanum til vinstri ferðu í færsluna **RetailSales** og velur **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="921cf-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="921cf-135">Gakktu úr skugga um að **Sjálfvirk uppfærsla virk** sé stillt á **Já**, veldu **Endurnýja** og veldu síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="921cf-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="921cf-136">Eftirfarandi mynd sýnir dæmi um Entity verslun með sjálfvirka endurnýjun virka.</span><span class="sxs-lookup"><span data-stu-id="921cf-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Dæmi um verslun Entity með sjálfvirka endurnýjun virka](./media/exampleADLSConfig2.png)

<span data-ttu-id="921cf-138">ADLS er nú stillt fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="921cf-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="921cf-139">Ef ekki er lokið þegar, fylgdu skrefunum fyrir [sem gerir ráð fyrir vöru og sérstillingu](enable-product-recommendations.md) fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="921cf-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="921cf-140">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="921cf-140">Additional resources</span></span>

[<span data-ttu-id="921cf-141">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="921cf-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="921cf-142">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="921cf-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="921cf-143">Bæta við listum með afurðartillögum við síður</span><span class="sxs-lookup"><span data-stu-id="921cf-143">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="921cf-144">Bæta stýringu ráðleggingar á færsluskjá á sölustaðartækjum</span><span class="sxs-lookup"><span data-stu-id="921cf-144">Add a recommendations control to the transaction screen on POS devices</span></span>](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)



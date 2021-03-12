---
title: Virkja sjóðstreymisspá (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að kveikja á eiginleikanum „Sjóðstreymisspár“ í fjármálainnsýn.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 1977dac4a3ab66cca2248dc0124d3a06d6963f40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978765"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="ad5df-103">Virkja sjóðstreymisspá (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="ad5df-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ad5df-104">Þetta efnisatriði útskýrir hvernig á að kveikja á eiginleikanum „Sjóðstreymisspár“ í fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="ad5df-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="ad5df-105">Til að nota greiðsluspár í sjóðstreymi þarf að setja upp greiðsluspár viðskiptavinar eins og lýst er í [Virkja greiðsluspár viðskiptavinar](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="ad5df-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="ad5df-106">Notaðu upplýsingar úr umhverfissíðunni í Microsoft Dynamics Lifecycle Services (LCS) til að tengjast aðaltilviki Azure SQL fyrir þetta umhverfi.</span><span class="sxs-lookup"><span data-stu-id="ad5df-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="ad5df-107">Keyrið eftirfarandi Transact-SQL (T-SQL) skipun til að kveikja á flugi fyrir sandkassaumhverfa.</span><span class="sxs-lookup"><span data-stu-id="ad5df-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="ad5df-108">(Hugsanlega þarf að kveikja á aðgangi að IP-tölu notanda í LCS áður en hægt er að fjartengjast við AOS \[Application Object Server\].)</span><span class="sxs-lookup"><span data-stu-id="ad5df-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="ad5df-109">Ef verið er að setja upp Microsoft Dynamics 365 Finance sem Service Fabric-uppsetningu er hægt að sleppa þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="ad5df-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="ad5df-110">Fjármögnunarteymið ætti nú þegar að hafa kveikt á forútgáfunni fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="ad5df-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="ad5df-111">Ef þú sérð ekki eiginleikana á vinnusvæðinu **Eiginleikastjórnun** eða ef vandamál koma upp þegar reynt er að kveikja á þeim skal hafa samband við <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="ad5df-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="ad5df-112">Opnið vinnusvæðið **Eiginleikastjórnun** og fylgið eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="ad5df-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="ad5df-113">Veldu **Leita að uppfærslum**.</span><span class="sxs-lookup"><span data-stu-id="ad5df-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="ad5df-114">Kveikja skal á eftirfarandi eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="ad5df-114">Turn on the following features:</span></span>

        - <span data-ttu-id="ad5df-115">Ný hnitanetsstýring</span><span class="sxs-lookup"><span data-stu-id="ad5df-115">New grid control</span></span>
        - <span data-ttu-id="ad5df-116">Flokkun í hnitanetum (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="ad5df-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="ad5df-117">Greiðsluspár viðskiptavinar (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="ad5df-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="ad5df-118">Sjóðstreymispár (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="ad5df-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="ad5df-119">Opnið **Reiðufjár- og bankastjórnun \> Uppsetning sjóðsstreymisspár** og bætið við greiðslugetulyklum sem eiga að vera með í spánum.</span><span class="sxs-lookup"><span data-stu-id="ad5df-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ad5df-120">Ef greiðslugetureikningar eru ekki settir upp er ekki hægt að mynda sjóðstreymið.</span><span class="sxs-lookup"><span data-stu-id="ad5df-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="ad5df-121">Opnaðu **Reiðufjár- og bankastjórnun \> Uppsetning \> Fjármálainnsýn (forskoða) \> Sjóðsstreymisspár (forskoða)** og fylgdu eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="ad5df-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="ad5df-122">Á flipanum **Sjóðsstreymisspá** skal velja **Virkja eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="ad5df-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="ad5df-123">Veljið **Stofna spálíkan**.</span><span class="sxs-lookup"><span data-stu-id="ad5df-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="ad5df-124">Frekari upplýsingar um afkastagetu sjóðstreymisspár er að finna í [Sjóðstreymisspár](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="ad5df-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="ad5df-125">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="ad5df-125">Privacy notice</span></span>

<span data-ttu-id="ad5df-126">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="ad5df-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>

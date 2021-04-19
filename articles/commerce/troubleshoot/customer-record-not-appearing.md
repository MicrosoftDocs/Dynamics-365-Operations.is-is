---
title: Færslur viðskiptavinar birtast ekki í Commerce Headquarters
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar færslur viðskiptavinar birtast ekki strax í Commerce Headquarters.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5499e3c059c9e735df87ef8b462d446e0710d90c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801796"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="69058-103">Færslur viðskiptavinar birtast ekki í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="69058-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69058-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar færslur viðskiptavinar birtast ekki strax í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="69058-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="69058-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="69058-105">Description</span></span>

<span data-ttu-id="69058-106">Þegar færsla viðskiptavinar er stofnuð með því að nota innskráningarflæðið í netverslun rafrænna viðskipta birtist samsvarandi færsla viðskiptavinar ekki strax í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="69058-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="69058-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="69058-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="69058-108">Slökkva á stofnun viðskiptavinar í ósamstilltri stillingu</span><span class="sxs-lookup"><span data-stu-id="69058-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69058-109">Ef slökkt er á stofnun ósamstillts viðskiptavinar gætu það haft áhrif á afköst kerfisins vegna þess að stofnun hverrar færslu býr til beiðni í rauntíma í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="69058-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="69058-110">Auk þess, ef Commerce Headquarters liggur niðri (til dæmis þegar þjónustuflæði er í gangi), mun stofnflæði nýrra viðskiptavina leiða til villu.</span><span class="sxs-lookup"><span data-stu-id="69058-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="69058-111">Til að slökkva á stofnun viðskiptavinar í ósamstilltri stillingu í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="69058-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="69058-112">Farið í **Smásala og viðskipti \> Uppsetning rásar \> Uppsetning netverslunar \> Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="69058-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="69058-113">Ef ekki er verið að nota virknireglu fyrir netrásina skal stofna slíka.</span><span class="sxs-lookup"><span data-stu-id="69058-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="69058-114">Ganga skal úr skugga um að valkosturinn **Stofna viðskiptavin í ósamstilltri stillingu** sé stilltur á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="69058-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="69058-115">Farið í **Smásala og viðskipti \> Rásir \> Netverslanir**.</span><span class="sxs-lookup"><span data-stu-id="69058-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="69058-116">Veljið netverslunina þar sem á að slökkva á stofnun ósamstillts viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="69058-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="69058-117">Í flipanum **Almennt** skal ganga úr skugga um að reiturinn **Virkniregla** sé stilltur á virkniregluna sem verið er að nota fyrir netrásina.</span><span class="sxs-lookup"><span data-stu-id="69058-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69058-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="69058-118">Additional resources</span></span>

[<span data-ttu-id="69058-119">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="69058-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

---
title: Vantar afurðir og flokka eftir afritun umhverfis
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar afurðir og flokka vantar eftir að svæði er afritað milli umhverfa eða innan sama umhverfis.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585383"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="813f0-103">Afurðir og flokka vantar eftir afritun umhverfis</span><span class="sxs-lookup"><span data-stu-id="813f0-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="813f0-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar afurðir og flokka vantar eftir að svæði er afritað milli umhverfa eða innan sama umhverfis.</span><span class="sxs-lookup"><span data-stu-id="813f0-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="813f0-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="813f0-105">Description</span></span>

<span data-ttu-id="813f0-106">Þegar svæði er afritað úr einu umhverfi í annað, eða innan sama umhverfis, vantar afurðir og flokka úr svæðinu.</span><span class="sxs-lookup"><span data-stu-id="813f0-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="813f0-107">Afurðirnar og flokkana vantar úr netverslun rafrænna viðskipta og úr flipanum **Afurðir** í vefsmið Commerce.</span><span class="sxs-lookup"><span data-stu-id="813f0-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="813f0-108">Upplausn</span><span class="sxs-lookup"><span data-stu-id="813f0-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="813f0-109">Varpa rásarnúmeri rekstrareiningar í nýlega afritað svæði í vefsmið Commerce</span><span class="sxs-lookup"><span data-stu-id="813f0-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="813f0-110">Til að varpa rásarnúmeri rekstrareiningar í nýlega afritað svæði í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="813f0-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="813f0-111">Veljið nýlega afritað svæði.</span><span class="sxs-lookup"><span data-stu-id="813f0-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="813f0-112">Undir **Svæðisstillingar** skal velja **Rásir**.</span><span class="sxs-lookup"><span data-stu-id="813f0-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="813f0-113">Við hliðina á heiti rásarinnar skal velja úrfellingarmerkið (**...**) og síðan velja **Breyta netverslunarrás**.</span><span class="sxs-lookup"><span data-stu-id="813f0-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="813f0-114">Í svarglugganum **Breyta netverslunarrás** skal velja rásina til að varpa í nýlega afritað svæði og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="813f0-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="813f0-115">Veljið **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="813f0-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="813f0-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="813f0-116">Additional resources</span></span>

[<span data-ttu-id="813f0-117">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="813f0-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)

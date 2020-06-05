---
title: Staðfesting afurðar fyrir klasatiltekt
description: Þetti efnisatriði lýsir uppsetningu á sannprófun vöru með klasatilekt.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272c3a13b68e2b862faf20cc269ca790322b61de
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367293"
---
# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="c4590-103">Staðfesting afurðar fyrir klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="c4590-103">Product confirmation for cluster picking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4590-104">Klasatiltekt gerir kleift að taka til vörur fyrir margar pantanir samtímis.</span><span class="sxs-lookup"><span data-stu-id="c4590-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="c4590-105">Þegar klasatiltekt er notuð, er vörustaðfesting nauðsynleg svo hægt sé að staðfesta þær vörur sem bætt er við klasa.</span><span class="sxs-lookup"><span data-stu-id="c4590-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="c4590-106">Hægt er að staðfesta vörur í klasatiltekt á meðan klasatiltekt stendur yfir.</span><span class="sxs-lookup"><span data-stu-id="c4590-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="c4590-107">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="c4590-107">Where it applies</span></span>

<span data-ttu-id="c4590-108">Vörustaðfesting fyrir klasatiltekt gengur eins fyrir sig og þegar vörur eru staðfestar í tiltekt sem er ekki klasatiltekt.</span><span class="sxs-lookup"><span data-stu-id="c4590-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="c4590-109">Uppsetning byggist á strikamerkjauppsetningu vöru.</span><span class="sxs-lookup"><span data-stu-id="c4590-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="c4590-110">Setja upp vörustaðfestingu með klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="c4590-110">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="c4590-111">Opna uppsetningarskjámynd fyrir vinnustaðfestingu í valmyndaratriði fartækis: **Vöruhúsastjórnun** > **Vöruhúsastjórnun** > **Uppsetning** > **Fartæki** > **Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="c4590-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
1. <span data-ttu-id="c4590-112">Opna **Uppsetning vinnustaðfestingar** í valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="c4590-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="c4590-113">Valkostur</span><span class="sxs-lookup"><span data-stu-id="c4590-113">Option</span></span>        |                                    <span data-ttu-id="c4590-114">lýsing</span><span class="sxs-lookup"><span data-stu-id="c4590-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c4590-115">Staðfesting afurðar</span><span class="sxs-lookup"><span data-stu-id="c4590-115">Product confirmation</span></span> | <span data-ttu-id="c4590-116">Gerir kleift að staðfesta hverja birgðaeiningu úr fartækinu þegar skannað er.</span><span class="sxs-lookup"><span data-stu-id="c4590-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |

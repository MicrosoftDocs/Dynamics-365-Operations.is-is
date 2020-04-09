---
title: Vildarkort og vildarpunktar viðskiptavinar
description: Þetta efni lýsir samþættingu gagna um vildarkort viðskiptavina og verðlaunapunkta á milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172970"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="d0d0c-103">Vildarkort og vildarpunktar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="d0d0c-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="d0d0c-104">Fyrirtæki flokka viðskiptavini og veita háþróaða þjónustu, byggð á innkaupum viðskiptavina og eyðslumynstri.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="d0d0c-105">Í Microsoft Dynamics 365 forritasvítunni hefur Dynamics 365 Commerce innviði og aðgerðir til að auðvelda og meðhöndla vildarkort viðskiptavina, verðlaunastig, verðmæti sem byggir á hollustu og umbun byggir á verslunarupplifun.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="d0d0c-106">Þegar gögn um vildarkort viðskiptavina og umbunarpunkta í viðskiptum eru samstillt við Common Data Service geta líkanadrifin forrit í Dynamics 365 notað þessi gögn.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="d0d0c-107">Til dæmis geta notendur Dynamics 365 Customer Service notað gögnin til að veita sömu háþróuðu þjónustu í gegnum þjónustuborðið.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="d0d0c-108">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="d0d0c-108">Templates</span></span>

| <span data-ttu-id="d0d0c-109">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="d0d0c-109">Finance and Operations apps</span></span> | <span data-ttu-id="d0d0c-110">Líkanadrifin forrit í Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d0d0c-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="d0d0c-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="d0d0c-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="d0d0c-112">Vildarkort</span><span class="sxs-lookup"><span data-stu-id="d0d0c-112">Loyalty card</span></span>                | <span data-ttu-id="d0d0c-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="d0d0c-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="d0d0c-114">Þetta sniðmát samstillir upplýsingar um vildarkort viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="d0d0c-115">Vildarpunktar</span><span class="sxs-lookup"><span data-stu-id="d0d0c-115">Loyalty reward points</span></span>       | <span data-ttu-id="d0d0c-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="d0d0c-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="d0d0c-117">Þetta sniðmát samstillir upplýsingar um vildarpunkta viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]

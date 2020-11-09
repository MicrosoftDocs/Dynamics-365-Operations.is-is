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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998015"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="6ca61-103">Vildarkort og vildarpunktar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="6ca61-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="6ca61-104">Fyrirtæki flokka viðskiptavini og veita háþróaða þjónustu, byggð á innkaupum viðskiptavina og eyðslumynstri.</span><span class="sxs-lookup"><span data-stu-id="6ca61-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="6ca61-105">Í Microsoft Dynamics 365 forritasvítunni hefur Dynamics 365 Commerce innviði og aðgerðir til að auðvelda og meðhöndla vildarkort viðskiptavina, verðlaunastig, verðmæti sem byggir á hollustu og umbun byggir á verslunarupplifun.</span><span class="sxs-lookup"><span data-stu-id="6ca61-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="6ca61-106">Þegar gögn um vildarkort viðskiptavina og umbunarpunkta í viðskiptum eru samstillt við Common Data Service geta líkanadrifin forrit í Dynamics 365 notað þessi gögn.</span><span class="sxs-lookup"><span data-stu-id="6ca61-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="6ca61-107">Til dæmis geta notendur Dynamics 365 Customer Service notað gögnin til að veita sömu háþróuðu þjónustu í gegnum þjónustuborðið.</span><span class="sxs-lookup"><span data-stu-id="6ca61-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="6ca61-108">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="6ca61-108">Templates</span></span>

| <span data-ttu-id="6ca61-109">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="6ca61-109">Finance and Operations apps</span></span> | <span data-ttu-id="6ca61-110">Líkanadrifin forrit í Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6ca61-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="6ca61-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="6ca61-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="6ca61-112">Vildarkort</span><span class="sxs-lookup"><span data-stu-id="6ca61-112">Loyalty card</span></span>                | <span data-ttu-id="6ca61-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="6ca61-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="6ca61-114">Þetta sniðmát samstillir upplýsingar um vildarkort viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="6ca61-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="6ca61-115">Vildarpunktar</span><span class="sxs-lookup"><span data-stu-id="6ca61-115">Loyalty reward points</span></span>       | <span data-ttu-id="6ca61-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="6ca61-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="6ca61-117">Þetta sniðmát samstillir upplýsingar um vildarpunkta viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="6ca61-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]

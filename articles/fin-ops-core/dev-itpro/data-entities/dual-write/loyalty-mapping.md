---
title: Vildarkort og vildarpunktar viðskiptavinar
description: Þetta efnisatriði lýsir samþættingu gagna um vildarkort viðskiptavinar og vildarpunkta í tvöfaldri skráningu.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747988"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="f30b7-103">Vildarkort og vildarpunktar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f30b7-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f30b7-104">Fyrirtæki flokka viðskiptavini og veita háþróaða þjónustu, byggð á innkaupum viðskiptavina og eyðslumynstri.</span><span class="sxs-lookup"><span data-stu-id="f30b7-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="f30b7-105">Til dæmis er Dynamics 365 Commerce með innviði og aðgerðir til að auðvelda meðhöndlun vildarkort viðskiptavina, vildarpunkta, verðlagningarverð, vildarverð og kaup með verðlaunum.</span><span class="sxs-lookup"><span data-stu-id="f30b7-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="f30b7-106">Þegar gögn um vildarkort viðskiptavinar og vildarpunkta í Commerce eru samstillt við Dataverse geta Customer Engagement forrit notað þessi gögn.</span><span class="sxs-lookup"><span data-stu-id="f30b7-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="f30b7-107">Til dæmis geta notendur Dynamics 365 Customer Service notað gögnin til að veita sömu háþróuðu þjónustu í gegnum þjónustuborðið.</span><span class="sxs-lookup"><span data-stu-id="f30b7-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="f30b7-108">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="f30b7-108">Templates</span></span>

| <span data-ttu-id="f30b7-109">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="f30b7-109">Finance and Operations apps</span></span> | <span data-ttu-id="f30b7-110">Líkanadrifin forrit í Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f30b7-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="f30b7-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="f30b7-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="f30b7-112">Vildarkort</span><span class="sxs-lookup"><span data-stu-id="f30b7-112">Loyalty card</span></span>                | <span data-ttu-id="f30b7-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="f30b7-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="f30b7-114">Þetta sniðmát samstillir upplýsingar um vildarkort viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="f30b7-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="f30b7-115">Vildarpunktar</span><span class="sxs-lookup"><span data-stu-id="f30b7-115">Loyalty reward points</span></span>       | <span data-ttu-id="f30b7-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="f30b7-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="f30b7-117">Þetta sniðmát samstillir upplýsingar um vildarpunkta viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="f30b7-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
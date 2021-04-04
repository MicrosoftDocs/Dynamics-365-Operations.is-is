---
title: Vildarkort og vildarpunktar viðskiptavinar
description: Þetta efnisatriði lýsir samþættingu gagna um vildarkort viðskiptavinar og vildarpunkta í tvöfaldri skráningu.
author: RamaKrishnamoorthy
manager: AnnBe
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
ms.openlocfilehash: 39e1d5b0a73b198b164e51a18222dbd985192070
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568029"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="3a42b-103">Vildarkort og vildarpunktar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="3a42b-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3a42b-104">Fyrirtæki flokka viðskiptavini og veita háþróaða þjónustu, byggð á innkaupum viðskiptavina og eyðslumynstri.</span><span class="sxs-lookup"><span data-stu-id="3a42b-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="3a42b-105">Til dæmis er Dynamics 365 Commerce með innviði og aðgerðir til að auðvelda meðhöndlun vildarkort viðskiptavina, vildarpunkta, verðlagningarverð, vildarverð og kaup með verðlaunum.</span><span class="sxs-lookup"><span data-stu-id="3a42b-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="3a42b-106">Þegar gögn um vildarkort viðskiptavinar og vildarpunkta í Commerce eru samstillt við Dataverse geta Customer Engagement forrit notað þessi gögn.</span><span class="sxs-lookup"><span data-stu-id="3a42b-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="3a42b-107">Til dæmis geta notendur Dynamics 365 Customer Service notað gögnin til að veita sömu háþróuðu þjónustu í gegnum þjónustuborðið.</span><span class="sxs-lookup"><span data-stu-id="3a42b-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="3a42b-108">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="3a42b-108">Templates</span></span>

| <span data-ttu-id="3a42b-109">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="3a42b-109">Finance and Operations apps</span></span> | <span data-ttu-id="3a42b-110">Líkanadrifin forrit í Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3a42b-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="3a42b-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="3a42b-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="3a42b-112">Vildarkort</span><span class="sxs-lookup"><span data-stu-id="3a42b-112">Loyalty card</span></span>                | <span data-ttu-id="3a42b-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="3a42b-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="3a42b-114">Þetta sniðmát samstillir upplýsingar um vildarkort viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="3a42b-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="3a42b-115">Vildarpunktar</span><span class="sxs-lookup"><span data-stu-id="3a42b-115">Loyalty reward points</span></span>       | <span data-ttu-id="3a42b-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="3a42b-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="3a42b-117">Þetta sniðmát samstillir upplýsingar um vildarpunkta viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="3a42b-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
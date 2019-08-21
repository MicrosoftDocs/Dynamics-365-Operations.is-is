---
title: Setja upp aðallykla flokka
description: Flokkar aðallykla eru notaðir fyrir sjálfgefnar skýrslur í fjárhagsskýrslu og Power BI.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e33df434b6a4361872bad10250fe3547d7c4affa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834807"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="b59c9-103">Setja upp aðallykla flokka</span><span class="sxs-lookup"><span data-stu-id="b59c9-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b59c9-104">Flokkar aðallykla eru notaðir fyrir sjálfgefnar skýrslur í fjárhagsskýrslu og Power BI.</span><span class="sxs-lookup"><span data-stu-id="b59c9-104">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="b59c9-105">Hægt er að endurnefna flokka aðallykla sem eru stofnaðir sjálfvirkt en ekki eyða.</span><span class="sxs-lookup"><span data-stu-id="b59c9-105">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="b59c9-106">Hægt er að stofna viðbótar lykilflokka og nota vegna skýrslugerðar og greiningar.</span><span class="sxs-lookup"><span data-stu-id="b59c9-106">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="b59c9-107">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="b59c9-107">This task uses the USMF demo company.</span></span>


## <a name="create-a-main-account-category"></a><span data-ttu-id="b59c9-108">Stofna tegund aðallykils</span><span class="sxs-lookup"><span data-stu-id="b59c9-108">Create a main account category</span></span>
1. <span data-ttu-id="b59c9-109">Fara í Fjárhagur > Línurit yfir lykla > Lyklar > Tegundir aðallykils.</span><span class="sxs-lookup"><span data-stu-id="b59c9-109">Go to General ledger > Chart of accounts > Accounts > Main account categories.</span></span>
2. <span data-ttu-id="b59c9-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b59c9-110">Click New.</span></span>
3. <span data-ttu-id="b59c9-111">Í reitnum Flokkur aðallykils skal færa inn einkvæmt heiti.</span><span class="sxs-lookup"><span data-stu-id="b59c9-111">In the Main account category field, enter a unique name.</span></span>
4. <span data-ttu-id="b59c9-112">Í reitnum Lýsing færirðu inn lýsingu á flokki aðallykils.</span><span class="sxs-lookup"><span data-stu-id="b59c9-112">In the Description field, enter a description for the main account category.</span></span>
5. <span data-ttu-id="b59c9-113">Í reitnum Gerð aðallykils skal velja þá gerð aðallykils sem verður tengd við flokkinn.</span><span class="sxs-lookup"><span data-stu-id="b59c9-113">In the Main account type field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="b59c9-114">Tengja aðallykla við tegund aðallykils</span><span class="sxs-lookup"><span data-stu-id="b59c9-114">Link main accounts to account category</span></span>
1. <span data-ttu-id="b59c9-115">Smellt er á Tengja aðallykla.</span><span class="sxs-lookup"><span data-stu-id="b59c9-115">Click Link main accounts.</span></span>
2. <span data-ttu-id="b59c9-116">Í listanum velurðu aðallykill til að úthluta á tegund aðalreiknings.</span><span class="sxs-lookup"><span data-stu-id="b59c9-116">In the list, select the main accounts to assign to the main account category.</span></span>
    * <span data-ttu-id="b59c9-117">Úthlutun aðallykla á flokk aðallykla mun safna saman stöðum lyklanna þegar sá flokkur er notaður fyrir fjárhagsskýrslugerð og fjárhagsgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b59c9-117">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="b59c9-118">Velja eða hreinsa valkostinn Tengdar til að velja aðallykla.</span><span class="sxs-lookup"><span data-stu-id="b59c9-118">Select or clear the Linked option to choose the main accounts.</span></span>
4. <span data-ttu-id="b59c9-119">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="b59c9-119">Click OK.</span></span>
5. <span data-ttu-id="b59c9-120">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="b59c9-120">Click Yes.</span></span>


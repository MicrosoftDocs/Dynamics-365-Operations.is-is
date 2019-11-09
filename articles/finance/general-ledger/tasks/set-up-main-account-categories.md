---
title: Setja upp aðallykla flokka
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp flokka aðallykla í Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e2ba1d900f5d87a76fa93bf53f2970320e7d84c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186004"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="18f41-103">Setja upp aðallykla flokka</span><span class="sxs-lookup"><span data-stu-id="18f41-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18f41-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp flokka aðallykla.</span><span class="sxs-lookup"><span data-stu-id="18f41-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="18f41-105">Flokkar aðallykla eru notaðir fyrir sjálfgefnar skýrslur í fjárhagsskýrslu og Power BI.</span><span class="sxs-lookup"><span data-stu-id="18f41-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="18f41-106">Hægt er að endurnefna flokka aðallykla sem eru stofnaðir sjálfvirkt en ekki eyða.</span><span class="sxs-lookup"><span data-stu-id="18f41-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="18f41-107">Hægt er að stofna viðbótar lykilflokka og nota vegna skýrslugerðar og greiningar.</span><span class="sxs-lookup"><span data-stu-id="18f41-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="18f41-108">Þetta efni notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="18f41-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="18f41-109">Stofna tegund aðallykils</span><span class="sxs-lookup"><span data-stu-id="18f41-109">Create a main account category</span></span>
1. <span data-ttu-id="18f41-110">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Bókhaldslykill > Lyklar > Flokkar aðallykla**.</span><span class="sxs-lookup"><span data-stu-id="18f41-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="18f41-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="18f41-111">Select **New**.</span></span>
3. <span data-ttu-id="18f41-112">Í reitnum **Flokkur aðallykils** skal færa inn einkvæmt heiti.</span><span class="sxs-lookup"><span data-stu-id="18f41-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="18f41-113">Í reitnum **Lýsing** færirðu inn lýsingu á flokki aðallykils.</span><span class="sxs-lookup"><span data-stu-id="18f41-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="18f41-114">Í reitnum **Gerð aðallykils** skal velja þá gerð aðallykils sem verður tengd við flokkinn.</span><span class="sxs-lookup"><span data-stu-id="18f41-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="18f41-115">Tengja aðallykla við tegund aðallykils</span><span class="sxs-lookup"><span data-stu-id="18f41-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="18f41-116">Smelltu á **Tengja aðallykla**.</span><span class="sxs-lookup"><span data-stu-id="18f41-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="18f41-117">Á listanum velurðu aðallyklana sem á að tengja við aðallyklaflokkinn með því að haka við reitina í dálkinum **Tengt**.</span><span class="sxs-lookup"><span data-stu-id="18f41-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="18f41-118">Úthlutun aðallykla á flokk aðallykla mun safna saman stöðum lyklanna þegar sá flokkur er notaður fyrir fjárhagsskýrslugerð og fjárhagsgreiningu.</span><span class="sxs-lookup"><span data-stu-id="18f41-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="18f41-119">Veldu eða hreinsaðu valkostinn **Tengt** til að velja aðallykla.</span><span class="sxs-lookup"><span data-stu-id="18f41-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="18f41-120">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="18f41-120">Select **OK**.</span></span>
5. <span data-ttu-id="18f41-121">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="18f41-121">Select **Yes**.</span></span>
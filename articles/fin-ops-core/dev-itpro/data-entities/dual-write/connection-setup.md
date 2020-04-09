---
title: Studdar atburðarás fyrir tvískipt skrifun
description: Þetta efni lýsir atburðarásum sem eru studdar fyrir tvískipt skrifun.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d7ff514768ee8e4797b591da89e190a855385885
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172855"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="ca8d9-103">Studdar atburðarás fyrir tvískipt skrifun</span><span class="sxs-lookup"><span data-stu-id="ca8d9-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="ca8d9-104">Þú getur sett upp tvískipt samband milli Finance and Operations umhverfis og Common Data Service umhverfis.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="ca8d9-105">Umhverfi **Finance and Operations** veitir undirliggjandi verkvang fyrir smáforrit **Finance and Operations** (til dæmis Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail og Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="ca8d9-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="ca8d9-106">**Common Data Service-umhverfi** veitir undirliggjandi verkvang fyrir **líkanadrifin forrit í Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="ca8d9-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="ca8d9-107">Skipulagið er mismunandi eftir áskrift og umhverfi.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="ca8d9-108">Fyrir ný tilvik af forrit Finance and Operations hefst uppsetningin á tvískiptri tengingu í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ca8d9-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ca8d9-109">Ef þú ert með leyfi fyrir Microsoft Power Platform geturðu fengið nýtt umhverfi Common Data Service ef leigjandi þinn hefur ekki slíkt.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="ca8d9-110">Fyrir núverandi tilvik forrita Finance and Operations hefst uppsetning tvískiptrar tengingar í umhverfi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="ca8d9-111">Eftirfarandi uppsetningaraðstæður eru studdar:</span><span class="sxs-lookup"><span data-stu-id="ca8d9-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="ca8d9-112">Nýtt forritstilvik Finance and Operations og nýtt líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="ca8d9-113">Nýtt forritstilvik Finance and Operations og fyrirliggjandi líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="ca8d9-114">Nýtt forritstilvik Finance and Operations sem er með sýnigögn og nýtt líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="ca8d9-115">Nýtt forritstilvik Finance and Operations sem er með sýnigögn og fyrirliggjandi líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="ca8d9-116">Fyrirliggjandi forritstilvik Finance and Operations og nýtt eða fyrirliggjandi líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="ca8d9-117">Nýtt forritstilvik Finance and Operations og nýtt líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="ca8d9-118">Til að koma á tvískiptri tengingu milli nýs dæmi um forrit Finance and Operations sem hefur engin gögn og nýtt tilvik af líkanadrifnu forriti í Dynamics 365 fylgirðu skrefunum í [Tvískipt uppsetning úr Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ca8d9-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="ca8d9-119">Þegar uppsetningu tengingarinnar er lokið fara eftirfarandi aðgerðir sjálfkrafa fram:</span><span class="sxs-lookup"><span data-stu-id="ca8d9-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="ca8d9-120">Nýtt, tómt umhverfi Finance and Operations er veitt.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="ca8d9-121">Nýtt, tómt tilvik af líkanadrifnu forriti er útbúið þar sem CRM frumlausnin er sett upp.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="ca8d9-122">Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="ca8d9-123">Einingakort eru virk fyrir samstillingu í beinni.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="ca8d9-124">Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="ca8d9-125">Nýtt forritstilvik Finance and Operations og fyrirliggjandi líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="ca8d9-126">Til að koma á tvískiptri tengingu milli nýs dæmi um forrit Finance and Operations sem hefur engin gögn og fyrirliggjandi tilvik af líkanadrifnu forriti í Dynamics 365 fylgirðu skrefunum í [Tvískipt uppsetning úr Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ca8d9-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="ca8d9-127">Þegar uppsetningu tengingarinnar er lokið fara eftirfarandi aðgerðir sjálfkrafa fram:</span><span class="sxs-lookup"><span data-stu-id="ca8d9-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="ca8d9-128">Nýtt, tómt umhverfi Finance and Operations er veitt.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="ca8d9-129">Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="ca8d9-130">Einingakort eru virk fyrir samstillingu í beinni.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="ca8d9-131">Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="ca8d9-132">Til að samstilla fyrirliggjandi gögn Common Data Service við forrit Finance and Operations fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="ca8d9-133">Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="ca8d9-134">Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="ca8d9-135">[Ræstu](bootstrap-company-data.md) Common Data Service-gögnin með því að nota þriggja stafa fyrirtækjakóða Alþjóðlegu staðlastofnunarinnar (ISO).</span><span class="sxs-lookup"><span data-stu-id="ca8d9-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="ca8d9-136">Þar sem tvískipt skrifun er í samstillingarstillingu í beinni fara gögnin úr Common Data Service sjálfkrafa að flæða í forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="ca8d9-137">Nýtt forritstilvik Finance and Operations sem er með sýnigögn og nýtt líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="ca8d9-138">Til að koma á tvískiptri tengingu milli nýs dæmi um forrit Finance and Operations sem er með kynningargögn og nýtt tilvik líkanadrifins forrits í Dynamics 365 fylgirðu skrefunum í hlutanum [Nýtt forritstilvik Finance and Operations og nýtt tilvik líkanadrifins forrits](#new-new) fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="ca8d9-139">Þegar uppsetningu á tengingunni er lokið, ef þú vilt samstilla kynningargögnin við líkanadrifna forritið, fylgdu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="ca8d9-140">Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="ca8d9-141">Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="ca8d9-142">Nýtt forritstilvik Finance and Operations sem er með sýnigögn og fyrirliggjandi líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="ca8d9-143">Til að koma á tvískiptri tengingu milli nýs dæmi um forrit Finance and Operations sem er með kynningargögn og fyrirliggjandi tilvik líkanadrifins forrits í Dynamics 365 fylgirðu skrefunum í hlutanum [Nýtt forritstilvik Finance and Operations og fyrirliggjandi tilvik líkanadrifins forrits](#new-existing) fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="ca8d9-144">Þegar uppsetningu á tengingunni er lokið, ef þú vilt samstilla kynningargögnin við líkanadrifna forritið, fylgdu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="ca8d9-145">Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="ca8d9-146">Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="ca8d9-147">Til að samstilla fyrirliggjandi gögn Common Data Service við forrit Finance and Operations fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="ca8d9-148">Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="ca8d9-149">Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="ca8d9-150">[Ræstu](bootstrap-company-data.md) Common Data Service-gögnin með því að nota þriggja stafa fyrirtækjakóða ISO.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="ca8d9-151">Þar sem tvískipt skrifun er í samstillingarstillingu í beinni fara gögnin úr Common Data Service sjálfkrafa að flæða í forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="ca8d9-152">Fyrirliggjandi forritstilvik Finance and Operations og nýtt eða fyrirliggjandi líkanadrifið forritstilvik</span><span class="sxs-lookup"><span data-stu-id="ca8d9-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="ca8d9-153">Skipulag á tvískiptri tengingu milli núverandi dæmi um forrit Finance and Operations og nýtt eða núverandi dæmi um líkanadrifið forrit í Dynamics 365 á sér stað í umhverfi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="ca8d9-154">Settu upp tenginguna úr forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="ca8d9-155">Til að samstilla núverandi Common Data Service-gögn við forrit Finance and Operations, [skaltu ræsa](bootstrap-company-data.md) Common Data Service-gögnin með þriggja stafa ISO fyrirtækjakóða.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="ca8d9-156">Þar sem tvískipt skrifun er í samstillingarstillingu í beinni fara gögnin úr Common Data Service sjálfkrafa að flæða í forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

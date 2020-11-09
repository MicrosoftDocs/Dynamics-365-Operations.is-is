---
title: Leiðsögn fyrir uppsetningu tvöfaldra skrifa
description: Þetta efni lýsir atburðarásum sem eru studdar fyrir tvískipt skrifun.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088507"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="27d77-103">Leiðsögn fyrir uppsetningu tvöfaldra skrifa</span><span class="sxs-lookup"><span data-stu-id="27d77-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="27d77-104">Þú getur sett upp tvískipt samband milli Finance and Operations umhverfis og Common Data Service umhverfis.</span><span class="sxs-lookup"><span data-stu-id="27d77-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="27d77-105">**Finance and Operations umhverfi** býður upp á undirliggjandi verkvanginn fyrir **Finance and Operations forrit** (til dæmis Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="27d77-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="27d77-106">**Common Data Service Umhverfi** veitir undirliggjandi verkvang fyrir **forrit viðskiptavina** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="27d77-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="27d77-107">Mannauður í Finance and Operations styður tengingu tvískiptra skrifa, en Dynamics 365 Human Resources-forritið gerir það ekki.</span><span class="sxs-lookup"><span data-stu-id="27d77-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="27d77-108">Skipulagið er mismunandi eftir áskrift og umhverfi.</span><span class="sxs-lookup"><span data-stu-id="27d77-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="27d77-109">Fyrir ný tilvik af forrit Finance and Operations hefst uppsetningin á tvískiptri tengingu í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="27d77-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="27d77-110">Ef þú ert með leyfi fyrir Power Platform geturðu fengið nýtt umhverfi Common Data Service ef leigjandi þinn hefur ekki slíkt.</span><span class="sxs-lookup"><span data-stu-id="27d77-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="27d77-111">Fyrir núverandi tilvik forrita Finance and Operations hefst uppsetning tvískiptrar tengingar í umhverfi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27d77-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="27d77-112">Áður en þú ræsir tvírita í einingu er hægt að keyra fyrstu samstillingu til að meðhöndla fyrirliggjandi gögn á báðum hliðum Finance and Operations -forrita og Customer Engagement-forrita.</span><span class="sxs-lookup"><span data-stu-id="27d77-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="27d77-113">Hægt er að sleppa upphaflegu samkeyrslunni ef ekki þarf að samstilla gögn á milli tveggja umhverfa.</span><span class="sxs-lookup"><span data-stu-id="27d77-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="27d77-114">Upphafleg samstilling gerir notanda kleift að afrita fyrirliggjandi gögn úr einu forriti í annað.</span><span class="sxs-lookup"><span data-stu-id="27d77-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="27d77-115">Ýmsar mismunandi uppsetningaráætlanir eru eftir því hvaða umhverfi er þegar til staðar og hvaða gerð gagna er í umhverfi.</span><span class="sxs-lookup"><span data-stu-id="27d77-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="27d77-116">Eftirfarandi uppsetningaraðstæður eru studdar:</span><span class="sxs-lookup"><span data-stu-id="27d77-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="27d77-117">Nýtt Finance and Operations -forritstilvik og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="27d77-118">Nýtt Finance and Operations -forritatilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="27d77-119">Nýtt Finance and Operations -forritstilvik sem inniheldur gögn og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="27d77-120">Nýtt Finance and Operations -forritstilvik sem inniheldur gögn og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="27d77-121">Fyrirliggjandi Finance and Operations -forritstilvik og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="27d77-122">Fyrirliggjandi Finance and Operations -hugbúnaðartilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="27d77-123">Nýtt Finance and Operations forritstilvik og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="27d77-124">Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations -forriti sem inniheldur engin gögn og nýs tilviks um þjónsforrit skal fylgja skrefunum í [Uppsetning tvöfaldra skrifa úr Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="27d77-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="27d77-125">Þegar uppsetningu tengingarinnar er lokið fara eftirfarandi aðgerðir sjálfkrafa fram:</span><span class="sxs-lookup"><span data-stu-id="27d77-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="27d77-126">Nýtt, tómt umhverfi Finance and Operations er veitt.</span><span class="sxs-lookup"><span data-stu-id="27d77-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="27d77-127">Nýju, auðu tilviki af forriti viðskiptavinar er úthlutað, þar sem CRM úrvalslausnin er uppsett.</span><span class="sxs-lookup"><span data-stu-id="27d77-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="27d77-128">Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="27d77-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="27d77-129">Einingakort eru virk fyrir samstillingu í beinni.</span><span class="sxs-lookup"><span data-stu-id="27d77-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="27d77-130">Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="27d77-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="27d77-131">Nýtt Finance and Operations -hugbúnaðartilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="27d77-132">Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations -forriti sem inniheldur engin gögn og fyrirliggjandi tilvik um þjónsforrit skal fylgja skrefunum í [Uppsetning tvöfaldra skrifa úr Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="27d77-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="27d77-133">Þegar uppsetningu tengingarinnar er lokið fara eftirfarandi aðgerðir sjálfkrafa fram:</span><span class="sxs-lookup"><span data-stu-id="27d77-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="27d77-134">Nýtt, tómt umhverfi Finance and Operations er veitt.</span><span class="sxs-lookup"><span data-stu-id="27d77-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="27d77-135">Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="27d77-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="27d77-136">Einingakort eru virk fyrir samstillingu í beinni.</span><span class="sxs-lookup"><span data-stu-id="27d77-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="27d77-137">Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="27d77-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="27d77-138">Til að samstilla fyrirliggjandi gögn Common Data Service við forrit Finance and Operations fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="27d77-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="27d77-139">Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27d77-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="27d77-140">Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="27d77-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="27d77-141">[Ræstu](bootstrap-company-data.md) Common Data Service-gögnin með því að nota þriggja stafa fyrirtækjakóða Alþjóðlegu staðlastofnunarinnar (ISO).</span><span class="sxs-lookup"><span data-stu-id="27d77-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="27d77-142">Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="27d77-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27d77-143">Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).</span><span class="sxs-lookup"><span data-stu-id="27d77-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="27d77-144">Nýtt Finance and Operations forritstilvik sem inniheldur gögn og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="27d77-145">Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations forriti sem inniheldur gögn og nýtt tilvik fyrir þátt viðskiptaþjónsforrits skal fylgja skrefunum í [Nýtt Finance and Operations forritstilviks og nýtt tilvik fyrir forrit viðskiptavinar](#new-new) í fyrri hluta þessa efnisatriðis.</span><span class="sxs-lookup"><span data-stu-id="27d77-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="27d77-146">Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="27d77-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="27d77-147">Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="27d77-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="27d77-148">Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="27d77-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27d77-149">Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).</span><span class="sxs-lookup"><span data-stu-id="27d77-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="27d77-150">Nýtt Finance and Operations hugbúnaðartilvik þar sem gögn og fyrirliggjandi forrit fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="27d77-151">Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations forriti sem inniheldur gögn og fyrirliggjandi tilvik um þátt viðskiptaþjónsforrits skal fylgja skrefunum í [Nýtt Finance and Operations forritstilvik og núverandi tilvik viðskiptaforritstilviks](#new-existing) kaflanum fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="27d77-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="27d77-152">Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="27d77-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="27d77-153">Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="27d77-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="27d77-154">Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="27d77-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27d77-155">Til að samstilla fyrirliggjandi gögn Common Data Service við forrit Finance and Operations fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="27d77-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="27d77-156">Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27d77-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="27d77-157">Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="27d77-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="27d77-158">[Ræstu](bootstrap-company-data.md) Common Data Service-gögnin með því að nota þriggja stafa fyrirtækjakóða ISO.</span><span class="sxs-lookup"><span data-stu-id="27d77-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="27d77-159">Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="27d77-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27d77-160">Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).</span><span class="sxs-lookup"><span data-stu-id="27d77-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="27d77-161">Fyrirliggjandi Finance and Operations forritstilviks og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="27d77-162">Uppsetning á tvískrifstengingu á milli nýs tilviks Finance and Operations forritsins og fyrirliggjandi tilviks fyrir Customer Engagement forrit Finance and Operation-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="27d77-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="27d77-163">[Setja upp tenginguna úr Finance and Operations forritinu](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="27d77-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="27d77-164">Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="27d77-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27d77-165">Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).</span><span class="sxs-lookup"><span data-stu-id="27d77-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="27d77-166">Fyrirliggjandi Finance and Operations -hugbúnaðartilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="27d77-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="27d77-167">Uppsetning á tvískrifstengingu á milli núverandi tilviks Finance and Operations forritsins og fyrirliggjandi tilviks fyrir Customer Engagement forrit Finance and Operation-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="27d77-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="27d77-168">Settu upp tenginguna úr forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27d77-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="27d77-169">Til að samstilla núverandi Common Data Service-gögn við forrit Finance and Operations, [skaltu ræsa](bootstrap-company-data.md) Common Data Service-gögnin með þriggja stafa ISO fyrirtækjakóða.</span><span class="sxs-lookup"><span data-stu-id="27d77-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="27d77-170">Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="27d77-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27d77-171">Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).</span><span class="sxs-lookup"><span data-stu-id="27d77-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="27d77-172">Dæmi</span><span class="sxs-lookup"><span data-stu-id="27d77-172">Example</span></span>

<span data-ttu-id="27d77-173">Til dæmis [Virkjun viðskiptavina v3 — einingakort tengiliða](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="27d77-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="27d77-174">Ef um er að ræða aðra nálgun sem byggist á gagnamagni í hverri einingu sem þarf að keyra upphaflega samstillingu, sjá [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="27d77-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>

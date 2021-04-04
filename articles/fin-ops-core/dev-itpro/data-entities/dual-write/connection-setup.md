---
title: Leiðbeinigar fyrir uppsetningu tvöfaldra skrifa
description: Þetta efni lýsir atburðarásum sem eru studdar fyrir tvískipt skrifun.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: dee6bc52a0967dfd6134258d3a02dc18feb404a5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560226"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="8522d-103">Leiðbeinigar fyrir uppsetningu tvöfaldra skrifa</span><span class="sxs-lookup"><span data-stu-id="8522d-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8522d-104">Þú getur sett upp tvískipt samband milli Finance and Operations umhverfis og Dataverse umhverfis.</span><span class="sxs-lookup"><span data-stu-id="8522d-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="8522d-105">Umhverfi **Finance and Operations** veitir undirliggjandi verkvang fyrir smáforrit **Finance and Operations** (til dæmis Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="8522d-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="8522d-106">**Dataverse Umhverfi** veitir undirliggjandi verkvang fyrir **forrit viðskiptavina** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="8522d-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8522d-107">Mannauðseiningin í Dynamics 365 Finance styður tengingu tvískiptra skrifa, en Dynamics 365 Human Resources-forritið gerir það ekki.</span><span class="sxs-lookup"><span data-stu-id="8522d-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="8522d-108">Uppsetningarkerfi er breytilegt, allt eftir áskrift þinni og umhverfi:</span><span class="sxs-lookup"><span data-stu-id="8522d-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="8522d-109">Fyrir ný tilvik af forrit Finance and Operations hefst uppsetningin á tvískiptri tengingu í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8522d-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8522d-110">Ef þú ert með leyfi fyrir Microsoft Power Platform geturðu fengið nýtt umhverfi Dataverse ef leigjandi þinn hefur ekki slíkt.</span><span class="sxs-lookup"><span data-stu-id="8522d-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="8522d-111">Fyrir núverandi tilvik forrita Finance and Operations hefst uppsetning tvískiptrar tengingar í umhverfi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8522d-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="8522d-112">Áður en þú ræsir tvírita í einingu er hægt að keyra fyrstu samstillingu til að meðhöndla fyrirliggjandi gögn á báðum hliðum Finance and Operations -forrita og Customer Engagement-forrita.</span><span class="sxs-lookup"><span data-stu-id="8522d-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="8522d-113">Hægt er að sleppa upphaflegu samstillingunni ef ekki þarf að samstilla gögn á milli umhverfanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="8522d-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="8522d-114">Upphafleg samstilling gerir notanda kleift að afrita fyrirliggjandi gögn úr einu forriti í annað.</span><span class="sxs-lookup"><span data-stu-id="8522d-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="8522d-115">Nokkrar uppsetningaraðstæður eru til staðar, allt eftir því umhverfi sem er þegar til staðar og gerð gagna í þeim.</span><span class="sxs-lookup"><span data-stu-id="8522d-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="8522d-116">Eftirfarandi uppsetningaraðstæður eru studdar:</span><span class="sxs-lookup"><span data-stu-id="8522d-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="8522d-117">Nýtt Finance and Operations -forritstilvik og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="8522d-118">Nýtt Finance and Operations -forritatilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="8522d-119">Nýtt Finance and Operations -forritstilvik sem inniheldur gögn og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="8522d-120">Nýtt Finance and Operations -forritstilvik sem inniheldur gögn og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="8522d-121">Fyrirliggjandi Finance and Operations -forritstilvik og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="8522d-122">Fyrirliggjandi Finance and Operations -hugbúnaðartilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="8522d-123">Nýtt Finance and Operations forritstilvik og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="8522d-124">Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations -forriti sem inniheldur engin gögn og nýs tilviks um þjónsforrit skal fylgja skrefunum í [Uppsetning tvöfaldra skrifa úr Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="8522d-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="8522d-125">Þegar uppsetningu tengingar er lokið eiga eftirfarandi aðgerðir sér stað sjálfkrafa:</span><span class="sxs-lookup"><span data-stu-id="8522d-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="8522d-126">Nýtt, tómt umhverfi Finance and Operations er veitt.</span><span class="sxs-lookup"><span data-stu-id="8522d-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="8522d-127">Nýju, auðu tilviki af forriti viðskiptavinar er úthlutað, þar sem CRM úrvalslausnin er uppsett.</span><span class="sxs-lookup"><span data-stu-id="8522d-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="8522d-128">Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="8522d-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="8522d-129">Töflukort eru virkjuð fyrir samstillingu í beinni.</span><span class="sxs-lookup"><span data-stu-id="8522d-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="8522d-130">Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="8522d-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="8522d-131">Nýtt Finance and Operations -hugbúnaðartilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="8522d-132">Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations -forriti sem inniheldur engin gögn og fyrirliggjandi tilvik um þjónsforrit skal fylgja skrefunum í [Uppsetning tvöfaldra skrifa úr Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="8522d-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="8522d-133">Þegar uppsetningu tengingar er lokið eiga eftirfarandi aðgerðir sér stað sjálfkrafa:</span><span class="sxs-lookup"><span data-stu-id="8522d-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="8522d-134">Nýtt, tómt umhverfi Finance and Operations er veitt.</span><span class="sxs-lookup"><span data-stu-id="8522d-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="8522d-135">Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="8522d-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="8522d-136">Töflukort eru virkjuð fyrir samstillingu í beinni.</span><span class="sxs-lookup"><span data-stu-id="8522d-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="8522d-137">Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="8522d-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="8522d-138">Til að samstilla fyrirliggjandi gögn Dataverse við forrit Finance and Operations fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8522d-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="8522d-139">Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8522d-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="8522d-140">Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="8522d-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="8522d-141">[Ræstu](bootstrap-company-data.md) Dataverse-gögnin með því að nota þriggja stafa fyrirtækjakóða Alþjóðlegu staðlastofnunarinnar (ISO).</span><span class="sxs-lookup"><span data-stu-id="8522d-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="8522d-142">Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="8522d-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="8522d-143">Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example) síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="8522d-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="8522d-144">Nýtt Finance and Operations forritstilvik sem inniheldur gögn og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="8522d-145">Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations forriti sem inniheldur gögn og nýtt tilvik fyrir þátt viðskiptaþjónsforrits skal fylgja skrefunum í [Nýtt Finance and Operations forritstilviks og nýtt tilvik fyrir forrit viðskiptavinar](#new-new) í fyrri hluta þessa efnisatriðis.</span><span class="sxs-lookup"><span data-stu-id="8522d-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="8522d-146">Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8522d-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="8522d-147">Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="8522d-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="8522d-148">Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="8522d-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="8522d-149">Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).</span><span class="sxs-lookup"><span data-stu-id="8522d-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="8522d-150">Nýtt Finance and Operations hugbúnaðartilvik þar sem gögn og fyrirliggjandi forrit fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="8522d-151">Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations forriti sem inniheldur gögn og fyrirliggjandi tilvik um þátt viðskiptaþjónsforrits skal fylgja skrefunum í [Nýtt Finance and Operations forritstilvik og núverandi tilvik viðskiptaforritstilviks](#new-existing) kaflanum fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="8522d-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="8522d-152">Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8522d-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="8522d-153">Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="8522d-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="8522d-154">Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="8522d-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="8522d-155">Til að samstilla fyrirliggjandi gögn Dataverse við forrit Finance and Operations fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8522d-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="8522d-156">Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8522d-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="8522d-157">Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="8522d-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="8522d-158">[Ræstu](bootstrap-company-data.md) Dataverse-gögnin með því að nota þriggja stafa fyrirtækjakóða ISO.</span><span class="sxs-lookup"><span data-stu-id="8522d-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="8522d-159">Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="8522d-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="8522d-160">Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).</span><span class="sxs-lookup"><span data-stu-id="8522d-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="8522d-161">Fyrirliggjandi Finance and Operations forritstilviks og nýtt tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="8522d-162">Uppsetning á tvískrifstengingu á milli nýs tilviks Finance and Operations forritsins og fyrirliggjandi tilviks fyrir Customer Engagement forrit Finance and Operation-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="8522d-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="8522d-163">[Setja upp tenginguna úr Finance and Operations forritinu](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="8522d-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="8522d-164">Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="8522d-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="8522d-165">Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).</span><span class="sxs-lookup"><span data-stu-id="8522d-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="8522d-166">Fyrirliggjandi Finance and Operations -hugbúnaðartilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="8522d-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="8522d-167">Uppsetning á tvískrifstengingu á milli núverandi tilviks Finance and Operations forritsins og fyrirliggjandi tilviks fyrir Customer Engagement forrit Finance and Operation-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="8522d-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="8522d-168">[Setja upp tenginguna úr Finance and Operations forritinu](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="8522d-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="8522d-169">Til að samstilla núverandi Dataverse-gögn við forrit Finance and Operations, [skaltu ræsa](bootstrap-company-data.md) Dataverse-gögnin með þriggja stafa ISO fyrirtækjakóða.</span><span class="sxs-lookup"><span data-stu-id="8522d-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="8522d-170">Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="8522d-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="8522d-171">Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).</span><span class="sxs-lookup"><span data-stu-id="8522d-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="8522d-172">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8522d-172">Example</span></span>

<span data-ttu-id="8522d-173">Sjá til dæmis [Virkjun viðskiptavina v3 — Töflukort tengiliða](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="8522d-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="8522d-174">Ef um er að ræða aðra nálgun sem byggir á gagnamagni í hverri einingu sem þarf að keyra upphaflega samstillingu, sjá [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="8522d-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
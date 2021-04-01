---
title: Setja upp og uppfæra viðskiptavinagátt
description: Þetta efnisatriði inniheldur upplýsingar um leyfi og uppsetningarleiðbeiningar fyrir viðskiptavinagáttina.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fa95995320a0f81c040eeebe6fd796200fbff13f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255038"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="fb956-103">Setja upp og uppfæra viðskiptavinagátt</span><span class="sxs-lookup"><span data-stu-id="fb956-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="fb956-104">Leyfiskröfur</span><span class="sxs-lookup"><span data-stu-id="fb956-104">Licensing requirements</span></span>

<span data-ttu-id="fb956-105">Til að innleiða viðskiptavinagáttina þarf að hafa eftirfarandi leyfi:</span><span class="sxs-lookup"><span data-stu-id="fb956-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="fb956-106">**Power Apps gáttir** – Þetta leyfi þarf til að hýsa viðskiptavinagáttina.</span><span class="sxs-lookup"><span data-stu-id="fb956-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="fb956-107">Gáttir fá leyfi samkvæmt notkun.</span><span class="sxs-lookup"><span data-stu-id="fb956-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="fb956-108">Frekari upplýsingar er að finna í [Leyfiskröfur Power Apps-gátta](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="fb956-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="fb956-109">**Tvöföld skrif** - Nauðsynlegt er að hafa réttu leyfin til að virkja tvöföld skrif fyrir töflur Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fb956-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management tables.</span></span> <span data-ttu-id="fb956-110">Frekari upplýsingar er að finna í [kerfiskröfur fyrir tvöföld skrif](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="fb956-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="fb956-111">Tengsl í tvöföldum skrifum og Power Apps-gáttum</span><span class="sxs-lookup"><span data-stu-id="fb956-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="fb956-112">Viðskiptavinagáttin er háð Power Apps-gáttum og tvöföldum skrifum eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="fb956-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="fb956-113">![Tengsl viðskiptavinagáttar](media/customer-portal-elements.png "Tengsl viðskiptavinagáttar")</span><span class="sxs-lookup"><span data-stu-id="fb956-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="fb956-114">Ólíkt öðrum eiginleikum frá Supply Chain Management er sniðmát viðskiptavinagáttar að finna í Power Apps-gáttum.</span><span class="sxs-lookup"><span data-stu-id="fb956-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="fb956-115">Þess vegna takmarkast viðskiptavinagáttin við virknina og möguleikana sem boðið er upp á af Power Apps-gáttum og töflunum í tvöföldum skrifum.</span><span class="sxs-lookup"><span data-stu-id="fb956-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the tables in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="fb956-116">Nauðsynleg uppsetning til að virkja viðskiptavinagáttina</span><span class="sxs-lookup"><span data-stu-id="fb956-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="fb956-117">Eftir að gengið hefur verið úr skugga um að nauðsynleg leyfi séu til staðar, er hægt að setja upp tvöföld skrif eins og lýst er í [leiðbeiningum um fyrstu samstillingu tvöfaldra skrifa](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="fb956-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="fb956-118">Ganga skal úr skugga um að virkja eftirfarandi töfluvarpanir í tvöföldum skrifum:</span><span class="sxs-lookup"><span data-stu-id="fb956-118">Be sure to enable the following table mappings in dual-write:</span></span>

- <span data-ttu-id="fb956-119">Sölupöntunarhaus</span><span class="sxs-lookup"><span data-stu-id="fb956-119">Sales Order Header</span></span>
- <span data-ttu-id="fb956-120">Upplýsingar um sölupöntun</span><span class="sxs-lookup"><span data-stu-id="fb956-120">Sales Order Details</span></span>
- <span data-ttu-id="fb956-121">Lyklar</span><span class="sxs-lookup"><span data-stu-id="fb956-121">Accounts</span></span>
- <span data-ttu-id="fb956-122">Tengiliðir</span><span class="sxs-lookup"><span data-stu-id="fb956-122">Contacts</span></span>
- <span data-ttu-id="fb956-123">Afurðir</span><span class="sxs-lookup"><span data-stu-id="fb956-123">Products</span></span>

<span data-ttu-id="fb956-124">Þegar þessari uppsetningu er lokið er hægt að úthluta sniðmáti viðskiptavinagáttar.</span><span class="sxs-lookup"><span data-stu-id="fb956-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="fb956-125">Úthluta viðskiptavinagátt</span><span class="sxs-lookup"><span data-stu-id="fb956-125">Provision the Customer portal</span></span>

<span data-ttu-id="fb956-126">Áður en hafist er handa skal ganga úr skugga um að [nauðsynlegri uppsetningu](#required-setup) sé lokið.</span><span class="sxs-lookup"><span data-stu-id="fb956-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="fb956-127">Síðan skal fylgja þessum skrefum til að úthluta viðskiptavinagáttinni.</span><span class="sxs-lookup"><span data-stu-id="fb956-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="fb956-128">Opnið [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="fb956-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="fb956-129">Gangið úr skugga um að notað sé umhverfið þar sem tvöföld skrif voru virkjuð.</span><span class="sxs-lookup"><span data-stu-id="fb956-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="fb956-130">Á flipanum **Stofna** skal fletta niður á hlutann **Byrja á sniðmáti** og velja sniðmátið sem heitir **Viðskiptavinagátt**.</span><span class="sxs-lookup"><span data-stu-id="fb956-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="fb956-131">Fylgdu leiðbeiningunum á skjánum.</span><span class="sxs-lookup"><span data-stu-id="fb956-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="fb956-132">Eftir að úthlutun er lokið er hægt að fá aðgang að viðskiptavinagáttinni í hlutanum **Forritin þín** á síðunni **Heim**.</span><span class="sxs-lookup"><span data-stu-id="fb956-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="fb956-133">Ef lausn tvöfaldra skrifa er ekki uppsett í umhverfinu sem unnið er í koma upp villuboð og viðskiptavinagáttinni verður ekki úthlutað.</span><span class="sxs-lookup"><span data-stu-id="fb956-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="fb956-134">Uppfæra viðskiptavinagáttina</span><span class="sxs-lookup"><span data-stu-id="fb956-134">Update the Customer portal</span></span>

<span data-ttu-id="fb956-135">Meiri virkni verður hugsanlega bætt við viðskiptavinagáttina síðar.</span><span class="sxs-lookup"><span data-stu-id="fb956-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="fb956-136">Allar breytingar sem Microsoft gerir á undirliggjandi hlutum lausnar munu sjálfkrafa birtast í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="fb956-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="fb956-137">Hins vegar mun vefsvæðið sem er úthlutað í umhverfinu ekki sjálfkrafa endurspegla breytingar sem eru gerðar á skilgreiningargögnunum.</span><span class="sxs-lookup"><span data-stu-id="fb956-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="fb956-138">Bæta verður þessum breytingum við handvirkt með því að ná í kóða frá nýja sniðmátinu og sameina það við úthlutað vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="fb956-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb956-139">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="fb956-139">Additional resources</span></span>

<span data-ttu-id="fb956-140">Til að komast að því hvernig á að setja upp og sérsníða viðskiptavinagáttina ætti að byrja á því að fara yfir eftirfarandi fylgiskjöl fyrir undirliggjandi tækni:</span><span class="sxs-lookup"><span data-stu-id="fb956-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="fb956-141">Power Apps fylgiskjöl gátta</span><span class="sxs-lookup"><span data-stu-id="fb956-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="fb956-142">Tvískrifuð fylgiskjöl</span><span class="sxs-lookup"><span data-stu-id="fb956-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="fb956-143">Til að stjórna gáttunum á áhrifaríkan hátt þarf að skilja gáttir Power Apps og stuðningstíma Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fb956-143">To effectively manage your portals, you must understand the Power Apps portals and Microsoft Dataverse lifecycle.</span></span> <span data-ttu-id="fb956-144">Frekari upplýsingar er að finna í eftirfarandi tilföngum:</span><span class="sxs-lookup"><span data-stu-id="fb956-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="fb956-145">Um stuðningstíma gáttar</span><span class="sxs-lookup"><span data-stu-id="fb956-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="fb956-146">Uppfæra gátt</span><span class="sxs-lookup"><span data-stu-id="fb956-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="fb956-147">Flytja grunnstillingu gáttar</span><span class="sxs-lookup"><span data-stu-id="fb956-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="fb956-148">Solution Lifecycle Management: Dynamics 365 fyrir forrit Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="fb956-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
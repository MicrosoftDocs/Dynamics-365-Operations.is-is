---
title: Starfsmenn ábyrgir fyrir samþykki ósamkvæmni
description: Í þessu efnisatriði er lýst hvernig á að skilgreina starfsmenn sem bera ábyrgð á að samþykkja ósamkvæm atriði.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956702"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="85414-103">Starfsmenn ábyrgir fyrir samþykki ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="85414-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85414-104">Í þessu efnisatriði er lýst hvernig á að skilgreina starfsmenn sem bera ábyrgð á að samþykkja ósamkvæm atriði.</span><span class="sxs-lookup"><span data-stu-id="85414-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="85414-105">Samþykkja verður ósamkvæmni áður en notendur geta byrjað að færa inn upplýsingar á borð við leiðréttingar eða aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="85414-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="85414-106">Áður en notendur geta samþykkt eða hafnað ósamkvæmni verður að tengja notandakenni (notandafærslu) þeirra við starfsmannaskrá.</span><span class="sxs-lookup"><span data-stu-id="85414-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="85414-107">Þú getur valið að velja starfskrafta sem bera ábyrgð á gæðum og leyfa síðan einum starfsmanni að samþykkja vinnu fyrir hönd annars starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="85414-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="85414-108">Virkja notanda fyrir úrvinnslu ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="85414-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="85414-109">Áður en notandi getur samþykkt eða hafnað ósamkvæmni þarftu að tengja notanafærslu þeirra við starfsmannaskrá.</span><span class="sxs-lookup"><span data-stu-id="85414-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="85414-110">Síðan er hægt að stilla samþykkissvæðin sjálfvirkt og fylla út núverandi notanda sjálfkrafa fyrir vinnukortið.</span><span class="sxs-lookup"><span data-stu-id="85414-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="85414-111">Áður en notandi getur notað athugasemdir skjals þarftu að virkja skjalameðhöndlun í valkostum notanda.</span><span class="sxs-lookup"><span data-stu-id="85414-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="85414-112">Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.</span><span class="sxs-lookup"><span data-stu-id="85414-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="85414-113">Finnið og opnið notandann sem á að geta samþykkt eða hafnað ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="85414-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="85414-114">Stillið reitinn **Einstaklingur** á heiti starfsmannsins sem tengist núgildandi notandafærslu.</span><span class="sxs-lookup"><span data-stu-id="85414-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="85414-115">Á aðgerðasvæðinu skal velja **Valkostir notanda**.</span><span class="sxs-lookup"><span data-stu-id="85414-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="85414-116">Á síðunni **Valkostir** fyrir núverandi færslu notanda, í flipanum **Kjörstillingar**, skal stilla valkostinn **Virkja skjalameðhöndlun** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="85414-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="85414-117">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="85414-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="85414-118">Skilgreina starfskrafta sem bera ábyrgð á gæðum</span><span class="sxs-lookup"><span data-stu-id="85414-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="85414-119">Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Starfsmenn ábyrgir fyrir gæðum**.</span><span class="sxs-lookup"><span data-stu-id="85414-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="85414-120">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="85414-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="85414-121">Í reitnum **Starfskraftur** skal velja starfsmanninn sem slær inn gæðaupplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="85414-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="85414-122">Í retinum **Ábyrgur starfsmaður** skal velja starfsmanninn sem valinn starfsmaður slær inn vinnu fyrir.</span><span class="sxs-lookup"><span data-stu-id="85414-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="85414-123">Þegar ósamkvæmni er búin til og uppfærð mun þessi starfsmaður vera sleginn inn sjálfgefið í reitinn **Starfskraftur**.</span><span class="sxs-lookup"><span data-stu-id="85414-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85414-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="85414-124">Additional resources</span></span>

- [<span data-ttu-id="85414-125">Gæðastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="85414-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="85414-126">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="85414-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="85414-127">Gæðagjöld</span><span class="sxs-lookup"><span data-stu-id="85414-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="85414-128">Biðgeymslusvæði fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="85414-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="85414-129">Gerðir greininga fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="85414-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="85414-130">Gæðagjöld fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="85414-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="85414-131">Aðgerðir fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="85414-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="85414-132">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="85414-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

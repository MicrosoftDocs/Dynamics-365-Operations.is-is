---
title: Takmörkun á breytingu persónuupplýsinga
description: Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum í Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e43b9127b247fa618558b725837d12bf290662f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052026"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="24a92-103">Takmörkun á breytingu persónuupplýsinga</span><span class="sxs-lookup"><span data-stu-id="24a92-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="24a92-104">Þetta efnisatriði lýsir því hvernig á að takmarka getu starfsmanna til að breyta tengiliðaupplýsingum í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="24a92-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="24a92-105">Þú gætir viljað koma í veg fyrir að starfsmenn geti breytt ákvenum samskiptaupplýsingum á borð við staðsetningu fyrirtækis þeirra eða netfang.</span><span class="sxs-lookup"><span data-stu-id="24a92-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="24a92-106">Til að nota þennan möguleika þarf fyrist að virkja **(Forskoðun) Takmarka möguleika starfsmanna á að bæta við eða breyta aðsetri og tengiliðaupplýsingum í völdum tilgangi.** í eiginleikastjórnun.</span><span class="sxs-lookup"><span data-stu-id="24a92-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="24a92-107">Frekari upplýsingar um hvernig forskoðunareiginleikar eru virkjaðir er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="24a92-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="24a92-108">![Virkja forskoðunareiginleika](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="24a92-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="24a92-109">Velja upplýsingarnar sem starfsmaður getur bætt við eða breytt</span><span class="sxs-lookup"><span data-stu-id="24a92-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="24a92-110">Í mannauði, veljið **Starfsmannastjórnun**, veljið **Tenglar** og veljið svo **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="24a92-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Opna Færibreytur mannauðs](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="24a92-112">Á síðunni **Færibreytur mannauðs** skal velja flipann **Sjálfsafgreiðsla starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="24a92-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Veljið Sjálfsafgreiðsla starfsmanna](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="24a92-114">Í flipanum **Sjálfsafgreiðsla starfsmanna** skal afhaka allar upplýsingar í hlutanum **Aðseturs og tengiliðaupplýsingar** sem starfsmenn eiga ekki að fá að bæta við eða breyta.</span><span class="sxs-lookup"><span data-stu-id="24a92-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="24a92-115">Í þessu dæmi höfum við ekki afhakað tengiliðaupplýsingarnar **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="24a92-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Takmarka breytingar á tengiliðaupplýsingum fyrirtækis](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="24a92-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="24a92-117">Select **Save**.</span></span>

   ![Vista breytingar](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="24a92-119">Reynsla starfsmanns</span><span class="sxs-lookup"><span data-stu-id="24a92-119">Employee experience</span></span>

<span data-ttu-id="24a92-120">Þegar búið er að takmarka starfsmenn frá því að bæta við eða breyta tengiliðaupplýsingum geta þeir séð upplýsingar en ekki breytt þeim.</span><span class="sxs-lookup"><span data-stu-id="24a92-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="24a92-121">Í þessu dæmi, þar sem starfsmönnum er meinað að breyta tengiliðaupplýsingunum **Fyrirtæki**, geta þeir samt séð upplýsingarnar í sjálfsafgreiðslu starfsmanna:</span><span class="sxs-lookup"><span data-stu-id="24a92-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Skoða upplýsingar tengiliðar](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="24a92-123">Hins vegar, þegar þeir velja tengiliðaupplýsingar fyrirtækisins, birtist svæðið **Breyta aðsetri** sem skrifvarið og þeir geta ekki breytt neinum reitanna.</span><span class="sxs-lookup"><span data-stu-id="24a92-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Upplýsingar um viðskiptatengiliði birtast skrifvarðir](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="24a92-125">Þar að auki, ef þeir velja **Bæta við** til að bæta við nýju aðsetri, geta þeir ekki valið **Fyrirtæki** úr felliglugganum **Tilgangur**.</span><span class="sxs-lookup"><span data-stu-id="24a92-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Starfsmaður getur ekki bætt við heimilisfangi fyrirtækis](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="24a92-127">Starfsmenn fá sömu upplifun þegar þeir velja **Tengiliðaupplýsingar** á síðunni **Persónulegar upplýsingar** og bæta við nýju aðsetri.</span><span class="sxs-lookup"><span data-stu-id="24a92-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="24a92-128">Felliglugginn **Tilgangur** sýnir aðeins hvers konar upplýsingum hægt er að bæta við.</span><span class="sxs-lookup"><span data-stu-id="24a92-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Starfsmaður getur ekki valið fyrirtæki í felliglugga fyrir tilgang](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="24a92-130">**Tengiliðaupplýsingar** sýna nú **Tilgang** í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="24a92-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Tilgangur birtist í hnitaneti tengiliðaupplýsinga](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="24a92-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="24a92-132">See also</span></span>

[<span data-ttu-id="24a92-133">Yfirlit yfir sjálfsafgreiðslu starfsmanns og stjórnanda</span><span class="sxs-lookup"><span data-stu-id="24a92-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="24a92-134">Grunnstilla færibreytur Human Resources</span><span class="sxs-lookup"><span data-stu-id="24a92-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="24a92-135">Breyta persónuupplýsingum</span><span class="sxs-lookup"><span data-stu-id="24a92-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)
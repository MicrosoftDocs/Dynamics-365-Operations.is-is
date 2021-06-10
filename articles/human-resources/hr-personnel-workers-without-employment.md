---
title: Starfskraftar án starfs
description: Starfsmenn með enga framtíðarráðningu, virka ráðningu eða eldri ráðningu hjá fyrirtækinu birtast í skjámyndinni Starfskraftar án ráðningar.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6fbada6feb55b8627b1aa1ddfe367177edb7a0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051714"
---
# <a name="workers-without-employment"></a><span data-ttu-id="b9b3d-103">Starfskraftar án starfs</span><span class="sxs-lookup"><span data-stu-id="b9b3d-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b9b3d-104">Starfsmenn með enga framtíðarráðningu, virka ráðningu eða eldri ráðningu hjá fyrirtækinu birtast í skjámyndinni **Starfskraftar án ráðningar**.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="b9b3d-105">Starfsmenn með þessa stöðu geta komið fram þegar þú flytur inn starfskrafta án ráðningarfærslu eða þegar þú eyðir ráðningu starfsmanns í gegnum **Starfskraftar > Ráðningarsaga**.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="b9b3d-106">Skjámyndin **Starfskraftar án ráðningar** er sjálfkrafa í boði fyrir eftirfarandi hlutverk:</span><span class="sxs-lookup"><span data-stu-id="b9b3d-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="b9b3d-107">Aðstoðarmanneskja mannauðsstjóra</span><span class="sxs-lookup"><span data-stu-id="b9b3d-107">Human Resources Assistant</span></span>
- <span data-ttu-id="b9b3d-108">Mannauðsstjóri</span><span class="sxs-lookup"><span data-stu-id="b9b3d-108">Human Resources Manager</span></span>
- <span data-ttu-id="b9b3d-109">Ráðningaraðili</span><span class="sxs-lookup"><span data-stu-id="b9b3d-109">Recruiter</span></span>
- <span data-ttu-id="b9b3d-110">Launa- og fríðindastjóri</span><span class="sxs-lookup"><span data-stu-id="b9b3d-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="b9b3d-111">Yfirmaður launamála</span><span class="sxs-lookup"><span data-stu-id="b9b3d-111">Payroll Administrator</span></span>
- <span data-ttu-id="b9b3d-112">Launastjóri</span><span class="sxs-lookup"><span data-stu-id="b9b3d-112">Payroll Manager</span></span>
- <span data-ttu-id="b9b3d-113">Þjálfunarstjóri</span><span class="sxs-lookup"><span data-stu-id="b9b3d-113">Training Manager</span></span>

<span data-ttu-id="b9b3d-114">Í listanum **Starfsmenn án atvinnu** er hægt að eyða þeim einstaklingum sem eru taldir upp.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="b9b3d-115">Aðstoðarmanneskja mannauðsstjóra fær þessi réttindi sjálfkrafa í hendurnar.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="b9b3d-116">Þú getur veitt öðrum hlutverkum þessi réttindi með eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="b9b3d-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="b9b3d-117">Veljið **Kerfisstjórnun** og veljið svo **Öryggisstillingar**.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="b9b3d-118">Á flipanum **Réttindi** síaðu listann **Réttindi** á **Viðhalda starfsmönnum**.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="b9b3d-119">[![Afmarka lista yfir réttindi](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="b9b3d-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="b9b3d-120">Í dálkinum **Tilvísanir** veldu **Birta valmyndaratriðin**.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="b9b3d-121">Í **Birta valmyndaratriði** skal velja **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="b9b3d-122">[![Valeyðublað](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="b9b3d-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="b9b3d-123">Stillið heimildina **Eyða** á **Útdeila**.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="b9b3d-124">Veldu flipann **Óbirtir hlutir**.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="b9b3d-125">Velja **Birta allt**.</span><span class="sxs-lookup"><span data-stu-id="b9b3d-125">Select **Publish all**.</span></span>

   <span data-ttu-id="b9b3d-126">[![Birta breytingar](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="b9b3d-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
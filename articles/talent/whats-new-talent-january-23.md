---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (23. janúar 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f27698c257301f52e5c77eaa8a04ca13a0315825
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "859619"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="c58cc-103">Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (23. janúar 2019)</span><span class="sxs-lookup"><span data-stu-id="c58cc-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c58cc-104">**Smíði 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="c58cc-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="c58cc-105">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.</span><span class="sxs-lookup"><span data-stu-id="c58cc-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="c58cc-106">Breytingar</span><span class="sxs-lookup"><span data-stu-id="c58cc-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="c58cc-107">Innflutningur á föstum launum starfsmanns virkar ekki þegar nýjar skrár fyrir föst laun eru stofnaðar</span><span class="sxs-lookup"><span data-stu-id="c58cc-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="c58cc-108">Breyting hefur verið gerð á einingunni fyrir föst laun starfsmanns til að sækja launastigið við innflutning.</span><span class="sxs-lookup"><span data-stu-id="c58cc-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="c58cc-109">Fyrir þessa útgáfu birtust skilaboð um að stigið væri nauðsynlegt.</span><span class="sxs-lookup"><span data-stu-id="c58cc-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="c58cc-110">Fjarlægja reit fyrir lágmarksstöðu úr svarglugganum fyrir beiðni um frí</span><span class="sxs-lookup"><span data-stu-id="c58cc-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="c58cc-111">Reiturinn **Lágmarksstaða** hefur verið fjarlægður úr svarglugganum **Beiðni um frí**.</span><span class="sxs-lookup"><span data-stu-id="c58cc-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="c58cc-112">Þessi breyting hefur áhrif á öll svæði þar sem hægt er að biðja um frítíma.</span><span class="sxs-lookup"><span data-stu-id="c58cc-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="c58cc-113">Gagnauppfærsla fyrir launastig sem uppfærast ekki við allar kringumstæður</span><span class="sxs-lookup"><span data-stu-id="c58cc-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="c58cc-114">Breyting hefur verið gerð til að uppfæra launastigið í launafyrirkomulagi fastra launa.</span><span class="sxs-lookup"><span data-stu-id="c58cc-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="c58cc-115">Þessi breyting mun fylla út í launastigið fyrir föst laun fyrir starfið sem starfsmanninum er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="c58cc-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="c58cc-116">Upplýsingar um launaskrá á síðu breytingastjórnunar er aðeins í boði þegar notandi er skráður inn sem kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="c58cc-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="c58cc-117">Þessi breyting gerir starfsmönnum með hlutverk launastjóra kleift að fá aðgang að upplýsingum um launaskrá á síðunni **Breytir tímalínu > Stjórna breytingum** fyrir stöðuna.</span><span class="sxs-lookup"><span data-stu-id="c58cc-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="c58cc-118">Reitir starfs fá sjálfgefin gildi stöðunnar</span><span class="sxs-lookup"><span data-stu-id="c58cc-118">Job fields default to positions</span></span>
<span data-ttu-id="c58cc-119">Þegar starfi er breytt fyrir stöðu, fá reitir starfsins sjálfgefin gildi stöðunnar.</span><span class="sxs-lookup"><span data-stu-id="c58cc-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="c58cc-120">Viðvörunarskilaboð birtast sem gefur möguleika á að samþykkja sjálfgefin gildi eða halda núverandi gildum fyrir þessa reiti.</span><span class="sxs-lookup"><span data-stu-id="c58cc-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="c58cc-121">Reynslutími og dagatal eru ekki sýnd fyrir starfsmenn með langtímaráðningu.</span><span class="sxs-lookup"><span data-stu-id="c58cc-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="c58cc-122">Með þessari breytingu hefur reitunum **Reynslutímabil** og **Dagatal** verið bætt við síðuna **Stjórna breytingum** til að leyfa gagnaskráningu fyrir komandi og fyrrverandi starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="c58cc-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="c58cc-123">Update 23 fyrir verkvang</span><span class="sxs-lookup"><span data-stu-id="c58cc-123">Platform update 23</span></span>
<span data-ttu-id="c58cc-124">Minniháttar lagfærslur á villum eru innifaldar í verkvangi uppfærslu 23.</span><span class="sxs-lookup"><span data-stu-id="c58cc-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="c58cc-125">Frekari upplýsingar er að finna í [Nýjungar eða breytingar í Dynamics 365 for Finance and Operations verkvangi uppfærsla 23 (janúar 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="c58cc-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 

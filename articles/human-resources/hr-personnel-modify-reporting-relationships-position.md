---
title: Breyta skýrslugjafarvenslum fyrir stöðu
description: Þessi verklýsing sýnir hvernig á að breyta í skýrslugerðarsambandi fyrir starfsmann.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4f54a162305a81b65f0657cd572df75a9dcbd38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794446"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="99f84-103">Breyta skýrslugjafarvenslum fyrir stöðu</span><span class="sxs-lookup"><span data-stu-id="99f84-103">Modify reporting relationships for a position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="99f84-104">Þessi verklýsing sýnir hvernig á að breyta í skýrslugerðarsambandi fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="99f84-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="99f84-105">Hægt er að nota í skýrslugerðarsambandi fyrir leiðaraðgerð skjöl gegnum verkflæði.</span><span class="sxs-lookup"><span data-stu-id="99f84-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="99f84-106">Ferlið einnig sýnir hvernig á að úthluta starfsmanns til viðbótar stigveldi.</span><span class="sxs-lookup"><span data-stu-id="99f84-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="99f84-107">Til dæmis er starfsmaður gæti verið hluti af verkhópur með óformleg skýrslugerðarsambandi við yfirmaður verks.</span><span class="sxs-lookup"><span data-stu-id="99f84-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="99f84-108">Hægt er að skilgreina viðbótar skýrslugerðarsamband á stöðu til að nota fyrir mismunandi verk- eða fylkisaðstæður.</span><span class="sxs-lookup"><span data-stu-id="99f84-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="99f84-109">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="99f84-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="99f84-110">Farið í Mannauður > Stöður > Stöður.</span><span class="sxs-lookup"><span data-stu-id="99f84-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="99f84-111">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="99f84-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="99f84-112">Til dæmis að sía eftir Stöðu svæði með gildið '000091'.</span><span class="sxs-lookup"><span data-stu-id="99f84-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="99f84-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="99f84-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="99f84-114">Útvíkka Skýrslurnar í hlutanum stöðu.</span><span class="sxs-lookup"><span data-stu-id="99f84-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="99f84-115">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="99f84-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="99f84-116">Sláið inn eða veldu gildi í reitnum veita skýrslu til.</span><span class="sxs-lookup"><span data-stu-id="99f84-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="99f84-117">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="99f84-117">Click Create.</span></span>
8. <span data-ttu-id="99f84-118">Stækka Vensl hluti.</span><span class="sxs-lookup"><span data-stu-id="99f84-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="99f84-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="99f84-119">Click Add.</span></span>
10. <span data-ttu-id="99f84-120">Veldu gátreitinn vinstra megin í hnitinu.</span><span class="sxs-lookup"><span data-stu-id="99f84-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="99f84-121">Sláið inn eða veldu gildi í reitnum heiti stigveldis.</span><span class="sxs-lookup"><span data-stu-id="99f84-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="99f84-122">Dæmi: Verks</span><span class="sxs-lookup"><span data-stu-id="99f84-122">Example: Project</span></span>  
12. <span data-ttu-id="99f84-123">Færa inn eða velja gildi í svæðis veitir Skýrslum til stöðu .</span><span class="sxs-lookup"><span data-stu-id="99f84-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="99f84-124">Til dæmis 000437.</span><span class="sxs-lookup"><span data-stu-id="99f84-124">Example:  000437</span></span>
13. <span data-ttu-id="99f84-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="99f84-125">Click Save.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
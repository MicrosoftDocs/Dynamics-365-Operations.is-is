--- 
title: "Setja upp skattyfirvöld"
description: "Skattayfirvöld eru einingar sem innheimtur virðisaukaskatt þarf að vera tilkynntur til og greiddur."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f75ee28343161026a73dd889b345d65ecc345884
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="fdc7f-103">Setja upp skattyfirvöld</span><span class="sxs-lookup"><span data-stu-id="fdc7f-103">Set up sales tax authorities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fdc7f-104">Skattayfirvöld eru einingar sem innheimtur virðisaukaskatt þarf að vera tilkynntur til og greiddur.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="fdc7f-105">Þú getur greitt söluskattur til yfirvaldsins beint eða í gegnum lánardrottnalykill sem þú stofnar fyrir virðisaukaskattsyfirvald.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="fdc7f-106">Ef þetta er gert getur fyrirtækið notað vanalegt greiðsluferli til að borga skattayfirvöldum á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="fdc7f-107">Ef skattayfirvöld eru ekki sett upp sem lánardrottinn verður að undirbúa handvirka greiðslu til skattayfirvalda á viðeigandi gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="fdc7f-108">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="fdc7f-109">Fara á Skattur > Óbeinir skattar > Virðisaukaskattur > Virðisaukaskattsyfirvöld.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="fdc7f-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-110">Click New.</span></span>
3. <span data-ttu-id="fdc7f-111">Í reitinn yfirvöld skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="fdc7f-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="fdc7f-113">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fdc7f-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="fdc7f-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fdc7f-116">Velurðu útlit skýrslu fyrir þitt land/svæði, ef er tiltækt.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="fdc7f-117">Ef skýrsluútlit ekki í samræmi við kröfur skattayfirvalda, nota sjálfgefið útlit.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="fdc7f-118">Færið inn gildi í skjámynd Sléttun og slétta svæðin til að tilgreina hvernig heildarupphæð skattur sem greiða á sléttuð.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="fdc7f-119">Hvaða sléttunarmun sem verður bókuð á Lykla fyrir sjálfvirkar færslur sett upp í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="fdc7f-120">Í reitinn sléttun skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="fdc7f-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-121">Click Save.</span></span>



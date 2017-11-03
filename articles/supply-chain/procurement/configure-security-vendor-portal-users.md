---
title: "Öryggi notanda í gátt lánardrottins"
description: "Þessi skrá útskýrir hvernig á að setja upp öryggisbúnað fyrir utanaðkomandi lánardrottna sem nota Gátt Lánardrottins. Upplýsingarnar gildir aðeins um 2016 Febrúar &amp; 2016 Maí útgáfum Dynamics AX."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f79f686720d615da6996f854a9e4cc18f840337f
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="5e84a-104">Öryggi notanda í gátt lánardrottins</span><span class="sxs-lookup"><span data-stu-id="5e84a-104">Vendor portal user security</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5e84a-105">Þessi skrá útskýrir hvernig á að setja upp öryggisbúnað fyrir utanaðkomandi lánardrottna sem nota Gátt Lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="5e84a-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="5e84a-106">Upplýsingarnar gildir aðeins um 2016 Febrúar &amp; 2016 Maí útgáfum Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="5e84a-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="5e84a-107">Virknin gátt Lánardrottins hefur verið skipt út fyrir virknina aukið samstarf lánardrottna í Dynamics 365 for Operations útgáfa 1611.</span><span class="sxs-lookup"><span data-stu-id="5e84a-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="5e84a-108">Nánari upplýsingar um uppsetningu öryggis fyrir samstarf lánardrottna sjá [ Uppsetning og viðhald samstarfs lánardrottna](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="5e84a-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="5e84a-109">Gátt lánardrottins birtir takmarkað safn upplýsinga um innkaupapantanir (POs) til ytri lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="5e84a-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="5e84a-110">Mikilvægt er að þú setjir rétt upp heimildir notanda fyrir gátt lánardrottins í Microsoft Dynamics AX, svo að lánardrottnar hafi ekki óviljandi aðgang að viðbótarupplýsingum í uppsetningu á Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="5e84a-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="5e84a-111">**Mikilvægt:** Ólíkt öðrum notendum ættu ytri lánardrottnar ekki að hafa hlutverkið **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="5e84a-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="5e84a-112">Hlutverkið **SystemUser** veitir aðgang að safni réttinda sem ekki eru hæafar fyrir utanaðkomandi notendur.</span><span class="sxs-lookup"><span data-stu-id="5e84a-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="5e84a-113">Setja upp notanda gáttar lánardrottins</span><span class="sxs-lookup"><span data-stu-id="5e84a-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="5e84a-114">Áður en notendareikningur er stofnaður fyrir einhvern sem mun nota gátt lánardrottins, verður að setja upp lánardrottinn til að heimila samvinnu við gátt lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="5e84a-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="5e84a-115">Notaðu reitinn **Innkaupapöntun samvinnu** á flipanum **Almennt** á síðunni **Lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="5e84a-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="5e84a-116">Ytri lánardrottnar sem nota gátt lánardrottins verða að hafa eftirfarandi uppsetningu:</span><span class="sxs-lookup"><span data-stu-id="5e84a-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="5e84a-117">Notandareikningurinn Microsoft Azure Active Directory (AAD) verður að vera skráður fyrir lánardrottinn á síðunni **Notendur** í Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="5e84a-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="5e84a-118">Lánardrottinn verður að hafa öryggishlutverkið **Lánardrottinn (ytri)** en ekki hlutverkið **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="5e84a-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="5e84a-119">**Ábending:** Hlutverkið **SystemUser** er veitt sjálfkrafa þegar þú stofnar nýjan lykil notanda í Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="5e84a-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="5e84a-120">Þess vegna þarf að fjarlægja það hlutverk og staðfesta viðvörunarboðin sem berast.</span><span class="sxs-lookup"><span data-stu-id="5e84a-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="5e84a-121">Lánardrottinsnotandi ætti ekki að veita heimild til að bæta viðbótarreitum úr töflum innkaupapöntunar við skoðun þeirra á innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="5e84a-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="5e84a-122">Á flipanum **Sérsnið**, á flipanum **Notendur**, skal stilla valkostinn **Yfirlýst sérsnið leyfð** fyrir notandann á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="5e84a-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="5e84a-123">Notandareikningurinn verður að vera tengdur skráðum tengilið.</span><span class="sxs-lookup"><span data-stu-id="5e84a-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="5e84a-124">Á síðunni **Notendur** skal velja tengilið í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="5e84a-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="5e84a-125">Sá sem er valinn ætti að hafa hlutverkið **Tengiliður** fyrir viðkomandi lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="5e84a-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="5e84a-126">Ef sami einstaklingur krefst aðgangs að gátt lánardrottins fyrir marga lánardrottna (kannski fyrir mismunandi lögaðila) verður hver notendareikningur þess einstaklings að vera tengdur sama skráðum tengilið.</span><span class="sxs-lookup"><span data-stu-id="5e84a-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="5e84a-127">Hlutverkið **Lánardrottinn (ytri)** inniheldur alla grunngetu sem þarf til að nota aðgerðirnar sem eru tiltækar í gátt lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="5e84a-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="5e84a-128">Þessi uppsetning hjálpar til við að tryggja að samræmt notendaviðmót sem ytri notandinn sér leggi aðeins áherslu á ætlaðar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="5e84a-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="see-also"></a><span data-ttu-id="5e84a-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5e84a-129">See also</span></span>
--------

[<span data-ttu-id="5e84a-130">Samstarf lánardrottna</span><span class="sxs-lookup"><span data-stu-id="5e84a-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)





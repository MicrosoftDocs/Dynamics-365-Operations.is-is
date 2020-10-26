---
title: Öryggisgreining fyrir verkskráningu
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að greina og stjórna kröfum öryggisheimildar út frá verkskráningu.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 4aecda7e0d604b70dec58a4f5bb2992fe7e0a5e2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982431"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="509cf-103">Öryggisgreining fyrir verkskráningu</span><span class="sxs-lookup"><span data-stu-id="509cf-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="509cf-104">Áður en hafist er handa</span><span class="sxs-lookup"><span data-stu-id="509cf-104">Before you begin</span></span>

<span data-ttu-id="509cf-105">Í þessu efnisatriði er að finna upplýsingar um hvernig á að greina og stjórna kröfum öryggisheimildar út frá verkskráningu.</span><span class="sxs-lookup"><span data-stu-id="509cf-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="509cf-106">Áður en þú klárar skrefin í þessu efnisatriði verður þú að hafa verkskráningu fyrir viðskiptaferlið sem þú vilt greina.</span><span class="sxs-lookup"><span data-stu-id="509cf-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="509cf-107">Upplýsingar um hvernig viðskiptaferli er skráð er að finna í [Tilföng verkskráningar](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="509cf-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="509cf-108">Stjórna öryggi fyrir verkskráningu</span><span class="sxs-lookup"><span data-stu-id="509cf-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="509cf-109">Farðu í **Kerfisstjórnun** > **Öryggi** > **Öryggisgreining fyrir verkskráningu**.</span><span class="sxs-lookup"><span data-stu-id="509cf-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="509cf-110">Opna verkskráningu úr staðsetningu sinni.</span><span class="sxs-lookup"><span data-stu-id="509cf-110">Open the task recording from its location.</span></span> <span data-ttu-id="509cf-111">Veldu **Opna í þessari tölvu** eða **Opna í Lifecycle Services** og veldu **Loka**.</span><span class="sxs-lookup"><span data-stu-id="509cf-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="509cf-112">Þetta opnar síðuna **Upplýsingar um öryggisvalmyndaratriði** þar sem finna má listi yfir öryggishluti sem eru nauðsynlegir fyrir ferlið.</span><span class="sxs-lookup"><span data-stu-id="509cf-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="509cf-113">Valmyndaratriðin **Aðgerð** og **Úttak** eru ekki á listanum.</span><span class="sxs-lookup"><span data-stu-id="509cf-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="509cf-114">Í reitinn **Notandakenni** skal velja notanda.</span><span class="sxs-lookup"><span data-stu-id="509cf-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="509cf-115">Ef notandinn hefur ekki heimild fyrir sum valmyndaratriði mun reiturinn **Vantar heimildir** uppfærast í **Já**.</span><span class="sxs-lookup"><span data-stu-id="509cf-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Upplýsingasíða um öryggisvalmyndaratriði](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="509cf-117">Veljið **Bæta við tilvísun** til að sjá lista yfir öryggishlutina, þar á meðal hlutverk, skyldur og réttindi sem veita heimildina sem vantar.</span><span class="sxs-lookup"><span data-stu-id="509cf-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="509cf-118">Velja öryggishlut af listanum:</span><span class="sxs-lookup"><span data-stu-id="509cf-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="509cf-119">Ef **Hlutverk** er valið skal velja **Bæta hlutverkum við notanda**.</span><span class="sxs-lookup"><span data-stu-id="509cf-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="509cf-120">Þetta mun opna síðuna **Úthluta notendum á hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="509cf-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="509cf-121">Frekari upplýsingar má finna á síðunni [Úthluta notendum á öryggishlutverk](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="509cf-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="509cf-122">Ef **Skylda** er valið skal velja **Bæta skyldu við hlutverk**, velja hlutverkin sem bæta á skyldunni við og velja svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="509cf-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="509cf-123">Ef **Réttindi** eru valin skal velja **Bæta réttindum við skyldur**, velja hlutverk sem bæta á skyldunni við og velja svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="509cf-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>

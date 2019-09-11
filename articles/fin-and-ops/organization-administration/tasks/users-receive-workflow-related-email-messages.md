---
title: Gera notendum kleift að fá tölvupóst sem tengjast verkflæði
description: Hægt er að grunnstilla kerfið til að senda tölvupóst til notenda þegar tilvik verkflæðis sem tengjast eiga sér stað.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916393"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="70072-103">Gera notendum kleift að fá tölvupóst sem tengjast verkflæði</span><span class="sxs-lookup"><span data-stu-id="70072-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70072-104">Hægt er að grunnstilla kerfið til að senda tölvupóst til notenda þegar tilvik verkflæðis sem tengjast eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="70072-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="70072-105">Til dæmis er hægt að senda tölvupóstskilaboð til notenda þegar skjöl eru send þeim til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="70072-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="70072-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="70072-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="70072-107">Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Notendur > Notendur**.</span><span class="sxs-lookup"><span data-stu-id="70072-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="70072-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="70072-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="70072-109">Í **Aðgerðarrúðunni** smellirðu á **Valkostir notanda**.</span><span class="sxs-lookup"><span data-stu-id="70072-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="70072-110">Smelltu á flipann **Verkflæði**. Gakktu úr skugga um að hlutinn **Tilkynningar** sé stækkaður.</span><span class="sxs-lookup"><span data-stu-id="70072-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="70072-111">Í hlutanum **Tilkynningar** er hægt að tilgreina hvernig notandi látinn vita um tilvik sem tengjast verkflæði.</span><span class="sxs-lookup"><span data-stu-id="70072-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="70072-112">Veljið valkost í reitnum **Gerð tilkynningar verkflæðis fyrir línuvöru**.</span><span class="sxs-lookup"><span data-stu-id="70072-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="70072-113">Flokkað - Tilkynningar fyrir línuatriði eru flokkaðar í einn tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="70072-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="70072-114">Stakt - Tölvupóstur eru send fyrir hvern línuatriði.</span><span class="sxs-lookup"><span data-stu-id="70072-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="70072-115">Ef óskað er eftir að notandi fái tilkynningar í biðlaranum velurðu gátreitinn **Senda tilkynningar í tölvupósti**.</span><span class="sxs-lookup"><span data-stu-id="70072-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="70072-116">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="70072-116">Click **Save**.</span></span>
7. <span data-ttu-id="70072-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="70072-117">Close the page.</span></span>


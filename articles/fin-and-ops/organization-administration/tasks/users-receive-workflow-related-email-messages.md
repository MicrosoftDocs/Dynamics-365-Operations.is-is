--- 
title: "Skilgreina kerfið til að senda tölvupósta tengda verkflæði til notenda"
description: "Hægt er að grunnstilla kerfið til að senda tölvupóst til notenda þegar tilvik verkflæðis sem tengjast eiga sér stað."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a><span data-ttu-id="a39d4-103">Skilgreina kerfið til að senda tölvupósta tengda verkflæði til notenda</span><span class="sxs-lookup"><span data-stu-id="a39d4-103">Configure the system to send workflow-related email to users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a39d4-104">Hægt er að grunnstilla kerfið til að senda tölvupóst til notenda þegar tilvik verkflæðis sem tengjast eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="a39d4-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="a39d4-105">Til dæmis er hægt að senda tölvupóstskilaboð til notenda þegar skjöl eru send þeim til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="a39d4-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="a39d4-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="a39d4-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a39d4-107">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="a39d4-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="a39d4-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a39d4-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a39d4-109">Smelltu á Notandastillingar</span><span class="sxs-lookup"><span data-stu-id="a39d4-109">Click User options.</span></span>
4. <span data-ttu-id="a39d4-110">Smellt er á flipann Verkflæði.</span><span class="sxs-lookup"><span data-stu-id="a39d4-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="a39d4-111">Gakktu úr skugga um að tilkynningahlutinn sé víkkaður út.</span><span class="sxs-lookup"><span data-stu-id="a39d4-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="a39d4-112">Í tilkynningahlutanum er hægt að tilgreina hvernig notandi látinn vita um tilvik sem tengjast verkflæði.</span><span class="sxs-lookup"><span data-stu-id="a39d4-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="a39d4-113">Veljið valkost í svæðinu Gerð tilkynningar verkflæðis fyrir línuvöru.</span><span class="sxs-lookup"><span data-stu-id="a39d4-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="a39d4-114">Flokkað - Tilkynningar fyrir línuatriði eru flokkaðar í einn tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="a39d4-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="a39d4-115">Stakt - Tölvupóstur eru send fyrir hvern línuatriði.</span><span class="sxs-lookup"><span data-stu-id="a39d4-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="a39d4-116">Ef óskað er eftir að notandi fái tilkynningar í biðlaranum velurðu gátreitinn Senda tilkynningar í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="a39d4-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="a39d4-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a39d4-117">Click Save.</span></span>
7. <span data-ttu-id="a39d4-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a39d4-118">Close the page.</span></span>



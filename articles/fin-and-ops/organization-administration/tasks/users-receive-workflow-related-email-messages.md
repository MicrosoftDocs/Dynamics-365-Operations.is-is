--- 
title: "Gera notendum kleift að fá tölvupóst sem tengjast verkflæði"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5458625d345412a0022eb9acaa4e5bd23b465948
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="1468f-103">Gera notendum kleift að fá tölvupóst sem tengjast verkflæði</span><span class="sxs-lookup"><span data-stu-id="1468f-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1468f-104">Hægt er að grunnstilla kerfið til að senda tölvupóst til notenda þegar tilvik verkflæðis sem tengjast eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="1468f-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="1468f-105">Til dæmis er hægt að senda tölvupóstskilaboð til notenda þegar skjöl eru send þeim til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="1468f-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="1468f-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="1468f-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="1468f-107">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="1468f-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="1468f-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1468f-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1468f-109">Smelltu á Notandastillingar</span><span class="sxs-lookup"><span data-stu-id="1468f-109">Click User options.</span></span>
4. <span data-ttu-id="1468f-110">Smellt er á flipann Verkflæði.</span><span class="sxs-lookup"><span data-stu-id="1468f-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="1468f-111">Gakktu úr skugga um að tilkynningahlutinn sé víkkaður út.</span><span class="sxs-lookup"><span data-stu-id="1468f-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="1468f-112">Í tilkynningahlutanum er hægt að tilgreina hvernig notandi látinn vita um tilvik sem tengjast verkflæði.</span><span class="sxs-lookup"><span data-stu-id="1468f-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="1468f-113">Veljið valkost í svæðinu Gerð tilkynningar verkflæðis fyrir línuvöru.</span><span class="sxs-lookup"><span data-stu-id="1468f-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="1468f-114">Flokkað - Tilkynningar fyrir línuatriði eru flokkaðar í einn tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="1468f-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="1468f-115">Stakt - Tölvupóstur eru send fyrir hvern línuatriði.</span><span class="sxs-lookup"><span data-stu-id="1468f-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="1468f-116">Ef óskað er eftir að notandi fái tilkynningar í biðlaranum velurðu gátreitinn Senda tilkynningar í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="1468f-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="1468f-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="1468f-117">Click Save.</span></span>
7. <span data-ttu-id="1468f-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1468f-118">Close the page.</span></span>



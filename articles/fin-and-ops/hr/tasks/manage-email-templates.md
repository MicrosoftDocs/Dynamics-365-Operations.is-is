---
title: Stjórna sniðmáti fyrir tölvupóst
description: Hægt er að flytja upplýsingar úr gagnagrunninum fyrirtækisins í bókamerki í nýju skjali og nota hana sem sniðmát sem auðvelda að eiga samskipti hagkvæman hátt með umsækjendur og umsækjendur.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4667d0506c5ae6bea87b982c7feebab8963797a6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1508034"
---
# <a name="manage-email-templates"></a><span data-ttu-id="092c7-103">Stjórna sniðmáti fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="092c7-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="092c7-104">Hægt er að flytja upplýsingar úr gagnagrunninum fyrirtækisins í bókamerki í nýju skjali og nota hana sem sniðmát sem auðvelda að eiga samskipti hagkvæman hátt með umsækjendur og umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="092c7-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="092c7-105">Til að gera þetta stofnarðu sniðmát sem inniheldur staðlaðan texta og einhver bókamerki þar sem kerfisgögn ætti að setja inn.</span><span class="sxs-lookup"><span data-stu-id="092c7-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="092c7-106">Til dæmis er hægt að setja inn aðsetur og tengslaupplýsingar fyrir umsækjanda í Microsoft Word-skjal sem hægt er að nota samskiptum við þann umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="092c7-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="092c7-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="092c7-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="092c7-108">Veljið hvaða bókmerki til að nota í sniðmát fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="092c7-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="092c7-109">Fara á umsóknabókamerki</span><span class="sxs-lookup"><span data-stu-id="092c7-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="092c7-110">Í listanum skal finna og velja þá samskiptaaðgerð sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="092c7-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="092c7-111">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="092c7-111">Click Edit.</span></span>
4. <span data-ttu-id="092c7-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="092c7-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="092c7-113">Veljið svæðin sem á þú myndir vilja nota í sniðmát fyrir tölvupóst fyrir valda Samskiptaaðgerð og flytja þær í svæði Bókarmerki.</span><span class="sxs-lookup"><span data-stu-id="092c7-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="092c7-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="092c7-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="092c7-115">Stofna tölvupóstssniðmát</span><span class="sxs-lookup"><span data-stu-id="092c7-115">Create an email template</span></span>
1. <span data-ttu-id="092c7-116">Farið í Mannauður > Ráðningar > Samskipti > Sniðmát tölvupósts fyrir umsóknir.</span><span class="sxs-lookup"><span data-stu-id="092c7-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="092c7-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="092c7-117">Click New.</span></span>
3. <span data-ttu-id="092c7-118">Í svæðinu Samskiptaaðgerð , veljið 'Viðtal'.</span><span class="sxs-lookup"><span data-stu-id="092c7-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="092c7-119">Veljið samskiptaaðgerð sem inniheldur bókmerki til að nota fyrir þessa gerð samskipta tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="092c7-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="092c7-120">Færa inn gildi í sniðmátssvæði tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="092c7-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="092c7-121">Í reitinn Efni skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="092c7-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="092c7-122">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="092c7-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="092c7-123">Í listanum skal finna og velja þá bókamerki sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="092c7-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="092c7-124">Halda áfram að því að skrifa tölvupósti og settu inn bókamerkið í svæði þar sem þú vilt.</span><span class="sxs-lookup"><span data-stu-id="092c7-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="092c7-125">Halda áfram að því að skrifa tölvupósti og settu inn bókamerkið í svæði þar sem þú vilt.</span><span class="sxs-lookup"><span data-stu-id="092c7-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="092c7-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="092c7-126">Click Save.</span></span>


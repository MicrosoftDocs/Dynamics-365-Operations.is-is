---
title: Haga sniðmáti fyrir tölvupóst
description: Í þessu efnisatriði er útskýrt hvernig á að stjórna tölvupóstsniðmátum.
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 3ecfa720dfa9b3ed6ee15ec68498d2a46612a9ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178381"
---
# <a name="manage-email-templates"></a><span data-ttu-id="15f86-103">Haga sniðmáti fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="15f86-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15f86-104">Hægt er að flytja upplýsingar úr gagnagrunninum fyrirtækisins í bókamerki í nýju skjali og nota hana sem sniðmát sem auðvelda að eiga samskipti hagkvæman hátt með umsækjendur og umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="15f86-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="15f86-105">Til að gera þetta stofnarðu sniðmát sem inniheldur staðlaðan texta og einhver bókamerki þar sem kerfisgögn ætti að setja inn.</span><span class="sxs-lookup"><span data-stu-id="15f86-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="15f86-106">Til dæmis er hægt að setja inn aðsetur og tengslaupplýsingar fyrir umsækjanda í Microsoft Word-skjal sem hægt er að nota samskiptum við þann umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="15f86-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="15f86-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="15f86-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="15f86-108">Veljið hvaða bókmerki til að nota í sniðmát fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="15f86-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="15f86-109">Farðu í **Einingar > Mannauður > Ráðning > Samskipti > Bókamerki umsókna**.</span><span class="sxs-lookup"><span data-stu-id="15f86-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="15f86-110">Í listanum skal finna og velja þá samskiptaaðgerð sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="15f86-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="15f86-111">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="15f86-111">Select **Edit**.</span></span>
4. <span data-ttu-id="15f86-112">Veljið svæðin sem á þú myndir vilja nota í sniðmát fyrir tölvupóst fyrir valda Samskiptaaðgerð og flytja þær í svæði Bókarmerki.</span><span class="sxs-lookup"><span data-stu-id="15f86-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="15f86-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="15f86-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="15f86-114">Stofna sniðmát fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="15f86-114">Create an email template</span></span>
1. <span data-ttu-id="15f86-115">Farðu í **Einingar > Mannauður > Ráðning > Samskipti > Tölvupóstsniðmát umsókna**.</span><span class="sxs-lookup"><span data-stu-id="15f86-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="15f86-116">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="15f86-116">Select **New**.</span></span>
3. <span data-ttu-id="15f86-117">Í reitnum **Samskiptaaðgerð** skaltu velja **Viðtal**.</span><span class="sxs-lookup"><span data-stu-id="15f86-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="15f86-118">Veljið samskiptaaðgerð sem inniheldur bókmerki til að nota fyrir þessa gerð samskipta tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="15f86-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="15f86-119">Í reitnum **Tölvupóstsniðmát** skaltu rita gildi.</span><span class="sxs-lookup"><span data-stu-id="15f86-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="15f86-120">Í reitinn **Efni** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="15f86-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="15f86-121">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="15f86-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="15f86-122">Í listanum skal finna og velja þá bókamerki sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="15f86-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="15f86-123">Halda áfram að því að skrifa tölvupósti og settu inn bókamerkið í svæði þar sem þú vilt.</span><span class="sxs-lookup"><span data-stu-id="15f86-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="15f86-124">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="15f86-124">Select **Save**.</span></span>

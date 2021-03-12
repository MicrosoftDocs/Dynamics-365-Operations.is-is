---
title: Setja upp staðgreiðsluskatt
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp staðgreiðsluskatt.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45ae7d6bb04dbf06b9b05d9f5610895fced650b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994441"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="b4bdc-103">Setja upp staðgreiðsluskatt</span><span class="sxs-lookup"><span data-stu-id="b4bdc-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4bdc-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp staðgreiðsluskatt.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="b4bdc-105">*Staðgreiðsluskattur* er skattur á lánardrottna sem ekki stofnar VSK-færslur.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="b4bdc-106">Staðgreiðsluskattur sem er reiknaður á greiðslur lánardrottins er skuld.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="b4bdc-107">Þess vegna eru bara efnahagslyklar eða afsláttarlyklar gildir við bókun á staðgreiðsluskatti.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="b4bdc-108">Þessi leiðarvísi fyrir verk sýnir hvernig á að setja upp staðgreiðsluskatt.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="b4bdc-109">Farðu í **Skoðunarrúða > Kerfiseiningar > Skattur > Óbeinir skattar > Staðgreiðsluskattur- > Kóðar staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="b4bdc-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-110">Select **New**.</span></span>
3. <span data-ttu-id="b4bdc-111">Í reitnum **Staðgreiðsluskattskóði** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="b4bdc-112">Í svæðið **heiti staðgreiðsluskatts**, færið inn heiti staðgreiðsluskattskóðann.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="b4bdc-113">Í **Aðallykill** svæðinu, veljið aðallykil fyrir bókun staðgreiðsluskattskuldarinnar.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="b4bdc-114">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-114">Select **Save**.</span></span>
7. <span data-ttu-id="b4bdc-115">Veldu **Gildi** og merktu þá færslu sem óskað er eftir í listanum.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="b4bdc-116">Í svæðinu **Gildi** færa inn prósentu sem er notuð til útreiknings á staðgreiðsluskattinum.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="b4bdc-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-117">Select **Save**.</span></span>
10. <span data-ttu-id="b4bdc-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-118">Close the page.</span></span>
11. <span data-ttu-id="b4bdc-119">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-119">Select **Save**.</span></span>
12. <span data-ttu-id="b4bdc-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-120">Close the page.</span></span>
13. <span data-ttu-id="b4bdc-121">Farðu í **Skoðunarrúða > Kerfiseiningar > Skattur > Óbeinir skattar > Staðgreiðsluskattur- > Hópar staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="b4bdc-122">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-122">Select **New**.</span></span>
15. <span data-ttu-id="b4bdc-123">Færa inn kenni staðgreiðsluskattsflokks í reitinn **Hópur staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="b4bdc-124">Færið inn heiti staðgreiðsluskattflokkur í svæðinu **Lýsingu**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="b4bdc-125">Veljið **staðgreiðsluskattskóði** í svæðinu fyrir staðgreiðsluskattskóði.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="b4bdc-126">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-126">Select **Save**.</span></span>
19. <span data-ttu-id="b4bdc-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-127">Close the page.</span></span>


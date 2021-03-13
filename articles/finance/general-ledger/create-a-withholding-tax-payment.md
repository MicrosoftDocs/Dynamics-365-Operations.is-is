---
title: Stofna greiðslu staðgreiðsluskatts
description: Vinnslan greiðsla staðgreiðsluskatts jafnar stöðu staðgreiðsluskatt af viðskiptaskuldum á staðgreiðsluskattslyklum og mótfærir þær á jöfnunarlykil staðgreiðsluskatts á tilteknu tímabili. Þetta efnisatriði telur upp skrefin fyrir uppsetningu staðgreiðsluskatts.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: e522711340b663bd849825b3d4dd2b7e78e4737c
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060752"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="7243f-104">Stofna greiðslu staðgreiðsluskatts</span><span class="sxs-lookup"><span data-stu-id="7243f-104">Create a withholding tax payment</span></span>

<span data-ttu-id="7243f-105">Vinnslan greiðsla staðgreiðsluskatts jafnar stöðu staðgreiðsluskatt af viðskiptaskuldum á staðgreiðsluskattslyklum og mótfærir þær á jöfnunarlykil staðgreiðsluskatts á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="7243f-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="7243f-106">Þetta efnisatriði telur upp skrefin fyrir uppsetningu staðgreiðsluskatts.</span><span class="sxs-lookup"><span data-stu-id="7243f-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="7243f-107">Ekki er tekið tillit til mótlykils staðgreiðsluskatts (af viðskiptakröfum) þegar greiðsla staðgreiðsluskatts er reiknuð.</span><span class="sxs-lookup"><span data-stu-id="7243f-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="7243f-108">Opnaðu **Yfirlitssvæði > Einingar > Skattur > Skýrslur > Staðgreiðsluskattur > Greiðsla staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="7243f-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="7243f-109">Í reitnum **jöfnunartímabil** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7243f-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7243f-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7243f-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7243f-111">Í reitnum **Frá dags.** færirði inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="7243f-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="7243f-112">Færa inn dagsetningu í reitinn **Færsludagsetning**.</span><span class="sxs-lookup"><span data-stu-id="7243f-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="7243f-113">Velja **uppfærslu** til að bóka fylgiseðil staðgreiðsluskatts á jöfnunarlykil staðgreiðsluskatts.</span><span class="sxs-lookup"><span data-stu-id="7243f-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="7243f-114">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="7243f-114">Click **OK**.</span></span>

![Færibreytur fyrir greiðslu staðgreiðsluskatts](media/withholding-tax-payment.png)

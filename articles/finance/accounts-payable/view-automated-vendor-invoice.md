---
title: Skoða niðurstöður sjálfvirkni reiknings lánardrottins (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að skoða stöðu reikninga lánardrottna sem eru í sjálfvirka verkflæðisferlinu.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 872ec404da0cce41c4ea0f882a3fa8af56316ce3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837226"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="b3440-103">Skoða niðurstöður sjálfvirkni reiknings lánardrottins</span><span class="sxs-lookup"><span data-stu-id="b3440-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3440-104">Þetta efnisatriði útskýrir hvernig á að skoða stöðu reikninga lánardrottna sem eru í sjálfvirka verkflæðisferlinu.</span><span class="sxs-lookup"><span data-stu-id="b3440-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="b3440-105">Upplýsingum um sjálfvirkniferilinn er haldið við fyrir hvern innfluttan lánardrottnareikning.</span><span class="sxs-lookup"><span data-stu-id="b3440-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="b3440-106">Það fer eftir viðskiptaferlunum sem voru gerðir sjálfvirkir, hvað síðan **Reikningar frá lánardrottni í bið** sýnir í gildunum **Staða sjálfvirkrar jöfnunar innhreyfingar** og **Staða sjálfvirkrar innsendingar í verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="b3440-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="b3440-107">Hægt er að skoða upplýsingarnar og gera áætlun um að einbeita sér að reikningunum sem tókust ekki í sjálfvirku skrefi.</span><span class="sxs-lookup"><span data-stu-id="b3440-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="b3440-108">Eftir að vandamálið hefur verið lagað er hægt að halda áfram með sjálfvirka ferlið fyrir innfluttan reikning.</span><span class="sxs-lookup"><span data-stu-id="b3440-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="b3440-109">Áður en hægt er að breyta reikningi sem hefur verið sendur inn, verður að gera hlé á sjálfvirku vinnslunni.</span><span class="sxs-lookup"><span data-stu-id="b3440-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="b3440-110">Ef gera verður hlé á sjálfvirkri innsendingu í verkflæði skal stilla reitinn **Hafa með í sjálfvirkri vinnslu** á **Nei** á síðunni **Reikningar frá lánardrottni**.</span><span class="sxs-lookup"><span data-stu-id="b3440-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="b3440-111">Sjálfvirkni keyrir þá ekki fyrr en reiturinn **Hafa með í sjálfvirkri vinnslu** er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="b3440-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="b3440-112">Hægt er að gera hlé á reikningi frá frekari sjálfvirkni ef hann er ekki enn í verkflæðiskerfinu og er ekki notaður af sjálfvirka ferlinu.</span><span class="sxs-lookup"><span data-stu-id="b3440-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="b3440-113">Ef innfluttur reikningur er sendur í verkflæðisferlið er hægt að skoða gildið **Staða sjálfvirkni** á síðunni **Reikningar frá lánardrottni**.</span><span class="sxs-lookup"><span data-stu-id="b3440-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="b3440-114">Eftirfarandi stöður eru raktar:</span><span class="sxs-lookup"><span data-stu-id="b3440-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="b3440-115">**Tekið með** – Sjálfvirku ferlin sem eru skilgreind á síðunni **Færibreytur viðskiptaskulda** keyra á réttan hátt en þeim er enn ekki lokið.</span><span class="sxs-lookup"><span data-stu-id="b3440-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="b3440-116">**Gert hlé** – Sjálfvirku ferlin sem eru skilgreind á síðunni **Færibreytur viðskiptaskulda** hafa verið keyrð, en að minnsta kosti eitt skref í ferlinu tókst ekki.</span><span class="sxs-lookup"><span data-stu-id="b3440-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="b3440-117">Staðan **Gert hlé** er einnig notuð ef reiturinn **Hafa með í sjálfvirkri vinnslu** er stilltur á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="b3440-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="b3440-118">Hægt er að skoða bilanirnar með því að velja **Skoða nýjustu niðurstöður**.</span><span class="sxs-lookup"><span data-stu-id="b3440-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="b3440-119">**Í verkflæði** - Innfluttur reikningur hefur verið sendur í verkflæðiskerfið, annaðhvort af sjálfvirkri innsendingu í verkflæðisferli eða handvirkt.</span><span class="sxs-lookup"><span data-stu-id="b3440-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="b3440-120">**Verkflæði lokið** – Verkflæðisferlinu hefur verið lokið fyrir innfluttan reikning.</span><span class="sxs-lookup"><span data-stu-id="b3440-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
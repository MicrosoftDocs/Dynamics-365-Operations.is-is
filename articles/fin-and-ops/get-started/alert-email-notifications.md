---
title: Viðvörunartilkynning biðlara með tölvupósti
description: Þetta efnisatriði veitir upplýsingar um hvernig á að setja upp reglur sem senda tilkynningar í tölvupósti þegar fyrirfram skilgreindir viðburðir eiga sér stað.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2019
ms.locfileid: "373784"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="d6409-103">Viðvörunartilkynning biðlara með tölvupósti</span><span class="sxs-lookup"><span data-stu-id="d6409-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d6409-104">Í Microsoft Dynamics 365 for Finance and Operations er hægt að skilgreina sérsniðar viðvörunarreglur sem fylgjast með síuðum yfirlitum á gögnum og senda sjálfkrafa tilkynningar í tölvupósti þegar fyrirfram skilgreindir viðburðir gerast.</span><span class="sxs-lookup"><span data-stu-id="d6409-104">In Microsoft Dynamics 365 for Finance and Operations, you can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="d6409-105">Möguleikinn til að senda tilkynningar í tölvupósti er tiltækur fyrir allar studdar gerðir viðvörunar og einnig er hægt að kveikja á honum fyrir núverandi viðvörunarreglur.</span><span class="sxs-lookup"><span data-stu-id="d6409-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="d6409-106">Hægt er að nota innbyggðar stýringar til að búa til viðvörunarreglur sem fylgjast með síuðum yfirlitum á runuvinnslum kerfis.</span><span class="sxs-lookup"><span data-stu-id="d6409-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="d6409-107">Með því að fylgjast með svæðinu **Staða** er einnig hægt að skilgreina viðvörunarreglur sem senda tölvupóst þegar runuvinnsla mistekst.</span><span class="sxs-lookup"><span data-stu-id="d6409-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="d6409-108">Eftir að þessar viðvörunarreglur eru búnar til þarf ekki lengur að athuga skýrslur út af breytingum á viðskiptagögnum.</span><span class="sxs-lookup"><span data-stu-id="d6409-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="d6409-109">Í staðinn er hægt að láta snjallþjónustu breytingagreininga Finance and Operations fylgjast með.</span><span class="sxs-lookup"><span data-stu-id="d6409-109">Instead, you can let the Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="d6409-110">Viðvaranir biðlara eru háðar undirkerfi tölvupósts sem er veitt í gegnum samþættingu við Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d6409-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="d6409-111">Við mælum með því að þú notir veituna fyrir SMTP-samskiptaregluna, þannig að dreifing á tölvupósti þarf ekki að treysta á staðbundinn póstþjón.</span><span class="sxs-lookup"><span data-stu-id="d6409-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="d6409-112">Til að senda tilkynningar með tölvupósti verða viðskiptavinir að skilgreina samþættar tölvupóstsþjónustur.</span><span class="sxs-lookup"><span data-stu-id="d6409-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="d6409-113">Tilkynningar í tölvupósti eru sendar viðtakendum af hálfu eigenda tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="d6409-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="d6409-114">Frekari upplýsingar um hvernig á að skilgrein tölvupóst í Finance and Operations er að finna í [Stilling og sending tölvupósts](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="d6409-114">For more information about how to configure email in Finance and Operations, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="d6409-115">Eftirfarandi mynd sýnir svargluggann **Stofna viðvörunarreglu** sem er nú með valkostinn **Senda tölvupóst**.</span><span class="sxs-lookup"><span data-stu-id="d6409-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="d6409-116">[![Stofna svarglugga viðvörunarreglu þar sem valkosturinn „Senda tölvupóst“ er stilltur á Já](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="d6409-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="d6409-117">Þegar valkosturinn **Senda tölvupóst** er stilltur á **Já** verður haldið áfram að senda viðvörunartilkynningar úr Aðgerðamiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="d6409-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="d6409-118">Sniðmát fyrir viðvörunartilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="d6409-118">Alert notification email templates</span></span>

<span data-ttu-id="d6409-119">Þjónustan sendir tilkynningar í tölvupósti með því að nota fyrirfram skilgreind sniðmát tölvupósts sem afhenda grunnupplýsingar um viðvörunartilkynninguna.</span><span class="sxs-lookup"><span data-stu-id="d6409-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span> <span data-ttu-id="d6409-120">Þessar upplýsingar innihalda beinan tengil á síðuna þar sem viðvörunarreglan var skilgreind.</span><span class="sxs-lookup"><span data-stu-id="d6409-120">These details include a direct link to the page where the alert rule was defined.</span></span>

<span data-ttu-id="d6409-121">Eftirfarandi mynd sýnir uppbyggingu á viðvörunartilkynningum þegar þær eru mótteknar með tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="d6409-121">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="d6409-122">[![Viðvörunartilkynningar sem byggjast á sniðmáti fyrir stofnun á færslu, breytingar á svæði og eyðingu á sniðmáti](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="d6409-122">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>

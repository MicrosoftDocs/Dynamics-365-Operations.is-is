---
title: Setja upp samþykktarverkflæði leigusamnings
description: Efnið útskýrir hvernig á að setja upp samþykktarverkflæði sem verður keyrt þegar nýr leigusamningur er stofnaður.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4d5416b3b24d5fbb3ac46afb3c672212d41d42d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827555"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="adc11-103">Setja upp samþykktarverkflæði leigusamnings</span><span class="sxs-lookup"><span data-stu-id="adc11-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adc11-104">Efnið útskýrir hvernig á að setja upp samþykktarverkflæði sem verður keyrt þegar nýr leigusamningur er stofnaður.</span><span class="sxs-lookup"><span data-stu-id="adc11-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="adc11-105">Upplýsingar um það hvernig á að nota verkflæðið er að finna í [nota samþykktarverkflæði leigusamninga](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="adc11-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="adc11-106">Opnið **Eignarleiga \> Uppsetning \> Verkflæði leigusamnings**.</span><span class="sxs-lookup"><span data-stu-id="adc11-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="adc11-107">Á síðunni **Verkflæði leigusamnings** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="adc11-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="adc11-108">Í svarglugganum sem birtist, undir **Verkflæðisgerð**, skal velja tengilinn **Verkflæði leigusamnings**.</span><span class="sxs-lookup"><span data-stu-id="adc11-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="adc11-109">Forritið opnast.</span><span class="sxs-lookup"><span data-stu-id="adc11-109">The application is opened.</span></span> <span data-ttu-id="adc11-110">Eftir að það er keyrt skal skrá sig inn á Azure Active Directory (Azure AD) til að komast í verkflæðiforritið.</span><span class="sxs-lookup"><span data-stu-id="adc11-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="adc11-111">Dragið **Verkflæðissamþykki leigusamnings** eininguna inn á verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="adc11-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="adc11-112">Tengið einn hnút frá **Ræsa** í **Verkflæðissamþykki leigusamnings**.</span><span class="sxs-lookup"><span data-stu-id="adc11-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="adc11-113">Tengið svo **Verkflæðissamþykki leigusamnings** í **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="adc11-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="adc11-114">Tvísmellið á **Verkflæðissamþykki leigusamnings**.</span><span class="sxs-lookup"><span data-stu-id="adc11-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="adc11-115">Veljið **Eiginleikar** og færi svo inn heiti fyrir verkflæðið undir **Grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="adc11-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="adc11-116">Á þessari síðu er einnig hægt að setja upp fleiri færibreytur fyrir verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="adc11-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="adc11-117">Ef kveikt hefur verið á **sjálfvirkum aðgerðum** mun kerfið sjálfkrafa framkvæma tiltekna aðgerð.</span><span class="sxs-lookup"><span data-stu-id="adc11-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="adc11-118">Hægt er að senda tilkynningar ef þær eru tilgreindar á flipanum **Tilkynningar**. Á flipanum **Ítarlegar stillingar** er hægt að tilgreina endanlegan samþykktaraðila, stilla tímamörk og tilnefna tilteknar aðgerðir sem þarf að ljúka.</span><span class="sxs-lookup"><span data-stu-id="adc11-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="adc11-119">Þegar búið er að stilla færibreytur verkflæðis skal velja **Loka**.</span><span class="sxs-lookup"><span data-stu-id="adc11-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="adc11-120">Veljið **Skref 1** og veljið svo **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="adc11-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="adc11-121">Undir **Grunnstillingar** skal færa inn heiti fyrir skrefið, stofna efnislínu fyrir samþykkið og tilgreina leiðbeiningar fyrir samþykkið.</span><span class="sxs-lookup"><span data-stu-id="adc11-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="adc11-122">Á síðunni **Úthlutun** er valin úthlutunargerð.</span><span class="sxs-lookup"><span data-stu-id="adc11-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="adc11-123">Til að úthluta tilteknum notendum á samþykktina skal velja **Notandi**, velja notendur sem samþykkja leigusamninga og velja svo **Loka**.</span><span class="sxs-lookup"><span data-stu-id="adc11-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="adc11-124">Veljið **Vista og loka** til að stofna verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="adc11-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="adc11-125">Síðan, þegar beðið er um það, skal velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="adc11-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="adc11-126">Á síðunni **Stofna verkflæði** skal velja **Loka**.</span><span class="sxs-lookup"><span data-stu-id="adc11-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="adc11-127">Veldu nýja verkflæðið og veldu því næst **Útgáfur**.</span><span class="sxs-lookup"><span data-stu-id="adc11-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="adc11-128">Síðan skal velja **Virkja** til að tryggja að verkflæðið sé virkt.</span><span class="sxs-lookup"><span data-stu-id="adc11-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="adc11-129">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="adc11-129">Select **Close**.</span></span> <span data-ttu-id="adc11-130">Nýja virka útgáfan birtist.</span><span class="sxs-lookup"><span data-stu-id="adc11-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
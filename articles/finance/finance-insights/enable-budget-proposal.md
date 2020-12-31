---
title: Virkja drög að fjárhagsáætlun (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að virkja eiginleikann Drög að fjárhagsáætlun í Fjármálainnsýn.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d8443c4e3e6f3d3a90acedc7c05b2846d6b68369
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646206"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="6b1c6-103">Virkja drög að fjárhagsáætlun (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="6b1c6-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6b1c6-104">Þetta efnisatriði útskýrir hvernig á að virkja eiginleikann Drög að fjárhagsáætlun í Fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="6b1c6-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="6b1c6-105">Notaðu upplýsingar úr umhverfissíðunni í Microsoft Dynamics Lifecycle Services (LCS) til að tengjast aðaltilviki Azure SQL fyrir þetta umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6b1c6-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="6b1c6-106">Keyrið eftirfarandi Transact-SQL (T-SQL) skipun til að kveikja á flugi fyrir sandkassaumhverfa.</span><span class="sxs-lookup"><span data-stu-id="6b1c6-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="6b1c6-107">(Hugsanlega þarf að kveikja á aðgangi að IP-tölu notanda í LCS áður en hægt er að fjartengjast við AOS \[Application Object Server\].)</span><span class="sxs-lookup"><span data-stu-id="6b1c6-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="6b1c6-108">Ef verið er að setja upp Microsoft Dynamics 365 Finance sem Service Fabric-uppsetningu er hægt að sleppa þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="6b1c6-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="6b1c6-109">Fjármögnunarteymið ætti nú þegar að hafa kveikt á forútgáfunni fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="6b1c6-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="6b1c6-110">Ef eiginleikinn er ekki sýnilegur í vinnusvæðinu **Eiginleikastjórnun** eða ef vandamál kemur upp þegar reynt er að kveikja á honum skal senda tölvupóst á [Teymi forskoðinar forritsins Fjárhagsinnsýnar](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6b1c6-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="6b1c6-111">Opnið vinnusvæðið **Eiginleikastjórnun** og fylgið eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="6b1c6-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="6b1c6-112">Veldu **Leita að uppfærslum**.</span><span class="sxs-lookup"><span data-stu-id="6b1c6-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="6b1c6-113">Leitið að **Drög að fjárhagsáætlun** og kveikið á þessum eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6b1c6-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="6b1c6-114">Farið í **Fjárhagsáætlanir \> Uppsetning \> grunnáætlanagerð \> Drög að fjárhagsáætlun (forskoðun)** og veljið **Virkja eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="6b1c6-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="6b1c6-115">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="6b1c6-115">Privacy notice</span></span>
<span data-ttu-id="6b1c6-116">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="6b1c6-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>

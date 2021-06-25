---
title: Virkja drög að fjárhagsáætlun (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að virkja eiginleikann Drög að fjárhagsáætlun í Fjármálainnsýn.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222535"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="8cb3d-103">Virkja drög að fjárhagsáætlun (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="8cb3d-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8cb3d-104">Þetta efnisatriði útskýrir hvernig á að virkja eiginleikann Drög að fjárhagsáætlun í Fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="8cb3d-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="8cb3d-105">Notaðu upplýsingar úr umhverfissíðunni í Microsoft Dynamics Lifecycle Services (LCS) til að tengjast aðaltilviki Azure SQL fyrir þetta umhverfi.</span><span class="sxs-lookup"><span data-stu-id="8cb3d-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="8cb3d-106">Keyrið eftirfarandi Transact-SQL (T-SQL) skipun til að kveikja á flugi fyrir sandkassaumhverfa.</span><span class="sxs-lookup"><span data-stu-id="8cb3d-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="8cb3d-107">(Hugsanlega þarf að kveikja á aðgangi að IP-tölu notanda í LCS áður en hægt er að fjartengjast við AOS \[Application Object Server\].)</span><span class="sxs-lookup"><span data-stu-id="8cb3d-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="8cb3d-108">Sleppið þessu skrefi ef notuð er útgáfa 10.0.20 eða nýrri eða ef notuð er uppsetning Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8cb3d-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="8cb3d-109">Fjármögnunarteymið ætti nú þegar að hafa kveikt á forútgáfunni fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="8cb3d-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="8cb3d-110">Ef þú sérð ekki eiginleikann á vinnusvæðinu **Eiginleikastjórnun** eða ef vandamál koma upp þegar reynt er að kveikja á honum skal hafa samband við <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="8cb3d-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="8cb3d-111">Opnið vinnusvæðið **Eiginleikastjórnun** og fylgið eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="8cb3d-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="8cb3d-112">Veldu **Leita að uppfærslum**.</span><span class="sxs-lookup"><span data-stu-id="8cb3d-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="8cb3d-113">Leitið að **Drög að fjárhagsáætlun** og kveikið á þessum eiginleika.</span><span class="sxs-lookup"><span data-stu-id="8cb3d-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="8cb3d-114">Farið í **Fjárhagsáætlanir \> Uppsetning \> grunnáætlanagerð \> Drög að fjárhagsáætlun (forskoðun)** og veljið **Virkja eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="8cb3d-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

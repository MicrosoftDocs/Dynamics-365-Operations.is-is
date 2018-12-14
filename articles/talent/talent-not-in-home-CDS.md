---
title: "Talent birtist ekki á meðal forrita Microsoft Dynamics 365 (CDS1.0)"
description: "Þetta efnisatriði útskýrir hvað á að gera ef viðskiptamaður sér ekki forritið Microsoft Dynamics 365 for Talent á meðal forrita Microsoft Dynamics 365."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="5aa4f-103">Talent birtist ekki á meðal forrita Microsoft Dynamics 365 (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="5aa4f-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5aa4f-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="5aa4f-104">**Issue**</span></span>

<span data-ttu-id="5aa4f-105">Viðskiptamaður sér ekki forritið Microsoft Dynamics 365 for Talent á meðal forrita Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5aa4f-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="5aa4f-106">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="5aa4f-106">**Resolution**</span></span>

<span data-ttu-id="5aa4f-107">Bæta verður notanda við hlutverk umhverfishönnuðar fyrir umhverfið í Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="5aa4f-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="5aa4f-108">Stjórnandi sem er með leyfi PowerApps Plan 2 verður að opna [Stjórnandagátt PowerApps](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="5aa4f-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="5aa4f-109">Veljið **Umhverfi** og veljið rétta umhverfið fyrir Talent.</span><span class="sxs-lookup"><span data-stu-id="5aa4f-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="5aa4f-110">Á flipanum **Öryggi**, á flipanum **Umhverfishlutverk**, skal velja **Hönnuður umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="5aa4f-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Flipinn „Umhverfishlutverk“](media/environment-roles.png)

4. <span data-ttu-id="5aa4f-112">Á flipanum **Notendur** skal bæta við notanda eða fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="5aa4f-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Flipinn „notendur“](media/environment-maker.png)

5. <span data-ttu-id="5aa4f-114">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5aa4f-114">Select **Save**.</span></span>
6. <span data-ttu-id="5aa4f-115">Notandi verður að skrá sig inn í [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="5aa4f-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="5aa4f-116">Veljið **Samstilling** til að uppfæra forrit notanda.</span><span class="sxs-lookup"><span data-stu-id="5aa4f-116">Select **Sync** to update the user apps.</span></span>

    ![Samstillingarhnappur](media/get-more.png)

    <span data-ttu-id="5aa4f-118">Talent birtist á heimasíðunni þegar samstillingu lýkur.</span><span class="sxs-lookup"><span data-stu-id="5aa4f-118">After synchronization is completed, Talent will appear on the home page.</span></span>


---
title: Talent birtist ekki á meðal forrita Microsoft Dynamics 365 (Common Data Service 1.0)
description: Þetta efnisatriði útskýrir hvað á að gera ef viðskiptamaður sér ekki forritið Microsoft Dynamics 365 Talent á meðal forrita Microsoft Dynamics 365.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a44d2e43752960d3026fa7ac92c7b261aee05448
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897028"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="69f76-103">Talent birtist ekki á meðal forrita Microsoft Dynamics 365 (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="69f76-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

<span data-ttu-id="69f76-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="69f76-104">**Issue**</span></span>

<span data-ttu-id="69f76-105">Viðskiptamaður sér ekki forritið Microsoft Dynamics 365 Talent á meðal forrita Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="69f76-105">The customer doesn't see the Microsoft Dynamics 365 Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="69f76-106">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="69f76-106">**Resolution**</span></span>

<span data-ttu-id="69f76-107">Bæta verður notanda við hlutverk umhverfishönnuðar fyrir umhverfið í Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="69f76-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="69f76-108">Stjórnandi sem er með leyfi Power Apps Plan 2 verður að opna [Power Apps-stjórnandagátt](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="69f76-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="69f76-109">Veljið **Umhverfi** og veljið rétta umhverfið fyrir Talent.</span><span class="sxs-lookup"><span data-stu-id="69f76-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="69f76-110">Á flipanum **Öryggi**, á flipanum **Umhverfishlutverk**, skal velja **Hönnuður umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="69f76-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Flipinn „Umhverfishlutverk“](media/environment-roles.png)

4. <span data-ttu-id="69f76-112">Á flipanum **Notendur** skal bæta við notanda eða fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="69f76-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Flipinn „notendur“](media/environment-maker.png)

5. <span data-ttu-id="69f76-114">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="69f76-114">Select **Save**.</span></span>
6. <span data-ttu-id="69f76-115">Notandi verður að skrá sig inn í [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="69f76-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="69f76-116">Veljið **Samstilling** til að uppfæra forrit notanda.</span><span class="sxs-lookup"><span data-stu-id="69f76-116">Select **Sync** to update the user apps.</span></span>

    ![Samstillingarhnappur](media/get-more.png)

    <span data-ttu-id="69f76-118">Talent birtist á heimasíðunni þegar samstillingu lýkur.</span><span class="sxs-lookup"><span data-stu-id="69f76-118">After synchronization is completed, Talent will appear on the home page.</span></span>

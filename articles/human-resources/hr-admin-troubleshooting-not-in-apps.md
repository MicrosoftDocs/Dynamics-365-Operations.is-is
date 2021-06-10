---
title: Human Resources birtist ekki í forritum Microsoft Dynamics 365
description: Þessi grein útskýrir hvað á að gera ef viðskiptamaður sér ekki forritið Microsoft Dynamics 365 Human Resources á meðal forrita Microsoft Dynamics 365.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17a454cd32a08db105a13577c32368ad819bed1c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053377"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="74c0c-103">Human Resources birtist ekki í forritum Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="74c0c-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="74c0c-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="74c0c-104">**Issue**</span></span>

<span data-ttu-id="74c0c-105">Viðskiptavinurinn sér ekki Dynamics 365 Human Resources meðal Microsoft Dynamics 365 forrita.</span><span class="sxs-lookup"><span data-stu-id="74c0c-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="74c0c-106">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="74c0c-106">**Resolution**</span></span>

<span data-ttu-id="74c0c-107">Bæta verður notanda við hlutverk umhverfishönnuðar fyrir umhverfið í Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="74c0c-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="74c0c-108">Stjórnandi sem er með leyfi Power Apps Plan 2 verður að opna [Power Apps-stjórnandagátt](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="74c0c-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="74c0c-109">Veljið **Umhverfi** og veljið rétta umhverfið fyrir Human Resources.</span><span class="sxs-lookup"><span data-stu-id="74c0c-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="74c0c-110">Á flipanum **Öryggi**, á flipanum **Umhverfishlutverk**, skal velja **Hönnuður umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="74c0c-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Flipinn „Umhverfishlutverk“](media/environment-roles.png)

4. <span data-ttu-id="74c0c-112">Á flipanum **Notendur** skal bæta við notanda eða fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="74c0c-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Flipinn „notendur“](media/environment-maker.png)

5. <span data-ttu-id="74c0c-114">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="74c0c-114">Select **Save**.</span></span>

6. <span data-ttu-id="74c0c-115">Notandi verður að skrá sig inn í [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="74c0c-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="74c0c-116">Veljið **Samstilling** til að uppfæra forrit notanda.</span><span class="sxs-lookup"><span data-stu-id="74c0c-116">Select **Sync** to update the user apps.</span></span>

    ![Samstillingarhnappur](media/get-more.png)

    <span data-ttu-id="74c0c-118">Human Resources birtist á heimasíðunni þegar samstillingu lýkur.</span><span class="sxs-lookup"><span data-stu-id="74c0c-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
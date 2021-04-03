---
title: Aðgangur að einkaaðsetrum eftir öryggishlutverki
description: Þessi grein útskýrir hvernig á að leysa vandamál þar sem viðskiptamaður fær ekki aðgang að einkaaðsetrum.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49f9f50b774df8e215c084bbb493a6be9de6b234
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463937"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="af2fb-103">Aðgangur að einkaaðsetrum í gegnum öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="af2fb-103">Access to private addresses by security role</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="af2fb-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="af2fb-104">**Issue**</span></span>

<span data-ttu-id="af2fb-105">Viðskiptamaður getur ekki séð aðsetur sem voru merkt sem einkaaðsetur þegar hann afritar öryggishlutverk og skráir sig inn með nýja hlutverkinu.</span><span class="sxs-lookup"><span data-stu-id="af2fb-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="af2fb-106">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="af2fb-106">**Resolution**</span></span>

<span data-ttu-id="af2fb-107">Til að leysa vandamálið verður viðskiptamaðurinn að fylgja þessum skrefum fyrir afrituð öryggishlutverk.</span><span class="sxs-lookup"><span data-stu-id="af2fb-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="af2fb-108">Opnið **Fyrirtækisstjórnun \> Altæk aðsetursbók \> Færibreytur altækrar aðsetursbókar**.</span><span class="sxs-lookup"><span data-stu-id="af2fb-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="af2fb-109">Á flipanum **Öryggi einkastaðsetningar** skal færa nýja öryggishlutverkið úr listanum **Tiltæk hlutverk** í listann **Valin hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="af2fb-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="af2fb-110">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="af2fb-110">Select **Save**.</span></span>

![Færibreytusíða altækrar aðsetursbókar](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Aðgangur að einkaaðsetrum eftir öryggishlutverki
description: Þessi grein útskýrir hvernig á að leysa vandamál þar sem viðskiptamaður fær ekki aðgang að einkaaðsetrum.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419000"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="f19e5-103">Aðgangur að einkaaðsetrum í gegnum öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="f19e5-103">Access to private addresses by security role</span></span>

<span data-ttu-id="f19e5-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="f19e5-104">**Issue**</span></span>

<span data-ttu-id="f19e5-105">Viðskiptamaður getur ekki séð aðsetur sem voru merkt sem einkaaðsetur þegar hann afritar öryggishlutverk og skráir sig inn með nýja hlutverkinu.</span><span class="sxs-lookup"><span data-stu-id="f19e5-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="f19e5-106">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="f19e5-106">**Resolution**</span></span>

<span data-ttu-id="f19e5-107">Til að leysa vandamálið verður viðskiptamaðurinn að fylgja þessum skrefum fyrir afrituð öryggishlutverk.</span><span class="sxs-lookup"><span data-stu-id="f19e5-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="f19e5-108">Opnið **Fyrirtækisstjórnun \> Altæk aðsetursbók \> Færibreytur altækrar aðsetursbókar**.</span><span class="sxs-lookup"><span data-stu-id="f19e5-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="f19e5-109">Á flipanum **Öryggi einkastaðsetningar** skal færa nýja öryggishlutverkið úr listanum **Tiltæk hlutverk** í listann **Valin hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="f19e5-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="f19e5-110">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f19e5-110">Select **Save**.</span></span>

![Færibreytusíða altækrar aðsetursbókar](media/GAD-parameters.png)

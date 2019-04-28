---
title: Aðgangur að einkaaðsetrum í gegnum öryggishlutverk
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem viðskiptamaður fær ekki aðgang að einkaaðsetrum.
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
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "859483"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="626e3-103">Aðgangur að einkaaðsetrum í gegnum öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="626e3-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="626e3-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="626e3-104">**Issue**</span></span>

<span data-ttu-id="626e3-105">Viðskiptamaður getur ekki séð aðsetur sem voru merkt sem einkaaðsetur þegar hann afritar öryggishlutverk og skráir sig inn með nýja hlutverkinu.</span><span class="sxs-lookup"><span data-stu-id="626e3-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="626e3-106">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="626e3-106">**Resolution**</span></span>

<span data-ttu-id="626e3-107">Til að leysa vandamálið verður viðskiptamaðurinn að fylgja þessum skrefum fyrir afrituð öryggishlutverk.</span><span class="sxs-lookup"><span data-stu-id="626e3-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="626e3-108">Opnið **Fyrirtækisstjórnun \> Altæk aðsetursbók \> Færibreytur altækrar aðsetursbókar**.</span><span class="sxs-lookup"><span data-stu-id="626e3-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="626e3-109">Á flipanum **Öryggi einkastaðsetningar** skal færa nýja öryggishlutverkið úr listanum **Tiltæk hlutverk** í listann **Valin hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="626e3-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="626e3-110">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="626e3-110">Select **Save**.</span></span>

![Færibreytusíða altækrar aðsetursbókar](media/GAD-parameters.png)

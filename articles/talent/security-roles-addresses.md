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
ms.openlocfilehash: 58f3322ad64f7de07e17d193ff665bd6536a4070
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897098"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="d7776-103">Aðgangur að einkaaðsetrum í gegnum öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="d7776-103">Access to private addresses by security role</span></span>

<span data-ttu-id="d7776-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="d7776-104">**Issue**</span></span>

<span data-ttu-id="d7776-105">Viðskiptamaður getur ekki séð aðsetur sem voru merkt sem einkaaðsetur þegar hann afritar öryggishlutverk og skráir sig inn með nýja hlutverkinu.</span><span class="sxs-lookup"><span data-stu-id="d7776-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="d7776-106">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="d7776-106">**Resolution**</span></span>

<span data-ttu-id="d7776-107">Til að leysa vandamálið verður viðskiptamaðurinn að fylgja þessum skrefum fyrir afrituð öryggishlutverk.</span><span class="sxs-lookup"><span data-stu-id="d7776-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="d7776-108">Opnið **Fyrirtækisstjórnun \> Altæk aðsetursbók \> Færibreytur altækrar aðsetursbókar**.</span><span class="sxs-lookup"><span data-stu-id="d7776-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="d7776-109">Á flipanum **Öryggi einkastaðsetningar** skal færa nýja öryggishlutverkið úr listanum **Tiltæk hlutverk** í listann **Valin hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="d7776-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="d7776-110">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d7776-110">Select **Save**.</span></span>

![Færibreytusíða altækrar aðsetursbókar](media/GAD-parameters.png)

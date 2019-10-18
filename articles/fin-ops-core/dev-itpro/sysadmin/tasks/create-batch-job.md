---
title: Stofna runuvinnslu
description: Runuvinnsla er flokkur verka sem er sendur til AOS-tilviksins (hugbúnaðarhlutarþjónstilviks) í sjálfvirka vinnslu.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191386"
---
# <a name="create-a-batch-job"></a>Stofna runuvinnslu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Runuvinnsla er flokkur verka sem er sendur til AOS-tilviksins (hugbúnaðarhlutarþjónstilviks) í sjálfvirka vinnslu. Runuvinnslur er keyrðar með því að nota öryggis- og notendaheimildir þess notanda sem stofnaði verkið. Fylgið eftirfarandi ferli ef stofna á runuvinnslu. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-the-batch-job"></a>Stofna runuvinnslu
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Fyrirspurnir > Runuvinnslur**.
2. Smellt er á **Nýtt**.
3. Færðu inn gildi í reitnum **Starfslýsing**.
4. Í reitinn **Áætluð upphafsdags./-tími** skráirðu dags. og tíma.
5. Smellt er á **Vista**.

## <a name="create-a-recurrence"></a>Stofna endurtekningu
1. Í aðgerðasvæðinu er smellt á **Runuvinnsla**.
2. Smelltu á **Endurtekning**. Notið þessa valkosti til að færa inn afmörkun og mynstur fyrir endurtekninguna.  
3. Smellt er á **OK**.

## <a name="add-alerts"></a>Bæta við viðvaranir
1. Í aðgerðasvæðinu er smellt á **Runuvinnsla**.
2. Smelltu á **Viðvaranir**. Tilgreina hvort óskað sé eftir að viðvörunarboðin birtist þegar runuvinnsla lýkur, villa er til staðar eða hætt er við. Tilgreinið síðan ef óskað er eftir að viðvaranir birtist sem sprettigluggar.   
3. Smellt er á **OK**.

## <a name="adjust-batch-job-status"></a>Stilla stöðu runuvinnslu
1. Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.
2. Veldu viðeigandi runuvinnslu.
3. Í aðgerðasvæðinu smellirðu á **Runuvinnsla > Aðgerðir > Breyta stöðu**.
4. Veldu viðeigandi stöðu:
    - **Halda eftir**: Stilla runuvinnsluna sem **halda eftir** svo að henni er haldið eftir í verkraðara runuvinnslu. Jafngildir *stöðva*.
    - **Bið**: Stilla runuvinnsluna sem **bið** svo að hún bíður þess að verkraðari runuvinnslu taki hana til. Jafngildir *ræsa*.
5. Smellt er á **OK**.

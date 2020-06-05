---
title: Kostnaður innan samstæðu
description: Starfskraftur sem starfar hjá einum lögaðila í fyrirtæki kann að vinna verk fyrir annan lögaðila í sama fyrirtæki. Í þeim aðstæðum er hægt að nota valkost kostnaðar innan samstæðu til að úthluta kostnaði starfsmannsins á lögaðilann sem verkið var unnið fyrir.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390885"
---
# <a name="intercompany-expenses"></a>Kostnaður innan samstæðu

[!include [banner](../includes/banner.md)]

Starfskraftur sem starfar hjá einum lögaðila í fyrirtæki kann að vinna verk fyrir annan lögaðila í sama fyrirtæki. Í þeim aðstæðum er hægt að nota valkost kostnaðar innan samstæðu til að úthluta kostnaði starfsmannsins á lögaðilann sem verkið var unnið fyrir. Lögaðilinn sem starfsmaðurinn vinnur hjá er kallaður lögaðili sem lánar. Lögaðilinn sem starfskrafturinn stofnar til kostnaðarins fyrir kallast lögaðili sem fær lánað. 

Áður en starfskraftur getur búið til og lagt fram kostnað vegna vinnu sem er framkvæmd fyrir annan lögaðilann, í lögaðila sem lánar, á **Færibreytur kostnaðarstjórnunar** síðunni skal velja **Leyfa kostnaðarlínur innan samstæðu**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Bókun skatts fyrir kostnað innan samstæðu

[!include [banner](../includes/banner.md)]

Ef óskað er eftir að nota skattflokka sem tengjast lánaeiningunni (Uppruni) í stað þess að lána (viðtökustaður) lögaðila í kostnaðarskýrslu þarf að stilla það í VSK-uppsetningu fjárhags. Þegar fjárhagsfæribreytan **Lögaðili fyrir skattbókun innan samstæðu** er stillt á **Uppruna** og færibreytan **Nota skattareglur virðisaukaskatts** er stillt á **Nei**, verður að nota skattsamsetningu fyrir lögaðilann sem lánar. Þegar sama færibreyta er stillt á **Áfangastað**, verður notuð skattsamsetning fyrir lögaðilann sem fær lánað. Fyrir lögaðila í Bandaríkjunum, þegar færibreytan er stillt á **Uppruni**, verður einnig að skilgreina **Innskatt** á síðu nýrra **fjárhagsbókunarflokka**. Bókhaldsvélin notar upplýsingarnar úr þessum reit fyrir skattatengda bókhaldsfærslu.   
Hegðunin er í samræmi við kostnaðarlínur sem bókaðar eru með eða án verks.  

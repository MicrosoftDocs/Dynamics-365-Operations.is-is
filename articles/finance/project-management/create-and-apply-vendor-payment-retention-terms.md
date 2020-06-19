---
title: Stofna og nota varðveisluskilmála greiðslu lánardrottins
description: Í þessu efnisatriði eru upplýsingar um hvernig á að setja upp og vinna með varðveisluskilmála fyrir lánardrottnagreiðslur.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410233"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Stofna og nota varðveisluskilmála greiðslu lánardrottins

[!include [banner](../includes/banner.md)] 

Uppsetning varðveisluskilmála lánardrottnagreiðslu fyrir verk er gagnlegt þegar fyrirtækið vill halda eftir hluta af greiðslunum sem greiddar eru lánardrottni. Til dæmis þegar óskað er eftir að bíða með greiðslu til lánardrottins þangað til afurðirnar sem afhentar eru uppfylla væntingar þínar. Hægt er að tilgreina varðveisluskilmála lánardrottnagreiðslu þegar samið er um lánardrottnasamning.

## <a name="create-vendor-payment-retention-terms"></a>Búa til varðveisluskilmála lánardrottnagreiðslu

Hægt er að færa inn það hlutfall af greiðslu til lánardrottins sem varðveita á og hlutfall áður viðhaldinna upphæða sem losa á. Upphæðir eru varðveittar sjálfkrafa á reikningum lánardrottna þar til samningur nær tilgreindri stöðu samningsloka. Eftir að varðveisluskilmálarnir eru settir upp er hægt að nota þá í hvaða verki sem er fyrir þennan lánardrottin.

Notið eftirfarandi skref til að setja upp og vinna með varðveisluskilmála fyrir lánardrottnagreiðslur. 

1. Opnið **Verkefnastjórnun og bókhald** > **Varðveisla** > **Varðveisluskilmálar lánardrottnagreiðslu**.
2. Veljið **Nýr** til að bæta við nýjum varðveisluskilmála lánardrottins. Gildið fyrir **Reglukenni** nýja hugtaksins er fært inn sjálfkrafa. 
3. Sláið inn stutta lýsingu í reitnum **Lýsing** og í flýtiflipanum **Skilmálar** skal velja **Bæta við línu** til að færa inn gildi skilmála fyrir eftirfarandi:

   - **Prósenta afhentra eininga**: Færið inn prósentu þess sem er lokið fyrir skilmálann. Upphæðir eru sjálfkrafa varðveittar á reikningum lánardrottna þar til verkstigi sem er lokið jafngildir tilgreindri prósentu. Til dæmis, ef fært er inn 50.00 eru upphæðir geymdar þar til 50 prósentum af verkinu er lokið.
   - **Prósenta til varðveislu**: Færa skal inn prósentu af reikningsupphæð lánardrottins sem á að varðveita. Til dæmis, ef fært er inn 10,00, þá eru 10 prósent upphæðarinnar á reikningi lánardrottins varðveitt þar til verkið nær yfir þá prósentu sem er lokið eins og það er stillt í reitnum **Prósenta afhentra eininga**.
   - **Prósenta til losunar**: Veljið **Bæta við línu** til að færa inn prósentu af áður varðveittum upphæðum sem á að losa fyrir valið stig verks sem er lokið.

> [!NOTE]
> Ef til eru fleiri en ein þáttaskil fyrir mismunandi stig verkloka skal færa inn sérstaka varðveisluskilmálalínu lánardrottins fyrir hverja varðveislureglu. Hver lína getur tilgreint mismunandi varðveisluprósentu og mismunandi losunarprósentu fyrir hvert uppgefið stig verkloka.

Þegar varðveisluskilmálar lánardrottins er búnir til fyrir lánardrottin er hægt að nota skilmálana fyrir verk.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Nota varðveisluskilmála lánardrottins í verk

1. Opnið **Verkefnastjórnun og bókhald** > **Verk** > **Öll verk** og opnið verk á listasíðu verksins.
2. Á flýtiflipanum **Samningar lánardrottins** velurðu **Bæta við línu**.
3. Veljið einn eftirfarandi valkosta í svæðinu **Lykilkóði**: 

   - **Tafla**: Varðveisluskilmálar lánardrottins eiga við um einn stakan lánardrottinn.
   - **Flokka** – Varðveisluskilmálar lánardrottins eiga við um alla lánardrottna í lánardrottnaflokki.
   - **Allt** – Varðveisluskilmálar lánardrottins eiga við um alla lánardrottna.

4. Á svæðinu **Lánardrottinn/lánardrottnaflokkur** er valinn sá lánardrottinn eða lánardrottnaflokkur sem varðveisluskilmálar lánardrottins eiga við um. Ef **Allir** var valið í skrefinu á undan er þetta svæði ekki tiltækt.
5. Í reitnum **Varðveisluskilmálar lánardrottins** skal velja varðveisluskilmálana sem voru búnir til í ferlinu á undan.
6. Ef „greiðist-þegar-greitt“-skilmálar (GÞG) hafa einnig verið settir upp fyrir lánardrottin skal færa inn þröskuldsprósentuna fyrir verkið í reitinn **GÞG-þröskuldsprósenta**.

Varðveisluskilmálar lánardrottins birtast einnig á innkaupapöntunum sem gerðar eru fyrir lánardrottininn.

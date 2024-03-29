---
title: Reikningsjöfnun og samstæðuinnkaupapöntun
description: Innkaupalögaðili sem er þáttakandi í samstæðuviðskiptafærslu gæti verið uppsett til að nota reikningsjöfnun viðskiptaskulda. Í þessu tilfelli þarf að uppfylla bókunarkröfur bæði fyrir samstæðuviðskipti og reikningsjöfnun viðskiptaskulda áður en hægt er að bóka lánardrottinsreikninga innan samstæðu.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4be32a7158561bdf00a996831dca7395ce6f331
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879741"
---
# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Reikningsjöfnun og samstæðuinnkaupapöntun

[!include [banner](../includes/banner.md)]

Innkaupalögaðili sem er þáttakandi í samstæðuviðskiptafærslu gæti verið uppsett til að nota reikningsjöfnun viðskiptaskulda. Þegar **Settu inn reikning með misræmi** reit á síðunni **Breytir viðskiptakrafna** form er stillt á **Krefjast samþykkis**, verður staðfesting staðfestingar reikninga gerð. Í þessu tilfelli þarf að uppfylla bókunarkröfur bæði fyrir samstæðuviðskipti og reikningsjöfnun viðskiptaskulda áður en hægt er að bóka lánardrottinsreikninga innan samstæðu.

Eftirfarandi uppsetning á samstæðuviðskiptum er notuð í þessari grein:
-   Fabrikam Purchase er innkaupalögaðilinn.
-   Fabrikam Sales er sölulögaðilinn.
-   Viðskiptavinurinn 4020 er í Fabrikam Sala.
-   Lánardrottinninn 3024 er í Fabrikam Innkaup.
-   Í Fabrikam Purchase eru samstæðuupplýsingar tilgreindar fyrir lánardrottinn 3024. Fabrikam Sales er tilgreindur sem fyrirtæki viðskiptavinar og viðskiptavinurinn 4020 er tilgreindur sem lykill viðskiptavinarins sem samsvarar lögaðila Fabrikam Purchase.
-   Í Fabrikam Sales eru samstæðuupplýsingar tilgreindar fyrir lánardrottinn 4020. Fabrikam Purches er tilgreindur sem fyrirtæki lánardrottins og lánardrottinn 3024 er tilgreindur sem lánardrottnalykill sem samsvarar lögaðila Fabrikam Sales.

Dæmið notar Eftirfarandi uppsetning á reikningsjöfnun viðskiptaskulda fyrir Fabrikam Purchase:
-   Á **Færibreytusíða viðskiptaskulda**, er valinn valkosturinn **Gera villuprófun á reikningsjöfnun virka**.
-   Á síðunni **Færibreytusíða viðskiptaskulda**, svæðið **Bóka reikning með misræmi** er stillt á að **Krefjast samþykkis**.
-   Vikmarkaprósenta verðs fyrir lögaðilann er 2%.

## <a name="example-price-matching-and-intercompany-trade"></a>Dæmi: Verðjöfnun og samstæðuviðskipti
Nettóupphæðir lánardrottinsreiknings innan samstæðu og samstæðureikningur viðskiptavinar verða að vera jafnar. Þessi krafa hnekkir allri samþykktri reikningsjöfnun eða verðvikmarkaprósentum sem eiga við. Fylgdu til dæmis eftirfarandi skrefum.
1.  Stofna sölupöntun SO888 fyrir viðskiptavin 4020 í Fabrikam Purchase. Samstæðuinnkaupapöntun númer ICPO222 er sjálfkrafa stofnuð í Fabrikam Purchase fyrir lánardrottininn 3024 og sölupöntunin ICSO888 er stofnuð sjálfkrafa í Fabrikam Sales.
2.  Skrá móttöku varanna og bóka fylgiseðil í Fabrikam Sala. Staða ICSO888 breytist í Afhent. Staða ICPO222 breytist í Móttekið.
3.  Í Fabrikam Sales, uppfæra reikning fyrir ICSO888. Einingarverð er 0,45 og 100 vörur eru uppfærðar.
4.  Stofna reikning fyrir ICPO222 í Fabrikam Innkaup. Þú breyttir óvart nettóverði úr 45,00 í 54,00. Teikn birtist sem gefur til kynna að verðið sé yfir leyfðum verðvikmörkum, 2 prósentum.
5.  Á upplýsingasíðunn **Reikningsjöfnun**, veljið valkost til að samþykkja bókun með misræmi í samsvörun. Á síðunni **Reikningur lánardrottins** skal smella á **í lagi**. Ef reikningur lánardrottins var ekki lánardrottinsreikningur innan samstæðu, myndi bókun heppnast. Hins vegar, þar sem unnið er með lánardrottinsreikning innan samstæðu, bókun tekst. Fyrir viðskipti innan samstæðu, Samtölur reikninga á samstæðusölupöntun, verður að vera jafnt og samtölur reikninga á samsvarandi samstæðuinnkaupapöntun. Til að leysa þetta vandamál verður að leiðrétta nettóverði reikningsins aftur í sjálfgefna upphæð, 45,00.

## <a name="example-quantity-matching-with-intercompany-trade"></a>Dæmi: Jöfnun magns í samstæðuviðskiptum
Magn samstæðuinnkaupapöntunarinnar og samstæðusölupöntunarinnar verður að vera jafnt. Krafan um þetta hnekkir allri samþykkt á reikningsjöfnun sem við á. Í þessu dæmi er eftirfarandi viðbótaruppsetning á samstæðuviðskiptum notuð:
-   Í Fabrikam Innkaup er aðgerðarregla innkaupapöntunar fyrir lánardrottinn 3024 sett upp til að bóka sjálfkrafa bæði upprunalega reikningur viðskiptavinar og reikningur lánardrottins innan samstæðu.

Dæmið notar Eftirfarandi aukalegu uppsetning á reikningsjöfnun viðskiptaskulda fyrir Fabrikam Purchase:
-   Á síðunni **Vörulíkanaflokkar** fyrir líkanaflokk sem er notað af vara B-R14 er valinn valkosturinn **Kröfur mótteknar**.
-   Magn vörunnar B-R14 á lager er 0.

Fylgdu til dæmis eftirfarandi skrefum.
1.  Stofna sölupöntun SO999 fyrir viðskiptavin 4020 í Fabrikam Purchase. Eitt línuatriði er í pöntuninni: 100 rafhlöður (vara B-R14) með einingarverðinu 1,00 hver. Samstæðuinnkaupapöntun númer ICPO333 er sjálfkrafa stofnuð í Fabrikam Purchase fyrir lánardrottininn 3024 og sölupöntunin ICSO999 er stofnuð sjálfkrafa í Fabrikam Sales.
2.  Gera reikningsuppfærslu fyrir ICSO999 í Fabrikam Sala. Bókun tekst ekki , þar sem varan er ekki til á lager og hefur ekki verið mótteknar. Þess vegna er hægt að uppfæra fjárhagslegar upplýsingar.
3.  Skrá móttöku varanna og bóka fylgiseðil ICSO999 í Fabrikam Sala. Með þessu er fylgiseðill bókaður sjálfkrafa fyrir ICPO333 í Fabrikam Innkaup. Móttekið magn vörunnar B-R14 í Fabrikam Innkaup breytist í 100.
4.  Gera reikningsuppfærslu fyrir ICSO999 í Fabrikam Sala. Bókun tekst í báðum lögaðilar. Keypt magn vörunnar B-R14 í Fabrikam Innkaup breytist í 100.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

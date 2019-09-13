---
title: Senda sölupantanir án vöruhúsa
description: Þetta efni útskýrir hvernig á að uppfæra sölupöntun þegar vörur eru sendar til viðskiptavinarins.
author: omulvad
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e311d3e033168ed577094e94477e7fe47d185d
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914931"
---
# <a name="ship-sales-orders-without-warehousing"></a>Senda sölupantanir án vöruhúsa

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta efni útskýrir hvernig á að uppfæra sölupöntun þegar vörur eru sendar til viðskiptavinarins. Leiðbeiningarnar eiga við um flæði uppfyllingar sem er ekki sett upp fyrir vöruhúsakerfi (hvorki grunnur eða ítarlegt vöruhús), og krefst þar af leiðandi ekki að afurð tiltektarlista sé skráð fyrir sendingu. Hægt er að keyra þetta ferli á eigin gögn eða í sýnigögn USMF fyrirtækis. Í báðum tilvikum, áður en þú ræsir þetta verk, skal stofna sölupöntun fyrir afurð á lager sem hefur magn sem er meira en 1. Til að forðast bókunarvillu þarf að athuga að afurðamagn á lager á því svæði og vöruhúsi sem var valið í pöntuninni nái yfir pöntunarmagnið.

## <a name="post-packing-slip-for-an-order"></a>Bóka fylgiseðil fyrir pöntun
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.
2. Í listanum skal finna og velja pöntun sem var stofnuð fyrir þetta verk.
3. Á aðgerðasvæðinu velurðu **Taka til og pakka**.
4. Veldu **Bóka fylgiseðil**.
5. Útvíkka eða draga saman hlutann **Færibreytur**.
6. Í reitnum **Magn** velurðu **Allt**.
    - Aðrir valkostir eru **Afhenda núna** og **Tekið til**. Ef senda á pöntunarlínuna að hluta til og reiturinn **Afhenda núna** í pöntunarlínunni inniheldur magn, myndirðu velja **Afhenda núna**. Ef flæði uppfyllingar fyrirtækis þíns felur í sér tiltektarlista sem aðskilda ferli sem er stjórnað af og skráð með tiltektarlista, myndirðu velja **Tiltekið**.  
    - Athuga að valkosturinn **Bókun** sé stilltur á **Já**.  
7. Stilla valkostinn **Prenta fylgiseðla** á **Já**. Flipinn **Yfirlit** inniheldur lista yfir fylgiseðla til að mynda í þessari bókun. Ef þú ert að senda einstaka pöntun verður yfirleitt einn fylgiseðil. Hins vegar ef pöntunarlínur eru til sendingar frá mismunandi svæðum verður bókun sjálfkrafa skipt í viðeigandi fjölda skjala. Þetta er áskilið skilyrði sem ekki er hægt að breyta. Á svipaðan hátt verður bókun einnig skipt upp í mörg skjöl ef senda á línur pöntunar á mismunandi afhendingaraðsetur og sendingarreglan er sett upp til að krefjast skiptingar.  
8. Á flipanum **Línur** velurðu röð fyrir pöntunarlínuna sem á að senda.
9. Í reitnum **Uppfæra** skal slá inn tölu sem er lægri en upphaflegt magn.
10. Veljið **Í lagi**.
11. Velja skal **Já**.
12. Lokið síðunni.
13. Í aðgerðasvæðinu velurðu **Valkostir**.
14. Veldu **Breyta skjámynd**.
15. Veldu **Hausyfirlit**.
    - Ef allar línur í pöntun hafa verið afgreiddar að fullu breytist staða pöntunar úr Opið í Afhent.  
    - Í þessu dæmi hefur pöntunarlínan verið send að hluta. Þess vegna helst pöntunarstaðan opin.     
    - Reiturinn **Staða skjals** er stilltur á fylgiseðil þar sem að minnsta kosti ein af pöntunarlínunum hefur verið send.  
16. Í aðgerðasvæðinu velurðu **Almennt**.
17. Velja **Línumagn**.
18. Lokið síðunni.
19. Á aðgerðasvæðinu velurðu **Taka til og pakka**.
20. Velja **Fylgiseðil**. Síðan **Færslubók fylgiseðla** inniheldur öll skjöl fylgiseðla sem voru mynduð fyrir pöntunina. Hægt er að fara yfir nákvæmar upplýsingar um hvert skjal og prenta þær, ef óskað er.  


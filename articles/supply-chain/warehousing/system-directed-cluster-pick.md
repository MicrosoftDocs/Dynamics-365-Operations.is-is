---
title: Kerfisstýrð klasatiltekt
description: Þetta efni veitir yfirlit yfir kerfisbundna klasatiltekt í Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 390e0a3379a6482e99a13f4f7835b5264e3747ac
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217242"
---
# <a name="system-directed-cluster-picking"></a>Kerfisstýrð klasatiltekt

[!include [banner](../includes/banner.md)]

Klasatiltekt er verk til að velja hluti sem gerir þér kleift að velja hluti fyrir margar pantanir á sama tíma með því að þjappa þeim í tiltektarklasa. Síðan verður þú að heimsækja tiltektarstaðinn aðeins einu sinni. Venjulega er þessi virkni notuð við litla pöntunartínslu eða magn sem er minna en tilfelli.

Þegar kerfisstýrð klasatiltekt er sett upp er hægt að klasatína vinnuhausa, byggð á kerfisframleiddum klasa. Kerfið klasatínir pantanir upp að fjölda staða sem tilgreindar eru í klasasniðinu. Þess vegna getur þú tínt margar pantanir á sama tíma án þess að þurfa að búa til klasa handvirkt.

Kerfisstýrð klasatiltekt býður annan valkost við handvirkra klasagerð, þar sem klasasnið er notað til að búa til klasa. Nokkrar uppsetningartengdar línur verða að vera skilgreindar í klasasniðinu áður en það er notað:

- **Fjöldi staða** samsvarar til fjölda pantana sem verða settar í klasa. Þess vegna samsvarar hann fjölda heildartölu.
- **Skipta klasaeiningu** ákvarðar hvenær skipta eigi klasaeiningunni.
- **Mynda klasaauðkenni** stjórnar því hvort klasakennið verði myndað af kerfinu eða fært inn af notandanum.
- **Gerð röðunarstaðfestingar** ákvarðar hvort staðfesting á stöðu sé nauðsynleg.

Nýtt valmyndaratriði fartækis er notað við kerfisstýrða klasatiltekt. Auðkenni klasasniðsins verður að vera tilgreint fyrir valkostinn **Stýrt af**. Að auki getur kerfisbundin fyrirspurnapöntun flokkað pantanir, byggðar á fyrirtækjasértækum forsendum. Þess vegna geturðu fínstillt úthlutun verkbeiðna frekar með því að tilgreina sérsniðnar flokkunarviðmiðanir í kerfisbundinni fyrirspurnapöntun.

Þegar kerfisstýrð klasatiltekt er gerð er starfskröftum vöruhúss birtur klasi þar sem tiltektarpöntunum hefur verið úthlutað á klasastöður. Þess vegna geta starfskraftar byrjað að taka til vöru fyrir margar verkbeiðnir með því að heimsækja tiltektarstaðinn aðeins einu sinni. Tínsluferlið fyrir kerfisstýrða klasatiltekt er það sama og ferlið fyrir notendastýrða klasatiltekt.

## <a name="set-up-system-directed-cluster-picking"></a>Setja upp kerfisstýrða klasatiltekt

### <a name="create-cluster-profiles"></a>Stofna klasaforstillingar

Klasaforstillngar stjórna því hvernig kerfið býr til hvern klasa. Ef krafist er mismunandi klasa ætti að búa til mismunandi klasastillingar fyrir hvert valmyndaratriði fartækis.

1. Farðu á **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Klasaforstillingar**.
2. Veljið **Nýtt**.
3. Í reitnum **Auðkenni klasaforstillinga** slærðu inn **2 staða**.
4. Í reitinn **Heiti** skal færa inn **Staða 2**.
5. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Mynda klasaauðkenni:** Stilltu þennan valkost á **Já**. Þessi valkostur ákvarðar hvort auðkenni klasans er sjálfkrafa búið til af kerfinu, eða hvort notandinn býr til það í upphafi tínslu.
    - **Virkja stöður:** Stilltu þennan valkost á **Já**. Þessi valkostur ákvarðar hvort stöðuheiti séu sjálfkrafa mynduð út frá uppsetningu stöðuheitis. Ef þessi valkostur er stilltur á **Nei** er kenni númeraplötuð notað fyrir stöðuna.
    - **Fjöldi staða:** Sláðu inn **2**. Þessi reitur ákvarðar hámarksfjölda staða sem klasinn getur haft (það er hámarksfjöldi kassa, heildartölur og svo framvegis).
    - **Stöðuheiti:** Veldu **Tölulegt** þannig að stöður séu nefndar með samfelldum tölum. Ef þú velur **Stafrófsröð** eru stöðurnar nefndar í stafrófsröð.
    - **Skipta klasaeiningu við:** Veldu **Frágangur**. Þessi reitur ákvarðar hvenær klasanum er skipt upp.
    - **Gerð röðunarstaðfestingar:** Veldu **Skönnun stöðu**. Þessi reitur ákvarðar hvort staðfestingarþrepið sé staðfest.

6. Á flýtiflipanum **Klasaröðun** er hægt að skilgreina röðunarviðmið með því að búa til nýja línu og stilla eftirfarandi reiti:

    - **Raðnúmer:** Þessi reitur ákvarðar röðina sem kerfið raðar eftir. Gildi er slegið sjálfkrafa inn en þú getur breytt því eins og þú vilt.
    - **Heiti reitar:** Veldu **WMSLocationId**. Þessi reitur ákvarðar reitinn sem línan notar sem röðunarviðmið.
    - **Röðun:** Veldu **Hækkandi**. Þessi reitur skilgreinir hvort röðunin sé gerð í hækkandi eða lækkandi röð.

### <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis

Fylgdu þessum skrefum til að búa til nýjan valmyndaratriði fartæki fyrir kerfisstýrða klasatiltekt og tengja kenni klasaforstillinga við valmyndaratriði fartækis.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti valmyndaratriðis** slærðu inn **SD-klasi**.
4. Í reitinn **Titill** slærðu inn **SD-klasi**.
5. Í reitnum **Stilling** velurðu **Vinna**.
6. Stilltu valkostinn **Nota fyrirliggjandi vinnu** á **Já**.
7. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Stýrt af:** Velduð **Stýrt af kerfi**.
    - **Mynda númeraplötu:** Stilltu þennan valkosti á **Já**.
    - **Auðkenni klasaforstillinga:** Veldu **Staða 2**.

8. Á flýtiflipanum **Vinnuklasar** skaltu setja upp gildan vinnuklasa fyrir þetta valmyndaratriði fartækis með því að stilla eftirfarandi reiti:

    - **Auðkenni vinnuklasa:** Gakktu úr skugga um að **Sala** sé slegin inn.
    - **Gerð verkbeiðnar:** Gakktu úr skugga um að **Sölupantanir** sé slegin inn.

9. Fylgdu þessum skrefum til að tilgreina nýja kerfisstýrða fyrirspurn vinnuraðar:

    1. Veljið **Nýtt**.
    2. Í reitinn **Raðarnúmer** skal rita **1**.
    3. Í reitnum **Lýsing** velurðu **Forgangur vinnu - Vinnukenni**.

10. Í valmyndinni velurðu **Breyta fyrirspurn**.
11. Á flipanum **Röðun** stillirðu eftirfarandi reiti:

    - **Tafla:** Veldu **Vinna**.
    - **Afleidd tafla:** Veldu **Vinna**.
    - **Reitur:** Veldu **Forgangur vinnu**.
    - **Leitarstefna:** Veldu **Hækkandi**.
    - **Tafla:** Veldu **Vinna**.
    - **Afleidd tafla:** Veldu **Vinna**.
    - **Reitur:** Veldu **Vinnukenni**.
    - **Leitarstefna:** Veldu **Hækkandi**.

Kerfið mun nú raða vinnukennum í klasanum, fyrst eftir forgangi vinnu og síðan eftir vinnukenni.

### <a name="set-up-a-mobile-device-menu"></a>Setja upp valmynd fartækja

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
2. Bættu valmyndaratriðinu sem þú bjóst til við valmyndina.

## <a name="example"></a>Dæmi

### <a name="create-picking-work"></a>Stofna tiltektarvinnu

Áður en þú getur sett upp kerfisstýrða klasatiltekt verður þú að búa til einhverja hæfa vinnu á útleið. Klasaforstillingin sem þú bjóst til áður tilgreinir tvær klasastöður. Þess vegna verður að búa til að minnsta kosti tvö vinnukenni.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
2. Smellið á **Nýtt** til að stofna nýja sölupöntun.
3. Í reitnum **Viðskiptavinalykill** velurðu einhvern viðskiptavin.
4. Á flýtiflipanum **Almennt**, í reitnum **Vöruhús**, velurðu vöruhús **62**.
5. Veljið **Í lagi**.
6. Á flýtiflipanum **Sölupantanalínur** skal velja **Bæta við línu**.
7. Í svæðið **Vörunúmer** veldu **A0001**.
8. Í **Magn** reitinn er fært inn **1**.
9. Veldu **Bæta við línu** til að bæta við annarri línu.
10. Í svæðið **Vörunúmer** veldu **A0002**.
11. Í **Magn** reitinn er fært inn **3**.
12. Endurtaktu skref 2 til 6.
13. Í svæðið **Vörunúmer** veldu **A0001**.
14. Í **Magn** reitinn er fært inn **4**.
15. Veldu **Bæta við línu** til að bæta við annarri línu.
16. Í svæðið **Vörunúmer** veldu **A0002**.
17. Í **Magn** reitinn er fært inn **2**.

Bókaðu birgðirnar og slepptu þeim í vöruhúsið. Tvö mismunandi vinnukenni eru búin til. Hvert vinnukenni hefur tvær tínslulínur.

### <a name="run-the-mobile-device-flow"></a>Keyrðu fartækjaflæðið

1. Í fartækinu velurðu valmynd sem inniheldur nýtt valmyndaratriði fartækis.
2. Veldu valmyndaratriðið **SD-klasi** og frumstilltu tínsluna. Klasi er búinn til og vinnukennin tvö sem þú bjóst til áður eru tengd við hann. Ef þú bjóst til fleiri en tvö vinnukenni er aðeins fyrstu tveimur bætt við klasann. Athugaðu að vinnukennum sé bætt við klasann í hækkandi röð eins og þú tilgreindir í fyrirspurnaruppsetningunni.

    > [!NOTE]
    > Nýi klasinn er sjálfkrafa aðeins myndaður ef nóg viðbótar vinnukenni hafa áður verið mynduð. Annars eru eftirfarandi skilaboð sýnd: "Ekki er hægt að finna næga vinnu fyrir klasann."

    Eftir að þú hefur valið valmyndina birtist fyrsta valmyndin. Kerfið safnar saman öllum samsvarandi tiltektarlínum úr vinnukennunum tveimur og beinir þér til að heimsækja tiltektarstaðinn einu sinni, svo að þú getir fullnægt báðum pöntunum með því að nota eina tínslu. Þetta ferli er gert á sama hátt og ferli fyrir notendastýrða klasatiltekt.

3. Staðfestu fyrstu tiltektina. Síðan verðurðu að slá inn stöðuheitið til að staðfesta að hlutirnir hafi verið settir á réttan stað.
4. Endurtaktu þetta ferli þar til allir hlutir hafa verið valdir og settir í rétta stöðu.
5. Síðasta skrefið í fartækinu er að ganga frá klasanum á endanlega staðsetningu. Þegar þessi aðgerð er staðfest er klasanum lokað og skipt upp, miðað við gildið sem þú stillir fyrir reitinn **Skipta klasaeiningu við** í klasaforstillingunum. Vinnukennum er einnig lokað.
6. Skilaboðin „Klasa lokið“ eru sýnd á fartækinu.

--- 
title: "Setja upp gámun"
description: "Þetta aðferð lýsir því hvernig á að gera sjálfvirka gámun á farm í vöruhúsakerfi"
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-containerization"></a>Setja upp gámun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta aðferð lýsir því hvernig á að gera sjálfvirka gámun á farm í vöruhúsakerfi Sjálfvirk gámun stofnar gáma og tínsluvinnu fyrir sendingar þegar unnið er úr bylgju og hægt er að skipta upp vinnulínum í magn sem passa við gáma. Þetta hjálpar starfsmenn vöruhúss að taka til vörur beint í gám sem var valið. Borið saman við handvirkt pökkunarferli eru verk eins og stofnun gáma, úthluta vörum og lokunar gáma sjálfvirk af kerfinu. Þetta ferli notar USMF sýnifyrirtækið og er framkvæmt af stjórnanda Vöruhúsi.


## <a name="set-up-a-wave-template"></a>Velja bylgjusniðmát
1. Fara í vöruhúsakerfi > Uppsetning > Bylgjur > bylgjusniðmát.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti bylgjusniðmáts skal slá inn gildi.
4. Færa inn gildi í reitnum lýsingu bylgjusniðmáts.
5. Sláið inn eða veldu gildi í reitnum svæði.
6. Sláðu inn eða veldu gildi í reitnum Vöruhús.
7. Víkkið út hlutann aðferðir.
    * Valdar aðferðir svæðið skráir aðferðir fyrir valið bylgjusniðmát tegund. Bylgjusniðmátið verður að hafa með gámunar aðferð.  
8. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
9. Færa inn gildi í svæðinu bylgjuskrefakóði.
    * Færið inn bylgjuskrefskóða fyrir viðbætta aðferð sem má vera hvaða kóði sem er. Hægt er að bæta við aðferð oftar en einu sinni og úthluta mismunandi kóðum fyrir bylgjuskref. Veljið Endurtekin fyrir þennan aðferð á síðu aðferðir Bylgju ferli til að gera þetta.  
10. Smellið á „Vista“.
11. Lokið síðunni.

## <a name="set-up-a-container-type"></a>Setja upp gámagerð
1. Fara í vöruhúsakerfi  > Uppsetningu  > Gáma  > gámagerðir.
    * Hægt er að skilgreina gáma á Gáms gerðir síðu. Þú getur stillt efnisleg vídd gámanna, þar á meðal töruþungi, hámarks þyngd, hámarksrúmmál, lengd, breidd og hæð. Í þessu dæmi eru þrjár mismunandi stærðum kassar.  
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðinu kóði gámagerðar.
4. Í reitinn Umbúðaþyngd skal slá inn númer.
5. Í reitinn hámarksþyngd skal slá inn númer.
6. Í reitinn Magn skal slá inn númer.
7. Í reitinn Lengd skal slá inn númer.
8. Færið númer inn í svæðið breidd.
9. Færið númer inn í svæðið hæð.
10. Sláið inn gildi í reitnum „Lýsing“.
11. Smellið á „Vista“.
12. Smellið á „Nýtt“.
13. Færa inn gildi í svæðinu kóði gámagerðar.
14. Sláið inn gildi í reitnum „Lýsing“.
15. Í reitinn Umbúðaþyngd skal slá inn númer.
16. Í reitinn hámarksþyngd skal slá inn númer.
17. Í reitinn Magn skal slá inn númer.
18. Í reitinn Lengd skal slá inn númer.
19. Færið númer inn í svæðið breidd.
20. Færið númer inn í svæðið hæð.
21. Smellið á „Vista“.
22. Smellið á „Nýtt“.
23. Færa inn gildi í svæðinu kóði gámagerðar.
24. Sláið inn gildi í reitnum „Lýsing“.
25. Í reitinn Umbúðaþyngd skal slá inn númer.
26. Í reitinn hámarksþyngd skal slá inn númer.
27. Í reitinn Magn skal slá inn númer.
28. Í reitinn Lengd skal slá inn númer.
29. Færið númer inn í svæðið breidd.
30. Færið númer inn í svæðið hæð.
31. Smellið á „Vista“.
32. Lokið síðunni.

## <a name="set-up-a-container-group"></a>Setja upp gámaflokk
1. Fara í vöruhúsakerfi  > Uppsetningu  > Gáma  > gámahópar.
2. Smellið á „Nýtt“.
    * Þú getur sett upp rökrétta flokka af gámagerðum. Fyrir hvern hóp er hægt að tilgreinir í hvaða röð gámar eru pakkaðar og fyllingarhlutfall hvers gáms. Stærð vídda vörunnar er notuð til að ákvarða hvort hún passar í gám. Geymir sem er næst er afhendingardegi stærð vídda vörunnar er notað. Ef margar gámagerðum eru í flokki, er ráðlagt að hagræða röðinni eftir stærð, þannig að stærsta gámurinn er fyrst, númer 1 í röðinni og minnsti gámurinn er síðasta.    
3. Færa inn gildi í reitnum Auðkenni gámahóps.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Smellt er á Nýtt.
6. Í listanum skal merkja valda línu.
7. Færa inn eða veljið gildi í svæðinu gerð gáms.
8. Smellt er á Nýtt.
9. Í listanum skal merkja valda línu.
10. Færa inn eða veljið gildi í svæðinu gerð gáms.
11. Smellt er á Nýtt.
12. Í listanum skal merkja valda línu.
13. Færa inn eða veljið gildi í svæðinu gerð gáms.
14. Smellið á „Vista“.
15. Lokið síðunni.

## <a name="set-up-a-container-build-template"></a>Setja upp gámaröðunarsniðmát
1. Fara í vöruhúsakerfi  > Uppsetningu  > Gáma  > gámaröðunarsniðmát.
2. Smellið á „Nýtt“.
    * Gámaröðunarsniðmát byggist á hvaða gámunarferli eru framkvæmdar. Hver gámaröðunarsniðmát skilgreinir eina gámunarferli sem verða notuð af bylgjusniðmáti. Breyta fyrirspurn valkostur gerir kleift að skilgreina skilyrðin sem völdu sniðmáti er unnið úr. Til dæmis kannt þú að vilja keyra aðeins gámunarferli fyrir tiltekna viðskiptavini, vörur eða vöruhús eða þá að þú getur bætt viðkomandi fyrirspurn við sniðmátið. Svæðið Bylgju skref kóði er hvernig gámaröðunarsniðmát er tengd við skrefin í bylgjusniðmáti. Þegar framkvæmt er bylgju ákvarðar hún hvaða gámaröðunarsniðmát eru notaðar til að hefja gámun. Reitur grunngerð fyrirspurnar ákvarða hverju á að pakka og hvað á að miða síufyrirspurnina á.  
3. Í listanum skal merkja valda línu.
4. Færa inn gildi í reitnum Kenni gámasniðmáts.
5. Í reitinn auðkenni gámahóps skal slá inn eða velja gildi.
6. Færa inn gildi í svæðinu bylgjuskrefakóði.
7. Veljið gátreitinn leyfa að skipta tiltekt.
8. Smellið á „Vista“.
9. Smella á Blöndunartakmarkanir gáma
    * Skipti í blöndunarrökum gerir kleift að setja upp reglur fyrir úthlutunarlínur í gáma. Til dæmis ef bætt er við svæðið vörunúmer þegar vara er úthlutuð á gáma, er nýjum gámi stofnað þar sem er nýtt vörunúmer. Þetta mun koma í veg fyrir að starfsmenn pakki úthlutunarlínum fyrir tvær mismunandi viðskiptavini í sama gám.  
10. Smellið á „Nýtt“.
11. Í reitnum tafla skal velja valkost.
12. Í reitinn velja Svæði skal slá inn eða veldu gildi.
13. Smellið á „Í lagi“.



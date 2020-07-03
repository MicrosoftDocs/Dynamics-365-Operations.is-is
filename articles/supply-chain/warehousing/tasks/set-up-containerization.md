---
title: Setja upp gámun
description: Þetta efni lýsir því hvernig á að gera sjálfvirka gámun á farm í vöruhúsakerfi
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d08b89ac32b8ec40ae9dff15dbbd3264800cfb1a
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454719"
---
# <a name="set-up-containerization"></a>Setja upp gámun

[!include [banner](../../includes/banner.md)]

Þetta efni lýsir því hvernig á að gera sjálfvirka gámun á farm í vöruhúsakerfi Sjálfvirk gámun stofnar gáma og tínsluvinnu fyrir sendingar þegar unnið er úr bylgju og hægt er að skipta upp vinnulínum í magn sem passa við gáma. Þetta hjálpar starfsmenn vöruhúss að taka til vörur beint í gám sem var valið. Borið saman við handvirkt pökkunarferli eru verk eins og stofnun gáma, úthluta vörum og lokunar gáma sjálfvirk af kerfinu. Þetta ferli notar USMF sýnifyrirtækið og er framkvæmt af stjórnanda Vöruhúsi.


## <a name="set-up-a-wave-template"></a>Velja bylgjusniðmát
1. Í skoðunarrúðunni ferðu í **Kerfi > Vöruhúsakerfi > Uppsetning > Bylgjur > Bylgjusniðmát**.
2. Veljið **Nýtt**.
3. Í reitnum **Heiti bylgjusniðmáts** skal slá inn gildi.
4. í reitnum **Lýsing bylgjusniðmáts** slærðu inn gildi.
5. Í reitnum **Svæði** slærðu inn eða velur gildi.
6. Í reitnum **Vöruhús** slærðu inn eða velur gildi.
7. Víkkið út hlutann **Aðferðir**. **Valdar aðferðir** svæðið skráir aðferðir fyrir valið bylgjusniðmát tegund. Bylgjusniðmátið verður að hafa með gámunar aðferð.  
8. Í reitinn **Bylgjuskrefakóði** færirðu inn gildi. Færið inn bylgjuskrefskóða fyrir viðbætta aðferð sem má vera hvaða kóði sem er. Hægt er að bæta við aðferð oftar en einu sinni og úthluta mismunandi kóðum fyrir bylgjuskref. Veljið **Endurtekin fyrir þennan aðferð** á síðu **aðferðir Bylgju ferli** til að gera þetta.  
9. Veljið **Vista**.
10. Lokið síðunni.

## <a name="set-up-a-container-type"></a>Setja upp gámagerð
1. Í skoðunarrúðunni ferðu í **Kerfi > Vöruhúsakerfi > Uppsetning > Gámar > Gámagerðir**. Hægt er að skilgreina gáma á síðunni **Gámagerðir**. Þú getur stillt efnisleg vídd gámanna, þar á meðal töruþungi, hámarks þyngd, hámarksrúmmál, lengd, breidd og hæð. Í þessu dæmi eru þrjár mismunandi stærðum kassar.  
2. Veljið **Nýtt**.
3. Í reitnum **Kóði gámagerðar** færirðu inn gildi.
4. Í reitnum **Umbúðaþyngd** skal slá inn tölu.
5. Í reitnum **Hámarksþyngd** skal slá inn tölu.
6. Í reitnum **Magn** skal slá inn tölu.
7. Í reitinn **Lengd** skal slá inn tölu.
8. Í reitinn **Breidd** skal slá inn tölu.
9. Í reitinn **Hæð** skal slá inn tölu.
10. Í reitinn **Lýsing** skal slá inn gildi.
11. Veljið **Vista**.
13. Endurtaktu skref 2-11 tvisvar í viðbót til að búa til þrjár heildar gerðir gáma.
14. Lokið síðunni.

## <a name="set-up-a-container-group"></a>Setja upp gámaflokk
1. Í skoðunarrúðunni ferðu í **Kerfi > Vöruhúsakerfi > Uppsetning > Gámar > Gámahópar**.
2. Í aðgerðarúðunni velurðu **Nýtt**. Þú getur sett upp rökrétta flokka af gámagerðum. Fyrir hvern hóp er hægt að tilgreinir í hvaða röð gámar eru pakkaðar og fyllingarhlutfall hvers gáms. Stærð vídda vörunnar er notuð til að ákvarða hvort hún passar í gám. Geymir sem er næst er afhendingardegi stærð vídda vörunnar er notað. Ef margar gámagerðum eru í flokki, er ráðlagt að hagræða röðinni eftir stærð, þannig að stærsta gámurinn er fyrst, númer 1 í röðinni og minnsti gámurinn er síðasta.    
3. Í **Auðkenni gámahóps** reitinn, sláðu inn gildi sem þú bjóst til fyrr.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Endurtaktu skref 2-4 fyrir allar þrjár gámategundirnar sem þú bjóst til áður.
6. Veljið **Vista**.
7. Lokið síðunni.

## <a name="set-up-a-container-build-template"></a>Setja upp gámaröðunarsniðmát
1. Í skoðunarrúðunni ferðu í **Kerfi > Vöruhúsakerfi > Uppsetning > Gámar > Gámaröðunarsniðmát**.
2. Veljið **Nýtt**. Gámaröðunarsniðmát byggist á hvaða gámunarferli eru framkvæmdar. Hver gámaröðunarsniðmát skilgreinir eina gámunarferli sem verða notuð af bylgjusniðmáti. **Breyta fyrirspurn** valkostur gerir kleift að skilgreina skilyrðin sem völdu sniðmáti er unnið úr. Til dæmis kannt þú að vilja keyra aðeins gámunarferli fyrir tiltekna viðskiptavini, vörur eða vöruhús eða þá að þú getur bætt viðkomandi fyrirspurn við sniðmátið. Svæðið **Bylgju skref kóði** er hvernig gámaröðunarsniðmát er tengd við skrefin í bylgjusniðmáti. Þegar framkvæmt er bylgju ákvarðar hún hvaða gámaröðunarsniðmát eru notaðar til að hefja gámun. Reitur grunngerð fyrirspurnar ákvarða hverju á að pakka og hvað á að miða síufyrirspurnina á. 
3. Í reitinn **Kenni gámasniðmáts** færiðu inn gildi.
4. Í reitinn **Kenni gámahóps** skal slá inn eða velja gildi.
5. Í reitinn **Bylgjuskrefakóði** færirðu inn gildi.
6. Veldu gátreitinn **Leyfa að skipta tiltekt**.
7. Veljið **Vista**.
8. Veljið **Blöndunartakmarkanir gáma**. Skipti í blöndunarrökum gerir kleift að setja upp reglur fyrir úthlutunarlínur í gáma. Til dæmis ef bætt er við svæðið **vörunúmer** þegar vara er úthlutuð á gáma, er nýjum gámi stofnað þar sem er nýtt vörunúmer. Þetta mun koma í veg fyrir að starfsmenn pakki úthlutunarlínum fyrir tvær mismunandi viðskiptavini í sama gám.  
9. Veljið **Nýtt**.
10. Í reitnum **Tafla** skal velja valkost.
11. Í reitinn **Velja reit** skal slá inn eða velja gildi.
12. Veljið **Í lagi**.


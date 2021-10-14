---
title: Skilgreina dæmi um bylgjuvinnslu
description: Þetta efnisatriði inniheldur dæmi um hvernig eigi að setja upp skilyrði sem ákvarða hvort bylgjur eru unnar handvirkt eða sjálfvirkt og vinnu sem er mynduð fyrir vöruhús þegar unnið er úr bylgju.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39c3fecf9250ee89c22003d5dff4ea662c3042e3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572986"
---
# <a name="configure-wave-processing-example"></a>Skilgreina dæmi um bylgjuvinnslu

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði inniheldur dæmi um hvernig eigi að setja upp skilyrði sem ákvarða hvort bylgjur eru unnar handvirkt eða sjálfvirkt og vinnu sem er mynduð fyrir vöruhús þegar unnið er úr bylgju. Tilgreina skal skilyrði með því að setja upp bylgjusniðmát og fyrirspurnir sem samsvara bylgju með losaðar línur í sölupantanir, framleiðslupantanir og kanban pantanir.

## <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér er nauðsynlegt að vera á kerfi þar sem venjuleg sýnigögn er sett upp. Þú verður einnig að velja lögaðilann **USMF** áður en þú byrjar.

## <a name="example-scenario-configure-wave-processing"></a>Dæmi um aðstæður: skilgreina bylgjuvinnslu

Þessar sýniaðstæður innihalda upplýsingar um margar þeirra stillinga sem hafa áhrif á það hvernig bylgjur eru búnar til, myndaðar, meðhöndlaðar og losaðar.

1. Farðu í **Skoðunarrúðu > Kerfi > Vöruhúsakerfi > Uppsetning > Bylgjur > Bylgjusniðmát**.
1. Veljið **Nýtt**.
1. Í reitnum **Heiti bylgjusniðmáts** skal slá inn gildi. Þegar sett er upp bylgjusniðmát er að tilgreina Röðina sem sniðmát eru samsvöruð við losuð lína á sölupantanir, framleiðslupantanir og kanbana. Þegar línu er losuð í vöruhús eða framleiðslu, notar hún fyrstu bylgjusniðmát sem hún uppfyllir skilyrði fyrir. Mælt er með því að setja sniðmát með nákvæmasta skilyrði efst á listanum. Því breiðara sem skilyrði er, því líklegra er fyrir línu til að uppfylla skilyrði, sem gæti leitt til að línur sé úthlutað á röng bylgju.  
1. í reitnum **Lýsing bylgjusniðmáts** slærðu inn gildi.
1. Í reitnum **Svæði** slærðu inn eða velur gildi. Ef verið er að nota USMF er hægt að velja svæði 2.  
1. Í reitnum **Vöruhús** slærðu inn eða velur gildi. Ef verið er að nota USMF er hægt að velja vöruhús 24.  
1. Stilltu reitinn **Gera stofnun bylgju sjálfvirka** á **Já**. Veljið þennan valkost til að stofna bylgju sjálfkrafa þegar sölupöntun, framleiðslupöntun eða kanban-losaðar í vöruhúsið.  
1. Stilltu valkostinn **Vinna úr bylgju við losun í vörugeymslu** á **Já**. Veljið þennan valkost til að vinna úr bylgjunni sjálfkrafa og stofna vinnu þegar lína er losuð í vöruhús.  
1. Stilltu valkostinn **Gera losun bylgju sjálfvirka** á **Já**. Veljið þennan valkost til að losa bylgju sjálfkrafa. Vinna tiltektarlista er stofnuð og í fartæki.  
1. Stilltu valkostinn **Úthluta á opnar bylgjur** á **Já**. Línur eru úthlutað til bylgjur á grundvelli fyrirspurnarsía fyrir bylgjusniðmát.  
1. Stilltu valkostinn **Vinna sjálfvirkt úr bylgjunni við þröskuld** á **Já**. Veljið þennan valkost til að vinna sjálfvirkt úr bylgjunni þegar hennar gildi nær þröskulda fyrir þyngd, sendingar, og línum sem tilgreind er í **Bylgjuþröskuldar** svæðisflokknum. Þessi valkostur er aðeins í boði ef **Sending** er valið í reitnum **Bylgjusniðmátsgerð**.  
1. Stilltu valkostinn **Gera áfyllingarvinnu sjálfvirka** á **Já**. Veljið þennan valkost til að stofna vinnu áfyllingar út frá eftirspurn og losa sjálfkrafa. Þú verður að bæta bylgjuaðferð áfyllingar við bylgjusniðmátið og stofna áfyllingarsniðmát með gerðina **Bylgjueftirspurn**.  
1. Notið stillingar í **Sjálfgildi** hópnum til að úthluta bylgjueiginleikum. Bylgjueigindir virka sem síur til að takmarka þær vörur sem geta notað bylgjuna. Til dæmis gætir þú tilgreint flokkvöru.  
1. Víkkið út **Aðferðir** hlutann og stillið aðgerðirnar sem bylgjusniðmátið tekur. Aðferðir bylgjusniðmáts gera þér kleift að stýra röð verkþátta sem hver bylgja fer í gegnum þegar hún er unnin. Til dæmis gæti verið til aðferð fyrir áfyllingu bylgja . Þegar þú bætir við aðferð er hún sjálfkrafa skráð í viðeigandi stað í röð af skrefum. Hafirðu stillt valkostinn **Útgefinn fyrir sjálfvirka áfyllingarvinnu** á **Já**, þarftu að bæta við áfyllingarmáta hér.  
1. Veljið **Vista**.
1. Lokið síðunni.
1. Farðu í **Vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis**.
1. Útvíkkaðu hlutann **Úrvinnsla bylgju**.
1. Í reitnum **Bylgjuúrvinnsla runuhóps** slærðu inn eða velur gildi.
1. Stilltu valkostinn **Vinna bylgjur í runu** á **Já**.
1. Í reitinn **Bið eftir lás (ms)** skal slá inn tölu. Færa inn þann tíma í millisekúndum sem úthlutun skref mun bíða þar til kerfið tilföng sem er læst af öðrum úthlutun skref. Þegar farið er yfir þennan tíma er ekki unnið úr bylgjunni og villuboð birtist.  
1. Veljið **Vista**.
1. Lokið síðunni.
1. Farðu í **Skoðunarrúða > Kerfi > Framleiðslustýring > Uppsetning > Færibreytur framleiðslustýringar**.
1. Í reitnum **Losa í vörugeymslu** skal velja valkost.

    Fyrir sölupantanir og kanbanpantanir verður að taka frá birgðir áður en pöntun er losuð í vöruhús. Annars eru vörur eða úthlutunarlínur ekki hægt að vinna í bylgju. Fyrir framleiðslupantanir, er einnig sá kostur tiltækur að velja **Leyfa hlutafrátekningu**. Til dæmis, er þetta hentugt ef efnin sem þarf til að hefja framleiðslu eru til staðar og geta beðið þar til viðbótar efni verða tiltækar til að klára ferlið. Ef þessi valkostur er valinn verður handvirkt að endurtaka losun í vöruhúsaferli þegar viðbótar efni verða tiltækar.
1. Lokið síðunni.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Stofnun og meðhöndlun bylgju](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

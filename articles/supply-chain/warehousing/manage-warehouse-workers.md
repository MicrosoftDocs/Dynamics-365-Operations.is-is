---
title: Stjórnun starfskrafta í vöruhúsi
description: Þessi skrá lýsir hvernig nota má vöruhúsaforrit til að aðstoða við stýringu og eftirlit með vinnu sem er framkvæmd af starfsmönnum í vöruhús.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage, WHSResetUserPassword
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8c3289ec049eeaa5a03b6cec02be85213c3bfa7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004526"
---
# <a name="manage-warehouse-workers"></a>Stjórnun starfskrafta í vöruhúsi

[!include [banner](../includes/banner.md)]

Þessi skrá lýsir hvernig nota má vöruhúsaforrit til að aðstoða við stýringu og eftirlit með vinnu sem er framkvæmd af starfsmönnum í vöruhús.

Ef verið er að nota virknina í vöruhúsastjórnun, eru allar aðgerðir starfsmanns í vöruhúsi vísað til sem *vinna*. Vinna t.d. tiltekt, flutningur, og Telja lagerbirgðir er skráð með því að nota fartæki. Áður en starfsmaður í vöruhús getur framkvæmt vinnu verður hann eða hún að vera tengdur við starfsmann í mannauði. Hver **Starfsmanns** lykill getur haft mörg vinnunotendur vöruhúss tengda. Þessir vinnunotendur getur unnið í mismunandi vöruhús og geta haft mismunandi aðgangsstig að ýmsum valmyndum fartækis. Þú getur líta á vinnunotendum vöruhúss sem margar innskráningar fyrir valinn starfsmann. Hver vinnunotanda hefur sjálfgefið vöruhús og tiltekin verkflæði eru birt af valmyndaratriðum sem eru tiltæk fyrir þann vinnunotanda. 

Til að stofna nýjan vinnunotanda á **Starfsmenn** síðunni á **Almennt** flipanum, á **Vöruhús** hlutanum, er smellt á **Starfsmanns**. Tilgreina verður Notandakenni og notandanafn, sjálfgefið vöruhús og nafn fyrir valmyndinni. Þessi valmynd er hlaðið þegar notandi skráir sig inn í Fartækjagátt Vöruhúss og gerir það mögulegt að skilgreina hvaða valmyndaratriði notandi hefur aðgang að. 

Sem Hluti af uppsetningu fyrir hvern vinnunotanda er einnig hægt að skilgreina verkflæði fyrir tiltekna vinnslu. Til dæmis er hægt að nota í **Er stjórnandi reglulegrar talningar** svæðið til að tilgreina hvort notandinn getur unnið leiðréttingu fyrir misræmi í reglulegri talningu við talningaraðgerð eða hvort þessar leiðréttingar verður fyrst að endurskoða af annar starfsmaður.

## <a name="defining-labor-standards"></a>Skilgreina vinnustaðla
**Vinnustöðlum** síðu gerir það mögulegt að skilgreina útreikningsaðferðir sem kerfið notar til að reikna út áætlaðan tíma sem þarfnast er fyrir tiltekna gerð vinnu. Hægt er að setja stilla þessa skilgreining á almennan hátt eða á ákveðnu stigi. Til dæmis hægt að tilgreina tíma sem á að vera nauðsynleg til að framkvæmta tiltekt á sölupöntun samkvæmt þyngd fyrir tiltekna skilgreiningu einingar þegar tiltekið tiltektarferli er notað. Á sama tíma er hægt að skrá tíma, byggt á annarri útreikningsaðferð, fyrir frágangsaðgerð fyrir lagerbirgðir sem teknar eru til. 

Til að virkja vinnustaðla sem hefur verið skilgreind, verður að velja **Leyfa vinnustaðla** valkost fyrir hvert vöruhús þar sem vinnustaðla verður notuð.

## <a name="monitoring-and-controlling-warehouse-work"></a>Fylgjast með og stýra vinnu í vöruhúsi.
**Alla vinnu** síðu gerir það mögulegt að fylgjast með og viðhalda alla vinnu sem er áætluð, í vinnslu og lokið. Úr þessari síðu er hægt að uppfæra mismunandi vinnslur eins og notandaúthlutun vinnu í vöruhúsi og forgang vinnu. Einnig er hægt að kafa niður í upplýsingar sem eru tengdar vinnuhaus og vinnulínum til að fá í skilning á áætluðu eða loknu vinnuferli. 

Ef þú virkjar **Vinnu stöðlum** valkost er hægt að sjá reiknaðan áætluðum tíma fyrir vinnu. Síðan, þegar unnið er úr vinnu verður rauntíma einnig sýnd fyrir hverja aðgerð vinnu. Á þennan hátt er hægt að bera saman áætlaðan tíma útreiknings við rauntíma. 

Þar að auki er hægt að nota áætlaðan tíma í reglum fyrir sjálfvirka skiptingu vinnu á meðan vinna er stofnuð. Á þennan hátt er hægt að hlaða vinnu með stöður, byggt á áætlaður tími til að ljúka verkunum. 

Greining á tíma sem er notuð til að vinna vinnuliði getur hjálpað við að knýja fram endurbætur á skilvirkni starfsmanna vöruhússins. eftirfarandi skýrsla eru tiltækar til að aðstoða við greininguna:

-   **Vinna eftir notanda** – Þetta sýnir framleiðni starfsmanns, byggt á raunverulegan tíma samanborið við áætluð tíma.
-   **Vinnu eftir vinnufærslugerð** – hægt er að nota þessa skýrslu til að rannsaka óhagkvæmni í tiltekið vöruhúsaferli. Til dæmis tekurðu eftir að tiltekt fyrir flutningspantanir taka lengri tíma í þessi vika en í fyrri vikur. Hægt er að nota þessar upplýsingar fyrir frekari athugunar.





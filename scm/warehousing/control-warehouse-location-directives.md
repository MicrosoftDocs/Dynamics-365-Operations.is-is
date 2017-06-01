---
title: "Stýra vöruhúsavinnu með vinnusniðmát og staðsetningarleiðbeiningar"
description: "Þessi skrá lýsir hvernig eigi að nota vinnusniðmát og staðsetningarleiðbeiningar til að ákvarða hvernig og hvar vinnu verður framkvæmd í vöruhúsinu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9d0ad4f64ee84da4e90dfa1525ebb5ff9fec4063
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Stýra vöruhúsavinnu með vinnusniðmát og staðsetningarleiðbeiningar

[!include[banner](../includes/banner.md)]


Þessi skrá lýsir hvernig eigi að nota vinnusniðmát og staðsetningarleiðbeiningar til að ákvarða hvernig og hvar vinnu verður framkvæmd í vöruhúsinu.

Leiðbeiningar sem starfsmenn vöruhúss fá í farsíma ákvarðast af sniðmát vinnu sem er sett upp í Microsoft Dynamics 365 for Operations til að skilgreina hin ýmsu vöruhúsaferli og verkefni. Vinnusniðmát ákvarða vinnuna fyrir hvert vöruhúsaferli. Með því að tengja staðsetningarleiðbeiningar við vinnusniðmát getur hjálpað að tryggja að vinna á sér stað á ákveðnum efnislegum svæðum vöruhúss.

## <a name="work-templates"></a>Vinnusniðmát
**Vinnusniðmát** síðu gerir það mögulegt að skilgreina vinnsluaðgerðir sem þarf að framkvæma í vöruhúsinu. Yfirleitt samanstanda vinnsluaðgerðir vöruhúss af aðgerðarpari: starfsmanns í vöruhúsi tekur til lagerbirgðir á einni staðsetningu og setur síðan tíndu birgðirnar niður á annarri staðsetningu. 

Vinnusniðmát samanstendur af haus og tengdar línur Hvert vinnusniðmát er fyrir tiltekna *gerð vinnupöntunar*. Margar gerðir vinnupöntunar tengjast upprunaskjöl, eins og innkaupa- eða sölupantanir. Hins vegar, aðrar gerðir vinnupöntunar standa fyrir aðskilin vöruhúsaferli, eins og reglulega talningu. *kenni vinnuhópa* leyfir þér að skipuleggja vinnu í flokka. 

stillingarnar í skilgreiningu vinnuhauss má nota til að ákvarða þegar á að stofna nýja vinnu. Til dæmis er hægt að setja inn hámarksfjölda tiltektarlína og hámark áætlaðs tínslutíma. Svo ef vinnu fyrir tiltektarferli sölupöntunar fer fram yfir annaðhvort þessara gilda, er þeirri vinnu skipt í tvær einingar vinnu. 

Vinnulínum tákna efnislega verkin sem nauðsynleg eru til að vinna úr vinnunni. Til dæmis, fyrir vöruhúsaferli á útleið, gæti verið vinnulína til að taka til vörur innan vöruhús og aðra línu til að setja þær vörur yfir í sviðsetningarsvæðið. Svo getur verið til viðbótar lína til að taka til vörur frá sviðsetningu, og aðra línu fyrir setja vörurnar í vörubíl sem hluti af ferlinu við að hlaða. Hægt er að setja inn *leiðbeiningarkóði * á línum vinnusniðmáts. leiðbeiningakóða er tengd staðsetningarleiðbeiningar og þar af leiðandi hjálpar til við að tryggja að vöruhúsavinna er unnin á réttum stað í vöruhúsinu. 

Hægt er að setja upp fyrirspurn til að stýra hvenær tiltekna vinnusniðmátið er notað. Til dæmis er hægt að setja takmörkun þannig að hægt er að nota tiltekið sniðmát fyrir vinnu eingöngu í ákveðnu vöruhúsi. Einnig gætirðu haft nokkur sniðmát sem eru notaðar til að stofna vinnu sölupöntunarferli á útleið , eftir uppruna sölu. Kerfið notar **Raðnúmer** svæði til að ákvarða röð tiltæk  vinnusniðmát eru metin í. Þess vegna, ef þú ert með mjög nákvæma fyrirspurn fyrir tiltekið vinnusniðmát , ætti að gefa því lágt raðnúmer. Sú Fyrirspurn verður síðan metnar á undan aðrar, almennari fyrirspurnir. 

Til að stöðva eða gera hlé á vinnuferli, geturðu notað að **Stöðva vinnu** stillingu á vinnulínunni. Í því tilfelli fær starfsmaður sem framkvæmir vinnuna ekki beiðnir um að framkvæma næsta vinnulínuskref. Til að fara í næsta skref, þarf sá starfsmaður eða annars starfsmanns að velja vinnuna aftur. Hægt er að aðskilja verk innan með vinnueiningar með því að nota annað *kenni vinnuklasa*á línum vinnusniðmáts.

## <a name="location-directives"></a>Staðsetningarleiðbeiningar
Staðsetningarleiðbeiningar eru reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar. Til dæmis, í sölupöntunarfærslu, ákvarða staðsetningarleiðbeiningar hvar vörurnar verða teknar til og hvar tilteknar vörur verða að setja. Staðsetningarleiðbeiningar samanstanda af haus tengdar línur, og þær eru stofnaðar á **staðsetningarleiðbeiningar** síðu. 

Í haus verður hver staðsetningarleiðbeining að vera tengd við *gerð verkpöntunar * sem tilgreinir gerð birgðafærslu sem leiðbeiningarnar verður notuð fyrir, eins og sölupantanir, áfyllingu eða tiltekt hráefnis. *vinnutegund* tilgreinir hvort staðsetningarleiðbeininga verður notuð fyrir tiltekt eða setja, eða fyrir eitthvað annað vöruhúsaferli, eins og talningu eða birgðastöðubreytingu. Einnig þarf að tilgreina *svæði * og *vöruhús*. *leiðbeiningarkóði *sem þú tilgreina í haus er hægt að nota til að tengja staðsetningarleiðbeiningu við eitt eða fleiri vinnusniðmát . 

Eins og fyrir Vinnusniðmát, er hægt er að setja upp fyrirspurn til að ákvarða hvenær tiltekna staðsetningarleiðbeiningar er notað. Til dæmis er hægt að tilgreina að þegar e-commerce er uppruni sölupöntunar,  verður að taka birgðir frá sérstöku svæði í vöruhúsinu. Kerfið notar **Raðnúmer** svæði til að ákvarða röð tiltækar staðsetningarleiðbeiningar eru metnar í. 

Línur staðsetningarleiðbeiningar setja frekari takmarkanir á notkun staðsetningaleitarreglna. Hægt er að tilgreina lágmarksmagn og hámarksmagnið sem á við leiðbeiningarnar eiga að gilda um, og hægt er að tilgreina að leiðbeiningarnar eigi að vera fyrir tiltekna birgðaeiningu. Til dæmis, ef mælieiningin er bretti þá er hægt að setja vörur í brettum á tilteknum stað. Einnig er hægt að tilgreina hvort magnið sé hægt að skipta á mörgum staðsetningar. Líkt og staðsetningarleiðbeiningar haus, hver lína staðsetningarleiðbeiningar hefur raðnúmer sem ákvarðar röð sem línurnar eru metnar í. 

Staðsetningarleiðbeiningar hafa eina viðbótar upplýsingastig: *aðgerðir í staðsetningarleiðbeiningum*. Hægt er að skilgreina margar aðgerðir í staðsetningarleiðbeiningum fyrir hverja línu. Einu sinni enn, númeraröð er notuð til að ákvarða röðun sem aðgerðir eru metnar í. Á þessu stigi er hægt að setja upp fyrirspurn til að skilgreina hvernig á að finna bestu staðsetningu í vöruhúsinu. Einnig er hægt að nota forskilgreint **Stjórnunarstefnu**stillingar til að finna bestu staðsetningu.

### <a name="example-of-the-use-of-location-directives"></a>Dæmi um notkun staðsetningarleiðbeiningar

Í þessu dæmi hugsum við um innkaupapöntunarferli þar sem staðsetningarleiðbeiningar verða að finna lausa afkastagetu í vöruhúsi fyrir birgðavara sem hafa einungis verið skráð í móttökusvæðinu. Fyrst reynum við að finna lausa afkastagetu innan vöruhúss með sameiningu við fyrirliggjandi lagerbirgðir. Ef Sameining er ekki möguleg, viljum við finna tóma staðsetningu. 

Fyrir þessar aðstæður verður að skilgreina tvær aðgerðir í staðsetningarleiðbeiningum. Fyrsta aðgerð í röðinni verður að nota í **Sameina** stjórnunarstefnu og annar ætti að nota í **Autt staðsetning með engu verki á innleið** stjórnunarstefnu. Nema við skilgreinum þriðja aðgerð til að meðhöndla aðstæður yfirflæðis , eru tveimur niðurstöður mögulegar þegar engar frekari afkastagetu er í vöruhúsinu: hægt er að stofna vinnu jafnvel þótt engin staðsetningar eru skilgreindir eða ferli verkstofnunar getur mistekist. Niðurstaðan er ákvarðaður með uppsetningu á **staðsetningarleiðbeiningum** síðuna,  þar sem hægt er að ákveða hvort að velja **Stöðva vinnu á misheppnuðum staðsetningarleiðbeiningum** valkost fyrir hverja gerð vinnupöntunar.





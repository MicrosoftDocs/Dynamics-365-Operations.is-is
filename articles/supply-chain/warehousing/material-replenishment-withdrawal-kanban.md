---
title: Áfylling með afturkölluðum kanban
description: Í þessari grein er lýst hvernig afturköllunartafla er notuð fyrir áfyllingu efnis fyrir framleiðsluaðgerðir.
author: perlynne
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 517b2eeb3b218fe0820ffa4e1d19b20841837b92
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863709"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>Áfylling með afturkölluðum kanban

[!include [banner](../includes/banner.md)]

Í þessari grein er lýst hvernig afturköllunartafla er notuð fyrir áfyllingu efnis fyrir framleiðsluaðgerðir.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Verkflæði fyrir áfyllingu hráefnis sem notast við kanban-úttekt

Nota má kanban-úttekt til að færa kanban einnar vöru á milli vöruhúsa og afurðastaðsetninga þar sem hráefnið er notað. Kanban-úttekt styður dráttarlausnir fyrir áfyllingu hráefnis, þar sem dráttarmerki er nauðsynlegt til að setja af stað framboð fyrir tiltekna eftirspurn. 

Eftirfarandi dæmi sýnir dráttaráfyllingarkerfi þar sem dráttarkerfi setur af stað stofnun á kanban til áfyllingar á hráefni fyrir framleiðsluferli. 

[![Togmerki ræsir stofnun á kanban til að fylla á efni fyrir framleiðsluferli.](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Kanban úttektar
2.  Kanban „frá“ staðsetningu og frágangsstaðsetningu fyrir vöruhúsavinnu
3.  Kanban „til“ staðsetningar og inntaksstaðsetningar framleiðslu
4.  Framleiðsluferli
5.  Vöruhúsavinna fyrir kanban-tínslu
6.  Vöruhúsastaðsetningar fyrir hráefni
7.  Hráefnisvöruhús
8.  Framleiðsluvöruhús

Í þessu tilfelli notar framleiðsluferli (4) hráefni úr staðsetningu framleiðsluinntaks (3) í framleiðsluvöruhúsi (8). Þegar afgreiðslueining af hráefninu (kanban) er notuð, er hún skráð sem tóm. Áfyllingarmerki er stofnað fyrir uppruna vörunnar og nýtt kanban (1) er stofnað. Í þessu tilfelli samanstendur uppruni vöru af staðsetningum í efnisvöruhúsi (7). Efni fyrir kanban er tekið til og sett í staðsetningu (2) í sama vöruhúsi. Þegar efnið er tekið til, er það tilbúið fyrir flutning úr staðsetningu 2 í staðsetningu framleiðsluinntaks (3) í framleiðsluvöruhúsi (8).

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Skilgreining vöruhúsavinnu fyrir tínslu á kanban fyrir kanban-úttekt

Til að virkja tínsluleið hráefnis fyrir kanban-úttekt skal stilla bylgjusmiðmát og staðsetningarleiðbeiningar fyrir vinnupöntunargerðina **Kanban-tiltekt**. Þessi gerð vinnupöntunar styður ekki bara við tiltektarferli fyrir kanban-úttekt. Hún styður einnig við tiltektarferlið fyrir kanban-framleiðslu. Hins vegar er hægt að skilgreina sérstakt tiltektarferli fyrir hverja gerð kanban með því að aðgreina bylgjusniðmát, vinnusniðmát og staðsetningarleiðbeiningar. Til að aðgreina bylgjusniðmát, vinnusniðmát og staðsetningarleiðbeiningar skal stilla viðmiðun á aðgerðartegundina (**Ferli** eða **Flytja**) í fyrirspurnum fyrir þær einingar.

## <a name="configure-the-withdrawal-kanban"></a>Skilgreina kanban-úttekt

Flutningsverkþátturinn sem er notaður fyrir kanban-úttekt er skilgreindur sem hluti af virkjaðri verkþáttaáætlun í lean-framleiðsluflæðinu. Þú tilgreinir „frá“ og „til“ staðsetningar fyrir flutninginn, sem hluta af skilgreiningu flutningsverkþáttarins. Þegar þú hefur skilgreint flutningsverkþáttinn getur þú úthlutað honum til kanban-reglu af tegundinni **Úttekt**. Kanban-reglan setur stefnur og skilgreiningar fyrir kanban-úttekt. Magn í kanban skilgreinir hversu margar einingar af afgreiðslueiningu kanban ber í flutningsferlinu. Fasta kanban-magnið er notað þegar áætlunin Föst áfylling er valin. Þetta magn tilgreinir hversu mörg kanban þarf til að koma í veg fyrir birgðaþrot þegar eftirspurn verður. Hægt er að reikna fast magn á grundvelli raunverulegrar eftirspurnar, sögulegrar eftirspurnar og þjónustustigs. Eftirfarandi tvö dæmi lýsa því hvernig hægt er að stjórna áfyllingu hráefnis sem notast við kanban-úttekt.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>Dæmi 1: Fylltu á staðsetningu framleiðsluinntaks með því að nota fasta kanban-úttekt

Framleiðsluferli notast við keypt hráefni úr staðsetningu framleiðsluinntaks sem er í framleiðsluvöruhúsi. Þegar hráefni er móttekið frá lánardrottni er það geymt í staðsetningum í efnisvöruhúsi. Þar sem eftirspurn eftir efni telst vera stöðug yfir tíma er hún sett upp þannig að hún leggi framleiðslunni til efni í föstu flæði kanban-úttektar. Þegar kanban er notað í staðsetningu framleiðsluinntaks er autt merki skráð og nýju kanban af sömu gerð er bætt við flæðið. 

Hægt er að skilgreina autt merki þannig að það verði til sjálfkrafa þegar kanban er lokið. Einnig er hægt að setja upp autt merki sem handvirkt inngrip sem kemur annaðhvort frá flutningstöflu kanban eða úr valmynd lófatækis. Flutningstafla kanbans er vinnusvæðið þar sem öllum aðgerðum á líftíma kanban er stýrt. 

Þegar kanban er stofnað er bylgjulínu fyrir hráefnið bætt við kanban-bylgju fyrir efnisvöruhúsið. Í tiltektarlistahluta fluningstöflu kanbans er hægt að fylgjast með stöðu efnis og tengdra vöruhúsaferla úr bylgjustofnun í vinnustofnun, allt þar til efnið er tiltækt í staðsetningunni „flytja úr“ og er tilbúið til flutnings í staðsetningu framleiðsluinntaks. Hægt er ljúka við kanban, annaðhvort úr flutningstöflu kanbans eða úr valmynd í lófatækinu. 

Í þessu tilfelli er tiltektarvinna í efnisvöruhúsi unnin sem einn verkþáttur. Flutningsverkþátturinn milli efnisvöruhúss og framleiðsluvöruhúss er unninn sem sérstakur verkþáttur. Þessi aðferð getur verið gagnleg ef það er til dæmis mikil efnisleg fjarlægð milli vöruhúsanna tveggja. Í þessu tilfelli getur flutningsverkþáttur kanbans verið vörubílsfarmur. 

Ef fjarlægðin milli vöruhúsastaðsetninga og staðsetningar framleiðsluinntaks er lítil, gæti verið skilvirkara að hafa flutningsverkþáttinn með í tiltektarferlinu. Eftir að efni er tekið til er síðan hægt að setja það beint í staðsetningu framleiðsluinntaks. Til að styðja við þetta ferli getur þú skilgreint flutningsverkþáttinn þannig að honum sé sjálfkrafa lokið þegar tiltektarvinna kanban-úttektar er unnin.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>Dæmi 2: Flutningsverkþætti er sjálfkrafa lokið þegar tiltektarvinna kanbans er yfirstaðin

Í eftirfarandi dæmi er flutningsverkþáttur kanban-úttektar skilgreindur þannig að hann flytjist milli tveggja staðsetninga í sama vöruhúsinu. Flutningsverkþáttur kanban-úttektar er settur þannig upp að honum sé lokið sjálfkrafa. 

[![Flutningsverkþáttur er sjálfkrafa lokið þegar unnið er úr kanban-tiltekt.](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Samnýtt vöruhús fyrir hráefni og framleiðslu
2.  Vöruhúsastaðsetningar fyrir hráefni
3.  Kanban „frá“ staðsetningu og frágangsstaðsetningu fyrir vöruhúsavinnu
4.  Kanban úttektar
5.  Staðsetning framleiðsluinntaks
6.  Framleiðsluferli

Eftir að kanban er notað í staðsetningu framleiðsluinntaks er kanban skráð sem autt og nýju kanban af sömu gerð er bætt við flæðið. Þegar kanban er stofnað er bylgjulínu bætt við kanban-bylgju. Þegar kanban-bylgja er yfirstaðin er vöruhúsavinna fyrir kanban-tiltekt stofnuð. Starfsmaður vöruhússins lýkur vinnu fyrir kanban-tiltekt og verkið segir honum að tína efnið fyrir kanban í vöruhúsastaðsetningu. Þegar þessi starfsmaður vöruhússins staðfestir tiltektina er kanban sjálfkrafa stofnað og starfsmanninum er sagt að setja efnið í staðsetningu framleiðsluinntaks.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
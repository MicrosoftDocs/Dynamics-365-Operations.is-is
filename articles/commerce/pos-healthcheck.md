---
title: Heilbrigðiseftirlit með POS jaðartæki og þjónustu
description: Þessi grein veitir yfirlit yfir heilsufarsskoðun á sölustað (POS).
author: BrianShook
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 44fd4b6246d3d7947527416c2b8b447bd64f179f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863322"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>Heilbrigðiseftirlit með POS jaðartæki og þjónustu

[!include [banner](includes/banner.md)]

Þessi grein lýsir heilsuskoðunaraðgerðum á sölustað (POS).

## <a name="overview"></a>Yfirlit

Smásöluverslanir geta verið flókið umhverfi þar sem mörg forrit og tæki eru notuð. Eftir því sem aðgerðir vaxa getur það reynst erfitt að tryggja að aðgerðir gangi alltaf vel, vegna háðs til dæmis jaðartækja sem geta brotnað eða óvart verið tengd yfir daginn. Úrræðaleit vegna vandamála sem tengjast tækjum og þjónustu getur verið dýrt fyrir stærri söluaðila og jafn pirrandi fyrir minni aðgerðir.

Microsoft Dynamics 365 Commerce útgáfur 10.0.10 og nýrri innihalda ástandsskoðunaraðgerð sem getur hjálpað við að koma í veg fyrir einhvern af þessum kostnaði og gremju. Þessi aðgerð veitir aðferð til að prófa tæki beint úr POS utan venjulegra aðgerða. Þess vegna getur það hjálpað smásöluaðilum að greina mál áður en þau koma upp.

## <a name="key-terms"></a>Lykilhugtök

| Hugtak | lýsing |
|---|---|
| Jaðarbúnaður | Öll tæki sem POS forritið notar til að auðvelda færslur og aðrar aðgerðir í versluninni. Sem dæmi má nefna peningaskúffur, strikamerkjaskanna og afgreiðslustöðvar. |
| Þjónusta | Í þessari grein er þjónusta aukaforrit sem POS forritið er háð til að framkvæma viðskipti og daglega rekstur. Sem dæmi má nefna forrit sem hjálpa til við útreikninga skatta eða flutninga. |

## <a name="health-check-operation"></a>Aðgerð við ástandsskoðun

Aðgerð ástandsskoðunar er aðgerð 717 á síðunni **Aðgerðir í POS** í Commerce Headquarters. Hana er hægt að nota á meðan POS er ekki í skúffu. Samt sem áður verður vélbúnaðarstöð að vera virk.

Sjálfgefið er að ástandsskoðunin prófar aðeins tæki sem eru stillt á vélbúnaðar prófílnum fyrir vélbúnaðarstöðina sem er nú virk fyrir skrá. Ef skrá notar margar vélbúnaðarstöðvar yfir einn dag, til að gera ástandsskoðanir fyrir þær allar verður hún að tengjast einni vélbúnaðarstöð í einu. Það er engin ástandsskoðun í versluninni. Hins vegar er mögulegt að hægt sé að gera þessa tegund af skoðun með stækkanleika Commerce Server.

### <a name="out-of-box-health-checks"></a>Tilbúnar ástandsskoðanir

| Gerð | Tenging | Upplýsingar |
|---|---|---|
| Prentari | OPOS | Þessi athugun prófar grunntengingu og innfellingu fyrir POS (OPOS) aðgerðir. Hér eru nokkur dæmi:<ul><li>Opna: **Opna** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Loka: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Loka**</li></ul> |
| Línuskjár | OPOS | Þessi athugun prófar grunn OPOS aðgerðir. Hér eru nokkur dæmi:<ul><li>Opna: **Opna** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Loka: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Loka**</li></ul> |
| Tvískiptur skjár | Gluggar | Þessi athugun tryggir að stýrikerfið finnur annan Windows skjá. | 
| MSR | OPOS | Þessi athugun prófar grunn OPOS aðgerðir. Hér eru nokkur dæmi:<ul><li>Opna: **Opna** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Loka: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Loka**</li></ul> |
| Skúffa | OPOS | Þessi athugun prófar grunn OPOS aðgerðir. Hér eru nokkur dæmi:<ul><li>Opna: **Opna** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Loka: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Loka**</li></ul> | 
| Skanni | OPOS | Þessi athugun prófar grunn OPOS aðgerðir. Hér eru nokkur dæmi:<ul><li>Opna: **Opna** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Loka: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Loka**</li></ul> | 
| Vigt | OPOS | Þessi athugun prófar grunn OPOS aðgerðir. Hér eru nokkur dæmi:<ul><li>Opna: **Opna** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Loka: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Loka**</li></ul> |
| PIN-takkaborð | OPOS | Þessi athugun prófar grunn OPOS aðgerðir. Hér eru nokkur dæmi:<ul><li>Opna: **Opna** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Loka: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Loka**</li></ul> |
| Greiðslustöð | SDK-greiðslur | Þessi athugun prófar grundvallar aðgerðir greiðslumiðstöðvar sem gefnar eru af SDK fyrir greiðslur. <ul><li>Læsing</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Lok</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>Notkun heilbrigðiseftirlitsaðgerðarinnar í POS

Þegar aðgerð við heilbrigðiseftirlit er hafin í POS birtir rúðan til hægri lista yfir uppsett tæki og sýnir stöðu hvers búnaðar. Til að gera heilbrigðiseftirlit með einu tæki, veldu tækið og veldu síðan **Próf valið**. Veldu til að gera heilsufarsskoðun á öllum tækjum **Prófa allt**. Virknin **Prófa allt** prófar öll tækin, í einu og uppfærir stöðu hvers tækis í dálkinum **Staða**.

Dálkurinn **Síðasta skoðun** sýnir hvenær ástandsskoðun var síðast gerð fyrir hvert tæki.

Ef ástandsskoðun tækis fer fram (það er að segja ef engar villur verða vart) verður staða tækisins **Í lagi**. Ef ástandsskoðunin mistekst bendir staðan til þess að um villu hafi verið að ræða. Í þessu tilfelli veitir rúðan til hægri upplýsingar sem tengjast villunni, eða það leiðbeinir notandanum að hafa samband við kerfisstjórann.

Sum tæki, svo sem OPOS takkalásinn, hafa ekki prófanir úr ástandsskoðunum. Ef ástandsskoðun er ekki fundin fyrir tæki sem notað er verður staðan **Ekki stutt**.

### <a name="extending-health-checks"></a>Útvíkkun ástandsskoðunar

Tilbúnar prófanir ástandsskoðana eru sett upp til að veita notendavæn skilaboð vegna dæmigerðra villna. Ekki er þó fjallað um allar sviðsmyndir. Með stækkun geta söluaðilar kortlagt notendavænt skilaboð að villum sem gætu verið sértækar fyrir umhverfi sitt.

Sérsniðnar ástandsskoðanir er einnig hægt að búa til til að prófa tæki sem ekki eru studd úr kassanum, eða til að prófa þjónustu sem POS fer eftir.

## <a name="related-articles"></a>Tengdar greinar

[Kveikjur og prentun í Modern POS (MPOS)](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Útboðsbundin afsláttur
description: Þessi grein lýsir tilboðsbundinni afsláttarvirkni sem gerir smásöluaðilum kleift að stilla afslátt fyrir tilteknar útboðsgerðir í Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: 3c28297e62e5b2880a7a39381702d5a1448c91ac
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337231"
---
# <a name="tender-based-discount"></a>Útboðsbundinn afsláttur

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein lýsir tilboðsbundinni afsláttarvirkni sem gerir smásöluaðilum kleift að stilla afslátt fyrir tilteknar útboðsgerðir í Microsoft Dynamics 365 Commerce.

Það er algengt hjá smásöluaðilum að gefa út einkakennd kreditkort. Söluaðilarnir njóta góðs af því að þeir fá valinn vexti frá bönkunum. Þar að auki, vegna þess að þessi kreditkort geta hvatt viðskiptavini til að heimsækja verslunina oftar, hjálpa þau til við að bæta niðurstöðulínu verslunarinnar. Þess vegna hafa smásalar hvata til að auka notkun viðskiptavina á vörumerkjakreditkortunum sínum. Til að ná þessu markmiði veita þeir oft frekari afslátt til viðskiptavina sem nota þessi kreditkort.

Að öðrum kosti gætu smásalar sem ekki bjóða upp á vörumerkt kreditkort viljað hvetja viðskiptavini til að greiða með því að nota aðrar útboðsgerðir, svo sem reiðufé, gjafakort eða vildarpunkta. Með þessum hætti geta þeir hjálpað til við að draga úr kostnaði við afgreiðslugjöld kreditkorta. Þess vegna gætu smásalar veitt afslátt til viðskiptavina sem nota þessar aðrar útboðsgerðir.

## <a name="tender-based-discount"></a>Útboðsbundinn afsláttur

Verslun styður a *útboðsbundinn afsláttur* að við skulum smásalar stilla afsláttarprósentu sem er notuð á færslu ef heildarfjölda færslu fer yfir tiltekna upphæð og viðskiptavinurinn greiðir með því að nota valinn greiðslutegund. Útboðsbundinn afsláttur er þrepamiðaður, þannig að mismunandi afsláttarprósentur geta tengst mismunandi upphæðarmörkum. Viðskiptavinurinn getur ákveðið hvort hann greiðir að hluta eða fullri greiðslu og verðlagningarvélin ákvarðar viðeigandi afsláttarupphæð. Útboðsbundinn afsláttur er ávallt gefinn af upphæð sölulínanna fyrir skatta.

Útboðsbundinn afsláttur er aðeins hægt að nota á sölulínur þar sem verð eru ekki læst og honum er dreift hlutfallslega á hæfu línurnar. Ef nýjum sölulínum er bætt við pöntun er útboðsbundinn afsláttur aðeins lagður á nýju sölulínurnar meðan á greiðslu stendur. Þegar pöntun viðskiptavinar til afhendingar eða afhendingar er lögð inn, er tilboðsbundinn afsláttur aðeins lagður á innborgunarupphæðina. Eftir að pöntunin hefur verið gerð, meðan á uppfyllingu stendur, eru verð á sölulínunum læst. Enginn útboðsbundinn afsláttur er notaður á eftirstöðvar sem eru greiddar við afhendingu eða heimilaðar við sendingu. Útboðsbundnum afslætti er aðeins hægt að beita á alla upphæð viðskiptavinapöntunar ef smásalinn innheimtir alla upphæðina sem innborgun meðan pöntunin er gerð.

Útboðsbundnir afslættir keppa ekki við vöruafslátt eins og einfalda afslætti, magnafslátt, viðmiðunarafslátt, blanda afslætti og handvirkan afslátt. Útboðsbundnir afslættir eru alltaf samsettir yfir vöruafslætti. Þess vegna, jafnvel þótt einkaafsláttur sé veittur á vöru, er enn hægt að leggja tilboðsbundinn afslátt ofan á einkaafsláttinn. Sömuleiðis, ef þröskuldarafslætti er beitt á færsluna og útboðsbundinn afsláttur lækkar samtöluna undir viðmiðunarmörk, er þröskuldafslætti enn beitt á færsluna.

Jafnvel þó að útboðsbundnir afslættir dragi úr undirsamtölu færslu, hafa sjálfvirk gjöld sem eru lögð á færsluna ekki áhrif. Til dæmis, ef afhendingargjöld eru reiknuð sem $5 vegna þess að meðaltalan var meiri en $100, og tilboðsbundinn afsláttur lækkar upphæðina þannig að hún er lægri en $100, verða sendingargjöldin áfram $5 fyrir pöntunina.

Útboðsbundinn afsláttur er eins og er takmarkaður við tvær greiðslutegundir: kreditkort og reiðufé. Ef margir tilboðsbundnir afslættir eru stilltir fyrir greiðslutegund er aðeins besti tilboðsbundinn afslátturinn notaður.

## <a name="pos-user-experience"></a>Notandareynsla POS

Ef útboðsbundinn afsláttur er settur upp fyrir reiðufé og gjaldkeri á sölustað (POS) velur **Borga reiðufé** hnappinn til að tékka á reiðufé og bera færslu, útboðsbundinn afsláttur er sjálfkrafa settur á færsluna. Minni upphæðin er síðan sýnd sem staða. Hins vegar, ef gjaldkerinn velur hnappinn **Til baka** á greiðsluskjánum er afslátturinn fjarlægður og upphafleg upphæð er sýnd á viðskiptaskjánum. Útboðsbundinn afsláttur er fjarlægður ef greiðslulínan er ógild.

Fyrir kreditkortagreiðslur geta smásalar sett útboðsbundinn afslátt á einni eða fleiri gerðum kreditkorta. Hins vegar getur kerfið ekki staðfest þá tegund kreditkorta sem er notuð nema kortið sé heimilað. Ef afslátturinn er notaður eftir heimild verður greiðsluheimildin fyrir stærri upphæð en greiðsluöflunin er fyrir minni upphæð. Til að koma í veg fyrir þetta ástand, ef viðskiptavinur greiðir með kreditkorti, er gjaldkeri beðinn um svarglugga sem sýnir öll valin kreditkort sem gefa viðskiptavinum aukaafslátt. Gjaldkeri getur síðan spurt hvort viðskiptavinurinn vilji nota eitt af völdu kortunum til að fá viðbótarafslátt. Ef gjaldkeri velur ákjósanlegt kort er tilboðsbundinn afsláttur settur á færsluna og lækkaða upphæðin birtist á greiðsluskjánum. Heimildin verður fyrir lægri fjárhæð. Ef viðskiptavinurinn setur inn kort sem er frábrugðið kortinu sem gjaldkerinn valdi, birtast villuboð og heimildin fellur úr gildi.

## <a name="call-center-user-experience"></a>Reynsla af símaþjónustuverum

Ef notandi símaversins velur **Heill** meðan á pöntun í símaveri stendur, **Samtals** skjárinn birtist. Til að byrja með eru heildartölurnar á þessum skjá ekki með afslætti sem byggir á útboðum því greiðslumátinn hefur ekki enn verið valinn. Á skjánum **Bæta við greiðslu**, ef notandinn velur greiðslumáta sem útboðsbundinn afsláttur er stilltur fyrir, er greiðslufjárhæðin sjálfkrafa leiðrétt þannig að hún endurspeglar upphæð með afslætti. Eins og viðskiptavinur í POS getur viðskiptavinur símaversins ákveðið hvort hann greiðir fulla greiðslu eða hlutagreiðslu. Miðað við fjárhæðina sem er greidd er útboðsbundnum afslætti beitt á sölupöntunina.

> [!NOTE]
> Staðfesting korta er ekki gerð fyrir pantanir í símaþjónustuver. Til dæmis, ef notandi símaþjónustunnar velur Visa sem kreditkort, en viðskiptavinurinn notar Mastercard, beitir kerfið afslættinum samt sem áður.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Aðgerðir sölustaðar (POS) með og án nettengingar
description: Þetta efnisatriði veitir upplýsingar um rekstur sölustaðs (POS) í Microsoft Dynamics 365 for Retail. Það tilgreinir hvar í forritinu má kalla fram aðgerðir og hvort þær séu tiltæk í ótengdum ham.
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44a2ec48f868c803c80c8df8eb809bc2254e63da
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505097"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Aðgerðir sölustaðar (POS) með og án nettengingar

[!include [banner](includes/banner.md)]

Flestar gjörðir sem notandi framkvæmir á sölustað (POS) eru taldar aðgerðir. Aðgerðir eru skilgreindar og þeim stjórnað í bakvinnslu Microsoft Dynamics 365 for Retail. Hægt er að bæta mörgum aðgerðum við takka í POS hnappakerfinu. Notendur geta síðan valið hnappana til að kalla fram aðgerðir og framkvæma virkni þeirra. Aðrar aðgerðir er hluti af aðal POS forritinu og kallaðar fram annaðhvort úr hnöppum á skjánum eða sem hluti af öðrum verkflæði eða ferlum.

Eftirfarandi tafla veitir upplýsingar um aðgerðir sem eru í boði í Retail Modern POS og Cloud POS fyrir Dynamics 365 for Retail. Taflan tilgreinir einnig hvar í forritinu má kalla fram aðgerðir og hvort þær séu tiltækar þegar POS er í ótengdum ham.

Sumar aðgerðir eru ekki í boði eins og er í Retail Modern POS eða Cloud POS fyrir Dynamics 365 for Retail. Sumar þessara aðgerða eru aðgerðir sem taka sérstaklega mið af staðsetningu og krefjast viðbótar viðbóta og skilgreininga. Aðrar aðgerðir eru eiginleikar frá Microsoft Dynamics AX 2012 sem ekki eru studdir eins og er.

Eftirfarandi dálkar tilgreina hvar hægt er að kalla fram aðgerðirnar:

- **Hnappahnit** – Aðgerðinni er hægt að úthluta til hnappa í POS hnappahnitum, sem eru hluti af POS skjár útliti.
- **Færsluskjár** – Hægt er að kalla fram aðgerðina frá POS hnappahnitum sem eru skilgreind á POS færsluskjánum.
- **Velkomin skjár** – Hægt er að kalla fram aðgerðina frá POS hnappahnitum sem eru skilgreind á POS velkomin skjánum.

> [!NOTE]
> Aðgerðirnar sem taldar eru upp hér að neðan eiga við um nýjustu útgáfuna af Dynamics 365 for Retail. Sumar aðgerðir kunna að hafa breyst eða kunna ekki að vera í boði í fyrri útgáfum.

| KENNI | Aðgerð | lýsing | Hnappahnit | Færsluskjár | Upphafsskjár | Tiltæk utan nets | Tekur sérstaklega mið af staðsetningu |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Gera tæki virkt | Virkjaðu núverandi tæki með því að leyfa sannvottuðum notanda að veita upplýsingar um tengingu og úthluta tæki og skráa auðkenni. | Númer | Númer | Númer | Númer | Númer |
| 134 | Bæta við fyrirtækjatengslum | Bæta við forvalinni tengingu við færslu. Veljið tengsl á **Eiginleikar hnapps** síðunni. | Já | Já | Númer | Já | Númer |
| 135 | Bæta við tengslum úr lista | Bæta tengslum við færslu með því að velja í lista. | Já | Já | Já | Já | Númer |
| 137 | Bæta tengslum við viðskiptavin | Bættu tengslum við viðskiptavin á síðunni **Upplýsingar um viðskiptavin**. | Númer | Númer | Númer | Já | Númer |
| 138 | Fjarlægja tengsl við viðskiptavin | Fjarlægja tengsl á síðunni **Upplýsingar um viðskiptavin**. | Númer | Númer | Númer | Já | Númer |
| 643 | Bæta við afsláttarmiðakóða | Bæta við afsláttarmiða með því að rita kóðann í POS. | Já | Já | Númer | Já | Númer |
| 117 | Bæta vildarkorti við | Hvettu notandann til að færa inn hollustukortanúmer sem verður bætt við núverandi viðskipti. | Já | Já | Númer | Já | Númer |
| 136 | Bæta við raðnúmeri | Þessi aðgerð gerir notandanum kleift að tilgreina raðnúmer fyrir vöru sem valin er núna. | Já | Já | Númer | Já | Númer |
| 1214 | Bæta við sendingaraðsetri | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 519 | Bæta við gjafakort | Bæta fé inn á tiltekið gjafakort. | Já | Já | Númer | Númer | Númer |
| 6000 | Leyfa að sleppa fjárhagsskráningu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 1212 | Peningaflutningur í banka | Skrá þá peningaupphæð sem er send í banka og aðrar upplýsingar, svo sem númer bankatösku. | Já | Já | Já | Já | Númer |
| 923 | Staðfesting bankasamtalna | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 915 | Auð aðgerð | Þessi aðgerð er með sérsniðinn hnapp sem forritari getur með forritun breytt fyrir allar sérhæfðar aðgerðir sem fyrirtækið þarf á að halda. | Já | Já | Já | Já | Númer |
| 1053 | Loka vakt blindandi | Stilltu núverandi vakt í loka blint og skráðu notandann út. Vakt sem er lokað blint er útilokuð frá viðbótarviðskiptum en er enn opin fyrir skúffuaðgerðum, eins og skiptimynt fjarlægð og talning skiptimyntar. | Já | Já | Já | Númer | Númer |
| 310 | Reikna út samtölu | Þegar afsláttarútreikningur er seinkað byrjar þessi aðgerð útreikning fyrir núverandi viðskipti. | Já | Já | Númer | Já | Númer |
| 642 | Framkvæma allar afurðir | Stilla afhendingarmáti fyrir allar línur á **Framkvæma**. | Já | Já | Númer | Já\* | Númer |
| 641 | Framkvæma valdar afurðir | Stilla afhendingarmáti fyrir valdar línur á **Framkvæma**. | Já | Já | Númer | Já\* | Númer |
| 1215 | Breyta aðgangsorði | Þessi aðgerð gerir POS notanda kleift að breyta aðgangsorði hans eða hennar. | Já | Já | Já | Númer | Númer |
| 123 | Breyta mælieiningu | Breyta mælieiningu fyrir valið línuatriði. | Já | Já | Númer | Já | Númer |
| 639 | Hreinsa sjálfgefinn sölufulltrúa í færslu | Fjarlægja söluflokk þóknunar (sölumaður) úr viðskiptinunum. | Já | Já | Númer | Já | Númer |
| 106 | Hreinsa magn | Endurstilla magn í línu sem er valin á **1**. | Já | Já | Númer | Já | Númer |
| 640 | Hreinsa sölufulltrúa í línu | Fjarlægja söluflokk þóknunar (sölumaður) frá línunni sem nú er valin. | Já | Já | Númer | Já | Númer |
| 121 | Hreinsa sölumann | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 1055 | Loka vakt | Loka núverandi vakt, prenta Z skýrslu og skrá notandann út úr kerfinu. | Já | Já | Já | Nei | Nei |
| 139 | Ljúka við færslu | Biður notanda um að velja greiðslumáta | Já | Já | Nei | Já | Nei |
| 620 | Stofna pöntun viðskiptavinar | Umbreyta POS viðskiptum í pöntun viðskiptavinar. | Já | Já | Nei | Já\* | Nei |
| 925 | Afritið bankaávísunina | Þessi aðgerð er ekki studd. | Á ekki við | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 620 | Stofna pöntun viðskiptavinar | Umbreyta POS viðskiptum í pöntun viðskiptavinar. | Já | Já | Númer | Já\* | Númer |
| 621 | Stofna tilboð | Umbreyta POS viðskiptum í sölutilboð. | Já | Já | Númer | Já\* | Númer |
| 636 | Stofna smásölufærslu | Þessi aðgerð gerir notandanum kleift að búa til staðlaða söluviðskipti þegar sjálfgefið POS hegðunin felst í því að búa til pantanir viðskiptavina. | Já | Já | Númer | Já | Númer |
| 600 | Viðskiptavinur | Bæta tilgreindum viðskiptavini við færsluna. | Númer | Númer | Númer | Já | Númer |
| 1100 | Innborgun á viðskiptavinalykil | Greiða inn á lykil viðskiptamanns. | Já | Já | Já | Já | Já |
| 612 | Nýr viðskiptavinur | Þessi aðgerð gerir notandanum kleift að stofna nýja skráningu viðskiptavinar. | Já | Já | Já | Já† | Númer |
| 603 | Viðskiptavinarhreinsun | Fjarlægja viðskiptavin af núgildandi færslu. | Já | Já | Númer | Já | Númer |
| 602 | Viðskiptavinaleit | Þessi aðgerð gerir notandanum kleift að leita að skráningu viðskiptavinar með því að fara á leitarsíðu viðskiptavina í POS. | Já | Já | Já | Já | Númer |
| 609 | Færslur viðskiptavinar | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 917 | Staða gagnagrunnstengingar | Þessi aðgerð gerir notandanum kleift að skoða núverandi tengistillingar og skipta á milli þess að vera með og án nettengingar. | Já | Já | Já | Já | Númer |
| 1200 | Skilgreina upphafsupphæð | Tilgreina upphæð í peningaskúffu við upphaf dags eða vaktar. | Já | Já | Já | Já | Númer |
| 132 | Hnekking innborgunar | Hnekkja sjálfgefinn innborgun fyrir pantanir viðskiptavina. | Já | Já | Númer | Já\* | Númer |
| 913 | Slökkva á hönnunarstillingu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 912 | Kveikja á hönnunarstillingu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 1217 | Hluta sundur sett | Sundurhluta setts í íhlutaafurðir sínar. | Já | Já | Já | Já | Númer |
| 624 | Birta endurgreiðsluupphæðir. | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 513 | Sýna samtölu | Sýna stöðu færslunnar á skjá viðskiptavinar. | Já | Já | Já | Já | Númer |
| 623 | Breyta viðskiptavini | Breyta núgildandi upplýsingum um viðskiptavin. | Já | Já | Númer | Númer | Númer |
| 614 | Breyta pöntun viðskiptavinar | Muna valda pöntun til þess að hægt sé að breyta henni í POS. | Númer | Númer | Númer | Númer | Númer |
| 615 | Breyta tilboði | Muna valið tilboð þannig að hægt sé að breyta því í POS. | Númer | Númer | Númer | Númer | Númer |
| 518 | Kostnaðarlyklar | Skrá fé sem fjarlægt er úr peningaskúffu vegna tilfallandi kostnaðar. | Já | Já | Já | Já | Númer |
| 919 | Löng innskráning | Úthluta eða fjarlægja heimild til að skrá sig inn með því að skanna strikamerki eða nota kort. | Já | Já | Já | Já | Nei |
| 1201 | Skiptimyntarfærsla | Þessi aðgerð gerir notandanum kleift að bæta við aukapeningum í núverandi skúffu eða vakt. | Já | Já | Já | Já | Númer |
| 1218 | Þvinga aflæsingu jaðarbúnaðar | Kerfið notar þessa aðgerð í innri vinnslu til að aflæsa POS-jaðarbúnað. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 520 | Staða gjafakorts | Birta innistæðu gjafakorts. | Já | Já | Númer | Númer | Númer |
| 708 | Gera tæki óvirkt | Slökktu á núverandi tæki þannig að það sé ekki hægt að nota sem POS skrá. | Númer | Númer | Númer | Númer | Númer |
| 517 | Tekjulyklar | Skrá peninga sem settir eru í peningaskúffuna af öðrum ástæðum en sölu. | Já | Já | Já | Já | Númer |
| 801 | Birgðauppfletting | Fletta upp magn tiltækt, í pöntun, og tiltækt að lofa (ATP) fyrir núgildandi verslun og aðrar tiltækar staðsetninga. | Já | Já | Já | Númer | Númer |
| 122 | Athugasemd við reikning | Þessi aðgerð gerir notandanum kleift að færa inn athugasemd varðandi núgildandi færslu. | Já | Já | Númer | Já | Númer |
| 511 | Gefa út kreditreikning | Gefðu út kreditreikning til leggja fram úttektarmiða í stað endurgreiðslu. | Já | Já | Númer | Númer | Númer |
| 512 | Gefa út gjafakort | Gefa út nýtt gjafakort fyrir tilgreint magn. | Já | Já | Númer | Númer | Númer |
| 625 | Gefa út vildarkort | Gefa út vildarkort til viðskiptavinar svo að viðskiptavinurinn getur tekið þátt í vildarkerfi verslunar. | Já | Já | Já | Númer | Númer |
| 300 | Línuafsláttarupphæð | Færa inn afsláttarupphæð fyrir línuatriði í færslunni. Þessi aðgerð er aðeins notuð fyrir afsláttarvörur og aðeins innan tilgreindra afsláttarmarka. | Já | Já | Númer | Já | Númer |
| 301 | Línuafsláttarprósenta | Færa inn afsláttarprósentu fyrir línuatriði í færslunni. Þessi aðgerð er aðeins notuð fyrir afsláttarvörur og aðeins innan tilgreindra afsláttarmarka. | Já | Já | Númer | Já | Númer |
| 703 | Læsa afgreiðslukassa | Læstu núverandi skrá, svo ekki sé hægt að nota hana, en ekki skrá núverandi notanda út. | Númer | Númer | Númer | Já | Númer |
| 701 | Skrá út | Skrá núverandi notanda út úr afgreiðslukassanum. | Já | Já | Já | Já | Númer |
| 521 | Punktastaða vildarkorts | Sýna punktastöðu fyrir tilgreint vildarkort. | Já | Já | Númer | Númer | Númer |
| 918 | Stjórna vöktum | Sýna lista yfir vaktir sem eru virkar, frestaðar og lokaðar blint. | Já | Já | Já | Númer | Númer |
| 914 | Minnka glugga sölustaðar | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 1000 | Opin skúffa | Framkvæma aðgerðina „engin sala“ og opna peningaskúffu sem er valin núna. | Já | Já | Já | Já | Númer |
| 928 | Uppfylling pöntunar | Þessi aðgerð gerir notendum kleift að taka til, pakka, senda eða afturkalla pantanir fyrir afhendingu í verslun. | Já | Já | Já | Númer | Númer |
| 129 | Hnekkja línuskatti | Hnekkja skatti á völdu línuatriði og nota annan tilgreindan skatt. | Já | Já | Númer | Já | Númer |
| 130 | Hnekkja línuskatti af lista | Hnekkja skatti á línuatriði og nota skatt sem notandi velur úr lista. | Já | Já | Númer | Já | Númer |
| 127 | Hnekkja færsluskatti | Hnekkja skatti á færslunni og nota annan tilgreindan skatt. | Já | Já | Númer | Já | Númer |
| 128 | Hnekkja færsluskatti af lista | Hnekkja skatti á færslunni og nota skatt sem notandi velur úr lista. | Já | Já | Númer | Já | Númer |
| 131 | Fylgiseðill | Bóka fylgiseðil fyrir valda pöntun. | Númer | Númer | Númer | Númer | Númer |
| 710 | Para vélbúnaðarstöð | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 201 | Greitt með korti | Samþykkja kortagreiðslu með kredit- eða debetkorti. | Já | Já | Númer | Já | Númer |
| 200 | Greitt með reiðufé | Samþykkja greiðslu með reiðufé. | Já | Já | Númer | Já | Númer |
| 206 | Greitt með reiðufé - nákvæm upphæð | Ljúka viðskiptunum með einni hendingu og samþykkja upphæðin sem er gjaldfærð í reiðufé (nákvæm skiptimynt). | Já | Já | Númer | Já | Númer |
| 204 | Greitt með ávísun | Samþykkja ávísun sem greiðslu. | Já | Já | Númer | Já | Númer |
| 213 | Greitt með kreditreikningi | Samþykkja kreditreikning (úttektarmiða) sem verslunin gefur út. | Já | Já | Númer | Númer | Númer |
| 203 | Greitt í gjaldmiðli | Samþykkja greiðslu í ýmsum gjaldmiðlum. | Já | Já | Númer | Já | Númer |
| 202 | Greitt með viðskiptavinalykli | Skrifa færsluna á reikning viðskiptamanns. Þessi greiðslumáti er ekki gild fyrir innistæður pantana viðskiptavina. | Já | Já | Númer | Númer | Númer |
| 214 | Greitt með gjafakorti | Samþykkja gjafakort sem verslunin gefur út. | Já | Já | Númer | Númer | Númer |
| 207 | Greitt með vildarkorti | Samþykkja vildarkort fyrir greiðslu og innleysa punkta fyrir gjaldgenga vöru. | Já | Já | Númer | Númer | Númer |
| 634 | Greiðslusaga | Sýna greiðslusögu viðskiptavinar fyrir núverandi pöntun viðskiptavinar. | Já | Já | Númer | Númer | Númer |
| 803 | Tiltekt og móttaka | Opnaðu síðu **Tiltekt og móttaka** þar sem þú getur valið pantanir til að taka til eða taka á móti í versluninni. | Já | Já | Já | Númer | Númer |
| 632 | Sækja allar afurðir | Stilltu uppfyllingaraðferðina á **Sótt í verslun** fyrir allar línur. | Já | Já | Númer | Já\* | Númer |
| 631 | Sækja valdar afurðir | Stilltu uppfyllingaraðferðina á **Sótt í verslun** fyrir allar línur. | Já | Já | Númer | Já\* | Númer |
| 400 | Sprettivalmynd | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 101 | Verðathugun | Þessi aðgerð gerir notandanum kleift að fletta upp verði fyrir tiltekinn vöru. | Já | Já | Já | Já | Númer |
| 104 | Verðbreyting | Hnekkja verði afurðarinnar, ef afurðin hefur verið sett upp til þess að leyfa að verði sé hnekkt. | Já | Já | Númer | Já | Númer |
| 1058 | Prenta fjárhag X | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 1059 | Prenta fjárhag Z | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 927 | Prenta vörumerkingu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 926 | Prenta hillumerkingu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 1056 | Prenta X | Prenta og X skýrslu fyrir núverandi vakt. | Já | Já | Já | Númer | Númer |
| 103 | Afurðarathugasemd | Bæta athugasemd við valið línuatriði í færslunni. | Já | Já | Númer | Já | Númer |
| 100 | Afurðarsala | Bæta tilgreindri afurð við færsluna. | Já | Já | Já | Já | Númer |
| 108 | Afurðaleit | Þessi aðgerð leyfir notandanum að leita að vöru með því að fara á vöruleitarsíðuna í POS. | Já | Já | Já | Já | Númer |
| 633 | Lokadagur tilboðs | Þessi aðgerð leyfir notandanum að skoða eða breyta lokadagsetningu á sölutilboði. | Já | Já | Númer | Já\* | Númer |
| 627 | Endurreikna | Endurreikna alla pöntunarlínur viðskiptavinar og skatta, byggt á núverandi grunnstillingu. | Já | Já | Númer | Já\* | Númer |
| 515 | Afturkalla pöntun | Þessi aðgerð leyfir notandanum að leita að og muna pantanir viðskiptavinar og sölutilboð. | Já | Já | Já | Númer | Númer |
| 504 | Afturkalla færslu | Þessi aðgerð leyfir notandanum að kalla aftur upp færslu sem hafði verið frestað áður í núverandi verslun. | Já | Já | Númer | Já‡ | Númer |
| 305 | Innleysa vildarpunkta | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 635 | Endurgreiða sendingargjöld | Þessi aðgerð gerir notendum kleift að endurgreiða flutningskostnað á pöntun sem hætt var við. | Númer | Númer | Númer | Númer | Númer |
| 644 | Fjarlægja afsláttarmiðakóða | Hvetja notandann til að fjarlægja afsláttarmiða með því að velja þau á lista yfir afsláttarmiða sem tengjast viðskiptunum. | Já | Já | Númer | Já | Númer |
| 1057 | Endurprenta Z | Endurprenta Z-skýrsluna fyrir fyrri vakt eða valda vakt. | Já | Já | Já | Númer | Númer |
| 1216 | Færið inn nýtt aðgangsorð | Þessi aðgerð gerir notanda sem hefur heimild fyrir endurstillingu aðgangsorðs kleift að endurstilla aðgangsorð annars starfsmanns með því að nota tímabundið aðgangsorð. | Já | Já | Já | Númer | Númer |
| 1219 | Opna vefslóð í POS | Þessi aðgerð gerir notanda kleift að opna vefslóð, sem stjórnandi hefur stillt, í POS. | Já | Já | Já | Já | Númer | 
| 109 | Skila afurð | Framkvæma skil á einstaka afurðum. Næsta skannaða afurð er birt sem skiluð vara sem hefur neikvætt magn og verð. | Já | Já | Númer | Já | Númer |
| 114 | Skilafærsla | Muna fyrri viðskipti út frá kvittunarnúmeri til að skila einhverjum eða öllum vörum. | Já | Já | Já | Já§ | Númer |
| 1211 | Peningaflutningur í öryggisskáp | Flytja peninga úr afgreiðslukassa í öryggisskáp. | Já | Já | Já | Já | Númer |
| 516 | Sölureikningur | Þessi aðgerð gerir viðskiptamanni kleift senda greiðslur á valda sölureikninginn. | Já | Já | Númer | Númer | Númer |
| 502 | Sölumaður | Þessi aðgerð leyfir notandanum að stilla **Sölutaki** gildið á sölupöntun fyrir pantanir viðskiptavina í POS. | Já | Já | Númer | Já\* | Númer |
| 2000 | Áætla stjórnun | Þessi aðgerð gerir notanda kleift að stofna, breyta eða skoða starfsmannaskemu. | Já | Já | Já | Númer | Númer |
| 2001 | Áætla beiðnir | Þessi aðgerð leyfir notandanum að biðja um frí, skipta um vaktir eða bjóða öðrum starfsmönnum vaktir. | Já | Já | Já | Númer | Númer |
| 622 | Leit | Þessi aðgerð gerir notendum kleift að forsamskipa POS hnappa til að framkvæma leitir út frá hlut, viðskiptavini eða flokki. | Já | Já | Já | Já | Númer |
| 1213 | Finna sendingaraðsetur | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 709 | Velja vélbúnaðarstöð | Þessi aðgerð gerir notandanum kleift að velja vélbúnaðarstöð á lista yfir tiltæka vélbúnaðarstöðvar. | Já | Já | Já | Já | Númer |
| 637 | Stilla sjálfgefinn sölufulltrúa í færslu | Þessi aðgerð gerir notandanum kleift að velja einn af viðurkenndum söluflokkum þóknunar (sölumenn) sem sjálfgefin sölumann fyrir línur sem eru bætt við seinna. | Já | Já | Númer | Já | Númer |
| 105 | Stilla magn | Breyta magni fyrir línuvöru í færslunni. | Já | Já | Númer | Já | Númer |
| 638 | Stilla sölufulltrúa í línu | Þessi aðgerð gerir notandanum kleift að velja einn af viðurkenndum söluflokkum þóknunar (sölumenn) fyrir línuna sem er valin nú. | Já | Já | Númer | Já | Númer |
| 630 | Senda allar afurðir | Stilla uppfyllingarhaminn í **Senda** fyrir alla línuatriði. | Já | Já | Númer | Já\* | Númer |
| 629 | Senda valdar afurðir | Stilltu uppfyllingarhaminn í **Sending** fyrir valdar línur. | Já | Já | Númer | Já\* | Númer |
| 115 | Sýna færslubók | Sýna færslubók verslunar. Þú getur skoðað viðskipti, endurprentað kvittanir og gjafakvittanir og afturköllun fyrir skil. | Já | Já | Já | Já\*\* | Númer |
| 802 | Birgðatalning | Þessi aðgerð gerir notandanum kleift að búa til eða breyta brigðatalningabókum fyrir efnislegar birgðir eða endurteknar talningar. | Já | Já | Já | Númer | Númer |
| 401 | Undirvalmynd | Þessi aðgerð tekur notandann í annað tengt hnappahnit. | Já | Já | Já | Já | Númer |
| 1054 | Ljúka vakt | Ljúka núverandi vakt, þannig að hægt sé að virkja nýja eða aðra vakt á núverandi afgreiðslukassa. | Já | Já | Já | Númer | Númer |
| 503 | Fresta færslu | Fresta núverandi sölufærslu, svo að hægt sé að afturkalla hana síðar í versluninni. | Já | Já | Númer | Já‡ | Númer |
| 1004 | Verkskráning | Opna verkskráning til að skrá tæknileg skref í POS | Númer | Númer | Númer | Já | Númer |
| 1052 | Talning skiptimyntar | Þessi aðgerð gerir notandanum kleift að tilgreina peningaupphæð í skúffunni fyrir hvern talinn greiðslumáta. | Já | Já | Já | Já | Númer |
| 1210 | Skiptimynt fjarlægð | Með þessari aðgerð er notandanum gert kleift að fjarlægja peninga úr núverandi skúffu eða vakt. | Já | Já | Já | Já | Númer |
| 920 | Stimpilklukka | Þessi aðgerð gerir notendum kleift að stimpla sig inn og út úr vöktum og hléum. | Já | Já | Já | Númer | Númer |
| 302 | Heildarafsláttarupphæð | Færa skal inn afsláttarupphæð fyrir færsluna. Þessi aðgerð er aðeins notuð fyrir afsláttarvörur og aðeins innan tilgreindra afsláttarmarka. | Já | Já | Númer | Já | Númer |
| 303 | Heildarafsláttarprósenta | Færa inn afsláttarprósentu fyrir færsluna. Þessi aðgerð er aðeins notuð fyrir afsláttarvörur og aðeins innan tilgreindra afsláttarmarka. | Já | Já | Númer | Já | Númer |
| 501 | Athugasemd við færslu | Bæta athugasemd við núverandi færslu. | Já | Já | Númer | Já | Númer |
| 922 | Skoða upplýsingar um afurð | Opna afurðarupplýsingasíðuna fyrir línuatriðið sem valið er núna. | Já | Já | Númer | Já | Númer |
| 1003 | Skoða skýrslur | Sýna skýrslurnar sem hafa verið skilgreindar fyrir núverandi notanda. | Já | Já | Já | Númer | Númer |
| 921 | Skoða færslur stimpilklukku | Sýna tímaklukkufærslur fyrir alla starfsmenn í versluninni. | Já | Já | Já | Númer | Númer |
| 211 | Ógilda greiðslu | Ógilda greiðslulínu sem nú er valin frá viðskiptunum. | Já | Já | Númer | Já | Númer |
| 102 | Ógild afurð | Ógilda greiðslulínuatriðið sem nú er valin frá viðskiptunum. | Já | Já | Númer | Já | Númer |
| 500 | Ógilda færslu | Eyða núgildandi færsla. | Já | Já | Númer | Já | Númer |
| 916 | Windows Workflow Foundation | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Númer |
| 924 | X-skýrsla fyrir bankakort | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |

\* Aðgerðin er í boði í ótengdum ham einungis þegar viðskiptavinapantanir eða sölutilboð eru stofnuð, og aðeins ef stofnun viðskiptavinapantanir eða sölutilboð í ótengdum ham er skilgreint í POS virknireglunni. Ekki er hægt að framkvæma aðgerðina þegar pantanir eru búnar til með því að nota rauntímaþjónustu eða þegar pantanir eru kallaðar fram aftur eða breyttar.

† Aðeins er hægt að framkvæma aðgerðina í ótengdum ham þegar POS er skilgreint til að leyfa stofnun viðskiptavina án nettengingar í POS virknireglunni.

‡ Þegar POS er ótengdur er einungis hægt að kalla aftur fram færslur sem var frestað frá ónettengdum gagnagrunni núverandi afgreiðslukassa. Notendur geta ekki frestað og kallað aftur fram viðskipti á milli skráa.

§ Þegar POS er ótengdur er aðeins hægt að kalla aftur fram viðskipti í núgildandi ótengda gagnagrunninum fyrir skil.

\*\* Þegar POS er ótengdur birtist aðeins viðskipti í núgildandi ótengda rásagagnagrunninum í færslubókinni.

---
title: Aðgerðir sölustaðar (POS) með og án nettengingar
description: Þetta efnisatriði veitir upplýsingar um rekstur sölustaðs (POS) í Dynamics 365 Commerce. Það tilgreinir hvar í forritinu má kalla fram aðgerðir og hvort þær séu tiltæk í ótengdum ham.
author: jblucher
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5e139b7b12b8f2e549fb9c2c8e39125e190c7396
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/16/2022
ms.locfileid: "8311980"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Aðgerðir sölustaðar (POS) með og án nettengingar

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Flestar aðgerðir sem notendur grípa til á sölustað (POS) eru taldar aðgerðir. Aðgerðir eru skilgreindar og þeim stjórnað í bakvinnslu Dynamics 365 Commerce. Hægt er að bæta mörgum aðgerðum við takka í POS hnappakerfinu. Notendur geta síðan valið hnappana til að kalla fram aðgerðir og framkvæma virkni þeirra. Aðrar aðgerðir er hluti af aðal POS forritinu og kallaðar fram annaðhvort úr hnöppum á skjánum eða sem hluti af öðrum verkflæði eða ferlum.

Eftirfarandi tafla veitir upplýsingar um aðgerðir sem eru í boði í Modern POS og Cloud POS. Taflan tilgreinir einnig hvar í forritinu er hægt að kalla fram aðgerðirnar og hvort þær séu tiltækar þegar POS er í ótengdum ham.

Sumar aðgerðir eru ekki í boði eins og er í Modern POS eða Cloud POS. Sumar þessara aðgerða eru staðbundnar aðgerðir sem krefjast viðbótarviðbóta og stillingar. Aðrar aðgerðir eru eiginleikar frá Microsoft Dynamics AX 2012 sem ekki eru studdir eins og er.

Eftirfarandi dálkar tilgreina hvar hægt er að kalla fram aðgerðirnar:

- **Hnappahnit** – Aðgerðinni er hægt að úthluta til hnappa í POS hnappahnitum, sem eru hluti af POS skjár útliti.
- **Færsluskjár** – Hægt er að kalla fram aðgerðina frá POS hnappahnitum sem eru skilgreind á POS færsluskjánum.
- **Velkomin skjár** – Hægt er að kalla fram aðgerðina frá POS hnappahnitum sem eru skilgreind á POS velkomin skjánum.

> [!NOTE]
> Aðgerðirnar sem taldar eru upp hér að neðan eiga við um nýjustu útgáfuna af Commerce. Sumar aðgerðir kunna að hafa breyst eða kunna ekki að vera í boði í fyrri útgáfum.


| KENNI | Aðgerð | lýsing | Hnappahnit | Færsluskjár | Upphafsskjár | Tiltæk utan nets | Tekur sérstaklega mið af staðsetningu |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Gera tæki virkt | Virkjaðu núverandi tæki með því að leyfa sannvottuðum notanda að veita upplýsingar um tengingu og úthluta tæki og skráa auðkenni. | Nei | Nei | Nei | Nei | Nei |
| 134 | Bæta við fyrirtækjatengslum | Bæta við forvalinni tengingu við færslu. Veljið tengsl á **Eiginleikar hnapps** síðunni. | Já | Já | Nei | Já | Nei |
| 135 | Bæta við tengslum úr lista | Bæta tengslum við færslu með því að velja í lista. | Já | Já | Já | Já | Nei |
| 137 | Bæta tengslum við viðskiptavin | Bættu tengslum við viðskiptavin á síðunni **Upplýsingar um viðskiptavin**. | Nei | Nei | Nei | Já | Nei |
| 138 | Fjarlægja tengsl við viðskiptavin | Fjarlægja tengsl á síðunni **Upplýsingar um viðskiptavin**. | Nei | Nei | Nei | Já | Nei |
| 643 | Bæta við afsláttarmiðakóða | Bæta við afsláttarmiða með því að rita kóðann í POS. | Já | Já | Nei | Já | Nei |
| 141 | Bæta við gjöldum í haus | Bættu ýmsum gjöldum við pöntunarhausinn. | Já | Já | Nei | Nei| Nei |
| 141 | Bæta við gjöldum í línu | Bættu ýmsum gjöldum við valda sölulínu. | Já | Já | Nei | Nei| Nei |
| 117 | Bæta vildarkorti við | Hvettu notandann til að færa inn hollustukortanúmer sem verður bætt við núverandi viðskipti. | Já | Já | Nei | Já | Nei |
| 136 | Bæta við raðnúmeri | Þessi aðgerð gerir notandanum kleift að tilgreina raðnúmer fyrir vöru sem valin er núna. | Já | Já | Nei | Já | Nei |
| 1214 | Bæta við sendingaraðsetri | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 519 | Bæta við gjafakort | Bæta fé inn á tiltekið gjafakort. | Já | Já | Nei | Nei | Nei |
| 6000 | Leyfa að sleppa fjárhagsskráningu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 1212 | Peningaflutningur í banka | Skrá þá peningaupphæð sem er send í banka og aðrar upplýsingar, svo sem númer bankatösku. | Já | Já | Já | Já | Nei |
| 923 | Staðfesting bankasamtalna | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 915 | Auð aðgerð | Þessi aðgerð er með sérsniðinn hnapp sem forritari getur með forritun breytt fyrir allar sérhæfðar aðgerðir sem fyrirtækið þarf á að halda. | Já | Já | Já | Já | Nei |
| 1053 | Loka vakt blindandi | Stilltu núverandi vakt í loka blint og skráðu notandann út. Vakt sem er lokað blint er útilokuð frá viðbótarviðskiptum en er enn opin fyrir skúffuaðgerðum, eins og skiptimynt fjarlægð og talning skiptimyntar. | Já | Já | Já | Nei | Nei |
| 310 | Reikna út samtölu | Þegar afsláttarútreikningur er seinkað byrjar þessi aðgerð útreikning fyrir núverandi viðskipti. | Já | Já | Nei | Já | Nei |
| 642 | Framkvæma allar afurðir | Stilla afhendingarmáti fyrir allar línur á **Framkvæma**. | Já | Já | Nei | Já\* | Nei |
| 641 | Framkvæma valdar afurðir | Stilla afhendingarmáti fyrir valdar línur á **Framkvæma**. | Já | Já | Nei | Já\* | Nei |
| 647 | Breyta afhendingarmáta | Breyta afhendingaraðferð fyrir fyrirfram samstilltar sendingarsölulínur. | Já | Já | Nei | Nei| Nei |
| 1215 | Breyta aðgangsorði | Þessi aðgerð gerir POS notanda kleift að breyta aðgangsorði sínu. | Já | Já | Já | Nei | Nei |
| 123 | Breyta mælieiningu | Breyta mælieiningu fyrir valið línuatriði. | Já | Já | Nei | Já | Nei |
| 639 | Hreinsa sjálfgefinn sölufulltrúa í færslu | Fjarlægja söluflokk þóknunar (sölumaður) úr viðskiptinunum. | Já | Já | Nei | Já | Nei |
| 106 | Hreinsa magn | Endurstilla magn í línu sem er valin á **1**. | Já | Já | Nei | Já | Nei |
| 640 | Hreinsa sölufulltrúa í línu | Fjarlægja söluflokk þóknunar (sölumaður) frá línunni sem nú er valin. | Já | Já | Nei | Já | Nei |
| 121 | Hreinsa sölumann | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 1055 | Loka vakt | Loka núverandi vakt, prenta Z skýrslu og skrá notandann út úr kerfinu. | Já | Já | Já | Nei | Nei |
| 139 | Ljúka við færslu | Biður notanda um að velja greiðslumáta | Já | Já | Nr. | Já | Nr. |
| 925 | Afritið bankaávísunina | Þessi aðgerð er ekki studd. | Á ekki við | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 620 | Stofna pöntun viðskiptavinar | Umbreyta POS viðskiptum í pöntun viðskiptavinar. | Já | Já | Nei | Já\* | Nei |
| 621 | Stofna tilboð | Umbreyta POS viðskiptum í sölutilboð. | Já | Já | Nr. | Já\* | Nr. |
| 636 | Stofna smásölufærslu | Stofna staðlaða sölufærslu þegar sjálfgefna POS hegðun er að búa til pantanir viðskiptavina. | Já | Já | Nei | Já | Nei |
| 600 | Viðskiptavinur | Bæta tilgreindum viðskiptavini við færsluna. | Nei | Nei | Nei | Já | Nei |
| 1100 | Innborgun á viðskiptavinalykil | Greiða inn á lykil viðskiptamanns. | Já | Já | Já | Já | Já |
| 612 | Nýr viðskiptavinur | Búðu til nýja viðskiptaskrá. | Já | Já | Já | Já† | Nr. |
| 603 | Viðskiptavinarhreinsun | Fjarlægja viðskiptavin af núgildandi færslu. | Já | Já | Nr. | Já | Nr. |
| 602 | Viðskiptavinaleit | Leitaðu að viðskiptavinaskrá með því að fara á leitarsíðu viðskiptavina í POS. | Já | Já | Já | Já | Nei |
| 609 | Færslur viðskiptavinar | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Á ekki við | Á ekki við | Nr. |
| 917 | Staða gagnagrunnstengingar | Skoðaðu núverandi tengistillingar og skiptu á milli nettengingar og ótengdra stillinga. | Já | Já | Já | Já | Nei |
| 1200 | Skilgreina upphafsupphæð | Tilgreina upphæð í peningaskúffu við upphaf dags eða vaktar. | Já | Já | Já | Já | Nei |
| 132 | Hnekking innborgunar | Hnekkja sjálfgefinn innborgun fyrir pantanir viðskiptavina. | Já | Já | Nei | Já\* | Nei |
| 913 | Slökkva á hönnunarstillingu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 912 | Kveikja á hönnunarstillingu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 1217 | Hluta sundur sett | Sundurhluta setts í íhlutaafurðir sínar. | Já | Já | Já | Já | Nei |
| 624 | Birta endurgreiðsluupphæðir. | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 513 | Sýna samtölu | Sýna stöðu færslunnar á skjá viðskiptavinar. | Já | Já | Já | Já | Nei |
| 623 | Breyta viðskiptavini | Breyta núgildandi upplýsingum um viðskiptavin. | Já | Já | Nei | Nei | Nei |
| 614 | Breyta pöntun viðskiptavinar | Muna valda pöntun til þess að hægt sé að breyta henni í POS. | Nei | Nei | Nei | Nei | Nei |
| 615 | Breyta tilboði | Muna valið tilboð þannig að hægt sé að breyta því í POS. | Nei | Nei | Nei | Nei | Nei |
| 518 | Kostnaðarlyklar | Skrá fé sem fjarlægt er úr peningaskúffu vegna tilfallandi kostnaðar. | Já | Já | Já | Já | Nei |
| 919 | Löng innskráning | Úthluta eða fjarlægja heimild til að skrá sig inn með því að skanna strikamerki eða nota kort. | Já | Já | Já | Já | Nr. |
| 1201 | Skiptimyntarfærsla | Bættu viðbótarfé við núverandi skúffu eða vakt. | Já | Já | Já | Já | Nei |
| 1218 | Þvinga aflæsingu jaðarbúnaðar | Kerfið notar þessa aðgerð í innri vinnslu til að aflæsa POS-jaðarbúnað. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 520 | Staða gjafakorts | Birta innistæðu gjafakorts. | Já | Já | Nei | Nei | Nei |
| 708 | Gera tæki óvirkt | Slökktu á núverandi tæki þannig að það sé ekki hægt að nota sem POS skrá. | Nei | Nei | Nei | Nei | Nei |
| 804 | Aðgerð á innleið | Fáðu aðgang að eiginleikum birgðastjórnunar á innleið. | Já | Nei | Já | Nei| Nei |
| 517 | Tekjulyklar | Skrá peninga sem settir eru í peningaskúffuna af öðrum ástæðum en sölu. | Já | Já | Já | Já | Nei |
| 801 | Birgðauppfletting | Fletta upp magn tiltækt, í pöntun, og tiltækt að lofa (ATP) fyrir núgildandi verslun og aðrar tiltækar staðsetninga. | Já | Já | Já | Nr. | Nr. |
| 806 | Leiðrétting birgða | Stilltu birgðahald innan eða utan vöruhúss verslunar með því að nota leiðréttingar- eða hreyfidagbók. | Já | Já | Já | Nr. | Nr. |
| 807 | Birgðahreyfing | Færa vörur frá einni birgðastað til annarrar innan vöruhúss verslunar. | Já | Já | Já | Nr. | Nr. |
| 122 | Athugasemd við reikning | Sláðu inn athugasemd um núverandi færslu. | Já | Já | Nr. | Já | Nei |
| 511 | Gefa út kreditreikning | Gefðu út kreditreikning til leggja fram úttektarmiða í stað endurgreiðslu. | Já | Já | Nei | Nei | Nei |
| 512 | Gefa út gjafakort | Gefa út nýtt gjafakort fyrir tilgreint magn. | Já | Já | Nei | Nei | Nei |
| 625 | Gefa út vildarkort | Gefa út vildarkort til viðskiptavinar svo að viðskiptavinurinn getur tekið þátt í vildarkerfi verslunar. | Já | Já | Já | Nei | Nei |
| 300 | Línuafsláttarupphæð | Færa inn afsláttarupphæð fyrir línuatriði í færslunni. Þessi aðgerð er aðeins notuð fyrir afsláttarvörur og aðeins innan tilgreindra afsláttarmarka. | Já | Já | Nei | Já | Nei |
| 301 | Línuafsláttarprósenta | Færa inn afsláttarprósentu fyrir línuatriði í færslunni. Þessi aðgerð er aðeins notuð fyrir afsláttarvörur og aðeins innan tilgreindra afsláttarmarka. | Já | Já | Nei | Já | Nei |
| 703 | Læsa afgreiðslukassa | Læstu núverandi skrá, svo ekki sé hægt að nota hana, en ekki skrá núverandi notanda út. | Nei | Nei | Nei | Já | Nei |
| 701 | Skrá út | Skrá núverandi notanda út úr afgreiðslukassanum. | Já | Já | Já | Já | Nei |
| 521 | Punktastaða vildarkorts | Sýna punktastöðu fyrir tilgreint vildarkort. | Já | Já | Nei | Nei | Nei |
| 142 | Stjórna gjöldum | Skoðaðu og stjórnaðu ýmsum gjöldum sem er beitt á færslu. | Já | Já | Nei | Nei| Nei |
| 918 | Stjórna vöktum | Sýna lista yfir vaktir sem eru virkar, frestaðar og lokaðar blint. | Já | Já | Já | Nei | Nei |
| 914 | Minnka glugga sölustaðar | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 1000 | Opin skúffa | Framkvæma aðgerðina „engin sala“ og opna peningaskúffu sem er valin núna. | Já | Já | Já | Já | Nei |
| 928 | Uppfylling pöntunar | Þessi aðgerð gerir notendum kleift að taka til, pakka, senda eða afturkalla pantanir fyrir afhendingu í verslun. | Já | Já | Já | Nei | Nei |
| 805 | Aðgerð á útleið | Aðgangsaðgerðir til að hafa umsjón með sendingum á pöntunum á útleið. | Já | Nei | Já | Nei| Nei |
| 129 | Hnekkja línuskatti | Hnekkja skatti á völdu línuatriði og nota annan tilgreindan skatt. | Já | Já | Nei | Já | Nei |
| 130 | Hnekkja línuskatti af lista | Hnekkja skatti á línuatriði og nota skatt sem notandi velur úr lista. | Já | Já | Nei | Já | Nei |
| 127 | Hnekkja færsluskatti | Hnekkja skatti á færslunni og nota annan tilgreindan skatt. | Já | Já | Nei | Já | Nei |
| 128 | Hnekkja færsluskatti af lista | Hnekkja skatti á færslunni og nota skatt sem notandi velur úr lista. | Já | Já | Nei | Já | Nei |
| 131 | Fylgiseðill | Bóka fylgiseðil fyrir valda pöntun. | Nei | Nei | Nei | Nei | Nei |
| 710 | Para vélbúnaðarstöð | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 201 | Greitt með korti | Samþykkja kortagreiðslu með kredit- eða debetkorti. | Já | Já | Nei | Já | Nei |
| 200 | Greitt með reiðufé | Samþykkja greiðslu með reiðufé. | Já | Já | Nei | Já | Nei |
| 206 | Greitt með reiðufé - nákvæm upphæð | Ljúka viðskiptunum með einni hendingu og samþykkja upphæðin sem er gjaldfærð í reiðufé (nákvæm skiptimynt). | Já | Já | Nei | Já | Nei |
| 204 | Greitt með ávísun | Samþykkja ávísun sem greiðslu. | Já | Já | Nei | Já | Nei |
| 213 | Greitt með kreditreikningi | Samþykkja kreditreikning (úttektarmiða) sem verslunin gefur út. | Já | Já | Nei | Nei | Nei |
| 203 | Greitt í gjaldmiðli | Samþykkja greiðslu í ýmsum gjaldmiðlum. | Já | Já | Nei | Já | Nei |
| 202 | Greitt með viðskiptavinalykli | Skrifa færsluna á reikning viðskiptamanns. Þessi greiðslumáti er ekki gild fyrir innistæður pantana viðskiptavina. | Já | Já | Nei | Nei | Nei |
| 214 | Greitt með gjafakorti | Samþykkja gjafakort sem verslunin gefur út. | Já | Já | Nei | Nei | Nei |
| 207 | Greitt með vildarkorti | Samþykkja vildarkort fyrir greiðslu og innleysa punkta fyrir gjaldgenga vöru. | Já | Já | Nei | Nei | Nei |
| 634 | Greiðslusaga | Sýna greiðslusögu viðskiptavinar fyrir núverandi pöntun viðskiptavinar. | Já | Já | Nei | Nei | Nei |
| 803 | Tiltekt og móttaka | Opnaðu síðu **Tiltekt og móttaka** þar sem þú getur valið pantanir til að taka til eða taka á móti í versluninni. | Já | Já | Já | Nei | Nei |
| 632 | Sækja allar afurðir | Stilltu uppfyllingaraðferðina á **Sótt í verslun** fyrir allar línur. | Já | Já | Nei | Já\* | Nei |
| 631 | Sækja valdar afurðir | Stilltu uppfyllingaraðferðina á **Sótt í verslun** fyrir allar línur. | Já | Já | Nei | Já\* | Nei |
| 400 | Sprettivalmynd | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 101 | Verðathugun | Þessi aðgerð gerir notandanum kleift að fletta upp verði fyrir tiltekinn vöru. | Já | Já | Já | Já | Nei |
| 104 | Verðbreyting | Hnekkja verði afurðarinnar, ef afurðin hefur verið sett upp til þess að leyfa að verði sé hnekkt. | Já | Já | Nei | Já | Nei |
| 1058 | Prenta fjárhag X | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 1059 | Prenta fjárhag Z | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 927 | Prenta vörumerkingu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 926 | Prenta hillumerkingu | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 1056 | Prenta X | Prenta og X skýrslu fyrir núverandi vakt. | Já | Já | Já | Nei | Nei |
| 103 | Afurðarathugasemd | Bæta athugasemd við valið línuatriði í færslunni. | Já | Já | Nei | Já | Nei |
| 100 | Afurðarsala | Bæta tilgreindri afurð við færsluna. | Já | Já | Já | Já | Nr. |
| 108 | Afurðaleit | Leitaðu að vöru með því að fara á vöruleitarsíðuna í POS. | Já | Já | Já | Já | Nr. |
| 633 | Lokadagur tilboðs | Skoðaðu eða breyttu fyrningardagsetningu á sölutilboði. | Já | Já | Nei | Já\* | Nei |
| 627 | Endurreikna | Endurreikna alla pöntunarlínur viðskiptavinar og skatta, byggt á núverandi grunnstillingu. | Já | Já | Nei | Já\* | Nei |
| 143 | Endurreikna gjöld | Reiknaðu aftur sjálfvirkt gjald fyrir pöntunina. | Já | Já | Nr. | Nr.| Nr. |
| 515 | Afturkalla pöntun | Leitaðu að og endurkallaðu pantanir viðskiptavina og sölutilboð. | Já | Já | Já | Nr. | Nr. |
| 504 | Afturkalla færslu | Muna áður stöðvuð viðskipti frá núverandi verslun. | Já | Já | Nei | Já‡ | Nei |
| 305 | Innleysa vildarpunkta | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Á ekki við | Á ekki við | Já |
| 635 | Endurgreiða sendingargjöld | Endurgreiðsla sendingarkostnaðar á hætt við pöntun. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 644 | Fjarlægja afsláttarmiðakóða | Hvetja notandann til að fjarlægja afsláttarmiða með því að velja þau á lista yfir afsláttarmiða sem tengjast viðskiptunum. | Já | Já | Nei | Já | Nei |
| 1057 | Endurprenta Z | Endurprenta Z-skýrsluna fyrir fyrri vakt eða valda vakt. | Já | Já | Já | Nei | Nei |
| 1216 | Færið inn nýtt aðgangsorð | Þessi aðgerð gerir notanda sem hefur heimild fyrir endurstillingu aðgangsorðs kleift að endurstilla aðgangsorð annars starfsmanns með því að nota tímabundið aðgangsorð. | Já | Já | Já | Nr. | Nr. |
| 1219 | Opna vefslóð í sölustað | Opnaðu stjórnandastillinga vefslóð í POS. | Já | Já | Já | Já | Nr. |
| 109 | Skila afurð | Framkvæma skil á einstaka afurðum. Næsta skannaða afurð er birt sem skiluð vara sem hefur neikvætt magn og verð. | Já | Já | Nei | Já | Nei |
| 114 | Skilafærsla | Muna fyrri viðskipti út frá kvittunarnúmeri til að skila einhverjum eða öllum vörum. | Já | Já | Já | Já§ | Nei |
| 1211 | Peningaflutningur í öryggisskáp | Flytja peninga úr afgreiðslukassa í öryggisskáp. | Já | Já | Já | Já | Nei |
| 516 | Sölureikningur | Þessi aðgerð gerir viðskiptamanni kleift senda greiðslur á valda sölureikninginn. | Já | Já | Nr. | Nr. | Nr. |
| 502 | Sölumaður | Stilltu **Sölumaður** gildi á sölupöntun fyrir pantanir viðskiptavina í POS. | Já | Já | Nei | Já\* | Nei |
| 2000 | Áætla stjórnun | Þessi aðgerð er ekki enn studd. | Já | Já | Já | Nei | Nei |
| 2001 | Áætla beiðnir | Þessi aðgerð er ekki enn studd. | Já | Já | Já | Nei | Nei |
| 622 | Leit | Þessi aðgerð gerir notendum kleift að forsamskipa POS hnappa til að framkvæma leitir út frá hlut, viðskiptavini eða flokki. | Já | Já | Já | Já | Nei |
| 1213 | Finna sendingaraðsetur | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Á ekki við | Á ekki við | Nr. |
| 709 | Velja hardware station | Veldu vélbúnaðarstöð af lista yfir tiltækar vélbúnaðarstöðvar. | Já | Já | Já | Já | Nr. |
| 637 | Stilla sjálfgefinn sölufulltrúa í færslu | Veldu einn af gjaldgengum þóknunarsöluhópum (sölufulltrúar) sem sjálfgefna sölufulltrúa fyrir línur sem bætast við síðar. | Já | Já | Nei | Já | Nei |
| 105 | Stilla magn | Breyta magni fyrir línuvöru í færslunni. | Já | Já | Nr. | Já | Nr. |
| 638 | Stilla sölufulltrúa í línu | Veldu einn af gjaldgengum þóknunarsöluhópum (sölufulltrúar) fyrir þá línu sem er valin. | Já | Já | Nei | Já | Nei |
| 630 | Senda allar afurðir | Stilla uppfyllingarhaminn í **Senda** fyrir alla línuatriði. | Já | Já | Nei | Já\* | Nei |
| 629 | Senda valdar afurðir | Stilltu uppfyllingarhaminn í **Sending** fyrir valdar línur. | Já | Já | Nei | Já\* | Nei |
| 115 | Sýna færslubók | Sýna færslubók verslunar. Þú getur skoðað viðskipti, endurprentað kvittanir og gjafakvittanir og afturköllun fyrir skil. | Já | Já | Já | Já\*\* | Nr. |
| 802 | Birgðatalning | Stofna eða breyta birgðatalningarbókum fyrir efnislegar birgðir eða lotutalningar. | Já | Já | Já | Nei | Nei |
| 401 | Undirvalmynd | Þessi aðgerð tekur notandann í annað tengt hnappahnit. | Já | Já | Já | Já | Nei |
| 1054 | Ljúka vakt | Ljúka núverandi vakt, þannig að hægt sé að virkja nýja eða aðra vakt á núverandi afgreiðslukassa. | Já | Já | Já | Nei | Nei |
| 503 | Fresta færslu | Fresta núverandi sölufærslu, svo að hægt sé að afturkalla hana síðar í versluninni. | Já | Já | Nei | Já‡ | Nei |
| 1004 | Verkskráning | Opna verkskráning til að skrá tæknileg skref í POS | Nr. | Nr. | Nr. | Já | Nr. |
| 1052 | Talning skiptimyntar | Tilgreindu peningaupphæðina í skúffunni fyrir hvern talinn greiðslumáta. | Já | Já | Já | Já | Nr. |
| 1210 | Skiptimynt fjarlægð | Fjarlægðu peninga úr núverandi skúffu eða vakt. | Já | Já | Já | Já | Nr. |
| 920 | Stimpilklukka | Kýla inn og kýla úr vinnuvöktum og pásum. | Já | Já | Já | Nr. | Nei |
| 302 | Heildarafsláttarupphæð | Færa skal inn afsláttarupphæð fyrir færsluna. Þessi aðgerð er aðeins notuð fyrir afsláttarvörur og aðeins innan tilgreindra afsláttarmarka. | Já | Já | Nei | Já | Nei |
| 303 | Heildarafsláttarprósenta | Færa inn afsláttarprósentu fyrir færsluna. Þessi aðgerð er aðeins notuð fyrir afsláttarvörur og aðeins innan tilgreindra afsláttarmarka. | Já | Já | Nei | Já | Nei |
| 501 | Athugasemd við færslu | Bæta athugasemd við núverandi færslu. | Já | Já | Nei | Já | Nei |
| 922 | Skoða upplýsingar um afurð | Opna afurðarupplýsingasíðuna fyrir línuatriðið sem valið er núna. | Já | Já | Nei | Já | Nei |
| 1003 | Skoða skýrslur | Sýna skýrslurnar sem hafa verið skilgreindar fyrir núverandi notanda. | Já | Já | Já | Nei | Nei |
| 921 | Skoða færslur stimpilklukku | Sýna tímaklukkufærslur fyrir alla starfsmenn í versluninni. | Já | Já | Já | Nei | Nei |
| 211 | Ógilda greiðslu | Ógilda greiðslulínu sem nú er valin frá viðskiptunum. | Já | Já | Nei | Já | Nei |
| 102 | Ógild afurð | Ógilda greiðslulínuatriðið sem nú er valin frá viðskiptunum. | Já | Já | Nei | Já | Nei |
| 500 | Ógilda færslu | Eyða núgildandi færsla. | Já | Já | Nei | Já | Nei |
| 916 | Windows Workflow Foundation | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Nei |
| 924 | X-skýrsla fyrir bankakort | Þessi aðgerð er ekki studd. | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Ekki tiltækt | Já |
| 311 | Fjarlægja kerfisafslætti úr færslum | Fjarlægið alla afslætti sem kerfið hefur sett á, þar á meðal afslætti með afsláttarmiða, úr færslunni. Þetta fjarlægir ekki handvirkt afslátt. | Já | Já | Já | Já | Nei |
| 312 | Endurnota kerfisafslætti | Endurnota kerfisafslátt á færslunni ef þeir voru fjarlægðir með því að nota aðgerðina **Fjarlægja kerfisafslætti úr færslunni**. | Já | Já | Já | Já | Nei |

\* Aðgerðin er í boði í ótengdum ham einungis þegar viðskiptavinapantanir eða sölutilboð eru stofnuð, og aðeins ef stofnun viðskiptavinapantanir eða sölutilboð í ótengdum ham er skilgreint í POS virknireglunni. Ekki er hægt að framkvæma aðgerðina þegar pantanir eru búnar til með því að nota rauntímaþjónustu eða þegar pantanir eru kallaðar fram aftur eða breyttar.

† Aðeins er hægt að framkvæma aðgerðina í ótengdum ham þegar POS er skilgreint til að leyfa stofnun viðskiptavina án nettengingar í POS virknireglunni.

‡ Þegar POS er ótengdur er einungis hægt að kalla aftur fram færslur sem var frestað frá ónettengdum gagnagrunni núverandi afgreiðslukassa. Notendur geta ekki frestað og kallað aftur fram viðskipti á milli skráa.

§ Þegar POS er ótengdur er aðeins hægt að kalla aftur fram viðskipti í núgildandi ótengda gagnagrunninum fyrir skil.

\*\* Þegar POS er ótengdur birtist aðeins viðskipti í núgildandi ótengda rásagagnagrunninum í færslubókinni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

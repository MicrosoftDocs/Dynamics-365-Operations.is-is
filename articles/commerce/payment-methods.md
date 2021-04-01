---
title: Greiðsluhættir
description: Það þarf að skilgreina hverja greiðslugerð sem smásali samþykkir þegar kerfið er uppsett. Þetta grein lýsir þær gerðir greiðslna sem hægt er að setja upp og lýsir ferlinu við uppsetninguna.
author: rubencdelgado
manager: AnnBe
ms.date: 06/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 681672e19feb5b3bada126c67cd600ee6328da04
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257026"
---
# <a name="payment-methods"></a>Greiðsluhættir

[!include [banner](includes/banner.md)]

Það þarf að skilgreina hverja greiðslugerð sem smásali samþykkir þegar kerfið er uppsett. Þetta grein lýsir þær gerðir greiðslna sem hægt er að setja upp og lýsir ferlinu við uppsetninguna.

Smásalar geta tekið við ýmsum gerðum af greiðslu í staðinn fyrir afurðir og þjónustu sem þeir selja. Þótt reiðufé er algengasta greiðsluform smásala getur hann einnig þurft að taka við greiðslu í formi ávísana, korta, fylgiskjala og svo framvegis. Hver greiðslugerð sem smásali samþykkir verður að vera skilgreind í Dynamics 365 Commerce þegar kerfið er sett upp. Eftirfarandi listi lýsir hverri greiðslugerð sem hægt er að setja upp:

- **Reiðufé –** Peningar, þ.e. efnislegur gjaldmiðill á borð við seðla og mynt. Gjaldmiðillinn getur verið gjaldmiðill fyrirtækisins eða gjaldmiðill verslunarinnar.
- **Ávísun –** Framseljanlegur gerningur sem gefur loforð um greiðslu tiltekinnar upphæðar í tilteknum gjaldmiðli úr tilteknum banka. Ávísun gildir venjulega annaðhvort óráðinn tíma eða í sex mánuði eftir útgáfudag, nema annar gildistímabil er tilgreint. Þetta tímabil er breytileg eftir bankans sem ávísunin er gefin út á. Ýmsar gerðir ávísana eru í boði, á borð við pantanaávísanir, ávísanir á handhafa o.s.frv. Hægt er að setja upp ávísanir sem greiðslumáta fyrir hverja verslun. Ávísanir má samþykkja í þeim gjaldmiðli sem er skilgreind á fyrirtækisstigi eða stigi einstakra verslana. Setja verður upp ávísana sem greiðslumáta áður en hægt er að samþykkja ávísun sem greiðsla í verslun.
- **Gjaldmiðill –** Algengasta form greiðslna fyrir utan sjálfgefinn gjaldmiðil fyrirtækisins. Mynt og seðlar eru gjaldmiðilsform. Greiðsluháttur með gjaldmiðli tekur til allra gjaldmiðla sem eru notaðir. Áður en þessi greiðslumáti er notaður þarf að setja upp gjaldmiðla og tilgreina gengisupplýsingar fyrir gjaldmiðlana.
- **Kort** – Allar gerðir korta sem notaðar eru, svo sem debetkort og kreditkort. Góð hugmynd er að setja upp einn greiðsluhátt með korti á stigi fyrirtækis, til að sýna hverja tegund korts. Í hverri verslun má síðan setja upp greiðsluhátt fyrir hvert kort eða mörg kort sem á að vinna með með sömu stillingum. Setja verður upp kort framleiðanda sem eru í boði á markaðnum, svo sem debetkort og kreditkort , áður en hægt er að samþykkja þau sem greiðslu í verslun.
- **Kreditreikningur** – Kreditreikningar sem eru gefnar út eða leystar út á sölustaðnum. Kreditreikningurinn getur kreditreikningur eða skilakreditreikningur sem er gefin út á móti skilavöru. Ef kreditreikningar eru aðeins innleystar að hluta gefur forritið út nýja kreditreikning með nýju númeri fyrir eftirstandandi stöðu. Ný kreditreikningurinn hefur nýtt númer. Aðeins er hægt að nota kreditreikning einu sinni og heldur forritið þá utan um lista yfir öll númer sem eru notuð. Færsluna má skoða á í **kreditreikningstafla** síðu. Viðskiptavinur getur ekki innleyst fleiri en eitt gildi á kreditreikningi.
- **Gjafakort -** Gjafakort sem eru gefin út og leyst út á sölustað. Ofgreiðslur eru ekki leyfðar fyrir gjafakort. Öll gjafakort ættu að vera með kortanúmeravarpanir. 
- **Viðskiptavinalykill** - greiðslur sem má skuldfæra á viðskiptavinalykil við sölu á afgreiðslukassa. Einnig er hægt að nota þennan greiðsluhátt til að safna upplýsingum á sölu eða afslætti fyrir viðskiptavin þegar viðskiptavinur greiðir inn með því að nota annan greiðslumáta. Í því tilfelli verður að skrá upplýsingar um viðskiptavininn.
- **Vildarpunktar** – punktar sem viðskiptavinir safnast upp í vildarkerfi. Ef stofna á vildarkerfi, geta viðskiptavinir unnið inn punkta og innleyst þá á mismunandi vegu. Til dæmis í sumum vildarkerfi, geta viðskiptavinir innleysa vildarpunkta sem afslátt eða jafnvel nota þá sem greiðslu.

Til að setja upp greiðslumáta verður að ljúka eftirtöldu.

1. Setja upp greiðslumáta fyrir fyrirtæki Stofna greiðslumáta sem er viðurkenndir af öllu fyrirtækinu.
2. Stofna kortategundir og kortanúmer fyrir fyrirtækið í heild sinni. Ef taka á við kredit- eða debetkortum þarf að búa til einn greiðslumáta fyrir kort og búa síðan til kortategundir og kortanúmer fyrir fyrirtækið allt.
3. Setja upp greiðsluhætti verslunar. Tengið greiðslumáta við hverja verslun og færið síðan inn stillingar fyrir einstakar verslanir fyrir hvern greiðslumáta verslunar.
4. Setja upp kortagreiðsluhætti fyrir verslanir. Ljúkið kortauppsetningu fyrir alla greiðsluhætti korts sem verslunin tekur á móti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
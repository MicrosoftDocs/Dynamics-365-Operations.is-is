---
title: "Greiðsluhættir"
description: "Verður að skilgreina hverja greiðslugerð sem er retailer samþykkir í Smásölu og commerce í Microsoft Dynamics 365 aðgerða þegar kerfið er sett upp. Þetta grein lýsir þær gerðir greiðslna sem hægt er að setja upp og lýsir ferlinu við uppsetninguna."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: MargoC
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b887fc5d03ea8982515e92725ce98cc416e56f9e
ms.openlocfilehash: 011beec07bf1ab858892ab1c374f1acf3839e877
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods"></a>Greiðsluhættir

Verður að skilgreina hverja greiðslugerð sem er retailer samþykkir í Smásölu og commerce í Microsoft Dynamics 365 aðgerða þegar kerfið er sett upp. Þetta grein lýsir þær gerðir greiðslna sem hægt er að setja upp og lýsir ferlinu við uppsetninguna.

Smásalar geta tekið við ýmsum gerðum af greiðslu í staðinn fyrir afurðir og þjónustu sem þeir selja. Þótt reiðufé er algengasta greiðsluform smásala getur hann einnig þurft að taka við greiðslu í formi ávísana, korta, fylgiskjala og svo framvegis. Verður að skilgreina hverja greiðslugerð sem retailer samþykkir í Dynamics 365 aðgerða - Smásölu þegar kerfið er sett upp. Eftirfarandi listi lýsir hverja greiðslugerð sem hægt er að setja upp í Dynamics 365 aðgerða - Smásölu:

-   **Reiðufé – **Peningar, þ.e. efnislegur gjaldmiðill á borð við seðla og mynt. Gjaldmiðillinn getur verið gjaldmiðill fyrirtækisins eða gjaldmiðill verslunarinnar.
-   **Ávísun – ** Framseljanlegur gerningur sem gefur loforð um greiðslu tiltekinnar upphæðar í tilteknum gjaldmiðli úr tilteknum banka. Ávísun gildir venjulega annaðhvort óráðinn tíma eða í sex mánuði eftir útgáfudag, nema annar gildistímabil er tilgreint. Þetta tímabil er breytileg eftir bankans sem ávísunin er gefin út á. Ýmsar gerðir ávísana eru í boði, á borð við pantanaávísanir, ávísanir á handhafa o.s.frv. Hægt er að setja upp ávísanir sem greiðslumáta fyrir hverja verslun. Ávísanir má samþykkja í þeim gjaldmiðli sem er skilgreind á fyrirtækisstigi eða stigi einstakra verslana. Setja verður upp ávísana sem greiðslumáta áður en hægt er að samþykkja ávísun sem greiðsla í verslun.
-   **Gjaldmiðill – **Algengasta form greiðslna fyrir utan sjálfgefinn gjaldmiðil fyrirtækisins. Mynt og seðlar eru gjaldmiðilsform. Greiðsluháttur gjaldmiðils tekur til alls gjaldmiðils sem er notaður í Smásölu og verslun. Áður en þessi greiðslumáti er notaður þarf að setja upp gjaldmiðla og tilgreina smásöluupplýsingar fyrir gjaldmiðlana.
-   **Kort** – Allar gerðir korta sem notaðar eru í Smásölu og viðskipti, svo sem debetkort og kreditkort. Góð hugmynd er að setja upp einn greiðsluhátt með korti á stigi fyrirtækis, til að sýna hverja tegund korts. Í hverri verslun má síðan setja upp greiðsluhátt fyrir hvert kort eða mörg kort sem á að vinna með með sömu stillingum. Setja verður upp kort framleiðanda sem eru í boði á markaðnum, svo sem debetkort og kreditkort , áður en hægt er að samþykkja þau sem greiðslu í verslun.
-   **Kreditreikningur** – Kreditreikningar sem eru gefnar út eða leystar út á sölustaðnum. Kreditreikningurinn getur kreditreikningur eða skilakreditreikningur sem er gefin út á móti skilavöru. Ef kreditreikningar eru aðeins innleystar að hluta gefur forritið út nýja kreditreikning með nýju númeri fyrir eftirstandandi stöðu. Ný kreditreikningurinn hefur nýtt númer. Aðeins er hægt að nota kreditreikning einu sinni og heldur forritið þá utan um lista yfir öll númer sem eru notuð. Færsluna má skoða á í **kreditreikningstafla** síðu. Viðskiptavinur getur ekki innleyst fleiri en eitt gildi á kreditreikningi.
-   **Gjafakort - ** Gjafakort sem eru gefin út og leyst út á sölustað. Ofgreiðslur eru ekki leyfðar fyrir gjafakort.
-   **Viðskiptavinalykill** - greiðslur sem má skuldfæra á viðskiptavinalykil við sölu á afgreiðslukassa. Einnig er hægt að nota þennan greiðsluhátt til að safna upplýsingum á sölu eða afslætti fyrir viðskiptavin þegar viðskiptavinur greiðir inn með því að nota annan greiðslumáta. Í því tilfelli verður að skrá upplýsingar um viðskiptavininn.
-   **Vildarpunktar** – punkta sem viðskiptavinir safnast upp í vildarkerfi. Ef stofna á vildarkerfi eru viðskiptavini getur unnið inn punkta og innleysa þær á mismunandi vegu. Til dæmis í sumum vildarkerfi, geta viðskiptavinir innleysa vildarpunkta sem afslátt eða jafnvel nota þá sem greiðslu.

Til að setja upp greiðslumáta í Smásölu og viðskipti, verður að ljúka eftirfarandi verkum.

1.  Setja upp greiðslumáta fyrir fyrirtæki Stofna greiðslumáta sem er viðurkenndir af öllu fyrirtækinu.
2.  Stofna póstskipana kortategundir og kortanúmer. Ef kreditkortum eða debetkortum eru samþykkt verður að búa til einn greiðslumáta fyrir kort og búa póstskipana kortategundir og kortanúmer.
3.  Setja upp greiðslumáta verslunar. Tengið greiðslumáta við hverja verslun og færið síðan inn stillingar fyrir einstakar fyrir hvern greiðslumáta.
4.  Setja upp greiðsluhætti korts fyrir verslanir. Ljúkið kortauppsetningu fyrir öll kort greiðslumáta sem verslunin tekur á móti.




---
title: Setja upp valkosti pantanavinnslu
description: "Þetta efni veitir upplýsingar um hvernig á að vinna pantanir fyrir símaver með Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 144bee2102b8d1901d1b4964f6c92501c1cd573d
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-order-processing-options"></a>Uppsetning valkosta pantanavinnslu

[!include[banner](includes/banner.md)]


Þetta efni veitir upplýsingar um hvernig á að vinna pantanir fyrir símaver með Microsoft Dynamics 365 for Retail. 

Retail styður fjölda smásölurása, þ.m.t. netverslanir og verslanir á staðnum og þjónustuver. Í símaverum, starfsmenn taka pantanir viðskiptavina yfir síma og stofna sölupantanir. Þetta efnisatriði lýsir hvernig stofna á símaveri og skilgreina valkosti vinnustöðvar símtalalista. Hvert símaver getur haft eigin notendur, greiðsluhætti, verðflokkar, fjárhagsvíddir og afhendingarmáta. Hægt er að skilgreina valkosti þegar símaver er stofnað. **Mikilvægt:** Áður en hægt er að nota verkflæði símavers þegar notandi stofnar sölupantanir verður að úthluta notanda á símaver sem notanda símavers. Síðuna **símaver** má einnig nota til að kveikja eða slökkva á eiginleikaflokkum sem eru sértækir fyrir símaver. Hægt er að virkja eftirfarandi þrjá flokka eiginleika:

-   **Lok pöntunar**– Þessi flokkur inniheldur eiginleika sem tengjast greiðslum og lokum pöntunar í síðunni **sölupöntun**.
-   **Beind sala**– Þessi flokkur inniheldur aðgerðir sem tengjast frumkóðum, forskriftum og beiðnum um vörulista.

Þegar þessir eiginleikar í stillingum símavers eru virkjaðar, eru þær tiltækar á síðunni **sölupöntun** fyrir notendur sem eru tengdir við símaverið. Flestar þessara aðgerða krefjast frekari uppsetningar áður en hægt er að nota þær. Myndir og forskriftir eru virkjuð sem hluti af stillingum beindar sölu fyrir tilteknar símaveri. Ef þessi aðgerð er virkjuð birtast forskriftir og vörumyndum í rúðu Upplýsingakassa á **sölupöntun** síðu. Sjálfgefin mynd sem er sett upp fyrir afurð er sýnd. Hægt er að skilgreina forskriftir fyrir vöru, vörulista, viðskiptavini eða vöru í vörulista. Símaver geta sýnt nánari upplýsingar um hvernig verð fyrir tilteknar pöntunarlínu var fengin. Til dæmis sýna pantanir hvaða afslættir voru notaðar. Hægt er að virkja þessa aðgerð á **Viðskiptakröfur** &gt; **Uppsetning** &gt; **Færibreytur viðskiptakrafna** &gt; **Verð** &gt; **Upplýsingar um Verð**. Hægt er að nálgast **Verð upplýsingar** síðuna úr **sölupöntunarlína** fellilistanum. Hægt er að nota rakningu pöntunaratburðar fyrir endurskoðunartilgangi, til að fara yfir aðgerðir sem eru teknar gagnvart pöntun á líftíma pöntunar, eða til að rekja aðgerðir af ákveðnum notanda. Til dæmis er hægt að skrá aðgerðina í hvert sinn sem notandi stofnar sölupöntun, setur pöntun í bið, hnekkir gjaldi eða uppfærir pöntunarlínu. Þú getur sett upp röð atburða til að rekja aðgerðir fyrir tiltekna notendur, hópa notenda eða alla notendur á tilteknu tímabili. Hægt er að skoða aðgerðirnar sem voru gerðar í skjal með því að opna **pöntunartilvik** síðuna úr á Aðgerðarúðu á síðunni fyrir það skjal. Hægt er að skilgreina pöntunartilvik á **Sölu og markaðssetningar** &gt; **Uppsetning** &gt; **Tilvik** &gt; **Pöntunartilvik**. Þegar pöntun viðskiptavinar er ekki hægt að senda á réttum tíma getur fyrirtæki sent sjálfkrafa tilkynningapóst til viðskiptavinarins til að útskýra stöðu pöntunar og veita viðskiptavini tækifæri til að hætta við pöntun. Ef seinkun nær fram yfir tilgreindum þröskuldi, hægt að hætta við pöntunina sjálfkrafa. Hægt er að senda allt að þrjú skilaboð í tölvupósti á tilteknum millibili:

1.  **Fyrsta afturköllunartilkynning** – viðskiptavinurinn hætta við pöntunina.
2.  **-Önnur afturköllunartilkynning** – viðskiptavinurinn getur hætta við pöntunina.
3.  **Síðasta afturköllunartilkynning** – kerfið hættir við pöntun, og viðskiptavinurinn fær tilkynningu um afturköllunina..

Hægt er að veita einstökum viðskiptavinum og afurðum undanþágu frá sjálfvirkum tilkynningum og afturköllunarferli. Framlegðarviðvörun er ræst þegar vöru er bætt við pöntun. Viðvörun inniheldur mikilvægar upplýsingar um vöruna, þar á meðal framlegð af verði og arðsemi. Hægt er að nota þessar upplýsingar til að ákveða hvort er verðhnekking er viðeigandi þegar vöru er bætt við sölupöntunina. Til dæmis seturðu upp þröskulda fyrir öryggismörk viðskipta til að tilgreina þröskuldinn 40 prósent eða meira yfir kostnaði er viðunandi fyrir vöru en þröskuld uppá 20 til 39 prósent yfir kostnaður er vafasamt. Í þessu tilfelli, allar vörur sem hefur þröskuldur milli 20 og 39 prósent ræsir viðvörun. Ekki er hægt að selja neinar vörur sem hefur þröskuld fyrir minna en 20 prósent yfir kostnaður, og ekki er hægt að leiðrétta vöruverð. Hægt er að skilgreina framlegðarviðvaranir á **Viðskiptakröfur** &gt; **Uppsetning** &gt; **Færibreytur viðskiptakrafna** &gt; **Framlegðarviðvaranir**. Þegar sett er upp úthlutun vsk á grunn sjálfgefinna reglna, er hægt að ákvarða samsvarandi forgang fyrir aðsetur einingar. Til dæmis er hægt að tilgreina sem samsvörun fyrir vsk-flokk eftir Póstnúmeri hefur er hærri forgang en samsvörun fyrir vsk-flokk eftir ríki. Þegar þú slærð inn skráningar um nýja viðskiptavini, er VSK-flokkur sjálfkrafa úthlutað á grundvelli þess hvernig netfang viðskiptavinarins passar við sjálfgefna samsvörun á reglum og forgangi sem þú tilgreindir. Þessi aðgerð er hægt að skilgreina á **fjárhagsfæribreytur** síðu.




